---
title: Базовый список воспроизведения
description: Базовый список воспроизведения
ms.assetid: fdd87959-861a-456e-b903-f5a27b4f6221
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
- Списки воспроизведения метафайлов Windows Media, пример базового списка воспроизведения
- списки воспроизведения, пример базового списка воспроизведения
- списки воспроизведения метафайлов, пример базового списка воспроизведения
- Проигрыватель Windows Media, примеры списков воспроизведения
- Проигрыватель Windows Media, примеры списков воспроизведения
- Проигрыватель Windows Media, образцы списков воспроизведения
- Проигрыватель Windows Media, пример базового списка воспроизведения
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
ms.openlocfilehash: 804bc69c9ab3b243030cd2c87545e6362ccfca79
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314787"
---
# <a name="a-basic-playlist"></a><span data-ttu-id="25391-125">Базовый список воспроизведения</span><span class="sxs-lookup"><span data-stu-id="25391-125">A Basic Playlist</span></span>

<span data-ttu-id="25391-126">В следующем примере списка воспроизведения показан базовый набор элементов списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="25391-126">The following playlist example shows a basic set of playlist elements.</span></span> <span data-ttu-id="25391-127">При написании собственного кода необходимо изменить все URL-адреса и имена файлов на допустимые имена файлов, доступные проигрывателю Windows Media.</span><span class="sxs-lookup"><span data-stu-id="25391-127">When writing your own code, you will need to change all URLs and file names to valid file names that are accessible to your Windows Media Player.</span></span>

<span data-ttu-id="25391-128">**Пример кода**</span><span class="sxs-lookup"><span data-stu-id="25391-128">**Code Example**</span></span>


```XML
<ASX version = "3.0">
<TITLE>Basic Playlist Demo</TITLE>
    <ENTRY>
        <TITLE>An Entry in a basic playlist</TITLE>
        <AUTHOR>Microsoft Corporation</AUTHOR>
        <COPYRIGHT>(c)2000 Microsoft Corporation</COPYRIGHT>
        <REF HREF = "mms://proseware.com/path/Yourfile.wma" />
    </ENTRY>
</ASX>

```



<span data-ttu-id="25391-129">В следующей таблице приведены сведения об использовании каждого элемента в примере кода.</span><span class="sxs-lookup"><span data-stu-id="25391-129">The following table provides details on the use of each element in the example code.</span></span>



