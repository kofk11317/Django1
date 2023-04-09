# Django1
> Django 스터디
------

## Member
> 조현호 고우석 김재윤 이정현

## Date
> 매주 월요일 오후 9시


-----

# Chapter4. Git & Github

## Git의 구조
<img width="1401" alt="git_structure" src="https://user-images.githubusercontent.com/67615226/229673845-10cf22fe-f34b-4fa4-aec3-bd5107a0874a.png">

  - working directory: 현재 작업 중이 프로젝트가 위치한 디렉토리
  - Staging: commit 할 파일의 예비 저장소
  - Local Repository: 각 컴퓨터의 git이 관리하는 로컬 저장소
  - Remote Repository: 외부에 위치한 원격 저장소
------

## Git의 사용
  ### git 저장소 만들기
<img width="824" alt="git_init" src="https://user-images.githubusercontent.com/67615226/229673870-4201bec6-48f6-4216-9764-a39cfef2384c.png">

    - 나의 프로젝트가 위치하 곳으로 이동 후 터미널에서 명령 실행
    - git init: 현재 디렉토리에서 git을 사용할 수 있도록 초기화
    - .git 디렉토리: Staging, Local Repository가 들어있음
    - .gitignore: 같은 위치에 있는 파일을 git에서 무시 ex) 데이터베이스 계정, 클라우드 시크릿 키, 각종 민감 정보
   
  ### 버전 만들기
  
   <img width="772" alt="git_status" src="https://user-images.githubusercontent.com/67615226/229673924-ffe22fbd-8c26-48a2-af71-12f2ae431266.png">

    - git status: git 상태를 확인하기 위한 명령어
      - on branch main: 현재 main 브랜치에 있음
      - No commits yet: 아직 commit한 파일이 없음
      - untracked files: 버전을 아직 한 번도 관리하지 않은 파일
    
   <img width="773" alt="git_add" src="https://user-images.githubusercontent.com/67615226/229674001-f95a064b-81b1-493e-9b8e-4bd08845b96e.png">

    - git add <file>: working directory -> staging
    - git add . : working directory에 있는 모든 파일을 staging에 이동
    - git commit -m " " : staging -> local repository

   <img width="637" alt="git_log" src="https://user-images.githubusercontent.com/67615226/229674155-2ccbd6ea-dc49-4c2b-8dc7-e504742514e3.png">

    - git log: 저장소에 저장된 버전을 확인할 때 사용
    - git pull origin main : 원격 저장소에서 commit을 pull할 때 사용하는 명령어
    - git commit -am " " : staging과 commit을 한 번에 처리, 한 번이라도 commit한 적이 있는 파일을 다시 커밋할 때만 사용 가능
 
## Github에 소스 반영
    - git remote add origin <원격저장소의 주소> : 원격 저장소에 origin(github 저장소 주소)을 추가하겠다고 git에게 알려 주는 명령어
        ex) git remote add origin https://github.com/LEEJH1029/Django1.git
     
    - git push -u origin <브랜치명> : 지역 저장소의 브랜치를 origin의 브랜치로 push하라는 명령어
      - -u: 지역 저장소의 브랜치를 원격 저장소의 브랜치에 연결하기 위한 옵션. 처음 한 번만 사용하면 됨
      ex) git push -u origin main
  
## Github로 협업하기
  <img width="700" alt="git_branch" src="https://user-images.githubusercontent.com/67615226/230717041-d5e0b3c1-0c03-4d0e-b44e-febfb9fd9718.png">
  
    - git clone <원격저장소의 주소> : 원격 저장소 -> 지역 저장소 복제
        ex) git clone https://github.com/Likelion-Kwangwoon/Django1.git
  
  <img width="764" alt="branch" src="https://user-images.githubusercontent.com/67615226/230718057-423fdfa5-631b-4fb0-bb5a-179e434f9f6d.png">
  
    - git checkout -b <브랜치명> : branch를 새로 만들고 해당 branch로 이동
    - git checkout <브랜치명> : <브랜치명>으로 이동
    - git merge <브랜치명> : 현재 있는 branch로 <브랜치명>을 병합
  
  <img width="871" alt="branch_merge" src="https://user-images.githubusercontent.com/67615226/230717634-0097e33a-ce90-40a0-b7bd-4a83e7ffabe6.png">
  
  ---
  
    - git branch <브랜치명> : branch 생성
    - git switch <브랜치명> : <브랜치명>으로 이동
