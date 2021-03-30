---
title: Программный доступ к библиотеке
description: Программный доступ к библиотеке
ms.assetid: f48fbb49-5b79-4a78-af72-8509c460a149
keywords:
- Проигрыватель Windows Media, Библиотека
- Объектная модель проигрывателя Windows Media, Библиотека
- Объектная модель, Библиотека
- Элемент управления ActiveX проигрывателя Windows Media, Библиотека для объектной модели
- Элемент управления ActiveX, Библиотека для объектной модели
- Элемент управления ActiveX мобильных устройств Windows Media Player, Библиотека для объектной модели
- Проигрыватель Windows Media Mobile, Библиотека для объектной модели
- Библиотека проигрывателя Windows Media, доступ программным способом
- Библиотека, доступ
- программный доступ к библиотеке проигрывателя Windows Media
- Библиотека проигрывателя Windows Media, добавление элементов мультимедиа
- Библиотека, добавление элементов мультимедиа
- Библиотека проигрывателя Windows Media, получение элементов мультимедиа
- Библиотека, получение элементов мультимедиа
- Библиотека проигрывателя Windows Media, удаление элементов мультимедиа
- Библиотека, удаление элементов мультимедиа
- Добавление элементов мультимедиа в библиотеку проигрывателя Windows Media
- Извлечение элементов мультимедиа из библиотеки проигрывателя Windows Media
- Удаление элементов мультимедиа из библиотеки проигрывателя Windows Media
- получение метаданных
- Библиотека проигрывателя Windows Media, получение метаданных из элементов мультимедиа
- Библиотека, получение метаданных из элементов мультимедиа
- метаданные, извлечение
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d40e03e91b2a67a24cb49b0ac1810ceb7b9544c9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411154"
---
# <a name="accessing-the-library-programmatically"></a><span data-ttu-id="fc319-126">Программный доступ к библиотеке</span><span class="sxs-lookup"><span data-stu-id="fc319-126">Accessing the Library Programmatically</span></span>

<span data-ttu-id="fc319-127">В коде библиотека представлена объектом **медиаколлектион** (или интерфейсом **ивмпмедиаколлектион** ).</span><span class="sxs-lookup"><span data-stu-id="fc319-127">In code, the library is represented by the **MediaCollection** object (or the **IWMPMediaCollection** interface).</span></span> <span data-ttu-id="fc319-128">Элементы мультимедиа представлены как объекты **мультимедиа** (или интерфейс **ивмпмедиа** ).</span><span class="sxs-lookup"><span data-stu-id="fc319-128">Media items are represented as **Media** objects (or by the **IWMPMedia** interface).</span></span> <span data-ttu-id="fc319-129">Элементы списка воспроизведения представляются как объекты **списков воспроизведения** (или интерфейс **ивмпплайлист** ).</span><span class="sxs-lookup"><span data-stu-id="fc319-129">Playlist items are represented as **Playlist** objects (or by the **IWMPPlaylist** interface).</span></span> <span data-ttu-id="fc319-130">Для простоты этот раздел будет просто ссылаться на имена объектов, когда это возможно.</span><span class="sxs-lookup"><span data-stu-id="fc319-130">For simplicity, this section will simply refer to object names, when possible.</span></span>

<span data-ttu-id="fc319-131">С помощью объекта **медиаколлектион** можно работать с элементами мультимедиа и списками воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="fc319-131">By using the **MediaCollection** object, you can work with media items and playlists.</span></span> <span data-ttu-id="fc319-132">Библиотека также предоставляет объект **плайлистколлектион** (или интерфейс **ивмпплайлистколлектион** ), который предоставляет некоторые функциональные возможности, характерные для работы с списками воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="fc319-132">The library also exposes the **PlaylistCollection** object (or the **IWMPPlaylistCollection** interface), which provides some functionality specific to working with playlists.</span></span> <span data-ttu-id="fc319-133">В большинстве случаев объект **медиаколлектион** предоставит вам необходимые вам функции даже при работе с списками воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="fc319-133">Most of the time, the **MediaCollection** object will provide you with the functionality you need, even when working with playlists.</span></span> <span data-ttu-id="fc319-134">Дополнительные сведения о работе с элементами мультимедиа см. в разделе [Управление элементами мультимедиа](managing-media-items.md).</span><span class="sxs-lookup"><span data-stu-id="fc319-134">For more information about working with media items, see [Managing Media Items](managing-media-items.md).</span></span> <span data-ttu-id="fc319-135">Дополнительные сведения о работе с списками воспроизведения см. в разделе [Управление списками воспроизведения](managing-playlists.md).</span><span class="sxs-lookup"><span data-stu-id="fc319-135">For more information about working with playlists, see [Managing Playlists](managing-playlists.md).</span></span>

