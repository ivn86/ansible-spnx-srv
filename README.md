spnx-srv
========
Эта роль устанавливает серверную часть ПО [СКУД Сфинкс](http://www.spnx.ru).

Требования
==========
Требуется Ansible версии не ниже 1.3 и Debian GNU/Linux (тестировал на Debian Wheezy).

Переменные
==========
Рекомендуется переопределить значения учётной записи mysql для пользователя Сфинкс:

    spnx_mysql_user: "spnx"
    spnx_mysql_password: "s0mePa$$word"

Возможно установить значения URL-адресов, если имеются копии программ:

    spnx_server_url: "http://some_local_repository/spnxserver_1.0.56.1-0_i386.deb"
    hasp_drv_url: "http://some_local_repository/aksusbd_7.32-1_i386.deb"

Пример
======

    - hosts: spnx-server
      remote_user: root
      roles:
      - ivn86.spnx-srv

Зависимости
===========
ivn86.spnx-cln

Лицензия
========
MIT

Информация об авторе
====================
[Жаренков Иван](https://www.zharenkov.ru). Считаю необходимым отметить, что не имею отношения к компании "ПромАвтоматика" и ПО "Сфинкс".
