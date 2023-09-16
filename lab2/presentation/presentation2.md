# РОССИЙСКИЙ УНИВЕРСИТЕТ ДРУЖБЫ НАРОДОВ
### Факультет физико-математических и естественных наук
### Кафедра прикладной информатики и теории вероятностей



# ЛАБОРАТОРНАЯ РАБОТА  № 2
### дисциплина: Информационная безопасность


### Студент: Пиняева Анна Андреевна
### Группа: НФИбд-02-20

### МОСКВА
### 2023 

____



# Цель работы

### Получение практических навыков работы в консоли с атрибутами файлов, закрепление теоретических основ дискреционного разграничения доступа в современных системах с открытым кодом на базе ОС Linux1.

____

# Ход работы

### 1. В установленной при выполнении предыдущей лабораторной работы операционной системе создали учётную запись пользователя guest (рис. 1-2). Задали пароль. 

*Рис. 1 Вход от имени админимтратора:*

![N|Solid](https://sun9-72.userapi.com/impg/ewp7Ia6gMR-G1jyLVLF9K8tpKZvggfXIdXTruw/vUaGdn1dvmA.jpg?size=2160x518&quality=95&sign=76132df89ff364204159b137b3660c7a&type=album)

*Рис. 2 Создание учетной записи guest:*

![N|Solid](https://sun9-43.userapi.com/impg/L5hDtAAXhE57TI2oemk028kR8dtiwPPoR-9b6A/R6s2qLQV3Mw.jpg?size=2160x518&quality=95&sign=ac134ba3658e2bb6ed84626007fa3c22&type=album)

____

### 3. Вошли в систему от имени пользователя guest (рис. 3). 
*Рис. 3 Вход в систему:*

![N|Solid](https://sun9-39.userapi.com/impg/_a1-waYX2_x__oC_fT1FVZFBCCpJDOAoWZlfPQ/U_PFkOfSAyo.jpg?size=2160x518&quality=95&sign=da6b31ff5e6b1d9291da9dcbee700674&type=album)
____


### 4. Определили директорию,в которой находимся,уточнили имя пользователя, его группу (рис. 4). 

*Рис. 4 Выполнение запросов:*

![N|Solid](https://sun9-57.userapi.com/impg/3QiwOLcrxvDLy44grnIJNYHAnma8Ly_1J_aixQ/3yzGQErGSn0.jpg?size=2560x1600&quality=95&sign=7107d2f1e725a284abdaecd77fe1e2b2&type=album)

____

### 5. Просмотрели файл /etc/passwd командой cat /etc/passwd (рис. 5). Нашли в нем свою учетную запись (рис. 6). 
*Рис. 5 Просмотре файла /etc/passwd:*

![N|Solid](https://sun9-23.userapi.com/impg/O6uhpxEmTR8IySfkOA5TA-BSwbkfIIrTbkE7fA/fvXhGA-P9SU.jpg?size=1910x1442&quality=95&sign=30bec25ac68e7c0305d0110120af993d&type=album)


*Рис. 6 Учетная запись:*

![N|Solid](https://sun9-79.userapi.com/impg/u5rk3v7NOlyRHe_tNVFRGXVZdl_7g3zX6U5gJg/6xNYtUraqCU.jpg?size=1910x120&quality=95&sign=68a618c2473a6f6de9d7b5028b7287cb&type=album)
_____


### 6. Определили существующие в системе директории командой ls -l /home/ (рис. 7). 
*Рис. 7 Определение директорий:*

![N|Solid](https://sun9-22.userapi.com/impg/uHrA4HaWlC63TM675IPzhgDqw7twvi6y_UhfOg/l4PNmVsJzc4.jpg?size=1910x214&quality=95&sign=745514015e88d4470d5ef58c6c3a183b&type=album)

____

### 7. Проверили, какие расширенные атрибуты установлены на поддиректориях, находящихся в директории /home (рис. 8). Увидели атрибуты текущего пользователя, но не других. 

*Рис. 8 Расширенные атрибуты:*

![N|Solid](https://sun9-53.userapi.com/impg/FQXSeV1KxgGHihrg5CpxbkBXxiWXUv0fzVxEoA/A3wrgxP0H3k.jpg?size=1910x214&quality=95&sign=112c319130910d798dd874d1073a40fc&type=album)

____

### 8. Создали в домашней директории поддиректорию dir1.  Определили, какие права доступа и расширенные атрибуты были выставлены на директорию dir1 (рис. 9). 

*Рис. 9 Создание директории, проверка прав доступа и расширенных атрибутов:*

![N|Solid](https://sun9-31.userapi.com/impg/3iQSt9K_CO6_bwvKOjiibWyrkS8L8FhDh6SP2g/GVGWYPlMsiQ.jpg?size=1910x1130&quality=95&sign=0bb4f2fcb118bb0e512142bf3e3da115&type=album)

____

### 9. Сняли с директории dir1 все атрибуты и проверили с её помощью правильность выполнения команды ls -l (рис. 10). 
*Рис. 10 Снятие атрибутов:*

![N|Solid](https://sun9-57.userapi.com/impg/H67SvY5y4Kd4z6MgmK4f0--CwrDwdiieRMNMvg/A-lnKRoEWCw.jpg?size=1910x642&quality=95&sign=2c3f61ea9bb35789c1cf59346adfc379&type=album)
____


### 10. Попытались создать в директории dir1 файл file1. Файл не удалось создать из-за отсутствия прав на создание. 
*Рис. 11 Создание файла:*

![N|Solid](https://sun9-71.userapi.com/impg/n84vGr-FPrO4yV-JrX3SJj40EUjLgAXWrJ5-PQ/pNV6YpwIkLs.jpg?size=1910x240&quality=95&sign=ce365174739c260ac1aaa57d132ba183&type=album)

____

### 11. Заполнили таблицу «Установленные права и разрешённые действия» (рис. 12). 
*Рис. 12 Таблица 1:*

![N|Solid](https://sun9-68.userapi.com/impg/NJbfs3Bupc-lS8BWlK7VdswxGWZuShuttu6Sdg/96TIu5_7-LE.jpg?size=1550x572&quality=95&sign=47a44d4da715881066c60a72ee739128&type=album)
____

### 14.  На основании заполненной таблицы определили те или иные минимально необходимые права для выполнения операций внутри директории dir1(рис. 13). 
*Рис. 13 Таблица 2:*

![N|Solid](https://sun9-25.userapi.com/impg/v50M7XKpbthFHj6PYoWaSRjXXn1t54jFDAa4eg/GHTeT9b4K6U.jpg?size=1550x572&quality=95&sign=41f441f7d7d5238d5bcfa17ac63adf47&type=album)

____

# Выводы

###Получены практические навыки работы в консоли с атрибутами файлов, закреплены теоретические основы дискреционного разграничения доступа в современных системах с открытым кодом на базе ОС Linux1.

