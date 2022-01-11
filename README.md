__Задание по терминалу линукс__ - [HW_1](https://github.com/AndreiHeranok/Linux_terminal/blob/main/HW_1.txt)

__Задание по GitHub_1__  - [github_HW_1](https://github.com/AndreiHeranok/Linux_terminal/blob/main/github_HW_1.txt)
___

__Linux terminal (GitBash) commands__

1) Посмотреть где я            ```pwd```
2) Создать папку               ```mkdir coursKsendzoff/```
3) Зайти в папку               ```cd coursKsendzoff/```
4) Создать 3 папки             ```mkdir hw_1 hw_2 hw_3```
5) Зайти в любоую папку        ```cd hw_2/```
6) Создать 5 файлов (3 txt, 2 json)     ```touch 1.txt 2.txt 3.txt 4.json 5.json```
7) Создать 3 папки                     ```mkdir h_1 h_2 h_3```
8) Вывести список содержимого папки     ```ls``` 
                                        ```ls -la```     
9) Открыть любой txt файл                    ```vim 1.txt```
10) Написать туда что-нибудь, любой текст.   ```нажать клавишу "i" ввести текст```
                                ```Hello```
                                ```I'm Andrei```
                                ```I'm from Minsk```
11) сохранить и выйти.                 ```"esc" ввести  ":wq"```
12) Выйти из папки на уровень выше            ```cd ..```

13) переместить любые 2 файла, которые вы создали, в любую другую папку.   
```mv 1.txt 2.txt h_1/```
                                                                          
       ```mv 1.txt 2.txt путь к папке/1.txt```  - перенести в другую директорию

14) скопировать любые 2 файла, которые вы создали, в любую другую папку.   ```cp 1txt 2.txt h_1/2.txt``` 
                                                                           
15) Найти файл по имени         ```find . -name 1.txt```
16) просмотреть содержимое в реальном времени (команда grep) изучите как она работает.  ```tail -f 1.txt``` 
                                                                                       

17) вывести несколько первых строк из текстового файла       ```head -2 1.txt```
18) вывести несколько последних строк из текстового файла    ```tail -2 1.txt```

19) просмотреть содержимое длинного файла (команда less) изучите как она работает.   ```less name_file```
20) вывести дату и время    ```date +"%D %T"```
---
__Задание *__
1) Отправить http запрос на сервер.
http://162.55.220.72:5005/object_info_3?name=Vadim&age=32&salary=1000

```curl 'http://162.55.220.72:5005/object_info_3?name=Vadim&age=32&salary=1000'```

1_1) Отправить http запрос на сервер.
http://162.55.220.72:5005/terminal-hw-request

```curl http://162.55.220.72:5005/terminal-hw-request```

приходит ответ с другим заданием.

```curl "http://162.55.220.72:5005/get_method?name=(Andrei)&age=(29)"```

2) Написать скрипт который выполнит автоматически пункты 3, 4, 5, 6, 7, 8, 13

Создаём файл: ```touch HW_1_1.sh```

Вносим изменения: ```vim HW_1_1.sh```

нажать клавишу ```"i"``` ввести текст 
```
#!/bin/sh 
cd coursKsendzoff/
mkdir h_1 h_2 h_3
cd h_1/
touch 1.txt 2.txt 3.txt 4.json 5.json
mkdir f_1 f_2 f_3
ls -la
mv 1.txt 2.txt f_1/
```
Cохранить и выйти: ```"esc" ":wq"```

Выполняем скрипт: ```sh HW_1_1.sh``` 
                  ```./HW_1_1 ```


---
---


__Задание по GitHub_1__

__JSON__

 4. Создать внешний репозиторий c названием JSON.     
 
 ```New```

  ```Create repository```

 5. Клонировать репозиторий JSON на локальный компьютер.   
 
 ```git clone git@github.com:AndreiHeranok/JSON.git```

 6. Внутри локального JSON создать файл “new.json”.     ```touch  new.json```

 7. Добавить файл под гит.          ```git add . new.json```

 8. Закоммитить файл.               ```git commit -m "add json"```

 9. Отправить файл на внешний GitHub репозиторий.  ```git push```

 10. Отредактировать содержание файла “new.json” - написать информацию о себе (ФИО, возраст, количество домашних животных, будущая желаемая зарплата). Всё написать в формате JSON.
 
