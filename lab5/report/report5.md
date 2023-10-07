# РОССИЙСКИЙ УНИВЕРСИТЕТ ДРУЖБЫ НАРОДОВ
### Факультет физико-математических и естественных наук
### Кафедра прикладной информатики и теории вероятностей 


# ОТЧЕТ
# ПО ЛАБОРАТОРНОЙ РАБОТЕ  № 5
### дисциплина: Информационная безопасность


### Студент: Пиняева Анна Андреевна
### Группа: НФИбд-02-20

### МОСКВА
### 2023 
---

# Цель работы

### Изучение механизмов изменения идентификаторов, применения SetUID- и Sticky-битов. Получение практических навыков работы в консоли с дополнительными атрибутами. Рассмотрение работы механизма смены идентификатора процессов пользователей, а также влияние бита Sticky на запись и удаление файлов.

# Ход работы

### 1. Вошли в ситсему от имени пользователя guest. Создали программу simplied.c (рис. 1). 

*Рис. 1 Программа simplied.c:*

![N|Solid](https://sun9-57.userapi.com/impg/vh_AzB-0UGWn86uCLXSKa1fgeDc2chYPkg5NZQ/9cc9VCbdx7g.jpg?size=2394x812&quality=95&sign=576b71d882ea57f390c60b72ee9f36a1&type=album)


### 2. Скомплилировали программу и убедились, что файл программы создан (рис. 2). 

*Рис. 2 Компиляция и запуск программы:*

![N|Solid](https://sun9-26.userapi.com/impg/u9uR8OpHD_eEoorI3LBX3wDkgLqtEH2kqgMr3g/z7bBsP4hdnQ.jpg?size=1988x272&quality=95&sign=6f44d3db2df364f587205b084b1f25e7&type=album)

---

### 3. Выполнили программу (рис. 2). 


### 4. Выполнили системную программу id (рис. 3).Получили результат аналогичный результату выполнения программы simplied.c. 
 

*Рис. 3 Выполнение программы id:*

![N|Solid](https://sun9-34.userapi.com/impg/OCAy0YYhMMScRBzp4HDi99LooEoqMPlaml-caA/pWm3tXGYD9g.jpg?size=1908x190&quality=95&sign=4c606e7cf7b21156c25590f53e70dbf6&type=album)


### 5. Создали новый файл с усложненной программой simplied.c simplied2.c (рис. 4). 

*Рис. 4 Программа simplied2.c:*

![N|Solid](https://sun9-8.userapi.com/impg/aUSxOG5lvdD1pmThFha1yIuKDkzHcVPXqs5FPw/jHBjHE7vOqA.jpg?size=1988x1060&quality=95&sign=fc2ef1d9c8197aec69e2a2a39ed9c154&type=album)


### 6. Скомпилировали и запустили программу (рис. 5).  
 
*Рис. 5 Компиляция и запуск:*

![N|Solid](https://sun9-26.userapi.com/impg/u9uR8OpHD_eEoorI3LBX3wDkgLqtEH2kqgMr3g/z7bBsP4hdnQ.jpg?size=1988x272&quality=95&sign=6f44d3db2df364f587205b084b1f25e7&type=album)


### 7. От имени суперпользователя выполнили команды: chown root:guest /home/guest/simpleid2, chmod u+s /home/guest/simpleid2 (рис. 6). 

*Рис. 6 Выполнение команд:*

![N|Solid](https://sun9-62.userapi.com/impg/_Z9EBh2rxPHz167yoMcbAEZO2uZP-NzKEQTl5g/LQLH98e0saQ.jpg?size=1988x372&quality=95&sign=ceab3fe1877316407bbe5ae06a5faf81&type=album)


### 8. Выполнили проверку правильности установки новых атрибутов и смены владельца файла simpleid2 (рис. 6). 


### 9. Запустили simpleid2 и id (рис. 7). 

*Рис. 7 Запуск программ:*

![N|Solid](https://sun9-70.userapi.com/impg/OOxqyhNYP6fMCemxd7OzogEJDeuvEn4p5IGY7g/hWT9W7BB9vw.jpg?size=1988x366&quality=95&sign=83026021f08e327781dc87596a0cdd45&type=album)

### 10. Сделали то же самое относительно  SetGID-бита (рис. 8). 

*Рис. 8 Запуск программ:*

![N|Solid](https://sun9-3.userapi.com/impg/tAWXhF40PvOTz_gyczpaOUW7LFDV9AGP6SXmcw/Dk6D_kcZ4Gg.jpg?size=1988x516&quality=95&sign=d2ccb48398eefda7e5210b6a3db5dfd8&type=album)


### 11. Создали программу readfile.c (рис. 9) и откомпилировали ее. 

*Рис. 9 Программа readfile.c:*

![N|Solid](https://sun9-19.userapi.com/impg/gD4wYy7o6Cgw-rURlbN4eZ69XohRX3ORY9bmiA/JpQSfxtwdDA.jpg?size=1988x1462&quality=95&sign=6f2033cd5ba4f6ce884712697578b287&type=album)

### 12. Сменили владельца у файла readfile.c и изменили права так, чтобы только суперпользователь (root) мог прочитать его, a guest не мог (рис. 9). 

*Рис. 10 Смена владельца и установка прав:*

![N|Solid](https://sun9-51.userapi.com/impg/bxFX5yGHLdobPMaHiV0noxX2IdZyme0W-RS-hQ/9QsdHaDDiXY.jpg?size=1806x168&quality=95&sign=f779cc24b7b1c8f6ecf60846f1fc2e15&type=album)

### 13. Проверили, что пользователь guest не может прочитать файл readfile.c (рис. 11). 

*Рис. 11 Проверка:*

![N|Solid](https://sun1-21.userapi.com/impg/-eXLm8GILaNVvqaGMqAtzgUqLxjIsm81GPQk9w/CUZGkZKFd14.jpg?size=1806x168&quality=95&sign=53b7141eace27975894a51f4820ba093&type=album)

### 14. Сменили у программы readfile владельца и установили SetU’D-бит. Проверили может ли программа прочитать файл readfile.c (рис. 12). 

*Рис. 12 Запуск программы:*

![N|Solid](https://sun9-78.userapi.com/impg/pvGHLcyK8O-HkZ95QCuNo0m3esyF87fLXnHtvg/3bdugVZgG4E.jpg?size=1806x1230&quality=95&sign=105f9e3de897f82f0f7f97db76a266c6&type=album)

### 15. Проверили может ли программа прочитать файл /etc/shadow (рис. 13). 

*Рис. 13 Запуск программ:*

![N|Solid](https://sun9-33.userapi.com/impg/EwETXrbm0Ou6KdGYArldGgDYIVxugzpyX1o18Q/XDYwSpxvXtU.jpg?size=1806x1132&quality=95&sign=a05258f71a848df7448060abe22d5f20&type=album)

### 16. Выяснили, установлен ли атрибут Sticky на директории /tmp (рис. 14). 

*Рис. 14 Команды:*

![N|Solid](https://sun9-14.userapi.com/impg/KZA8Kl3h67zjUtMo0MtUA29xuII-5-ACoZGgEw/U_1JNSI-0xU.jpg?size=1806x424&quality=95&sign=6a8895efec736bcf60439c9c1fa5a636&type=album)

### 17. От имени пользователя guest создали файл file01.txt в директории /tmp со словом test (рис. 14). 

### 18. Просмотрели атрибуты у только что созданного файла и разрешили чтение и запись для категории пользователей «все остальные» (рис. 14). 

### 19. От пользователя guest2 попробовали прочитать файл /tmp/file01.txt (рис. 15). 

*Рис. 15 Чтение файла:*

![N|Solid](https://sun9-57.userapi.com/impg/_l73f7_aCUW24y8k6ARGXb-ib3t6AGr846E2cw/j7oiXmzlIWQ.jpg?size=1806x192&quality=95&sign=c351cc053db897cb40aefc08d7a3a6fb&type=album)

### 20. От пользователя guest2 дозаписали в файл /tmp/file01.txt слово test2 (рис. 16). 

*Рис. 16 Дозапись в файл:*

![N|Solid](https://sun1-96.userapi.com/impg/cxPPoyNjNxnA9e-K8In6p-TFsivbg4qdq1tssg/ABoO1sBlUqw.jpg?size=1806x208&quality=95&sign=2038c1a1bb71424b6886e39f274b5720&type=album)

### 21.  От пользователя guest2 попробуйте записать в файл /tmp/file01.txt слово test3, стерев при этом всю имеющуюся в файле информацию (рис. 17). 

*Рис. 17 Изменение файла:*

![N|Solid](https://sun9-36.userapi.com/impg/MdXdCNiv8Dw9sSA7erP2Gg9MP-_gE4w3YqTqZg/Zjf2SKOpAEU.jpg?size=1806x208&quality=95&sign=1783dd4a6622f517daf2bcdcf369a0c6&type=album)

### 22. От пользователя guest2 попробовали удалить файл /tmp/file01.txt (рис. 18). 

*Рис. 18 Удаление файла:*

![N|Solid](https://sun9-35.userapi.com/impg/ompYfRWOBuY6-KlRkwHD7qKQSkD_aZbmLZog9w/8jTmM9SEw-s.jpg?size=1806x166&quality=95&sign=28c2106f944035ce91854a22e6dc8a10&type=album)

### 23. От имени суперпользователя сняли атрибут t с файла (рис. 19). 

*Рис. 19 Снятие атрибута:*

![N|Solid](https://sun1-97.userapi.com/impg/p0_y1tv_6bWF4qDoq6YjWc0W3tLxhaVl1h6Vtw/WPZ1CbvxDoU.jpg?size=1806x166&quality=95&sign=9881b1f3c215faef46da663ac04b2650&type=album)

### 24. Попробовали выполнить все предыдцщие действия заново (рис. 20). 

*Рис. 20 Выполнение команд:*

![N|Solid](https://sun9-74.userapi.com/impg/FORnYb5PVmc6_6EAFPbxYEH2HAwEHSgesm3PaQ/CFd15dy_EB0.jpg?size=1806x568&quality=95&sign=7446e71693c7428e614f6491c3caceeb&type=album)

### 25. Вернули атрибут t (рис. 21). 

*Рис. 21 Установка атрибута:*

![N|Solid](https://sun9-74.userapi.com/impg/kA-wvodqaw4A7qZxIgQypMexmbk2iPav4VV7dQ/F93qc94t7CQ.jpg?size=1806x212&quality=95&sign=3bcf6f7d6211bca9c0c1f86a2f1bdefc&type=album)




# Выводы

### Изучили механизмы изменения идентификаторов, применения SetUID- и Sticky-битов. Получили практические навыки работы в консоли с дополнительными атрибутами. Рассмотрели работы механизма смены идентификатора процессов пользователей, а также влияние бита Sticky на запись и удаление файлов. 

# Список используемой литературы

#### 1. Методические материалы курса