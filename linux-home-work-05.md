0) Создать
- пользователей user-1, user-2, student-1, student-2
- группы developers, designers, admins (команда `groupadd`)
Добавить
- в группу developers пользователей user-1 и student-1
- в группу designers пользователей user-2 и student-2
1) В директории /opt создать директорию magento
2) В директории magento создать директории media, code и styles
3) В директории code создать файл index.php с содержимым
```
<?php
phpinfo();
?>
```
4) В директории styles создать файл main.css с содержимым
```
h1 {
    color: #333; /* Цвет текста */
    text-align: center; /* Выравнивание по центру */
}
```
5) В директории magento создать файл index.html с содержимым
```
<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>E-commerce page</title>
    <link rel="stylesheet" href="styles.css"> <!-- Подключаем CSS -->
</head>
<body>
    <header>
        <h1>Welcome!</h1>
        <h2>e-commerce site</h2>
    </header>
```
6) Сделать владельцем файла index.html пользователя user-2, а группой владельцев - группу developers
7) Сделать владельцем файла styles/main.css пользователя student-1, а группой владельцев - группу designers