Вносим изменения: ```vim new.json```

нажать клавишу ```"i"``` ввести текст
```
{
 "FIO": "Heranok Andrei Vladimirovich",
 "age": 29,
 "number of pets": "1",
 "Future desired salary": "500"
}
```
Cохранить и выйти: ```"esc" ":wq"```

 11. Отправить изменения на внешний репозиторий.  ```git commit -am "add edit json"```
                                                  ```git push```

 12. Создать файл preferences.json    ```touch preferences.json```

 13. В файл preferences.json добавить информацию о своих предпочтениях (Любимый фильм, любимый сериал, любимая еда, любимое время года, сторона которую хотели бы посетить) в формате JSON.

Вносим изменения: ```vim preferences.json```

нажать клавишу ```"i"``` ввести текст
```
{
 "Favorite movie": "The Big Lebowski",
 "Favorite series": "La casa de papel",
 "favorite food": "Potato",
 "favorite time of year": "Summer",
 "country you'd like to visit": "Canada"
}
```
Cохранить и выйти: ```"esc" ":wq"```

 14. Создать файл skills.json добавить информацию о скиллах которые будут изучены на курсе в формате JSON

Создаём файл: ```touch skills.json```

Вносим изменения: ```vim skills.json```

нажать клавишу ```"i"``` ввести текст
```
{
    "Базовая теория": "Что такое тестирование, багрепорты, документация, виды, методы, направления тестирования, SDLC, STLC.",
    "клиент-сервер": "клиент-серверная архитектура",
    "Методы запросов на сервер": "HTTP",
    "Коды ответов": "HTTP сервера",
    "Структуры": "HTTP запросов и ответов",
    "Структура": "JSON, XML",
    "Тестирование API": "через Postman (JS, автотесты API)",
    "Снятие и чтение логов": "c внешнего сервера",
    "Снифинг": " http web трафика через Charles и Fiddler",
    "Dev Tools веб браузеров": "Google Chrome, FireFox",
    "VPN": "Как работает, зачем нужен, как использовать, варианты инструментов",
    "тестирование": "Мобильное",
    "гайдлайны": "Особенность iOS, Android",
    "Сборка": "iOS приложений на XCode.",
    "Сборка": "Androidприложений на Android Studio.",
    "ADB": "управление андройд девайсами",
    "Настройка": " прокси и vpn на iOS и Android",
    "Перехват (сниффинг) мобильного трафика": "через Charles и Fiddler на iOS и Android",
    "Командная строка (terminal) Linux": "копирование, создание, просмотр, перемещение файлов на серверах без графического интерфейса",
    "Основы bash скриптинг": "автоматизация рутинных задач на сервере",
    "Доступ": "к удалённым серверам",
    "Основы SQL": "Create, Delete, Drop, Insert Into, Select, From, Where, Join",
    "База данных": "Postgres, установка, настройка и использование",
    "Нереляционная база данных": " Redis установка, настройка и использование",
    "Нагрузочное тестирование": "в Jmeter",
    "Методология разработки": "Scrum",
    "Python": "Изучение основ. Создание клиент серверного приложения"
}
```
Cохранить и выйти: ```"esc" ":wq"```

 15. Отправить сразу 2 файла на внешний репозиторий.  
 
  ```git add .```
                                                      
 ```git commit -m "add skills and preference"```

```git push```

 16. На веб интерфейсе создать файл bug_report.json.        - 
 
 ```Add file```

```- Create new file```

```- Commit new file```
 
17. Сделать Commit changes (сохранить) изменения на веб интерфейсе. 

 ```-edit this file```

```в строке Commit changes пишем новый Commit```

```Commit changes```

 18. На веб интерфейсе модифицировать файл bug_report.json, добавить баг репорт в формате JSON.

