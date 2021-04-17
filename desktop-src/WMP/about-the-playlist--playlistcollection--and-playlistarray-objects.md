---
title: Сведения об объектах списков воспроизведения, Плайлистколлектион и Плайлистаррай
description: Сведения об объектах списков воспроизведения, Плайлистколлектион и Плайлистаррай
ms.assetid: 19867944-c836-4b7e-ada3-f696905e6327
keywords:
- Проигрыватель Windows Media, объект списка воспроизведения
- Объектная модель проигрывателя Windows Media, объект списка воспроизведения
- Объектная модель, объект списка воспроизведения
- Элемент управления ActiveX проигрывателя Windows Media, объект списка воспроизведения
- Элемент управления ActiveX, объект списка воспроизведения
- Элемент управления мобильными устройствами ActiveX проигрывателя Windows Media, объект списка воспроизведения
- Проигрыватель Windows Media Mobile, объект списка воспроизведения
- Объект списка воспроизведения
- Проигрыватель Windows Media, объект Плайлистколлектион
- Объектная модель проигрывателя Windows Media, объект Плайлистколлектион
- Объектная модель, объект Плайлистколлектион
- Элемент управления ActiveX проигрывателя Windows Media, объект Плайлистколлектион
- Элемент управления ActiveX, объект Плайлистколлектион
- Элемент управления мобильными устройствами ActiveX проигрывателя Windows Media, объект Плайлистколлектион
- Проигрыватель Windows Media Mobile, объект Плайлистколлектион
- Объект Плайлистколлектион
- Проигрыватель Windows Media, объект Плайлистаррай
- Объектная модель проигрывателя Windows Media, объект Плайлистаррай
- Объектная модель, объект Плайлистаррай
- Элемент управления ActiveX проигрывателя Windows Media, объект Плайлистаррай
- Элемент управления ActiveX, объект Плайлистаррай
- Элемент управления мобильными устройствами ActiveX проигрывателя Windows Media, объект Плайлистаррай
- Проигрыватель Windows Media Mobile, объект Плайлистаррай
- Объект Плайлистаррай
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ee9d24f4f5decc28a369e44910990ff41b99e9e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105691222"
---
# <a name="about-the-playlist-playlistcollection-and-playlistarray-objects"></a><span data-ttu-id="0cb4d-127">Сведения об объектах списков воспроизведения, Плайлистколлектион и Плайлистаррай</span><span class="sxs-lookup"><span data-stu-id="0cb4d-127">About the Playlist, PlaylistCollection, and PlaylistArray Objects</span></span>

<span data-ttu-id="0cb4d-128">Объекты **списков воспроизведения**, **плайлистколлектион** и **плайлистаррай** управляют списками воспроизведения, которые проигрыватель Windows Media может использовать для указания порядка, в котором будет воспроизводиться содержимое.</span><span class="sxs-lookup"><span data-stu-id="0cb4d-128">The **Playlist**, **PlaylistCollection**, and **PlaylistArray** objects govern the playlists that Windows Media Player can use to specify the order in which content will be played.</span></span> <span data-ttu-id="0cb4d-129">Вы получаете объект **плайлистколлектион** из свойства **плайлистколлектион** объекта **Player** .</span><span class="sxs-lookup"><span data-stu-id="0cb4d-129">You get the **PlaylistCollection** object from the **playlistCollection** property of the **Player** object.</span></span> <span data-ttu-id="0cb4d-130">Свойство **плайлистколлектион** возвращает объект **плайлистколлектион** .</span><span class="sxs-lookup"><span data-stu-id="0cb4d-130">The **playlistCollection** property returns the **PlaylistCollection** object.</span></span> <span data-ttu-id="0cb4d-131">Доступ к свойствам объекта **плайлистколлектион** можно получить только после его создания.</span><span class="sxs-lookup"><span data-stu-id="0cb4d-131">You can only access the properties of the **PlaylistCollection** object after you have created it.</span></span> <span data-ttu-id="0cb4d-132">Например, чтобы создать новый список воспроизведения, сначала необходимо получить объект **плайлистколлектион** , а затем использовать метод для этого объекта.</span><span class="sxs-lookup"><span data-stu-id="0cb4d-132">For example, to create a new playlist, you must first get the **PlaylistCollection** object and then use a method on that object.</span></span>


```C++
player.playlistcollection.newplaylist('myplaylist');
```



<span data-ttu-id="0cb4d-133">Текущий список воспроизведения можно получить с помощью свойства **куррентплайлист** .</span><span class="sxs-lookup"><span data-stu-id="0cb4d-133">You can get the current playlist by using the **currentPlaylist** property.</span></span> <span data-ttu-id="0cb4d-134">Например, чтобы получить имя текущего списка воспроизведения, используйте следующий код:</span><span class="sxs-lookup"><span data-stu-id="0cb4d-134">For example, to get the name of the current playlist, use the following code:</span></span>


```C++
myname = player.currentplaylist.name;
```



<span data-ttu-id="0cb4d-135">Объект **плайлистаррай** возвращается методами **жеталл** и **жетбинаме** объекта **плайлистколлектион** .</span><span class="sxs-lookup"><span data-stu-id="0cb4d-135">The **PlaylistArray** object is returned by the **getAll** and **getByName** methods of the **PlaylistCollection** object.</span></span> <span data-ttu-id="0cb4d-136">Например, чтобы получить количество списков воспроизведения, используйте следующий код:</span><span class="sxs-lookup"><span data-stu-id="0cb4d-136">To get the number of playlists, for example, use the following code:</span></span>


```C++
howmany = player.playlistcollection.getAll().count;
```



<span data-ttu-id="0cb4d-137">Чтобы получить известный список воспроизведения по имени, используйте следующий код:</span><span class="sxs-lookup"><span data-stu-id="0cb4d-137">To retrieve a known playlist by name, use the following code:</span></span>


```C++
if (player.playlistcollection.getbyname('myplaylist').count == 1) {
    pl = player.playlistcollection.getbyname('myplaylist').item(0);
}
```



## <a name="related-topics"></a><span data-ttu-id="0cb4d-138">См. также</span><span class="sxs-lookup"><span data-stu-id="0cb4d-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0cb4d-139">**Объектная модель проигрывателя для языков сценариев**</span><span class="sxs-lookup"><span data-stu-id="0cb4d-139">**Player Object Model for Scripting Languages**</span></span>](player-object-model-for-scripting-languages.md)
</dt> <dt>

[<span data-ttu-id="0cb4d-140">**Объект списка воспроизведения**</span><span class="sxs-lookup"><span data-stu-id="0cb4d-140">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="0cb4d-141">**Объект Плайлистаррай**</span><span class="sxs-lookup"><span data-stu-id="0cb4d-141">**PlaylistArray Object**</span></span>](playlistarray-object.md)
</dt> <dt>

[<span data-ttu-id="0cb4d-142">**Объект Плайлистколлектион**</span><span class="sxs-lookup"><span data-stu-id="0cb4d-142">**PlaylistCollection Object**</span></span>](playlistcollection-object.md)
</dt> </dl>

 

 




