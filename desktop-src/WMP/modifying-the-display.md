---
title: Изменение экрана
description: Изменение экрана
ms.assetid: 21d68a34-d3d8-4b5b-b8fe-0489dc6247ec
keywords:
- Списки воспроизведения метафайлов Windows Media, изменение экранов
- списки воспроизведения, изменение отображения
- списки воспроизведения метафайлов, изменение экранов
- Списки воспроизведения метафайлов Windows Media, изменение экрана
- списки воспроизведения, изменение экрана
- списки воспроизведения метафайлов, изменение экрана
- Проигрыватель Windows Media, отображение изменений
- Проигрыватель Windows Media, изменение экранов
- Проигрыватель Windows Media, свойства текста
- Проигрыватель Windows Media, свойства изображения
- Проигрыватель Windows Media, свойства МОРЕИНФО
- Проигрыватель Windows Media, АБСТРАКТный текст
- Свойства МОРЕИНФО
- АБСТРАКТный текст
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c5c36c55b455b797446cde627449ea705b3bd2ce
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067760"
---
# <a name="modifying-the-display"></a><span data-ttu-id="5aec1-117">Изменение экрана</span><span class="sxs-lookup"><span data-stu-id="5aec1-117">Modifying the Display</span></span>

<span data-ttu-id="5aec1-118">Списки воспроизведения могут изменять пользовательский интерфейс проигрывателя Windows Media четырьмя основными способами:</span><span class="sxs-lookup"><span data-stu-id="5aec1-118">Playlists can alter the Windows Media Player user interface in four main ways:</span></span>

-   <span data-ttu-id="5aec1-119">Свойства текста</span><span class="sxs-lookup"><span data-stu-id="5aec1-119">Text properties</span></span>
-   <span data-ttu-id="5aec1-120">Свойства образа</span><span class="sxs-lookup"><span data-stu-id="5aec1-120">Image properties</span></span>
-   <span data-ttu-id="5aec1-121">Свойства МОРЕИНФО</span><span class="sxs-lookup"><span data-stu-id="5aec1-121">MOREINFO properties</span></span>
-   <span data-ttu-id="5aec1-122">АБСТРАКТный текст</span><span class="sxs-lookup"><span data-stu-id="5aec1-122">ABSTRACT text</span></span>

## <a name="text-properties"></a><span data-ttu-id="5aec1-123">Свойства текста</span><span class="sxs-lookup"><span data-stu-id="5aec1-123">Text properties</span></span>

<span data-ttu-id="5aec1-124">Проигрыватель Windows Media позволяет отображать заголовок, автор, авторские права и текст метаданных описания.</span><span class="sxs-lookup"><span data-stu-id="5aec1-124">Windows Media Player enables the display of Title, Author, Copyright, and Description metadata text.</span></span> <span data-ttu-id="5aec1-125">Метаданные клипа могут поступать из потока или из файла мультимедиа, а также из списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="5aec1-125">Clip metadata can come from the stream or media file, or it can come from a playlist.</span></span> <span data-ttu-id="5aec1-126">Отображение метаданных поступает из списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="5aec1-126">Show metadata comes from the playlist.</span></span> <span data-ttu-id="5aec1-127">Как правило, списки воспроизведения являются лучшим методом передачи свойств текста в проигрыватель Windows Media, особенно если текстовые элементы, скорее всего, изменятся.</span><span class="sxs-lookup"><span data-stu-id="5aec1-127">In general, playlists are a better method of passing text properties to Windows Media Player, especially if text elements are likely to change.</span></span> <span data-ttu-id="5aec1-128">Редактировать текст в списке воспроизведения проще, чем повторно создавать файл мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="5aec1-128">It is easier to edit text in a playlist than to re-author a media file.</span></span> <span data-ttu-id="5aec1-129">А поскольку свойства, считанные из списка воспроизведения, переопределяют те, которые содержатся в файле мультимедиа, отображаемый текст можно легко обновить, добавив новый текст к соответствующему свойству в списке воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="5aec1-129">And because properties read from a playlist override those contained in the media file, you can easily update display text by adding the new text to the corresponding property in a playlist.</span></span> <span data-ttu-id="5aec1-130">В следующем примере текст метаданных Title и Author в списке воспроизведения переопределяет заголовок и текст автора, содержащиеся в файле мультимедиа Sample. WMA.</span><span class="sxs-lookup"><span data-stu-id="5aec1-130">In the following example, the text of the Title and Author metadata in the playlist overrides the Title and Author text contained in the media file, sample.wma.</span></span>

