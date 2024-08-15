# Домашнее задание к занятию 3 «ELK» - `Ханнанов Эльдар`


### Задание 1. Elasticsearch 

Установите и запустите Elasticsearch, после чего поменяйте параметр cluster_name на случайный. 

*Приведите скриншот команды 'curl -X GET 'localhost:9200/_cluster/health?pretty', сделанной на сервере с установленным Elasticsearch. Где будет виден нестандартный cluster_name*.

_**Ответ 1.**_

![](https://github.com/eldarkhan/eldar_khannanov_hw/blob/39aebabdffe2520f36fb634a24a7bbbcfa409745/sdb_HW/2.%20%D0%9A%D0%B5%D1%88%D0%B8%D1%80%D0%BE%D0%B2%D0%B0%D0%BD%D0%B8%D0%B5%20Redis-memcached/img/Redis-memcached-scr-4.png)

---

### Задание 2. Kibana

Установите и запустите Kibana.

*Приведите скриншот интерфейса Kibana на странице http://<ip вашего сервера>:5601/app/dev_tools#/console, где будет выполнен запрос GET /_cluster/health?pretty*.

_**Ответ 2.**_

![](https://github.com/eldarkhan/eldar_khannanov_hw/blob/39aebabdffe2520f36fb634a24a7bbbcfa409745/sdb_HW/2.%20%D0%9A%D0%B5%D1%88%D0%B8%D1%80%D0%BE%D0%B2%D0%B0%D0%BD%D0%B8%D0%B5%20Redis-memcached/img/Redis-memcached-scr-4.png)

---

### Задание 3. Logstash

Установите и запустите Logstash и Nginx. С помощью Logstash отправьте access-лог Nginx в Elasticsearch. 

*Приведите скриншот интерфейса Kibana, на котором видны логи Nginx.*

_**Ответ 3.**_

![](https://github.com/eldarkhan/eldar_khannanov_hw/blob/39aebabdffe2520f36fb634a24a7bbbcfa409745/sdb_HW/2.%20%D0%9A%D0%B5%D1%88%D0%B8%D1%80%D0%BE%D0%B2%D0%B0%D0%BD%D0%B8%D0%B5%20Redis-memcached/img/Redis-memcached-scr-4.png)


---

### Задание 4. Filebeat. 

Установите и запустите Filebeat. Переключите поставку логов Nginx с Logstash на Filebeat. 

*Приведите скриншот интерфейса Kibana, на котором видны логи Nginx, которые были отправлены через Filebeat.*

_**Ответ 4.**_

![](https://github.com/eldarkhan/eldar_khannanov_hw/blob/39aebabdffe2520f36fb634a24a7bbbcfa409745/sdb_HW/2.%20%D0%9A%D0%B5%D1%88%D0%B8%D1%80%D0%BE%D0%B2%D0%B0%D0%BD%D0%B8%D0%B5%20Redis-memcached/img/Redis-memcached-scr-4.png)
