# Техническое задание на настройку целей в квизе https://promo.splatglobal.com/diagnostics/
Необходимо установить счетчики Яндекс.Метрика и Google Analytics и прописать идентицикаторы/названия событий и их параметры в коде страниц квиза https://promo.splatglobal.com/diagnostics/ для фиксации целей Яндекс.Метрика и Google Analytics
## Зачем
Необходимо, что при срабатывании Javacript события на страницах квиза https://promo.splatglobal.com/diagnostics/ данные о срабатывании передавались в Яндекс.Метрику и Google Analytics.
Где они будут фиксироваться и отображаться.
## Что нужно сделать
### Установка счетчиков
Добавьте код счетчика в HTML-код всех страниц сайта https://promo.splatglobal.com/. Код нужно разместить в пределах тегов <head> </head> или <body> </body> как можно ближе к началу страницы: так он будет раньше загружаться и сможет отправить данные о просмотре в Метрику, даже если посетитель почти сразу же закроет страницу.

**Код Яндекс.Метрики**
<!-- Yandex.Metrika counter -->
<script type="text/javascript" >
   (function(m,e,t,r,i,k,a){m[i]=m[i]||function(){(m[i].a=m[i].a||[]).push(arguments)};
   m[i].l=1*new Date();
   for (var j = 0; j < document.scripts.length; j++) {if (document.scripts[j].src === r) { return; }}
   k=e.createElement(t),a=e.getElementsByTagName(t)[0],k.async=1,k.src=r,a.parentNode.insertBefore(k,a)})
   (window, document, "script", "https://mc.yandex.ru/metrika/tag.js", "ym");

   ym(92962183, "init", {
        clickmap:true,
        trackLinks:true,
        accurateTrackBounce:true,
        webvisor:true
   });
</script>
<noscript><div><img src="https://mc.yandex.ru/watch/92962183" style="position:absolute; left:-9999px;" alt="" /></div></noscript>
<!-- /Yandex.Metrika counter -->

**Код Google Analytics**
<!-- Google tag (gtag.js) -->
<script async src="https://www.googletagmanager.com/gtag/js?id=G-FRXEH8R5E9"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());

  gtag('config', 'G-FRXEH8R5E9');
</script>

Ниже указан тег Google для этого аккаунта. Скопируйте и вставьте его в код каждой страницы сайта, сразу после элемента <head>. На каждую страницу можно добавить только один тег Google.

### Установка целей
#### Яндекс.Метрика
Уже созданы цели для Яндекс.Метрики и идентификаторы для них. Подробнее в таблице: https://docs.google.com/spreadsheets/d/1KY6WM6_pxxCDocHyAGZYsVfXKmIWYT22j4IUgAdHhUM/edit#gid=0 
При достижении цели вызывается метод reachGoal, в который передается указанный идентификатор. Подробнее про данный метод в справочнике Яндекс.Метрики https://yandex.ru/support/metrica/objects/reachgoal.html
### Google Analytics
Используйте API gtag.js для отправки событий в Google Analytics. gtag() — это функция JavaScript, поэтому вам нужно добавить эту функцию в JavaScript на вашей веб-странице. 
Название событий, значения их параметров отображены в таблице https://docs.google.com/spreadsheets/d/1KY6WM6_pxxCDocHyAGZYsVfXKmIWYT22j4IUgAdHhUM/edit#gid=0

Подробнее про настройку событий: https://developers.google.com/analytics/devguides/collection/ga4/events?hl=ru&client_type=gtag
https://developers.google.com/analytics/devguides/collection/gtagjs/events?hl=ru


