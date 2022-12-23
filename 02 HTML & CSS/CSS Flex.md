# CSS Flex(Flexible Box)

> [1분코딩 CSS Flex](https://studiomeal.com/archives/197)

레이아웃 배치 전용 기능

- Flex Containcer: 부모 요소, 영향을 받는 전체 공간
- Flex Item: 자식 요소, 설정된 속성에 따라 특정 형태로 배치되는 아이템들

<br />

### Flex Container 적용 속성

#### `display: flex`

- default: item들은 가로 방향으로 배치된다.
  - width: 각각의 item은 자신의 width 만큼 차지한다.
  - height: container의 높이만큼 늘어난다.
- main axis
- cross axis

#### `flex-direction`

배치 방향 설정

- row (default)
- column
- row-reverse
- column-reverse

#### `flex-wrap`

줄넘김 처리 설정

- nowrap (default)
- wrap
- wrap-reverse

#### `justify-content`

main axis 방향 정렬

- flex-start (default)
- flex-end
- center
- space-between
- space-around
- space-evenly

#### `align-items`

cross axis 방향 정렬

- stretch (default)
- flex-start
- flex-end
- center
- baseline

#### `align-content`

- stretch (default)
- flex-start
- flex-end
- center
- space-between
- space-around
- space-evenly

### Flex Item 적용 속성

#### `flex-basis`

- default value: auto
- 아이템의 기본 크기 설정

#### `flex-grow`

- default value: 0

#### `flex-shrink`

- default value: 1
