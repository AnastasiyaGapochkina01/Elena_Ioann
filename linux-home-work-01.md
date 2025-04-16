1) В домашнем каталоге создать директорию home_works, в ней - директорию lab_01.
2) В lab_01 создать директории task_01, task_02 и task_03 и файл readme.md с содержимым
```
# Learn Linux project
## Chapter 01: Simplets actions
```
3) В task_01 создать файлы 
- app.py с содержимым
```
print("Hello from LInux")
```
- config.py с содержимым
```
import os

class Config:
    SQLALCHEMY_DATABASE_URI = os.environ.get('DATABASE_URL') or 'postgresql://user:password@db/bookstore'
    SQLALCHEMY_TRACK_MODIFICATIONS = False

```
4) В директории task_02 создать файл users с содержимым
```
root,www-data,admin,developer,qa,manager
```
5) Скопировать в директорию task_03 все файлы из директорий task_01 и task_02
6) Переименовать файл app.py в директории task_03 в server.py
7) В директории task_03 создать директорию part-1 и переместить туда все файлы, которые были в task_03
8) В директории task_03 создать директорию part-2. В part-2 создать директорию college
9) В директории college создать директории groups, students, lecturers
10) В директории groups создать файл group_list с содержимым
```
dvps-36
back-87
dba-05
```
11) В директории groups создать директории dvps-36, back-87, dba-05. В каждой из этих директорий создать файл students_list с произвольным списком слушателей курса (3-4 студента)
12) В директории students создать файл all_list, который будет содержать всех студентов
13) В директории lecturers создать файл list с с произвольным списком лекторов и предметов, которые они преподают
14) В директории part-2 создать директорию college_bkp
15) Скопировать содержимое всей директории college в college_bkp
16) Переименовать college_bkp в college_archive
