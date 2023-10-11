# Setevoe_Programmirovanie
Laba1 Данная программа запрашивает у пользователя его имя и выводит приветственное сообщение с этим именем. Затем программа находит имя ПК, IP-адрес и MAC-адрес ПК и выводит их на экран.

Для работы с сетью используется модуль socket, для генерации уникального идентификатора ПК - модуль uuid.

Пример использования:

What's your name? John Hello, John PC name: DESKTOP-ABC123 IP address: 192.168.1.10 MAC address: 00:11:22:33:44:55

Laba2Client.py

Программа для отправки сообщения на сервер
Данная программа использует библиотеку socket для создания TCP-сокета и отправки сообщения на сервер.

Пример использования:

Импортируем библиотеку socket
import socket

Создаем TCP-сокет
sock = socket.socket(socket.AF_INET, socket.SOCK_STREAM)

Запрашиваем у пользователя IP-адрес и порт сервера
print('Введите IP-адрес сервера:') ip = input() print('Введите порт сервера:') port = int(input())

Устанавливаем соединение с сервером
sock.connect((ip, port))

Запрашиваем у пользователя сообщение для отправки на сервер
print('Введите сообщение для отправки на сервер:') message = input()

Кодируем сообщение в байты с использованием кодировки UTF-8 и отправляем через сокет
sock.send(bytes(message, encoding='UTF-8'))

Закрываем сокет
sock.close()

Программа запрашивает у пользователя IP-адрес и порт сервера, а также сообщение для отправки. Затем она устанавливает соединение с сервером, кодирует сообщение в байты с помощью кодировки UTF-8 и отправляет его через сокет. После этого сокет закрывается.

Laba2Server.py Данная программа использует библиотеку socket для создания TCP-сокета и отправки сообщения на сервер.

Использование
Запустите программу.
Введите IP-адрес сервера и порт, к которому нужно подключиться.
Введите сообщение для отправки на сервер.
Нажмите Enter.
Пример
Write IP address of Server: 192.168.0.1 Write Port of Server: 8080 Write the massage you want to send: Hello, server!

Описание
Программа запрашивает у пользователя IP-адрес и порт сервера, а также сообщение для отправки. Затем она устанавливает соединение с сервером, кодирует сообщение в байты с помощью кодировки UTF-8 и отправляет его через сокет. После этого сокет закрывается.

Laba2_2Client.py

Программа для отправки файла на сервер
Данная программа использует библиотеку socket для создания TCP-сокета и отправки файла на сервер.

Использование
Запустите программу.
Укажите IP-адрес сервера и порт, к которому нужно подключиться.
Укажите имя файла, который нужно отправить на сервер.
Нажмите Enter.
Пример
Write IP address of Server: 192.168.0.1 Write Port of Server: 8080 Write the file name you want to send: 1.txt

Описание
Программа запрашивает у пользователя IP-адрес и порт сервера, а также имя файла для отправки. Затем она устанавливает соединение с сервером, отправляет имя файла в виде байтовой строки с помощью кодировки UTF-8 и открывает файл на чтение в бинарном режиме. Далее программа читает файл блоками по 1024 байта и отправляет их через сокет, пока не достигнет конца файла. После этого сокет закрывается.

Обратите внимание, что перед запуском программы нужно убедиться, что файл существует в указанной директории и у пользователя есть права на его чтение.

Laba2_2Server.py

Программа для отправки файла на сервер
Данная программа использует библиотеку socket для создания TCP-сокета и отправки файла на сервер.

Использование
Запустите программу.
Укажите IP-адрес сервера и порт, к которому нужно подключиться.
Укажите имя файла, который нужно отправить на сервер.
Нажмите Enter.
Пример
Write IP address of Server: 192.168.0.1 Write Port of Server: 8080 Write the file name you want to send: 1.txt

Описание
Программа запрашивает у пользователя IP-адрес и порт сервера, а также имя файла для отправки. Затем она устанавливает соединение с сервером, отправляет имя файла в виде байтовой строки с помощью кодировки UTF-8 и открывает файл на чтение в бинарном режиме. Далее программа читает файл блоками по 1024 байта и отправляет их через сокет, пока не достигнет конца файла. После этого сокет закрывается.

Обратите внимание, что перед запуском программы нужно убедиться, что файл существует в указанной директории и у пользователя есть права на его чтение.

