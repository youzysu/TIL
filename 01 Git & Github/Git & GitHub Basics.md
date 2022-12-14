# Git & GitHub Basics

## Linux

### π λ¦¬λμ€ νμ λ°°κ²½

- μν©: λ¦¬μ°¨λ μ€ν¨λ¨Όμ΄ μ€ν μννΈμ¨μ΄ μμ μ± νλ³΄λ₯Ό μν GNU(GNU is Not Unix..) νλ‘μ νΈμ λμ! κ·Όλ° μ»€λ μμ€ν μννΈμ¨μ΄κ° μλ€.
  - μ»€λ(Kernel): νλμ¨μ΄μ μμ© νλ‘κ·Έλ¨μ μ΄μ΄μ£Όλ μ΄μμ²΄μ μ ν΅μ¬ μμ€νμννΈμ¨μ΄
  - Applications βοΈ Kernel βοΈ CPU, Memory, Devices

### π Linux

- GNU νλ‘μ νΈμ λΌμ΄λΈλ¬λ¦¬μ λκ΅¬κ° ν¬ν¨λ μ΄μμ²΄μ 
- PCμ λͺ¨λ°μΌ, μλ², μλ² λλ μμ€ν λ± λ€μν λΆμΌμμ νμ©
- λ€μν λ°°ν¬νμ΄ μ‘΄μ¬(Redhat, Debian, Ubuntu, Android λ±)

### π Shell

- μ΄μμ²΄μ μ μ»€λκ³Ό μ¬μ©μλ₯Ό μ΄μ΄μ£Όλ μννΈμ¨μ΄
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
- `..` νμ λλ ν λ¦¬
- `../` μμ λλ ν λ¦¬
- `mv` move
  - `mv νμΌλͺ λλ ν λ¦¬λͺ`
  - `mv ../app.js .` μμ λλ ν λ¦¬μ μλ app.jsλ₯Ό νμ¬ μμΉλ‘ μ΄λ
  - - `mv ./app.js ./main.js` νμ¬ μμΉμ μλ app.jsλ₯Ό main.jsλ‘ μ΄λ¦μ λ³κ²½νκ³  μΆμ λλ μ¬μ©
- `.` νμ¬ λλ ν λ¦¬
- `cp` copy
  - `cp μλ³Έλͺ λ³΅μ¬λ³Έλͺ`
- `cat`
  - νμΌ λ―Έλ¦¬λ³΄κΈ°
- `vi νμΌλͺ`
  - vim

## Vim command

### π vim modes

- Normal mode: press `esc` on any other mode.
- Insert mode: press `i` on Normal mode.
- Visual mode: press `v` on Normal mode.
- Command mode: press `:` on Normal mode.

### π Command mode

#### Normal Mode

- `:q` - quit
- `:q!` - quit discarding all changes
- `:w` - write
- `:wq` - write and quit
- `dd` - delete a line
- `p` - paste a line
- `u` - undo
- `shift` + `Y` - copy line

## Git

### π Gitμ΄λ?

- VCS (Version Control System)
- λΆμ°ν(Distributed)
- λΉμ νμ  κ°λ°
  - λμ μμ κ°λ₯

### π Git νκ²½μ€μ  λ°©λ²

- `git config --list`
  - μ€μ  νμΈ
- `git config --global user.name`
- `git config --global user.email`
- `git config --global core.editor 'vim'`
- `git config --global core.pager 'cat'`
- `git lg`
  - [lg alias μ€μ ](https://gist.github.com/johanmeiring/3002458)
- `vi ~/.gitconfig`μμ μμ  κ°λ₯

### π Git Workflow

<br />

<img src='img/Git Workflow.png' />

<br />

#### λ‘μ»¬μμ λ¨Όμ  λλ ν λ¦¬ μμ±ν κ²½μ°

- `git init` μ¬μ©νκΈ° μ  λ°λμ μ μνκΈ°!
- `origin` remote(μκ²© μ μ₯μ)μ addressλ₯Ό μλ―Ένλ€.

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

#### κΈ°μ‘΄ repoλ₯Ό cloneνλ κ²½μ°

```
$ git clone {repo address}
$ git add .
$ git commit
$ git push origin main
```

<br />

### π Conventional Commits

> [Conventional Commits μ°Έκ³ ](https://www.conventionalcommits.org/ko/v1.0.0/)

#### Prefix

- feat: κΈ°λ₯ κ°λ° κ΄λ ¨
- fix: μ€λ₯ κ°μ  νΉμ λ²κ·Έ ν¨μΉ
- docs: λ¬Έμν μμ
- test: test κ΄λ ¨
- chore: νκ²½μ€μ  κ΄λ ¨
- build: λΉλ κ΄λ ¨
- ci: continuous Integration

#### Commit μμΉ

- λμ κ°λ₯ν μ΅μ λ¨μλ‘ Commit
- μ λͺ©κ³Ό λ΄μ©μ νμ€ λμ λΆλ¦¬

<br />

### π README νμΌ

- νλ‘μ νΈλ₯Ό μ€λͺνλ λ¬Έμ

#### template

- [νλ‘μ νΈ μκ°](https://github.com/Integerous/all-in-one/blob/main/%ED%8F%AC%ED%8A%B8%ED%8F%B4%EB%A6%AC%EC%98%A4/project.md)
- κ·ΈμΈμλ μ°νμ½, μ€νμμ€ λ± λ€λ₯Έ λ¦¬λλ―Έ νμΌ μ°Έκ³ νμ¬ νμν ν­λͺ© μΆκ°

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

### π .gitignore

- gitμ΄ νμΌμ μΆμ ν  λ, μ΄λ€ νμΌμ΄λ ν΄λ λ±μ μΆμ νμ§ μλλ‘ λͺμνκΈ° μν΄ μμ±νλ λ¬Έμ
- `.gitignore` λ¬Έμμ μμ±λ λ¦¬μ€νΈλ μμ  μ¬ν­μ΄ λ°μνλλΌλ gitμ΄ μΆμ νμ§ μμ λ¬΄μλλ€.
- [gitignore.io](https://www.toptal.com/developers/gitignore/)μμ μ΄μμ²΄μ , κ°λ° νκ²½, νλ‘κ·Έλλ° μΈμ΄μ λ°λΌ `.gitignore` λ¬Έμ λ΄μ©μ μμ±ν  μ μλ€.

### π LICENSE

κΈ°λ³Έμ μΌλ‘ repository μμ± μ ν¨κ» μμ±νκΈ°

- MIT License
  - MITμμ λ§λ  λΌμ΄μΌμ€λ‘ λͺ¨λ  νλμ μ μ½μ΄ μκ³  μ μκΆμλ μννΈμ¨μ΄μ κ΄λ ¨ν μ±μμμ μμ λ‘­λ€.
- Apache License 2.0
  - νΉνκΆ κ΄λ ¨ λ΄μ© ν¬ν¨, Apache μ¬λ¨μ΄ λ§λ  λΌμ΄μΌμ€
- GNU General Public License v3.0
  - ν΄λΉ λΌμ΄μΌμ€κ° μ μ©λ μμ€μ½λ μ¬μ© μ GPLμ λ°λΌμΌ νλ€.
