---
title: Пример списка воспроизведения для радиостанции
description: Пример списка воспроизведения для радиостанции
ms.assetid: 99b33036-6391-446c-816c-8d5d76107d37
keywords:
- Списки воспроизведения метафайлов Windows Media, примеры списков воспроизведения
- списки воспроизведения, примеры списков воспроизведения
- списки воспроизведения метафайлов, примеры списков воспроизведения
- Списки воспроизведения метафайлов Windows Media, примеры списков воспроизведения
- списки воспроизведения, примеры списков воспроизведения
- списки воспроизведения метафайлов, примеры списков воспроизведения
- Списки воспроизведения метафайлов Windows Media, примеры списков воспроизведения
- списки воспроизведения, образцы списков воспроизведения
- списки воспроизведения метафайлов, образцы списков воспроизведения
- Списки воспроизведения метафайлов Windows Media, пример кода
- списки воспроизведения, пример кода
- списки воспроизведения метафайлов, пример кода
- Список воспроизведения метафайлов Windows Media, пример списка воспроизведения радиостанции
- списки воспроизведения, пример списка воспроизведения радиостанции
- списки воспроизведения метафайлов, пример списка воспроизведения радиостанции
- Проигрыватель Windows Media, примеры списков воспроизведения
- Проигрыватель Windows Media, примеры списков воспроизведения
- Проигрыватель Windows Media, образцы списков воспроизведения
- Проигрыватель Windows Media, пример списка воспроизведения радиостанции
- примеры списков воспроизведения
- примеры списков воспроизведения
- Образцы списков воспроизведения
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: da797937ee461ccb3afbfb000e7704486d6896e4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104410828"
---
# <a name="an-example-radio-station-playlist"></a><span data-ttu-id="27865-125">Пример списка воспроизведения для радиостанции</span><span class="sxs-lookup"><span data-stu-id="27865-125">An Example Radio Station Playlist</span></span>

<span data-ttu-id="27865-126">В следующем примере кода показано, как создать список воспроизведения для сканирования трех радиостанций-переключателей.</span><span class="sxs-lookup"><span data-stu-id="27865-126">The following example code illustrates how to create a playlist to scan three rock radio stations.</span></span> <span data-ttu-id="27865-127">Вымышленная фирма Adventure Works Radio Марка находится в списке воспроизведения и всех отдельных потоках в списке воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="27865-127">The fictitious company Adventure Works Radio brand is on the playlist and on all of the individual streams within the playlist.</span></span> <span data-ttu-id="27865-128">При написании кода измените все URL-адреса и имена файлов на допустимые имена файлов, доступные проигрывателю Windows Media.</span><span class="sxs-lookup"><span data-stu-id="27865-128">When you write your code, change all URLs and file names to valid file names that are accessible to your Windows Media Player.</span></span>

<span data-ttu-id="27865-129">Для каждой станции создается список воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="27865-129">A playlist is created for each of the stations.</span></span> <span data-ttu-id="27865-130">Четвертый список воспроизведения просматривает первые три.</span><span class="sxs-lookup"><span data-stu-id="27865-130">A fourth playlist scans through the first three.</span></span> <span data-ttu-id="27865-131">Списки воспроизведения создаются для ссылки на динамически создаваемые объявления и имеют фирменную символику Adventure Works Radio.</span><span class="sxs-lookup"><span data-stu-id="27865-131">The playlists are created to reference dynamically generated advertisements and have Adventure Works Radio branding.</span></span>

<span data-ttu-id="27865-132">Один из списков воспроизведения, представляющих радиостанции, может выглядеть следующим образом.</span><span class="sxs-lookup"><span data-stu-id="27865-132">One of the playlists representing a radio station might look like this.</span></span>


