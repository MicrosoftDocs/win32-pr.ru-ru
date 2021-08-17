---
title: Обработка событий на веб-странице, отображаемой Firefox
description: Обработка событий на веб-странице, отображаемой Firefox
ms.assetid: 361c46ff-36e2-4497-a511-86b0439e9437
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
- проигрыватель Windows Media ActiveX элемент управления, обработка событий
- проигрыватель Windows Media управление мобильными ActiveXми, обработка событий
- управление ActiveXми, обработка событий
- внедрение, веб-страницы
- Внедрение веб-страниц, обработка событий
- проигрыватель Windows Media, Firefox
- объектная модель проигрыватель Windows Media, Firefox
- Объектная модель, Firefox
- проигрыватель Windows Media Mobile, Firefox
- проигрыватель Windows Media ActiveX элемент управления, Firefox
- проигрыватель Windows Media мобильный ActiveX элемент управления, Firefox
- ActiveX элемент управления, Firefox
- Firefox, обработка событий
- Внедрение веб-страниц, Firefox
- события, Firefox
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e971caef18114b670678fc76d0515858bee77a94a5e3f8b5c24ca5322177b8e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117748419"
---
# <a name="handling-events-in-a-web-page-displayed-by-firefox"></a>Обработка событий на веб-странице, отображаемой Firefox

при внедрении элемента управления проигрыватель Windows Media на веб-странице можно написать сценарий, обрабатывающий события. Список событий, вызванных элементом управления проигрывателя, см. в разделе [объект Player](player-object.md).

Если тип MIME, связанный с внедренным элементом управления игрока, — Application/x-MS-WMP, можно написать обработчики событий, имеющие следующий формат:


```HTML
<SCRIPT for="Player" language="jscript" event="EventName(Params)">
  ...
</SCRIPT>
```



где *EventName* — это имя проигрыватель Windows Media события, а *params* — это список параметров события. Например, следующий код имеет обработчик для события [плайстатечанже](player-player-playstatechange.md) .


```HTML
<OBJECT id="Player" type="application/x-ms-wmp" width="300" height="200">
  <PARAM name="URL" value="c:\MediaFiles\Seattle.wmv"/>
</OBJECT>

<P id="p1">...</P>

<SCRIPT for="Player" event="PlayStateChange(NewState)">
  document.getElementById("p1").innerHTML = "Play state: " + NewState;
</SCRIPT>
```



Если на веб-странице имеется несколько экземпляров элемента управления Player и используется формат, показанный в предыдущем примере, каждый обработчик событий привязан к конкретному экземпляру элемента управления проигрывателя. В предыдущем примере обработчик событий вызывается только при изменении состояния воспроизведения для элемента управления с идентификатором "Player".

Если тип MIME, связанный с внедренным элементом управления игрока, не является Application/x-MS-WMP, можно написать обработчики событий, имеющие следующий формат:


```HTML
<SCRIPT language="jscript">
  function OnDSEventNameEvt(Params)
  {...}
</SCRIPT>
```



где *EventName* — это имя проигрыватель Windows Media события, а *params* — это список параметров события. Например, следующий код имеет обработчик для события **плайстатечанже** .


```HTML
<OBJECT id="Player" type="application/asx" width="300" height="200">
  <PARAM name="URL" value="c:\MediaFiles\Test.asx"/>
</OBJECT>

<P id="p1">...</P>

<SCRIPT>
  function OnDSPlayStateChangeEvt(NewState)
  {
    p1.innerHTML = "Play state: " + NewState;
  }
</SCRIPT>

```



Если на веб-странице имеется несколько экземпляров элемента управления Player и используется формат, показанный в предыдущем примере, каждый обработчик событий привязан ко всем экземплярам элемента управления проигрывателя, а обработчик событий вызывается при изменении состояния воспроизведения для любого элемента управления проигрывателя на странице.

> [!Note]  
> Если тип MIME не является Application/x-MS-WMP, событие **DoubleClick** отправляется как ондсдблкликкевт (не ондсдаублекликкевт) для совместимости с элементом управления проигрывателя версии 6,4.

 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**использование элемента управления проигрыватель Windows Media с браузером Firefox**](using-the-windows-media-player-control-with-firefox.md)
</dt> </dl>

 

 




