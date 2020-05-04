200504 - git

## 1. git, github, 
- git : 버전 관리 시스템 (Version Control System)
- github : git 데이터를 저장하는 서버 (cf. gitlab, bitbucket)
- CLI(Command Line Interface) vs GUI(Graphic User Interface)
- git --version : 버전확인
- git --config user.name or code.editor : 기본설정
- git --help : 매뉴얼 치트키

## 2. gitbash 개요
- gitbash : user@pcname:~$
  - ~ : 사용자 최상단 폴더
  - $ : 명령 대기 상태 
- 기본 명령어
  - cd : change directory, cd ., cd .., cd <foldername>
  - ls : 하위 디렉토리 및 파일 조회, -a 숨김파일 조회 
  - mkdir : make directory
  - touch : make file
  - mv : 이동, rename
  - cp : copy
  - rm : remove file
  - rm -rf : remove folder
  - pwd : 절대 경로 조회
  - chmod : 파일의 권한 설정 (not supported at git bash)
    - d, - : direcory, file
    - 000 000 000 : user group other (0~7)
    - rwx : read write execute
    - - : no permission

## 3. vim 
- 기본적인 텍스트 에디터 (cf. Emacs)
- vi 파일명 형태로 구동
- 기본 명령어
  - :q  quit
  - :wq write quit
  - :set nu 줄보기 옵션
- 기본 동작
  - paste : shift + ins
  - ESC to escpae

# 4. git Process (important!)
- Blob(파일) -> Tree(파일모음) -> Commit(기능이 작동하는 최소단위)
- Workspace(local pc) -> Index(stage) -> Local Repositary(log 추가) -> Remote Repository(github)
- add -> commit -> push // pull & clone 
- git status : 현재 파일의 상태 조회
- git init : git 초기화 선언
- git remote and <name> [url] : github의 repo 경로와 pc의 로컬 경로를 연결
- git add <filename> : on stage, 커밋 대상으로 올리는 것 (untracked -> tracked)
  - git add . 수정한 모든 파일 추가
- git commit : 파일에 변경 로그를 추가하여 push 준비함
  - git commit -m "변경로그"
  - commit 주요 상태값
    - feat: features
    - docs: documentations 
    - conf: configuration
    - fix: bug-fix
    - reafact: refactoring
- git push -u <name> master : 깃헙으로 푸시 
  - -u(upstream) 옵션 확인해야 함
- git clone [repo url] : github에서 repo를 생성해 로컬 피씨로 가져오는 방법
- git pull <name> master : 다른 작업자의 repo에 commit한 소스를 내 repo로 끌어옴

## 5. github 블로그
- 생성 : username.github.io
- .gitignore : 특정 파일을 추적하지 않도록 설정하여 크롤링 방지
  - [파일 생성 사이트](http://gitignore.io/)
  - 특정 파일을 추가하고 싶은 경우 : *.확장자 형태로 기입

## 6. HEXO 프레임워크 연결
- node.js 설치, npm 설치, hexo 설치
  npm install -g 파일명
- hexo init <foldername>
- hexo clean && hexo generate && hexo server : 가상환경 확인 가능
- hexo deploy : git push