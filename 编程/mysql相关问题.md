进入数据库：
cd  /www/wdlinux/mysql-5.5.62/bin
mysql -u root -p yh_f(数据库名称)

===============

数据导入报错：Got a packet bigger than‘max_allowed_packet’bytes的问题  

2个解决方法：  

1.临时修改：mysql>set global max_allowed_packet=524288000;修改 #512M  

2.修改my.cnf，需重启mysql。 

   在 [MySQLd] 部分添加一句（如果存在，调整其值就可以）：  

   max_allowed_packet=10M

===============


[不能用IP连接Mysql的几个原因]
mysql 连接
mysql -h localhost -P3307 -u root -p
use database;
grant all on * to 'root' identified by '123456';
grant all privileges on *.* to 'root'@'170.168.0.187' identified by '123456';
flush privileges;

mysql允许ip连接：

GRANT ALL PRIVILEGES ON *.* TO 'root'@'%' IDENTIFIED BY '123456' WITH GRANT OPTION;
flush privileges;

=====================

[安装多版本mysql]
linux安装mysql
./mysqld_safe --defaults-file=/www/wdlinux/mysql-5.7.12/my.cnf  --user=root &
./mysqld  --defaults-file=/www/wdlinux/mysql-5.7.12/my.cnf --initialize --user=mysql