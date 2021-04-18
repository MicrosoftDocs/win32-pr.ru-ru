---
title: Списки воспроизведения и объект Плайлистколлектион
description: Списки воспроизведения и объект Плайлистколлектион
ms.assetid: 63c8955b-34ad-447b-b734-657207bcecbb
keywords:
- Проигрыватель Windows Media, списки воспроизведения
- Объектная модель проигрывателя Windows Media, списки воспроизведения
- Объектная модель, списки воспроизведения
- Проигрыватель Windows Media Mobile, списки воспроизведения
- Элемент управления ActiveX проигрывателя Windows Media, списки воспроизведения
- Элемент управления ActiveX в проигрывателе Windows Media Mobile, списки воспроизведения
- Элементы управления ActiveX, списки воспроизведения
- списки воспроизведения, объект Плайлистколлектион
- списки воспроизведения метафайлов, объект Плайлистколлектион
- Списки воспроизведения метафайлов Windows Media, объект Плайлистколлектион
- Объект Плайлистколлектион
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98744c2c5b97129db2824c42567802a374f90b6c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105700521"
---
# <a name="playlists-and-the-playlistcollection-object"></a><span data-ttu-id="16993-114">Списки воспроизведения и объект Плайлистколлектион</span><span class="sxs-lookup"><span data-stu-id="16993-114">Playlists and the PlaylistCollection Object</span></span>

<span data-ttu-id="16993-115">Объект **плайлистколлектион** предоставляет доступ к спискам воспроизведения в библиотеке и содержит методы для создания новых, пустых списков воспроизведения и новых списков воспроизведения из метафайлов.</span><span class="sxs-lookup"><span data-stu-id="16993-115">The **PlaylistCollection** object gives you access to playlists in the library and has methods for creating new, empty playlists and new playlists from metafiles.</span></span>

## <a name="working-with-existing-playlists"></a><span data-ttu-id="16993-116">Работа с существующими списками воспроизведения</span><span class="sxs-lookup"><span data-stu-id="16993-116">Working with Existing Playlists</span></span>

<span data-ttu-id="16993-117">*Плайлистколлектион*. **жеталл** и *плайлистколлектион*. методы **жетбинаме** возвращают объект **плайлистаррай** , который может содержать несколько списков воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="16993-117">The *PlaylistCollection*.**getAll** and *PlaylistCollection*.**getByName** methods each return a **PlaylistArray** object, which can contain multiple playlists.</span></span>

<span data-ttu-id="16993-118">*Плайлистколлектион*. метод **жеталл** возвращает все существующие списки воспроизведения, которые находятся в библиотеке.</span><span class="sxs-lookup"><span data-stu-id="16993-118">The *PlaylistCollection*.**getAll** method returns all of the existing playlists that are in the library.</span></span> <span data-ttu-id="16993-119">Например, можно вызвать этот метод, а затем извлечь списки воспроизведения в объекте **плайлистаррай** , чтобы определить, используется ли уже данное имя списка воспроизведения, или отобразить все списки воспроизведения для пользователя.</span><span class="sxs-lookup"><span data-stu-id="16993-119">For example, you can call this method and then retrieve the playlists in the **PlaylistArray** object to determine whether a given playlist name has already been used, or to display all of the playlists to the user.</span></span> <span data-ttu-id="16993-120">Пример кода в [атрибутах списка воспроизведения](playlist-attributes.md) использует метод **жеталл** .</span><span class="sxs-lookup"><span data-stu-id="16993-120">The sample code in [Playlist Attributes](playlist-attributes.md) uses the **getAll** method.</span></span>

<span data-ttu-id="16993-121">*Плайлистколлектион*. метод **жетбинаме** возвращает все списки воспроизведения с заданным именем.</span><span class="sxs-lookup"><span data-stu-id="16993-121">The *PlaylistCollection*.**getByName** method returns all of the playlists with a given name.</span></span> <span data-ttu-id="16993-122">Этот метод можно использовать для каждого из этих списков воспроизведения отдельно.</span><span class="sxs-lookup"><span data-stu-id="16993-122">You can use this method to handle each of those playlists separately.</span></span>

<span data-ttu-id="16993-123">Можно также использовать метод **жетбинаме** для получения уникального списка воспроизведения по имени.</span><span class="sxs-lookup"><span data-stu-id="16993-123">You can also use the **getByName** method to retrieve a unique playlist by name.</span></span> <span data-ttu-id="16993-124">В этом случае объект **плайлистаррай** содержит только один элемент.</span><span class="sxs-lookup"><span data-stu-id="16993-124">In that case, the **PlaylistArray** object has only one element.</span></span> <span data-ttu-id="16993-125">Этот метод показан в следующем примере C#.</span><span class="sxs-lookup"><span data-stu-id="16993-125">The following C# example demonstrates this technique.</span></span>


```C++
IWMPPlaylistArray PlayListArray;
IWMPPlaylist Playlist;
// Store the playlist named "BluesTest" in the array
PlayListArray = Player.playlistCollection.getByName("BluesTest");
// Retrieve the first playlist in the collection.
Playlist = PlaylistArray.Item(0);

```



## <a name="working-with-new-playlists"></a><span data-ttu-id="16993-126">Работа с новыми списками воспроизведения</span><span class="sxs-lookup"><span data-stu-id="16993-126">Working with New Playlists</span></span>

