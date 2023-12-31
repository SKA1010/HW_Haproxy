# Домашнее задание к занятию 2 «Кластеризация и балансировка нагрузки» Sychugov Konstantin

### Цель задания
В результате выполнения этого задания вы научитесь:
1. Настраивать балансировку с помощью HAProxy
2. Настраивать связку HAProxy + Nginx

------

### Задание 1
- Запустите два simple python сервера на своей виртуальной машине на разных портах
- Установите и настройте HAProxy, воспользуйтесь материалами к лекции
- Настройте балансировку Round-robin на 4 уровне.
- На проверку направьте конфигурационный файл haproxy, скриншоты, где видно перенаправление запросов на разные серверы при обращении к HAProxy.

------

### Решение 1

Установил haproxy, настроил конфиг на баллансировку на порты 8888 и 9999, на которых работает python сервер.

![1-1](https://github.com/SKA1010/HW_Haproxy/assets/125235217/9c9a279f-fb09-47db-b0d6-b4b6aa1ddfff)

------


### Задание 2
- Запустите три simple python сервера на своей виртуальной машине на разных портах
- Настройте балансировку Weighted Round Robin на 7 уровне, чтобы первый сервер имел вес 2, второй - 3, а третий - 4
- HAproxy должен балансировать только тот http-трафик, который адресован домену example.local
- На проверку направьте конфигурационный файл haproxy, скриншоты, где видно перенаправление запросов на разные серверы при обращении к HAProxy c использованием домена example.local и без него.

### Решение 2

Изменили конфиг, добавили "вес" серверам и добавили третий сервер
Скриншот, обращения к узлу по имени:

![2-1](https://github.com/SKA1010/HW_Haproxy/assets/125235217/bce0f0a1-3f35-485e-a3b0-94ad08ff8f06)

Скриншот, обращения к узлу по адресу:

![2-2](https://github.com/SKA1010/HW_Haproxy/assets/125235217/8d134e2b-17e5-4032-8f16-799194830311)



---
