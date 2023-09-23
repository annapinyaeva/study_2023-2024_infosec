# РОССИЙСКИЙ УНИВЕРСИТЕТ ДРУЖБЫ НАРОДОВ
### Факультет физико-математических и естественных наук
### Кафедра прикладной информатики и теории вероятностей


# Презентация
# ПО ЛАБОРАТОРНОЙ РАБОТЕ  № 3
### дисциплина: Информационная безопасность


### Студент: Пиняева Анна Андреевна
### Группа: НФИбд-02-20

### МОСКВА
### 2023 
---
# Цель работы 

### Получение практических навыков работы в консоли с атрибутами файлов для групп пользователей. 

# Ход работы

### 1. Создали учётную запись пользователя guest2 (рис. 1). 
*Рис. 1 Создание учетной записи guest2:*

![N|Solid](https://sun9-67.userapi.com/impg/VZBEOxWzY0SrPExDi_ffJMtq5SRaHtAOyhG1bQ/DZYa_6tv97Q.jpg?size=1586x176&quality=95&sign=cc7ae5b7bea6ed48d9c82d8ffeb5fd20&type=album)


### 2. Добавили пользователя guest2 в группу guest (рис. 2). 

*Рис. 2 Добавление пользователя guest2 в группу guest:*

![N|Solid](https://sun9-1.userapi.com/impg/vodmRL3uN7hAzLUrMGynNWh_z3RxId_qmi__OQ/oJWldSIFiMs.jpg?size=1586x176&quality=95&sign=f733eb3928c1086e4adec9ba11c73b25&type=album)
---
### 3. Осуществили вход в систему от двух пользователей на двух разных консолях (рис. 3). 
*Рис. 3 Вход в систему:*

![N|Solid](https://sun9-74.userapi.com/impg/dxwlkbm9tf29iY0d5LeG16vaGmhrrduSSqfztw/Dsx2l8PwjOE.jpg?size=1960x752&quality=95&sign=2391e098f66ef46fdc8bf97dfa027c45&type=album)

### 4-5. Для обоих пользователей определили директорию,в которой находимся (рис. 4-5). 

*Рис. 4 Выполнение команд guest2:*

![N|Solid](https://sun1-98.userapi.com/impg/anYgzsBhDW9yTssNfFKOo28hMf4S3aXzfMBFUw/-m6PvmVXdB0.jpg?size=1960x420&quality=95&sign=7b7f951a2d341b8e7a139585347e87b6&type=album)

*Рис. 5 Выполнение команд guest:*

![N|Solid](https://sun9-47.userapi.com/impg/T0Nq0XsGaTQHO2z-moRizHR5yJBDskF6XXX5rw/I6f6rqKNJPg.jpg?size=1960x380&quality=95&sign=52073fed13ac93fbb4da645add3d124f&type=album)



### 6. Сравнили полученную информацию с содержимым файла /etc/group (рис. 6). 
 
*Рис. 6 Фрагмент файла /etc/passwd:*

![N|Solid](https://sun9-38.userapi.com/impg/-qnmYSuNfptI-BTXUAJ45FnW3-mK808oCuhjhQ/VZoHh3wA9i0.jpg?size=1960x420&quality=95&sign=294123c517291f923564477f08e706ae&type=album)

### 7. От имени пользователя guest2 выполнили регистрацию пользователя guest2 в группе guest (рис. 7). 

*Рис. 7 Регистрация:*

![N|Solid](https://sun9-61.userapi.com/impg/tm3Omf2nAiG9h7BIZSh_Coz07rdaza0BuY-9EQ/BbgK9U5RCL4.jpg?size=1960x98&quality=95&sign=9fe4aae0974560a49d6875df3d6ab216&type=album)

### 8. От имени пользователя guest изменили права директории /home/guest, разрешив все действия для пользователей группы (рис. 8). 

*Рис. 8 Выполнение команд:*

![N|Solid](https://sun9-69.userapi.com/impg/RL3bjH0fSMUKXrucYbUNTS7KJ3cYkgWDxazU3Q/OS-vxZdVx74.jpg?size=1960x670&quality=95&sign=b87f14d5cfd38f5050d4d8f30ea6de3e&type=album)


### 9. От имени пользователя guest сняли с директории /home/guest/dir1 все атрибуты и проверили правильность снятия атрибутов (рис. 8). 



### 10. Заполнили таблицу «Установленные права и разрешённые действия» (рис. 9). Таблица идентична таблице из предыдущей лабораторной работы. 
*Рис. 9 Таблица 1:*

![N|Solid](https://sun9-68.userapi.com/impg/NJbfs3Bupc-lS8BWlK7VdswxGWZuShuttu6Sdg/96TIu5_7-LE.jpg?size=1550x572&quality=95&sign=47a44d4da715881066c60a72ee739128&type=album)

### 11.  На основании заполненной таблицы определили те или иные минимально необходимые права для выполнения операций внутри директории dir1(рис. 13). 
*Рис. 13 Таблица 2:*

![N|Solid](https://sun9-25.userapi.com/impg/v50M7XKpbthFHj6PYoWaSRjXXn1t54jFDAa4eg/GHTeT9b4K6U.jpg?size=1550x572&quality=95&sign=41f441f7d7d5238d5bcfa17ac63adf47&type=album)



# Выводы

### Получены практические навыки работы в консоли с атрибутами файлов для групп пользователей.

# Список используемой литературы

####1. Методические материалы курса