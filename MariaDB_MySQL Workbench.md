## MariaDB - MySQL Workbench
- 아래 기재된 버전은 글 작성 시 버전이므로 설치 당시의 최적화 버전을 설치하면 됨   
<br>

- [MariaDB 10.5.18 다운로드](https://mariadb.org/download/?t=mariadb&p=mariadb&r=10.5.18&os=windows&cpu=x86_64&pkg=msi&m=blendbyte)   
  - MariaDB Server Version 선택 시 버전 뒤에 Alpha, RC 등이 없는 것으로 선택할 것을 권장함   
  - 운영체계, x86_64, MSI 확인 후 다운로드 > Modify password~, Use UTF8~ check > 설치   
    MariaDB cmd promp 관리자 버전 접속 > #mariadb -u root -p > #root 비밀번호 설정   
  - **root 비밀번호 메모 必**
  <br>
  
- [MySQL Workbench 다운로드](https://dev.mysql.com/downloads/workbench/)   
  Windows(x86, 64-bit), MSI Installer(8.0.31) 다운로드 > No thanks, just start my download >   
  (설치간 에러 발생 시 링크 설치 후 MySQL 설치) [VC_redist.x64.exe](https://github.com/Son-Sumin/mine/blob/main/VC_redist.x64.exe) > 설치   
  <br>   
  
 - MariaDB cmd promp 관리자 버전 접속   
 ---mysql -u root -p > 비밀번호 입력  
 ---show databases; > 잘 나오면 완료   
   <br>
   
 - MySQL Workbench
   * root 계정 생성   
     - '+' > Connection name, Username : root 입력 > Test Connection > ok   
   * 일반 계정 생성 (root 계정 들어가서 아래 입력)     
     - database 생성   
     ---create database cocktaildb default character set utf8mb4;   
     - user 생성   
     ---create user 'cocktaildb'@'%' identified by '1234';   
     ---create user 'cocktaildb'@'localhost' identified by '1234';   
     - 권한 부여   
       % : 모든 대상   
       localhost : 해당 ip   
     ---grant all privileges on cocktaildb.* to 'cocktaildb'@'%';   
     ---grant all privileges on cocktaildb.* to 'cocktaildb'@'localhost';   
     - 새 변경사항 적용   
     ---flush privileges;   
     - 모든 user 확인   
     ---use mysql;   
     ---select user, host from user;   
