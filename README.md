# mysql-db
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
CREATE DATABASE emilydb;
show databases;
mysql -uroot -pmypass emilydb;
show tables;
```
```
CREATE TABLE Persons (
    PersonID int,
    LastName varchar(255),
    FirstName varchar(255),
    Address varchar(255),
    City varchar(255)
);
describe Persons;

```

