[TOC]

Базовая конфигурация.
=====================

Указанные в данной конфигурации пакеты устанавливаются на все хосты, равно как и настройки применяются также на всех хостах. Список ПО зависит только от типа хоста: контейнер, виртуалка, железный хост.

## Базовый список ПО:

Приведённый в этом разделе список устанавливается на все, без исключения, хосты. Тут нет управления сетью, утилит диагностики аппаратных средств, загрузчика и ядра, т.к. все эти функции выполняются хост-системой.

### Системные утилиты:

* bash-completion
* sudo (необходимо описать требования: кто имеет доступ, откуда берётся информация)
* wipe

### Архиваторы:

* bzip2
* gzip
* p7zip
* tar
* unrar

### Редакторы и сопровождающие пакеты:

* vim
* vim-spell-en
* vim-spell-ru

### Диагностика системы:

* strace
* lsof

### Диагностика сети:

* traceroute
* tcpdump
* bind-tools
* telnet-bsd
* net-tools

Помимо перечисленных выше наименований пакетов необходимо устанавливать агент мониторинга MTA (в режиме только отправки диагностических сообщений внутри корпоративной сети).

## Виртуалки.

Для виртуалок добавляется загрузчик и специализированное ПО для взаимодействия с гипервизором (зависит от гипервизора).

### Системное ПО.

grub
kernel
linux-firmware

### Сетевые утилиты/сервисы.

NetworkManager

## Железные хосты.

В список ПО для разворачивания на железных хостах добавляются утилиты диагностики аппаратуры:
lm-sensors
smartmontools