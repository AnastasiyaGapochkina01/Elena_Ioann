# Часть 1
1) В директории lab_02 создать директорию college
2) В директории college создать директории groups, students, academic_subjects, lecturers
3) Перейти в директорию groups
4) В директории groups создать файл group_list с содержимым
```
dvps-36
back-87
dba-05
```
4) В директории groups создать директории dvps-36, back-87, dba-05
5) Не выходя из groups, в директории dvps-36 создать файл students_list с содержимым
```
1 Stepanov V.D.
2 Kozlov A.K.
3 Perepelitsa F.R.
```
6) Не выходя из groups, в директории back-87 создать файл students_list с содержимым
```
1 Petrov A.V.
2 Kuznetsov A.F.
3 Mikhaylov S.T.
```
7) Не выходя из groups, в директории dba-05 создать файл students_list с содержимым
```
1 Mendeleev G.F.
2 Foltz R.
3 Alekhin A.A.
```
8) В директории students создать файл all_list с содержимым
```
1 Stepanov V.D.
2 Kozlov A.K.
3 Perepelitsa F.R.
4 Petrov A.V.
5 Kuznetsov A.F.
6 Mikhaylov S.T.
7 Mendeleev G.F.
8 Foltz R.
9 Alekhin A.A.
```
9) В директории academic_subjects создать директории programming, operating_systems, electrical_engineering
10) В директории lecturers создать файл list с содержимым
```
Kotov A.S.
Rebrov K.F.
Tokarev R.R
```
11) В директории college создать директорию backups
12) В директории academic_subjects/programming создать директорию python
13) В директории academic_subjects/operating_systems создать директорию linux
14) В директории academic_subjects/electrical_engineering создать файлы first_level, second_level, third_level
15) В директории academic_subjects/programming/python создать файл plan с содержимым
```
Intro
Base syntax
Strings
Packages and modules
Lists
Files
```
16) В директории academic_subjects/operating_systems/linux создать файл plan
```
Intro
Files and directories
```
17) Вывести полученную структуру каталогов и файлов командой ```tree -a```
# Часть 2
1) В директории lab_02 создать директорию seaport; перейти в директорию /var
3) Не выходя из /var в директории seaport создать директории departments, areas, journal_lists
4) Перейти в директорию journal_lists и не выходя из нее в директории departments создать файл dep_list с содержимым
```
1. Pilotage service
2. Traffic management service
3. Tugboat service
4. Hydrographic service
5. Emergency rescue service
6. Security service
```
5) Не выходя из journal_lists в директории areas создать файл area_list с содержимым
```
1. An external raid
2. Internal raid
3. Gateways
4. Mooring lines
5. Warehouses
6. Administrative and industrial buildings
7. Ship repair area
```
6) В директории journal_lists создать файл с именем copy_list 
7) Вывести полученную структуру командой tree
8) Перейти в /etc и не выходя из нее в lab_02 создать директорию seaport_backup
9) Перейти в свою домашнюю директорию и скопировать _содержимое_ seaport в seaport_backup
10) В home_works создать директорию backups
11) Переместить seaport_backup в backups
12) Переименовать seaport_backup в copy_seaport 
13) Создать файл list_of_bk в директории home_works и записать в него вывод команды ```ls -1 backups```
14) Скопировать файл list_of_bk в директорию journal_lists
