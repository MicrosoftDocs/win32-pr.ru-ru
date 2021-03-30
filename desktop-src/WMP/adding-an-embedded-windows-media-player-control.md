---
title: Добавление встроенного элемента управления проигрывателя Windows Media
description: Добавление встроенного элемента управления проигрывателя Windows Media
ms.assetid: e002bf2a-c51a-448a-80a0-a35d6f32e9c0
keywords:
- Списки воспроизведения метафайлов Windows Media, Добавление встроенных элементов управления проигрывателя Windows Media
- списки воспроизведения, Добавление встроенных элементов управления проигрывателя Windows Media
- списки воспроизведения метафайлов, Добавление встроенных элементов управления проигрывателя Windows Media
- Списки воспроизведения метафайлов Windows Media, встроенные элементы управления проигрывателя Windows Media
- списки воспроизведения, встроенные элементы управления проигрывателя Windows Media
- списки воспроизведения метафайлов, встроенные элементы управления проигрывателя Windows Media
- Добавление встроенных элементов управления проигрывателя Windows Media
- Встроенные элементы управления проигрывателя Windows Media
- Проигрыватель Windows Media, Добавление внедренных элементов управления
- Проигрыватель Windows Media, внедренные элементы управления
- Хтмлвиев, Добавление встроенных элементов управления проигрывателя Windows Media
- Хтмлвиев, встроенные элементы управления проигрывателя Windows Media
- Хтмлвиев, объектная модель проигрывателя Windows Media
- Хтмлвиев, объектная модель проигрывателя
- Объектная модель проигрывателя Windows Media, о программе
- Объектная модель, сведения
- Объект Player
- Windows Media, объектная модель проигрывателя
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1dea3b11f59bff2edbcef99f1acda5fd0cfcff46
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411152"
---
# <a name="adding-an-embedded-windows-media-player-control"></a><span data-ttu-id="47037-121">Добавление встроенного элемента управления проигрывателя Windows Media</span><span class="sxs-lookup"><span data-stu-id="47037-121">Adding an Embedded Windows Media Player Control</span></span>

<span data-ttu-id="47037-122">Существует две причины, по которым можно добавить встроенный экземпляр проигрывателя Windows Media в презентацию Хтмлвиев.</span><span class="sxs-lookup"><span data-stu-id="47037-122">There are two reasons you might consider adding an embedded instance of Windows Media Player to your HTMLView presentation.</span></span> <span data-ttu-id="47037-123">Прежде всего, если требуется отобразить видеосодержимое, необходимо использовать элемент управления ActiveX проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="47037-123">First, if you want to display video content, you need to use the Windows Media Player ActiveX control.</span></span> <span data-ttu-id="47037-124">Во-вторых, если вы хотите воспользоваться преимуществами функций объектной модели проигрывателя Windows Media, находящихся на странице Хтмлвиев, необходимо использовать для этого экземпляр элемента управления Player.</span><span class="sxs-lookup"><span data-stu-id="47037-124">Second, if you want to take advantage of features of the Windows Media Player object model from within your HTMLView webpage, you must use an instance the Player control to do so.</span></span>

## <a name="using-the-player-control-to-display-video-in-htmlview-content"></a><span data-ttu-id="47037-125">Использование элемента управления "проигрыватель" для показа видео в Хтмлвиев содержимом</span><span class="sxs-lookup"><span data-stu-id="47037-125">Using the Player control to display video in HTMLView content</span></span>

<span data-ttu-id="47037-126">Как правило, проигрыватель Windows Media отображает видео с помощью панели видео и визуализации в **воспроизводимой** функции.</span><span class="sxs-lookup"><span data-stu-id="47037-126">Usually, Windows Media Player displays video using the Video and Visualization pane of the **Now Playing** feature.</span></span> <span data-ttu-id="47037-127">Так как Хтмлвиев использует эту область для вывода веб-страницы, необходимо предоставить дополнительную область экрана, если вы хотите, чтобы проигрыватель воспроизводил видео.</span><span class="sxs-lookup"><span data-stu-id="47037-127">Since HTMLView uses this area to display your webpage, you must supply an additional video display area if you want the Player to play video.</span></span> <span data-ttu-id="47037-128">Это легко сделать с помощью элемента управления ActiveX проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="47037-128">This is easy to do by using the Windows Media Player ActiveX control.</span></span>

