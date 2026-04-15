Кузнецов Станислав Андреевич 

# Стандартная структура HTML-документа

Каждая HTML-страница имеет базовую структуру (каркас), без которой
браузер не сможет корректно отобразить содержимое.

## Базовый шаблон:

``` html
<!DOCTYPE html>
<html lang="ru">
<head>
  <meta charset="UTF-8">
  <title>Название страницы</title>
</head>
<body>

</body>
</html>
```

### Объяснение:

-   `<!DOCTYPE html>` - сообщает браузеру, что используется HTML5

-   `<html>` - корневой элемент всей страницы
-   `<head>` - служебная часть (метаданные, заголовок, кодировка)
-   `<body>` - всё, что видит пользователь

## Семантическая (стандартная) разметка страницы

Семантические теги помогают структурировать страницу логически.

### Пример структуры:

``` html
<body>

  <header>
    <nav>
      <a href="#">Главная</a>
      <a href="#">О нас</a>
    </nav>
  </header>

  <main>
    <section>
      <h2>Раздел</h2>
      <p>Контент</p>
    </section>

    <article>
      <h2>Статья</h2>
      <p>Текст статьи</p>
    </article>
  </main>

  <footer>
    <p>© 2026</p>
  </footer>

</body>
```

### Основные теги:

-   `<header>` - верхняя часть страницы

-   `<nav>` - навигация (меню)
-   `<main>` - основной контент
-   `<section>` - логический раздел
-   `<article>` - самостоятельный блок (статья)
-   `<footer>` - нижняя часть страницы

## HTML формы

Формы используются для ввода и отправки данных пользователя.

### Основной тег:

``` html
<form action="/submit" method="post">
</form>
```

### Важные атрибуты:

-   `action` - куда отправляются данные

-   `method` - способ отправки (GET или POST)

### Основные элементы формы

#### Поля ввода:

``` html
<input type="text" name="name">
<input type="email" name="email">
<input type="password" name="password">
```

#### Кнопка:

``` html
<button type="submit">Отправить</button>
```

#### Многострочное поле:

``` html
<textarea name="message"></textarea>
```

#### Выпадающий список:

``` html
<select name="city">
  <option>Москва</option>
  <option>СПб</option>
</select>
```

#### Чекбоксы и радио:

``` html
<input type="checkbox"> Согласен

<input type="radio" name="gender"> Муж
<input type="radio" name="gender"> Жен
```

### Атрибуты

- `required` - обязательное поле

- `minlength` - минимальная длина поля
- `maxlength` - максимальная длина поля
- `placeholder` - подсказка

### Пример полной формы:

``` html
<form action="/submit" method="post">

  <label>Имя:</label>
  <input type="text" name="name">

  <label>Email:</label>
  <input type="email" name="email">

  <label>Сообщение:</label>
  <textarea name="message"></textarea>

  <button type="submit">Отправить</button>

</form>
```

## Поток документа (Document Flow)

Поток документа - это порядок, в котором элементы располагаются на
странице по умолчанию.

### Блочные элементы:

-   занимают всю ширину строки

-   каждый начинается с новой строки

``` html
<div>Блок 1</div>
<div>Блок 2</div>
<p>Абзац</p>
```

### Строчные элементы:

-   занимают только нужную ширину

-   располагаются в одной строке

``` html
<span>Текст 1</span>
<span>Текст 2</span>
<a href="#">Ссылка</a>
```

### Важное поведение:

``` html
<p>Текст <span>внутри</span> абзаца</p>
```

-   `<span>` не ломает строку

-   `<p>` - создаёт новый блок

### Нарушение потока (кратко):

CSS может изменять поток:

-   `display: block/inline`
-   `position`
-   `float`

# Задание:

1. Сделать страницу с семантической разметкой:

    -   header

    -   nav
    -   main
    -   section
    -   footer

2. Сделать простую форму регистрации

    ``` html
    <form>
      <!-- имя -->
      ???

      <!-- email -->
      ???

      <!-- пароль -->
      ???

      <!-- кнопка -->
      ???
    </form>
    ```

3. В script.js вставить:

    ```js
    const form = document.getElementById("form");

    form.addEventListener("submit", function(event) {
      event.preventDefault();

      const email = form.elements["email"].value;
      alert("Пользователь с email " + email + " зарегистрирован");
    });
    ```

4. Запустить Live Server и проверить что при отправке формы появляется `alert` с успешной регистрацией 
