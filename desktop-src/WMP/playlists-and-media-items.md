---
title: Списки воспроизведения и элементы мультимедиа
description: Списки воспроизведения и элементы мультимедиа
ms.assetid: 281c744d-380e-4200-8585-a3f378bc1c36
keywords:
- Проигрыватель Windows Media, списки воспроизведения
- Объектная модель проигрывателя Windows Media, списки воспроизведения
- Объектная модель, списки воспроизведения
- Проигрыватель Windows Media Mobile, списки воспроизведения
- Элемент управления ActiveX проигрывателя Windows Media, списки воспроизведения
- Элемент управления ActiveX в проигрывателе Windows Media Mobile, списки воспроизведения
- Элементы управления ActiveX, списки воспроизведения
- списки воспроизведения, элементы мультимедиа
- списки воспроизведения метафайлов, элементы мультимедиа
- Списки воспроизведения метафайлов Windows Media, элементы мультимедиа
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4716a8ce07e7b0ec8348ce1a6981e23291335e7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986331"
---
# <a name="playlists-and-media-items"></a><span data-ttu-id="10b2b-113">Списки воспроизведения и элементы мультимедиа</span><span class="sxs-lookup"><span data-stu-id="10b2b-113">Playlists and Media Items</span></span>

<span data-ttu-id="10b2b-114">Список воспроизведения — это набор элементов мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="10b2b-114">A playlist is a set of media items.</span></span> <span data-ttu-id="10b2b-115">Объект **списка воспроизведения** может управлять объектами **мультимедиа** , представляющими эти элементы.</span><span class="sxs-lookup"><span data-stu-id="10b2b-115">A **Playlist** object can manipulate the **Media** objects that represent those items.</span></span>

## <a name="retrieving-media-items"></a><span data-ttu-id="10b2b-116">Получение элементов мультимедиа</span><span class="sxs-lookup"><span data-stu-id="10b2b-116">Retrieving Media Items</span></span>

<span data-ttu-id="10b2b-117">Для существующего списка воспроизведения можно прочитать *список воспроизведения*. **Count** свойство, чтобы определить, сколько элементов мультимедиа находится в списке воспроизведения, и вы можете получить ссылку на объект **мультимедиа** , соответствующий определенному элементу, с помощью *списка воспроизведения*. Свойство **элемента** .</span><span class="sxs-lookup"><span data-stu-id="10b2b-117">For an existing playlist, you can read the *Playlist*.**count** property to determine how many media items are in the playlist, and you can get a reference to the **Media** object corresponding to a specific item using the *Playlist*.**item** property.</span></span>

<span data-ttu-id="10b2b-118">Следующий пример на C# извлекает ссылку на объект для определенного элемента мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="10b2b-118">The following C# example retrieves an object reference to a specific media item.</span></span> <span data-ttu-id="10b2b-119">(В этом разделе переменная *pList* является ссылкой на объект **списка воспроизведения** .)</span><span class="sxs-lookup"><span data-stu-id="10b2b-119">(Throughout this topic, the variable *pList* is a reference to a **Playlist** object.)</span></span>


```C++
currMedia = pList.Item(0);

```



<span data-ttu-id="10b2b-120">Следующий пример на C# извлекает имена всех элементов мультимедиа в списке воспроизведения и помещает их в ListBox с именем Лстаутпут.</span><span class="sxs-lookup"><span data-stu-id="10b2b-120">The following C# example retrieves the names of all the media items in a playlist and puts them in a ListBox named lstOutput.</span></span>


```C++
for (j=0; j < pList.count; j++)
{
    strItemName = pList.get_Item(j).name;
    lstOutput.Items.Add(strItemName);
}

```



## <a name="adding-items-to-a-playlist"></a><span data-ttu-id="10b2b-121">Добавление элементов в список воспроизведения</span><span class="sxs-lookup"><span data-stu-id="10b2b-121">Adding Items to a Playlist</span></span>

<span data-ttu-id="10b2b-122">Элемент мультимедиа можно добавить в конец списка воспроизведения или в заданную позицию в списке воспроизведения с помощью *списка воспроизведения*. **аппендитем** и *список воспроизведения*. методы **insertItem** .</span><span class="sxs-lookup"><span data-stu-id="10b2b-122">You can add a media item to the end of a playlist or at a specific position in a playlist, using the *Playlist*.**appendItem** and *Playlist*.**insertItem** methods.</span></span>

<span data-ttu-id="10b2b-123">В этом разделе объект **Player** был определен следующим образом:</span><span class="sxs-lookup"><span data-stu-id="10b2b-123">Throughout this topic, the **Player** object was defined in the following manner:</span></span>


```C++
AxWMPLib.AxWindowsMediaPlayer Player;
using WMPLib;

```



<span data-ttu-id="10b2b-124">В следующем примере C# показаны обе методики, добавляя текущий элемент мультимедиа в список воспроизведения с именем «Блуестест», сначала в конце, а затем в начале списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="10b2b-124">The following C# example demonstrates both techniques by adding the current media item to a playlist named "BluesTest", first at the end and then at the beginning of the playlist.</span></span>