<span data-ttu-id="47037-129">Чтобы использовать элемент управления проигрывателя для показа видео, внедрите элемент управления на веб-страницу Хтмлвиев с помощью тега **Object** .</span><span class="sxs-lookup"><span data-stu-id="47037-129">To use the Player control to display video, embed the control in your HTMLView webpage by using the **OBJECT** tag.</span></span> <span data-ttu-id="47037-130">Это тот же метод, который используется для внедрения элемента управления Player в любую веб-страницу, в которой нужно отобразить видео.</span><span class="sxs-lookup"><span data-stu-id="47037-130">This is the same technique you use to embed the Player control into any webpage in which you want to display video.</span></span> <span data-ttu-id="47037-131">В следующем примере кода показан базовый синтаксис для внедрения элемента управления Player в Internet Explorer:</span><span class="sxs-lookup"><span data-stu-id="47037-131">The following example code shows the basic syntax for embedding the Player control in Internet Explorer:</span></span>


```XML
<OBJECT id = "Player" 
    CLASSID = "CLSID:6BF52A52-394A-11d3-B153-00C04F79FAA6"> 
        <PARAM Name = "autoStart"  Value = "true">
        <PARAM Name = "uiMode" Value = "none">
</OBJECT>

```



<span data-ttu-id="47037-132">Параметр *автозапуска* обеспечивает автоматическое воспроизведение содержимого при указании нового URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="47037-132">The *autoStart* parameter ensures that content plays automatically whenever a new URL is specified.</span></span> <span data-ttu-id="47037-133">Значение, заданное для *uiMode* , не зависит от вас, но при создании содержимого для презентаций хтмлвиев обычно требуется указать "нет".</span><span class="sxs-lookup"><span data-stu-id="47037-133">The value you specify for *uiMode* is up to you, but you will usually want to specify "none" when creating content for HTMLView presentations.</span></span> <span data-ttu-id="47037-134">При внедрении элемента управления проигрывателя Windows Media для показа видео таким образом пользователь может управлять воспроизведением с помощью элементов управления проигрывателя в полноэкранном режиме, поэтому на веб-странице не нужно предоставлять дополнительные элементы управления для передачи данных.</span><span class="sxs-lookup"><span data-stu-id="47037-134">When you embed the Windows Media Player control to display video in this manner, the user can control playback using the controls of the full-mode Player, so there's no need to provide additional transport controls in the webpage.</span></span> <span data-ttu-id="47037-135">Можно использовать пространство, которое обычно выделяется для элементов управления транспорта, для вывода большего текста, графики или ссылок на другое содержимое.</span><span class="sxs-lookup"><span data-stu-id="47037-135">You can use the space you would usually allocate for transport controls to display more text, graphics, or links to other content.</span></span>

<span data-ttu-id="47037-136">Не указывайте параметр *URL-адреса* при внедрении элемента управления проигрывателя Windows Media в веб-страницу, предназначенную для отображения в хтмлвиев презентации.</span><span class="sxs-lookup"><span data-stu-id="47037-136">Do not specify a *URL* parameter when embedding the Windows Media Player control in a webpage designed to display in an HTMLView presentation.</span></span> <span data-ttu-id="47037-137">Вместо этого укажите цифровые файлы мультимедиа в файле ASX, который открывает содержимое.</span><span class="sxs-lookup"><span data-stu-id="47037-137">Instead, specify the digital media files in the .asx file that opens the content.</span></span>

