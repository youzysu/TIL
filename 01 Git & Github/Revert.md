## Revert

### Rename File name

- `git mv {last name} {name to be changed}`

### Undoing

- `git restore {filename}`

### Unstaging

`git add`로 staging한 파일을 수정하고 싶을 때

- `git reset HEAD {filename}`

### Edit latest commit

- `git commit --amend` 직전 commit을 다시 작성할 수 있다.

### Edit prior commit

- rebase
- `git rebase -i <commit>`

### Reset Commit

#### Revert

- `git revert --no-commit HEAD~n..`
  - HEAD로부터 n만큼의 commit을 되돌린다.
  - `--no-commit` revert는 기본적으로 각각의 commit이 남기 때문에 이를 한번에 처리하기 위함

#### Reset

과거 이력이 깔끔하게 사라지므로 tracking이 어렵기 때문에 `reset` 사용 지양
