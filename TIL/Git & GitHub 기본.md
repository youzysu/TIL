# Git & GitHub 기본

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
  -   - `mv ./app.js ./main.js` 현재 위치에 있는 app.js를 main.js로 이름을 변경하고 싶을 때도 사용
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

## git
### 📌 git이란?
- VCS (Version Control System)
- 분산형(Distributed)
- 비선형적 개발
  - 동시 작업 가능

```
📝 Memo
히피가 소프트웨어에도 영향을 미쳤구낭 잼따
```
