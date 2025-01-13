# Ansible Playbook: ClickHouse & Vector Install

Плейбук для установки ClickHouse и Vector на ОС Centos 8 и Centos 9

## Требования

Перед началом запуска плейбука, на хостах необходимо выполнить следующие команды

`sed -i 's/mirrorlist/#mirrorlist/g' /etc/yum.repos.d/CentOS-*`

`sed -i 's|#baseurl=http://mirror.centos.org|baseurl=http://vault.centos.org|g' /etc/yum.repos.d/CentOS-*`

## Переменные, используемые в плейбуке

В плейбуке используется ряд переменных. Они находятся в каталоге [group_vars](./group_vars/). При необходимости вы можете изменить следующие переменные:

1. clickhouse_version - версия устанавливаемых пакетов для ClickHouse. По умолчанию устанавливается версия 22.3.7.28
2. clickhouse_packages - список устанавливаемых пакетов. По умолчанию устанавливаются следующие пакеты: clickhouse-client, clickhouse-server и clickhouse-common-static
3. vector_version - по умолчанию будет установлен Vector версии 0.43.1

## Зависимости

Отсутствуют

## Пример для запуска плейбука

`ansible-playbook -i inventory/prod.yml site.yml`

## Лицензия

Нет

## Информация об авторе

Плейбук был написан в рамках учебного задания. Автор широко известен достаточно в узких кругах.