<span data-ttu-id="47037-138">Так как вы предоставляете область отображения видео на веб-странице Хтмлвиев, вы можете выбрать расположение видео и размер области отображения.</span><span class="sxs-lookup"><span data-stu-id="47037-138">Because you provide the video display region in your HTMLView webpage, you can decide where to position the video and how large you want the display region to be.</span></span> <span data-ttu-id="47037-139">Например, можно разместить объект **Player** в элементе HTML **div** , а затем указать расположение элемента **div** , ситуате отображение видео на веб-странице.</span><span class="sxs-lookup"><span data-stu-id="47037-139">For example, you can contain the **Player** object within an HTML **DIV** element and then specify the position for the **DIV** to situate the video display on the webpage.</span></span> <span data-ttu-id="47037-140">Можно изменить размеры экрана видео, указав значения атрибутов Height и Width элемента **Object** .</span><span class="sxs-lookup"><span data-stu-id="47037-140">You can change the dimensions of the video display by specifying values for the height and width attributes of the **OBJECT** element.</span></span> <span data-ttu-id="47037-141">Эти значения также можно указать с помощью кода скрипта.</span><span class="sxs-lookup"><span data-stu-id="47037-141">You can also specify these values using script code.</span></span>

## <a name="using-the-player-object-model"></a><span data-ttu-id="47037-142">Использование объектной модели проигрывателя</span><span class="sxs-lookup"><span data-stu-id="47037-142">Using the Player object model</span></span>

<span data-ttu-id="47037-143">Объектная модель проигрывателя Windows Media предоставляет свойства, методы и события, которые можно использовать на веб-страницах Хтмлвиев.</span><span class="sxs-lookup"><span data-stu-id="47037-143">The Windows Media Player object model exposes properties, methods, and events that you can use in your HTMLView webpages.</span></span> <span data-ttu-id="47037-144">При внедрении элемента управления ActiveX проигрывателя Windows Media на веб-странице Хтмлвиев вы автоматически получите доступ к объектной модели проигрывателя.</span><span class="sxs-lookup"><span data-stu-id="47037-144">When you embed the Windows Media Player ActiveX control in your HTMLView webpage, you automatically have access to the Player object model.</span></span>

<span data-ttu-id="47037-145">Если вы внедряете элемент управления проигрывателя Windows Media на веб-страницу Хтмлвиев, не используйте объектную модель проигрывателя, чтобы указать воспроизводимый файл мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="47037-145">If you embed the Windows Media Player control in your HTMLView webpage, do not use the Player object model to specify the digital media file to be played.</span></span> <span data-ttu-id="47037-146">Например, если вы используете код скрипта для указания значения свойства **URL-адрес** внедренного элемента управления, веб-страница хтмлвиев будет выгружена из функции **Now** при воспроизведении файла мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="47037-146">For example, if you use script code to specify a value for the **URL** property of the embedded control, your HTMLView webpage will be unloaded from the **Now Playing** feature when the digital media file plays.</span></span> <span data-ttu-id="47037-147">Чтобы избежать этого, всегда открывать файлы. ASX, которые содержат параметры Хтмлвиев, когда необходимо использовать сценарий для открытия мультимедийного содержимого на веб-странице Хтмлвиев.</span><span class="sxs-lookup"><span data-stu-id="47037-147">To prevent this from happening, always open .asx files that include HTMLView parameters when you need to use script to open digital media content from your HTMLView webpage.</span></span>

## <a name="related-topics"></a><span data-ttu-id="47037-148">См. также</span><span class="sxs-lookup"><span data-stu-id="47037-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="47037-149">**Отображение веб-страниц в проигрывателе Windows Media**</span><span class="sxs-lookup"><span data-stu-id="47037-149">**Displaying Web Pages in Windows Media Player**</span></span>](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[<span data-ttu-id="47037-150">**Player. uiMode**</span><span class="sxs-lookup"><span data-stu-id="47037-150">**Player.uiMode**</span></span>](player-uimode.md)
</dt> <dt>

[<span data-ttu-id="47037-151">**Player. URL**</span><span class="sxs-lookup"><span data-stu-id="47037-151">**Player.URL**</span></span>](player-url.md)
</dt> <dt>

[<span data-ttu-id="47037-152">**Параметры. Автозапуск**</span><span class="sxs-lookup"><span data-stu-id="47037-152">**Settings.autoStart**</span></span>](settings-autostart.md)
</dt> </dl>

 

 




