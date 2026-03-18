Кузнецов Станислав Андреевич
# Мультимедиа-объекты. Макет страницы и навигационные карты.

Мультимедиа‑объекты в HTML — это элементы страницы, которые содержат или показывают не только текст: изображения, звук, видео, анимации, встроенные документы и т.п.

К ним относят: картинки, аудио, видео, встроенные PDF/карты, iframe‑вставки, SVG и др.

## Вставка изображения

Основной тег: ```<img>``` (одиночный, без закрывающего тега).

### Главные атрибуты

* ```src``` — путь к картинке

* ```alt``` — альтернативный текст (важно для доступности и если картинка не загрузилась)
* ```width```, ```height``` — размеры (лучше задавать, чтобы не “прыгала” верстка)
* ```loading="lazy"``` — ленивая загрузка

### Пример
```html
<img src="images/lec5/cat.png" alt="Рыжий кот на подоконнике" width="400" loading="lazy">
```

### Картинка с подписью
```html
<figure>
  <img src="images/lec5/cat.png" alt="Рыжий кот на подоконнике" width="400">
  <figcaption>Рис. 1 — Кот у окна</figcaption>
</figure>
```

## Вставка аудио и видео

### Аудио — ```<audio>```

```html
<audio controls>
  <source src="images/lec5/music.mp3" type="audio/mpeg">
  <source src="images/lec5/music.ogg" type="audio/ogg">
  Ваш браузер не поддерживает аудио.
</audio>
```

### Полезные атрибуты:

* ```controls``` — показать кнопки управления

* ```autoplay``` — автостарт (часто блокируется браузерами)
* ```loop``` — повтор
* ```muted``` — без звука (часто нужно для autoplay)
* ```preload="none|metadata|auto"``` — предзагрузка

### Видео — ```<video>```

```html
<video controls width="640" poster="images/preview.jpg">
  <source src="images/lec5/movie.mp4" type="video/mp4">
  <source src="images/lec5/movie.webm" type="video/webm">
  Ваш браузер не поддерживает видео.
</video>
```
Дополнительно можно добавить субтитры:

```html
<track src="subs/ru.vtt" kind="subtitles" srclang="ru" label="Русские" default>
```

## Вставка других мультимедиа‑объектов (встраивание)

Кроме img/audio/video, часто встраивают “чужой” контент:

```<iframe>``` — встроить страницу/карту/видео‑плеер

```html
<iframe
  src="https://www.youtube.com/embed/JKlTjCQa_eY"
  width="560" height="315"
  title="Видео"
  allowfullscreen>
</iframe>
```

```<object>``` / ```<embed>``` — например PDF (используется реже)

```html
<object data="files/book.pdf" type="application/pdf" width="600" height="400">
  <p>Не удалось показать PDF. <a href="files/book.pdf">Скачать</a></p>
</object>
```

## Что такое навигационные карты‑изображения (image map)

Карта‑изображение — это картинка, на которой можно сделать несколько кликабельных областей (например, нажать на разные страны на карте).

Реализуется через:

* ```<img usemap="#mapname">```
* ```<map name="mapname">```
* ```<area>``` — описывает области (прямоугольник/круг/многоугольник)
Пример:

```html
<img src="images/lec5/plan.png" alt="План кабинета" usemap="#roommap" width="600">

<map name="roommap">
  <area shape="rect" coords="50,50,200,150" href="desk.html" alt="Стол">
  <area shape="circle" coords="350,120,60" href="board.html" alt="Доска">
</map>
```

Где coords — координаты области на изображении (в пикселях).


# Задание:

1. Запонить пропуски (пропуск - ???)

    ```html
    <!doctype html>
    <html lang="ru">
    <head>
      <meta charset="utf-8">
      <title>Мультимедиа</title>
    </head>
    <body>

      <header>
        <h1>Моя мультимедиа-страница</h1>
      </header>

      <nav>
        <!-- Сделай 3 ссылки-меню: к #img, #media, #footer -->
        ???
      </nav>

      <main>
        <section id="img">
          <h2>Изображение</h2>

          <!-- figure + img + figcaption -->
          ???
          
          <!-- Карта-изображение: img usemap + map + 2 area -->
          ???
        </section>

        <section id="media">
          <h2>Аудио и видео</h2>

          <p>Аудио:</p>
          <!-- audio controls + source -->
          ???

          <p>Видео:</p>
          <!-- video controls width + source -->
          ???
        </section>
      </main>

      <footer id="footer">
        <!-- Автор и год -->
        ???
      </footer>

    </body>
    </html>

    ```

2. Сделать работающую навигационную карту по изображению cabinet.png

3. Запустить Live Server и проверить работоспособность всех элементов
