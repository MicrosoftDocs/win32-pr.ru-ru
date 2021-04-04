---
title: Использование HTML с проигрывателем Windows Media
description: Использование HTML с проигрывателем Windows Media
ms.assetid: 321d4396-511b-4f0d-9ee9-8bdddceedc0e
keywords:
- Проигрыватель Windows Media, HTML
- Объектная модель проигрывателя Windows Media, HTML
- Объектная модель, HTML
- Элемент управления ActiveX проигрывателя Windows Media, HTML для объектной модели
- Элемент управления ActiveX, HTML для объектной модели
- Элемент управления ActiveX в проигрывателе Windows Media Mobile, HTML для объектной модели
- Проигрыватель Windows Media Mobile, HTML для объектной модели
- HTML с проигрывателем Windows Media
- Внедрение веб-страниц, HTML
- внедрение, веб-страницы
- команды сценария
- Перелистывание URL-адресов
- Мультимедийная потоковая передача мультимедиа
- поддержка браузеров
- Отображение веб-страниц
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7cd96932573802d0a75f95a437b2c7284b3de44
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888499"
---
# <a name="using-html-with-windows-media-player"></a><span data-ttu-id="50bd7-118">Использование HTML с проигрывателем Windows Media</span><span class="sxs-lookup"><span data-stu-id="50bd7-118">Using HTML with Windows Media Player</span></span>

## <a name="overview"></a><span data-ttu-id="50bd7-119">Обзор</span><span class="sxs-lookup"><span data-stu-id="50bd7-119">Overview</span></span>

<span data-ttu-id="50bd7-120">Использование HTML с проигрывателем Windows Media Player — отличный способ сочетать аудио и видео с текстом и графикой.</span><span class="sxs-lookup"><span data-stu-id="50bd7-120">Using HTML with Windows Media Player is an excellent way to combine audio and video with text and graphics.</span></span> <span data-ttu-id="50bd7-121">Вы можете внедрить элемент управления проигрывателя Windows Media на веб-страницу, если хотите дополнить статическое содержимое или создать веб-приложения с цифровым мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="50bd7-121">You can embed the Windows Media Player control in a webpage when you want to supplement your static content or create Web applications with digital media.</span></span> <span data-ttu-id="50bd7-122">С другой стороны, если вы хотите дополнить свой цифровой мультимедиа с помощью HTML, вы можете отображать веб-страницы в полном режиме проигрывателя, ссылаясь на них в списках воспроизведения метафайлов Windows Media.</span><span class="sxs-lookup"><span data-stu-id="50bd7-122">When you want to supplement your digital media with HTML, on the other hand, you can display webpages in the full mode of the Player by referencing them in Windows Media metafile playlists.</span></span>

<span data-ttu-id="50bd7-123">При написании пользовательских программ, которые внедряют элемент управления проигрывателя Windows Media в удаленном режиме, можно также управлять веб-страницами, отображаемыми на различных панелях полноэкранного режима проигрывателя, когда пользователь отсоединяет элемент управления.</span><span class="sxs-lookup"><span data-stu-id="50bd7-123">If you write custom programs that embed the Windows Media Player control in remote mode, you can also control the webpages displayed in the various panes of the full mode of the Player when your users undock the control.</span></span> <span data-ttu-id="50bd7-124">Это позволяет сохранить непрерывность между закрепленными и незакрепленными состояниями.</span><span class="sxs-lookup"><span data-stu-id="50bd7-124">This lets you preserve continuity between the docked and undocked states.</span></span>

## <a name="web-embedding"></a><span data-ttu-id="50bd7-125">Веб-внедрение</span><span class="sxs-lookup"><span data-stu-id="50bd7-125">Web Embedding</span></span>

<span data-ttu-id="50bd7-126">Элемент управления проигрывателя Windows Media можно использовать как часть создаваемой веб-страницы.</span><span class="sxs-lookup"><span data-stu-id="50bd7-126">You can use the Windows Media Player control as part of a webpage you create.</span></span> <span data-ttu-id="50bd7-127">См. раздел [встраивание элемента управления проигрывателя Windows Media на веб-страницу](embedding-the-windows-media-player-control-in-a-web-page.md).</span><span class="sxs-lookup"><span data-stu-id="50bd7-127">See [Embedding the Windows Media Player Control in a Web Page](embedding-the-windows-media-player-control-in-a-web-page.md).</span></span>

## <a name="script-commands-and-url-flipping"></a><span data-ttu-id="50bd7-128">Команды скрипта и зеркальное отображение URL-адресов</span><span class="sxs-lookup"><span data-stu-id="50bd7-128">Script Commands and URL Flipping</span></span>

