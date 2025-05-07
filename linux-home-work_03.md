# Часть 1
1) Перейти в директорию /opt
2) Не выходя из /opt в директории /home/USER/home_works создать директорию lab_03 (USER - имя вашего пользователя)
3) Не выходя из /opt в директории lab_03 создать директории 
- text_processing
- films
4) Не выходя из /opt в директории films создать директории
- western
- action
- drama
- comedy
5) Перейти в директорию western
6) Не выходя из директории western создать в директории action директорию FastFurious и файлы
- JohnWick
- Gentlemen
7) Не выходя из директории western создать в директории drama файлы
- Intouchables
- TheGreenMile
- Hachi
8) Перейти в директорию films
9) В директории comedy создать директории movies и TVseries
10) В директории movies создать файлы HomeAlone, TheMask
11) В директории TVseries создать файлы Friends, MiracleWorkers, TheOffice
12) Перейти в директорию /etc и не выходя из нее в директории lab_03 создать директорию films_archive
13) Скопировать содержимое директории films в films_archive
14) Переименовать директорию films_archive/western в films_archive/westernCopy
# Часть 2
1) В директории lab_03/text_processing создать файл info.csv с таким содержимым
```
Name:Company:Price:Ganre:Multiplayer
Item1:Company1:60000$:Ganre1:Yes
Item2:Company2:70000$:Ganre2:Yes
Item3:Company3:90000$:Ganre1:Yes
Item4:Company4:90000$:Ganre1:No
Item5:Company5:110000$:Ganre1:Yes
Item6:Company6:410000$:Ganre2:Yes
Item7:Company1:60000$:Ganre1:Yes
Item8:Company4:40000$:Ganre2:No
Item9:Company3:90000$:Ganre1:Yes
```
2) В файле info.csv (с помощью grep) найти строки, которые содержат слово No
3) В файле info.csv найти все строки, в которых встречается слово Ganre2
4) В файле info.csv найти все строки, в которых встречается слово Ganre2 и вывести только 3 поле
5) В директории lab_03/text_processing создать файл metrics с таким содержимым
```
metric_name:metric_type:interval
cache_disk_use:gauge:1
cache_use:gauge:0
key_buffer_bytes_used:byte:3
table.rows.read:count:10
disk_use:gauge:10
data_size:gauge:1
rows_deleted:count:1
bytes_received:byte:1
```
6) В файле metrics найти все строки, в которых встречается слово gauge и вывести только первое поле
7) В файле metrics найти все строки, в которых встречается слово byte и вывести только 3 поле
8) В файле metrics найти все строки, в которых встречается слово disk и вывести только 2 поле
9) В файле metrics найти все строки, которые начинаются с cache
10) В файле info.csv найти все строки, которые содержат слово Company4
11) В директории text_processing создать файл products с содержимым
```
Handle:Title:SKU:Location:On hand:Available:Count
product-1:Product A:PROD-A:Warehouse A:100
product-1:Product A:PROD-A:Warehouse A:50
product-2:Product B:PROD-B:Warehouse B:200
product-2:Product B:PROD-B:Warehouse B:150
product-3:Product C:PROD-C:Warehouse C:300
product-4:Product D:PROD-D:Warehouse A:400
product-4:Product D:PROD-D:Warehouse A:250
product-5:Product E:PROD-E:Warehouse B:500
product-5:Product E:PROD-E:Warehouse B:300
product-6:Product F:PROD-F:Warehouse C:600
product-6:Product F:PROD-F:Warehouse C:400
```
12) Найти в файле products все строки, содержащие слово PROD-C
13) Найти в файле products все строки, содержащие слово product-3 и вывести для них последний столбец
14) Найти в файле products все строки, у которых столбец Available равен 'Warehouse C' и для них вывести первый и последний столбец
15) В директории text_processing создать файл hosts с содержимым
```
hostname,interval,timestamp,%user,%system,%memory
sel-srv1,600,2023-10-08 00:00:01 UTC,30.01,20.77,96.21
sel-srv1,600,2023-10-08 00:05:01 UTC,40.07,13.00,84.55
sel-srv1,600,2023-10-08 00:10:01 UTC,5.00,90.55,89.23
sel-srv2,600,2023-10-09 00:15:01 UTC,25.01,15.77,92.21
sel-srv3,600,2023-10-09 00:20:01 UTC,35.07,10.00,80.55
sel-srv3,600,2023-10-09 00:25:01 UTC,10.00,85.55,88.23
sel-srv2,600,2023-10-09 00:30:01 UTC,20.01,25.77,95.21
sel-srv2,600,2023-10-09 00:35:01 UTC,45.07,12.00,82.55
sel-srv3,600,2023-10-09 00:40:01 UTC,15.00,80.55,87.23
```
16) Найти в файле hosts строки, содержащие sel-srv2 и вывести 3 столбец
17) Найти в файле hosts строки, содержащие дату 2023-10-08
# Часть 3
1) В директории home_works создать директорию roles
2) В директории roles создать директории
- nginx
- docker

и файлы
- inventory
- main.yml
3) В директории nginx создать директории
- handlers
- tasks
- vars
- files
4) В директории nginx/tasks создать файл install.yml с содержимым (*!в директорию nginx НЕ ПЕРЕХОДИТЬ, ОСТАВАТЬСЯ в roles*)
```
---
- name: Install nginx
  apt:
    name: nginx
    state: stable
    update_cahce: yes
```
5) В файл inventory записать следуюущий текст
```
[webservers]
192.168.0.1
```
6) В директории nginx/handlers создать файл main.yml с содержимым
```
---
- name: Restart Nginx
  service:
    name: nginx
    state: restarted
```
7) В директории nginx/vars создать файл main.yml
8) В директории nginx/files создать файл nginx.conf с содержимым
```
user www-data;
pid /var/run/nginx.pid;

events {
        worker_connections 1024;
        # multi_accept on;
}
```
9) В директории home_works создать директорию infrastructure и переместить туда всю директорию roles
10) В директории infrastructure создать директорию tf
11) Переместить файлы inventory и main.yml из директории roles в директорию infrastructure
12) В директории infrastructure/tf создать директории aws и yandex
13) В директориях aws и yandex создать пустой файл main.tf
14) Вывести полученную структуру директорий командой tree
