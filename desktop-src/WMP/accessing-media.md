---
title: Доступ к носителю
description: Доступ к носителю
ms.assetid: 18ea844d-98c9-4168-9af2-161dda52f6bd
keywords:
- Списки воспроизведения метафайлов Windows Media, доступ к мультимедиа
- списки воспроизведения, доступ к мультимедиа
- списки воспроизведения метафайлов, доступ к мультимедиа
- Списки воспроизведения метафайлов Windows Media, доступ к мультимедиа
- списки воспроизведения, доступ к мультимедиа
- списки воспроизведения метафайлов, доступ к мультимедиа
- Списки воспроизведения метафайлов Windows Media, Управление воспроизведением
- списки воспроизведения, Управление воспроизведением
- списки воспроизведения метафайлов, Управление воспроизведением
- Списки воспроизведения метафайлов Windows Media, Настройка длительности
- списки воспроизведения, Настройка длительности
- списки воспроизведения метафайлов, Настройка длительности
- Проигрыватель Windows Media, доступ к носителю
- Проигрыватель Windows Media, доступ к мультимедиа
- Проигрыватель Windows Media, Управление воспроизведением
- Проигрыватель Windows Media, Задание длительности
- доступ к носителю
- доступ к носителю
- Управление воспроизведением
- Длительность установки
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c5a995a6816e3c46a002bd1ea924c9ea9a207000
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105691312"
---
# <a name="accessing-media"></a><span data-ttu-id="0597c-123">Доступ к носителю</span><span class="sxs-lookup"><span data-stu-id="0597c-123">Accessing Media</span></span>

<span data-ttu-id="0597c-124">Используйте списки воспроизведения для указания и управления потоками мультимедиа или мультимедийными файлами, которые воспроизводит проигрыватель Windows Media.</span><span class="sxs-lookup"><span data-stu-id="0597c-124">Use playlists to specify and to control the streaming media or media files that Windows Media Player plays.</span></span>

<span data-ttu-id="0597c-125">Используйте элемент **entry** , чтобы указать один элемент мультимедиа (файл мультимедиа или динамический поток) и любые дочерние элементы (например, изображения, ссылки **мореинфо** и **абстрактный** текст).</span><span class="sxs-lookup"><span data-stu-id="0597c-125">Use the **ENTRY** element to specify a single media element (a media file or a live stream) and any child elements (such as images, **MOREINFO** links, and **ABSTRACT** text).</span></span> <span data-ttu-id="0597c-126">Используйте элемент **ентриреф** для указания списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="0597c-126">Use an **ENTRYREF** element to specify a playlist.</span></span> <span data-ttu-id="0597c-127">Список воспроизведения может содержать один или несколько элементов **entry** или **ентриреф** .</span><span class="sxs-lookup"><span data-stu-id="0597c-127">A playlist can contain one or more **ENTRY** or **ENTRYREF** elements.</span></span> <span data-ttu-id="0597c-128">Проигрыватель Windows Media выполняет список воспроизведения, начиная с первой записи, а затем проигрывать каждую запись по очереди, пока список не будет завершен.</span><span class="sxs-lookup"><span data-stu-id="0597c-128">Windows Media Player executes a playlist by starting with the first entry and then playing each entry in turn until the list is finished.</span></span>

<span data-ttu-id="0597c-129">Элемент **entry** может указывать на любой тип мультимедиа, который проигрыватель Windows Media может воспроизвести.</span><span class="sxs-lookup"><span data-stu-id="0597c-129">An **ENTRY** element can point to any type of media that Windows Media Player can play.</span></span> <span data-ttu-id="0597c-130">Сюда входят не только файлы WMA, WMV, ASF и AVI, но также несколько, но и динамические потоки.</span><span class="sxs-lookup"><span data-stu-id="0597c-130">This includes not only .wma, .wmv, .asf, and .avi files, to name a few, but live streams as well.</span></span> <span data-ttu-id="0597c-131">Используя ряд элементов **entry** или **ентриреф** для ссылки на мультимедийное содержимое, можно использовать список воспроизведения для отправки одного потока, состоящего из нескольких источников.</span><span class="sxs-lookup"><span data-stu-id="0597c-131">By using a series of **ENTRY** or **ENTRYREF** elements to reference media content, you can use a playlist to send a single stream that consists of multiple sources.</span></span> <span data-ttu-id="0597c-132">Потоки, на которые имеются ссылки, воспроизводятся последовательно и отображаются в средстве просмотра как один непрерывный поток.</span><span class="sxs-lookup"><span data-stu-id="0597c-132">The referenced streams will play sequentially and be seen as one continuous stream by the viewer.</span></span> <span data-ttu-id="0597c-133">Например, список воспроизведения может содержать два элемента **записи** : стандартное введение из файла Windows Media с расширением WMA и динамический поток Windows Media.</span><span class="sxs-lookup"><span data-stu-id="0597c-133">For example, the playlist can contain two **ENTRY** elements: a standard introduction from a Windows Media file with a .wma extension, and a live Windows Media stream.</span></span>

> [!Note]  
> <span data-ttu-id="0597c-134">Список воспроизведения не должен содержать ссылки на файлы мультимедиа с содержимым, созданным с помощью различных версий Digital Rights Management (DRM).</span><span class="sxs-lookup"><span data-stu-id="0597c-134">A playlist must not contain links to media files that have content created with different versions of Digital Rights Management (DRM).</span></span> <span data-ttu-id="0597c-135">Если в списке воспроизведения метафайла имеются ссылки для файлов мультимедиа с содержимым DRM версии 1 и для файлов мультимедиа, созданных с помощью более поздних версий DRM, проигрыватель Windows Media воспроизводит только содержимое DRM версии 1.</span><span class="sxs-lookup"><span data-stu-id="0597c-135">In a metafile playlist, if there are links for media files with DRM version 1 content and for media files created with later DRM versions, Windows Media Player will only play the DRM version 1 content.</span></span>

 