```XML
<ASX version = "3.0">
    <TITLE>Adventure Works Radio</TITLE>
    <MOREINFO href = "https://www.adventure-works.com" />
    <ENTRY clientSkip = "no" skipIfRef = "yes">
       <REF href = "https://www.adventure-works.com/ad.asp/" />
    </ENTRY>
    <ENTRY>
        <TITLE>MyWRCK Radio</TITLE>
        <ABSTRACT>MyTown's Best Rock 'n Roll</ABSTRACT>
        <COPYRIGHT>2000 RadioNetwork</COPYRIGHT>
        <MOREINFO href = "https://www.adventure-works.com" />
        <REF href = "https://www.adventure-works.com" />
        <REF href = "https://backup.adventure-works.com" />
    </ENTRY>
</ASX>

```



<span data-ttu-id="27865-133">Затем список воспроизведения может быть создан в виде ссылок на отдельные списки воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="27865-133">The playlist can then be constructed of references to the individual playlists.</span></span>

<span data-ttu-id="27865-134">Пример кода</span><span class="sxs-lookup"><span data-stu-id="27865-134">Example Code</span></span>


```XML
<ASX Version = "3.0">
    <TITLE>Adventure Works Radio Top 3 Rock Stations</TITLE>
    <MOREINFO href = "https://www.adventure-works.com/MyTop3Rocks"/>
    <REPEAT>
        <ENTRY ClientSkip = "no">
            <REF HREF = "https://www.adventure-works.com/ad.asp/">
        </ENTRY>
        <DURATION VALUE="00:00:30" />
        <ENTRYREF  HREF = "https://www.adventure-works.com/asx/RadioNetwork.wax"/>
        <DURATION VALUE="00:00:30" />
        <ENTRYREF HREF = "https://www.adventure-works.com/asx/RadioNetwork2.wax/>
        <DURATION VALUE="00:00:30" />
        <ENTRYREF HREF = "https://www.adventure-works.com/asx/RadioNetwork3.wax"/>
    </REPEAT>
</ASX>

```



<span data-ttu-id="27865-135">В этом примере воспроизводится рекламное объявление, за которым следует 30 секунд каждой из трех станций, на которые имеется ссылка, один за другим.</span><span class="sxs-lookup"><span data-stu-id="27865-135">This example would play an ad followed by 30 seconds of each of the three stations referenced, one after the other.</span></span> <span data-ttu-id="27865-136">Этот цикл будет повторяться в течение неограниченного времени, так как атрибут **Count** элемента **Repeat** не определен.</span><span class="sxs-lookup"><span data-stu-id="27865-136">This cycle will repeat indefinitely because the **COUNT** attribute of the **REPEAT** element is not defined.</span></span>

-   <span data-ttu-id="27865-137">Названия организаций, предприятий и изделий, а также имена и события, используемые в качестве примеров, являются вымышленными.</span><span class="sxs-lookup"><span data-stu-id="27865-137">The example companies, organizations, products, people and events depicted herein are fictitious.</span></span> <span data-ttu-id="27865-138">Возможное сходство с реально существующими организациями, предприятиями, изделиями, лицами и событиями следует рассматривать как случайное.</span><span class="sxs-lookup"><span data-stu-id="27865-138">No association with any real company, organization, product, person or event is intended or should be inferred.</span></span>

## <a name="related-topics"></a><span data-ttu-id="27865-139">См. также</span><span class="sxs-lookup"><span data-stu-id="27865-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="27865-140">**Создание списков воспроизведения метафайлов**</span><span class="sxs-lookup"><span data-stu-id="27865-140">**Creating Metafile Playlists**</span></span>](creating-metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="27865-141">**Примеры списков воспроизведения**</span><span class="sxs-lookup"><span data-stu-id="27865-141">**Example Playlists**</span></span>](example-playlists.md)
</dt> <dt>

[<span data-ttu-id="27865-142">**Списки воспроизведения метафайлов**</span><span class="sxs-lookup"><span data-stu-id="27865-142">**Metafile Playlists**</span></span>](metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="27865-143">**Справочник по элементам метафайлов Windows Media**</span><span class="sxs-lookup"><span data-stu-id="27865-143">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="27865-144">**Путеводитель по метафайлу Windows Media**</span><span class="sxs-lookup"><span data-stu-id="27865-144">**Windows Media Metafile Guide**</span></span>](windows-media-metafile-guide.md)
</dt> </dl>

 

 