Для запуска программы на сервере:
Сохраните программу на сервере.
Установите IP-адрес сервера и порт, к которому нужно подключиться.
Запустите программу.
Ожидайте подключения клиента.
Для запуска программы на клиенте:
Сохраните программу на клиенте.
Установите IP-адрес сервера и порт, к которому нужно подключиться.
Установите имя файла, который нужно отправить на сервер.
Запустите программу.
Ожидайте сообщения о получении файла на сервере.
Важно: перед запуском программы убедитесь, что на сервере и клиенте установлен Python и библиотека socket.

Laba3.py

Описание программы для получения расписания с сайта БИИК СибГУТИ
Данная программа использует библиотеку requests для отправки запроса на сайт БИИК СибГУТИ и получения расписания.

Использование
Запустите программу.
Программа отправит запрос на сайт БИИК СибГУТИ и получит расписание.
Расписание будет выведено на экран.
Пример
Вторник, 23.02.2021

Время Группа Предмет Преподаватель Аудитория 09:00-10:30 CG109 Математика Иванов И.И. А-101 10:40-12:10 CG109 Физика Петров П.П. А-102 12:20-13:50 CG109 Информатика Сидоров С.С. А-103

Описание
Программа отправляет запрос на сайт БИИК СибГУТИ и получает ответ в виде HTML-страницы. Затем она использует метод encoding для указания кодировки страницы и выводит полученный текст на экран.

Обратите внимание, что программа выводит расписание только на текущий день. Если нужно получить расписание на другой день, то нужно изменить URL запроса в соответствии с требуемой датой.

Для запуска программы:
Сохраните программу на своем компьютере.
Запустите программу.
Расписание будет выведено на экран.
Важно: перед запуском программы убедитесь, что у вас установлена библиотека requests. Если она не установлена, то можно установить ее с помощью pip: pip install requests

Laba4.py

Описание программы для получения расписания с сайта БИИК СибГУТИ
Данная программа использует библиотеку requests для отправки запроса на сайт БИИК СибГУТИ и получения расписания. Затем она использует библиотеку BeautifulSoup для парсинга HTML-кода страницы и извлечения нужных данных.

Использование
Запустите программу.
Программа отправит запрос на сайт БИИК СибГУТИ и получит расписание.
Расписание будет выведено на экран.
Пример
Вторник, 23.02.2021

Время Группа Предмет Преподаватель Аудитория 09:00-10:30 CG109 Математика Иванов И.И. А-101 10:40-12:10 CG109 Физика Петров П.П. А-102 12:20-13:50 CG109 Информатика Сидоров С.С. А-103

Описание
Программа отправляет запрос на сайт БИИК СибГУТИ и получает ответ в виде HTML-страницы. Затем она использует библиотеку BeautifulSoup для парсинга HTML-кода страницы и извлечения нужных данных.

Обратите внимание, что программа выводит расписание только на текущий день. Если нужно получить расписание на другой день, то нужно изменить URL запроса в соответствии с требуемой датой.

Для запуска программы:
Сохраните программу на своем компьютере.
Установите библиотеки requests и BeautifulSoup с помощью команды pip install requests beautifulsoup4.
Запустите программу.
Расписание будет выведено на экран.
Laba5.py

Описание программы для получения файла с FTP-сервера
Данная программа использует модуль ftplib для установления соединения с FTP-сервером и получения файла с сервера.

Использование
Запустите программу.
Программа установит соединение с FTP-сервером ftp.gnu.org и авторизуется на нем.
Задайте путь и имя файла, который нужно получить с FTP-сервера.
Файл будет получен и сохранен по указанному пути.
Пример
Путь и имя файла: /root/recieve/tree.json.gz Файл успешно получен и сохранен по указанному пути.

Описание
Программа устанавливает соединение с FTP-сервером ftp.gnu.org и авторизуется на нем. Затем она использует метод retrbinary для получения файла с сервера и записи его содержимого в открытый файл.

Обратите внимание, что для успешного получения файла нужно знать его путь и имя на FTP-сервере. Если вы не знаете эти данные, то обратитесь к администратору сервера.

Для запуска программы:
Сохраните программу на своем компьютере.
Запустите программу.
Укажите путь и имя файла, который нужно получить с FTP-сервера.
Файл будет получен и сохранен по указанному пути.
