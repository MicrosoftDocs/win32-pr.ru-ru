---
title: Расширенный список воспроизведения
description: Расширенный список воспроизведения
ms.assetid: 3f27562f-bc3b-4b7f-a83b-78317d3ad612
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
- Списки воспроизведения метафайлов Windows Media, пример расширенного списка воспроизведения
- списки воспроизведения, пример расширенного списка воспроизведения
- списки воспроизведения метафайлов, пример расширенного списка воспроизведения
- Проигрыватель Windows Media, примеры списков воспроизведения
- Проигрыватель Windows Media, примеры списков воспроизведения
- Проигрыватель Windows Media, образцы списков воспроизведения
- Проигрыватель Windows Media, пример расширенного списка воспроизведения
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
ms.openlocfilehash: f52251fedb13d41be5c94706bee4460c3f13c1e9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067764"
---
# <a name="an-advanced-playlist"></a><span data-ttu-id="30bc2-125">Расширенный список воспроизведения</span><span class="sxs-lookup"><span data-stu-id="30bc2-125">An Advanced Playlist</span></span>

<span data-ttu-id="30bc2-126">В следующем примере списка воспроизведения показано, как использовать более полный набор элементов списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="30bc2-126">The following playlist example shows how to use a more complete set of playlist elements.</span></span> <span data-ttu-id="30bc2-127">При написании собственного кода необходимо изменить все URL-адреса и имена файлов на допустимые имена файлов, доступные проигрывателю Windows Media.</span><span class="sxs-lookup"><span data-stu-id="30bc2-127">When writing your own code, you will need to change all URLs and file names to valid file names that are accessible to your Windows Media Player.</span></span>

<span data-ttu-id="30bc2-128">Пример кода</span><span class="sxs-lookup"><span data-stu-id="30bc2-128">Example Code</span></span>


``` XML
<ASX version = "3.0">
    <TITLE>Advanced Playlist Demo</TITLE>
    <ABSTRACT>More Information at this website</ABSTRACT>
    <MOREINFO HREF="https://www.microsoft.com/windows/windowsmedia" />
    <BANNER HREF = "..\samples\home.gif">
        <ABSTRACT>MSN website</ABSTRACT>
        <MOREINFO HREF = "https://www.msn.com" />
    </BANNER>
    <PARAM name="track" value="1"/>
    <ENTRY ClientSkip="no">
        <BANNER HREF = "..\sample\contact.gif">
            <ABSTRACT>Visit Our website</ABSTRACT>
            <MOREINFO HREF = "https://www.msn.com" />
        </BANNER>
        <MOREINFO HREF = "https://www.msn.com" />
        <!-- This is the ToolTip text for Title/Author/Copyright text -->
        <ABSTRACT>Visit the YourImage website</ABSTRACT>
        <TITLE>The first entry in an advanced playlist</TITLE>
        <AUTHOR>YourImage</AUTHOR>
        <COPYRIGHT>(c)2000 YourImage</COPYRIGHT>
        <!-- This is a comment.  Change the following path to point to 
            your Windows Media file -->
         <REF HREF = "..\media\laure.wma" />
    </ENTRY>

    <ENTRY>
        <TITLE>The second entry in the advanced playlist</TITLE>
        <AUTHOR>Microsoft Corporation</AUTHOR>
        <COPYRIGHT>(c)2000 Microsoft Corporation</COPYRIGHT>
        <!-- This is the ToolTip text for Title text -->
        <ABSTRACT>This is where you can include your tool tips</ABSTRACT>
        <!-- This is a comment.  Change the following path to point to 
            your Windows Media file -->
        <REF HREF = "..\media\mellow.wma" />
    </ENTRY>
</ASX>

```



<span data-ttu-id="30bc2-129">В следующей таблице описаны предыдущие дополнительные списки воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="30bc2-129">The following table describes the preceding advanced playlist.</span></span>



