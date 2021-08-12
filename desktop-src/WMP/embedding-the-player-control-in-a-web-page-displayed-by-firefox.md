---
title: Внедрение элемента управления игрока в веб-страницу, отображаемую в браузере Firefox
description: Внедрение элемента управления игрока в веб-страницу, отображаемую в браузере Firefox
ms.assetid: 57e725dc-6430-43ec-a39c-c17854a7d8db
keywords:
- проигрыватель Windows Media, встраивание ActiveX элемента управления
- проигрыватель Windows Media объектная модель, встраивание ActiveX элемента управления
- объектная модель, встраивание элемента управления ActiveX
- проигрыватель Windows Media мобильный, внедренный элемент управления ActiveX
- проигрыватель Windows Media элемент управления ActiveX, внедрение
- проигрыватель Windows Media управление мобильными ActiveXми, внедрение
- элемент управления ActiveX, встраивание
- проигрыватель Windows Media элемент управления ActiveX, веб-страницы
- проигрыватель Windows Media мобильный ActiveX элемент управления, веб-страницы
- элемент управления ActiveX, веб-страницы
- проигрыватель Windows Media, Firefox
- объектная модель проигрыватель Windows Media, Firefox
- Объектная модель, Firefox
- проигрыватель Windows Media Mobile, Firefox
- проигрыватель Windows Media ActiveX элемент управления, Firefox
- проигрыватель Windows Media мобильный ActiveX элемент управления, Firefox
- ActiveX элемент управления, Firefox
- Firefox, о внедрении веб-страниц
- внедрение, веб-страницы
- Внедрение веб-страниц, Firefox
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0c1db799df78cb6c62516798f4bbd196c093f02225386f0c1009bfa11d9a668
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118578591"
---
# <a name="embedding-the-player-control-in-a-web-page-displayed-by-firefox"></a>Внедрение элемента управления игрока в веб-страницу, отображаемую в браузере Firefox

чтобы внедрить элемент управления проигрыватель Windows Media в веб-страницу, которая может отображаться браузером Firefox, создайте объектный элемент или элемент embed с одним из следующих типов mime в качестве атрибута **type** :

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



Предшествующие примеры работают в браузере Firefox, но не в Internet Explorer. чтобы внедрить элемент управления проигрывателя в веб-страницу, которая может отображаться в Internet Explorer, необходимо создать элемент OBJECT с атрибутом **classid** , которому задан идентификатор класса элемента управления проигрыватель Windows Media.

в следующем примере показано, как внедрить элемент управления проигрыватель Windows Media в веб-страницу, которая может отображаться правильно в Internet Explorer и Firefox. Сценарий на странице определяет тип браузера и создает соответствующий тег объекта.


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



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**использование элемента управления проигрыватель Windows Media с браузером Firefox**](using-the-windows-media-player-control-with-firefox.md)
</dt> </dl>

 

 




