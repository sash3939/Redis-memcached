# Домашнее задание к занятию «Кеширование Redis/memcached»


### Задание 1. Кеширование 

Приведите примеры проблем, которые может решить кеширование. 

*Приведите ответ в свободной форме.*
---
### Решение 1. Кеширование
1. **Уменьшение нагрузки на базу данных**: Когда приложение часто запрашивает одни и те же данные из базы данных, кеширование позволяет временно хранить результаты запросов в памяти. Это уменьшает количество запросов к базе данных, снижая нагрузку на неё и улучшая производительность приложения.

2. **Улучшение скорости загрузки страниц**: Кеширование может использоваться для кэширования целых страниц или их фрагментов, таких как HTML, CSS, JavaScript. Это позволяет быстрее отображать страницы пользователю, так как сервер может отдавать закэшированные версии вместо генерации их заново.

3. **Снижение задержек в API**: При работе с внешними сервисами или API, кеширование ответов может существенно сократить время ожидания. Если данные редко меняются, их можно закэшировать на определенное время, что снизит частоту обращений к внешним сервисам.

4. **Повышение отказоустойчивости**: Использование кеша может помочь в ситуациях, когда основной источник данных недоступен или медленно отвечает. Если данные уже закэшированы, приложение может использовать их в качестве временной заглушки, обеспечивая непрерывную работу.

5. **Масштабируемость**: Кеширование позволяет снизить нагрузку на основные компоненты приложения, такие как базы данных или внешние API. Это делает приложение более масштабируемым, поскольку кэш можно распределить по нескольким серверам или кластерам.

6. **Улучшение производительности медленных операций**: Если у вас есть операции, которые занимают много времени, кеширование результатов этих операций может значительно ускорить их выполнение.

---

### Задание 2. Memcached

Установите и запустите memcached.

*Приведите скриншот systemctl status memcached, где будет видно, что memcached запущен.*

---

### Задание 3. Удаление по TTL в Memcached

Запишите в memcached несколько ключей с любыми именами и значениями, для которых выставлен TTL 5. 

*Приведите скриншот, на котором видно, что спустя 5 секунд ключи удалились из базы.*

---

### Задание 4. Запись данных в Redis

Запишите в Redis несколько ключей с любыми именами и значениями. 

*Через redis-cli достаньте все записанные ключи и значения из базы, приведите скриншот этой операции.*


## Дополнительные задания (со звёздочкой*)
Эти задания дополнительные, то есть не обязательные к выполнению, и никак не повлияют на получение вами зачёта по этому домашнему заданию. Вы можете их выполнить, если хотите глубже разобраться в материале.

### Задание 5*. Работа с числами 

Запишите в Redis ключ key5 со значением типа "int" равным числу 5. Увеличьте его на 5, чтобы в итоге в значении лежало число 10.  

*Приведите скриншот, где будут проделаны все операции и будет видно, что значение key5 стало равно 10.*
