# ๐ DOM์ด๋?

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

### ๐ DOM: Document Object Model

- ์นํ์ด์ง๋ฅผ ๊ตฌ์ฑํ๋ JavaScript ๊ฐ์ฒด๋ค์ ์งํฉ
  - ์นํ์ด์ง์ ๋ชจ๋  ์ฝํ์ธ ๋ฅผ ๋ํ๋ด๋ ๊ฐ์ฒด์ ๋ชจ์
  - ๋ธ๋ผ์ฐ์ ๊ฐ ์นํ์ด์ง๋ฅผ ๋์ธ ๋ HTML, CSS ํ์ผ์ ํตํด HTML ์์์ CSS ์คํ์ผ์ ๊ธฐ๋ฐ์ผ๋ก ์์ฑํ๋ JavaScript ๊ฐ์ฒด๋ฅผ ์๋ฏธํ๋ค.
- Browser์์ ์๋์ผ๋ก ์์ฑ๋๋ Document ๊ฐ์ฒด
  - ํ์ด์ง์ ์ฝํ์ธ ๋ฅผ ๋ํ๋ด๋ Collection of Objects
  - Click, Drag์ ๊ฐ์ events์ ๋ํ method์ properties๋ฅผ ๋ด๊ณ  ์๋ค.
  - ์ด๋ฅผ ์ด์ฉํ์ฌ DOM์ ์กฐ์ ๋ฐ ๋ณ๊ฒฝํ๋ค.

## 2. Selecting

### `getElementById`

์ผ์นํ๋ ID๋ฅผ ๊ฐ์ง ์์๋ฅผ ๋ํ๋ด๋ ๊ฐ์ฒด๋ฅผ ๋ฐํํ๋ ๋ฉ์๋

### `getElementsByTagName`

์ผ์นํ๋ TagName๋ฅผ ๊ฐ์ง ์์๋ค์ ๋ํ๋ด๋ ๊ฐ์ฒด(HTMLCollection)์ ๋ฐํํ๋ ๋ฉ์๋

- ํน์  Tag๋ค์ ํ๋ฒ์ ์ ํ ๊ฐ๋ฅ

### `getElementsByClassName`

์ผ์นํ๋ ClassName์ ๊ฐ์ง ์์๋ค์ ๋ํ๋ด๋ ๊ฐ์ฒด(HTMLCollection)์ ๋ฐํํ๋ ๋ฉ์๋

### ๐ getElementById Practice

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

CSS ์ ํ์์ ๊ฐ์ ๋ฐฉ์์ผ๋ก ํด๋น ์์๋ฅผ ๋ํ๋ด๋ ๊ฐ์ฒด๋ฅผ ๋ฐํํ๋ ๋ฉ์๋

- ์ฒซ๋ฒ์งธ๋ก ์ผ์นํ๋ ๊ฐ ํ๋๋ง ๋ฐํ
- ex. `document.querySelector('a[title='JavaScript']')`

### `querySelectorAll`

CSS ์ ํ์์ ๊ฐ์ ๋ฐฉ์์ผ๋ก ์ผ์นํ๋ ์์๋ฅผ ๋ํ๋ด๋ ๊ฐ์ฒด๋ฅผ ๋ชจ๋ ๋ฐํํ๋ ๋ฉ์๋

### ๐ querySelector Practice

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
