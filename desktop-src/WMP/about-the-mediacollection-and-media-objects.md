---
title: Сведения об объектах Медиаколлектион и Media
description: Сведения об объектах Медиаколлектион и Media
ms.assetid: e3260efd-44cc-4b4e-9f48-3441631bfa4f
keywords:
- Проигрыватель Windows Media, объект Медиаколлектион
- Объектная модель проигрывателя Windows Media, объект Медиаколлектион
- Объектная модель, объект Медиаколлектион
- Элемент управления ActiveX проигрывателя Windows Media, объект Медиаколлектион
- Элемент управления ActiveX, объект Медиаколлектион
- Элемент управления мобильными устройствами ActiveX проигрывателя Windows Media, объект Медиаколлектион
- Проигрыватель Windows Media Mobile, объект Медиаколлектион
- Объект Медиаколлектион
- Проигрыватель Windows Media, объект мультимедиа
- Объектная модель проигрывателя Windows Media, объект мультимедиа
- Объектная модель, объект мультимедиа
- Элемент управления ActiveX проигрывателя Windows Media, объект мультимедиа
- Элемент управления ActiveX, объект мультимедиа
- Элемент управления мобильными устройствами ActiveX проигрывателя Windows Media, объект мультимедиа
- Проигрыватель Windows Media Mobile, объект мультимедиа
- Объект мультимедиа
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe902fd9ed046e0197fb5c8c2d995d26befafe29
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105691317"
---
# <a name="about-the-mediacollection-and-media-objects"></a><span data-ttu-id="65225-119">Сведения об объектах Медиаколлектион и Media</span><span class="sxs-lookup"><span data-stu-id="65225-119">About the MediaCollection and Media Objects</span></span>

<span data-ttu-id="65225-120">Объекты **медиаколлектион** и **Media** управляют коллекцией носителей, которая определяет расположение цифровых файлов мультимедиа, к которым имеет доступ проигрыватель Windows Media.</span><span class="sxs-lookup"><span data-stu-id="65225-120">The **MediaCollection** and **Media** objects govern the media collection, which defines the locations of digital media files that Windows Media Player can access.</span></span> <span data-ttu-id="65225-121">Вы получаете объект **медиаколлектион** из свойства **медиаколлектион** объекта **Player** .</span><span class="sxs-lookup"><span data-stu-id="65225-121">You get the **MediaCollection** object from the **mediaCollection** property of the **Player** object.</span></span> <span data-ttu-id="65225-122">Свойство **медиаколлектион** возвращает объект **медиаколлектион** .</span><span class="sxs-lookup"><span data-stu-id="65225-122">The **mediaCollection** property returns the **MediaCollection** object.</span></span> <span data-ttu-id="65225-123">Доступ к свойствам объекта **медиаколлектион** можно получить только после его создания.</span><span class="sxs-lookup"><span data-stu-id="65225-123">You can only access the properties of the **MediaCollection** object after you have created it.</span></span> <span data-ttu-id="65225-124">Например, чтобы добавить объект **мультимедиа** (песню), используйте следующий код:</span><span class="sxs-lookup"><span data-stu-id="65225-124">For example, to add a **Media** object (a song), use the following code:</span></span>


```C++
player.mediacollection.add('laure.wma');

```



<span data-ttu-id="65225-125">Вы добавили файл Лауре. wma в коллекцию носителей.</span><span class="sxs-lookup"><span data-stu-id="65225-125">You have added the file laure.wma to the media collection.</span></span>

<span data-ttu-id="65225-126">Текущий объект **мультимедиа** можно получить с помощью свойства **куррентмедиа** **проигрывателя**.</span><span class="sxs-lookup"><span data-stu-id="65225-126">You can get the current **Media** object by using the **currentMedia** property of the **Player**.</span></span> <span data-ttu-id="65225-127">Например, этот код получает свойство **Duration** текущего объекта **мультимедиа** :</span><span class="sxs-lookup"><span data-stu-id="65225-127">For example, this code gets the **duration** property of the current **Media** object:</span></span>


```C++
myduration = player.currentmedia.duration;

```



<span data-ttu-id="65225-128">Существует много способов получить объект **мультимедиа** , чтобы получить доступ к его свойствам.</span><span class="sxs-lookup"><span data-stu-id="65225-128">There are many ways to get a **Media** object so that you can access its properties.</span></span> <span data-ttu-id="65225-129">Например, если требуется получить доступ к свойству **Duration** текущего носителя, можно использовать каждую из следующих строк кода.</span><span class="sxs-lookup"><span data-stu-id="65225-129">For example, if you want to access the **duration** property of the current media, each of the following lines of code could be used.</span></span>

<span data-ttu-id="65225-130">Чтобы получить время воспроизведения мультимедиа, сделайте следующее:</span><span class="sxs-lookup"><span data-stu-id="65225-130">To get the duration of the currently playing media:</span></span>


```C++
player.currentMedia.duration;

```



<span data-ttu-id="65225-131">Чтобы получить длительность текущего носителя в списке воспроизведения, сделайте следующее:</span><span class="sxs-lookup"><span data-stu-id="65225-131">To get the duration of the current media in a playlist:</span></span>


```C++
player.controls.currentItem.duration;

```



<span data-ttu-id="65225-132">Чтобы получить длительность третьего элемента мультимедиа в списке воспроизведения, сделайте следующее:</span><span class="sxs-lookup"><span data-stu-id="65225-132">To get the duration of the third media item in a playlist:</span></span>


```C++
player.currentPlaylist.item(2).duration;

```



<span data-ttu-id="65225-133">Чтобы получить длительность третьего элемента мультимедиа в жанре джаз, сделайте следующее:</span><span class="sxs-lookup"><span data-stu-id="65225-133">To get the duration of the third media item in a "Jazz" genre:</span></span>


```C++
player.mediaCollection.getByGenre("jazz").item(2).duration;

```



<span data-ttu-id="65225-134">Чтобы получить длительность третьего элемента мультимедиа во втором списке воспроизведения, сделайте следующее:</span><span class="sxs-lookup"><span data-stu-id="65225-134">To get the duration of the third media item in the second playlist:</span></span>


```C++
player.playlistCollection.getAll.item(1).item(2).duration; 
```



## <a name="related-topics"></a><span data-ttu-id="65225-135">См. также</span><span class="sxs-lookup"><span data-stu-id="65225-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="65225-136">**Объект мультимедиа**</span><span class="sxs-lookup"><span data-stu-id="65225-136">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="65225-137">**Объект Медиаколлектион**</span><span class="sxs-lookup"><span data-stu-id="65225-137">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="65225-138">**Объектная модель проигрывателя для языков сценариев**</span><span class="sxs-lookup"><span data-stu-id="65225-138">**Player Object Model for Scripting Languages**</span></span>](player-object-model-for-scripting-languages.md)
</dt> </dl>

 

 




