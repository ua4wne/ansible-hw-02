# Ansible Playbook: ClickHouse & Vector Install & LightHouse

Плейбук для установки ClickHouse, Vector и LightHouse на ОС Ubuntu

## Требования

ОС Ubuntu

## Переменные, используемые в плейбуке

В плейбуке используется ряд переменных. Они находятся в каталоге [group_vars](./group_vars/). При необходимости вы можете изменить следующие переменные:

1. clickhouse_version - версия устанавливаемых пакетов для ClickHouse. По умолчанию устанавливается версия 22.3.8.39
2. clickhouse_packages - список устанавливаемых пакетов. По умолчанию устанавливаются следующие пакеты: clickhouse-client, clickhouse-server и clickhouse-common-static
3. vector_version - по умолчанию будет установлен Vector версии 0.43.1
4. repo_url - ссылка на репозиторий LightHouse. По умолчанию "https://github.com/VKCOM/lighthouse"
5. lighthouse_nginx_user - пользователь, от имени которого будет запущен nginx. По умолчанию установлен root
6. lighthouse_dir - директория, куда будет скачан репозиторий LightHouse. По умолчанию "/var/www/lhouse"

## Зависимости

Отсутствуют

## Пример для запуска плейбука

`ansible-playbook -i inventory/prod.yml site.yml`

## Лицензия

Нет

## Информация об авторе

Плейбук был написан в рамках учебного задания. Автор широко известен достаточно в узких кругах.