```-edit this file```
```
{
	"ID": 1,
        "Version": "Windows 10",
	"Summary": "Не отображаеться предупреждающие окно в приложении при деление на ноль",
	"Req id": "22.3",
	"Steps": "Открыть приложение, Ввести число, Нажать кнопку '/', вссети другое число, нажать кнопку '='",
	"Actual result": "в полле ввода число 0,предупреждающего окна нету",
	"Expected result": "Появляется окно ошибки с текстом,'вы не можете делить на 0'",
	"Severity": "Minor",
	"Priority": "Low",
        "Attachments": "Скриншот"
}
```
19. Сделать Commit changes (сохранить) изменения на веб интерфейсе.    в строке Commit changes пишем новый Commit
                                                                       ```Commit changes```

20. Синхронизировать внешний и локальный репозиторий JSON       ```git pull```


__XML__

 21. Создать внешний репозиторий c названием XML.     
 
 ```New```

```Create repository```

 22. Клонировать репозиторий XML на локальный компьютер.   
 
 ```git clone git@github.com:AndreiHeranok/XML.git```

 23. Внутри локального XML создать файл “new.xml”.  ```touch new.xml```

 24. Добавить файл под гит.    ```git add . new.xml```

 25. Закоммитить файл.       ```git commit -m "add xml"```

 26. Отправить файл на внешний GitHub репозиторий.  ```git push```
 
 27. Отредактировать содержание файла “new.xml” - написать информацию о себе (ФИО, возраст, количество домашних животных, будущая желаемая зарплата). Всё написать в формате XML.

Вносим изменения: ```vim new.xml```

нажать клавишу ```"i"``` ввести текст
```
<info>
 <FIO>Heranok Andrei Vladimirovich</FIO>
 <AGE>29</AGE>
 <number_of_pets>1</number_of_pets>
 <Future_desired_salary>500</Future_desired_salary>
</info>
```
Cохранить и выйти: ```"esc" ":wq"```

28. Отправить изменения на внешний репозиторий.  

 ```git commit -am "edit xml"```
 
 ```git push```
 
29. Создать файл preferences.xml       ```touch preferences.xml```

30. В файл preferences.xml добавить информацию о своих предпочтениях (Любимый фильм, любимый сериал, любимая еда, любимое время года, сторона которую хотели бы посетить) в формате XML.
  
Вносим изменения: ```vim preferences.xml```

нажать клавишу ```"i"``` ввести текст
```
<Favorite>
 <Favorite_movie>The Big Lebowski</Favorite_movie>
 <Favorite_series>La casa de papel</Favorite_series>
 <favorite_food>Potato</favorite_food>
 <favorite_time_of_year>Summer</favorite_time_of_year>
 <country_you_like_to_visit>Canada</country_you_like_to_visit>
</Favorite>
```
Cохранить и выйти: ```"esc" ":wq"```

 31. Создать файл skills.xml добавить информацию о скиллах которые будут изучены на курсе в формате XML 

Создаём файл: ```touch skills.xml```

Вносим изменения: ```vim skills.xml```