<span data-ttu-id="50bd7-129">Команды сценария — это пары "текст-значение", которые можно внедрять в цифровые файлы мультимедиа или потоки.</span><span class="sxs-lookup"><span data-stu-id="50bd7-129">Script commands are text/value pairs you can embed in your digital media files or streams.</span></span> <span data-ttu-id="50bd7-130">Вы можете использовать пользовательские команды сценария только для активации кода сценария, при этом проигрыватель Windows Media автоматически обрабатывает другие команды сценариев.</span><span class="sxs-lookup"><span data-stu-id="50bd7-130">You might use custom script commands solely to trigger script code, while letting Windows Media Player handle other script commands automatically.</span></span>

<span data-ttu-id="50bd7-131">При наличии нескольких веб-страниц, сопровождающих мультимедийную презентацию, команды сценария URL-адреса могут автоматически изменять страницу в одном кадре, пока элемент управления проигрывателя Windows Media продолжит воспроизведение цифрового мультимедиа в другом кадре.</span><span class="sxs-lookup"><span data-stu-id="50bd7-131">When you have several webpages that accompany a digital media presentation, URL script commands can automatically change the page in one frame while the Windows Media Player control continues playing digital media in another frame.</span></span> <span data-ttu-id="50bd7-132">Это называется отражением URL-адресов и является отличным способом создания показа слайдов мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="50bd7-132">This is called URL flipping, and is an excellent way to create a multimedia slide show.</span></span> <span data-ttu-id="50bd7-133">Другие автоматически обрабатываемые команды сценария позволяют переключать воспроизведение в другой файл мультимедиа или поток, отображать заголовки текста или запускать события, например вставки рекламы, определенные в списке воспроизведения метафайла Windows Media.</span><span class="sxs-lookup"><span data-stu-id="50bd7-133">Other automatically handled script commands let you switch playback to a different media file or stream, display captioning text, or trigger events such as ad insertions defined in a Windows Media metafile playlist.</span></span>

<span data-ttu-id="50bd7-134">Дополнительные сведения о перелистывание URL-адресов см. в разделе [создание Web-Based презентаций](creating-web-based-presentations.md).</span><span class="sxs-lookup"><span data-stu-id="50bd7-134">For more information about URL flipping, see [Creating Web-Based Presentations](creating-web-based-presentations.md).</span></span>

## <a name="rich-media-streaming"></a><span data-ttu-id="50bd7-135">Мультимедийная потоковая передача мультимедиа</span><span class="sxs-lookup"><span data-stu-id="50bd7-135">Rich Media Streaming</span></span>

<span data-ttu-id="50bd7-136">Перелистывание URL-адресов лучше работает с простыми страницами, которые быстро загружаются.</span><span class="sxs-lookup"><span data-stu-id="50bd7-136">URL flipping works best with simple pages that load rapidly.</span></span> <span data-ttu-id="50bd7-137">При использовании более сложных страниц несколько компонентов передаются по отдельности, что затрудняет синхронизацию страниц с цифровым носителем.</span><span class="sxs-lookup"><span data-stu-id="50bd7-137">With more complex pages, multiple components are transferred individually, making it difficult to synchronize page display with digital media.</span></span> <span data-ttu-id="50bd7-138">Чтобы разрешить сложные мультимедийные презентации, веб-страницы могут добавляться в поток мультимедиа и доставляться проигрывателю таким же образом, как аудио и видео.</span><span class="sxs-lookup"><span data-stu-id="50bd7-138">To allow complex rich media presentations, webpages can be added to a media stream and delivered to the Player in the same way as audio and video.</span></span> <span data-ttu-id="50bd7-139">Это позволяет значительно упростить синхронизацию компонентов презентации, особенно при низкой скорости подключения.</span><span class="sxs-lookup"><span data-stu-id="50bd7-139">This lets you synchronize the components of your presentation much more easily, especially over low-speed connections.</span></span>

<span data-ttu-id="50bd7-140">Дополнительные сведения о многофункциональной потоковой передаче мультимедиа см. в разделе [создание Web-Based презентаций](creating-web-based-presentations.md).</span><span class="sxs-lookup"><span data-stu-id="50bd7-140">For more information about rich media streaming, see [Creating Web-Based Presentations](creating-web-based-presentations.md).</span></span>

## <a name="browser-support"></a><span data-ttu-id="50bd7-141">Поддержка браузеров</span><span class="sxs-lookup"><span data-stu-id="50bd7-141">Browser Support</span></span>

<span data-ttu-id="50bd7-142">Элемент управления проигрывателя Windows Media можно внедрить в Microsoft Internet Explorer, Firefox и Netscape Navigator, хотя этот процесс немного отличается для каждого из них.</span><span class="sxs-lookup"><span data-stu-id="50bd7-142">You can embed the Windows Media Player control in Microsoft Internet Explorer, Firefox, and Netscape Navigator, although the process is slightly different for each.</span></span> <span data-ttu-id="50bd7-143">Также можно создавать веб-страницы, предназначенные для работы со всеми тремя браузерами.</span><span class="sxs-lookup"><span data-stu-id="50bd7-143">You can also create webpages designed to work with all three browsers.</span></span>

