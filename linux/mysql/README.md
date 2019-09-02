# Summary

## url

https://www.runoob.com/linux/mysql-install-setup.html

## 登录mysql

mysql -u robotlocal -p

##  查看全局变量

show variables like '%general%'; 






# Usage

show variables like '%general%';

show variables like 'log%';

SET GLOBAL general_log = 'ON';

SET GLOBAL general_log_file = '/var/lib/mysql/mysql.log';



mysql -u robotlocal -p





  (3) 自动提交

show variables like '%AUTOCOMMIT%';



​     若把 AUTOCOMMIT 设置为 ON ，则在插入、修改、删除语句执行后，系统将自动进行提交，这就是自动提交。其格式为： SQL>SET AUTOCOMMIT ON ；



show variables like '%max_connections%';

show processlist;