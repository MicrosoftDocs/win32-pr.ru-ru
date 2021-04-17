---
title: Внедрение элемента управления игрока в веб-страницу, отображаемую в браузере Firefox
description: Внедрение элемента управления игрока в веб-страницу, отображаемую в браузере Firefox
ms.assetid: 57e725dc-6430-43ec-a39c-c17854a7d8db
keywords:
- Проигрыватель Windows Media, внедрение элемента управления ActiveX
- Объектная модель проигрывателя Windows Media, внедрение элемента управления ActiveX
- Объектная модель, внедрение элемента управления ActiveX
- Проигрыватель Windows Media Mobile, внедрение элемента управления ActiveX
- Элемент управления ActiveX проигрывателя Windows Media, внедрение
- Мобильный элемент управления ActiveX проигрывателя Windows Media, внедрение
- Элемент управления ActiveX, внедрение
- Элемент управления ActiveX проигрывателя Windows Media, веб-страницы
- Элемент управления мобильными устройствами ActiveX проигрывателя Windows Media, веб-страницы
- Элемент управления ActiveX, веб-страницы
- Проигрыватель Windows Media, Firefox
- Объектная модель проигрывателя Windows Media, Firefox
- Объектная модель, Firefox
- Проигрыватель Windows Media Mobile, Firefox
- Элемент управления ActiveX проигрывателя Windows Media, Firefox
- Элемент управления ActiveX проигрывателя Windows Media Mobile, Firefox
- Элемент управления ActiveX, Firefox
- Firefox, о внедрении веб-страниц
- внедрение, веб-страницы
- Внедрение веб-страниц, Firefox
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a16063ea07a0262ab798e58ed02e4d5a5b6b5d65
ms.sourcegitcommit: e22adfb0dd3bb989e59455baedb4d905a877a240
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/21/2019
ms.locfileid: "105691397"
---
# <a name="embedding-the-player-control-in-a-web-page-displayed-by-firefox"></a>Внедрение элемента управления игрока в веб-страницу, отображаемую в браузере Firefox

Чтобы внедрить элемент управления проигрывателя Windows Media на веб-страницу, которая может отображаться браузером Firefox, создайте ОБЪЕКТный элемент или элемент EMBED с одним из следующих типов MIME в качестве атрибута **Type** :

-   Application/x-MS-WMP
-   приложение/ASX
-   видео/x-MS-ASF-подключаемый модуль
-   приложение/x — Mplayer2
-   видео/x — MS-ASF
-   видео/x — MS-WM
-   аудио/x-MS-WMA
-   Audio/x — MS-мастика
-   видео/x — MS-WMV
-   видео/x — MS-ввкс

Предпочтительный тип MIME — application/x-MS-WMP.

В следующих примерах показано, как внедрить элемент управления "проигрыватель" с помощью элемента объекта или элемента EMBED.


```HTML
<OBJECT id="Player"
  type="application/x-ms-wmp" 
  width="320" height="320">
  <PARAM name="autostart" value="false"/>
</OBJECT>

<EMBED id="Player"
  type="application/x-ms-wmp" 
  width="320" height="320"
  autostart="false"/>

```



Предшествующие примеры работают в браузере Firefox, но не в Internet Explorer. Чтобы внедрить элемент управления проигрывателя в веб-страницу, которая может отображаться в Internet Explorer, необходимо создать элемент OBJECT с атрибутом **ClassID** , которому задан идентификатор класса для элемента управления проигрывателя Windows Media.

В следующем примере показано, как внедрить элемент управления проигрывателя Windows Media на веб-страницу, которая может отображаться правильно в Internet Explorer и Firefox. Сценарий на странице определяет тип браузера и создает соответствующий тег объекта.


```HTML
<HTML>
  <BODY>
    <SCRIPT type="text/javascript">
      if(-1 != navigator.userAgent.indexOf("MSIE"))
      {
        document.write('<OBJECT id="Player"');
        document.write(' classid="clsid:6BF52A52-394A-11d3-B153-00C04F79FAA6"');
        document.write(' width=300 height=200></OBJECT>');
      }
      else if(-1 != navigator.userAgent.indexOf("Firefox"))
      {
        document.write('<OBJECT id="Player"'); 
        document.write(' type="application/x-ms-wmp"'); 
        document.write(' width=300 height=200></OBJECT>');
      }         
    </SCRIPT>
  </BODY>
</HTML>

```



## <a name="related-topics"></a>См. также

<dl> <dt>

[**Использование элемента управления проигрывателя Windows Media с браузером Firefox**](using-the-windows-media-player-control-with-firefox.md)
</dt> </dl>

 

 




