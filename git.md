### git 최초 설치 시  
$ git config --global user.name “user”   
$ git config --global user.email “email”   

(user, email 입력 잘 되었는지 확인 아래 중 1개 실행)   
$ git config --global --list   
$ cat ~/.gitconfig   
(잘 완료되었다면 앞으로 로컬에서 git add/commit/push 진행 시 확인된 내용으로 진행)   

(local storage 내 계정 등록)
$ git config --global user.name “user”   
$ git config --global user.email “email”   

(local storage 등록 확인)
$ git config --list   
<br>

### global user, email 설정
$ git config --global user.name “user”   
$ git config --global user.email “email”   
<br>

### repository user, email 설정 (해당 저장소 디렉토리로 이동 후)   
$ git config user.name “user”   
$ git config user.email “email”   
<br>

### 전역 설정 정보 조회   
$ (전체정보) git config --global - -list   
$ (사용자정보) git config --global user.email   
$ (사용자정보) git config --global user.name   
<br>

### repository 설정 정보 조회   
$ git config --list   
<br>

### staging, unstaging, untracked 파일 확인   
$ git status   
<br>

* * *

### branch 생성, 이동, 삭제   
- branch 생성 및 생성된 branch로 전환   
  $ git checkout -b <branch 이름>   
- branch 생성   
  $ git branch <branch 이름>   
- branch로 전환   
  $ git checkout <branch>   
- local branch 삭제   
  $ git branch -d <branch 이름>   
- local branch 강제 삭제(위 경우 불가 시 사용)   
  $ git branch -D <branch 이름>   
 - remote branch 삭제   
  $ git push <remote 이름> --delete <branch 이름>   
  <br>

### branch 조회 및 관리, 작업   
- branch 목록 조회 ('*' 가 현재 branch)   
  $ git branch   
- 원격 branch 목록 조회   
  $ git branch -r   
- 전체 branch 목록 조회   
  $ git branch -a   
 <br>

- branch에 push   
  $ git push origin <branch 이름>   
- 원격저장소 내용을 branch 로컬저장소로 가져오기    
  $ git pull <remote 이름> <branch 이름>   
<br>

### merge   
- merge하기 위해서는 merge하는 branch로 이동 후 merge하려는 branch를 합쳐야한다.   
   $ git checkout <branch 이름>   
   $ git merge <branch 이름>   
 
> 예시) main에  A branch를 merge하기   
      $ git checkout main   
      $ git merge A   

 * * *
 
### compare&pull request 불가 시   
- 에러 내용 : "There isn't anything to compare"   
  $ git checkout master   
  $ git branch main master -f   
  $ git checkout main   
  $ git push origin main -f   
<br>
 
### compare&pull request 불가 시   
- 에러 내용 : pathspec 'main' did not match any file(s) known to git   
  $ git remote update   
 
* * *

### gitignore 추후 적용   
$ git rm --cached .   
$ git add .   
$ git commit -m 'gitignore 적용'   
$ git push   
<br>

* * *

### create a new repository on the command line    
$ git init   
$ git add README.md    
$ git commit -m "first commit"   
$ git branch -M main    
$ git remote add origin <추가하려는 레포지토리 주소>   
$ git push -u origin main    
<br>

### push an existing repository from the command line    
$ git remote add origin <추가하려는 레포지토리 주소>    
$ git branch -M main   
$ git push -u origin main   
<br>

* * *

### repository 합치기   
통합할 새로운 repository "A" 생성   
repository A를 둘 폴더로 이동   
$ git clone <repository A 주소>
repository A 폴더로 이동   
$ git subtree add --prefix=<합칠 repository 이름> <합칠 repository 주소> <합칠 repository branch 이름>    
$ git add -A   
$ git commit -m "~"   
$ git branch -M main    
$ git push -u origin main    
<br>
