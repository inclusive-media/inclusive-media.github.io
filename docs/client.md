## client
Выдача метки устройства

*Для успешной интеграции с Yandex.Metrika и Google Analytics необходимо подключать данный скрипт до подключения счетчиков*
```javascript
window.imm_mark
```

### Подключение
```html
<script type='text/javascript' src='https://web.uta-manager.ru/client'></script>

```

#### Интеграция с Яндекс.Метрикой
```html
<!-- Подключение маркера -->

...

<!-- А вообще лучше в менеджере зайти в раздел "Яндекс.Метрика" и взять код встаривания счетчика оттуда, -->
<!-- потому что тут может быть неактуальная версия для метрики -->
<!-- Yandex.Metrika counter -->
<script type="text/javascript">
    (function (d, w, c) {
        (w[c] = w[c] || []).push(function() {
            try {
                w.yaCounterXXXXXXXX = new Ya.Metrika({
                    id:XXXXXXXX,
                    ...
                    params: {
                      imm_id: window.imm_mark
                    }
                });
            } catch(e) { }
        });
        var n = d.getElementsByTagName("script")[0],
            s = d.createElement("script"),
            f = function () { n.parentNode.insertBefore(s, n); };
        s.type = "text/javascript";
        s.async = true;
        s.src = "https://mc.yandex.ru/metrika/watch.js";

        if (w.opera == "[object Opera]") {
            d.addEventListener("DOMContentLoaded", f, false);
        } else { f(); }
    })(document, window, "yandex_metrika_callbacks");
</script>
<noscript><div><img src="https://mc.yandex.ru/watch/XXXXXXXX" style="position:absolute; left:-9999px;" alt="" /></div></noscript>
<!-- /Yandex.Metrika counter -->
```