нажать клавишу ```"i"``` ввести текст
```
<skills>
    <Базовая_теория>Что такое тестирование, багрепорты, документация, виды, методы, направления тестирования, SDLC, STLC</Базовая_теория>,
    <клиент_сервер>клиент-серверная архитектура</клиент_сервер>,
    <Методы_запросов_на_сервер>HTTP<Методы_запросов_на_сервер>,
    <Коды_ответов>HTTP сервера</Коды_ответов>,
    <Структуры>HTTP запросов и ответов</Структуры>,
    <Структура>JSON, XML</Структуры>,
    <Тестирование_API>через Postman (JS, автотесты API)</Тестирование_API>,
    <Снятие_и_чтение_логов>c внешнего сервера</Снятие_и_чтение_логов>,
    <Снифинг>http web трафика через Charles и Fiddler</Снифинг>,
    <Dev_Tools_веб_браузеров>Google Chrome, FireFox</Dev_Tools_веб_браузеров>,
    <VPN>Как работает, зачем нужен, как использовать, варианты инструментов</VPN>,
    <тестирование>Мобильное</тестирование>,
    <гайдлайны>Особенность iOS, Android</гайдлайны>,
    <Сборка>iOS приложений на XCode</Сборка>,
    <Сборка>Androidприложений на Android Studio</Сборка>,
    <ADB>управление андройд девайсами</ADB>,
    <Настройка>прокси и vpn на iOS и Android</Настройка>,
    <Перехват_(сниффинг)_мобильного_трафика>через Charles и Fiddler на iOS и Android</Перехват_(сниффинг)_мобильного_трафика>,
    <Командная_строка_(terminal)_Linux>копирование, создание, просмотр, перемещение файлов на серверах без графического интерфейса</Командная_строка_(terminal)_Linux>,
    <Основы_bash_скриптинг>автоматизация рутинных задач на сервере</Основы_bash_скриптинг>,
    <Доступ>к удалённым серверам</Доступ>,
    <Основы_SQL>Create, Delete, Drop, Insert Into, Select, From, Where, Join</Основы_SQL>,
    <База_данных>Postgres, установка, настройка и использование</База_данных>,
    <Нереляционная_база_данных>Redis установка, настройка и использование</Нереляционная_база_данных>,
    <Нагрузочное_тестирование>Jmeter</Нагрузочное_тестирование>,
    <Методология_разработки>Scrum</Методология_разработки>,
    <Python>Изучение основ. Создание клиент серверного приложения</Python>
</skills>
```
Cохранить и выйти: ```"esc" ":wq"```

 32. Сделать коммит в одну строку.                   ```git commit -ma "add new xml"```

 33. Отправить сразу 2 файла на внешний репозиторий.

```git add``` . 

```git commit -m "edit new xml"```

```git push```

 34. На веб интерфейсе создать файл bug_report.xml.  
 
 ```- Add file```

```- Create new file```

```- Commit new file```

 35. Сделать Commit changes (сохранить) изменения на веб интерфейсе. 
 
 ```-edit this file```
                                                               
```в строке Commit changes пишем новый Commit```

```Commit changes```

 36. На веб интерфейсе модифицировать файл bug_report.xml, добавить баг репорт в формате XML.
```
<bug>
    <ID>1</ID>,
    <Version>Windows 10</Version>,
    <Summary>Не отображаеться предупреждающие окно в приложении при деление на ноль</Summary>,
    <Req_id>22.3</Req_id>,
    <Steps>ткрыть приложение, Ввести число, Нажать кнопку '/', вссети другое число, нажать кнопку '='</Steps>,
    <Actual_result>в полле ввода число 0,предупреждающего окна нету</Actual_result>,
    <Expected_result>Появляется окно ошибки с текстом,'вы не можете делить на 0'</Expected_result>,
    <Severity>Minor</Severity>,
    <Priority>Low</Priority>,
    <Attachments>screenshot</Attachments>
</bug>
```
 37. Сделать Commit changes (сохранить) изменения на веб интерфейсе.    
 
 ```в строке Commit changes пишем новый Commit```

```Commit changes```

 38. Синхронизировать внешний и локальный репозиторий XML   ```git pull```

__TXT__
 
 1. Создать внешний репозиторий c названием TXT.       
 
 ```New```

```Create repository```

 2. Клонировать репозиторий TXT на локальный компьютер.     
 
 ```git clone https://github.com/AndreiHeranok/TXT.git```

 3. Внутри локального TXT создать файл “new.txt”.      ```touch new.txt```

 4. Добавить файл под гит.     ```git add . new.txt```
       
 5. Закоммитить файл.         ```git commit -m "add txt"```

 6. Отправить файл на внешний GitHub репозиторий.     ```git push```

 7. Отредактировать содержание файла “new.txt” - написать информацию о себе (ФИО, возраст, количество домашних животных, будущая желаемая зарплата). Всё написать в формате TXT.
 
Вносим изменения: ```vim new.txt```

нажать клавишу ```"i"``` ввести текст
```
FIO - Heranok Andrei Vladimirovich
AGE - 29
Number of pets - 1
Future desired salary - 500
```
Cохранить и выйти: ```"esc" ":wq"```

