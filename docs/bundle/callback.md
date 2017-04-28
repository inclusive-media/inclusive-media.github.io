# Обратный звонок
Форма звонка с сайта

## Селектор открытия
```html
<button class='im-callback-opener'>Кнопка открытия формы обратного звонка</button>
<button class='im-callback-opener' data-im-title='Заголовок для формы обратного звонка'>Такая же кнопка</button>
...
```

## Ручное открытие
```javascript
IMM.callback.showPanel()
IMM.callback.showPanel({title: 'Заголовок формы'})
```
### События, передаваемые в метрику
| Описание                                                | Событие                     |
| ------------------------------------------------------- | --------------------------- |
| Открытие формы                                          | `siteCallbackOpen`          |
| Нажал "Перезвонить еще раз"                             | `siteCallbackRepeat`        |
| Попытка подтверждения неправильно заполненного телефона | `siteCallbackSubmitInvalid` |
| Подтверждение правильно заполненной формы               | `siteCallbackSubmit`        |
| Сервер принял запрос и начнет обработку                 | `siteCallbackSubmitSuccess` |
