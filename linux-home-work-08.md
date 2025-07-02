# Работа с процессами
> [!NOTE]  
> Изучить:
> 1) Приоритеты процессов
> 2) Сигналы и утилита `kill` 

1) Вывести список всех процессов; вывести список процессов в виде дерева
2) Найти в списке процессов свою ssh сессию; для найденного процесса вывести PPID, PID и COMM
3) Выполнить команду `sleep 15000 &` и найти в списке процессов процесс `sleep`; "убить" процесс (команда `kill`)
4) С помощью `ps` вывести топ-5 процессов, потребляющих
- cpu
- mem
5) В домашней директории создать директориюю `artifical_processes`; в этой директории создать файл `web-server.sh` с содержимым
```bash
#!/bin/bash
LOG_FILE="$HOME/web_server.log"
log_levels=("ERROR" "INFO" "WARNING" "DEBUG")
methods=("GET" "POST" "PUT" "PATCH" "OPTIONS" "DELETE")
echo "Starting web-server on $(hostname)" >> $LOG_FILE
while true
do
  sleep 5
  random_method=${methods[$RANDOM % ${#methods[@]}]}
  random_level=${log_levels[$RANDOM % ${#log_levels[@]}]}
  echo "$(date +"%Y-%d-%m [%H:%M:%S]") $random_level $random_method" >> $LOG_FILE
  sleep 5
done
```
6) Сделать файл `web-server.sh` исполняемым и запустить в фоновом режиме: `./web_server.sh &> /dev/null &`
7) Найти в списке процессов запущенный в п6 скрипт, вывести его PPID, PID, NICE, COMM
8) Приостановить процесс `web-server.sh` и посмотреть, есть ли в директории `artifical_processes` файл `web_server.log`. Если файл есть, то посмотреть его содержимое
9) Возобновить процесс `web-server.sh`
10) "Убить" процесс `web-server.sh`
11) Установить на ВМ nginx, если еще не установлен; найти все процессы nginx и с помощью wc посчитать их количество
