▶ 리눅스 처음 접속 후 터미널 실행 

$date
$cal
$whoami
$ping  -c  8.8.8.8


▶ 패키지 설치 
$sudo  apt  list  --installed | nl         ## 설치된 패키지 목록 
$sudo  apt  list  --installed | grep  mysql ## mysql 설치 확인 
$sudo  apt  list  --installed | grep  ssh   ## ssh 설치 확인 
$sudo  apt  -y  install  openssh-server     ## 설치 

$who

▶ ping test  
$ping  8.8.8.8  -c3

▶ mysql-server 설치 
$ sudo apt  -y  install mysql-server

▶ mysql-server root로 접속 
$sudo mysql -u root
mysql>


*******************************************


▶ mysql 계정 만들기

mysql> use mysql
mysql> show  tables;
mysql> create  database acedb;
mysql> show  databases;

## root password 지정 

mysql> alter  user  'root'@'localhost' identified with mysql_native_password by 'jj';
mysql> flush privileges;

## mysql 계정(account) 만들기 

계정(account)
id : ace
pw : 1234
사용DB : acedb



mysql> create  user ace@'%' identified by '1234';
mysql> grant all privileges on acedb.*  to  ace@'%' with grant option;
mysql> flush  privileges;



▶ 다른 터미널 : putty 새로 열기 

j@j:~$ mysql  -u  ace  -p1234

mysql> select user();
mysql> show  databases;
mysql> use  acedb;
Database changed
mysql> use mysql     ## 에러나면 정상 
ERROR 1044 (42000): Access denied for user 'ace'@'%' to database 'mysql'



*******************************************

mysql> use mysql
mysql> show  tables;
mysql> create  database acedb;
mysql> show  databases;

## root password 지정 

mysql> alter  user  'root'@'localhost' identified with mysql_native_password by 'jj';
mysql> flush privileges;

## mysql 계정(account) 만들기 

계정(account)
id : ace
pw : 1234
사용DB : acedb



mysql> create  user ace@'%' identified by '1234';
mysql> grant all privileges on acedb.*  to  ace@'%' with grant option;
mysql> flush  privileges;



▶ 다른 터미널 : putty 새로 열기 

j@j:~$ mysql  -u  ace  -p1234

mysql> select user();
mysql> show  databases;
mysql> use  acedb;
Database changed
mysql> use mysql     ## 에러나면 정상 
ERROR 1044 (42000): Access denied for user 'ace'@'%' to database 'mysql'
mysql>




*************************************

$ sudo  apt  -y  install  apache2
$ sudo service  apache2  start
$ ps -ef | grep  apache
$ cd  /var/www/html/
$ pwd
$ sudo mv  index.html  old.html
$ sudo  vi  index.html
  ### ESC 누른 후 i를 누를 후 아래 입력 
 
<meta charset="UTF-8">
<h1><center><hr><br>
<body  bgcolor=green  text=white><br>
안녕하세요. 양주종입니다.
<br><br><hr>

  
 ###입력 후  ESC 누른 후 :x  입력 하면 저장 종료됨.

 이후 브라우저에서 확인  127.0.0.1

 
