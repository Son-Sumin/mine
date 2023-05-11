## Oracle Developer 기본 명령어
<br>

- 사용자 생성   
  ``` sql
    CREATE USER 사용자이름 IDENTIFIED BY 비밀번호;
  ```
<br>

- 권한 부여   
  - 생성된 사용자 계정에 권한을 부여   
  - connect: DB에 접속을 위한 권한   
  - resource: 테이블 생성을 위한 권한   
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

    ```
<br>

- 테이블 구조 확인   
  ``` sql
    DESC 테이블명;
  ```

<br><br>

<참고 사이트>
- [DBMS 오라클 SQL DEVELOPER 단축키 정리](https://jhnyang.tistory.com/entry/DBMS-%EC%98%A4%EB%9D%BC%ED%81%B4-SQL-DEVELOPER-%EB%8B%A8%EC%B6%95%ED%82%A4-%EC%B4%9D%EC%A0%95%EB%A6%AC)
- [[Oracle]SQLDeveloper-기본 명령어/테이블 생성하기](https://ga-you-ni.tistory.com/37)
