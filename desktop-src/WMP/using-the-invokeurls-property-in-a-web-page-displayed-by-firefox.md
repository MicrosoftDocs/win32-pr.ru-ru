---
title: Использование свойства Инвокеурлс на веб-странице, отображаемой в браузере Firefox
description: Использование свойства Инвокеурлс на веб-странице, отображаемой в браузере Firefox
ms.assetid: cec2ba89-b08f-4c83-bcb2-a4df1ce6f179
keywords:
- Проигрыватель Windows Media, внедрение элемента управления ActiveX
- Объектная модель проигрывателя Windows Media, внедрение элемента управления ActiveX
- Объектная модель, внедрение элемента управления ActiveX
- Проигрыватель Windows Media Mobile, внедрение элемента управления ActiveX
- Элемент управления ActiveX проигрывателя Windows Media, внедрение
- Мобильный элемент управления ActiveX проигрывателя Windows Media, внедрение
- Элемент управления ActiveX проигрывателя Windows Media, веб-страницы
- Элемент управления мобильными устройствами ActiveX проигрывателя Windows Media, веб-страницы
- Элемент управления ActiveX проигрывателя Windows Media, свойство Инвокеурлс
- Элемент управления мобильными устройствами ActiveX проигрывателя Windows Media, свойство Инвокеурлс
- внедрение, веб-страницы
- Веб-страница внедрения, свойство Инвокеурлс
- Проигрыватель Windows Media, Firefox
- Объектная модель проигрывателя Windows Media, Firefox
- Объектная модель, Firefox
- Элемент управления ActiveX проигрывателя Windows Media, Firefox
- Элемент управления ActiveX, Firefox
- Firefox, свойство Инвокеурлс
- Внедрение веб-страниц, Firefox
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb0a2eb96e65d8fa6d2758669e3c844b2d13c0bc
ms.sourcegitcommit: e22adfb0dd3bb989e59455baedb4d905a877a240
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/21/2019
ms.locfileid: "105700728"
---
# <a name="using-the-invokeurls-property-in-a-web-page-displayed-by-firefox"></a><span data-ttu-id="42b4a-122">Использование свойства Инвокеурлс на веб-странице, отображаемой в браузере Firefox</span><span class="sxs-lookup"><span data-stu-id="42b4a-122">Using the invokeURLs Property in a Web Page Displayed by Firefox</span></span>

<span data-ttu-id="42b4a-123">Некоторые файлы мультимедиа содержат внедренные URL-адреса, для которых проигрыватель Windows Media отображает веб-страницы в окне или фрейме браузера по мере воспроизведения файла мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="42b4a-123">Some media files contain embedded URLs for which Windows Media Player displays webpages in a Web browser window or frame as the media file plays.</span></span> <span data-ttu-id="42b4a-124">В Windows Internet Explorer можно использовать свойство [Settings. инвокеурлс](settings-invokeurls.md) , чтобы указать, отображаются ли страницы для внедренных URL-адресов, а также можно использовать свойство [Settings. дефаултфраме](settings-defaultframe.md) , чтобы указать кадр для отображения таких страниц.</span><span class="sxs-lookup"><span data-stu-id="42b4a-124">In Windows Internet Explorer, you can use the [Settings.invokeURLs](settings-invokeurls.md) property to specify whether pages are displayed for embedded URLs, and you can use the [Settings.defaultFrame](settings-defaultframe.md) property to specify a frame for displaying such pages.</span></span>

<span data-ttu-id="42b4a-125">В Firefox некоторые обходные пути необходимы для установки свойства **инвокеурлс** и для указания кадра для отображения страниц для внедренных URL-адресов.</span><span class="sxs-lookup"><span data-stu-id="42b4a-125">In Firefox, some workarounds are required to set the **invokeURLs** property and to specify a frame for displaying pages for embedded URLs.</span></span>

## <a name="setting-the-invokeurls-property"></a><span data-ttu-id="42b4a-126">Установка свойства Инвокеурлс</span><span class="sxs-lookup"><span data-stu-id="42b4a-126">Setting the invokeURLs property</span></span>

<span data-ttu-id="42b4a-127">По умолчанию свойство **Settings. инвокеурлс** имеет значение true, поэтому если требуется, чтобы значение было равно false, необходимо явно задать его.</span><span class="sxs-lookup"><span data-stu-id="42b4a-127">The default value of the **Settings.invokeURLs** property is true, so if you want the value to be false, you must set it explicitly.</span></span> <span data-ttu-id="42b4a-128">В Internet Explorer можно задать **инвокеурлс** в качестве значения false в элементе param внутри элемента объекта управления Player.</span><span class="sxs-lookup"><span data-stu-id="42b4a-128">In Internet Explorer, you can set **invokeURLs** to false in a PARAM element inside the Player control's OBJECT element.</span></span>

<span data-ttu-id="42b4a-129">Подключаемый модуль Firefox не поддерживает задание свойства **инвокеурлс** в элементе param.</span><span class="sxs-lookup"><span data-stu-id="42b4a-129">The Firefox plug-in does not support setting the **invokeURLs** property in a PARAM element.</span></span>

<span data-ttu-id="42b4a-130">Это ограничение можно обойти, задав свойство **инвокеурлс** в скрипте.</span><span class="sxs-lookup"><span data-stu-id="42b4a-130">You can work around this limitation by setting the **invokeURLs** property in script.</span></span> <span data-ttu-id="42b4a-131">В следующем коде показано, как установить свойство **инвокеурлс** в значение false на веб-странице, которая может отображаться как в Internet Explorer, так и в браузере Firefox.</span><span class="sxs-lookup"><span data-stu-id="42b4a-131">The following code shows how to set the **invokeURLs** property to false in a webpage that can be displayed by both Internet Explorer and Firefox.</span></span>