<span data-ttu-id="5aec1-131">Текст **описания** извлекается из файла Windows Media, указанного в элементе **entry** , если в списке воспроизведения метафайла отсутствует **абстрактный** элемент.</span><span class="sxs-lookup"><span data-stu-id="5aec1-131">**DESCRIPTION** text is retrieved from a Windows Media file referenced in an **ENTRY** element unless there is an **ABSTRACT** element in a metafile playlist.</span></span> <span data-ttu-id="5aec1-132">Если имеется **абстрактный** текст, он будет отображен, переопределяя текст **описания** .</span><span class="sxs-lookup"><span data-stu-id="5aec1-132">If there is **ABSTRACT** text, it will be displayed, overriding the **DESCRIPTION** text.</span></span>


```XML
<ASX version="3.0" BANNERBAR="AUTO" >
    <ENTRY>
        <BANNER HREF="YourPath\2.gif">
        </BANNER>
        <TITLE>Upgrade</TITLE>
        <AUTHOR>Ad Department</AUTHOR>
        <REF href="YourPath\sample.wma"/>
    </ENTRY>
</ASX>

```



## <a name="image-properties"></a><span data-ttu-id="5aec1-133">Свойства образа</span><span class="sxs-lookup"><span data-stu-id="5aec1-133">Image properties</span></span>

<span data-ttu-id="5aec1-134">Изображения баннера можно добавлять в пользовательский интерфейс проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="5aec1-134">Banner images can be added to the user interface of Windows Media Player.</span></span> <span data-ttu-id="5aec1-135">Рисунок можно использовать для рекламы, предоставления информации и предоставления доступа к веб-сайтам, чтобы наименовать несколько возможностей.</span><span class="sxs-lookup"><span data-stu-id="5aec1-135">The graphic can be used for advertising, providing information, and providing access to websites, to name a few possibilities.</span></span>

<span data-ttu-id="5aec1-136">Используйте элемент **баннера** для указания графического изображения (32 пикселей высотой 194 пикселей в ширину) для отображения проигрывателем Windows Media.</span><span class="sxs-lookup"><span data-stu-id="5aec1-136">Use the **BANNER** element to specify a graphic image (32 pixels high by 194 pixels wide) for display by Windows Media Player.</span></span> <span data-ttu-id="5aec1-137">Рисунок отображается под любым содержимым видео.</span><span class="sxs-lookup"><span data-stu-id="5aec1-137">The graphic is displayed below any video content.</span></span> <span data-ttu-id="5aec1-138">Гиперссылку можно добавить в баннер с помощью дочернего элемента **мореинфо** .</span><span class="sxs-lookup"><span data-stu-id="5aec1-138">A hyperlink can be added to the banner using the **MOREINFO** child element.</span></span>

<span data-ttu-id="5aec1-139">Подсказку можно определить с помощью **абстрактного** элемента в области элемента **баннера** .</span><span class="sxs-lookup"><span data-stu-id="5aec1-139">A ToolTip can be defined by an **ABSTRACT** element within the scope of the **BANNER** element.</span></span> <span data-ttu-id="5aec1-140">Любой определенный текст подсказки можно отобразить, наведя указатель мыши на рисунок баннера.</span><span class="sxs-lookup"><span data-stu-id="5aec1-140">Any defined ToolTip text can be displayed by pausing the mouse pointer over the banner graphic.</span></span> <span data-ttu-id="5aec1-141">Если выбрать рисунок баннера с помощью указателя мыши, будет активирована Любая гиперссылка, определенная с помощью элемента **мореинфо** .</span><span class="sxs-lookup"><span data-stu-id="5aec1-141">Selecting the banner graphic with the mouse pointer will activate any hyperlink defined with the **MOREINFO** element.</span></span>

<span data-ttu-id="5aec1-142">Предпочтительный формат изображения **баннера** — формат GIF.</span><span class="sxs-lookup"><span data-stu-id="5aec1-142">The preferred **BANNER** graphics format is the GIF format.</span></span> <span data-ttu-id="5aec1-143">Формат JPG можно использовать, если изображение имеет правильный размер.</span><span class="sxs-lookup"><span data-stu-id="5aec1-143">The JPG format can be used if the graphic is properly sized.</span></span>

<span data-ttu-id="5aec1-144">В предыдущем примере показано использование элемента **баннера** .</span><span class="sxs-lookup"><span data-stu-id="5aec1-144">The previous example illustrates use of the **BANNER** element.</span></span>

