## transition

transition 전환 속성은 요소의 변화를 자연스럽게 만들어준다.
전환 속성은 요소가 변화하기 **전** 상태에 적용해야 한다.

default

- transition-property: all
- transition-duration: 0s
  - 지속시간

#### transition-timing-function

- linear

#### transition-delay

- 지연시간

## Animation

애니메이션 속성으로 프레임을 제어한다.

#### animation-name

#### animation-duration

#### animation-iteration-count

- 횟수
- infinite

#### animation-timing-function

- linear

#### @keyframes

frame 규칙을 만드는 property

animation

#### animation-play-state

#### animation-fill-mode

애니메이션이 동작하는 방식

> https://codepen.io/heropark/pen/PKQbQM

- default: none;
- forwards
- backwards
- both

#### animation-direction

> https://codepen.io/heropark/pen/XveLKq

- default: normal
- reverse
- alternate
- alternate-reverse

왕복하려면 animation-iteration-count: 2 함께 해줘야 한다.

## 미디어 쿼리

> https://www.daleseo.com/css-media-queries/

반응형 웹디자인
viewport 너비에 따라 콘텐츠를 배치하는 기술

#### syntax

- media type
  - default: all
  - screen, tv, print, ...
- condition
  - orientation: portrait

```css
@media (max-width: 450px) {
  .item {
    width: 200px;
    background-color: royalblue;
  }
}
```

- 최대 가로 너비 명시

## Grid

> https://heropy.blog/2019/08/17/css-grid/

> https://codepen.io/heropark/pen/ExYKWrR

#### grid-template-columns

column 개수만큼
`grid-template-columns: repeat(4, 100px);`

#### grid-template-rows

row 개수만큼

```css
.container {
  display: grid;
  grid-template-columns: repeat(4, 100px);
  grid-template-rows: 100px 100px;
}
.item {
  border: 4px solid;
}
```

#### grid-column

`grid-column: span 4;`

#### grid-template-rows

명시적

#### grid-auto-rows

암시적

#### grid-auto-flow

## 변수

```css
html {
  --color: red;
}

.item {
  --width: 122px
  width: var(--width)
  height: calc(var(--width) * 3 / 2)
  background-color: var(--color)
}
```

## Reference

> https://greensock.com/docs/v2/Easing

> https://easings.net/ko
