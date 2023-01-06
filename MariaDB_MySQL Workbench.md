## MariaDB - MySQL Workbench

- [MariaDB 10.5.18 다운로드](https://mariadb.org/download/?t=mariadb&p=mariadb&r=10.5.18&os=windows&cpu=x86_64&pkg=msi&m=blendbyte)   
  x86_64 확인 후 다운로드 > 설치   
  MariaDB cmd promp 관리자 버전 접속 > #mariadb -u root -p > #root 비밀번호 설정
  <br>
  
- [MySQL Workbench 다운로드](https://dev.mysql.com/downloads/workbench/)   
  Windows(x86, 64-bit), MSI Installer(8.0.31) 다운로드 > No thanks, just start my download > VC_redist.x64.exe > 설치   
  <br>   
  
 - MariaDB cmd promp 관리자 버전 접속 > #mariadb -u root -p > #비밀번호 입력 > #show databases; > 잘 나오면 완료   
   <br>
   
 - MySQL Workbench
   * root 계정
     ---create database cocktaildb default character set utf8mb4;   
     ---create user 'cocktaildb'@'%' identified by '1234';   
     ---create user 'cocktaildb'@'localhost' identified by '1234';   
     ---grant all privileges on cocktaildb.* to 'cocktaildb'@'%';   
     ---grant all privileges on cocktaildb.* to 'cocktaildb'@'localhost';   
     ---flush privileges;   
  
