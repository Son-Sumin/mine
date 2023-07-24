## Eclipse

- [Eclipse 다운로드](https://www.eclipse.org/downloads/)   
  Eclipse IDE Download Packages > Eclipse IDE for Enterprise Java and Web Developers > Windows x86_64 설치   

  - 상단 Window > Preferences >   
    encoding 검색 > Content Types > Text 내 모든 항목 UTF-8로 세팅 ( java Properties File 제외)	   
    encoding 검색 > Workspace, Web, XML  UTF-8로 세팅   
    spelling 검색 > Enable spell checking 체크 해제   


  - 상단 Window > Perspective > Open perspective > Java   
    상단 Window > Show View > Project Explorer, Git Repository, Git Staging, Navigator 세팅(없으면 Other... 에서 검색)   
    (우측 상단 javaEE , java 주로 사용하니 참고)

  - 상단 Window > Preferences > Java > 
    Compiler > Compiler compliance level : Java 설치 버전으로 세팅   
    installed JREs > 존재하는거 지우고 jdk 설치 경로 add (C:\Program Files\Java\jdk-12.0.2)   
<br>

- file upload setting   
  - 상단 Window > Preferences >   
    workspace 검색 > Refresh using native hooks or polling 체크   
    ![file upload setting](https://github.com/Son-Sumin/mine/assets/114986832/1d6a321a-56e0-4868-b133-0fe7349aa925)
<br>

- **eclipse - Sringboot 프로젝트 생성**   
  - 상단 Help > Eclipse Marketplace > spring 검색 > Spring Tools4 (aka Spring Tool Suite 4) 설치 > 이클립스 재시작   

  - Springboot 프로젝트 생성 ①   
    [spring initializr](https://start.spring.io/) 활용하여 스프링부트 프로젝트 생성   
    이클립스에서 프로젝트 임포트   

  - Springboot 프로젝트 생성 ②   
    이클립스에서 Create a project > Spring Boot > Spring Starter Project > 아래 사진 참고 하 프로젝트 생성  
    <img src="https://github.com/Son-Sumin/mine/assets/114986832/b0e4528e-603f-4641-8f24-679e5df38e55" width="600" height="450"/>   
    <img src="https://github.com/Son-Sumin/mine/assets/114986832/c501489e-0bac-4151-9026-b54a3ce0483f" width="600" height="450"/>   

  - git 연결   
    - [참고 링크](https://github.com/Son-Sumin/mine/blob/main/git.md)   

  - Lombok   
    - [Lombok 다운로드](https://projectlombok.org/download)   
    - [Lombok 설치 및 적용](https://github.com/Son-Sumin/mine/blob/main/Lombok%20%EC%84%A4%EC%B9%98%20%EB%B0%8F%20%EC%A0%81%EC%9A%A9.md)

<br> 
* * *
<br>

### 이클립스 삭제   
이클립스는 별도의
