# MySQL-Cheatsheet
MySQL Cheat Sheet 

دستورات

ورود به ناحیه کاربری دیتابیس:  mysql -u [username] -p

ورود به ناحیه کاربری با نام و دیتابیس:  mysql -u [username] -p [database]

مشاهده دیتابیس ها :  show databases;

ایجاد دیتابیس جدید :  create database [database];

انتخاب دیتابیس:  use [database];

نشان دادن جداول یک دیتابیس :  show tables;

نشان دادن جزئیات یک جدول دیتابیس :  describe [table];

ساختن یک جدول با ستون :  CREATE TABLE [table] ([column] VARCHAR(120), [another-column] DATETIME);

ایجاد ستون بر روی جدول :  ALTER TABLE [table] ADD COLUMN [column] VARCHAR(120);

ایجاد یک ستون با یک آی دی منحصر به فرد و غیر تکراری :   ALTER TABLE [table] ADD COLUMN [column] int NOT NULL AUTO_INCREMENT PRIMARY KEY;

ایجاد یگ رکورد: INSERT INTO [table] ([column], [column]) VALUES ('[value]', [value]');

انتخاب رکورد: SELECT * FROM [table];

نشان دادن جزئیات یک جدول دیتابیس :  EXPLAIN SELECT * FROM [table];

انتخاب قسمتی هایی از یک رکورد:  SELECT [column], [another-column] FROM [table];

بدست آوردن تعداد رکوردهای یک جدول:  SELECT COUNT([column]) FROM [table];

انتخاب رکوردها با مقادیر مورد نظر:  [value]: SELECT * FROM [table] WHERE [column] LIKE '%[value]%';

انتخاب رکوردها با مقادیر که آغز می گردد:   [value]: SELECT * FROM [table] WHERE [column] LIKE '[value]%';

انتخاب رکوردها با رنج مورد نظر  :  SELECT * FROM [table] WHERE [column] BETWEEN [value1] and [value2];

به روز رسانی مقادیر یه دیتابیس :  UPDATE [table] SET [column] = '[updated-value]' WHERE [column] = [value];

پاک کردن مقادیر یک رکورد :  DELETE FROM [table] WHERE [column] = [value];

پاک نمودن ستون های یک جدول  :  ALTER TABLE [table] DROP COLUMN [column];

 پا نمودن جداول:  DROP TABLE [table];
 
 پاک نمودن دیتابیس :  DROP DATABASE [database];
 
 خروجی گرفتن از یک دیتابیس به صورت بکاپ :   mysqldump -u [username] -p [database] > db_backup.sql
 
 وارد نمودن اطلاعات یک دیتابیس : mysql -u [username] -p -h localhost [database] < db_backup.sql
 
 خروج : exit;
 
 
توابع مربوط به کاربران

 لیست کاربران : SELECT User,Host FROM mysql.user;
 
 ایحاد یک کاربر جدید :  CREATE USER 'username'@'localhost' IDENTIFIED BY 'password';
 
 ایجاد دسترسی کاربر به یک دیتابیس :  GRANT ALL ON database.* TO 'user'@'localhost';
 
 
 
 













