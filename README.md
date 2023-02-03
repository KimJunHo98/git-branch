# Git 사용방법
## 원격 저장소를 로컬 저장소로 복사
1. 원격 저장소 생성 하거나 기존의 원격저장소 주소를 복사
2. vscode 실행 -> 터미널 열기
3. git clone 원격 저장소 주소
## 로컬에서 수정한 파일을 원격으로 다시 올리기
1. 파일 수정
2. git add .
3. git commit -m "로컬에서 수정 ver2"
4. git push origin main
## 팀장+팀원: 로컬저장소 생성
1. git init 로컬 저장소명
2. cd 로컬 저장소명
3. git config user.name "내이름"
4. git config user.email "내메일주소"
## 팀원
로컬저장소와 원격저장소 연결 - 터미널에 아래의 명령어를 입력
1. git remote add origin 원격저장소주소
2. pull 하기
3. "git pull origin 브랜치명"

🔑 항상 최신 커밋을 pull 한 다음 push한다.
## 팀원별 브랜치 만들기
1. 팀원별 브랜치 생성하기 (로컬저장소에서 진행)
2. 브랜치 생성시 다른 팀원과 이름이 중복되지 않도록 유의한다. 아래의 명령어는 브랜치를 생성하면서 변경하는 명령어이다.

  git switch -c 브랜치명
  
3. 자신의 브랜치에서 작업을 한후 버전을 생성한다.

  git add .

  git commit -m "" 

## 처음 작업할 때 (git init)
```
1. 파일 생성
2. git init 레포리토지 이름
3. git config user.name "깃허브 이름"
4. git config user.email "깃허브에 이메일"
5. git remote add origin 원격저장소주소
6. git pull origin 풀 할 브랜치이름
7. git switch -c 사용할 브랜치 이름
8. 작업
9. git add .
10. git commit -m ""
11. git pull origin 풀 할 브랜치이름
12. git switch 풀 했던 브랜치 이름
13. git merge 스위치 했던 브랜치 이름
14. git add .
15. git commit -m ""
16. git push origin 풀 했던 브랜치 이름
```
## 처음 작업할 때 <git clone>
```
1. 파일 생성
2. git clone 원격저장소 주소
3. git switch -c 사용할 내 브랜치 이름
4. 작업
5. git add .
6. git commit -m ""
7. git pull origin 풀 할 브랜치이름
8. git switch 풀 했던 브랜치 이름
9. git merge 자신의 브랜치 이름
10. git add .
11. git commit -m ""
12. git push origin 풀 했던 브랜치 이름
```
## 수정 할 때 
```
1. git switch 내 브랜치 이름
2. git pull origin 풀 할 브랜치이름
3. 작업
4. git add .
5. git commit -m ""
6. git pull origin 풀 할 브랜치이름
7. git switch 풀 했던 브랜치 이름
8. git merge 자신의 브랜치 이름
9. git add .
10. git commit -m ""
11. git push origin 풀 했던 브랜치 이름
```
## 팀원별 브랜치 병합
1. 원격저장소의 main 브랜치 최신 커밋을 pull 한다.
2. 나의 로컬 브랜치의 최신버전과 merge 후 push 한다.
```
   git switch main

   git merge 내브랜치

   git add .

   git commit -m ""

   git push origin main 
```
