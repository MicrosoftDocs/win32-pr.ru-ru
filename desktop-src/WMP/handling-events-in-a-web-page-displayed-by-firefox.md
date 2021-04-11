---
title: Обработка событий на веб-странице, отображаемой Firefox
description: Обработка событий на веб-странице, отображаемой Firefox
ms.assetid: 361c46ff-36e2-4497-a511-86b0439e9437
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
- Элемент управления ActiveX проигрывателя Windows Media, обработка событий
- Мобильный элемент управления ActiveX проигрывателя Windows Media, обработка событий
- Элемент управления ActiveX, обработка событий
- внедрение, веб-страницы
- Внедрение веб-страниц, обработка событий
- Проигрыватель Windows Media, Firefox
- Объектная модель проигрывателя Windows Media, Firefox
- Объектная модель, Firefox
- Проигрыватель Windows Media Mobile, Firefox
- Элемент управления ActiveX проигрывателя Windows Media, Firefox
- Элемент управления ActiveX проигрывателя Windows Media Mobile, Firefox
- Элемент управления ActiveX, Firefox
- Firefox, обработка событий
- Внедрение веб-страниц, Firefox
- события, Firefox
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b9659d1920ffc4d5e39f4cd44e15e24b08f6ddc
ms.sourcegitcommit: e22adfb0dd3bb989e59455baedb4d905a877a240
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/21/2019
ms.locfileid: "104332875"
---
# <a name="handling-events-in-a-web-page-displayed-by-firefox"></a>Обработка событий на веб-странице, отображаемой Firefox

При внедрении элемента управления проигрывателя Windows Media на веб-страницу можно написать сценарий, обрабатывающий события. Список событий, вызванных элементом управления проигрывателя, см. в разделе [объект Player](player-object.md).

Если тип MIME, связанный с внедренным элементом управления игрока, — Application/x-MS-WMP, можно написать обработчики событий, имеющие следующий формат:


```HTML
<SCRIPT for="Player" language="jscript" event="EventName(Params)">
  ...
</SCRIPT>
```



где *EventName* — это имя события проигрывателя Windows Media, а *params* — это список параметров события. Например, следующий код имеет обработчик для события [плайстатечанже](player-player-playstatechange.md) .


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



где *EventName* — это имя события проигрывателя Windows Media, а *params* — это список параметров события. Например, следующий код имеет обработчик для события **плайстатечанже** .


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

 

## <a name="related-topics"></a>См. также

<dl> <dt>

[**Использование элемента управления проигрывателя Windows Media с браузером Firefox**](using-the-windows-media-player-control-with-firefox.md)
</dt> </dl>

 

 




