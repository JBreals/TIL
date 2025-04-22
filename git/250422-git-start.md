# git 기초 개념 및 shell 구문

- **git: 버전관리 프로그램. 개발 진행에 큰 도움을 주며 특히 협업에 엄청난 강점을 가진다.**

## git 개념

- working directory: 현재 개발하는 공간
- staging area: commit하여 local repo에 올릴 파일들이 지정된 공간
- local repository: 변경사항들이 저장된 공간. 여러 commit들이 각각의 변경사항에 적용됨.
- remote repository: 원격 저장소. local repository에 기록된 변경사항을 remote repository로 push 혹은 remote에서 local로 pull.(ex: github)

## git 구문(중요한 것만)

```shell
$git status ##현재 git 상태 확인(추적한 파일의 변경사항 감지, 추적이 안된 파일 알림)
$git add [/file_name or .] ##지정된 파일이나 현재 폴더에 존재하는 파일을 staging area에 올림
$git commit [option: -m "message"] ## staging area에 존재하는 변경사항 local repo에 올림
$git clone "remote repo 주소" ## remote 주소에 있는 프로젝트를 현재 디렉토리에 git을 적용하여 clone할 수 있다.
$git branch "branch name" ## 새로운 브랜치 생성
$git switch "branch name" ## 해당 브랜치로 이동
$git push origin main ##local repo에 있는 변경사항들을 원격저장소의 main 브랜치로 push. local의 내용을 원격에도 적용시킬 수 있다
```

## git conventional commit

> **commit 메세지는 변경사항의 내용이 무엇인지 보기 쉽게 작성되어야 한다. 이를 위한 commit 메세지 작성 가이드**

1. commit 제목은 문장형이 아닌 구나 절이 형태로 작성
2. commit title은 capitalize 중요. -> This Is Commit Title.
3. 주요 prefix

```
feat: 기능 개발 관련
fix: 오류 개선 및 버그 패치
docs: 문서화 작업(ex: readme.md)
test: test 관련
conf: 환경 설정 관련
build: 빌드 작업 관련
chore: 패키지 매니저, 스크립트 등
style: 코드 포맷팅
```

## 중요한 부분들

- git clone할 때 생성되는 프로젝트 폴더는 자동으로 origin이 remote repo로 지정되어 있다. 그래서 push origin main이 원격 저장소의 main 브랜치를 가르키는 것이다.
- .gitignore 파일을 만들어서 버전관리에 포함을 안하는 파일을 지정할 수도 있다. [gitignore.io](https://www.toptal.com/developers/gitignore)