## <a name="adding-media-items-to-the-library"></a><span data-ttu-id="fc319-136">Добавление элементов мультимедиа в библиотеку</span><span class="sxs-lookup"><span data-stu-id="fc319-136">Adding Media Items to the Library</span></span>

<span data-ttu-id="fc319-137">Добавление цифрового мультимедийного содержимого в библиотеку — это просто.</span><span class="sxs-lookup"><span data-stu-id="fc319-137">Adding digital media content to the library is straightforward.</span></span> <span data-ttu-id="fc319-138">Просто вызовите метод [медиаколлектион. Add](mediacollection-add.md) , указав путь к файлу мультимедиа в качестве аргумента.</span><span class="sxs-lookup"><span data-stu-id="fc319-138">Simply call the [MediaCollection.add](mediacollection-add.md) method, providing the path to the media file as an argument.</span></span>

## <a name="retrieving-media-items-from-the-library"></a><span data-ttu-id="fc319-139">Получение элементов мультимедиа из библиотеки</span><span class="sxs-lookup"><span data-stu-id="fc319-139">Retrieving Media Items from the Library</span></span>

<span data-ttu-id="fc319-140">При извлечении элементов мультимедиа из библиотеки вы действительно получаете список воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="fc319-140">When you retrieve media items from the library, what you really retrieve is a playlist.</span></span> <span data-ttu-id="fc319-141">Даже если предполагается получение только одного элемента мультимедиа, будет получен объект **списка воспроизведения** , содержащий один элемент, который будет связан с нулевым индексом.</span><span class="sxs-lookup"><span data-stu-id="fc319-141">Even if you expect to retrieve only one media item, you will get a **Playlist** object containing a single item, which will be associated with index zero.</span></span> <span data-ttu-id="fc319-142">Например, если требуется получить объект **мультимедиа** , представляющий песню с именем «жеанне», можно использовать следующий код JScript:</span><span class="sxs-lookup"><span data-stu-id="fc319-142">For example, if you want to retrieve a **Media** object that represents the song named "Jeanne", you could use the following JScript code:</span></span>


```C++
// Retrieve media named Jeanne from the library.
var playlist = player.mediaCollection.getByName("Jeanne");

```



<span data-ttu-id="fc319-143">Приведенный выше код извлекает список воспроизведения, содержащий все элементы мультимедиа с именем «Жеанне» в качестве заголовка.</span><span class="sxs-lookup"><span data-stu-id="fc319-143">The preceding code retrieves a playlist containing all the media items having the name "Jeanne" as the title.</span></span> <span data-ttu-id="fc319-144">В этом примере предположим, что имеется только одна песня с этим именем в библиотеке (Обратите внимание, что библиотека поддерживает несколько песен, имеющих одно и то же имя).</span><span class="sxs-lookup"><span data-stu-id="fc319-144">For this example, assume that you know there is only one song by that name in the library (note that the library supports multiple songs having the same name).</span></span> <span data-ttu-id="fc319-145">Это означает, что количество элементов в списке воспроизведения, которое вы извлекли, можно считать равным одному, а элемент мультимедиа будет представлен нулевым индексом.</span><span class="sxs-lookup"><span data-stu-id="fc319-145">This means you could expect the count of items in the playlist you retrieved to equal one and the media item would be represented by index zero.</span></span> <span data-ttu-id="fc319-146">Следующий пример кода продолжит предыдущий пример, чтобы продемонстрировать, как можно извлечь элемент мультимедиа из списка воспроизведения с помощью метода renесли [. Item](playlist-item.md) .</span><span class="sxs-lookup"><span data-stu-id="fc319-146">The following example code continues the previous example to demonstrate how you would retrieve the media item from the playlist by using the [Playlist.item](playlist-item.md) method.</span></span>


```C++
// Retrieve the individual media item from the playlist.
var media = playlist.item(0);

```



<span data-ttu-id="fc319-147">Дополнительные сведения о получении элементов мультимедиа из списков воспроизведения см. в разделе [списки воспроизведения и элементы мультимедиа статьи](playlists-and-media-items.md) [Управление проигрывателем](player-control-guide.md).</span><span class="sxs-lookup"><span data-stu-id="fc319-147">For more information about retrieving media items from playlists, see [Playlists and Media Items](playlists-and-media-items.md) in the [Player Control Guide](player-control-guide.md).</span></span>

## <a name="retrieving-metadata-from-a-media-item"></a><span data-ttu-id="fc319-148">Получение метаданных из элемента мультимедиа</span><span class="sxs-lookup"><span data-stu-id="fc319-148">Retrieving Metadata from a Media Item</span></span>

