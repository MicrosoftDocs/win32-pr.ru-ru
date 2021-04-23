---
title: Списки воспроизведения и объект Медиаколлектион
description: Списки воспроизведения и объект Медиаколлектион
ms.assetid: 3c98ceed-2545-4774-998b-c1db0d172a81
keywords:
- Проигрыватель Windows Media, списки воспроизведения
- Объектная модель проигрывателя Windows Media, списки воспроизведения
- Объектная модель, списки воспроизведения
- Проигрыватель Windows Media Mobile, списки воспроизведения
- Элемент управления ActiveX проигрывателя Windows Media, списки воспроизведения
- Элемент управления ActiveX в проигрывателе Windows Media Mobile, списки воспроизведения
- Элементы управления ActiveX, списки воспроизведения
- списки воспроизведения, объект Медиаколлектион
- списки воспроизведения метафайлов, объект Медиаколлектион
- Списки воспроизведения метафайлов Windows Media, объект Медиаколлектион
- Объект Медиаколлектион
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 334b693046e6c78e92a4af901816b57bb9c4cddc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104410789"
---
# <a name="playlists-and-the-mediacollection-object"></a><span data-ttu-id="df903-114">Списки воспроизведения и объект Медиаколлектион</span><span class="sxs-lookup"><span data-stu-id="df903-114">Playlists and the MediaCollection Object</span></span>

<span data-ttu-id="df903-115">Объект **медиаколлектион** предоставляет доступ к разнообразным спискам воспроизведения и включает метод для создания нового списка воспроизведения из метафайла.</span><span class="sxs-lookup"><span data-stu-id="df903-115">The **MediaCollection** object gives you access to a variety of special playlists, and includes a method for creating a new playlist from a metafile.</span></span>

<span data-ttu-id="df903-116">Следующие методы получают специальные списки воспроизведения:</span><span class="sxs-lookup"><span data-stu-id="df903-116">The following methods retrieve special playlists:</span></span>

-   <span data-ttu-id="df903-117">**жеталл**</span><span class="sxs-lookup"><span data-stu-id="df903-117">**getAll**</span></span>
-   <span data-ttu-id="df903-118">**жетбялбум**</span><span class="sxs-lookup"><span data-stu-id="df903-118">**getByAlbum**</span></span>
-   <span data-ttu-id="df903-119">**жетбяттрибуте**</span><span class="sxs-lookup"><span data-stu-id="df903-119">**getByAttribute**</span></span>
-   <span data-ttu-id="df903-120">**жетбяусор**</span><span class="sxs-lookup"><span data-stu-id="df903-120">**getByAuthor**</span></span>
-   <span data-ttu-id="df903-121">**жетбиженре**</span><span class="sxs-lookup"><span data-stu-id="df903-121">**getByGenre**</span></span>
-   <span data-ttu-id="df903-122">**жетбинаме**</span><span class="sxs-lookup"><span data-stu-id="df903-122">**getByName**</span></span>

<span data-ttu-id="df903-123">Как следует из своих имен, эти методы извлекают списки воспроизведения, содержащие все элементы мультимедиа в библиотеке, соответствующие определенным критериям.</span><span class="sxs-lookup"><span data-stu-id="df903-123">As their names suggest, these methods retrieve playlists containing all of the media items in the library that match certain criteria.</span></span>

<span data-ttu-id="df903-124">Будьте внимательны, чтобы не путать *медиаколлектион*. метод **жетбинаме** с параметром *плайлистколлектион*. метод **жетбинаме** .</span><span class="sxs-lookup"><span data-stu-id="df903-124">Be careful not to confuse the *MediaCollection*.**getByName** method with the *PlaylistCollection*.**getByName** method.</span></span> <span data-ttu-id="df903-125">Метод **медиаколлектион** возвращает объект **списка воспроизведения** , содержащий все элементы мультимедиа с указанным именем.</span><span class="sxs-lookup"><span data-stu-id="df903-125">The **MediaCollection** method returns a **Playlist** object containing all of the media items that have the specified name.</span></span> <span data-ttu-id="df903-126">Метод **плайлистколлектион** возвращает объект **плайлистаррай** , содержащий все списки воспроизведения с указанным именем.</span><span class="sxs-lookup"><span data-stu-id="df903-126">The **PlaylistCollection** method returns a **PlaylistArray** object containing all of the playlists that have the specified name.</span></span>

<span data-ttu-id="df903-127">Можно использовать *медиаколлектион*. **добавьте** метод для добавления списков воспроизведения, а также элементов мультимедиа в библиотеку.</span><span class="sxs-lookup"><span data-stu-id="df903-127">You can use the *MediaCollection*.**add** method to add playlists as well as media items to the library.</span></span> <span data-ttu-id="df903-128">Чтобы добавить список воспроизведения, необходимо передать методу путь к метафайлу, который определяет список воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="df903-128">To add a playlist, you pass the method the path to the metafile that defines the playlist.</span></span> <span data-ttu-id="df903-129">Метод всегда возвращает объект **мультимедиа** .</span><span class="sxs-lookup"><span data-stu-id="df903-129">The method always returns a **Media** object.</span></span> <span data-ttu-id="df903-130">Невозможно выполнить приведение между объектами **мультимедиа** и **списками воспроизведения** .</span><span class="sxs-lookup"><span data-stu-id="df903-130">You cannot cast between **Media** and **Playlist** objects.</span></span> <span data-ttu-id="df903-131">Для работы с добавленным списком воспроизведения извлеките объект **списка воспроизведения** , имя которого совпадает с именем объекта **мультимедиа** .</span><span class="sxs-lookup"><span data-stu-id="df903-131">To work with the playlist that you added, retrieve the **Playlist** object that has the same name as the **Media** object.</span></span>