| <span data-ttu-id="25391-130">График</span><span class="sxs-lookup"><span data-stu-id="25391-130">Line</span></span>                                                                                            | <span data-ttu-id="25391-131">Описание</span><span class="sxs-lookup"><span data-stu-id="25391-131">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \<ASX version = "3.0">                                                                     | <span data-ttu-id="25391-132">Элемент [ASX](asx-element.md) определяет для клиента (проигрыватель Windows Media), что это список воспроизведения метафайла Windows Media.</span><span class="sxs-lookup"><span data-stu-id="25391-132">The [ASX](asx-element.md) element identifies for the client (Windows Media Player) that this is a Windows Media metafile playlist.</span></span> <span data-ttu-id="25391-133">Атрибут **Version** указывает номер версии элементов метафайла.</span><span class="sxs-lookup"><span data-stu-id="25391-133">The **version** attribute specifies the version number of the metafile elements.</span></span>                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="25391-134">\<TITLE>Демонстрация базового списка воспроизведения\</TITLE></span><span class="sxs-lookup"><span data-stu-id="25391-134">\<TITLE>Basic Playlist Demo\</TITLE></span></span>                                                  | <span data-ttu-id="25391-135">Элемент [Title](title-element--metafile.md) определяет заголовок списка воспроизведения в целом.</span><span class="sxs-lookup"><span data-stu-id="25391-135">The [TITLE](title-element--metafile.md) element identifies the title of the playlist as a whole.</span></span> <span data-ttu-id="25391-136">Проигрыватель Windows Media отображает эти метаданные в качестве заголовка для отображения.</span><span class="sxs-lookup"><span data-stu-id="25391-136">Windows Media Player displays this metadata as the show title.</span></span>                                                                                                                                                                                                                                                                                                                                                                                               |
| \<ENTRY>                                                                                   | <span data-ttu-id="25391-137">Начинает элемент [entry](entry-element.md) .</span><span class="sxs-lookup"><span data-stu-id="25391-137">Begins the [ENTRY](entry-element.md) element.</span></span> <span data-ttu-id="25391-138">Элемент **entry** — это способ определения определенного клипа в списке воспроизведения</span><span class="sxs-lookup"><span data-stu-id="25391-138">An **ENTRY** element is a way to define a particular clip in a playlist</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="25391-139">\<TITLE>Запись в базовом списке воспроизведения\</TITLE></span><span class="sxs-lookup"><span data-stu-id="25391-139">\<TITLE>An Entry in a basic playlist\</TITLE></span></span>                                         | <span data-ttu-id="25391-140">Определяет название клипа списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="25391-140">Identifies the title of the playlist clip .</span></span> <span data-ttu-id="25391-141">Он отличается от предыдущего элемента **заголовка** , так как он вложен в элемент **entry** .</span><span class="sxs-lookup"><span data-stu-id="25391-141">It is different than the previous **TITLE** element because this one is nested within an **ENTRY** element.</span></span> <span data-ttu-id="25391-142">Проигрыватель Windows Media отображает эти метаданные как заголовок клипа.</span><span class="sxs-lookup"><span data-stu-id="25391-142">Windows Media Player displays this metadata as the clip title.</span></span>                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="25391-143">\<AUTHOR>Microsoft Corporation\</AUTHOR></span><span class="sxs-lookup"><span data-stu-id="25391-143">\<AUTHOR>Microsoft Corporation\</AUTHOR></span></span>                                              | <span data-ttu-id="25391-144">Элемент [Author](author-element.md) определяет автора клипа мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="25391-144">The [AUTHOR](author-element.md) element identifies the author of the media clip .</span></span> <span data-ttu-id="25391-145">Проигрыватель Windows Media отображает эти метаданные в качестве **автора** клипа.</span><span class="sxs-lookup"><span data-stu-id="25391-145">Windows Media Player displays this metadata as the clip **AUTHOR**.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                         |
| \<!-- This is a comment. Change the following path to point to your Windows media file --> | <span data-ttu-id="25391-146">Примечание.</span><span class="sxs-lookup"><span data-stu-id="25391-146">A comment.</span></span> <span data-ttu-id="25391-147">[Комментарии](comments.md) видны только при просмотре кода и имеют тот же формат, что и комментарии **XML** .</span><span class="sxs-lookup"><span data-stu-id="25391-147">[Comments](comments.md) are visible only when the code is viewed, and are in the same format as **XML** comments.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| \<REF HREF = "mms://proseware.com/path/Yourfile.wma" />                                    | <span data-ttu-id="25391-148">Фактический указатель на файл мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="25391-148">Actual pointer to the media file.</span></span> <span data-ttu-id="25391-149">Элемент [ref](ref-element.md) определяет строку как указатель на мультимедийное содержимое, а атрибут **href** — URL-адрес файла мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="25391-149">The [REF](ref-element.md) element identifies the line as a pointer to media content, while the **HREF** attribute is the URL to the media file.</span></span> <span data-ttu-id="25391-150">В этом случае URL-адрес использует протокол MMS, поэтому он указывает на сервер Windows Media. Файлы мультимедиа на сервере мультимедиа обычно хранятся в том же расположении, что и HTML-документы.</span><span class="sxs-lookup"><span data-stu-id="25391-150">In this case, the URL uses the MMS protocol, so it points to a Windows Media server.Media files on your media server are not usually kept in the same location as your HTML documents.</span></span><br/> <span data-ttu-id="25391-151">Обратите внимание на использование закрывающего XML элемента "/>" вместо " &lt; /реф &gt; ".</span><span class="sxs-lookup"><span data-stu-id="25391-151">Note the use of the XML-like closing of the element , "/>", instead of "&lt;/REF&gt;".</span></span> <span data-ttu-id="25391-152">Поскольку этот элемент не имеет дочерних элементов, он закрывается.</span><span class="sxs-lookup"><span data-stu-id="25391-152">Because this element does not have child elements, it closes itself.</span></span><br/> |
| \</ENTRY>                                                                                  | <span data-ttu-id="25391-153">Задает конец элемента **entry** .</span><span class="sxs-lookup"><span data-stu-id="25391-153">Specifies the end of the **ENTRY** element.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| \</ASX>                                                                                    | <span data-ttu-id="25391-154">Указывает конец списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="25391-154">Specifies the end of the playlist.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |



 

## <a name="related-topics"></a><span data-ttu-id="25391-155">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="25391-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="25391-156">**Создание списков воспроизведения метафайлов**</span><span class="sxs-lookup"><span data-stu-id="25391-156">**Creating Metafile Playlists**</span></span>](creating-metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="25391-157">**Примеры списков воспроизведения**</span><span class="sxs-lookup"><span data-stu-id="25391-157">**Example Playlists**</span></span>](example-playlists.md)
</dt> <dt>

[<span data-ttu-id="25391-158">**Списки воспроизведения метафайлов**</span><span class="sxs-lookup"><span data-stu-id="25391-158">**Metafile Playlists**</span></span>](metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="25391-159">**Справочник по элементам метафайлов Windows Media**</span><span class="sxs-lookup"><span data-stu-id="25391-159">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="25391-160">**Путеводитель по метафайлу Windows Media**</span><span class="sxs-lookup"><span data-stu-id="25391-160">**Windows Media Metafile Guide**</span></span>](windows-media-metafile-guide.md)
</dt> </dl>

 

 





