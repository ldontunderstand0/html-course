Кузнецов Станислав Андреевич 

## Форматирование документа и текста

## Блочная модель (Box Model)

Каждый элемент - прямоугольный блок. У каждого элемента есть:

-   content (содержимое)
-   padding (внутренние отступы)
-   border (граница)
-   margin (внешние отступы)

``` css
div {
  width: 200px;
  padding: 10px;
  border: 2px solid black;
  margin: 20px;
}
```
Разберем подробнее каждый пункт

## Внешние отступы (margin)

### Задание одинакового внешнего отступа со всех сторон элемента
``` css
div {
  margin: 20px;
}
```

### Задание одинакового внешнего отступа на верх/низ и право/лево элемента
``` css
div {
  margin: 20px 10px;
}
```
* сверху и снизу - 20px
* слева и справа - 10px

### Задание одинакового внешнего отступа на право/лево и индивидуального для верха и низа элемента
``` css
div {
  margin: 20px 10px 15px;
}
```
* сверху - 20px
* слева и справа - 10px
* снизу - 15px

### Задание индивидуального отступа на верх/низ/право/лево элемента
``` css
div {
  margin: 20px 10px 15px 18px;
}
```
* сверху - 20px
* справа - 10px
* снизу - 15px
* слева - 18px

### Отдельные свойства на верх/низ/право/лево элемента
``` css
margin-top: ???;
margin-right: ???;
margin-bottom: ???;
margin-left: ???;
```

## Внутренние отступы (padding)

### Задание одинакового внешнего отступа со всех сторон элемента
``` css
div {
  padding: 15px;
}
```
* для остальных случаев задание отступа работает как описано в margin

### Задание индивидуального отступа на верх/низ/право/лево элемента
``` css
padding-top: ???;
padding-right: ???;
padding-bottom: ???;
padding-left: ???;
```

## Границы (border)

``` css
div {
  border: 2px solid black;
}
```

## Типы линий

``` css
border-style: solid;
border-style: dashed;
border-style: dotted;
border-style: double;
```

## Цвет текста и фона

``` css
color: red;
background: yellow;
```

## Отступ текста

``` css
p {
  text-indent: 20px;
}
```

## Выравнивание

``` css
text-align: left;
text-align: center;
text-align: right;
text-align: justify;
```

## Оформление текста

``` css
font-weight: bold;
font-style: italic;
text-decoration: underline;
```

## Интервалы

``` css
letter-spacing: 2px;
word-spacing: 5px;
line-height: 1.5;
```

## Регистр

``` css
text-transform: uppercase;
text-transform: lowercase;
text-transform: capitalize;
```

## Практика

# Задание

1. Создать блок:

``` css
.box {
  margin: ???;
  padding: ???;
  border: ???;
}
```
2. Добавить границу:

``` css
.box {
  border-width: ???;
  border-style: ???;
  border-color: ???;
}
```

3. Настроить текст:

``` css
p {
  color: ???;
  text-align: ???;
}
```

4. Оформить текст:

``` css
h1 {
  font-weight: ???;
  text-decoration: ???;
}
```

5. Настроить интервалы:

``` css
p {
  letter-spacing: ???;
  line-height: ???;
}
```

6. Изменить регистр:

``` css
p {
  text-transform: ???;
}
```

7. Проверить корректность в браузере