```C++
IWMPPlaylistCollection pListColl;
IWMPPlaylistArray pListArray;
IWMPPlaylist pList;

// Initialize the Media object
IWMPMedia currMedia = Player.currentMedia;

if(currMedia != null)
{
    // Retrieve the playlist collection
    pListColl = Player.playlistCollection;

    // Retrieve a playlist array containing
    // playlists named BluesTest
    pListArray = pListColl.getByName("BluesTest");

    // Retrieve the first element with this name from the
    // array.
    pList = pListArray.Item(0);

    // Add the current item to the end, and then, the beginning
    // of the specified playlist.
    pList.appendItem(currMedia);
    pList.insertItem(0, currMedia);
}

```



<span data-ttu-id="10b2b-125">При создании нового пустого списка воспроизведения с помощью *плайлистколлектион*. метод **невплайлист** . к нему можно добавить элементы мультимедиа путем повторного вызова *списка воспроизведения*. метод **аппендитем** .</span><span class="sxs-lookup"><span data-stu-id="10b2b-125">When you create a new, empty playlist by using the *PlaylistCollection*.**newPlaylist** method, you can add media items to it by repeatedly calling the *Playlist*.**appendItem** method.</span></span>

## <a name="manipulating-media-items-in-a-playlist"></a><span data-ttu-id="10b2b-126">Управление элементами мультимедиа в списке воспроизведения</span><span class="sxs-lookup"><span data-stu-id="10b2b-126">Manipulating Media Items in a Playlist</span></span>

<span data-ttu-id="10b2b-127">Вы можете изменить расположение элемента мультимедиа в списке воспроизведения с помощью *списка воспроизведения*. метод **мовеитем** .</span><span class="sxs-lookup"><span data-stu-id="10b2b-127">You can change the position of a media item in the playlist by using the *Playlist*.**moveItem** method.</span></span> <span data-ttu-id="10b2b-128">Вы указываете элемент по его текущему индексу, а затем указываете новый индекс.</span><span class="sxs-lookup"><span data-stu-id="10b2b-128">You specify the item by its current index, and then you specify the new index.</span></span> <span data-ttu-id="10b2b-129">В следующем примере C# элемент с индекса 5 перемещается в индекс 0 в списке воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="10b2b-129">The following C# example moves an item from index 5 to index 0 within a playlist.</span></span>


```C++
// Move the 6th item to the beginning
// of the specified playlist.
pList.moveItem(5, 0);

```



<span data-ttu-id="10b2b-130">Вы можете удалить элемент мультимедиа из списка воспроизведения с помощью **списка воспроизведения**. метод **RemoveItem** .</span><span class="sxs-lookup"><span data-stu-id="10b2b-130">You can remove a media item from the playlist by using the **Playlist**.**removeItem** method.</span></span> <span data-ttu-id="10b2b-131">Обратите внимание, что если удаленный элемент не был последним в списке воспроизведения, значения индекса последующих элементов изменяются.</span><span class="sxs-lookup"><span data-stu-id="10b2b-131">Note that if the removed item was not the final item in the playlist, the index values of the subsequent items change.</span></span> <span data-ttu-id="10b2b-132">В следующем примере C# удаляется указанный элемент.</span><span class="sxs-lookup"><span data-stu-id="10b2b-132">The following C# example removes the specified item.</span></span>


```C++
// Remove the currently playing item from the
// specified playlist.
pList.removeItem(currMedia);

```



> [!Note]  
> <span data-ttu-id="10b2b-133">Пользователи могут изменять содержимое списка воспроизведения за пределами приложения.</span><span class="sxs-lookup"><span data-stu-id="10b2b-133">Users can change the contents of a playlist outside of your application.</span></span> <span data-ttu-id="10b2b-134">Каждый раз, когда вы управляете элементами списка воспроизведения, следует отслеживать и обрабатывать связанные с списками воспроизведения события элемента управления проигрывателя Windows Media, чтобы обеспечить правильную работу кода.</span><span class="sxs-lookup"><span data-stu-id="10b2b-134">Whenever you manipulate the items in a playlist, you should monitor and handle the playlist-related events of the Windows Media Player control to ensure that your code works correctly.</span></span> <span data-ttu-id="10b2b-135">Эти события являются *проигрывателем*. **Куррентплайлистчанже** и *Player*. **Плайлистчанже**.</span><span class="sxs-lookup"><span data-stu-id="10b2b-135">These events are *Player*.**CurrentPlaylistChange** and *Player*.**PlaylistChange**.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="10b2b-136">См. также</span><span class="sxs-lookup"><span data-stu-id="10b2b-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="10b2b-137">**Управление списками воспроизведения**</span><span class="sxs-lookup"><span data-stu-id="10b2b-137">**Managing Playlists**</span></span>](managing-playlists.md)
</dt> <dt>

[<span data-ttu-id="10b2b-138">**Объект мультимедиа**</span><span class="sxs-lookup"><span data-stu-id="10b2b-138">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="10b2b-139">**Объект списка воспроизведения**</span><span class="sxs-lookup"><span data-stu-id="10b2b-139">**Playlist Object**</span></span>](playlist-object.md)
</dt> </dl>

 

 




