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
CREATE TABLE Customers (
    CustomerID int NOT NULL AUTO_INCREMENT,
    CustomerName varchar(255),
    ContactName varchar(255),
    Address varchar(255),
    City varchar(255),
    PostalCode varchar(255),
    Country  varchar(255),
    PRIMARY KEY (CustomerID)
);
describe Customers;

# INSERT INTO Customers (CustomerName, ContactName, Address, City, PostalCode, Country) VALUES ('Alfreds Futterkiste', Maria Anders', 'Obere Str. 57', 'Berlin', '12209', 'Germany');

INSERT INTO Customers VALUES (1, 'Alfreds Futterkiste', 'Maria Anders', 'Obere Str. 57', 'Berlin', '12209', 'Germany');
INSERT INTO Customers VALUES (2, 'Ana Trujillo Emparedados y helados',	'Ana Trujillo', 	'Avda. de la Constitución 2222', 	'México D.F.', 	'05021', 	'Mexico');
INSERT INTO Customers VALUES (3, 'Antonio Moreno Taquería', 'Antonio Moreno','Mataderos 2312', 'México D.F.','05023', 'Mexico');
INSERT INTO Customers VALUES (4, 'Around the Horn','Thomas Hardy','120 Hanover Sq.','London', 'WA1 1DP','UK');
INSERT INTO Customers VALUES (5, 'Berglunds snabbköp','Christina Berglund','Berguvsvägen 8','Luleå', 'S-958 22', 'Sweden');
INSERT INTO Customers VALUES (6, 'Blauer See Delikatessen','Hanna Moos','Forsterstr. 57', 'Mannheim', '68306', 'Germany');
INSERT INTO Customers VALUES (7, 'Blondel père et fils','Frédérique Citeaux',	'24, place Kléber','Strasbourg','67000','France');
INSERT INTO Customers VALUES (8, 'Bólido Comidas preparadas','Martín Sommer', 'C/ Araquil, 67', 'Madrid','28023','Spain');
INSERT INTO Customers VALUES (9, 'Bon app\'','Laurence Lebihans','12, rue des Bouchers','Marseille','13008','France');
```


