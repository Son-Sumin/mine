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
