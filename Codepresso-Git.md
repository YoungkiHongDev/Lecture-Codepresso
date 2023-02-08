# 소프트웨어의 형상
- 와이어프레임 - 실제 사용자에게 제공할 모습을 설계
- 플로우차트 - 서비스 로직의 흐름을 도식화
- 소스코드 - 컴퓨터가 인지할 수 있도록 프로그래밍

# 소프트웨어의 형상은 계속 변화
요구사항은 언제든지 변화 및 추가될 수 있다.
1. 요구사항
2. 디자인
3. 구현
4. 검증
5. 유지보수

# 형상관리 SCM
소프트웨어 변경점을 체계적으로 추적하고 관리하는 일련의 모든 활동

# 형상관리 중요성
- 프로젝트 리스크 최소화
- 소프트웨어 품질 확보

# 형상관리 대상
- 개발 시 발생하는 모든 산출물
- 요구사항도출 단계 - 서비스 정의서, 요구사항 명세서
- 디자인 단계 - 스토리보드, 와이어프레임, 프로토타입, 소프트웨어 아키텍처 문서
- 구현 단계 - 소스코드, API문서, 개발자가이드 문서

# Git
- 소스코드를 효율적으로 관리하는 형상관리 도구 (버전 관리 도구)
- 리누스 토발즈가 개발

# Git 목표
- 빠른 속도
- 단순 구조
- 비선형적 개발
- 완벽한 분산
- 대규모 프로젝트

# 중앙 집중형 버전 관리
- CVS, SVN 방식
- 원격 서버 하나를 두고 각 개발자가 다른부분을 내려받고 개발해서 업로드
- 네트워크가 없으면 작업이 불가능
- 데이터 손실이 발생하면 복구가 어렵다

# 분산 집중형 버전 관리
- Git, Mercurial 방식
- 원격 서버 하나를 두고 각 개발자의 로컬에도 동일한 파일이 존재함
- 네트워크가 없어도 작업이 가능
- 데이터 손실이 발생하면 복원이 쉬움

# Git의 특징
- 커맨드 기반
- 설치 공간이 매우 작음
- 브랜치 기능
- 스테이징 영역
- 다양한 워크플로우

# Git 설치 여부 확인
- git --verison

# GIt 기본 용어
- 원격 저장소: 원격 서버의 저장소
- 로컬 저장소: 개발하는 개발자의 PC
- 클론: 원격 저장소의 소스코드를 로컬 저장소로 복사
- 작업 디렉토리: PC에서 현재 작업중인 공간, git에서 관리하지만 추적은 하지않음
- 스테이징 영역: 작업 디렉토리에서 작업한 의미있는 변경점을 임시 저장하는 영역, git에서 추적 관리, 커밋을 준비하는 영역
- 커밋: git에서 가장 의미있는 변경 단위, 변경점을 로컬 저장소로 영구 저장하는 과정

# Git 기본 명령어
- git clone : 원격 저장소의 소스코드를 다운로드
- git add : 작업한 변경점을 워킹 디렉토리에서 스테이징 영역으로 임시 저장
- git commit : 쌓인 변경점을 스테이징 영역에서 로컬 저장소로 영구 저장
- git pull : 원격 저장소에서 로컬 저장소로 커밋을 다운로드
- git push : 로컬 저장소에서 원격 저장소로 커밋을 업로드 (push 하기 전 pull 필수!)

# Git 협업
- 개발자들은 각자 자신의 로컬 저장소에서 개발을 진행하고 커밋을 만들어서 원격 저장소로 저장
- 다른 개발자가 작업한 내용을 자신의 로컬 저장소에 가져옴

# Git 기본 환경 설정
## 사용자의 이름, 이메일 기본 설정
- git config --global user.name "이름"
- git config --global user.email "이메일주소"

## 기본 에디터를 vim으로 설정
- git config --global core.editor vim

## 설정 정보 확인
- git config --global --list

## 기본 설정 변경
- vi ~/.gitconfig
- i 버튼 입력 후 수정 가능
- 수정 후 저장 및 종료는 ESC 버튼 + :wq 입력

# 원격 저장소
- 대표적인 웹 기반 플랫폼 서비스는 GitHub, GitLab, Bitbucket이 있다.

# GitLab
- Private 저장소 Community 버전은 무료
- 주로 기업에서 인트라넷에 연결해서 사용하고 있다.

# Git 저장소 연결 방법 1
- GitHub 혹은 GitLab에 원격 저장소 생성
- 컴퓨터에 작업할 폴더를 생성
- 명령어 창 안에서 작업할 폴더로 이동
- 원격 저장소의 Clone 주소를 복사
- git clone [원격 저장소 주소] 명령어 입력

