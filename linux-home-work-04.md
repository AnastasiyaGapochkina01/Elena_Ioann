1) В директории /home/USER/home_works создать директорию `lab_04` (USER - имя вашего пользователя)
2) В директории `lab_04` создать директорию complex_texts
3) В директории `complex_texts` создать файл `python.log` с содержимым
```
2024-11-09 08:00:01,123 - myapp - INFO - The application is running.
2024-11-09 08:00:01,456 - myapp - DEBUG - Configuration initialization...
2024-11-09 08:00:01,789 - myapp - INFO - Database connection...
2024-11-09 08:00:02,012 - myapp - WARNING - Database is not responding, retry after 5 seconds.
2024-11-09 08:00:07,345 - myapp - ERROR - Failed to connect to the database: Timeout expired.
2024-11-09 08:00:07,678 - myapp - INFO - Shutdown of the application.
2024-10-31 04:43:12,591 - DEBUG - User logged in
2024-10-31 04:43:12,591 - - INFO - Warning: Low memory
2024-10-31 04:43:12,592 - - INFO - Error: Failed to connect to the database
2024-10-31 04:43:12,591 - - WARNING - Data retrieved successfully
2024-10-31 04:43:12,591 - - app1 - DEBUG - Critical error: System failure
2024-10-31 04:43:12,591 - app1 - ERROR - Application started
```
Необходимо из файла `python.log`:
- вывести все записи, содержащие ERROR и вывести для них время и сообщение об ошибке
- вывести записи, содержащие Database (в любом регистре) и получить из них только уровень лога
- найти записи о неудачном подключении к базе данных
- найти записи, у которых отсутствует поле с именем приложения
4) В директории complex_texts создать файл `searchd.log` с содержимым
```
2024-11-09 08:00:01: [INFO] Sphinx 3.0.3 started
2024-11-09 08:00:01: [INFO] listening on 127.0.0.1:9306
2024-11-09 08:00:01: [INFO] listening on 127.0.0.1:9312
2024-11-09 08:00:01: [INFO] using config file '/home/user/sphinxdata/sphinx.conf'
2024-11-09 08:00:02: [DEBUG] starting indexer process
2024-11-09 08:00:02: [INFO] indexing index 'my_index'
2024-11-09 08:00:02: [INFO] collected 5000 documents, 1.2 MB
2024-11-09 08:00:02: [INFO] sorted 0.5 Mhits, 100.0% done
2024-11-09 08:00:02: [INFO] total indexed documents: 5000
2024-11-09 08:00:02: [INFO] total time spent indexing: 2.3 sec
2024-11-09 08:00:03: [WARNING] failed to open pid_file '/home/user/sphinxdata/searchd.pid'
2024-11-09 08:00:04: [ERROR] unable to connect to MySQL server at 'localhost': Access denied for user 'root'@'localhost' (using password: YES)
2024-11-09 08:00:05: [INFO] searchd stopped
```
Необходимо из файла `searchd.log`:
- найти записи, содержащие listening и вывести хост и порт
- найти все записи уровня error
5) Получить из вывода команды free -h размер доступной памяти (available)
6) Получить из вывода команды lscpu количество ядер
7) В директории complex_texts создать файл `nginx.log` с содержимым
```
192.168.1.100 - - [06/Nov/2024:08:30:15 +0300] "GET /index.html HTTP/1.1" 200 1234 "http://example.com" "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/118.0.0.0 Safari/537.36"
203.0.113.5 - - [06/Nov/2024:08:30:16 +0300] "POST /api/login HTTP/1.1" 401 173 "-" "PostmanRuntime/7.29.2"
10.0.0.1 - - [06/Nov/2024:08:30:17 +0300] "GET /images/logo.png HTTP/1.1" 304 0 "http://example.com/about" "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/605.1.15 (KHTML, like Gecko) Version/16.1 Safari/605.1.15"
192.168.1.101 - - [06/Nov/2024:08:30:18 +0300] "GET /css/style.css HTTP/1.1" 200 4321 "http://example.com" "Mozilla/5.0 (iPhone; CPU iPhone OS 16_1 like Mac OS X) AppleWebKit/605.1.15 (KHTML, like Gecko) Version/16.1 Mobile/15E148 Safari/604.1"
203.0.113.10 - - [06/Nov/2024:08:30:19 +0300] "GET /api/users HTTP/1.1" 403 234 "-" "curl/7.68.0"
192.168.1.102 - - [06/Nov/2024:08:30:20 +0300] "GET /blog HTTP/1.1" 301 0 "-" "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/118.0.0.0 Safari/537.36"
10.0.0.2 - - [06/Nov/2024:08:30:21 +0300] "GET /favicon.ico HTTP/1.1" 404 555 "http://example.com" "Mozilla/5.0 (X11; Ubuntu; Linux x86_64; rv:109.0) Gecko/20100101 Firefox/119.0"
192.168.1.103 - - [06/Nov/2024:08:30:22 +0300] "POST /contact HTTP/1.1" 200 678 "http://example.com/contact" "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/118.0.0.0 Safari/537.36"
203.0.113.15 - - [06/Nov/2024:08:30:23 +0300] "GET /admin HTTP/1.1" 302 0 "-" "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/118.0.0.0 Safari/537.36"
203.0.113.10 - - [06/Nov/2024:10:30:15 +0300] "POST /api/login HTTP/1.1" 401 173 "-" "Mozilla/5.0 (iPhone; CPU iPhone OS 17_1 like Mac OS X) AppleWebKit/605.1.15 (KHTML, like Gecko) Version/17.1 Mobile/15E148 Safari/604.1"
```
Необходимо из файла `nginx.log`:
- найти записи, содержащие "/api/login"
- найти POST запросы и вывести их код ответа
8) В директории complex_texts создать файл `apps.log` с содержимым
```
2024-10-27 08:15:23 INFO [Server] Application started successfully
2024-10-27 08:17:45 DEBUG [UserService] User login attempt: john_doe@example.com
2024-10-27 08:17:46 INFO [UserService] User john_doe@example.com logged in successfully
2024-10-27 08:20:12 WARN [DatabaseService] High database load detected
2024-10-27 08:22:30 ERROR [PaymentService] Transaction failed for user: alice@example.com
2024-10-27 08:22:31 INFO [PaymentService] Retrying transaction for alice@example.com
2024-10-27 08:22:32 INFO [PaymentService] Transaction successful for alice@example.com
2024-10-27 08:25:00 DEBUG [CacheService] Cache hit ratio: 0.75
2024-10-27 08:35:15 INFO [BackupService] Daily backup started
2024-10-27 08:35:22 ERROR [NetworkService] Connection timeout: 192.168.1.105
2024-10-27 08:35:25 WARN [NetworkService] Retrying connection to 192.168.1.105
2024-10-27 08:35:30 INFO [NetworkService] Connection established with 192.168.1.105
2024-10-27 08:40:00 DEBUG [MemoryManager] Current memory usage: 2.5GB
2024-10-27 08:45:12 INFO [UpdateService] Checking for system updates
2024-10-27 08:45:15 INFO [UpdateService] No new updates available
2024-10-27 08:50:30 WARN [SecurityService] Multiple failed login attempts for user: eve@example.com
2024-10-27 08:50:35 ERROR [SecurityService] Account locked: eve@example.com
2024-10-27 08:55:00 INFO [MonitoringService] All systems operating normally
2024-10-27 09:00:00 INFO [SchedulerService] Running hourly tasks
2024-10-27 09:05:23 DEBUG [APIService] API request received from 10.0.0.15
2024-10-27 09:05:24 ERROR [APIService] Invalid API key from 10.0.0.15
2024-10-27 09:10:00 INFO [LoadBalancer] Traffic distribution: Server1: 40%, Server2: 35%, Server3: 25%
2024-10-27 09:15:30 WARN [DiskService] Low disk space on /dev/sda1: 85% used
2024-10-27 09:20:00 INFO [BackupService] Daily backup completed successfully
2024-10-27 09:25:45 DEBUG [CacheService] Cache invalidation triggered
2024-10-27 09:30:00 INFO [ReportGenerator] Monthly report generation started
```
Необходимо из файла `apps.log`:
- найти все ошибки и вывести к какому сервису они относятся
- найти строки, относящиеся к PaymentService и вывести из этих строк только email
- найти записи о запросах к APIService и вывести с каких ip были запросы
- найти записи о backup и вывести время, когда бэкап запустился и когда завершился
9) Из вывода команды `df -Th` получить размер корневой ФС
10) Выполнить команду lsmem (она выводит информацию о памяти) и из ее вывода найти значение Total online memory
11) В файле `/etc/ssh/sshd_config` найти строку, содержащую PasswordAuthentication
12) Вывести файл `/etc/ssh/sshd_config` без комментариев
13) В файле `/proc/filesystems` найти все записи, содержащие ext
14) Выяснить, существует ли файл `/etc/resolv.conf`, если да, то получить из него значение domain
15) Выяснить, существует ли в директории /etc файл ntp.conf, если да, то вывести его содержимое , исключив все строки комментариев (начинающиеся с #) и найти строки начинающиеся с pool
16) Из файла `/etc/passwd` получить имена и id пользователей
17) Из вывода команды `printenv` получить значение переменной USER