## <a name="controlling-playback"></a><span data-ttu-id="0597c-136">Управление воспроизведением</span><span class="sxs-lookup"><span data-stu-id="0597c-136">Controlling Playback</span></span>

<span data-ttu-id="0597c-137">Используйте списки воспроизведения, чтобы контролировать не только воспроизведение клипа мультимедиа, но и то, какие части клипа воспроизводятся и как.</span><span class="sxs-lookup"><span data-stu-id="0597c-137">Use playlists to control not only which media clip is played, but also which portions of the clip are played and how.</span></span> <span data-ttu-id="0597c-138">Списки воспроизведения можно использовать для определения набора клипов, которые будут циклическими или повторяться, задать длительность воспроизведения и назначить время начала, а также начальные и конечные маркеры для каждой записи.</span><span class="sxs-lookup"><span data-stu-id="0597c-138">You can use playlists to define a set of clips to be looped or repeated, to set the duration of play, and to assign start times, and start and end markers for each entry.</span></span> <span data-ttu-id="0597c-139">Элементы **StartTime**, **стартмаркер** и **ендмаркер** работают вместе с маркерами в файле мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="0597c-139">The **STARTTIME**, **STARTMARKER**, and **ENDMARKER** elements work in conjunction with markers in the media file.</span></span>

<span data-ttu-id="0597c-140">Например, следующий список воспроизведения использует баннер рекламного объявления и связанную с ним ссылку **мореинфо** в одной **записи** и ссылается на **стартмаркер** и **ендмаркер**.</span><span class="sxs-lookup"><span data-stu-id="0597c-140">For example, the following playlist uses an ad banner and the associated **MOREINFO** link in one **ENTRY**, and references a **STARTMARKER** and **ENDMARKER**.</span></span>


```XML
<ASX version ="3.0">
<Title>Windows Media Example</Title>
<Abstract>Windows Media Technologies</Abstract>
<MoreInfo href = "https://www.proseware.com"/>
    <!--This is the first Entry -->
    <Entry>
        <Title>This is the ad</Title>
        <Author>Ad Department</Author>
        <Copyright>2000</Copyright>
        <Abstract>This is a description of the ad.</Abstract>
        <MoreInfo href = "https://www.proseware.com/"/>
        <Ref href="ad.wma"/>
        <Banner href ="purchase.gif">
           <Abstract>Click here to go to our website.</Abstract>
           <MoreInfo href = "https://www.litwareinc.com/" />
        </Banner>
     </Entry>        
    <!-- This is the second Entry -->
    <!-- The Windows Media file plays from Segment2 to Segment3 -->
    <Entry>
        <Title>Playlist Clip Number Two</Title>
        <Author>Windows Media</Author>
        <Copyright>2000</Copyright>
        <Ref href="show.wma"/>
        <StartMarker Name = "Segment2" />
        <EndMarker Name = "Segment3" />
    </Entry>
</ASX>

```



## <a name="setting-duration"></a><span data-ttu-id="0597c-141">Длительность установки</span><span class="sxs-lookup"><span data-stu-id="0597c-141">Setting Duration</span></span>

<span data-ttu-id="0597c-142">Используйте элемент **DURATION** , чтобы указать продолжительность воспроизведения клипа или набора клипов.</span><span class="sxs-lookup"><span data-stu-id="0597c-142">Use the **DURATION** element to specify how long to play a clip or set of clips.</span></span> <span data-ttu-id="0597c-143">Можно также использовать атрибут **PREVIEWMODE** элемента **ASX** в сочетании с элементом **превиевдуратион** , чтобы указать продолжительность воспроизведения клипа или набора клипов.</span><span class="sxs-lookup"><span data-stu-id="0597c-143">You can also use the **PREVIEWMODE** attribute of the **ASX** element in conjunction with the **PREVIEWDURATION** element to specify how long to play a clip or set of clips.</span></span> <span data-ttu-id="0597c-144">Задайте для атрибута **PREVIEWMODE** значение Да, чтобы использовать элемент **превиевдуратион** для указания времени воспроизведения связанного клипа.</span><span class="sxs-lookup"><span data-stu-id="0597c-144">Set the **PREVIEWMODE** attribute to YES to use the **PREVIEWDURATION** element to specify how long to play the associated clip.</span></span> <span data-ttu-id="0597c-145">Элементы **превиевдуратион** и **DURATION** имеют одинаковое поведение.</span><span class="sxs-lookup"><span data-stu-id="0597c-145">The **PREVIEWDURATION** and **DURATION** elements have the same behavior.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0597c-146">См. также</span><span class="sxs-lookup"><span data-stu-id="0597c-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0597c-147">**Списки воспроизведения метафайлов**</span><span class="sxs-lookup"><span data-stu-id="0597c-147">**Metafile Playlists**</span></span>](metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="0597c-148">**Использование списков воспроизведения метафайлов**</span><span class="sxs-lookup"><span data-stu-id="0597c-148">**Using Metafile Playlists**</span></span>](using-metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="0597c-149">**Справочник по элементам метафайлов Windows Media**</span><span class="sxs-lookup"><span data-stu-id="0597c-149">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="0597c-150">**Путеводитель по метафайлу Windows Media**</span><span class="sxs-lookup"><span data-stu-id="0597c-150">**Windows Media Metafile Guide**</span></span>](windows-media-metafile-guide.md)
</dt> </dl>

 

 




