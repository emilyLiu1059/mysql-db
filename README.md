# mysql-db
- https://docs.yugabyte.com/preview/sample-data/northwind/
- https://en.wikiversity.org/wiki/Database_Examples/Northwind
- https://en.wikiversity.org/wiki/Database_Examples/Northwind/MySQL  
```
sudo rpm --import https://repo.mysql.com/RPM-GPG-KEY-mysql-2022
wget http://dev.mysql.com/get/mysql57-community-release-el7-8.noarch.rpm
sudo yum localinstall -y mysql57-community-release-el7-8.noarch.rpm
sudo yum install -y mysql-community-server
```
```
sudo systemctl start mysqld 
sudo systemctl enable mysqld
```

```
sudo grep 'temporary password' /var/log/mysqld.log
mysql -u root -p
```
```
ALTER USER 'root'@'localhost' IDENTIFIED BY '{mypass}';
exit;
```
```
GRANT ALL ON *.* to root@'%' IDENTIFIED BY '{mypass}'   # make ip/hostname available for access from another vm
FLUSH PRIVILEGES;
```
```
# mysql --host=localhost --user=myname --password=password mydb
# mysql -h localhost -uusername -ppassword mydb
```

```
mysql -u username -p pass yourdb < my.sql
```

```
CREATE DATABASE emilydb;
show databases;
mysql -uroot -pmypass emilydb;
show tables;
describe Customers;

```