<span data-ttu-id="df903-132">В следующем примере C# показано, как получить мультимедиа по типу с помощью **медиаколлектион**. метод **жетбяттрибуте** .</span><span class="sxs-lookup"><span data-stu-id="df903-132">The following C# example demonstrates how to retrieve media by type using the **MediaCollection**.**getByAttribute** method.</span></span> <span data-ttu-id="df903-133">Этот код извлекает имена всех атрибутов, связанных с данным типом, а также состояние этих атрибутов для чтения и записи или только для чтения.</span><span class="sxs-lookup"><span data-stu-id="df903-133">This code retrieves the names of all attributes associated with a given type as well as the read/write or read-only status of those attributes.</span></span> <span data-ttu-id="df903-134">Он создает один файл, содержащий списки атрибутов для аудио, видео, Радио, списков воспроизведения, других, музыкальных и фотографий.</span><span class="sxs-lookup"><span data-stu-id="df903-134">It generates a single file that contains lists of attributes for the Audio, Video, Radio, Playlist, Other, Music, and Photo types.</span></span>


```C++
string strOutFile = "AttribList.txt";    // Name of the output file
...
StreamWriter sw = new StreamWriter(strOutFile, true);

sw.Write(getMediaCollectionNames("Audio"));
sw.Write(getMediaCollectionNames("Video"));
sw.Write(getMediaCollectionNames("Radio"));
sw.Write(getMediaCollectionNames("Playlist"));
sw.Write(getMediaCollectionNames("Other"));
sw.Write(getMediaCollectionNames("Music"));
sw.Write(getMediaCollectionNames("Photo"));
sw.Close();
...
// The getMediaCollection method retrieves the names of
// all attributes for a specified type.
private string getMediaCollectionNames(string sSchema)
{
IWMPPlaylist playlist;
IWMPMedia media;
string strResult = "";    // Cumulative list of attributes
string strAttrName = "";  // Attribute name
string strReadWrite = ""; // Read/Write status of attribute
int iAttrCount = 0;       // Count of playlist attributes

// Retrieve a playlist corresponding to the requested type.
playlist = Player.mediaCollection.getByAttribute("MediaType", sSchema);

// Initialize the result string
strResult += "\n" + sSchema.ToString() + " Schema: \n";

// Retrieve the attributes for the playlist
if (playlist.count != 0)
{
    media = playlist.get_Item(0);
    iAttrCount = media.attributeCount;
    for (int i = 0; i < iAttrCount; i++)
    {
        strAttrName = media.getAttributeName(i);
        strResult += "   " + strAttrName  +"\n";
        if (media.isReadOnlyItem(strAttrName))
            strReadWrite = "Read Only";
        else
            strReadWrite = "Read/Write";
        strResult += "         " + strReadWrite + "\n";
    }
}

return strResult;
}

```



<span data-ttu-id="df903-135">В следующем примере кода C# показано, как добавить список воспроизведения из метафайла в библиотеку.</span><span class="sxs-lookup"><span data-stu-id="df903-135">The following C# example demonstrates how to add a playlist from a metafile to the library.</span></span>


```C++
// Add a playlist as a media item
IWMPMedia Media = Player.mediaCollection.add("c:\\testPlayList.asx");

```



<span data-ttu-id="df903-136">К статическим спискам воспроизведения относятся определенные элементы мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="df903-136">Static playlists include specific media items.</span></span> <span data-ttu-id="df903-137">Автоматические списки воспроизведения выполняют поиск в библиотеке при каждом открытии и могут содержать разные элементы мультимедиа в разные моменты времени.</span><span class="sxs-lookup"><span data-stu-id="df903-137">Auto playlists search the library every time they are opened and may contain different media items at different times.</span></span> <span data-ttu-id="df903-138">В библиотеку можно добавить как статические, так и автоматические списки воспроизведения с помощью *медиаколлектион*. **добавьте** метод.</span><span class="sxs-lookup"><span data-stu-id="df903-138">You can add both static and auto playlists to the library by using the *MediaCollection*.**add** method.</span></span> <span data-ttu-id="df903-139">Также можно добавить статические списки воспроизведения с помощью *плайлистколлектион*. метод **импортплайлист** .</span><span class="sxs-lookup"><span data-stu-id="df903-139">You can also add static playlists by using the *PlaylistCollection*.**importPlaylist** method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="df903-140">См. также</span><span class="sxs-lookup"><span data-stu-id="df903-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="df903-141">**Управление списками воспроизведения**</span><span class="sxs-lookup"><span data-stu-id="df903-141">**Managing Playlists**</span></span>](managing-playlists.md)
</dt> <dt>

[<span data-ttu-id="df903-142">**Объект Медиаколлектион**</span><span class="sxs-lookup"><span data-stu-id="df903-142">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="df903-143">**Объект списка воспроизведения**</span><span class="sxs-lookup"><span data-stu-id="df903-143">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="df903-144">**Объект Плайлистколлектион**</span><span class="sxs-lookup"><span data-stu-id="df903-144">**PlaylistCollection Object**</span></span>](playlistcollection-object.md)
</dt> <dt>

[<span data-ttu-id="df903-145">**Списки воспроизведения и объект Плайлистколлектион**</span><span class="sxs-lookup"><span data-stu-id="df903-145">**Playlists and the PlaylistCollection Object**</span></span>](playlists-and-the-playlistcollection-object.md)
</dt> <dt>

[<span data-ttu-id="df903-146">**Статические и автоматические списки воспроизведения**</span><span class="sxs-lookup"><span data-stu-id="df903-146">**Static and Auto Playlists**</span></span>](static-and-auto-playlists.md)
</dt> </dl>

 

 




