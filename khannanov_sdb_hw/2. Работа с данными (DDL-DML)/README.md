# Домашнее задание к занятию «Работа с данными (DDL/DML)» - Ханнанов Эльдар


### Задание 1
1.1. Поднимите чистый инстанс MySQL версии 8.0+. Можно использовать локальный сервер или контейнер Docker.

1.2. Создайте учётную запись sys_temp. 

1.3. Выполните запрос на получение списка пользователей в базе данных. (скриншот)

![](https://github.com/eldarkhan/eldar_khannanov_hw/blob/5f1389c0f2d9272ce4b56b13c2658fa89fa3340a/khannanov_sdb_hw/2.%20%D0%A0%D0%B0%D0%B1%D0%BE%D1%82%D0%B0%20%D1%81%20%D0%B4%D0%B0%D0%BD%D0%BD%D1%8B%D0%BC%D0%B8%20(DDL-DML)/IMG/SDBSQL-leeson2-scr-1.jpg)

1.4. Дайте все права для пользователя sys_temp. 

1.5. Выполните запрос на получение списка прав для пользователя sys_temp. (скриншот)


![](https://github.com/eldarkhan/eldar_khannanov_hw/blob/5f1389c0f2d9272ce4b56b13c2658fa89fa3340a/khannanov_sdb_hw/2.%20%D0%A0%D0%B0%D0%B1%D0%BE%D1%82%D0%B0%20%D1%81%20%D0%B4%D0%B0%D0%BD%D0%BD%D1%8B%D0%BC%D0%B8%20(DDL-DML)/IMG/SDBSQL-leeson2-scr-2.jpg)

1.6. Переподключитесь к базе данных от имени sys_temp.

Для смены типа аутентификации с sha2 используйте запрос: 
```sql
ALTER USER 'sys_test'@'localhost' IDENTIFIED WITH mysql_native_password BY 'password';
```
1.6. По ссылке https://downloads.mysql.com/docs/sakila-db.zip скачайте дамп базы данных.

1.7. Восстановите дамп в базу данных.

1.8. При работе в IDE сформируйте ER-диаграмму получившейся базы данных. При работе в командной строке используйте команду для получения всех таблиц базы данных. (скриншот)

![](https://github.com/eldarkhan/eldar_khannanov_hw/blob/5f1389c0f2d9272ce4b56b13c2658fa89fa3340a/khannanov_sdb_hw/2.%20%D0%A0%D0%B0%D0%B1%D0%BE%D1%82%D0%B0%20%D1%81%20%D0%B4%D0%B0%D0%BD%D0%BD%D1%8B%D0%BC%D0%B8%20(DDL-DML)/IMG/SDBSQL-leeson2-scr-3.jpg)

*Результатом работы должны быть скриншоты обозначенных заданий, а также простыня со всеми запросами.*

***Список команд:***
```

sudo apt update
sudo apt install mysql-server mysql-client
sudo mysql_secure_installation
sudo mysql -u root -p

CREATE USER 'sys_temp'@'localhost' IDENTIFIED BY 'password';
SELECT user,authentication_string,plugin,host FROM mysql.user;
GRANT ALL PRIVILEGES ON *.* TO 'sys_temp'@'localhost';
SHOW GRANTS for 'sys_temp'@'localhost';
exit
mysql -u sys_temp -p
exit

wget https://downloads.mysql.com/docs/sakila-db.zip
unzip sakila-db.zip

mysql -u sys_temp -p
CREATE DATABASE `sakila`;
SHOW DATABASES;
exit

cd sakila-db/

mysql -u sys_temp -p sakila < sakila-schema.sql
mysql -u sys_temp -p sakila < sakila-data.sql

mysql -u sys_temp -p
SHOW DATABASES;
USE sakila;
SHOW TABLES;
```


### Задание 2
Составьте таблицу, используя любой текстовый редактор или Excel, в которой должно быть два столбца: в первом должны быть названия таблиц восстановленной базы, во втором названия первичных ключей этих таблиц. Пример: (скриншот/текст)
```
Название таблицы | Название первичного ключа
customer         | customer_id
```
## Ответ к заданию 2

![](https://github.com/eldarkhan/eldar_khannanov_hw/blob/293307c9707732e8cf6f2d4f6224e170e771f8f7/khannanov_sdb_hw/2.%20%D0%A0%D0%B0%D0%B1%D0%BE%D1%82%D0%B0%20%D1%81%20%D0%B4%D0%B0%D0%BD%D0%BD%D1%8B%D0%BC%D0%B8%20(DDL-DML)/IMG/SDBSQL-leeson2-scr-4.jpg)

```
+---------------+--------------+
| TABLE_NAME    | COLUMN_NAME  |
+---------------+--------------+
| actor         | actor_id     |
| address       | address_id   |
| category      | category_id  |
| city          | city_id      |
| country       | country_id   |
| customer      | customer_id  |
| film          | film_id      |
| film_actor    | actor_id     |
| film_actor    | film_id      |
| film_category | film_id      |
| film_category | category_id  |
| film_text     | film_id      |
| inventory     | inventory_id |
| language      | language_id  |
| payment       | payment_id   |
| rental        | rental_id    |
| staff         | staff_id     |
| store         | store_id     |
+---------------+--------------+

```
