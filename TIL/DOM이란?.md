# 📑 DOM이란?

> [Udemy The Web Developer BootCamp](https://www.udemy.com/course/the-web-developer-bootcamp-2021-korea/)

## Contents

- [1. Intro to the DOM](#1-intro-to-the-dom)
- [2. Selecting](#2-selecting)
  - getElementById
  - querySelector
- [3. innerHTML and Text](#3-innerhtml-and-text)
- Changing Styles
- classList
- Creating/Removing Elements
- Manipulating Attributes
- Traversing the DOM

<br />

## 1. Intro to the DOM

### 📌 DOM: Document Object Model

- 웹페이지를 구성하는 JavaScript 객체들의 집합
  - 웹페이지의 모든 콘텐츠를 나타내는 객체의 모음
  - 브라우저가 웹페이지를 띄울 때 HTML, CSS 파일을 통해 HTML 요소와 CSS 스타일을 기반으로 생성하는 JavaScript 객체를 의미한다.
- Browser에서 자동으로 생성되는 Document 객체
  - 페이지의 콘텐츠를 나타내는 Collection of Objects
  - Click, Drag와 같은 events에 대한 method와 properties를 담고 있다.
  - 이를 이용하여 DOM을 조작 및 변경한다.

## 2. Selecting

### `getElementById`

일치하는 ID를 가진 요소를 나타내는 객체를 반환하는 메서드

### `getElementsByTagName`

일치하는 TagName를 가진 요소들을 나타내는 객체(HTMLCollection)을 반환하는 메서드

- 특정 Tag들을 한번에 선택 가능

### `getElementsByClassName`

일치하는 ClassName을 가진 요소들을 나타내는 객체(HTMLCollection)을 반환하는 메서드

### 📌 getElementById Practice

- Select the image element by its id and save it to a variable called image
- Select the h1 by its id and save it to a variable called heading

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Unicorn</title>
  </head>
  <body>
    <h1 id="mainheading">I &hearts; unicorns</h1>
    <img
      src="https://devsprouthosting.com/images/unicorn.jpg"
      id="unicorn"
      alt="unicorn"
    />
  </body>
</html>
```

```js
const image = document.getElementById('unicorn');
const heading = document.getElementById('mainheading');
```

### `querySelector`

CSS 선택자와 같은 방식으로 해당 요소를 나타내는 객체를 반환하는 메서드

- 첫번째로 일치하는 값 하나만 반환
- ex. `document.querySelector('a[title='JavaScript']')`

### `querySelectorAll`

CSS 선택자와 같은 방식으로 일치하는 요소를 나타내는 객체를 모두 반환하는 메서드

### 📌 querySelector Practice

- Select all elements that have the class of "done" and save them in a variable called doneTodos.
- Select the one checkbox and save it in a variable called checkbox. Be careful, there is more than one input element on the page! You'll need to select using the type attribute. (if you can't remember the css attribute selector...google it! That's what I would do!)

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Todos</title>
  </head>

  <body>
    <h1>Garden Todos</h1>
    <input type="text" placeholder="New Todo" />
    <ul>
      <li>Start Seedlings</li>
      <li class="done">Deadhead Zinnias</li>
      <li class="done">Water Tomatoes</li>
      <li class="done">Harvest Potatoes</li>
      <li>Prune Roses</li>
    </ul>
    <label>Delete All</label>
    <input type="checkbox" id="scales" name="scales" checked />
  </body>
</html>
```

```js
const doneTodos = document.querySelectorAll('.done');
const checkbox = document.querySelector('input[type="checkbox"]');
```

## 3. innerHTML and Text

### `innerText`

### `textContent`

### `innerHTML`
