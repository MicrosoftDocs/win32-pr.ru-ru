---
title: Перелистывание URL-адресов
description: Перелистывание URL-адресов
ms.assetid: 2921dff1-f740-491c-9b5e-79b7638e2065
keywords:
- Проигрыватель Windows Media, веб-презентации
- Объектная модель проигрывателя Windows Media, веб-презентации
- Объектная модель, веб-презентации
- Проигрыватель Windows Media Mobile, веб-презентации
- Элемент управления ActiveX проигрывателя Windows Media, веб-презентации
- Элемент управления мобильными устройствами ActiveX проигрывателя Windows Media, веб-презентации
- Элементы управления ActiveX, веб-презентации
- Проигрыватель Windows Media, перелистывание URL-адресов
- Объектная модель проигрывателя Windows Media, перелистывание URL-адресов
- Объектная модель, перелистывание URL-адресов
- Проигрыватель Windows Media Mobile, зеркальное отображение URL-адресов
- Элемент управления ActiveX проигрывателя Windows Media, зеркальное отображение URL-адресов
- Мобильный элемент управления ActiveX проигрывателя Windows Media, зеркальное отображение URL-адресов
- Элемент управления ActiveX, перелистывание URL-адресов
- Веб-презентации, перелистывание URL-адресов
- Создание веб-презентаций, перелистывание URL-адресов
- Перелистывание URL-адресов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 141fdd6b4a7ffc57288a08ffa2f6760cfb029847
ms.sourcegitcommit: e22adfb0dd3bb989e59455baedb4d905a877a240
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/21/2019
ms.locfileid: "103780258"
---
# <a name="url-flipping"></a><span data-ttu-id="3243d-120">Перелистывание URL-адресов</span><span class="sxs-lookup"><span data-stu-id="3243d-120">URL Flipping</span></span>

<span data-ttu-id="3243d-121">Использование веб-страниц для показа слайдов называется отражением URL-адресов и автоматически обрабатывается проигрывателем Windows Media при обнаружении команд сценария URL-адреса, внедренных в поток цифрового мультимедиа, который воспроизводится.</span><span class="sxs-lookup"><span data-stu-id="3243d-121">Using webpages for slide shows is called URL flipping, and is handled automatically by Windows Media Player when it encounters URL script commands embedded in the digital media stream it is playing.</span></span> <span data-ttu-id="3243d-122">Можно указать целевой кадр для страниц в каждой команде сценария или указать его, задав свойство **Settings. дефаултфраме** .</span><span class="sxs-lookup"><span data-stu-id="3243d-122">You can specify a target frame for your pages in each script command, or you can specify it by setting the **Settings.defaultFrame** property.</span></span> <span data-ttu-id="3243d-123">Это свойство можно задать в коде скрипта или с помощью элемента PARAM в элементе OBJECT, который внедряет элемент управления проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="3243d-123">You can set this property in script code or by using a PARAM element within the OBJECT element that embeds the Windows Media Player control.</span></span>

<span data-ttu-id="3243d-124">Вы можете работать с командами сценария URL-адреса в коде JScript точно так же, как при обработке пользовательских команд сценария.</span><span class="sxs-lookup"><span data-stu-id="3243d-124">You are free to handle the URL script commands in your JScript code just as you would handle custom script commands.</span></span> <span data-ttu-id="3243d-125">Если требуется, чтобы проигрыватель Windows Media игнорировал команды сценария URL-адреса, чтобы их можно было полностью обрабатывать самостоятельно, задайте *Параметры*. **инвокеурлс** свойство в значение false либо в коде скрипта, либо с помощью элемента Param, как описано выше.</span><span class="sxs-lookup"><span data-stu-id="3243d-125">If you want the Windows Media Player control to ignore URL script commands so that you can handle them entirely by yourself, set the *Settings*.**invokeURLs** property to false either in script code or using a PARAM element as previously described.</span></span>

<span data-ttu-id="3243d-126">В следующем примере показан типичный набор фреймов для переворачивания URL-адресов.</span><span class="sxs-lookup"><span data-stu-id="3243d-126">The following example illustrates a typical frameset for URL flipping.</span></span> <span data-ttu-id="3243d-127">Сначала создайте страницу, описывающую набор рамок:</span><span class="sxs-lookup"><span data-stu-id="3243d-127">First, create a page that describes the frameset:</span></span>


```HTML
<HTML>
<FRAMESET cols="300,*">
  <FRAME name="player" src="player.html">
  <FRAME name="content">
</FRAMESET>
</HTML>

```



<span data-ttu-id="3243d-128">Затем создайте файл player.html, указанный в наборе фреймов, с помощью следующего кода (предполагается, что файл Video. wmv находится в том же каталоге, что и файлы HTML):</span><span class="sxs-lookup"><span data-stu-id="3243d-128">Next, create the player.html file referenced in the frameset by using the following code (the video.wmv file is assumed to exist in the same directory as the HTML files):</span></span>


```HTML
<HTML>
<BODY>
<OBJECT ID="Player" CLASSID="CLSID:6BF52A52-394A-11d3-B153-00C04F79FAA6">
  <PARAM name="URL" value="https://www.proseware.com/Media/video.wmv"/>
  <PARAM name="defaultFrame" value="content"/>
</OBJECT>
</BODY>
</HTML>

```



<span data-ttu-id="3243d-129">Если веб-страницы достаточно малы для быстрой загрузки, эта установка может быть достаточной для ваших нужд.</span><span class="sxs-lookup"><span data-stu-id="3243d-129">If your webpages are small enough to load rapidly, this setup may be sufficient for your needs.</span></span> <span data-ttu-id="3243d-130">Если, с другой стороны, веб-страницы сложны, в зависимости от скорости подключения аудитории может быть более эффективной потоковая передача мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="3243d-130">If, on the other hand, your webpages are complex, rich media streaming may be more effective depending on the connection speed of your audience.</span></span>

> [!Note]  
> <span data-ttu-id="3243d-131">Перелистывание URL-адресов неправильно работает со страницами, просматриваемыми в Netscape Navigator.</span><span class="sxs-lookup"><span data-stu-id="3243d-131">URL flipping does not work correctly with pages viewed in Netscape Navigator.</span></span> <span data-ttu-id="3243d-132">Вместо отображения в кадре, указанном параметром **дефаултфраме**, каждая полученная команда сценария URL-адреса в навигаторе отображает URL-адрес в новом окне браузера.</span><span class="sxs-lookup"><span data-stu-id="3243d-132">Instead of appearing in the frame specified by **defaultFrame**, each URL script command received in Navigator displays the URL in a new browser window.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="3243d-133">См. также</span><span class="sxs-lookup"><span data-stu-id="3243d-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3243d-134">**Создание Web-Based презентаций**</span><span class="sxs-lookup"><span data-stu-id="3243d-134">**Creating Web-Based Presentations**</span></span>](creating-web-based-presentations.md)
</dt> <dt>

[<span data-ttu-id="3243d-135">**Использование сценария для управления перелистыванием URL-адресов**</span><span class="sxs-lookup"><span data-stu-id="3243d-135">**Using Script to Control URL Flipping**</span></span>](using-script-to-control-url-flipping.md)
</dt> </dl>

 

 




