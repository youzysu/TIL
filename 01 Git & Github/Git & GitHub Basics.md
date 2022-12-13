# Git & GitHub Basics

## Linux

### 📌 리눅스 탄생 배경

- 상황: 리차드 스톨먼이 오픈 소프트웨어 자유성 확보를 위한 GNU(GNU is Not Unix..) 프로젝트에 돌입! 근데 커널 시스템 소프트웨어가 없다.
  - 커널(Kernel): 하드웨어와 응용 프로그램을 이어주는 운영체제의 핵심 시스템소프트웨어
  - Applications ↔️ Kernel ↔️ CPU, Memory, Devices

### 📌 Linux

- GNU 프로젝트의 라이브러리와 도구가 포함된 운영체제
- PC와 모바일, 서버, 임베디드 시스템 등 다양한 분야에서 활용
- 다양한 배포판이 존재(Redhat, Debian, Ubuntu, Android 등)

### 📌 Shell

- 운영체제의 커널과 사용자를 이어주는 소프트웨어
  - ex. bash, zsh(Z shell)

## Shell Command

- `ls` list
- `cd` change directory
- `pwd` print working directory
- `mkdir` make directory
- `touch` create / modify file
- `rm` remove file
  - `-rf` flag: remove --recursive forced
- `rmdir` remove directory
- `..` 하위 디렉토리
- `../` 상위 디렉토리
- `mv` move
  - `mv 파일명 디렉토리명`
  - `mv ../app.js .` 상위 디렉토리에 있는 app.js를 현재 위치로 이동
  - - `mv ./app.js ./main.js` 현재 위치에 있는 app.js를 main.js로 이름을 변경하고 싶을 때도 사용
- `.` 현재 디렉토리
- `cp` copy
  - `cp 원본명 복사본명`
- `cat`
  - 파일 미리보기
- `vi 파일명`
  - vim

## Vim command

### 📌 vim modes

- Normal mode: press `esc` on any other mode.
- Insert mode: press `i` on Normal mode.
- Visual mode: press `v` on Normal mode.
- Command mode: press `:` on Normal mode.

### 📌 Command mode

- `:q` - quit
- `:q!` - quit discarding all changes
- `:w` - write
- `:wq` - write and quit

## Git

### 📌 Git이란?

- VCS (Version Control System)
- 분산형(Distributed)
- 비선형적 개발
  - 동시 작업 가능

### 📌 Git 환경설정 방법

- `git config --list`
  - 설정 확인
- `git config --global user.name`
- `git config --global user.email`
- `git config --global core.editor 'vim'`
- `git config --global core.pager 'cat'`
- `git lg`
  - [lg alias 설정](https://gist.github.com/johanmeiring/3002458)
- `vi ~/.gitconfig`에서 수정 가능

### 📌 Git Workflow

<br />

<img src='img/Git Workflow.png' />

<br />

#### 로컬에서 먼저 디렉토리 생성한 경우

- `git init` 사용하기 전 반드시 유의하기!

```
$ mkdir {reponame}
$ cd {reponame}
$ git init
$ git remote add origin https://github.com/{username}/{reponame}.git
$ touch README.md
$ git add README.md
$ git commit -m "docs: Create README.md"
$ git push -u origin master
```

#### 기존 repo를 clone하는 경우

```
$ git clone {repo address}
$ git add .
$ git commit
$ git push origin main
```

<br />

### 📌 Conventional Commits

> [Conventional Commits 참고](https://www.conventionalcommits.org/ko/v1.0.0/)

#### Prefix

- feat: 기능 개발 관련
- fix: 오류 개선 혹은 버그 패치
- docs: 문서화 작업
- test: test 관련
- chore: 환경설정 관련
- build: 빌드 관련
- ci: continuous Integration

#### Commit 원칙

- 동작 가능한 최소 단위로 Commit
- 제목과 내용은 한줄 띄워 분리

<br />

### 📌 README 파일

- 프로젝트를 설명하는 문서

#### template

- [프로젝트 소개](https://github.com/Integerous/all-in-one/blob/main/%ED%8F%AC%ED%8A%B8%ED%8F%B4%EB%A6%AC%EC%98%A4/project.md)
- 그외에도 우테코, 오픈소스 등 다른 리드미 파일 참고하여 필요한 항목 추가

```md
# Project Name

Abstract your project in few lines.
see [project sample page](project link)

## Documentation

### Installation

To install,
`$ pip install sesame`
and run `$ python open_sesame.py`

### Supported Python versions

`>=3.6`

### More Information

- [API docs]()
- [Official website]()

### Contributing

Please see [CONTRIBUTING.md]()

### License

Sesame is Free software, and may be redistributed under the terms of specified in the [LICENSE]() file.
```

### 📌 .gitignore

- git이 파일을 추적할 때, 어떤 파일이나 폴더 등을 추적하지 않도록 명시하기 위해 작성하는 문서
- `.gitignore` 문서에 작성된 리스트는 수정 사항이 발생하더라도 git이 추적하지 않아 무시된다.
- [gitignore.io](https://www.toptal.com/developers/gitignore/)에서 운영체제, 개발 환경, 프로그래밍 언어에 따라 `.gitignore` 문서 내용을 생성할 수 있다.

### 📌 LICENSE

기본적으로 repository 생성 시 함께 생성하기

- MIT License
  - MIT에서 만든 라이센스로 모든 행동에 제약이 없고 저작권자는 소프트웨어와 관련한 책임에서 자유롭다.
- Apache License 2.0
  - 특허권 관련 내용 포함, Apache 재단이 만든 라이센스
- GNU General Public License v3.0
  - 해당 라이센스가 적용된 소스코드 사용 시 GPL을 따라야 한다.
