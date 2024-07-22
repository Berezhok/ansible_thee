



## Домашнее задание к занятию 3 «Использование Ansible»
### Подготовка к выполнению
### Подготовьте в Yandex Cloud три хоста: для clickhouse, для vector и для lighthouse.
### Репозиторий LightHouse находится по ссылке.
### Основная часть
### Допишите playbook: нужно сделать ещё один play, который устанавливает и настраивает LightHouse.
### При создании tasks рекомендую использовать модули: get_url, template, yum, apt.
### Tasks должны: скачать статику LightHouse, установить Nginx или любой другой веб-сервер, настроить его конфиг для открытия LightHouse, запустить веб-сервер.
### Подготовьте свой inventory-файл prod.yml.
### ![](https://github.com/Berezhok/ansible_thee/blob/main/img/playall.png)
### Вроде все прошло
### Запустите ansible-lint site.yml и исправьте ошибки, если они есть.
### ![](https://github.com/Berezhok/ansible_thee/blob/main/img/lint.png)
### Вроде исправили
### Попробуйте запустить playbook на этом окружении с флагом --check.
### Запустите playbook на prod.yml окружении с флагом --diff. Убедитесь, что изменения на системе произведены.
### Повторно запустите playbook с флагом --diff и убедитесь, что playbook идемпотентен.
### Прописали diff и check все норм
### Единственное я прописал хардКод 
### repo: "https://github.com/VKCOM/lighthouse.git"
###        version: master
###        dest: "/usr/share/nginx/html/lighthouse/"
### Не могу понять почему не работает если беру переменные
### lighthouse_vcs: "https://github.com/VKCOM/lighthouse.git"
### lighthous_local_dir: "/usr/share/nginx/html/lighthouse/"
### Подготовьте README.md-файл по своему playbook. В нём должно быть описано: что делает playbook, какие у него есть параметры и теги.
### Готовый playbook выложите в свой репозиторий, поставьте тег 08-ansible-03-yandex на фиксирующий коммит, в ответ предоставьте ссылку на него.
### https://github.com/Berezhok/ansible_thee/releases/tag/08-ansible-03-yandex
### Как оформить решение задания
### Выполненное домашнее задание пришлите в виде ссылки на .md-файл в вашем репозитории.