<span data-ttu-id="16993-127">Можно использовать *плайлистколлектион*. метод **невплайлист** для создания нового пустого списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="16993-127">You can use the *PlaylistCollection*.**newPlaylist** method to create a new, empty playlist.</span></span> <span data-ttu-id="16993-128">Метод возвращает ссылку на новый объект **списка воспроизведения** .</span><span class="sxs-lookup"><span data-stu-id="16993-128">The method returns a reference to the new **Playlist** object.</span></span> <span data-ttu-id="16993-129">Затем можно вызвать *список воспроизведения*. метод **аппендитем** для добавления элементов мультимедиа в список воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="16993-129">You can then call the *Playlist*.**appendItem** method to add media items to the playlist.</span></span>

<span data-ttu-id="16993-130">Можно также создать новый список воспроизведения на основе метафайла списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="16993-130">You can also create a new playlist based on a playlist metafile.</span></span> <span data-ttu-id="16993-131">Сначала передайте имя списка воспроизведения и путь к метафайлу *проигрывателю*. метод **невплайлист** .</span><span class="sxs-lookup"><span data-stu-id="16993-131">First, pass the name of the playlist and the path to the metafile to the *Player*.**newPlaylist** method.</span></span> <span data-ttu-id="16993-132">Этот метод возвращает ссылку на новый объект **списка воспроизведения** .</span><span class="sxs-lookup"><span data-stu-id="16993-132">That method returns a reference to the new **Playlist** object.</span></span> <span data-ttu-id="16993-133">Затем передайте новый объект **списка воспроизведения** в *плайлистколлектион*. метод **импортплайлист** , чтобы добавить его в библиотеку.</span><span class="sxs-lookup"><span data-stu-id="16993-133">Then, pass the new **Playlist** object to the *PlaylistCollection*.**importPlaylist** method to add it to the library.</span></span>

<span data-ttu-id="16993-134">Обратите внимание на разницу между *плайлистколлектион*. метод **невплайлист** и *проигрыватель*. метод **невплайлист** .</span><span class="sxs-lookup"><span data-stu-id="16993-134">Notice the difference between the *PlaylistCollection*.**newPlaylist** method and the *Player*.**newPlaylist** method.</span></span> <span data-ttu-id="16993-135">Метод **плайлистколлектион** создает новый пустой список воспроизведения и добавляет его в библиотеку.</span><span class="sxs-lookup"><span data-stu-id="16993-135">The **PlaylistCollection** method creates a new, empty playlist and adds it to the library.</span></span> <span data-ttu-id="16993-136">Метод **Player** создает новый, заполненный объект **списка воспроизведения** , но не добавляет его в библиотеку.</span><span class="sxs-lookup"><span data-stu-id="16993-136">The **Player** method creates a new, populated **Playlist** object but does not add it to the library.</span></span>

<span data-ttu-id="16993-137">В этом разделе объект **Player** был определен следующим образом:</span><span class="sxs-lookup"><span data-stu-id="16993-137">Throughout this topic, the **Player** object was defined in the following manner:</span></span>


```C++
AxWMPLib.AxWindowsMediaPlayer Player;
using WMPLib;

```



<span data-ttu-id="16993-138">В следующем примере кода C# демонстрируется импорт списка воспроизведения из метафайла.</span><span class="sxs-lookup"><span data-stu-id="16993-138">The following C# example demonstrates importing a playlist from a metafile.</span></span> <span data-ttu-id="16993-139">Аргумент *стрплистнаме* указывает имя нового списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="16993-139">The *strPListName* argument specifies the name of the new playlist.</span></span> <span data-ttu-id="16993-140">*Стрметафиленаме* указывает имя метафайла, из которого импортируется список воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="16993-140">The *strMetaFileName* specifies the name of the metafile from which the playlist is imported.</span></span>


```C++
private IWMPPlaylist importPlaylist(string strPlaylistName, string strMetaFileName)
{
    IWMPPlaylist  NewPlaylist;
    IWMPPlaylist  ImportPlaylist;

    NewPlaylist = Player.newPlaylist(strPlaylistName, strMetaFileName);
    ImportPlaylist = Player.playlistCollection.importPlaylist(NewPlaylist);

    return ImportPlaylist;
}

```



## <a name="related-topics"></a><span data-ttu-id="16993-141">См. также</span><span class="sxs-lookup"><span data-stu-id="16993-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="16993-142">**Управление списками воспроизведения**</span><span class="sxs-lookup"><span data-stu-id="16993-142">**Managing Playlists**</span></span>](managing-playlists.md)
</dt> <dt>

[<span data-ttu-id="16993-143">**Player. Невплайлист**</span><span class="sxs-lookup"><span data-stu-id="16993-143">**Player.newPlaylist**</span></span>](player-newplaylist.md)
</dt> <dt>

[<span data-ttu-id="16993-144">**Список воспроизведения. Аппендитем**</span><span class="sxs-lookup"><span data-stu-id="16993-144">**Playlist.appendItem**</span></span>](playlist-appenditem.md)
</dt> <dt>

[<span data-ttu-id="16993-145">**Объект Плайлистаррай**</span><span class="sxs-lookup"><span data-stu-id="16993-145">**PlaylistArray Object**</span></span>](playlistarray-object.md)
</dt> <dt>

[<span data-ttu-id="16993-146">**Объект Плайлистколлектион**</span><span class="sxs-lookup"><span data-stu-id="16993-146">**PlaylistCollection Object**</span></span>](playlistcollection-object.md)
</dt> <dt>

[<span data-ttu-id="16993-147">**Списки воспроизведения и элементы мультимедиа**</span><span class="sxs-lookup"><span data-stu-id="16993-147">**Playlists and Media Items**</span></span>](playlists-and-media-items.md)
</dt> </dl>

 

 




