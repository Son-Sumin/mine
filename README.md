# tool 설치 및 세팅, git 명령어 정리, Deployment
> - [git 명령어 정리](https://github.com/Son-Sumin/mine/blob/main/git.md)   
> - [github markdown emoji markup](https://gist.github.com/rxaviers/7360908)   
>    
> - [Deployment](https://github.com/Son-Sumin/springboot-test/tree/main/deployment)
<br>

## tool 설치 및 세팅   
- [MariaDB - MySQLWorkbench](https://github.com/Son-Sumin/mine/blob/main/MariaDB_MySQL%20Workbench.md)   
  MariaDB 설치 > [VC_redist.x64.exe](https://github.com/Son-Sumin/mine/blob/main/VC_redist.x64.exe) 설치 > MySQLWorkbench 설치 >   
  시스템변수 추가(C:\Program Files\MariaDB 10.5\bin)   
  cmd > #mariadb --version > 버전 출력되면 설치 완료   
  cmd > #mysql --version > 버전 출력되면 설치 완료   
  <br>
  
- [VS Code](https://code.visualstudio.com/Download)   
  User Installer 64bit 설치 > 시스템변수 추가(C:\Users\user\AppData\Local\Programs\Microsoft VS Code\bin)   
  * Extensions 설치 권장   
    - Live Server    
    - Auto Rename Tag   
    - HTML to CSS autocompletion/solnurkarim   
    - ESLint   
    - File & Folder Icons   
    - JavaScript (ES6) code snippets   
    - Jupyter   
    - ES7+ React/Redux/React-Native snippets   
    - Prettier   
    - Live Sass Compiler   
    - Sass   
    - Live Preview   
  <br>
 
- [Java](https://www.oracle.com/kr/java/technologies/javase/jdk12-archive-downloads.html)   
  시스템변수 추가(C:\Program Files\Java\jdk-12.0.2\bin)   
  cmd > #java --version > 버전 출력되면 설치 완료   
  <br>
  
- [Eclipse](https://github.com/Son-Sumin/mine/blob/main/Eclipse.md)   
  <br>
  
- [Pycharm](https://github.com/Son-Sumin/python-practices/blob/main/1017%20%ED%8C%8C%EC%9D%B4%EC%B0%B8%20%EC%84%A4%EC%B9%98.md) (pip 활용)   
  [Pycharm 설치](https://www.jetbrains.com/ko-kr/pycharm/download/#section=windows)   
  community 다운로드 > 시스템변수 추가(C:\Program Files\JetBrains\PyCharm Community Edition 2022.3.1\bin)
  <br>

- [Linux 세팅](https://github.com/Son-Sumin/Linux)
  * VirtualBox, Xshell5   
  * tomcat, java, git, mariadb, maven, jenkins, 기존 프로젝트 jenkins 실행   
  * 고정아이피 설정   
  <br>
  
- [빅데이터 & 인공지능(AI)](https://github.com/Son-Sumin/ml_dl/blob/main/%EC%B4%88%EA%B8%B0%EC%84%A4%EC%A0%95.md)
  * jupyter와 Windows Terminal로 miniconda 설치 및 세팅   
  * scraping
  <br>
  
- [django 세팅](https://github.com/Son-Sumin/django)   
  * Django - Pycharm - MariaDB   
  * django로 project-app 생성   
  <br>
   
- 기타 설치 권장 Tool   
  * [Git](https://git-scm.com/download/win)   
    cmd > #git --version > 버전 출력되면 설치 완료
  * [Tomcat](https://tomcat.apache.org/download-90.cgi)   
    [Tomcat 설치 확인](https://www.iotworks.co.kr/xe/index.php?mid=Server&document_srl=59397)
  * [jenkins](https://github.com/Son-Sumin/Linux/tree/main/%EC%84%A4%EC%B9%98)   
  * [VirtualBox, Xshell5, CentOS7](https://github.com/Son-Sumin/Linux)    
  * [Ubuntu](https://ubuntu.com/download/desktop)   
  * [BootStrap](https://getbootstrap.com/docs/3.4/getting-started/)   
  * [Node.js](https://nodejs.org/ko/download/)   
    (Node.js 설치 시 npm 자동 설치됨)   
    Windows Installer(.msi) 64-bit 다운로드 > 시스템변수 추가(C:\Program Files\nodejs\)   
    cmd > #node --version > 버전 출력되면 설치 완료
  * [Miniconda, Jupyter](https://github.com/Son-Sumin/ml_dl/blob/main/%EC%B4%88%EA%B8%B0%EC%84%A4%EC%A0%95.md)   
    Microsoft Store > terminal 검색 > Windows Terminal 다운로드   
  * [Lombok](https://projectlombok.org/download)   
    [Lombok 설치 및 Eclipse 적용 불가 시 해결법](https://github.com/Son-Sumin/mine/blob/main/Lombok%20%EC%84%A4%EC%B9%98%20%EB%B0%8F%20%EC%A0%81%EC%9A%A9.md)   
  * [Postman](https://www.postman.com/downloads/)   
  * [Swagger](https://github.com/Son-Sumin/mine/blob/main/Swagger%20dependency.md)   
  * [Redis](https://oingdaddy.tistory.com/225)   
    해당 링크 참고하여 설치 후 확인   
  * MobaXterm
  * [FileZilla Download](https://filezilla-project.org/)   
    Download FileZilla Client
  <br>

- 기타 Tool   
  * [ALPDF](https://www.altools.co.kr/download/alpdf.aspx)   
  * [7-Zip](https://www.7-zip.org/download.html)   
    64-bit Windows x64 다운로드   
  * [Notepad++](https://notepad-plus-plus.org/downloads/)   
  * Windows Terminal   
  * [Slack](https://slack.com/intl/ko-kr/downloads/windows)   
    사이트, 앱으로 사용 가능   
  * Office365   
  * WPS   
  * Google Driver   
    [설치 간 참고 링크](https://github.com/Son-Sumin/ml_dl/tree/main/scraping)   
    (크롤링 selenium을 구글에서 사용할 것이므로 설치)   
    (다른 사이트 크롤링 시 해당 드라이버 설치)   