<span data-ttu-id="fc319-149">После получения объекта **мультимедиа** можно считать значения атрибутов, связанные с содержимым.</span><span class="sxs-lookup"><span data-stu-id="fc319-149">After you retrieve a **Media** object, you can read the attribute values associated with the content.</span></span> <span data-ttu-id="fc319-150">В самом простом случае может быть просто известно одно значение, например имя исполнителя, выполнившего музыкальную запись. В следующем примере JScript показано, как использовать метод [Media. getItemInfo](media-getiteminfo.md) для получения имени исполнителя из носителя, полученного в предыдущем примере:</span><span class="sxs-lookup"><span data-stu-id="fc319-150">In the simplest case, you might simply want to know a single value, such as the name of the artist who performed a music track. The following JScript example shows how to use the [Media.getItemInfo](media-getiteminfo.md) method to retrieve the name of the artist from the media retrieved in the previous example:</span></span>


```C++
// Retrieve the artist name string.
var author = media.getItemInfo("Artist");

```



<span data-ttu-id="fc319-151">Элемент мультимедиа может иметь множество различных атрибутов, и работа с метаданными не всегда так проста, как простой вариант, показанный в предыдущем примере.</span><span class="sxs-lookup"><span data-stu-id="fc319-151">A media item can have many different attributes, and working with metadata is not always as straightforward as the simple case shown in the previous example.</span></span> <span data-ttu-id="fc319-152">Например, некоторые атрибуты могут содержать несколько значений или иметь значения более чем на одном языке.</span><span class="sxs-lookup"><span data-stu-id="fc319-152">For instance, some attributes can contain multiple values or have values in more than one language.</span></span> <span data-ttu-id="fc319-153">Дополнительные сведения о работе с метаданными см. в разделе [атрибуты элементов мультимедиа](media-item-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="fc319-153">For more information about working with metadata, see [Media Item Attributes](media-item-attributes.md).</span></span> <span data-ttu-id="fc319-154">Дополнительные сведения о различных атрибутах, их значениях и поддержке типов файлов см. в [справочнике по атрибутам](attribute-reference.md).</span><span class="sxs-lookup"><span data-stu-id="fc319-154">For more information about the various attributes, their meanings, and file type support, see the [Attribute Reference](attribute-reference.md).</span></span>

## <a name="removing-media-items-from-the-library"></a><span data-ttu-id="fc319-155">Удаление элементов мультимедиа из библиотеки</span><span class="sxs-lookup"><span data-stu-id="fc319-155">Removing Media Items from the Library</span></span>

<span data-ttu-id="fc319-156">Удаление мультимедийного содержимого из библиотеки также упрощается.</span><span class="sxs-lookup"><span data-stu-id="fc319-156">Removing digital media content from the library is also straightforward.</span></span> <span data-ttu-id="fc319-157">Просто вызовите **медиаколлектион. Remove**, указав объект **мультимедиа** , представляющий элемент в качестве первого аргумента, и значение **true** в качестве второго.</span><span class="sxs-lookup"><span data-stu-id="fc319-157">Simply call **MediaCollection.remove**, providing the **Media** object that represents the item as the first argument and the value **true** as the second.</span></span> <span data-ttu-id="fc319-158">В следующем примере JScript файл с именем Жеанне (полученный в предыдущем примере) удаляется из библиотеки:</span><span class="sxs-lookup"><span data-stu-id="fc319-158">The following JScript example removes the file named Jeanne (retrieved in the previous example) from the library:</span></span>


```C++
// Remove Jeanne from the library.
playst.mediaCollection.remove(media, true);

```



## <a name="related-topics"></a><span data-ttu-id="fc319-159">См. также</span><span class="sxs-lookup"><span data-stu-id="fc319-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fc319-160">**Сведения о библиотеке**</span><span class="sxs-lookup"><span data-stu-id="fc319-160">**About the Library**</span></span>](about-the-library.md)
</dt> <dt>

[<span data-ttu-id="fc319-161">**Сведения об объектах Медиаколлектион и Media**</span><span class="sxs-lookup"><span data-stu-id="fc319-161">**About the MediaCollection and Media Objects**</span></span>](about-the-mediacollection-and-media-objects.md)
</dt> <dt>

[<span data-ttu-id="fc319-162">**Сведения об объектах списков воспроизведения, Плайлистколлектион и Плайлистаррай**</span><span class="sxs-lookup"><span data-stu-id="fc319-162">**About the Playlist, PlaylistCollection, and PlaylistArray Objects**</span></span>](about-the-playlist--playlistcollection--and-playlistarray-objects.md)
</dt> <dt>

[<span data-ttu-id="fc319-163">**Работа с библиотекой**</span><span class="sxs-lookup"><span data-stu-id="fc319-163">**Working with the Library**</span></span>](working-with-the-library.md)
</dt> </dl>

 

 




