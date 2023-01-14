### global user, email 설정
- git config - -global user.name “user”
- git config - -global user.email “email”
<br>

### repository user, email 설정 (해당 저장소 디렉토리로 이동 후)
- git config user.name “user”
- git config user.email “email”
<br>

### 전역 설정 정보 조회
- (전체정보) git config - -global - -list
- (사용자정보) git config --global user.email
- (사용자정보) git config --global user.name
<br>

### repository 설정 정보 조회
- git config - -list
<br>

### staging, unstaging, untracked 파일 확인
- git status
<br>

* * *

### branch
- branch 목록 조회 ('*' 가 현재 branch)   
  * git branch
- 원격 branch 목록 조회
  * git branch -r
- 전체 branch 목록 조회
  * git branch -a
<br>

* * *

### gitignore 추후 적용   
- git rm -r --cached .
- git add .
- git commit -m '내용'
<br>
