

### PostgreSQL

[Linux Mint 20.x Ubuntu-based / Can't install pgadmin4](https://stackoverflow.com/questions/68777587/linux-mint-20-x-ubuntu-based-cant-install-pgadmin4)


### Команды управления сервисом
`service postgesql`

### Работа через терминал
При установке СУБД соддается суперпользователь postgres

#### Входим в учетную запись
`sudo -i -u postgres`

#### Открываем консоль postgres
`psql`

#### Базовые команды
`\l #выводит список баз данных`

`q #выйти назад`

#### Выйходим из консоли перед создание базы данных
`\q`

`createdb bot #создает базу данных с названием bot`

`dropdb bot #удаляет базу данных с названием bot`

`\du #отображает пользователей`

`ALTER USER postgres WITH PASSWORD `qwerty`; #изменить пароль пользователя USER на qwerty`

`CREATE USER yu WITH PASSWORD '0';`
`ALTER USER yu WITH SUPERUSER; #даем пользователю yu права суперпользователя`
`DROP USER yu; #удалить пользователя yu`
`\q #выходим из консоли`
`exit or CTRL + D #выходим из учетной записи`
`sudo -i -u postgres`
`man psql #мануал psql`











`






 


 

 