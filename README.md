## Задача 1

1. Создайте в старой версии playbook файл requirements.yml и заполните его содержимым:

`
---
  - src: git@github.com:AlexeySetevoi/ansible-clickhouse.git
    scm: git
    version: "1.13"
    name: clickhouse 
`
2. При помощи ansible-galaxy скачайте себе эту роль.

>`ansible-galaxy install -r requirements.yml -p roles`

3. Создайте новый каталог с ролью при помощи ansible-galaxy role init vector-role.

>`ansible-galaxy role init vector-role`

4. На основе tasks из старого playbook заполните новую role. Разнесите переменные между vars и default.
5. Перенести нужные шаблоны конфигов в templates.
6. Опишите в README.md обе роли и их параметры. Пример качественной документации ansible role по ссылке.
7. Повторите шаги 3–6 для LightHouse. Помните, что одна роль должна настраивать один продукт.

>`ansible-galaxy role init lighthouse-role`

8. Выложите все roles в репозитории. Проставьте теги, используя семантическую нумерацию. Добавьте roles в requirements.yml в playbook.

`git tag -a 08-ansible-03-yandex -m "08-ansible-03-yandex"`

`git push origin 08-ansible-03-yandex`

>[vector role](https://github.com/ua4wne/vector-role)
>[lighthouse role](https://github.com/ua4wne/lighthouse-role)
>[requirements.yml](./requirements.yml)

9. Переработайте playbook на использование roles. Не забудьте про зависимости LightHouse и возможности совмещения roles с tasks.

[install_roles](./task3/roles.png)

>Ответ: [site.yml](./site.yml)

10. Выложите playbook в репозиторий.

11. В ответе дайте ссылки на оба репозитория с roles и одну ссылку на репозиторий с playbook.