# Git 저장소 연결 방법 2
- GitHub 혹은 GitLab에 원격 저장소 생성
- 컴퓨터에 작업할 폴더를 생성
- 명령어 창 안에서 작업할 폴더로 이동
- git init 명령어 입력
- 원격 저장소의 Clone 주소를 복사
- git remote add origin [원격 저장소 주소] 명령어 입력하여 저장소 연결
- git remote -v 명령어 입력하여 연결된 저장소 확인

# git 상태 확인 명령어
- git status : 현재 폴더 내 파일의 상태 확인
- git log : 커밋의 히스토리 확인
- git log --help : 명령어 뒤에 help 옵션 입력 시 웹브라우저를 통해 해당 명령어의 매뉴얼 페이지가 실행됨
- git log -u : 전체 커밋의 내용과 변경점 확인
- git log -u [커밋ID] : 해당 커밋의 내용과 변경점 확인
- git log -1 : 가장 최근 커밋 1개의 내용과 변경점 확인
- git log -2 : 가장 최근 커밋 2개의 내용과 변경점 확인
- git log --name-only : 커밋 내용과 변경점 그리고 변경된 파일명까지 확인
- git log --oneline : 각 커밋을 간결하게 한줄씩 만들어 확인
- git log --reverse : 가장 오래된 커밋부터 확인
- git show [커밋ID] : 해당 커밋의 내용과 변경점 확인 (git log -u [커밋ID]와 같음)
- git diff : 변경 코드 확인, 작업 디렉토리에서 기존 코드에서 변경된 점 확인이 가능, 변경점이 적으면 파악이 쉽고 변경점이 많으면 파악이 어려움

# Commit의 히스토리
- git log로 확인 가능
- Commit의 아이디, 개발자 정보, 시간, 메시지 확인 가능
- Commit의 아이디는 SHA-1 해시 알고리즘으로 만들어진다.
- git은 해시값으로 저장소의 히스토리를 관리한다.

## 작업 디렉토리의 파일 상태
- Untracked: 변경점이 발생한 Git에 의해 관리되지 않은 파일, Staging Area에 한번도 포함되지 않음
- Tracked: Git에 의해 관리되는 파일, Staging Area에 한번 이상 포함됨

# Git CRLF Warning 로그
- 명령어로 경고 메시지 설정을 끌 수 있다.
- git config --global core.safecrlf false

# Git 기본 플로우
- Remote Repository의 새로운 프로젝트를 git clone으로 나의 Local Repository에 내려받는다.
- Working Directory에 작업한다.
- Working Directory에서 작업한 파일을 git add 한다.
- git add한 파일이 Staging Area에 변경점으로 추가된다.
- Staging Area의 파일을 git commit 한다.
- Commit이 Local Repository에 저장된다.
- Local Repository의 Commit을 git push하여 Remote Repository에 업로드된다.
- 다른 개발자가 push한 Commit을 git pull하여 Remote Repository에서 나의 Local Repository에 내려받는다.

# 커밋 되돌리기 (덮어쓰기 방식)
- git commit --amend
- 마지막에 반영한 최신 커밋 메시지를 변경하고 싶으면 사용, 최신 커밋 수정 가능한 에디터가 실행됨, 되돌린 것은 복구불가
- 커밋에 추가할 변경점이 있을 때 사용, 파일을 수정 후 git add로 스테이징 영역에 추가, git commit --amend 명령어로 커밋을 생성

# 커밋 되돌리기 (롤백하는 방식)
- git revert [커밋ID]
- 코드를 원복 (반영한 특정 코드 제거, 변경 취소, 반영한 커밋 되돌리기, 반영한 커밋 revert)
- 새로운 Revert 커밋이 추가되지만 내용은 가장 최근 커밋을 롤백

# 원격 저장소에 커밋 반영
- git push [저장소별칭] [브랜치]
- git push origin master

# GitLab push 에러 및 해결방법
- 유저명과 패스워드가 다를 경우 발생
- remote: HTTP Basic: Access denied
- fatal: Authentication faild for
- 1. 자격 증명 관리자 실행
- 2. Windows 자격 증명 클릭
- 3. gitlab에 해당되는 내용을 찾아 제거 후 git push 다시시도

# GitLab 팀원 등록
- 프로젝트로 들어가서 왼쪽 메뉴에서 Settings의 Members 들어가기
- Invite member에 협업할 사용자를 입력하고 permission으로 Developer을 선택 후 Invite 클릭
- 다시 왼쪽 메뉴에서 Settings의 Repository 들어가기
- Protected Branches에서 master Branch의 Allowed to push를 누르고 Developers + Maintainers 클릭하여 팀원에게 push 권한 허용
- 팀원은 본인의 GitLab 페이지에서 협업 프로젝트가 보이고 등록되어 있는지 확인

# Merge
- git pull 시 다른 개발자가 올린 커밋이 있을 경우 발생할 수 있다.
- 같은 파일을 작업했을 경우 수동으로 수정이 필요하다.
- pull 완료 후 Merge를 커밋한다.