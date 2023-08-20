# Домашнее задание к занятию "`Система мониторинга Prometheus. Часть 2`" - `Викулов Александр`

### Задание 1

Процесс выполнения

1. Создадим файл с правилом в папке `/etc/prometheus`

<p></p>
<kbd>
  <img src="https://github.com/AleksandrVikulov/08-05-prometheus-part-02/blob/master/img/task01-img01.png">
</kbd>
<p></p>

2. Пропишем правило в созданном файле

<p></p>
<kbd>
  <img src="https://github.com/AleksandrVikulov/08-05-prometheus-part-02/blob/master/img/task01-img02.png">
</kbd>
<p></p>

3. Добавим правило в конфигурационный файл `prometheus.yml`

<p></p>
<kbd>
  <img src="https://github.com/AleksandrVikulov/08-05-prometheus-part-02/blob/master/img/task01-img03.png">
</kbd>
<p></p>

4. Перезапустим Prometheus и проверим, что всё работает.

<p></p>
<kbd>
  <img src="https://github.com/AleksandrVikulov/08-05-prometheus-part-02/blob/master/img/task01-img04.png">
</kbd>
<p></p>

5. Видим, что правило добавилось в Prometheus

<p></p>
<kbd>
  <img src="https://github.com/AleksandrVikulov/08-05-prometheus-part-02/blob/master/img/task01-img05.png">
</kbd>
<p></p>

6. Выключим Node Exporter и увидим, что оповещение перешло в статус `PENDING`

<p></p>
<kbd>
  <img src="https://github.com/AleksandrVikulov/08-05-prometheus-part-02/blob/master/img/task01-img06.png">
</kbd>
<p></p>

---

### Задание 2

Процесс выполнения

1. Скачиваем Alertmanager.

<p></p>
<kbd>
  <img src="https://github.com/AleksandrVikulov/08-05-prometheus-part-02/blob/master/img/task02-img01.png">
</kbd>
<p></p>

2. Разархивируем.

<p></p>
<kbd>
  <img src="https://github.com/AleksandrVikulov/08-05-prometheus-part-02/blob/master/img/task02-img02.png">
</kbd>
<p></p>

3. Скопируем файлы Alertmanager'а в нужные папки:

    * Файлы `alermanager` и `amtool` в папку `/usr/local/bin`
    * Кофигурационный файл `alermanager.yml` в папку `/etc/prometheus`

<p></p>
<kbd>
  <img src="https://github.com/AleksandrVikulov/08-05-prometheus-part-02/blob/master/img/task02-img03.png">
</kbd>
<p></p>

4. Передадим права на эти файлы пользователю `prometheus`

<p></p>
<kbd>
  <img src="https://github.com/AleksandrVikulov/08-05-prometheus-part-02/blob/master/img/task02-img04.png">
</kbd>
<p></p>

5. Создадим файл с сервисом Alertmanager

<p></p>
<kbd>
  <img src="https://github.com/AleksandrVikulov/08-05-prometheus-part-02/blob/master/img/task02-img05.png">
</kbd>
<p></p>

6. Пропишем в файле код сервиса

<p></p>
<kbd>
  <img src="https://github.com/AleksandrVikulov/08-05-prometheus-part-02/blob/master/img/task02-img06.png">
</kbd>
<p></p>

7. Добавим сервис в автозагрузку, запустим и проверим, что всё работает.

<p></p>
<kbd>
  <img src="https://github.com/AleksandrVikulov/08-05-prometheus-part-02/blob/master/img/task02-img07-1.png">
</kbd>
<p></p>

<p></p>
<kbd>
  <img src="https://github.com/AleksandrVikulov/08-05-prometheus-part-02/blob/master/img/task02-img07-2.png">
</kbd>
<p></p>

8. Теперь интегрируем Alertmanager и Prometheus.
   Для этого добавим соответствующие инструкции в конфигурационный файл `/etc/prometheus/prometheus.yml`

<p></p>
<kbd>
  <img src="https://github.com/AleksandrVikulov/08-05-prometheus-part-02/blob/master/img/task02-img08.png">
</kbd>
<p></p>

9. Перезапустим Prometheus и убедимся, что всё работает

<p></p>
<kbd>
  <img src="https://github.com/AleksandrVikulov/08-05-prometheus-part-02/blob/master/img/task02-img09.png">
</kbd>
<p></p>

10. Изменим настройки конфигурационного файла для работы с оповещениями

<p></p>
<kbd>
  <img src="https://github.com/AleksandrVikulov/08-05-prometheus-part-02/blob/master/img/task02-img10.png">
</kbd>
<p></p>

11. Перезапустим Prometheus и убедимся, что всё работает

<p></p>
<kbd>
  <img src="https://github.com/AleksandrVikulov/08-05-prometheus-part-02/blob/master/img/task02-img11.png">
</kbd>
<p></p>

12. Отключим Node Exporter и убедимся, что он отключился

<p></p>
<kbd>
  <img src="https://github.com/AleksandrVikulov/08-05-prometheus-part-02/blob/master/img/task02-img12.png">
</kbd>
<p></p>

13. Подождем минуту и увидим, что оповещение в Prometheus перешло в статус `Firing`

<p></p>
<kbd>
  <img src="https://github.com/AleksandrVikulov/08-05-prometheus-part-02/blob/master/img/task02-img13.png">
</kbd>
<p></p>

14. Перейдем в Alertmanager и увидим оповещение об отключении хоста

<p></p>
<kbd>
  <img src="https://github.com/AleksandrVikulov/08-05-prometheus-part-02/blob/master/img/task02-img14.png">
</kbd>
<p></p>

---

### Задание 3

Процесс выполнения

1.

2.

3.

4.

5.

6.

7.

8.

9.

10.

---

## Дополнительные задания (со звездочкой*)

Эти задания дополнительные (не обязательные к выполнению) и никак не повлияют на получение вами зачета по этому домашнему заданию. Вы можете их выполнить, если хотите глубже и/или шире разобраться в материале.

### Задание 4*

1.

2.

3.

4.

5.

6.

7.

8.

9.

10.
