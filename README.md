# Проект по созданию таблиц в PostgreSQL.
![Klass_proect](https://img.shields.io/badge/Klass_proect-blue?style=flat)

## 📝 Описание проекта
Проект направлен на разработку и внедрение структуры таблиц в базе данных **PostgreSQL** для эффективного хранения и управления данными. **PostgreSQL** является мощным и открытым сервером реляционных баз данных, известным своей надежностью и функциональностью.


## 🚀 Установка

1. Создайте таблицы:

```bash
    CREATE TABLE surname ( 
    surname_id INT PRIMARY KEY,
    surname VARCHAR(50) 
);
 ```
```bash
CREATE TABLE name ( 
    name_id INT PRIMARY KEY,
    name VARCHAR(50)
);
```
 ```bash
CREATE TABLE patronymic ( 
    patronymic_id INT PRIMARY KEY,
    patronymic VARCHAR(50)
);
    ```

2. Загрузите данные в таблицы:

 ```bash
   INSERT INTO surname (surname_id, surname) VALUES 
    ('1', 'Иванов'),
    ('2', 'Петров'),
    ('3', 'Сидоров');
```
```bash
INSERT INTO name (name_id, name) VALUES 
    ('1', 'Иван'),
    ('2', 'Петр'),
    ('3', 'Сидор');
```
 ```bash
INSERT INTO patronymic (patronymic_id, patronymic) VALUES 
    ('1', 'Иванович'),
    ('2', 'Петрович'),
    ('3', 'Сидорович');
    ```

3. Проверьте данные:

    Выполните следующий скрипт, чтобы инициализировать базу данных SQLite:

    
SELECT *
FROM surname 
FULL JOIN name ON surname_id = name_id
FULL JOIN patronymic ON name_id = patronymic_id;


## 🥳 Заключение.

Создание таблиц в PostgreSQL требует тщательного планирования и реализации для обеспечения надежности и производительности. Этот проект позволит эффективно управлять данными, поддерживая их целостность и готовность к масштабированию в будущем.
