---
title: Статические и автоматические списки воспроизведения
description: Статические и автоматические списки воспроизведения
ms.assetid: 708c236e-8f3c-4188-aefb-eda7da598944
keywords:
- Проигрыватель Windows Media, списки воспроизведения
- Объектная модель проигрывателя Windows Media, списки воспроизведения
- Объектная модель, списки воспроизведения
- Проигрыватель Windows Media Mobile, списки воспроизведения
- Элемент управления ActiveX проигрывателя Windows Media, списки воспроизведения
- Элемент управления ActiveX в проигрывателе Windows Media Mobile, списки воспроизведения
- Элементы управления ActiveX, списки воспроизведения
- списки воспроизведения, статические
- списки воспроизведения метафайлов, статический
- Списки воспроизведения метафайлов Windows Media, статические
- Статические списки воспроизведения
- автоматические списки воспроизведения
- списки воспроизведения, авто
- списки воспроизведения метафайлов, авто
- Списки воспроизведения метафайлов Windows Media, авто
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 083ee2029eec2cfee7510766790f4ca7eb6468e5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104410695"
---
# <a name="static-and-auto-playlists"></a><span data-ttu-id="f92e3-118">Статические и автоматические списки воспроизведения</span><span class="sxs-lookup"><span data-stu-id="f92e3-118">Static and Auto Playlists</span></span>

<span data-ttu-id="f92e3-119">Существует два типа списков воспроизведения:</span><span class="sxs-lookup"><span data-stu-id="f92e3-119">There are two types of playlists:</span></span>

-   <span data-ttu-id="f92e3-120">Статические списки воспроизведения, включающие определенные элементы мультимедиа</span><span class="sxs-lookup"><span data-stu-id="f92e3-120">Static playlists, which include specific media items</span></span>
-   <span data-ttu-id="f92e3-121">Автоматические списки воспроизведения, которые выполняют поиск в библиотеке при каждом открытии и могут содержать разные элементы мультимедиа в разные моменты времени.</span><span class="sxs-lookup"><span data-stu-id="f92e3-121">Auto playlists, which search the library every time they are opened and may contain different media items at different times.</span></span> <span data-ttu-id="f92e3-122">Автоматический список воспроизведения является результатом запроса к базе данных.</span><span class="sxs-lookup"><span data-stu-id="f92e3-122">An auto playlist is the result of a database query.</span></span>

<span data-ttu-id="f92e3-123">Чтобы импортировать статический список воспроизведения из метафайла, сначала вызовите метод *Player*. **невплайлист** создать объект **списка воспроизведения** на основе данных в метафайле, а затем передать этот объект в *плайлистколлектион*. **импортплайлист** , чтобы добавить список воспроизведения в библиотеку.</span><span class="sxs-lookup"><span data-stu-id="f92e3-123">To import a static playlist from a metafile, first call *Player*.**newPlaylist** to create a **Playlist** object based on the data in the metafile, and then pass that object to *PlaylistCollection*.**importPlaylist** to add the playlist to the library.</span></span>

<span data-ttu-id="f92e3-124">Чтобы импортировать автоматический список воспроизведения из метафайла, используйте *медиаколлектион*. **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="f92e3-124">To import an auto playlist from a metafile, use *MediaCollection*.**add**.</span></span> <span data-ttu-id="f92e3-125">Дополнительные сведения см. [в разделе Списки воспроизведения и объект медиаколлектион](playlists-and-the-mediacollection-object.md).</span><span class="sxs-lookup"><span data-stu-id="f92e3-125">For more information, see [Playlists and the MediaCollection Object](playlists-and-the-mediacollection-object.md).</span></span>

<span data-ttu-id="f92e3-126">Чтобы импортировать статический список воспроизведения из метафайла автоматического списка воспроизведения, используйте *проигрыватель*. **невплайлист** и *плайлистколлектион*. **импортплайлист** , как описано выше.</span><span class="sxs-lookup"><span data-stu-id="f92e3-126">To import a static playlist from an auto playlist metafile, use *Player*.**newPlaylist** and *PlaylistCollection*.**importPlaylist** as described earlier.</span></span> <span data-ttu-id="f92e3-127">Автоматический список воспроизведения будет выполняться один раз, и в зависимости от результата выполнения будет создан статический список воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="f92e3-127">The auto playlist will be executed once and a static playlist will be created based on the result of that execution.</span></span>

<span data-ttu-id="f92e3-128">Использование автоматического списка воспроизведения для запроса библиотеки пользователя не поддерживается для веб-страниц, к которым пользователи обращаются через Интернет.</span><span class="sxs-lookup"><span data-stu-id="f92e3-128">Using an auto playlist to query the user's library is not supported for webpages that users access over the Internet.</span></span>

<span data-ttu-id="f92e3-129">В следующем примере кода C# демонстрируется импорт метафайла автоматического списка воспроизведения в виде статического списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="f92e3-129">The following C# example code demonstrates importing an auto playlist metafile as a static playlist.</span></span> <span data-ttu-id="f92e3-130">Чтобы запустить этот пример, создайте автоматический список воспроизведения с помощью пользовательского интерфейса библиотеки, а затем включите в этот код правильный путь к метафайлу автоматического списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="f92e3-130">To run this sample, create an auto playlist by using the library user interface, and then include the correct path to the auto playlist metafile in this code.</span></span>


```C++
private void addStaticPlaylist()
{
    IWMPPlaylist pList;

    pList = Player.newPlaylist("NewImportedList", "\\\\myServer\\myPath\\artistcollection.wpl");
    if (pList.count == 0)
        MessageBox.Show("The specified playlist is empty.");
    else
        Player.playlistCollection.importPlaylist(pList);
}

```



## <a name="related-topics"></a><span data-ttu-id="f92e3-131">См. также</span><span class="sxs-lookup"><span data-stu-id="f92e3-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f92e3-132">**Управление списками воспроизведения**</span><span class="sxs-lookup"><span data-stu-id="f92e3-132">**Managing Playlists**</span></span>](managing-playlists.md)
</dt> </dl>

 

 




