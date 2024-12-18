# Домашнее задание к занятию «SQL. Часть 2» - Ханнанов Эльдар

---

Задание можно выполнить как в любом IDE, так и в командной строке.

### Задание 1

Одним запросом получите информацию о магазине, в котором обслуживается более 300 покупателей, и выведите в результат следующую информацию: 
- фамилия и имя сотрудника из этого магазина;
- город нахождения магазина;
- количество пользователей, закреплённых в этом магазине.


```SQL
SELECT CONCAT(s2.first_name, ' ', s2.last_name) AS Name, a.address AS Address, COUNT(c.store_id) AS Customers
FROM store s 
JOIN customer c ON s.store_id = c.store_id 
JOIN staff s2 ON s.manager_staff_id = s2.staff_id 
JOIN address a ON s.address_id = a.address_id 
GROUP BY c.store_id 
HAVING COUNT(c.store_id) > 300;
```

![1](https://github.com/eldarkhan/eldar_khannanov_hw/blob/026f9f6e466dd5275d53d97f9253877ffe482923/khannanov_sdb_hw/4.%20SQL.%20%D0%A7%D0%B0%D1%81%D1%82%D1%8C%202/img/Eldar-SDBSQL-lesson4-scr1.jpg)



### Задание 2

Получите количество фильмов, продолжительность которых больше средней продолжительности всех фильмов.


```SQL
SELECT (SELECT  AVG(`length`) from film) AS Average, (SELECT COUNT(1) from film) AS 'All films', COUNT(1) AS 'Long Films'
FROM film 
WHERE `length` > (SELECT AVG(`length`) from film) ;
```

![2](https://github.com/eldarkhan/eldar_khannanov_hw/blob/026f9f6e466dd5275d53d97f9253877ffe482923/khannanov_sdb_hw/4.%20SQL.%20%D0%A7%D0%B0%D1%81%D1%82%D1%8C%202/img/Eldar-SDBSQL-lesson4-scr2.jpg)

---


### Задание 3

Получите информацию, за какой месяц была получена наибольшая сумма платежей, и добавьте информацию по количеству аренд за этот месяц.


```SQL
SELECT MONTH(payment_date) AS Month, COUNT(payment_id) As Payments, SUM(amount) AS Amount
FROM payment
GROUP BY MONTH(payment_date) 
ORDER BY COUNT(payment_id)  DESC LIMIT 1 ;
```

![3](https://github.com/eldarkhan/eldar_khannanov_hw/blob/026f9f6e466dd5275d53d97f9253877ffe482923/khannanov_sdb_hw/4.%20SQL.%20%D0%A7%D0%B0%D1%81%D1%82%D1%8C%202/img/Eldar-SDBSQL-lesson4-scr3.jpg)
