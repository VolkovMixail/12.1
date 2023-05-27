# Домашнее задание к занятию 12.1 "Базы данных - Волков М.П."


### Легенда

Заказчик передал вам [файл в формате Excel](https://github.com/netology-code/sdb-homeworks/blob/main/resources/hw-12-1.xlsx), в котором сформирован отчёт. 

На основе этого отчёта нужно выполнить следующие задания.

### Задание 1

Опишите не менее семи таблиц, из которых состоит база данных:

- какие данные хранятся в этих таблицах;
- какой тип данных у столбцов в этих таблицах, если данные хранятся в PostgreSQL.

Приведите решение к следующему виду:

Сотрудники (

- идентификатор, первичный ключ, serial,
- фамилия varchar(50),
- ...
- идентификатор структурного подразделения, внешний ключ, integer).
___

**Ответ**

Какие данные хранятся в этих таблицах :

1 фио  - фамилия имя и отчество сотрудника 

2 ОКЛАД  - заработная плата сотрудника

3 должность  - Занимаемая должность сотрудника

4 Тип подразделения - отдел в котором работает сотрудник

5 Дата - дата найма сотрудника

6 Адрес - местонахождение филиала

7 Проэкт - наименование проэкта для конкретного сотрудника.
___

Какой тип данных у столбцов в этих таблицах, если данные хранятся в PostgreSQL.

1 фио  -  строковый (varchar)

2 ОКЛАД  - числовой (decimal/numeric)

3 должность  - строковый (varchar)

4 Тип подразделения - строковый (varchar)

5 Дата - дата и время (tinyint)

6 Адрес - местонахождение филиала (varchar)

7 Проэкт - строковый (varchar)
___
решение к следующему виду: 


staff (

 staff_id primary_key,

 fname varchar(50) ,
 
 lname varchar(50) ,
 
 patronymic varchar(50),

 divisions_id varchar(50),
 
 structura_id varchar(50),
 
 date_off_id datetime,
 
 position_id varchar(50),
 
 salary_id numeric,
 
 address_id varchar(50),
 
 project_id varchar(50),
 
)

salary (

salary_id primary_key

pay numeric

)

position (

position_id primary_key

spethion_type

)

divisions (

divisions_id primary_key

department varchar(50)

unit group varchar(50)

unit group_type

department_type

)

structura (

structura_id primary_key

group varchar(50)

structura_type 

structura_title

)


date_off_Employee )

date_off_id primary_key

date datetime

(


branch address (

address_id primary_key

edge varchar(50)

city varchar(50)

street varchar(50)

house varchar(50)

)

project (

project_id primary_key

project_type

)