| <span data-ttu-id="30bc2-130">Линия</span><span class="sxs-lookup"><span data-stu-id="30bc2-130">Line</span></span>                                                                                            | <span data-ttu-id="30bc2-131">Описание</span><span class="sxs-lookup"><span data-stu-id="30bc2-131">Description</span></span>                                                                                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `<ASX version = "3.0">`                                                                     | <span data-ttu-id="30bc2-132">Элемент [ASX](asx-element.md) определяет для клиента (проигрыватель Windows Media), что это список воспроизведения метафайла Windows Media.</span><span class="sxs-lookup"><span data-stu-id="30bc2-132">The [ASX](asx-element.md) element identifies for the client (Windows Media Player) that this is a Windows Media metafile playlist.</span></span> <span data-ttu-id="30bc2-133">Атрибут **Version** указывает номер версии элементов метафайла.</span><span class="sxs-lookup"><span data-stu-id="30bc2-133">The **version** attribute specifies the version number of the metafile elements.</span></span>                                                                                                                    |
| `<TITLE>Advanced Playlist Demo</TITLE>`                                               | <span data-ttu-id="30bc2-134">Элемент [Title](title-element--metafile.md) определяет заголовок списка воспроизведения в целом.</span><span class="sxs-lookup"><span data-stu-id="30bc2-134">The [TITLE](title-element--metafile.md) element identifies the title of the playlist as a whole.</span></span> <span data-ttu-id="30bc2-135">Проигрыватель Windows Media отображает эти метаданные в качестве заголовка для отображения.</span><span class="sxs-lookup"><span data-stu-id="30bc2-135">Windows Media Player displays this metadata as the show title.</span></span>                                                                                                                                                                        |
| `<ABSTRACT>More Information at this Web Site< /ABSTRACT>`                             | <span data-ttu-id="30bc2-136">[Абстрактный](abstract-element.md) элемент предоставляет подсказку для заголовка отображения.</span><span class="sxs-lookup"><span data-stu-id="30bc2-136">The [ABSTRACT](abstract-element.md) element provides the ToolTip for the show title.</span></span>                                                                                                                                                                                                                                                   |
| `<MOREINFO HREF ="https://www.microsoft.com/windows/windowsmedia" />`                        | <span data-ttu-id="30bc2-137">Элемент [мореинфо](moreinfo-element.md) связывает заголовок "показывать" с URL-адресом.</span><span class="sxs-lookup"><span data-stu-id="30bc2-137">The [MOREINFO](moreinfo-element.md) element links the show title to an URL.</span></span> <span data-ttu-id="30bc2-138">При наведении указателя мыши на заголовок Показывать подсказку, если она определена.</span><span class="sxs-lookup"><span data-stu-id="30bc2-138">Pausing the mouse pointer over the show title accesses the ToolTip, if defined.</span></span> <span data-ttu-id="30bc2-139">При выборе пункта "показывать" заданный URL-адрес будет открыт.</span><span class="sxs-lookup"><span data-stu-id="30bc2-139">Selecting the show title will then open the designated URL.</span></span>                                                                                                                |
| `<BANNER HREF = "..\\samples\\home.gif">`                                                   | <span data-ttu-id="30bc2-140">Элемент [баннера](banner-element.md) создает баннер рекламного объявления в проигрывателе Windows Media.</span><span class="sxs-lookup"><span data-stu-id="30bc2-140">The [BANNER](banner-element.md) element creates an advertising banner in Windows Media Player.</span></span> <span data-ttu-id="30bc2-141">Атрибут **href** указывает рисунок баннера (Ширина 194 пикселей в ширину составляет 32 пикселей в высоту).</span><span class="sxs-lookup"><span data-stu-id="30bc2-141">The **HREF** attribute specifies the banner graphic (which must be 194 pixels wide by 32 pixels tall).</span></span>                                                                                                                                  |
| `<ABSTRACT>MSN website</ABSTRACT>`                                                    | <span data-ttu-id="30bc2-142">[Абстрактный](abstract-element.md) элемент предоставляет подсказку для **баннера**.</span><span class="sxs-lookup"><span data-stu-id="30bc2-142">The [ABSTRACT](abstract-element.md) element provides the ToolTip for the **BANNER**.</span></span>                                                                                                                                                                                                                                                   |
| `<MOREINFO HREF = "https://www.msn.com" </ABSTRACT>`                                      | <span data-ttu-id="30bc2-143">Элемент [мореинфо](moreinfo-element.md) связывает изображение **баннера** с URL-адресом.</span><span class="sxs-lookup"><span data-stu-id="30bc2-143">The [MOREINFO](moreinfo-element.md) element links the **BANNER** graphic to a URL.</span></span> <span data-ttu-id="30bc2-144">Наведение указателя мыши на **баннер** обращается к подсказке, если она определена.</span><span class="sxs-lookup"><span data-stu-id="30bc2-144">Holding the mouse pointer over the **BANNER** accesses a ToolTip, if defined.</span></span> <span data-ttu-id="30bc2-145">При выборе **баннера** будет открыт указанный URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="30bc2-145">Selecting the **BANNER** will open the designated URL.</span></span>                                                                                                                |
| <PARAM name = "track" value="1"/>                                                         | <span data-ttu-id="30bc2-146">Элемент [param](param-element.md) определяет пользовательский параметр.</span><span class="sxs-lookup"><span data-stu-id="30bc2-146">The [PARAM](param-element.md) element defines a custom parameter.</span></span> <span data-ttu-id="30bc2-147">Атрибут **Name** определяет имя пользовательского параметра как Track.</span><span class="sxs-lookup"><span data-stu-id="30bc2-147">The **name** attribute defines the name of the custom parameter as "track".</span></span> <span data-ttu-id="30bc2-148">Атрибут **value** определяет значение "Track", равное "1".</span><span class="sxs-lookup"><span data-stu-id="30bc2-148">The **value** attribute defines the value of "track" to be "1".</span></span>                                                                                                                          |
| `</BANNER>`                                                                                 | <span data-ttu-id="30bc2-149">Закрывает элемент **баннера**</span><span class="sxs-lookup"><span data-stu-id="30bc2-149">Closes the **BANNER** element</span></span>                                                                                                                                                                                                                                                                                                           |
| `<ENTRY ClientSkip="no">`                                                                   | <span data-ttu-id="30bc2-150">Начинает блок элемента [entry](entry-element.md) .</span><span class="sxs-lookup"><span data-stu-id="30bc2-150">Begins the [ENTRY](entry-element.md) element block.</span></span> <span data-ttu-id="30bc2-151">Этот элемент определяет клип в списке воспроизведения, указывая ссылку в элементе **ref** .</span><span class="sxs-lookup"><span data-stu-id="30bc2-151">This element defines a clip in a playlist by specifying a link in the **REF** element.</span></span> <span data-ttu-id="30bc2-152">Если для параметра **клиентскип** задать значение "нет", то пользователь не сможет выполнить перемотку вперед или перейти к следующему клипу</span><span class="sxs-lookup"><span data-stu-id="30bc2-152">Setting **ClientSkip** to "no" means that the user cannot fast forward or jump to the next clip</span></span>                                                                                             |
| `<BANNER HREF = "..\\samples\\contact.gif">`                                                | <span data-ttu-id="30bc2-153">Создает баннер объявления.</span><span class="sxs-lookup"><span data-stu-id="30bc2-153">Creates an advertising banner.</span></span> <span data-ttu-id="30bc2-154">**Href** — это рисунок баннера (194x32 пикселей).</span><span class="sxs-lookup"><span data-stu-id="30bc2-154">The **HREF** is the banner graphic (194x32 pixels).</span></span>                                                                                                                                                                                                                                                      |
| `<ABSTRACT>Visit Our website< /ABSTRACT>`                                             | <span data-ttu-id="30bc2-155">Предоставляет подсказку для баннера.</span><span class="sxs-lookup"><span data-stu-id="30bc2-155">Provides the ToolTip for the banner.</span></span>                                                                                                                                                                                                                                                                                                    |
| `<MOREINFO HREF = "https://www.msn.com" />`                                                  | <span data-ttu-id="30bc2-156">Содержит ссылку на URL-адрес баннера.</span><span class="sxs-lookup"><span data-stu-id="30bc2-156">Provides a link to the URL for the banner.</span></span> <span data-ttu-id="30bc2-157">При выборе баннера подключается к URL-адресу.</span><span class="sxs-lookup"><span data-stu-id="30bc2-157">Selecting the banner connects to the URL.</span></span>                                                                                                                                                                                                                                                    |
| `</BANNER>`                                                                                 | <span data-ttu-id="30bc2-158">Закрывает элемент **баннера**</span><span class="sxs-lookup"><span data-stu-id="30bc2-158">Closes the **BANNER** element</span></span>                                                                                                                                                                                                                                                                                                           |
| `<MOREINFO HREF = "https://www.msn.com" />`                                                  | <span data-ttu-id="30bc2-159">Содержит ссылку на URL-адрес для текста **заголовка** клипа.</span><span class="sxs-lookup"><span data-stu-id="30bc2-159">Provides a link to the URL for the clip **Title** text.</span></span>                                                                                                                                                                                                                                                                                 |
| `<!--This is the ToolTip text for the Title text -->`                                       | <span data-ttu-id="30bc2-160">Примечание.</span><span class="sxs-lookup"><span data-stu-id="30bc2-160">A comment.</span></span> <span data-ttu-id="30bc2-161">[Комментарии](comments.md) отображаются только при просмотре кода.</span><span class="sxs-lookup"><span data-stu-id="30bc2-161">[Comments](comments.md) are only be visible when the code is viewed.</span></span>                                                                                                                                                                                                                                                        |
| `<Abstract>Visit the YourImage website</abstract>`                                    | <span data-ttu-id="30bc2-162">Предоставляет подсказку для текста **заголовка** клипа.</span><span class="sxs-lookup"><span data-stu-id="30bc2-162">Provides the ToolTip for the clip **Title** text.</span></span>                                                                                                                                                                                                                                                                                       |
| `<TITLE>The first entry in an advanced playlist</TITLE>`                              | <span data-ttu-id="30bc2-163">Определяет заголовок клипа.</span><span class="sxs-lookup"><span data-stu-id="30bc2-163">Identifies the title of the clip.</span></span> <span data-ttu-id="30bc2-164">Это **заголовок** клипа, так как он вложен в элемент **entry** .</span><span class="sxs-lookup"><span data-stu-id="30bc2-164">It is the clip **TITLE** because it is nested within an **ENTRY** element.</span></span> <span data-ttu-id="30bc2-165">Проигрыватель Windows Media отображает эти метаданные как заголовок клипа.</span><span class="sxs-lookup"><span data-stu-id="30bc2-165">Windows Media Player displays this metadata as the clip title.</span></span>                                                                                                                                                             |
| `<AUTHOR>YourImage</AUTHOR>`                                                          | <span data-ttu-id="30bc2-166">Определяет автора клипа мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="30bc2-166">Identifies the author of the media clip.</span></span> <span data-ttu-id="30bc2-167">Эти метаданные отображаются проигрывателем Windows Media как **Автор** клипа.</span><span class="sxs-lookup"><span data-stu-id="30bc2-167">This metadata is displayed as the clip **AUTHOR** by Windows Media Player.</span></span>                                                                                                                                                                                                                     |
| `<COPYRIGHT>(c)2000 YourImage</COPYRIGHT>`                                            | <span data-ttu-id="30bc2-168">Элемент [Copyright](copyright-element.md) указывает авторские права, связанные с клипом мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="30bc2-168">The [COPYRIGHT](copyright-element.md) element specifies the copyrights associated with the media clip.</span></span> <span data-ttu-id="30bc2-169">Проигрыватель Windows Media отображает эти метаданные в виде обрезки АВТОРских прав.</span><span class="sxs-lookup"><span data-stu-id="30bc2-169">Windows Media Player displays this metadata as the clip COPYRIGHT.</span></span>                                                                                                                                                              |
| `<!-- This is a comment. Change the following path to point to your Windows Media file -->` | <span data-ttu-id="30bc2-170">Комментарий в том же формате, что и **XML-** комментарии.</span><span class="sxs-lookup"><span data-stu-id="30bc2-170">A comment, in the same format as **XML** comments.</span></span>                                                                                                                                                                                                                                                                                      |
| `<REF HREF = "..\\media\\laure.wma" />`                                                     | <span data-ttu-id="30bc2-171">URL-адрес мультимедийного содержимого.</span><span class="sxs-lookup"><span data-stu-id="30bc2-171">URL for the media content.</span></span> <span data-ttu-id="30bc2-172">Элемент [ref](ref-element.md) определяет строку как указатель на мультимедийное содержимое.</span><span class="sxs-lookup"><span data-stu-id="30bc2-172">The [REF](ref-element.md) element identifies the line as a pointer to media content.</span></span> <span data-ttu-id="30bc2-173">Атрибут **href** является URL-адресом файла. Обратите внимание на использование закрытия элемента, похожего на XML, "/>" вместо " &lt; /реф &gt; ".</span><span class="sxs-lookup"><span data-stu-id="30bc2-173">The **HREF** attribute is the URL to the file.Note the use of the XML-like closing of the element , "/>" instead of "&lt;/REF&gt;".</span></span> <span data-ttu-id="30bc2-174">Поскольку этот элемент не имеет дочерних элементов, он закрывается.</span><span class="sxs-lookup"><span data-stu-id="30bc2-174">Because this element does not have child elements, it closes itself.</span></span><br/> |
| `</ENTRY>`                                                                                  | <span data-ttu-id="30bc2-175">Задает конец первого элемента **entry** .</span><span class="sxs-lookup"><span data-stu-id="30bc2-175">Specifies the end of the of the first **ENTRY** element.</span></span>                                                                                                                                                                                                                                                                                |
| `<ENTRY>`                                                                                   | <span data-ttu-id="30bc2-176">Начинает второй элемент **entry** .</span><span class="sxs-lookup"><span data-stu-id="30bc2-176">Begins the second **ENTRY** element.</span></span>                                                                                                                                                                                                                                                                                                    |
| `<TITLE>The second Entry in the advanced playlist</TITLE>`                            | <span data-ttu-id="30bc2-177">Определяет заголовок второго клипа.</span><span class="sxs-lookup"><span data-stu-id="30bc2-177">Identifies the title of the second clip.</span></span>                                                                                                                                                                                                                                                                                                |
| `<AUTHOR>Microsoft Corporation</AUTHOR>`                                              | <span data-ttu-id="30bc2-178">Определяет автора второго клипа мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="30bc2-178">Identifies the author of the second media clip.</span></span>                                                                                                                                                                                                                                                                                         |
| `<!--This is the ToolTip text for the Title/Author/Copyright text -->`                      | <span data-ttu-id="30bc2-179">Примечание.</span><span class="sxs-lookup"><span data-stu-id="30bc2-179">A comment.</span></span> <span data-ttu-id="30bc2-180">Он будет отображаться только при просмотре кода.</span><span class="sxs-lookup"><span data-stu-id="30bc2-180">It will only be visible when the code is viewed.</span></span>                                                                                                                                                                                                                                                                             |
| `<ABSTRACT>This is where you can include your tool tips</ABSTRACT>`                   | <span data-ttu-id="30bc2-181">Это текст подсказки для текста **заголовка** клипа.</span><span class="sxs-lookup"><span data-stu-id="30bc2-181">This is the ToolTip text for the **TITLE** text of the clip.</span></span>                                                                                                                                                                                                                                                                            |
| `<!-- This is a comment. Change the following path to point to your Windows Media file -->` | <span data-ttu-id="30bc2-182">Примечание.</span><span class="sxs-lookup"><span data-stu-id="30bc2-182">A comment.</span></span> <span data-ttu-id="30bc2-183">Он будет отображаться только при просмотре кода.</span><span class="sxs-lookup"><span data-stu-id="30bc2-183">It will only be visible when the code is viewed.</span></span>                                                                                                                                                                                                                                                                             |
| `<REF HREF = ..\\media\\mellow.wma" />`                                                     | <span data-ttu-id="30bc2-184">Определяет строку как указатель на мультимедийное содержимое.</span><span class="sxs-lookup"><span data-stu-id="30bc2-184">Identifies the line as a pointer to media content.</span></span> <span data-ttu-id="30bc2-185">Атрибут **href** является URL-адресом файла.</span><span class="sxs-lookup"><span data-stu-id="30bc2-185">The **HREF** attribute is the URL to the file.</span></span>                                                                                                                                                                                                                                       |
| `</ENTRY>`                                                                                  | <span data-ttu-id="30bc2-186">Задает конец второго элемента **entry** .</span><span class="sxs-lookup"><span data-stu-id="30bc2-186">Specifies the end of the second **ENTRY** element.</span></span>                                                                                                                                                                                                                                                                                      |
| `</ASX>`                                                                                    | <span data-ttu-id="30bc2-187">Указывает конец списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="30bc2-187">Specifies the end of the playlist.</span></span>                                                                                                                                                                                                                                                                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="30bc2-188">См. также</span><span class="sxs-lookup"><span data-stu-id="30bc2-188">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="30bc2-189">**Создание списков воспроизведения метафайлов**</span><span class="sxs-lookup"><span data-stu-id="30bc2-189">**Creating Metafile Playlists**</span></span>](creating-metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="30bc2-190">**Примеры списков воспроизведения**</span><span class="sxs-lookup"><span data-stu-id="30bc2-190">**Example Playlists**</span></span>](example-playlists.md)
</dt> <dt>

[<span data-ttu-id="30bc2-191">**Списки воспроизведения метафайлов**</span><span class="sxs-lookup"><span data-stu-id="30bc2-191">**Metafile Playlists**</span></span>](metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="30bc2-192">**Справочник по элементам метафайлов Windows Media**</span><span class="sxs-lookup"><span data-stu-id="30bc2-192">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="30bc2-193">**Путеводитель по метафайлу Windows Media**</span><span class="sxs-lookup"><span data-stu-id="30bc2-193">**Windows Media Metafile Guide**</span></span>](windows-media-metafile-guide.md)
</dt> </dl>

 

 





