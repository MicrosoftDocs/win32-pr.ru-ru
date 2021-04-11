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
# <a name="handling-events-in-a-web-page-displayed-by-firefox"></a><span data-ttu-id="5bb8d-128">Обработка событий на веб-странице, отображаемой Firefox</span><span class="sxs-lookup"><span data-stu-id="5bb8d-128">Handling Events in a Web Page Displayed by Firefox</span></span>

<span data-ttu-id="5bb8d-129">При внедрении элемента управления проигрывателя Windows Media на веб-страницу можно написать сценарий, обрабатывающий события.</span><span class="sxs-lookup"><span data-stu-id="5bb8d-129">When you embed the Windows Media Player control in a webpage, you can write script that handles events.</span></span> <span data-ttu-id="5bb8d-130">Список событий, вызванных элементом управления проигрывателя, см. в разделе [объект Player](player-object.md).</span><span class="sxs-lookup"><span data-stu-id="5bb8d-130">For a list of events raised by the Player control, see [Player Object](player-object.md).</span></span>

<span data-ttu-id="5bb8d-131">Если тип MIME, связанный с внедренным элементом управления игрока, — Application/x-MS-WMP, можно написать обработчики событий, имеющие следующий формат:</span><span class="sxs-lookup"><span data-stu-id="5bb8d-131">If the mime type associated with an embedded Player control is application/x-ms-wmp, you can write event handlers that have the following format:</span></span>


```HTML
<SCRIPT for="Player" language="jscript" event="EventName(Params)">
  ...
</SCRIPT>
```



<span data-ttu-id="5bb8d-132">где *EventName* — это имя события проигрывателя Windows Media, а *params* — это список параметров события.</span><span class="sxs-lookup"><span data-stu-id="5bb8d-132">where *EventName* is the name of a Windows Media Player event, and *Params* is a list of the event's parameters.</span></span> <span data-ttu-id="5bb8d-133">Например, следующий код имеет обработчик для события [плайстатечанже](player-player-playstatechange.md) .</span><span class="sxs-lookup"><span data-stu-id="5bb8d-133">For example, the following code has a handler for the [PlayStateChange](player-player-playstatechange.md) event.</span></span>


```HTML
<OBJECT id="Player" type="application/x-ms-wmp" width="300" height="200">
  <PARAM name="URL" value="c:\MediaFiles\Seattle.wmv"/>
</OBJECT>

<P id="p1">...</P>

<SCRIPT for="Player" event="PlayStateChange(NewState)">
  document.getElementById("p1").innerHTML = "Play state: " + NewState;
</SCRIPT>
```



<span data-ttu-id="5bb8d-134">Если на веб-странице имеется несколько экземпляров элемента управления Player и используется формат, показанный в предыдущем примере, каждый обработчик событий привязан к конкретному экземпляру элемента управления проигрывателя.</span><span class="sxs-lookup"><span data-stu-id="5bb8d-134">If you have several instances of the Player control on a webpage and if you use the format shown in the preceeding example, then each event handler is tied to a specific instance of the Player control.</span></span> <span data-ttu-id="5bb8d-135">В предыдущем примере обработчик событий вызывается только при изменении состояния воспроизведения для элемента управления с идентификатором "Player".</span><span class="sxs-lookup"><span data-stu-id="5bb8d-135">In the preceeding example, the event handler is called only when the play state changes for the control that has id="Player".</span></span>

<span data-ttu-id="5bb8d-136">Если тип MIME, связанный с внедренным элементом управления игрока, не является Application/x-MS-WMP, можно написать обработчики событий, имеющие следующий формат:</span><span class="sxs-lookup"><span data-stu-id="5bb8d-136">If the mime type associated with an embedded Player control is not application/x-ms-wmp, you can write event handlers that have the following format:</span></span>


```HTML
<SCRIPT language="jscript">
  function OnDSEventNameEvt(Params)
  {...}
</SCRIPT>
```



<span data-ttu-id="5bb8d-137">где *EventName* — это имя события проигрывателя Windows Media, а *params* — это список параметров события.</span><span class="sxs-lookup"><span data-stu-id="5bb8d-137">where *EventName* is the name of a Windows Media Player event, and *Params* is a list of the event's parameters.</span></span> <span data-ttu-id="5bb8d-138">Например, следующий код имеет обработчик для события **плайстатечанже** .</span><span class="sxs-lookup"><span data-stu-id="5bb8d-138">For example, the following code has a handler for the **PlayStateChange** event.</span></span>


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



<span data-ttu-id="5bb8d-139">Если на веб-странице имеется несколько экземпляров элемента управления Player и используется формат, показанный в предыдущем примере, каждый обработчик событий привязан ко всем экземплярам элемента управления проигрывателя, а обработчик событий вызывается при изменении состояния воспроизведения для любого элемента управления проигрывателя на странице.</span><span class="sxs-lookup"><span data-stu-id="5bb8d-139">If you have several instances of the Player control on a webpage and if you use the format shown in the preceeding example, then each event handler is tied to all instances of the Player control and the event handler is called when the play state changes for any Player control on the page.</span></span>

> [!Note]  
> <span data-ttu-id="5bb8d-140">Если тип MIME не является Application/x-MS-WMP, событие **DoubleClick** отправляется как ондсдблкликкевт (не ондсдаублекликкевт) для совместимости с элементом управления проигрывателя версии 6,4.</span><span class="sxs-lookup"><span data-stu-id="5bb8d-140">If the mime type is not application/x-ms-wmp, the **DoubleClick** event is sent as OnDSDblClickEvt (not OnDSDoubleClickEvt) for compatibility with version 6.4 of the Player control.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="5bb8d-141">См. также</span><span class="sxs-lookup"><span data-stu-id="5bb8d-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5bb8d-142">**Использование элемента управления проигрывателя Windows Media с браузером Firefox**</span><span class="sxs-lookup"><span data-stu-id="5bb8d-142">**Using the Windows Media Player Control with Firefox**</span></span>](using-the-windows-media-player-control-with-firefox.md)
</dt> </dl>

 

 




