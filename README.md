# MySQL-Cheatsheet
MySQL Cheat Sheet 

##ﺕاﺭﻮﺘﺳﺩ

***ﺱیﺏﺎﺗیﺩ یﺮﺑﺭاک ﻩیﺡﺎﻧ ﻪﺑ ﺩﻭﺭﻭ:***  mysql -u [username] -p

***ﺱیﺏﺎﺗیﺩ ﻭ ﻡﺎﻧ ﺎﺑ یﺮﺑﺭاک ﻩیﺡﺎﻧ ﻪﺑ ﺩﻭﺭﻭ:***  mysql -u [username] -p [database]

***ﺎﻫ ﺱیﺏﺎﺗیﺩ ﻩﺪﻫﺎﺸﻣ :***  show databases;

ﺩیﺪﺟ ﺱیﺏﺎﺗیﺩ ﺩﺎﺟیا : ---sql create database [database]; ---

ﺱیﺏﺎﺗیﺩ ﺏﺎﺨﺘﻧا:  use [database];

ﺱیﺏﺎﺗیﺩ کی ﻝﻭاﺪﺟ ﻥﺩاﺩ ﻥﺎﺸﻧ :  show tables;

ﺱیﺏﺎﺗیﺩ ﻝﻭﺪﺟ کی ﺕایﺉﺰﺟ ﻥﺩاﺩ ﻥﺎﺸﻧ :  describe [table];

ﻥﻮﺘﺳ ﺎﺑ ﻝﻭﺪﺟ کی ﻦﺘﺧﺎﺳ :  `CREATE TABLE [table] ([column] VARCHAR(120), [another-column] DATETIME);`

ﻝﻭﺪﺟ یﻭﺭ ﺮﺑ ﻥﻮﺘﺳ ﺩﺎﺟیا :  ALTER TABLE [table] ADD COLUMN [column] VARCHAR(120);

یﺭاﺭکﺕ ﺭیﻍ ﻭ ﺩﺮﻓ ﻪﺑ ﺮﺼﺤﻨﻣ یﺩ یﺁ کی ﺎﺑ ﻥﻮﺘﺳ کی ﺩﺎﺟیا :   `ALTER TABLE [table] ADD COLUMN [column] int NOT NULL AUTO_INCREMENT PRIMARY KEY;`

ﺩﺭﻭکﺭ گی ﺩﺎﺟیا: `SELECT COUNT([column]) FROM [table];`

ﺩﺭﻭکﺭ ﺏﺎﺨﺘﻧا: SELECT * FROM [table];

ﺱیﺏﺎﺗیﺩ ﻝﻭﺪﺟ کی ﺕایﺉﺰﺟ ﻥﺩاﺩ ﻥﺎﺸﻧ :  EXPLAIN SELECT * FROM [table];

ﺩﺭﻭکﺭ کی ﺯا ییﺎﻫ یﺖﻤﺴﻗ ﺏﺎﺨﺘﻧا:  SELECT [column], [another-column] FROM [table];

ﻝﻭﺪﺟ کی یﺎﻫﺩﺭﻭکﺭ ﺩاﺪﻌﺗ ﻥﺩﺭﻭﺁ ﺖﺳﺪﺑ:  SELECT COUNT([column]) FROM [table];

ﺮﻈﻧ ﺩﺭﻮﻣ ﺭیﺩﺎﻘﻣ ﺎﺑ ﺎﻫﺩﺭﻭکﺭ ﺏﺎﺨﺘﻧا:  [value]: SELECT * FROM [table] WHERE [column] LIKE '%[value]%';

ﺩﺩﺭگ یﻡ ﺰﻏﺁ ﻩک ﺭیﺩﺎﻘﻣ ﺎﺑ ﺎﻫﺩﺭﻭکﺭ ﺏﺎﺨﺘﻧا:   [value]: SELECT * FROM [table] WHERE [column] LIKE '[value]%';

ﺮﻈﻧ ﺩﺭﻮﻣ ﺞﻧﺭ ﺎﺑ ﺎﻫﺩﺭﻭکﺭ ﺏﺎﺨﺘﻧا  :  SELECT * FROM [table] WHERE [column] BETWEEN [value1] and [value2];

ﺱیﺏﺎﺗیﺩ ﻩی ﺭیﺩﺎﻘﻣ یﻥﺎﺳﺭ ﺯﻭﺭ ﻪﺑ :  UPDATE [table] SET [column] = '[updated-value]' WHERE [column] = [value];

ﺩﺭﻭکﺭ کی ﺭیﺩﺎﻘﻣ ﻥﺩﺭک کاپ :  DELETE FROM [table] WHERE [column] = [value];

ﻝﻭﺪﺟ کی یﺎﻫ ﻥﻮﺘﺳ ﻥﺩﻮﻤﻧ کاپ  :  ALTER TABLE [table] DROP COLUMN [column];

 ﻝﻭاﺪﺟ ﻥﺩﻮﻤﻧ اپ:  DROP TABLE [table];
 
 ﺱیﺏﺎﺗیﺩ ﻥﺩﻮﻤﻧ کاپ :  DROP DATABASE [database];
 
 پاکﺏ ﺕﺭﻮﺻ ﻪﺑ ﺱیﺏﺎﺗیﺩ کی ﺯا ﻦﺘﻓﺭگ یﺝﻭﺮﺧ :   mysqldump -u [username] -p [database] > db_backup.sql
 
 ﺱیﺏﺎﺗیﺩ کی ﺕﺎﻋﻼﻃا ﻥﺩﻮﻤﻧ ﺩﺭاﻭ : mysql -u [username] -p -h localhost [database] < db_backup.sql
 
 ﺝﻭﺮﺧ : exit;
 
 
##ﻥاﺮﺑﺭاک ﻪﺑ ﻁﻮﺑﺮﻣ ﻊﺑاﻮﺗ

ﻥاﺮﺑﺭاک ﺖﺳیﻝ  : SELECT User,Host FROM mysql.user;
 
 ﺩیﺪﺟ ﺮﺑﺭاک کی ﺩﺎﺣیا :  CREATE USER 'username'@'localhost' IDENTIFIED BY 'password';
 
 ﺱیﺏﺎﺗیﺩ کی ﻪﺑ ﺮﺑﺭاک یﺱﺮﺘﺳﺩ ﺩﺎﺟیا :  GRANT ALL ON database.* TO 'user'@'localhost';
 
 
 
 













