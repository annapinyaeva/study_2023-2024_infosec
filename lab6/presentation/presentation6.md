# РОССИЙСКИЙ УНИВЕРСИТЕТ ДРУЖБЫ НАРОДОВ
### Факультет физико-математических и естественных наук
### Кафедра прикладной информатики и теории вероятностей 


# Презентация
# ПО ЛАБОРАТОРНОЙ РАБОТЕ  № 6 
### дисциплина: Информационная безопасность


### Студент: Пиняева Анна Андреевна
### Группа: НФИбд-02-20

### МОСКВА
### 2023 

---

# Цель работы

### Развить навыки администрирования ОС Linux. Получить первое практическое знакомство с технологией SELinux1. Проверить работу SELinx на практике совместно с веб-сервером Apache.

---

# Ход работы

### 1. Вошли в систему с полученными учётными данными и убедились, что SELinux работает в режиме enforcing политики targeted с помощью команд getenforce и sestatus. (рис. 1). 

*Рис. 1 Конфигурации SELinux:*

![N|Solid](https://sun9-61.userapi.com/impg/J6B046qWYcO_T0genlSjEfrOeI8fhW6Bss0kFA/QJ4IICVn_Ug.jpg?size=1218x676&quality=95&sign=2ce99d10c8c9e59481c9f65b9cce59f7&type=album)


### 2. Обратились с помощью браузера к веб-серверу, запущенному на компьютере, и убедились, что последний работает (рис. 2). 

*Рис. 2 Обращение к веб-серверу:*

![N|Solid](https://sun9-3.userapi.com/impg/RX0VZraidYEcvBSu3UYaPaQ8U7PdGRJRdthlcw/YuEQa0QzxXk.jpg?size=1946x1244&quality=95&sign=14358858b3de51eb37ca88b53d795c7f&type=album)

---

### 3. Нашли веб-сервер Apache в списке процессов, определили его контекст безопасности (рис. 3).

 *Рис. 3 Контекст безопасности:*

![N|Solid](https://sun9-3.userapi.com/impg/h6IKm6GMXVSmllblVOZmrLQh8wCuUOO6aNsdrQ/EEqJUSAO0GY.jpg?size=2122x730&quality=95&sign=e10492701692346c07f85527ca46a1de&type=album)

---


### 4. Посмотрели текущее состояние переключателей SELinux для Apache (рис. 4).  
 

*Рис. 4 Состояние переключателей SELinux:*

![N|Solid](https://sun9-52.userapi.com/impg/EqLFfQr5bpMqbQVy7-Upg-MoHehI9jgErM4zWQ/aHW1o-dIqWQ.jpg?size=2122x1222&quality=95&sign=2b6a0448123eedbeae1b84b5cb1699a0&type=album)

---

### 5. Посмотрели статистику по политике (рис. 5). 

*Рис. 5 Статистика по политике:*

![N|Solid](https://sun9-12.userapi.com/impg/2M3wInc2DJ2sLhlL0BzqMh9oE5280mLYlybMxQ/4MKtYlB5TWA.jpg?size=2122x1286&quality=95&sign=16bcac846cfeeabc1b416fcc89ad5566&type=album)


### 6. Определили тип файлов и поддиректорий, находящихся в директории /var/www (рис. 6).  
 
*Рис. 6 Дирректория /var/www:*

![N|Solid](https://sun9-80.userapi.com/impg/aaZGDCNIjjOLwEZsY1hJsx5BrEJ29HCbJTU10g/9n3hgqwry3U.jpg?size=2122x320&quality=95&sign=ce0079a3f906e2ee387e678d583e5dc3&type=album)

---

### 7. Определили тип файлов, находящихся в директории /var/www/html (рис. 7). 

*Рис. 7 Дирректория /var/www/html:*

![N|Solid](https://sun9-79.userapi.com/impg/dilyWdWEqTk_EFmqqfxqO9gO-bF2_B_C7oQ35A/6esVehc-qls.jpg?size=2122x120&quality=95&sign=5392a8630731184b32203f18eb33fbdc&type=album)


### 8. Создали от имени суперпользователя html-файл /var/www/html/test.html (рис. 8). 

*Рис. 8 Файл /var/www/html/test.html:*

![N|Solid](https://sun9-71.userapi.com/impg/woyFRNyrLeIA1xxNY9ittC8RQK_LlHVN-n44tQ/pQk029ldC1E.jpg?size=2122x342&quality=95&sign=d553b0f4e793d089155304dce276aa90&type=album)

---

### 9. Проверили контекст созданного файла (рис. 9). 

*Рис. 9 Контекст файла:*

![N|Solid](https://sun9-10.userapi.com/impg/zFAcTsp9VJ3yYCUTzo408K6_g49_GULddg5Kzg/F_JS4OV-XtA.jpg?size=2122x164&quality=95&sign=ebcc0162f0bb3de992e9c4b46c8816d5&type=album)

### 10. Обратитились к файлу через веб-сервер, введя в браузере адрес http://127.0.0.1/test.html (рис. 10). 

*Рис. 10 Запуск в браузере:*

![N|Solid](https://sun9-80.userapi.com/impg/smBJVLEVbjIcVamePkSEPeFZjVI25DwWHiYEUA/3lOhsVtDVHo.jpg?size=2122x344&quality=95&sign=1c916fb3a9782f84683579efda76798e&type=album)

---

### 11. Изучили справку man httpd_selinux (рис. 11). 

*Рис. 11 Справка man httpd_selinux:*

![N|Solid](https://sun9-65.userapi.com/impg/WqdW7zSGknilho0bmFiCT_hMfWCfvoZeXNwSiA/NWoFWaeBCHU.jpg?size=2122x1488&quality=95&sign=b7c247785d9f2c44cd54823bcf685697&type=album)

---

### 12.  Измените контекст файла /var/www/html/test.html с httpd_sys_content_t на другой (рис. 12). 

*Рис. 12 Изменение контекста:*

![N|Solid](https://sun9-77.userapi.com/impg/qxIgzDPoecDZU4GFRWqrwHN1jXmgVMu10WMluQ/pYk25gdZAWY.jpg?size=2122x210&quality=95&sign=a4c775141b7fdfe4b8eb87fbf444fd79&type=album)

### 13. Попробовали ещё раз получить доступ к файлу через веб-сервер (рис. 13). 

*Рис. 13 Запуск в браузере:*

![N|Solid](https://sun9-21.userapi.com/impg/spFye4MhMHVeBr5VarnjO7X6thVFu5ZfU_960Q/uZvxR64Sk7c.jpg?size=2122x534&quality=95&sign=2ebd93cf57e9ac5744f19ab8b1d2df99&type=album)

---

### 14. Просмотрели log-файлы веб-сервера Apache и системный лог-файл (рис. 14). 

*Рис. 14 Лог-файлы:*

![N|Solid](https://sun9-29.userapi.com/impg/WsErgHTcCiVFKOczO1mIHwdLVqOnFabNh-XNRg/XRNpsz6wyVQ.jpg?size=2122x1308&quality=95&sign=550348333f3e6bbcc084a0e9c6595af1&type=album)

### 15. Попробовали запустить веб-сервер Apache на прослушивание ТСР-порта 81. Для этого в файле /etc/httpd/httpd.conf нашли строчку Listen 80 и заменили её на Listen 81. 

---

### 16. Выполнили перезапуск веб-сервера Apache (рис. 15). 

*Рис. 15 Перезапуск сервера:*

![N|Solid](https://sun9-77.userapi.com/impg/ZJAuX37FZ4NWB-Wf3RJJFQsa_dtFLQP3_vfZBw/8-wWkjESOfw.jpg?size=2122x1308&quality=95&sign=86193e338f269de5f4e696a51ac53ffb&type=album)

---

### 17. Проанализировали лог-файлы (рис. 16). 

*Рис. 16 Лог-файлы:*

![N|Solid](https://sun9-13.userapi.com/impg/lgzNWwXXgFDUvWaYHpzsDlxlpG_10_98Xyliuw/bvC4n6_dzS8.jpg?size=2122x604&quality=95&sign=df62244c3627fed5e4bcc1a7b756af0f&type=album)

---


### 18. Выполнили команду semanage port -a -t http_port_t -р tcp 81. После этого провеили список портов командой semanage port -l | grep http_port_t (рис. 17). 

*Рис. 17 Команды:*

![N|Solid](https://sun9-80.userapi.com/impg/yqCX4mXO30GzWS3wVCOVVfwDLqDmA89HxCgh6A/p-9t33IzSww.jpg?size=2122x490&quality=95&sign=89739928786e3b77114aec9e4f419a29&type=album)

---


### 19. Запустили веб-сервер Apache ещё раз (рис. 18). 

*Рис. 18 Запуск веб-сервера:*

![N|Solid](https://sun9-77.userapi.com/impg/ZJAuX37FZ4NWB-Wf3RJJFQsa_dtFLQP3_vfZBw/8-wWkjESOfw.jpg?size=2122x1308&quality=95&sign=86193e338f269de5f4e696a51ac53ffb&type=album)

---

### 20. Вернули контекст httpd_sys_cоntent__t к файлу /var/www/html/test.html (рис. 19). После этого попробовали получить доступ к файлу через веб-сервер (рис. 20)

*Рис. 19 Возвращение контекста:*

![N|Solid](https://sun9-15.userapi.com/impg/MI98f8pRO6kVUfY1YZJL8O8q0F-YCgxJBdU0dw/vsIteQMT5lA.jpg?size=2122x518&quality=95&sign=7eeb8a503d57754773c62e736968690d&type=album)

*Рис. 20 Запуск в браузере:*

![N|Solid](https://sun9-38.userapi.com/impg/ClFOOQ0cSfWha6T96na6HaKIX_XbrjiWjMEqrA/7ZbTYnCy3d0.jpg?size=2122x490&quality=95&sign=4e63f60b0dc3839fa681c0a8db6aac26&type=album)

---

### 21.  Исправили обратно конфигурационный файл apache, вернув Listen80, удалили привязку http_port_t к 81 порту, удалили файл (рис. 21). 

*Рис. 21 Команды:*

![N|Solid](https://sun9-15.userapi.com/impg/MI98f8pRO6kVUfY1YZJL8O8q0F-YCgxJBdU0dw/vsIteQMT5lA.jpg?size=2122x518&quality=95&sign=7eeb8a503d57754773c62e736968690d&type=album)

---


# Выводы

