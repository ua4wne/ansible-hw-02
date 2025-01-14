## Задача 1

1. Допишите playbook: нужно сделать ещё один play, который устанавливает и настраивает LightHouse.
2. При создании tasks рекомендую использовать модули: get_url, template, yum, apt.
3. Tasks должны: скачать статику LightHouse, установить Nginx или любой другой веб-сервер, настроить его конфиг для открытия LightHouse, запустить веб-сервер.

>Ответ: [site.yml](./site.yml)

4. Подготовьте свой inventory-файл prod.yml.

>Ответ: [prod.yml](./inventory/prod.yml)

5. Запустите ansible-lint site.yml и исправьте ошибки, если они есть.

>Ошибок нет

![lint_ok](task1/lint_ok.png)

6. Попробуйте запустить playbook на этом окружении с флагом --check.

![play_check](task2/play_check1.png)
![play_check](task2/play_check1_1.png)

7. Запустите playbook на prod.yml окружении с флагом --diff. Убедитесь, что изменения на системе произведены.

![diff1_1](task2/diff1_1.png)
![diff1_2](task2/diff1_2.png)
![diff1_3](task2/diff1_3.png)

8. Повторно запустите playbook с флагом --diff и убедитесь, что playbook идемпотентен.

![diff2_1](task2/diff2_1.png)
![diff2_2](task2/diff2_2.png)

9. Подготовьте README.md-файл по своему playbook. В нём должно быть описано: что делает playbook, какие у него есть параметры и теги.

>Файл [README.md](./README.md), скриншоты разместил выше по тексту.

10. Готовый playbook выложите в свой репозиторий, поставьте тег 08-ansible-03-yandex на фиксирующий коммит, в ответ предоставьте ссылку на него.

`git tag -a 08-ansible-03-yandex -m "08-ansible-03-yandex"`

`git push origin 08-ansible-03-yandex`