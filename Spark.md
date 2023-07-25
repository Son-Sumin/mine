## Spark   
- 현재 Local에 Java12, 가상환경에 Python 3.8를 설치해 놓은 상태임   
  * [Java 설치](https://www.oracle.com/kr/java/technologies/javase/jdk12-archive-downloads.html)   
    시스템변수 추가(C:\Program Files\Java\jdk-12.0.2\bin)   
  cmd > #java --version > 버전 출력되면 설치 완료     
  * [가상환경 생성 및 Python 3.8 설치 참고](https://github.com/Son-Sumin/ml_dl/blob/main/%EC%B4%88%EA%B8%B0%EC%84%A4%EC%A0%95.md)
- Spark를 Local에 설치할 것이고, PySpark를 사용할 때는 Python이 설치되어 있는 가상환경에 진입하여 사용 예정임
<br><br><br>

- ### [Spark](https://spark.apache.org/downloads.html)   
  'Download Spark' 클릭 > 여러 .tgz 파일 중 하나 다운로드   
  내 PC > C: >  'Spark' 폴더 생성 > 방금 다운받은 tgz 파일을 폴더 안으로 이동   
  tgz 압축 해제 (압축 해제 방법 아래 참고)   
  시스템변수 추가(C:\Spark\spark-3.4.1-bin-hadoop3\bin) 
  - cmd   
  ```
    .tgz 파일이 있는 디렉토리로 이동 후
    $ tar -xvzf 파일이름.tgz
  ```  
  <img src="https://github.com/Son-Sumin/mine/assets/114986832/98774de9-659f-4c4e-81de-2c640848679b" width="450" height="350"/>
  <img src="https://github.com/Son-Sumin/mine/assets/114986832/e967a908-2d14-4063-b6ab-831a6f64bad1" width="450" height="350"/>
  <br><br><br>

- ### [Winutils](http://github.com/cdarlint/winutils)   
  - 분산 처리 환경으로부터 데이터를 하나의 실행 환경에서 다루는 것처럼 해주므로 Spark는 Hadoop이 필요함   
    그 Hadoop 역할을 하는 것이 Winutils   
  
  내 PC > C: >  'Hadoop ' 폴더 생성 > Hadoop 폴더 안에 'bin' 폴더 생성   
  Spark 버전에 맞는 'hadoop-x.x.x/bin' 클릭 >  방금 생성한 bin 폴더 안에 winutils.exe 파일 다운로드   
  시스템변수 추가(C:\Hadoop\bin)    

<br><br>

- 설치 확인  
  cmd   
  ```
    $ pip install pyspark
  
    - Scala 사용할 경우
    $ spark-shell
    
    - Python 사용할 경우
    $ pyspark
  ```
  - [Apache Spark란?](https://yuna96.tistory.com/83#google_vignette)
  - [스파크 자료구조](https://blog.naver.com/pjt3591oo/222724676035)   

<br><br>

* * *

<br>

### TroubleShooting
- 에러내용 :    
  Error [WinError 225] 파일에 바이러스 또는 기타 사용자 동의 없이 설치된 소프트웨어가 있기 때문에 작업이 완료되지 않았습니다 while executing command python setup.py egg_info
- 해결방안 :
   > Window 검색창 > 설정 > 개인 정보 및 보안 > Windows 보안 > 바이러스 및 위협 방지 > 앱열기   
     > (앱 활성화) 설정 > 보호 > 실시간 보호 활성화 끔   
     10분 후에 자동으로 켜진다고 하니 잠깐 끄고 설치하기
   <img src="https://github.com/Son-Sumin/mine/assets/114986832/33e3468d-c27e-468d-90f4-9db1e281fd4e" width="450" height="350"/>  
   <img src="https://github.com/Son-Sumin/mine/assets/114986832/ea6bfc21-d73d-4b59-a1e6-a5c07f996ae6" width="450" height="350"/>


<br><br>

* * *

<br>

### REFERENCE   
- Windows 에 Apache Spark 설치  
  - https://dibrary.tistory.com/89#recentComments   
  - https://ahnty0122.tistory.com/22   
  - https://yuna96.tistory.com/83#google_vignette   
  - https://spidyweb.tistory.com/199     

- TroubleShooting
  - https://wubl.net/%EC%9C%88%EB%8F%84%EC%9A%B0-%ED%8C%8C%EC%9D%BC%EC%97%90-%EB%B0%94%EC%9D%B4%EB%9F%AC%EC%8A%A4-%EB%98%90%EB%8A%94-%EA%B8%B0%ED%83%80-%EC%82%AC%EC%9A%A9%EC%9E%90-%EB%8F%99%EC%9D%98-%EC%97%86%EC%9D%B4/   
