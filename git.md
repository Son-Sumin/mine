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

### branch 생성, 이동, 삭제
- branch 생성 및 생성된 branch로 전환
  * git checkout -b <branch 이름>
- branch 생성
  * git branch <branch 이름>
- branch로 전환
  * git checkout <branch>
- local branch 삭제
  * git branch -d <branch 이름> 
- local branch 강제 삭제(위 경우 불가 시 사용)
  * git branch -D <branch 이름>
 - remote branch 삭제
  * git push <remote 이름> —delete <branch 이름>
  <br>

### branch 조회 및 관리, 작업
- branch 목록 조회 ('*' 가 현재 branch)   
  * git branch
- 원격 branch 목록 조회
  * git branch -r
- 전체 branch 목록 조회
  * git branch -a
 <br>

- branch에 push
  * git push origin <branch 이름>
- 원격저장소 내용을 branch 로컬저장소로 가져오기   
  * git pull <remote 이름> <branch 이름>   
<br>

### merge
- merge하기 위해서는 merge하는 branch로 이동 후 merge하려는 branch를 합쳐야한다.   
   * git checkout <branch 이름>   
     git merge <branch 이름>   
 
> 예시) main에  A branch를 merge하기   
        git checkout main   
        git merge A

 
* * *

### gitignore 추후 적용   
- git rm -r --cached .
- git add .
- git commit -m '내용'
<br>
