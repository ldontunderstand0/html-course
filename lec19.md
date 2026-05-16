Кузнецов Станислав Андреевич

# Работа с DOM и событиями

## Что такое DOM

DOM (Document Object Model) - это объектная модель документа.

Браузер представляет HTML-страницу как дерево объектов, с которым можно работать через JavaScript.

## DOM-дерево

HTML-документ состоит из элементов, связанных между собой.

Пример HTML:

``` html
<html>
  <body>
    <h1>Заголовок</h1>
    <p>Текст</p>
  </body>
</html>
```

## Структура DOM

``` text
html
 └── body
      ├── h1
      └── p
```

## HTML как структура элементов

Каждый HTML-элемент: 
- имеет тег 

- содержит текст 
- может иметь атрибуты 
- может содержать другие элементы

Пример:

``` html
<div class="box">
  <p>Текст</p>
</div>
```

## Получение элементов страницы

### `getElementById()`

Получение элемента по `id`.

``` html
<h1 id="title">Заголовок</h1>
```

``` js
const title = document.getElementById("title");
```

### `querySelector()`

Получение первого элемента по CSS-селектору.

``` js
const element = document.querySelector(".box");
```

Примеры:

``` js
document.querySelector("#title");
document.querySelector(".box");
document.querySelector("p");
```


### `querySelectorAll()`

Получение всех элементов.

``` js
const items = document.querySelectorAll("p");
```

## Изменение содержимого

### `innerText`

Изменяет текст элемента.

``` js
element.innerText = "Новый текст";
```

### `innerHTML`

Позволяет изменять HTML внутри элемента.

``` js
element.innerHTML = "<b>Жирный текст</b>";
```

## Изменение стилей

``` js
element.style.color = "red";
element.style.fontSize = "30px";
```

## Понятие события

Событие - это действие пользователя или браузера.

Примеры: 
- `click` 

- `mouseover` 
- `keydown`

## `addEventListener()`

Метод для обработки событий.

``` js
element.addEventListener("событие", function() {
  // код
});
```

## Основные события

### `click`

Щелчок мыши.

``` js
button.addEventListener("click", function() {
  console.log("Клик");
});
```

### `mouseover`

Наведение мыши.

``` js
element.addEventListener("mouseover", function() {
  console.log("Наведение");
});
```

### `keydown`

Нажатие клавиши.

``` js
document.addEventListener("keydown", function() {
  console.log("Клавиша");
});
```

### Пример кнопки

HTML:

``` html
<button id="btn">Нажми</button>
<p id="text">Текст</p>
```


JavaScript:

``` js
const btn = document.getElementById("btn");
const text = document.getElementById("text");

btn.addEventListener("click", function() {
  text.innerText = "Текст изменён";
});
```

## Работа с `input`

``` html
<input type="text" id="email">
```

``` js
const email = document.getElementById("email");

console.log(email.value);
```

# Задание

1. Сделать в `HTML` форму регистрации со следующими полями:
    - `login` - обязателен, должен быть больше 5 символов;

    - `email` - обязателен, должен соответствовать email формату;
    - `password` - обязателен, должен содержать более 10 символов и соответствовать формату пароля;
    - `button` - кнопка "Отправить".

2. Добавить стили с помощью `CSS`.

3. Написать скрипт с помощью `JavaScript`, который  по нажатию на кнопку "Отправить", если пользователь ввел корректные данные, будет показывать сообщение (`alert`) об успешной регистрации