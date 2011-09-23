## 安装 MySQL ##

### 从 yum 安装 MySQL ###

    yum install mysql-server
	yum install mysql-workbench
	
### 配置 ###

	$ sudo vi /etc/my.cnf

```java
	[mysqld]
	...
	# Default character
	character_set_server=utf8

	# connection character
	init_connect='SET NAMES utf8'

	# default engine
	default-storage-engine=INNODB

	[client]

	# default character
	default-character-set=utf8

	# localhost default connection
	#user=root
	#password=123456
	#host=localhost

```

### 启动服务 ###

    # service mysqld start

### 修改成自启动级别 ###

	# chkconfig mysqld on

### 设置密码 ###

    # mysqladmin -u root password '123456'



### MySQL 用户配置 ###

    mysql -u root -p

#### show user info ####

```java
	mysql> select user,host,password from mysql.user;
	+------+-----------------------+-------------------------------------------+
	| user | host                  | password                                  |
	+------+-----------------------+-------------------------------------------+
	| root | localhost             | *6BB4837EB74329105EE4568DDA7DC67ED2CA2AD9 |
	| root | localhost.localdomain |                                           |
	| root | 127.0.0.1             |                                           |
	| root | ::1                   |                                           |
	|      | localhost             |                                           |
	|      | localhost.localdomain |                                           |
	+------+-----------------------+-------------------------------------------+
```

#### set root password for 127.0.0.1 ####
mysql> set password for root@'127.0.0.1'=password('password');

#### set root password for localhost.localdomain ####
mysql> set password for root@'localhost.localdomain'=password('password');

#### delete IPV6 user ####
delete from mysql.user where user='root' and host='::1';

#### delete anonymous user ####
delete from mysql.user where user='';

```java
	mysql> select user,host,password from mysql.user;
	+------+-----------------------+-------------------------------------------+
	| user | host                  | password                                  |
	+------+-----------------------+-------------------------------------------+
	| root | localhost             | *6BB4837EB74329105EE4568DDA7DC67ED2CA2AD9 |
	| root | localhost.localdomain | *6BB4837EB74329105EE4568DDA7DC67ED2CA2AD9 |
	| root | 127.0.0.1             | *6BB4837EB74329105EE4568DDA7DC67ED2CA2AD9 |
	+------+-----------------------+-------------------------------------------+
```

###　修改 Root 密码　###

    mysqladmin -u root password "newpass"
    
    SET PASSWORD FOR 'root'@'localhost' = PASSWORD('newpass');
    
    mysqladmin -u root password oldpass "newpass"
    
    #在丢失root密码的时候，可以这样
    mysqld_safe --skip-grant-tables
    mysql -u root mysql
    mysql> UPDATE user SET password=PASSWORD("new password") WHERE user='root';
    mysql> FLUSH PRIVILEGES;


