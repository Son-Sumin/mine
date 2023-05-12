##  SQL Plus, SQL Developer 사용법 및 기본 명령어
-  SQL Plus : SQL 명령어를 직접 입력하여 그 결과를 바로 확인할 수 있는 console 도구 (Oracle 설치시 포함)
-  Oracle Developer : GUI 환경에서 SQL 작업  
- [[Oracle] SQL developer 유용한 환경설정/단축키](https://loghada.tistory.com/12)
<br>

- SYS vs SYSTEM
  - SYS : 오라클 DB 관리자(SUPER USER)로서 DB 생성 가능, /as sysdba 로 접속
  - SYSTEM : 권한은 SYS와 같으나 DB 생성 권한 없음, 패스워드는 설치 시 직접 설정함
<br>

- SQL Plus 사용법
  ```
  ○ 접속방법   
    1. 시작줄 'sql' 검색 > SQL Plus으로 바로 접속  
    2. cmd >
       - SYS계정 외 접속
         $ sqlplus 계정명/비밀번호   
       
       - SYS계정 접속
         $ SQLPLUS "/ as sysdba"
         
       - 로그인 없이 SQLPlus 에 접속한 후 나중에 Connect 또는 Conn 명령어로 DB 로그인
         $ SQLPLUS/nolog
         
         
  ○ SYS계정 로그인 방법
   1 SQL Plus 접속 > 
     사용자명 입력: $ /as sysdba
     
   2 cmd > $ sqlplus "/as sysdba"


  ○ 계정 정보 확인
    - 계정명은 dba_users 테이블의 username 칼럼에 저장되어 있음
        SELECT USERNAME FROM DBA_USERS; 
        
        
  ○ 사용자 생성
    - oracle 12 이상부터 계정명 앞에 'C##' 붙여야함
      $ CREATE USER C##계정명 IDENTIFIED BY 비밀번호;
      
    - 계정명 앞에 'C##' 붙이지 않고 사용자 생성
      $ ALTER SESSION SET "_ORACLE_SCRIPT"=TRUE;
      $ CREATE USER 계정명 IDENTIFIED BY 비밀번호;
      
   
  ○ SQL Plus다른 계정으로 이동
    1. CONN
    2. CONNECT
   ```
<br>

- SQL Developer 사용법   
  - SYS(관리자) 계정으로 접속하기   
    <img src="https://github.com/Son-Sumin/mine/assets/114986832/4c96ff78-6ba5-4df9-ab59-787399813f50" width="600" height="450"/>   
    - 위 그림에 맞게 설치 진행   
      그림에는 '비밀번호 저장'이 check되어 있음(개인용은 상관 없으나 사무실용은 unckeck!)   
      저장 시 좌측 베너에 방금 생성한 접속 이름 생김   

    - 7 저장 후 **The Network Adapter could not establish the connection** 에러 발생시   
      ```
      cmd > $ ipconfig > IPv4 주소 확인   
      Oracle SQL Developer > 호스트 이름 : localhost → IPv4 주소 > 저장   
      ```
    - 추후 생성된 DB에 접속할 때 위 그림에서 테스트 버튼 클릭 시 "상태:성공" 이 되야 접속 가능   
    - 일반 계정으로 접속 시 사용자 계정 생성 후 위 과정 실시
<br>

- 사용자 생성   
  ``` sql
    CREATE USER 사용자이름 IDENTIFIED BY 비밀번호;
  ```
<br>

- 권한 부여   
  - 생성된 사용자 계정에 권한을 부여   
  - CONNECT : 사용자가 DB에 접속 가능하도록 가장 기본적인 시스템 권한 8가지를 묶어놓음 (R 가능)   
  - RESOURCE : 사용자가 객체(테이블, 뷰, 인덱스)를 생성할 수 있는 시스템 권한을 묶어놓음 (CRUD 가능)    
  - DBA : 사용자가 시스템 관리에 필요한 모든 권한을 부여할 수 있는 강력한 권한 (CRUD, DB 조와 보안, 백업 및 복원, 권한 관리 등)
  ``` sql
    GRANT resource, connect TO 사용자이름 ;
  ```
<br>

- 영구저장(DCL)   
  - 오라클에서는 데이터를 추가하면 데이터가 영구 저장되는 것이 아니고 메모리 상에만 추가된 것   
  - 추가한 데이터를 영구적으로 저장하지 않으려면 rollback 명령어로 취소   
  - 데이터를 영구적으로 저장하기 위해서는 commit 명령어 실행   
  ``` sql
    COMMIT;
  ```
<br>

- 현재 사용자 정보   
  ``` sql
    SHOW USER;
  ```
<br>

- 테이블 생성   
  - 테이블명은 가능한 단수형, 다른 테이블과 중복 불가, 반드시 문자로 시작   
  - 각 컬럼은 "," 구분, 테이블 생성문은 ";" 로 종결
  - 컬럼명 뒤에 데이터타입 반드시 지정
  ``` sql
    CREATE TABLE 테이블명(컬럼명 컬럼타입);
  ```
  - 예시   
    <DEPARTMENT 테이블>
    |NO|속성명|칼럼명|자료형|크기|유일키여부|NULL여부|키종류|
    |:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
    |1|DNO|부서번호|NUMBER|2|Y|N|PK|
    |2|DNAME|부서명|VARCHAR|14|N|N||
    |3|LOC|지역명|VARCHAR|13|N|N||
    ``` sql
    -- PK 설정 방법1
      CREATE TABLE DEPARTMENT(
        DNO NUMBER(2) CONSTRAINT PK_DEPT PRIMARY KEY,
        DNAME VARCHAR(14) NOT NULL,
        LOC VARCHAR(13) NOT NULL
      );
      COMMIT;
    ```
    ``` sql
    -- PK 설정 방법2
      CREATE TABLE DEPARTMENT(
        DNO NUMBER(2) NOT NULL,
        DNAME VARCHAR(14) NOT NULL,
        LOC VARCHAR(13) NOT NULL
        CONSTRAINT PK_DEPT PRIMARY KEY(DNO)
      );
      COMMIT;
    ```
    ``` sql
    -- FK 설정 방법1
      CREATE TABLE EMPLOYEE(
        ENO NUMBER(4) CONSTRAINT PK_EMP PRIMARY KEY,
        ...
        DNO NUMBER(2) CONSTRAINT FK_DNO REFERENCES DEPARTMENT
      );
      COMMIT;
    ```
    ``` sql
    -- FK 설정 방법2
      CREATE TABLE EMPLOYEE(
        ENO NUMBER(4) NOT NULL,
        ...
        DNO NUMBER(2) NOT NULL,
        CONSTRAINT PK_EMP PRIMARY KEY(ENO),
        CONSTRAINT FK_DNO FOREIGN KEY(DNO) REFERENCES DEPARTMENT
      );
      COMMIT;
    ```
<br>

- 테이블 구조 확인   
  ``` sql
    DESC 테이블명;
  ```
<br>

- 테이블 삭제
  - DELETE
    - WHERE절 없으면 테이블 전체 삭제, WHERE절 있으면 특정 ROW 삭제
    - COMMIT을 하지 않으면 되돌릴 수 있음
    - 테이블의 데이터를 삭제하지만, 테이블 자체는 그대로 유지
    ``` sql
    DELETE FROM DEPARTMENT;
    DELETE FROM DEPARTMENT WHERE DNO = 1;
    ROLLBACK;
    COMMIT;
    ```
    
  - TRUNCATE
    - 테이블 초기화
    ``` sql
    TRUNCATE TABLE DEPARTMENT;
    ```
    
  - DROP
    - 데이터베이스 객체(테이블, 뷰, 인덱스 등) 자체를 삭제하는 데 사용
    - 해당 객체와 관련된 모든 데이터, 인덱스, 제약 조건 등도 함께 삭제
    - 객체를 삭제하면 해당 객체와 관련된 모든 데이터와 구조가 완전히 제거
    ``` sql
    DROP TABLE DEPARTMENT;
    ```
<br>

- ERD 생성   
  SQL Developer > (상단) 파일 > Data Modeler > 임포트 > 데이터 딕셔너리   
  데이터베이스 선택 후 (하단) 다음 > 임포트하려는 스키마/데이터베이스 선택 > 임포트할 객체(테이블) 선택 > 완료   
  
  - FK 명시적으로 관계되어 있지 않으나 서로 참조관계가 있는 경우   
    암묵적 참조를  추가하고자 하는 테이블 선택 > 우클릭 > implied Foreign Keys Dialog   
    상단 + > Target Object, Local Column, Referenced Object, Referenced Column 선택 > 확인   
<br><br>

<참고 사이트>
- [DBMS 오라클 SQL DEVELOPER 단축키 정리](https://jhnyang.tistory.com/entry/DBMS-%EC%98%A4%EB%9D%BC%ED%81%B4-SQL-DEVELOPER-%EB%8B%A8%EC%B6%95%ED%82%A4-%EC%B4%9D%EC%A0%95%EB%A6%AC)
- [[Oracle]SQLDeveloper-기본 명령어/테이블 생성하기](https://ga-you-ni.tistory.com/37)
- [SQL 계정 설정과 로그](https://hec-ker.tistory.com/97)