```HTML
<HTML>
  <BODY OnLoad="Initialize()">

    <SCRIPT type="text/javascript">

      document.write('<OBJECT id="Player"'); 

      if(-1 != navigator.userAgent.indexOf("MSIE"))
      {               
        document.write(' classid="clsid:6BF52A52-394A-11d3-B153-00C04F79FAA6"');       
      }
      else if(-1 != navigator.userAgent.indexOf("Firefox"))
      {      
        document.write(' type="application/x-ms-wmp"');        
      }  

      document.write(' width=300 height=200>');
      document.write('<PARAM name="autoStart" value="false"/>');
      document.write('<PARAM name="url" value="c:\\MediaFiles\\Glass.wmv"/>');
      document.write('</OBJECT>'); 
      
    </SCRIPT>

    <SCRIPT>
      function Initialize()
      {
        Player.settings.invokeURLs = false;
        Player.controls.play();
      }
    </SCRIPT>

  </BODY>
</HTML>

```



## <a name="displaying-webpages-in-a-frame"></a><span data-ttu-id="42b4a-132">Отображение веб-страниц в рамке</span><span class="sxs-lookup"><span data-stu-id="42b4a-132">Displaying webpages in a frame</span></span>

<span data-ttu-id="42b4a-133">Файл мультимедиа может содержать URL-адреса, отображающие веб-страницы в окне или рамке браузера по мере воспроизведения файла мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="42b4a-133">A media file can contain URLs that display webpages in a browser window or frame as the media file is played.</span></span> <span data-ttu-id="42b4a-134">В Internet Explorer можно использовать свойство [Settings. дефаултфраме](settings-defaultframe.md) , чтобы указать кадр, в котором отображаются эти страницы.</span><span class="sxs-lookup"><span data-stu-id="42b4a-134">In Internet Explorer, you can use the [Settings.defaultFrame](settings-defaultframe.md) property to specify the frame in which those pages are displayed.</span></span> <span data-ttu-id="42b4a-135">Если не задать свойство **дефаултфраме** , URL-адреса будут отображаться в отдельном окне браузера по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="42b4a-135">If you do not set the **defaultFrame** property, URLs are displayed in a separate window of the default browser.</span></span> <span data-ttu-id="42b4a-136">Однако подключаемый модуль Firefox не поддерживает свойство **Settings. дефаултфраме** .</span><span class="sxs-lookup"><span data-stu-id="42b4a-136">However, the Firefox plug-in does not support the **Settings.defaultFrame** property.</span></span> <span data-ttu-id="42b4a-137">Чтобы обойти это ограничение, присвойте свойству **Settings. инвокеурлс** значение false и напишите обработчик событий [команду скрипта](player-player-scriptcommand.md) , который задает расположение целевого кадра.</span><span class="sxs-lookup"><span data-stu-id="42b4a-137">To work around this limitation, set the **Settings.invokeURLs** property to false and write a [ScriptCommand](player-player-scriptcommand.md) event handler that sets the location of the target frame.</span></span> <span data-ttu-id="42b4a-138">Этот метод показан в следующем примере, который работает в Internet Explorer и Firefox.</span><span class="sxs-lookup"><span data-stu-id="42b4a-138">The following example, which works in Internet Explorer and Firefox, illustrates this technique.</span></span> <span data-ttu-id="42b4a-139">Предположим, что веб-страница, показанная в примере, находится в кадрах \[ 0 \] , и вы хотите, чтобы страница URL-адреса отображалась в кадрах \[ 1 \] .</span><span class="sxs-lookup"><span data-stu-id="42b4a-139">Assume that the webpage shown in the example is in frames\[0\] and you want the URL's page to be displayed in frames\[1\].</span></span>


```HTML
<HTML>
  <BODY OnLoad="Initialize()">

    <SCRIPT type="text/javascript">

      document.write('<OBJECT id="Player"'); 

      if(-1 != navigator.userAgent.indexOf("MSIE"))
      {               
        document.write(' classid="clsid:6BF52A52-394A-11d3-B153-00C04F79FAA6"');       
      }
      else if(-1 != navigator.userAgent.indexOf("Firefox"))
      {      
        document.write(' type="application/x-ms-wmp"');        
      }  

      document.write(' width=300 height=200>');
      document.write('<PARAM name="autoStart" value="false"/>');
      document.write('<PARAM name="url" value="c:\\MediaFiles\\Glass.wmv"/>');
      document.write('</OBJECT>'); 
      
    </SCRIPT>

    <SCRIPT>
      function Initialize()
      {
        Player.settings.invokeURLs = false;
        Player.controls.play();
      }
    </SCRIPT>

    <SCRIPT for="Player" event="ScriptCommand(scType, scParam)">
      if( scType == "URL" )
      {
        parent.frames[1].location = scParam;
      }
    </script>

  </BODY>
</HTML>

```



## <a name="related-topics"></a><span data-ttu-id="42b4a-140">См. также</span><span class="sxs-lookup"><span data-stu-id="42b4a-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="42b4a-141">**Использование элемента управления проигрывателя Windows Media с браузером Firefox**</span><span class="sxs-lookup"><span data-stu-id="42b4a-141">**Using the Windows Media Player Control with Firefox**</span></span>](using-the-windows-media-player-control-with-firefox.md)
</dt> </dl>

 

 