<span data-ttu-id="50bd7-144">В Internet Explorer и Firefox вы внедряете элемент управления с помощью HTML-элемента OBJECT.</span><span class="sxs-lookup"><span data-stu-id="50bd7-144">With Internet Explorer and Firefox, you embed the control using the HTML OBJECT element.</span></span> <span data-ttu-id="50bd7-145">Однако навигатор требует другого подхода, так как он не поддерживает элементы управления ActiveX напрямую.</span><span class="sxs-lookup"><span data-stu-id="50bd7-145">Navigator requires a different approach, however, because it doesn't directly support ActiveX controls.</span></span> <span data-ttu-id="50bd7-146">С помощью навигатора элемент АППЛЕТ используется для внедрения на страницу специального Java-приложения.</span><span class="sxs-lookup"><span data-stu-id="50bd7-146">With Navigator, you use the APPLET element to embed a special Java applet into the page.</span></span> <span data-ttu-id="50bd7-147">Этот апплет обрабатывает связь с элементом управления ActiveX проигрывателя.</span><span class="sxs-lookup"><span data-stu-id="50bd7-147">This applet handles communication with the Player ActiveX control.</span></span>

<span data-ttu-id="50bd7-148">Дополнительные сведения о поддержке Firefox см. [в статье Использование элемента управления проигрывателя Windows Media с браузером Firefox](using-the-windows-media-player-control-with-firefox.md).</span><span class="sxs-lookup"><span data-stu-id="50bd7-148">For more information about Firefox support, see [Using the Windows Media Player Control with Firefox](using-the-windows-media-player-control-with-firefox.md).</span></span>

<span data-ttu-id="50bd7-149">Дополнительные сведения о поддержке Netscape Navigator см. в статье [Использование проигрывателя Windows Media Player с Netscape 7,1](using-windows-media-player-with-netscape-7-1.md).</span><span class="sxs-lookup"><span data-stu-id="50bd7-149">For more information about Netscape Navigator support, see [Using Windows Media Player with Netscape 7.1](using-windows-media-player-with-netscape-7-1.md).</span></span>

## <a name="displaying-web-pages-in-the-full-mode-of-the-player"></a><span data-ttu-id="50bd7-150">Отображение веб-страниц в полноэкранном режиме проигрывателя</span><span class="sxs-lookup"><span data-stu-id="50bd7-150">Displaying Web Pages in the Full Mode of the Player</span></span>

<span data-ttu-id="50bd7-151">Вы можете расширить функциональные возможности проигрывателя Windows Media или предоставить собственное представление информации, сопровождающей цифровые носители, отображая веб-страницы в полноэкранном режиме проигрывателя.</span><span class="sxs-lookup"><span data-stu-id="50bd7-151">You can extend the functionality of Windows Media Player or provide a custom view of information that accompanies your digital media by displaying webpages in the full mode of the Player.</span></span> <span data-ttu-id="50bd7-152">Это Хтмлвиев функция метафайлов Windows Media.</span><span class="sxs-lookup"><span data-stu-id="50bd7-152">This is the HTMLView feature of Windows Media metafiles.</span></span> <span data-ttu-id="50bd7-153">Метафайлы позволяют значительно управлять содержимым списка воспроизведения, позволяя легко переходить от картинок, вставлять рекламу и отображать изображения в проигрывателе Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="50bd7-153">Metafiles give you great control over playlist content, allowing you to seamlessly transition between clips, insert advertisements, and display still images in Windows Media Player.</span></span> <span data-ttu-id="50bd7-154">Чтобы отобразить веб-страницы в полноэкранном режиме проигрывателя, используйте элемент PARAM, чтобы добавить URL-ссылки на записи списка воспроизведения или во все списки воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="50bd7-154">To display webpages in the full mode of the Player, you use the PARAM element to add URL references to your playlist entries or to entire playlists.</span></span>

<span data-ttu-id="50bd7-155">Дополнительные сведения об использовании веб-страниц в метафайлах см. [в разделе Отображение Web-страниц в проигрывателе Windows Media](displaying-web-pages-in-windows-media-player.md).</span><span class="sxs-lookup"><span data-stu-id="50bd7-155">For more information about using webpages in metafiles, see [Displaying Web Pages in Windows Media Player](displaying-web-pages-in-windows-media-player.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="50bd7-156">См. также</span><span class="sxs-lookup"><span data-stu-id="50bd7-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="50bd7-157">**Сведения об объектной модели проигрывателя**</span><span class="sxs-lookup"><span data-stu-id="50bd7-157">**About the Player Object Model**</span></span>](about-the-player-object-model.md)
</dt> </dl>

 

 




