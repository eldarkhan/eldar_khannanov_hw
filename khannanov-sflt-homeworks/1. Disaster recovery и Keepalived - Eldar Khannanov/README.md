# Домашнее задание к занятию 1 «Disaster recovery и Keepalived» - `Ханнанов Эльдар`


### Задание 1

**Что нужно сделать:**

- Дана [схема](1/hsrp_advanced.pkt) для Cisco Packet Tracer, рассматриваемая в лекции.
- На данной схеме уже настроено отслеживание интерфейсов маршрутизаторов Gi0/1 (для нулевой группы)
- Необходимо аналогично настроить отслеживание состояния интерфейсов Gi0/0 (для первой группы).
- Для проверки корректности настройки, разорвите один из кабелей между одним из маршрутизаторов и Switch0 и запустите ping между PC0 и Server0.
- На проверку отправьте получившуюся схему в формате pkt и скриншот, где виден процесс настройки маршрутизатора.

---
# Решение задания 1:
[Ссылка на .pkt](https://github.com/eldarkhan/eldar_khannanov_hw/blob/7e576e4efa4de05cde413fae071a2dbf5b724b5a/khannanov-sflt-homeworks/1.%20Disaster%20recovery%20%D0%B8%20Keepalived%20-%20Eldar%20Khannanov/img/hsrp_advanced_eldar.pkt)
 

![Скрин 1](https://github.com/eldarkhan/eldar_khannanov_hw/blob/7e576e4efa4de05cde413fae071a2dbf5b724b5a/khannanov-sflt-homeworks/1.%20Disaster%20recovery%20%D0%B8%20Keepalived%20-%20Eldar%20Khannanov/img/hw-1-scr-1.PNG)

![Скрин 2](https://github.com/eldarkhan/eldar_khannanov_hw/blob/7e576e4efa4de05cde413fae071a2dbf5b724b5a/khannanov-sflt-homeworks/1.%20Disaster%20recovery%20%D0%B8%20Keepalived%20-%20Eldar%20Khannanov/img/hw-1-scr-2.PNG)

![Скрин 3](https://github.com/eldarkhan/eldar_khannanov_hw/blob/7e576e4efa4de05cde413fae071a2dbf5b724b5a/khannanov-sflt-homeworks/1.%20Disaster%20recovery%20%D0%B8%20Keepalived%20-%20Eldar%20Khannanov/img/hw-1-scr-3.PNG)

---

### Задание 2

**Что нужно сделать:**

- Запустите две виртуальные машины Linux, установите и настройте сервис Keepalived как в лекции, используя пример конфигурационного [файла](1/keepalived-simple.conf).
- Настройте любой веб-сервер (например, nginx или simple python server) на двух виртуальных машинах
- Напишите Bash-скрипт, который будет проверять доступность порта данного веб-сервера и существование файла index.html в root-директории данного веб-сервера.
- Настройте Keepalived так, чтобы он запускал данный скрипт каждые 3 секунды и переносил виртуальный IP на другой сервер, если bash-скрипт завершался с кодом, отличным от нуля (то есть порт веб-сервера был недоступен или отсутствовал index.html). Используйте для этого секцию vrrp_script
- На проверку отправьте получившейся bash-скрипт и конфигурационный файл keepalived, а также скриншот с демонстрацией переезда плавающего ip на другой сервер в случае недоступности порта или файла index.html


---
# Решение задания 2:

[Баш скрипт](https://github.com/eldarkhan/eldar_khannanov_hw/blob/2bff3c1eeffe9a3e12052be97e1b63eb464f8e2f/khannanov-sflt-homeworks/1.%20Disaster%20recovery%20%D0%B8%20Keepalived%20-%20Eldar%20Khannanov/eldar-keepalived.sh)

[Конфиг keepalived](https://github.com/eldarkhan/eldar_khannanov_hw/blob/2bff3c1eeffe9a3e12052be97e1b63eb464f8e2f/khannanov-sflt-homeworks/1.%20Disaster%20recovery%20%D0%B8%20Keepalived%20-%20Eldar%20Khannanov/keepalived.conf)
 

![Скрин 1](https://github.com/eldarkhan/eldar_khannanov_hw/blob/c89371bbc37d70fe452d15941ad38aa003bc9c50/khannanov-sflt-homeworks/1.%20Disaster%20recovery%20%D0%B8%20Keepalived%20-%20Eldar%20Khannanov/img/hw-1-scr-4.png)

![Скрин 2](https://github.com/eldarkhan/eldar_khannanov_hw/blob/c89371bbc37d70fe452d15941ad38aa003bc9c50/khannanov-sflt-homeworks/1.%20Disaster%20recovery%20%D0%B8%20Keepalived%20-%20Eldar%20Khannanov/img/hw-1-scr-5.png)

![Скрин 3](https://github.com/eldarkhan/eldar_khannanov_hw/blob/c89371bbc37d70fe452d15941ad38aa003bc9c50/khannanov-sflt-homeworks/1.%20Disaster%20recovery%20%D0%B8%20Keepalived%20-%20Eldar%20Khannanov/img/hw-1-scr-6.png)