> [!Note]  
> <span data-ttu-id="5aec1-145">Изображения **баннеров** не поддерживаются в файлах DRM, или если проигрыватель Windows Media внедрен в веб-страницу.</span><span class="sxs-lookup"><span data-stu-id="5aec1-145">**BANNER** images are not supported with DRM files or when Windows Media Player is embedded in a webpage.</span></span>

 

<span data-ttu-id="5aec1-146">Дополнительные сведения о баннерах см. [в статье пользовательские графики в проигрывателе Windows Media](custom-graphics-in-windows-media-player.md).</span><span class="sxs-lookup"><span data-stu-id="5aec1-146">For more information about banners, see [Custom Graphics in Windows Media Player](custom-graphics-in-windows-media-player.md).</span></span>

## <a name="moreinfo-properties"></a><span data-ttu-id="5aec1-147">Свойства МОРЕИНФО</span><span class="sxs-lookup"><span data-stu-id="5aec1-147">MOREINFO properties</span></span>

<span data-ttu-id="5aec1-148">Текстовые и графические области пользовательского интерфейса могут быть связаны с URL-адресами.</span><span class="sxs-lookup"><span data-stu-id="5aec1-148">Text and image areas of the user interface can be associated with URLs.</span></span> <span data-ttu-id="5aec1-149">Во время воспроизведения пользователи могут выбрать один из этих разделов для подключения к URL-адресу, связанному с ним, в веб-браузере.</span><span class="sxs-lookup"><span data-stu-id="5aec1-149">During playback, users can select one of these sections to connect to the URL associated with it in their Web browser.</span></span> <span data-ttu-id="5aec1-150">Например, можно связать веб-сайт рекламного объявления с изображением баннера AD, как показано в следующем фрагменте кода.</span><span class="sxs-lookup"><span data-stu-id="5aec1-150">For example, you can associate an advertiser's website with an ad banner image as shown in the following code snippet.</span></span>


```XML
<BANNER HREF="YourPath\2.gif">
    <ABSTRACT>More Information.</ABSTRACT>
    <MOREINFO HREF="https://www.proseware.com" />
</BANNER>

```



## <a name="abstract-text"></a><span data-ttu-id="5aec1-151">АБСТРАКТный текст</span><span class="sxs-lookup"><span data-stu-id="5aec1-151">ABSTRACT text</span></span>

<span data-ttu-id="5aec1-152">**Абстрактный** текст используется для отображения короткого всплывающего описания областей текста или изображений пользовательского интерфейса, с которым он связан.</span><span class="sxs-lookup"><span data-stu-id="5aec1-152">**ABSTRACT** text is used to display a short pop-up description of the text or image areas of the user interface it is associated with.</span></span> <span data-ttu-id="5aec1-153">Во время воспроизведения, если указатель мыши наведен на одну из этих областей, рядом с указателем мыши появляется подсказка с **абстрактным** текстом, связанным с областью.</span><span class="sxs-lookup"><span data-stu-id="5aec1-153">During playback, if the mouse pointer hovers over one of these areas, a ToolTip appears beside the mouse pointer displaying the **ABSTRACT** text associated with the area.</span></span> <span data-ttu-id="5aec1-154">**Абстрактный** текст извлекается из метафайла и определяется с помощью **абстрактного** элемента.</span><span class="sxs-lookup"><span data-stu-id="5aec1-154">**ABSTRACT** text is retrieved from a metafile and is defined with the **ABSTRACT** element.</span></span> <span data-ttu-id="5aec1-155">**Абстрактный** элемент может быть дочерним элементом либо элемента **записи** , либо элементом **баннера** .</span><span class="sxs-lookup"><span data-stu-id="5aec1-155">The **ABSTRACT** element can be a child element of either an **ENTRY** or a **BANNER** element.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5aec1-156">См. также</span><span class="sxs-lookup"><span data-stu-id="5aec1-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5aec1-157">**Списки воспроизведения метафайлов**</span><span class="sxs-lookup"><span data-stu-id="5aec1-157">**Metafile Playlists**</span></span>](metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="5aec1-158">**Использование списков воспроизведения метафайлов**</span><span class="sxs-lookup"><span data-stu-id="5aec1-158">**Using Metafile Playlists**</span></span>](using-metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="5aec1-159">**Справочник по элементам метафайлов Windows Media**</span><span class="sxs-lookup"><span data-stu-id="5aec1-159">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="5aec1-160">**Путеводитель по метафайлу Windows Media**</span><span class="sxs-lookup"><span data-stu-id="5aec1-160">**Windows Media Metafile Guide**</span></span>](windows-media-metafile-guide.md)
</dt> </dl>

 

 




