Кузнецов Станислав Андреевич

# Flexbox (display: flex)

## Что такое Flexbox

Flexbox - это модель расположения элементов, которая позволяет удобно
управлять выравниванием и распределением пространства внутри контейнера.

* используется вместо float и position для построения интерфейсов

## Основные понятия

-   flex-контейнер - родитель (display: flex)
-   flex-элементы - дочерние элементы

``` css
.container {
  display: flex;
}
```

## Нормальный поток vs Flexbox

По умолчанию элементы идут сверху вниз.

Flexbox: выстраивает элементы в строку (по умолчанию)

## Основные свойства Flex-контейнера

Flexbox работает через две оси:

- главная ось (main axis) — направление элементов  
- поперечная ось (cross axis) — перпендикулярно главной  

---

## 1. flex-direction — направление элементов

Определяет, как располагаются элементы внутри контейнера.

```css
flex-direction: row;            /* слева направо (по умолчанию) */
flex-direction: column;         /* сверху вниз */
flex-direction: row-reverse;    /* справа налево */
flex-direction: column-reverse; /* снизу вверх */
```

### Пример:
```css
.container {
  display: flex;
  flex-direction: column;
}
```
```html
<div class="container">
  <div>1</div>
  <div>2</div>
  <div>3</div>
</div>
```

* элементы будут располагаться вертикально

## 2. justify-content — выравнивание по главной оси

Управляет расположением элементов вдоль главной оси.

```css
justify-content: flex-start;    /* в начале */
justify-content: center;        /* по центру */
justify-content: flex-end;      /* в конце */
justify-content: space-between; /* равномерно, без отступов по краям */
justify-content: space-around;  /* отступы вокруг элементов */
justify-content: space-evenly;  /* равные отступы */
```

### Пример:

```css
.container {
  display: flex;
  justify-content: center;
}
```

* элементы будут выровнены по центру по горизонтали

## 3. align-items — выравнивание по поперечной оси

Управляет выравниванием элементов перпендикулярно главной оси.

```css
align-items: stretch;     /* растягивает (по умолчанию) */
align-items: center;      /* по центру */
align-items: flex-start;  /* к началу */
align-items: flex-end;    /* к концу */
```

### Пример:
```css
.container {
  display: flex;
  align-items: center;
  height: 200px;
}
```

* элементы будут выровнены по центру по вертикали

Важно
justify-content → главная ось
align-items → поперечная ось

## 4. flex-wrap — перенос элементов

Определяет, будут ли элементы переноситься на новую строку.

```css
flex-wrap: nowrap; /* по умолчанию, все в одну строку */
flex-wrap: wrap;   /* перенос на новую строку */
```

## Пример:

```css
.container {
  display: flex;
  flex-wrap: wrap;
}
```

* элементы переходят на новую строку при нехватке места

### Пример Flex-контейнера

```css
.container {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 200px;
}
```
```html
<div class="container">
  <div>1</div>
  <div>2</div>
  <div>3</div>
</div>
```

* элементы по центру и по горизонтали, и по вертикали

## Итог
* Flexbox управляет расположением элементов по осям
* контейнер управляет расположением

# Задание

1. Сделать контейнер flex-контейнером
    ``` css
    .container {
      display: ???;
    }
    ```
2. задать ему flex-direction

    ``` css
    flex-direction: ???;
    ```

3. задать ему justify-content и align-items
    ``` css
    justify-content: ???;
    align-items: ???;
    ```
4. задать ему flex-wrap
    ``` css
    flex-wrap: ???;
    ```
