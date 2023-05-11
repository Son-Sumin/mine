## Oracle Database Express Edition(XE), Oracle SQL Developer
<br>

- [Oracle Database Express Edition(XE)](https://www.oracle.com/database/technologies/xe-downloads.html)   
  압축 해제 > setup.exe 실행 > 설치 시작 > 설치 중 설치경로 지정 가능 > 비밀번호(암기) > 완료   
  시스템변수 추가(C:\app\USER\product\21c\dbhomeXE\bin)   
  바탕화면 하단 작업 표시줄에서 '서비스' 검색 > OracleServicetXE와 Oracle~Listener 확인   
  ```
  상태 : 실행   
  시작유형 : 확인   
  ```
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
     ```
     서버 최고 관리자 : system 또는 sys
     ```
    [참고링크](https://jenny-daru.tistory.com/4)
   
- [Oracle SQL Developer](https://www.oracle.com/database/sqldeveloper/technologies/download/)
  압축 해제 > 'C:\' 경로 이동
