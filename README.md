# "Работа с git и bash"

Открыть домашнюю директорию через терминал        $ cd 
Определить имя папки, в которой вы находитесь     $ pwd
Создать внутри этой папки каталог с именем test1  $ mkdir test1
Перейти в папку test1                             $ cd test1
Создать файл 1,2 и 3 внутри каталога test1        $ touch 1.txt 2.txt 3.txt
Проверить содержимое каталога test1               $ ls
Перейти в домашнюю директорию                     $ cd ..
Создать папку test2 внутри домашней директории    $ mkdir test2
Удалить папку test2                               $ rmdir test2
Удалить файл 2 из папки test1                     $ rm test1/2.txt
Создать папку в домашней директории test3         $ mkdir test3 
и добавить в нее два файла                          touch test3/1.txt test3/2.txt
Удалить папку test3                               $ rm -r test3
Создать папку test4 в домашней директории         $ mkdir test4
Переместить файлы 1 и 3 из папки                  $ mv test1/1.txt test4/
test1 в папку test4                                 mv test1/3.txt test4/
Добавить в файл 1 три строки со словами line      $ echo "line" >> test4/1.txt
                                                    echo "line" >> test4/1.txt
                                                    echo "line" >> test4/1.txt
Посмотреть содержимое файла 1                     $ cat test4/1.txt
Добавьте в файл 3 три строки со словами line      $ echo "line" >> test4/3.txt
                                                    echo "line" >> test4/3.txt
                                                    echo "line" >> test4/3.txt 
Просмотрите содержимое двух файлов (1 и 3) сразу  $ cat test4/1.txt test4/3.txt
Используя один из редакторов замените             $ nano test4/1.txt
все строки в файле 1


Зайти в домашнюю директорию через терминал.                           $ cd 
Создать папку test 3                                                  $ mkdir test3
Добавить в папку test 3 три файла 4, 5 и 6,                           $ touch test3/{4,5,6}.txt && { echo row1; echo row2; echo row3; echo row4; } | tee test3/{4,5,6}.txt
в каждом из которых должно быть по 4 строки row1, row2, row3, row4 
Найдите строку row2 в файле 5                                         $ grep "row2" test3/5.txt
Найдите строку row в папке test3                                      $ grep -r "row" test3
Посчитайте сколько строк с содержимым row в файле 6                   $ grep -c "row" test3/6.txt
Найдите файл 5 внутри папки test3                                     $ find test3 -name "5.txt"
Используя команду find, удалите файл 5                                $ find test3 -name "5.txt" -delete
Используя команду echo, добавьте слово test                           $ echo "test" > test3/4.txt
в файл 4 (без сохранения содержимого)
Замените слово test в файле 4 на fail                                 $ sed -i 's/test/fail/g' test3/4.txt

Добавьте в файл 4 слово test так, чтобы сохранилось содержимое        $ echo "test" >> test3/4.txt
Просмотрите все процессы для юзеров не только в консоли,              $ ps aux
которые происходят в системе 
Убейте процесс в консоли(можно не убивать, а просто написать команду) $ kill PID
Узнайте доступность ресурса rusau.net, используя ping                 $ ping rusau.net
Отправьте 5 пакетов на сайт rusau.net                                 $ ping -c 5 rusau.net
Используя GET и команду curl, получите информацию о                   $ curl -X GET "https://petstore.swagger.io/v2/pet/findByStatus?status=sold"
зарегистрированных питомцах с любым статусом на 
https://petstore.swagger.io/
Используя POST и команду curl, создайте нового                      $ curl -X POST "https://petstore.swagger.io/v2/user" -H "Content-Type: application/json" -d '{"id": 0, "username": "new", 
пользователя на https://petstore.swagger.io/                          "firstName": "First", "lastName": "Last", "email": "email", "password": "password", "phone": "phone", "userStatus": 0}'





