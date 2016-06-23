# MySQL-Cheatsheet
MySQL Cheat Sheet 

دستورات

ورود به ناحیه کاربری دیتابیس:  mysql -u [username] -p

ورود به دیتابیس با نام کابیس:  mysql -u [username] -p [database]

مشاهده دیتابیس ها :  show databases;

ایجاد دیتابیس جدید :  create database [database];

انتخاب دیتابیس:  use [database];

نشان دادن جداول یک دیتابیس :  show tables;

نشان دادن جزئیات یک جدول دیتابیس :  describe [table];

ساختن یک جدول با ستون :  CREATE TABLE [table] ([column] VARCHAR(120), [another-column] DATETIME);

ایجاد ستون بر روی جدول :  ALTER TABLE [table] ADD COLUMN [column] VARCHAR(120);

ایجاد یک ستون با یک آی دی منحصر به فرد و غیر تکراری :   ALTER TABLE [table] ADD COLUMN [column] int NOT NULL AUTO_INCREMENT PRIMARY KEY;







