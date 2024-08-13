# Домашнее задание к занятию 2 «Кеширование Redis/memcached» - `Ханнанов Эльдар`


### Задание 1. Кеширование 

Приведите примеры проблем, которые может решить кеширование. 

*Приведите ответ в свободной форме.*

_**Ответ 1.**_

Основная проблема, которую решает кеширование - производительность. Данные с использованием кеша (например, в RAM) будут читаться из записывать в десятки а может и в сотни раз быстрее, сильно увеличивая общую производительность, сглаживая пики потребления ресурсов, не допускаем перегрузки работы СУБД.

Ещё на ум приходит проблема со сбережением ресурса хранилищ данных. Ресурс записи-чтения ОЗУ несравнимо выше чем у SSD/HDD.  

---

### Задание 2. Memcached

Установите и запустите memcached.

*Приведите скриншот systemctl status memcached, где будет видно, что memcached запущен.*

_**Ответ 2.**_

![](https://github.com/eldarkhan/eldar_khannanov_hw/blob/39aebabdffe2520f36fb634a24a7bbbcfa409745/sdb_HW/2.%20%D0%9A%D0%B5%D1%88%D0%B8%D1%80%D0%BE%D0%B2%D0%B0%D0%BD%D0%B8%D0%B5%20Redis-memcached/img/Redis-memcached-scr-1.png)




### Задание 3. Удаление по TTL в Memcached

Запишите в memcached несколько ключей с любыми именами и значениями, для которых выставлен TTL 5. 

*Приведите скриншот, на котором видно, что спустя 5 секунд ключи удалились из базы.*

_**Ответ 3.**_

![](https://github.com/eldarkhan/eldar_khannanov_hw/blob/39aebabdffe2520f36fb634a24a7bbbcfa409745/sdb_HW/2.%20%D0%9A%D0%B5%D1%88%D0%B8%D1%80%D0%BE%D0%B2%D0%B0%D0%BD%D0%B8%D0%B5%20Redis-memcached/img/Redis-memcached-scr-2.png)


### Задание 4. Запись данных в Redis

Запишите в Redis несколько ключей с любыми именами и значениями. 

*Через redis-cli достаньте все записанные ключи и значения из базы, приведите скриншот этой операции.*

_**Ответ 4.**_

![](https://github.com/eldarkhan/eldar_khannanov_hw/blob/39aebabdffe2520f36fb634a24a7bbbcfa409745/sdb_HW/2.%20%D0%9A%D0%B5%D1%88%D0%B8%D1%80%D0%BE%D0%B2%D0%B0%D0%BD%D0%B8%D0%B5%20Redis-memcached/img/Redis-memcached-scr-3.png)
![](https://github.com/eldarkhan/eldar_khannanov_hw/blob/39aebabdffe2520f36fb634a24a7bbbcfa409745/sdb_HW/2.%20%D0%9A%D0%B5%D1%88%D0%B8%D1%80%D0%BE%D0%B2%D0%B0%D0%BD%D0%B8%D0%B5%20Redis-memcached/img/Redis-memcached-scr-4.png)
