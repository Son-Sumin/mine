## 웹 개발 간 Swagger 사용하기 위한 추가할 기본 내용

**Gradle**
 - build.gradle에 추가할 dependency
```
  // Swagger2 gradle
  implementation (group: 'io.springfox', name: 'springfox-swagger2', version: '2.9.2'){
      exclude module: 'swagger-annotations' exclude module: 'swagger-models'
  }
  implementation "io.swagger:swagger-annotations:1.5.21"
  implementation "io.swagger:swagger-models:1.5.21"
  implementation group: 'io.springfox', name: 'springfox-swagger-ui', version: '2.9.2'
```
<br>

**Maven**
 - pom.xml에 추가할 dependency   
```
    <!-- springfox-swagger2 -->
    <dependency>
      <groupId>io.springfox</groupId>
      <artifactId>springfox-swagger2</artifactId>
      <version>2.9.2</version>
      <exclusions>
        <exclusion>
          <groupId>io.swagger</groupId>
          <artifactId>swagger-annotations</artifactId>
        </exclusion>
        <exclusion>
          <groupId>io.swagger</groupId>
          <artifactId>swagger-models</artifactId>
        </exclusion>
      </exclusions>
    </dependency>
    
    <!-- springfox-swagger-ui -->
    <dependency>
      <groupId>io.springfox</groupId>
      <artifactId>springfox-swagger-ui</artifactId>
      <version>2.9.2</version>
    </dependency>
    <dependency>
      <groupId>io.swagger</groupId>
      <artifactId>swagger-annotations</artifactId>
      <version>1.5.21</version>
    </dependency>
    <dependency>
      <groupId>io.swagger</groupId>
      <artifactId>swagger-models</artifactId>
      <version>1.5.21</version>
    </dependency>
```
<br>

 - configuration 파일에 "@EnableSwagger2" 어노테이션 추가   
