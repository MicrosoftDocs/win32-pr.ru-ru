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
# <a name="embedding-the-player-control-in-a-web-page-displayed-by-firefox"></a><span data-ttu-id="94ed0-123">Внедрение элемента управления игрока в веб-страницу, отображаемую в браузере Firefox</span><span class="sxs-lookup"><span data-stu-id="94ed0-123">Embedding the Player Control in a Web Page Displayed by Firefox</span></span>

<span data-ttu-id="94ed0-124">Чтобы внедрить элемент управления проигрывателя Windows Media на веб-страницу, которая может отображаться браузером Firefox, создайте ОБЪЕКТный элемент или элемент EMBED с одним из следующих типов MIME в качестве атрибута **Type** :</span><span class="sxs-lookup"><span data-stu-id="94ed0-124">To embed the Windows Media Player control in a webpage that can be displayed by a Firefox browser, create an OBJECT element or an EMBED element that has one of the following mime types as its **type** attribute:</span></span>

-   <span data-ttu-id="94ed0-125">Application/x-MS-WMP</span><span class="sxs-lookup"><span data-stu-id="94ed0-125">application/x-ms-wmp</span></span>
-   <span data-ttu-id="94ed0-126">приложение/ASX</span><span class="sxs-lookup"><span data-stu-id="94ed0-126">application/asx</span></span>
-   <span data-ttu-id="94ed0-127">видео/x-MS-ASF-подключаемый модуль</span><span class="sxs-lookup"><span data-stu-id="94ed0-127">video/x-ms-asf-plugin</span></span>
-   <span data-ttu-id="94ed0-128">приложение/x — Mplayer2</span><span class="sxs-lookup"><span data-stu-id="94ed0-128">application/x-mplayer2</span></span>
-   <span data-ttu-id="94ed0-129">видео/x — MS-ASF</span><span class="sxs-lookup"><span data-stu-id="94ed0-129">video/x-ms-asf</span></span>
-   <span data-ttu-id="94ed0-130">видео/x — MS-WM</span><span class="sxs-lookup"><span data-stu-id="94ed0-130">video/x-ms-wm</span></span>
-   <span data-ttu-id="94ed0-131">аудио/x-MS-WMA</span><span class="sxs-lookup"><span data-stu-id="94ed0-131">audio/x-ms-wma</span></span>
-   <span data-ttu-id="94ed0-132">Audio/x — MS-мастика</span><span class="sxs-lookup"><span data-stu-id="94ed0-132">audio/x-ms-wax</span></span>
-   <span data-ttu-id="94ed0-133">видео/x — MS-WMV</span><span class="sxs-lookup"><span data-stu-id="94ed0-133">video/x-ms-wmv</span></span>
-   <span data-ttu-id="94ed0-134">видео/x — MS-ввкс</span><span class="sxs-lookup"><span data-stu-id="94ed0-134">video/x-ms-wvx</span></span>

<span data-ttu-id="94ed0-135">Предпочтительный тип MIME — application/x-MS-WMP.</span><span class="sxs-lookup"><span data-stu-id="94ed0-135">The preferred mime type is application/x-ms-wmp.</span></span>

<span data-ttu-id="94ed0-136">В следующих примерах показано, как внедрить элемент управления "проигрыватель" с помощью элемента объекта или элемента EMBED.</span><span class="sxs-lookup"><span data-stu-id="94ed0-136">The following examples show how to embed the Player control using an OBJECT element or an EMBED element.</span></span>


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



<span data-ttu-id="94ed0-137">Предшествующие примеры работают в браузере Firefox, но не в Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="94ed0-137">The preceeding examples work in Firefox but not in Internet Explorer.</span></span> <span data-ttu-id="94ed0-138">Чтобы внедрить элемент управления проигрывателя в веб-страницу, которая может отображаться в Internet Explorer, необходимо создать элемент OBJECT с атрибутом **ClassID** , которому задан идентификатор класса для элемента управления проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="94ed0-138">To embed the Player control in a webpage that can be displayed by Internet Explorer, you must create an OBJECT element that has a **classid** attribute set to the class ID of the Windows Media Player control.</span></span>

<span data-ttu-id="94ed0-139">В следующем примере показано, как внедрить элемент управления проигрывателя Windows Media на веб-страницу, которая может отображаться правильно в Internet Explorer и Firefox.</span><span class="sxs-lookup"><span data-stu-id="94ed0-139">The following example shows how to embed the Windows Media Player control in a webpage that can be displayed correctly by both Internet Explorer and Firefox.</span></span> <span data-ttu-id="94ed0-140">Сценарий на странице определяет тип браузера и создает соответствующий тег объекта.</span><span class="sxs-lookup"><span data-stu-id="94ed0-140">Script on the page detects the browser type and generates the appropriate OBJECT tag.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="94ed0-141">См. также</span><span class="sxs-lookup"><span data-stu-id="94ed0-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="94ed0-142">**Использование элемента управления проигрывателя Windows Media с браузером Firefox**</span><span class="sxs-lookup"><span data-stu-id="94ed0-142">**Using the Windows Media Player Control with Firefox**</span></span>](using-the-windows-media-player-control-with-firefox.md)
</dt> </dl>

 

 




