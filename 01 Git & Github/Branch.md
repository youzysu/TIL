# Branch

> [Branch Practice](https://github.com/youzysu/branch-practice)

- 분기점을 생성하여 **독립적으로** 코드를 변경할 수 있도록 도와주는 모델
- Default Branch: `main`, `master`
  - github에서 처음 생성된 프로젝트인 경우 `main`

## 📌 Branch Command

### `git branch`

- Show available local branch

### `git branch {branch name}`

- Create new branch stem

### `git switch {branch name}`

- 해당 branch로 이동
- 이전 기능 `checkout`

### `git merge {branch name}`

- 현재 위치: merge를 **수행하는** branch (ex. main branch)
- `{branch name}` the branch to be merged, 즉 merge **당하는** 브랜치명
- Merge Conflict 발생은 필연적
  - Conflict가 발생한 파일에서 일치하지 않는 부분을 수정하여 해결

### `git branch -D {branch name}`

- delete branch

### Branch Timeline

- [Git repository > Insights > Network](https://github.com/youzysu/branch-practice/network) 에서 브랜치를 통해 작업한 타임라인을 확인할 수 있다.
- 이를 참고하여 문제 상황을 파악하여 어떤 버전으로 되돌릴지 결정할 수 있다.

<br />

## 📌 Branching Models

### git flow

- Master - (Release) / (Hotfix) - Develop - Feature
- 가장 많이 적용되는 모델로 각 단계가 명확히 구분되는 장점
- 웹, 앱 개발과 같이 애자일 방식으로 개발하는 경우 대부분 git flow를 따른다.

  <img src='img/git flow strategy.png' />

### else

개발 후 바로 배포하는 방식

- github flow
- gitlab flow

## 📌 Git flow

### Requirement

- [Homebrew로 Git-flow 설치하기]()
