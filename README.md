# Операционные системы и виртуализация (Linux) (семинары)

## Урок 1. Установка ОС Ubuntu в виртуальной машине. Работа в SSH-клиенте

### Условие

• Установить Ubuntu Desktop 22.04 в виртуальную машину.
• Установить гостевые дополнения ОС.
• Установить Midnight Commander.
• Установить SSH-соединение с виртуальной машиной из хостовой.

Результат

Скриншот SSH-подключения к установленной системе с запущенным mc.


## Урок 2. Работа с файлами и ссылками

• Используя команду cat, создать два файла с данными, а затем объединить их.
Просмотреть содержимое созданного файла.
Переименовать файл, дав ему новое имя.

• Создать несколько файлов.
Создать директорию, переместить файл туда.
Удалить все созданные в этом и предыдущем задании директории и файлы.

• Создать файл file1 и наполнить его произвольным содержимым.
Скопировать его в file2.
Создать символическую ссылку file3 на file1.
Создать жёсткую ссылку file4 на file1.
Посмотреть, какие айноды у файлов.
Удалить file1.
Что стало с остальными созданными файлами?
Попробовать вывести их на экран.

• Дать созданным файлам другие, произвольные имена.
Создать новую символическую ссылку.
Переместить ссылки в другую директорию.


## Урок 3. Права доступа и безопасность

• Создать два произвольных файла.
Первому присвоить права на чтение и запись для владельца и группы, только на чтение — для всех.
Второму присвоить права на чтение и запись только для владельца. Сделать это в численном и символьном виде.
Назначить новых владельца и группу для директории целиком.

### Управление пользователями:
* создать пользователя, используя утилиту useradd и adduser;
* удалить пользователя, используя утилиту userdel.

### Управление группами:

создать группу с использованием утилит groupadd и addgroup;
попрактиковаться в смене групп у пользователей;
добавить пользователя в группу, не меняя основной;
• Создать пользователя с правами суперпользователя. Сделать так, чтобы sudo не требовал пароль для выполнения команд.

### Дополнительные (необязательные) задания

• Используя дополнительные материалы, выдать одному из созданных пользователей право на выполнение ряда команд, требующих прав суперпользователя (команды выбираем на своё усмотрение).

• Создать группу developer и нескольких пользователей, входящих в неё.
Создать директорию для совместной работы.
Сделать так, чтобы созданные одними пользователями файлы могли изменять другие пользователи этой группы.

• Создать в директории для совместной работы поддиректорию для обмена файлами, но чтобы удалять файлы могли только их создатели.

• Создать директорию, в которой есть несколько файлов.
Сделать так, чтобы открыть файлы можно было, только зная имя файла, а через ls список файлов посмотреть было нельзя.


## Урок 4. Подключение сторонних репозиториев, ручная установка пакетов

• Подключить дополнительный репозиторий на выбор: Docker, Nginx, Oracle MySQL. Установить любой пакет из этого репозитория.

• Установить и удалить deb-пакет с помощью dpkg.

• Установить и удалить snap-пакет.

• Добавить задачу для выполнения каждые 3 минуты (создание директории, запись в файл).

•* Подключить PPA-репозиторий на выбор. Установить из него пакет. Удалить PPA из системы.

•* Создать задачу резервного копирования (tar) домашнего каталога пользователя. Реализовать с использованием пользовательских crontab-файлов.


## Урок 5. Настройка сети в Linux. Работа с IPtables


• Настроить статическую конфигурацию (без DHCP) в Ubuntu через ip и netplan.
Настроить IP, маршрут по умолчанию и DNS-сервера (1.1.1.1 и 8.8.8.8).
Проверить работоспособность сети.

• Настроить правила iptables для доступности сервисов на TCP-портах 22, 80 и 443.
Также сервер должен иметь возможность устанавливать подключения к серверу обновлений.
Остальные подключения запретить.

• Запретить любой входящий трафик с IP 3.4.5.6.

•* Запросы на порт 8090 перенаправлять на порт 80 (на этом же сервере).

•* Разрешить подключение по SSH только из сети 192.168.0.0/24.

## Урок 6. Запуск стека для веб-приложения

### Задание

• Установить Nginx и настроить его на работу с PHP-FPM.

• Установить Apache. Настроить обработку PHP. Добиться одновременной работы с Nginx.

• Настроить схему обратного прокси для Nginx (динамика - на Apache).

• Установить MySQL. Создать новую базу данных и таблицу в ней.

•* Установить пакет phpmyadmin и запустить его веб-интерфейс для управления MySQL.

•* Настроить схему балансировки трафика между несколькими серверами Apache на стороне Nginx с помощью модуля ngx_http_upstream_module.

## Урок 7. Запуск веб-приложения из контейнеров
### Задание

• Установить в виртуальную машину или VDS Docker, настроить набор контейнеров через docker compose по инструкции.
Часть с настройкой certbot и HTTPS опустить, если у вас нет настоящего домена и белого IP.

• Запустить два контейнера, связанные одной сетью (используя документацию).
Первый контейнер БД (например, образ mariadb:10.8), второй контейнер — phpmyadmin.
Получить доступ к БД в первом контейнере через второй контейнер (веб-интерфейс phpmyadmin).

### Результат

Текст команд, которые применялись при выполнении задания.
При наличии: часть конфигурационных файлов, которые решают задачу.
Скриншоты результата запуска контейнеров (веб-интерфейс).
Присылаем в формате текстового документа: задание и команды для решения (без вывода).
Формат — PDF (один файл на все задания).

## Урок 8. Скрипты Bash
### Задание

• Написать скрипт очистки директорий.
На вход принимает путь к директории.
Если директория существует, то удаляет в ней все файлы с расширениями .bak, .tmp, .backup.
Если директории нет, то выводит ошибку.

• Создать скрипт ownersort.sh, который в заданной папке копирует файлы в директории, названные по имени владельца каждого файла.
Учтите, что файл должен принадлежать соответствующему владельцу.

### Результат

Код скриптов в текстовом виде (каждый скрипт в отдельном файле).
Кодировка файлов UTF-8.

Данная промежуточная аттестация оценивается по системе «зачёт» / «не зачёт»
— «Зачёт» ставится, если Слушатель успешно выполнил задание 1 или 2 задания
— «Незачёт» ставится, если Слушатель не выполнил задание.

### Критерии оценивания

1 — Слушатель написал скрипт очистки директорий
2 — Слушатель создал скрипт ownersort.sh