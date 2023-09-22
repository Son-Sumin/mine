## Oracle Database Express Edition(XE), Oracle SQL Developer
- Oracle 서버 최고 관리자 : system 또는 sys
<br>

- **방법1**   
  [참고 링크](https://velog.io/@anak_2/Database-DBMS-%EC%84%A4%EB%AA%85-Oracle-DBMS-%EC%84%A4%EC%B9%98%ED%95%98%EA%B8%B0) 통해서 Oracle Database Express Edition(XE), Oracle SQL Developer 설치
<br>

- **방법2**  
  - [Oracle Database Express Edition(XE)](https://www.oracle.com/database/technologies/xe-downloads.html)   
    압축 해제 > setup.exe 실행 > 설치 시작 > 설치 중 설치경로 지정 가능 > 비밀번호(암기) > 완료   
    시스템변수 추가(C:\app\USER\product\21c\dbhomeXE\bin)   
    바탕화면 하단 작업 표시줄에서 '서비스' 검색 > OracleServicetXE와 Oracle~Listener 확인   
      > 상태 : 실행      
      > 시작유형 : 확인   
    
    * 미작동시
      ```
      해당 항목 우클릭 > 실행
      
      단, OracleServicetXE 미실행이면
      Oracle~Listener 정지 후 OracleServicetXE, Oracle~Listener 순차적으로 실행
      ```
    
     * 다른 사람과 같이 사용하려면 방화벽 조정 필요
       ```
       제어판 > 시스템 및 보안 > Windows Defender 방화벽 > (좌측)고급설정 > 인바운드 규칙 > (우측)새규칙
          규칙종류 > 포트 클릭
          프로토콜 및 포트 > 특정 로컬 포트 : 1521
          이름 > Oracle
          마침
       ```
      - 설치 테스트   
        시작 화면에서 'sql' 검색 > SQL Plus 실행 > ID : SYSTEM / PW : 설치 간 설정한 패스워드   
        이상 없으면 Oracle SQL Developer 실행   
          > (경로 참고)   
          > Oracle Database XE : C:\app\USER\product\21c   
          > SQL Plus : C:\ProgramData\Microsoft\Windows\Start Menu\Programs\Oracle - OraDB21Home1\응용 프로그램 개발   
  
  <br><br>
  
  - [Oracle SQL Developer](https://www.oracle.com/database/sqldeveloper/technologies/download/)   
    압축 해제 > 'C:\' 경로 이동 > sqldeveloper.exe 실행    
    
    - 설치 테스트   
      아래 그림에 맞게 설치 진행   
      그림에는 '비밀번호 저장'이 check되어 있음(개인용은 상관 없으나 사무실용은 unckeck!)   
      ![oracle](https://github.com/Son-Sumin/mine/assets/114986832/86dd24ba-81c8-442f-ae74-5bd919eb6a71)
  
      - 6 저장 후 **The Network Adapter could not establish the connection** 에러 발생시   
        ```
        cmd > $ ipconfig > IPv4 주소 확인   
        Oracle SQL Developer > 호스트 이름 : localhost → IPv4 주소 > 저장
        ```
      그림의 <> 과 같이 생성됨   
      좌측 베너 > SYSTEM\테이블(필터링됨)\하위 아무거나 더블클릭 > 나오면 설치 테스트 완료   
      <br>
      
      추후 생성된 DB에 접속할 때 위 그림에서 테스트 버튼 클릭 시 "상태:성공" 이 되야 접속 가능   
  <br><br>

<참고 사이트>   
https://jenny-daru.tistory.com/4     
https://0pen3r.tistory.com/147   
https://velog.io/@anak_2/Database-DBMS-%EC%84%A4%EB%AA%85-Oracle-DBMS-%EC%84%A4%EC%B9%98%ED%95%98%EA%B8%B0
