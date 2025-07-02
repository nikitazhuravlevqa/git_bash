# Работа с git и bash
## ЗАДАЧА 1
# 1. Предварительно создайте файл bash1.txt, в который вы будете добавлять выполненные команды  
touch bash1.txt

# 2. Открыть домашнюю директорию через терминал  
cd

# 3. Определить имя папки, в которой вы находитесь  
pwd

# 4. Создать внутри этой папки каталог с именем test1  
mkdir test1

# 5. Перейти в папку test1  
cd test1

# 6. Создать файл 1, 2 и 3 внутри каталога test1  
touch 1 2 3

# 7. Проверить содержимое каталога test1  
ls

# 8. Перейти в домашнюю директорию  
cd

# 9. Создать папку test2 внутри домашней директории  
mkdir test2

# 10. Удалить папку test2  
rmdir test2

# 11. Удалить файл 2 из папки test1  
rm test1/2

# 12. Создать папку в домашней директории test3 и добавить в нее два файла  
cd  
mkdir test3  
cd test3  
touch 1 2

# 13. Удалить папку test3  
rm -r test3

# 14. Создать папку test4 в домашней директории  
mkdir test4

# 15. Переместить файлы 1 и 3 из папки test1 в папку test4  
mv test1/1 test4  
mv test1/3 test4

# 16. Добавить в файл 1 три строки со словами line  
echo line >> test4/1  
echo line >> test4/1  
echo line >> test4/1

# 17. Посмотреть содержимое файла 1  
cd  
cat test4/1

# 18. Добавьте в файл 3 три строки со словами line  
echo line >> test4/3  
echo line >> test4/3  
echo line >> test4/3

# 19. Просмотрите содержимое двух файлов (1 и 3) сразу  
cat test4/1 test4/3

# 20. Используя один из редакторов замените все строки в файле 1  
nano test4/1

## ЗАДАЧА 2

# 1. Предварительно создайте файл bash2.txt, в который вы будете добавлять выполненные команды
touch bash2.txt

# 2. Зайти в домашнюю директорию через терминал
cd

# 3. Создать папку test3
mkdir test3

# 4. Перейти в папку test3, создать файлы 4, 5 и 6 и добавить в каждый по 4 строки row1, row2, row3, row4
cd test3
touch 4 5 6

echo row1 >> 4
echo row1 >> 5
echo row1 >> 6

echo row2 >> 4
echo row2 >> 5
echo row2 >> 6

echo row3 >> 4
echo row3 >> 5
echo row3 >> 6

echo row4 >> 4
echo row4 >> 5
echo row4 >> 6

# 5. Найти строку row2 в файле 5
grep row2 test3/5

# 6. Найти строки с текстом row в папке test3
grep row test3/*

# 7. Посчитать количество строк с текстом row в файле 6
grep -c row test3/6

# 8. Найти файл с именем 5 внутри папки test3
find test3 -name 5

# 9. Найти и удалить файл 5 в папке test3 с помощью find
find test3 -name 5 -type f -exec rm {} \;

# 10. Добавить слово test в файл 4 (перезаписать содержимое)
echo test > test3/4

# 11. Заменить слово test на fail в файле 4
echo fail > test3/4

# 12. Добавить слово test в файл 4, сохраняя содержимое
echo test >> test3/4

# 13. Просмотреть все процессы в системе (включая процессы других пользователей)
ps aux

# 14. Команда для завершения процесса с PID 666 (не обязательно выполнять)
kill 666

# 15. Проверить доступность ресурса rusau.net с помощью ping
ping rusau.net

# 16. Отправить 5 пакетов на сайт rusau.net
ping -c 5 rusau.net

# 17. Получить информацию о зарегистрированных питомцах со статусом sold с помощью curl (GET)
curl https://petstore.swagger.io/v2/pet/findByStatus?status=sold

# 18. Создать нового пользователя с помощью curl (POST)
curl -X POST "https://petstore.swagger.io/v2/user" \
  -H "accept: application/json" \
  -H "Content-Type: application/json" \
  -d '{
  "id": 0,
  "category": {
    "id": 0,
    "name": "string"
  },
  "name": "doggie",
  "photoUrls": [
    "string"
  ],
  "tags": [
    {
      "id": 0,
      "name": "string"
    }
  ],
  "status": "available"
}'
