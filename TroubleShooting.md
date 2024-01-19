## TroubleShooting

- **에러 내용**
  ```
  PKIX path building failed: sun.security.provider.certpath.SunCertPathBuilderException
  ```
- **해결 방법**   
  참고 : https://www.lesstif.com/system-admin/java-validatorexception-keystore-ssl-tls-import-12451848.html   
- **추가 내용**
  - 해결 도중 cmd에서 ''keytool'은(는) 내부 또는 외부 명령, 실행할 수 있는 프로그램, 또는 배치 파일이 아닙니다.' 나타나면
    1. jdk 있는 곳 (예를 들어 C:\Program Files\Java\jdk-11\bin) 안에 keytool.exe 존재하는지 확인
    2. jdk 환경변수 설정되어 있는지 확인
<br><br>