8. Отправить изменения на внешний репозиторий.   

```git commit -am "edit txt"```

```git push```

 9. Создать файл preferences.txt         ```touch preferences.txt```

 10. В файл preferences.txt” добавить информацию о своих предпочтениях (Любимый фильм, любимый сериал, любимая еда, любимое время года, сторона которую хотели бы посетить) в формате TXT.

Вносим изменения: ```vim preferences.txt```

нажать клавишу ```"i"``` ввести текст
```
Favorite movie - The Big Lebowski,
Favorite series - La casa de papel,
favorite food - Potato,
favorite time of year - Summer,
country you'd like to visit - Canada.
```
Cохранить и выйти: ```"esc" ":wq"```

 11. Создать файл skills.txt добавить информацию о скиллах которые будут изучены на курсе в формате TXT

Создаём файл: ```touch skills.txt```

Вносим изменения: ```vim skills.txt```
нажать клавишу ```"i"``` ввести текст
```
Базовая теория (Что такое тестирование, багрепорты, документация, виды, методы, направления тестирования и т.п.) SDLC, STLC.
Что такое клиент-серверная архитектура.
HTTP Методы запросов на сервер.
Коды ответов HTTP сервера.
Структуры HTTP запросов и ответов.
Что такое JSON, XML. Их структура.
Тестирование API через Postman (JS, автотесты API).
Снятие и чтение логов c внешнего сервера.
Снифинг http web трафика через Charles и Fiddler.
Dev Tools веб браузеров (Google Chrome, FireFox).
VPN. (Как работает, зачем нужен, как использовать, варианты инструментов)
Мобильное тестирование.
Особенность iOS, Android, гайдлайны.
Сборка iOS приложений на XCode. (У кого нет Mac компьютера, просто посмотрят)
Сборка Android приложений на Android Studio.
ADB (управление андройд девайсами).
Настройка прокси и vpn на iOS и Android.
Перехват (сниффинг) мобильного трафика через Charles и Fiddler на iOS и Android.
Командная строка (terminal) Linux (копирование, создание, просмотр, перемещение файлов на серверах без графического интерфейса)
Основы bash скриптинг, автоматизация рутинных задач на сервере.
Доступ к удалённым серверам.
Основы SQL (Create, Delete, Drop, Insert Into, Select, From, Where, Join).
База данных Postgres (установка, настройка и использование).
Нереляционная база данных Redis (установка, настройка и использование).
Нагрузочное тестирование в Jmeter.
Методология разработки Scrum.
Python. (Изучение основ. Создание клиент серверного приложения)
```
Cохранить и выйти: ```"esc" ":wq"```

 12. Сделать коммит в одну строку.              ```git commit -am "add new txt"```

13. Отправить сразу 2 файла на внешний репозиторий.        

```git add .``` 

```git commit -am "add new txt"```

```git push```
              
 14. На веб интерфейсе создать файл bug_report.txt.      
 
 ```Add file```

```- Create new file```

```- Commit new file```
  
 15. Сделать Commit changes (сохранить) изменения на веб интерфейсе.   
 
 ```-edit this file```

```в строке Commit changes пишем новый Commit```

```Commit changes```
 
 16. На веб интерфейсе модифицировать файл bug_report.txt, добавить баг репорт в формате TXT.
 ```
  ID - 1,
  Version - Windows 10,
  Summary - Не отображаеться предупреждающие окно в приложении при деление на ноль,
  Req id - 22.3,
  Steps - Открыть приложение, Ввести число, Нажать кнопку '/', вссети другое число, нажать кнопку '=',
  Actual result - в полле ввода число 0,предупреждающего окна нету,
  Expected result - Появляется окно ошибки с текстом,'вы не можете делить на 0',
  Severity - Minor,
  Priority - Low,
  Attachments - Скриншот.
```
 17. Сделать Commit changes (сохранить) изменения на веб интерфейсе.   
 
```edit this file```

```в строке Commit changes пишем новый Commit```

```Commit changes```
 
 18. Синхронизировать внешний и локальный репозиторий TXT       ```git pull```