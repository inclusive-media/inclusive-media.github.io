# Формы ("открытые")

Формы, встраиваемые в существующие элементы ```<form></form>```

> **Важно!** Указывайте в настройках формы селектор, указывающий именно на элемент(ы) ```<form></form>```

## Атрибуты

У формы и ее элементов можно задать атрибуты конфигурации

### Атрибуты формы
| Атрибут | Описание | Возможные значения | Значение по умолчанию |
| ------- | -------- | ------------------ | --------------------- |
| im-tooltip-placement | Положение всплывающей подсказки ФОРМЫ (ошибка сервера и тд) | `auto` `top` `top-start` `top-end` `right` `right-start` `right-end` `bottom` `bottom-start` `bottom-end` `left` `left-start` `left-end` | `bottom` |

### Атрибуты элементов формы
| Атрибут | Описание | Возможные значения | Значение по умолчанию |
| ------- | -------- | ------------------ | --------------------- |
| im-tooltip-placement | Положение всплывающей подсказки элемента | `auto` `top` `top-start` `top-end` `right` `right-start` `right-end` `bottom` `bottom-start` `bottom-end` `left` `left-start` `left-end` | `bottom-start` |

## События, передаваемые в Yandex.Metrika

{!docs/bundle/forms/metrika/attach.md!}

## События, передаваемые в Google Analytics

{!docs/bundle/forms/ga/attach.md!}


## Пример

```html
<!DOCTYPE html>
<html lang="ru">
  <head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <link rel="stylesheet" type="text/css" href="style.css">
  </head>
  <body>
    <script src="https://web.uta-manager.ru/bundle/id-проекта" async></script>
    <div>
      <div>
        <form class="form1" id="form11" im-tooltip-placement="left" >
          <div class="form-group">
            <div class="form-label">
              Имя
            </div>
            <div class="form-control">
              <input type="text" name="username" />
            </div>
          </div>
          <div class="form-group">
            <div class="form-label">
              Телефон
            </div>
            <div class="form-control">
              <input name="phone" im-tooltip-placement="right" />
            </div>
          </div>
          <div class="form-group">
            <div class="form-label">
              Почта
            </div>
            <div class="form-control">
              <input type="TeXt" name="email" />
            </div>
          </div>
          <div class="form-group">
            <div class="form-label">
              Color
            </div>
            <div class="form-control">
              <select name="color">
                <option value="red">Красный</option>
                <option value="yellow">Желтый</option>
                <option value="green">Зеленый</option>
              </select>
            </div>
          </div>
          <div class="form-group">
            <div class="form-label">
              Color radio
            </div>
            <div class="form-control">
              <input type='radio' name='color-radio' value='red' title='Красный' />
              <input type='radio' name='color-radio' value='yellow' title='Желтый' />
              <input type='radio' name='color-radio' value='green' title='Зеленый' />
            </div>
          </div>
          <div class="form-group">
            <div class="form-label">
              Коммент
            </div>
            <div class="form-control">
              <textarea name="comment"></textarea>
            </div>
          </div>
          <div class="form-group">
            <div class="form-label">
              Length
            </div>
            <div class="form-control">
              <input type="text" name="length" />
            </div>
          </div>
          <div class="form-group">
            <div class="form-control">
              <input type="submit" value="Отправить" />
            </div>
          </div>
          <div class="form-group">
            <div class="form-control">
              <input type="reset" value="Сброс" />
            </div>
          </div>
        </form>
      </div>
    </div>
  </body>
</html>
```
