# git command

- [git-docs](https://git-scm.com/docs)
- [github-git-cheat-sheet](https://services.github.com/on-demand/downloads/github-git-cheat-sheet.pdf)
- [만들면서 배우는 Git GitHub 입문](http://book.naver.com/bookdb/book_detail.nhn?bid=9415223)

![git_working_area](./git_area.jpg)


# 설정

- ```#git config --global user.name "name"```  
Git에서 커밋할 때 기록할 이름 설정  

- ```#git config --global user.email "email"```  
Git에서 커밋할 때 기록하는 이메일 설정  

---

# 저장소 생성

- ```#git init 저장소이름```  
명령을 실행한 위치에 <저장소 이름>으로 저장소를 만듬  

- ```#git clone 저장소주소```   
<저장소 주소>의 원격 저장소를 클론  

---

# 변경 내역 다루기

- ```#git status```  
저장소의 상태를 확인. 추적하지 않는 파일, 추적 중이지만  
변경되어 커밋해야 하는 파일 등을 보여줌  

- ```#git diff```  
마지막 커밋과 현재 변경된 내용을 비교해 보여줌  

- ```#git add 파일이름```   
버전 관리를 하기 위한 파일 추적을 시작.  
stage에 add를 하는 것  

- ```#git reset 파일이름```   
변경 내역이 생겨서 git add 명령을 실행해  
커밋할 준비가 된 파일을 Staging영역에서 제거  
파일의 변경 내역은 보존  

- ```#git commit -m "커밋설명 메시지"```  
git add 명령을 실행해 커밋할 준비가 된(staged 상태인)  
파일을 로컬 저장소에 <커밋설명메시지>로 설명을 입력해 커밋

---

# 브랜칭

- ```#git branch```  
저장소에 있는 브랜치 목록을 보여줌(+현재 브런치)  

- ```#git branch 이름```  
<이름>으로 브랜치를 만듬  

- ```#git checkout 브랜치이름```  
<브랜치이름>으로 현재 작업 중인 브랜치를 변경  

- ```#git merge 브랜치이름```  
현재 작업 중인 브랜치에 <브랜치이름> 브랜치를 가져와 병합  

- ```#git branch -d 브랜치이름```  
<브랜치 이름>브랜치를 삭제  

- ```#git push --set-upstream origin develop```  

# 추적 중인 파일 삭제와 변경
- ```#git rm 파일이름```  
저장소에서 버전 관리 중인 파일을 삭제. 그와 더불어 실제 로컬  
파일도 삭제. 삭제 기록이 저장소에 남음  

- ```#git rm --checked 파일이름```  
저장소에서 버전 관리 중인 파일만 삭제. 로컬은 그대로 남음  

- ```#git mv 파일이름 변경될파일이름```  
저장소에서 버전 관리 중인 파일의 이름(혹은 경로)를 변경  
변경 기록이 저장소에 남음  

---

# 커밋하지 않은 상태로 임시 보관

- ```#git stash```  
Staged 상태에 있는 커밋되지 않는 변경 내역을 stash라는 임시 공간에 저장  

- ```#git stash pop```  
stash에 마지막으로 저장 된 변경 내역을 현재 브랜치에 적용  

- ```#git stash list```  
stash에 저장된 변경 내역의 목록을 출력  

- ```#git stash drop```  
마지막으로 저장된 변경 내역을 삭제

---

# 내역 살펴보기

- ```#git log```  
현재 브랜치의 버전 내역을 출력  

- ```#git log --follow 파일이름```  
파일의 변경 내역들을 출력. 파일 이름의 변경까지 포함한 내역을 출력  

- ```#git diff 브랜치 ... 다른 브랜치```  
파일의 변경 내역들을 출력. 파일 이름의 변경까지 포함한 내역 출력  

- ```#git show 커밋```  
대상 커밋의 메타데이터와 변경 내역을 출력  

---

# 커밋 취소하기

- ```#git reset 커밋```  
대상 커밋 이후에 생긴 모든 커밋을 취소.  
하지만 커밋과 함께 변경된 내역은 로컬 저장소에 남겨둠  

- ```#git reset --hard 커밋```  
대상 커밋 이후에 생긴 모든 커밋과 변경 내역을 대상 커밋  
시점으로 되돌림

---

# 원격 저장소와 동기화

- ```#git fetch 원격저장소이름```  
원격 저장소의 모든 변경 내역을 로컬 저장소에 다운로드  

- ```#git merge 원격저장소이름/브랜치이름```  
원격 저장소의 대상 브랜치를 현재 작업 중인 브랜치에 병합  

- ```#git push 원격저장소이름 브랜치이름```  
로컬 브랜치의 모든 커밋을 원격 저장소의 대상 브랜치에 업로드  

- ```#git pull 원격저장소이름```  
git fetch와 git merge 명령을 차례로 실행하는 것과 같은 명령  
즉, git fetch 원격저장소이름 명령 과 git merge 원격저장소이름/현재브랜치  
명령을 실행한 결과와 같음

- ```#git remote add origin? http:...```  
원격 저장소 추가

- ```#git checkout -t origin/branch-name```  
원격 브런치 checkout 




  

