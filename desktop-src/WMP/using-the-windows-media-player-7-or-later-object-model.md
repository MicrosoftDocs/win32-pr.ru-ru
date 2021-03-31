---
title: Использование объектной модели проигрывателя Windows Media 7 или более поздней версии
description: Использование объектной модели проигрывателя Windows Media 7 или более поздней версии
ms.assetid: e2dbe2c1-23be-499b-b754-b7e87486ecd6
keywords:
- Проигрыватель Windows Media, объектная модель
- Объектная модель проигрывателя Windows Media версии 7 или более поздней
- Объектная модель версии 7 или более поздней
- Элемент управления ActiveX проигрывателя Windows Media версии 7 или более поздней
- Элемент управления ActiveX, версия 7 или более поздняя
- Элемент управления ActiveX проигрывателя Windows Media для мобильных устройств, версия 7 или более поздняя
- Проигрыватель Windows Media Mobile, объектная модель
- инструкции по миграции, версия 7 или более поздняя
- версии проигрывателя Windows Media, объектная модель
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8eb4d3d09b38e381d0cddeb25ee7cb5d7de3cb2b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330707"
---
# <a name="using-the-windows-media-player-7-or-later-object-model"></a><span data-ttu-id="fe98f-112">Использование объектной модели проигрывателя Windows Media 7 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="fe98f-112">Using the Windows Media Player 7 or Later Object Model</span></span>

<span data-ttu-id="fe98f-113">Большинство задач, которые вы могли выполнять с помощью объектной модели элемента управления ActiveX проигрывателя Windows Media 6,4, потребовали нового подхода.</span><span class="sxs-lookup"><span data-stu-id="fe98f-113">Most of the tasks you may have been performing using the Windows Media Player 6.4 ActiveX control object model will require a new approach.</span></span> <span data-ttu-id="fe98f-114">Во многих случаях имена свойств, методов и событий изменились в объектной модели проигрывателя Windows Media 7 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="fe98f-114">In many cases, the names of the properties, methods, and events have changed in the Windows Media Player 7 or later object model.</span></span> <span data-ttu-id="fe98f-115">Например, чтобы указать путь к файлу в объектной модели версии 6,4, необходимо задать свойство **Player6. filename** :</span><span class="sxs-lookup"><span data-stu-id="fe98f-115">For instance, to specify the file path in the version 6.4 object model, you set the **Player6.FileName** property:</span></span>


```C++
WMP64.FileName = "https://www.microsoft.com/somefile.wmv";

```



<span data-ttu-id="fe98f-116">При использовании объектной модели проигрывателя Windows Media 7 или более поздней версии необходимо задать свойство **Player. URL** :</span><span class="sxs-lookup"><span data-stu-id="fe98f-116">When using the Windows Media Player 7 or later object model, you must set the **Player.URL** property:</span></span>


```C++
WMP9.URL = "https://www.microsoft.com/somefile.wmv";

```



<span data-ttu-id="fe98f-117">Кроме того, используя модель с 10 объектами, можно получить объект **мультимедиа** из библиотеки, а затем задать свойство **Player. куррентмедиа** :</span><span class="sxs-lookup"><span data-stu-id="fe98f-117">Alternatively, using the 10 object model, you can obtain a **Media** object from the library, and then set the **Player.currentMedia** property:</span></span>


```C++
// Get the first media object in the media collection.
var MyMediaItem = WMP9.mediaCollection.getAll().item(0)

// Make the MyMediaItem object the current media.
WMP9.currentMedia = MyMediaItem;

```



<span data-ttu-id="fe98f-118">Многие функции в объектной модели проигрывателя Windows Media 7 или более поздней версии доступны через иерархию объектов.</span><span class="sxs-lookup"><span data-stu-id="fe98f-118">Much of the functionality in the Windows Media Player 7 or later object model is accessed through the object hierarchy.</span></span> <span data-ttu-id="fe98f-119">Как было показано в предыдущем примере, можно получить объект **списка воспроизведения** с помощью метода **жеталл** объекта **медиаколлектион** , доступ к которому осуществляется через объект корневого **проигрывателя** .</span><span class="sxs-lookup"><span data-stu-id="fe98f-119">As the previous example showed, you can obtain a **Playlist** object by using the **getAll** method of the **mediaCollection** object, which is accessed through the root **Player** object.</span></span> <span data-ttu-id="fe98f-120">Затем можно получить определенный объект **мультимедиа** из объекта **списка воспроизведения** с помощью метода **Item** объекта **списка воспроизведения** .</span><span class="sxs-lookup"><span data-stu-id="fe98f-120">You can then obtain a particular **Media** object from the **Playlist** object by using the **item** method of the **Playlist** object.</span></span> <span data-ttu-id="fe98f-121">Существует пять дополнительных методов, доступных через объект **медиаколлектион** , который возвращает объект **списка воспроизведения** . Каждый метод позволяет получить объект на основе конкретного критерия, например жанра или альбома.</span><span class="sxs-lookup"><span data-stu-id="fe98f-121">There are five additional methods accessible through the **mediaCollection** object that return a **Playlist** object; each method allows you to retrieve the object based on specific criteria, like genre or album.</span></span>

<span data-ttu-id="fe98f-122">Иерархическая структура объектной модели элемента управления ActiveX в проигрывателе Windows Media 7 или более поздней версии предоставляет более логичный подход к Организации свойств, методов и событий, доступных для использования.</span><span class="sxs-lookup"><span data-stu-id="fe98f-122">The hierarchical structure of the Windows Media Player 7 or later ActiveX control object model provides a more logical approach to organizing the properties, methods, and events available for your use.</span></span> <span data-ttu-id="fe98f-123">Все функции элементов управления проигрывателя содержатся в объекте **Controls** , все функциональные возможности сетевого подключения проигрывателя содержатся в объекте **Network** и т. д.</span><span class="sxs-lookup"><span data-stu-id="fe98f-123">All the functionality for the Player controls is contained in the **Controls** object, all the functionality for the Player network connection is contained in the **Network** object, and so forth.</span></span> <span data-ttu-id="fe98f-124">Например, чтобы запустить воспроизведение содержимого с помощью объектной модели версии 6,4, используйте метод **Player6. Play** :</span><span class="sxs-lookup"><span data-stu-id="fe98f-124">For example, to start content playing using the version 6.4 object model, you use the **Player6.Play** method:</span></span>


```C++
WMP64.Play();

```



<span data-ttu-id="fe98f-125">При использовании объектной модели проигрывателя Windows Media 7 или более поздней версии необходимо получить доступ к методу **Play** с помощью объекта **Controls** :</span><span class="sxs-lookup"><span data-stu-id="fe98f-125">When using the Windows Media Player 7 or later object model, you must access the **Play** method by using the **Controls** object:</span></span>


```C++
WMP9.controls.play();

```



<span data-ttu-id="fe98f-126">Однако глубина объектной модели может привести к очень длинным инструкциям скрипта:</span><span class="sxs-lookup"><span data-stu-id="fe98f-126">The depth of the object model, however, can lead to very long script statements:</span></span>


```C++
WMP9.currentPlaylist.appendItem(WMP9.mediaCollection.getByName("MySong").item(0));

```



<span data-ttu-id="fe98f-127">Инструкции, подобные предыдущему, можно сделать намного проще и удобнее читать, работая с отдельными именованными объектами.</span><span class="sxs-lookup"><span data-stu-id="fe98f-127">Statements like the preceding one can be made much simpler and more readable by working with individual named objects.</span></span> <span data-ttu-id="fe98f-128">В следующем примере приведенный выше оператор Code заменяет синтаксис с использованием отдельных переменных объекта:</span><span class="sxs-lookup"><span data-stu-id="fe98f-128">The following example replaces the preceding code statement with syntax using separate object variables:</span></span>


```C++
// Store the current playlist object.
var pl = WMP9.currentPlaylist;

// Get a playlist from the media collection that contains
// one media item named "MySong".
var temp = WMP9.mediaCollection.getByName("MySong");

// Get the individual media item from the temp playlist.
var song = temp.item(0);

// Append the media item to the current playlist.
pl.appendItem(song);

```



<span data-ttu-id="fe98f-129">Этот стиль написания кода требует больше строк сценария, но его гораздо проще выполнить, особенно с добавленными комментариями.</span><span class="sxs-lookup"><span data-stu-id="fe98f-129">This coding style requires more lines of script, but is much easier to follow, especially with the added comments.</span></span> <span data-ttu-id="fe98f-130">Существует еще одно преимущество: объект **куррентплайлист** легко использовать повторно, так как он хранится в переменной PL.</span><span class="sxs-lookup"><span data-stu-id="fe98f-130">There is another advantage: the **currentPlaylist** object is easy to reuse because it is stored in the variable pl.</span></span>

<span data-ttu-id="fe98f-131">Многие свойства, методы и события в объектной модели проигрывателя Windows Media 7 или более поздней версии задают или извлекают различные значения или возвращают значения другого типа или числа по сравнению с соответствующими функциями в объектной модели версии 6,4.</span><span class="sxs-lookup"><span data-stu-id="fe98f-131">Many of the properties, methods, and events in the Windows Media Player 7 or later object model set or retrieve different values, or return values of a different type or number, compared to corresponding functionality in the version 6.4 object model.</span></span> <span data-ttu-id="fe98f-132">Например, когда **Player6. опенстате** получает 2, это значение соответствует Visual Basic константной **нслоадингнск**, означающее, что проигрыватель загружает файл станции с расширением NSC.</span><span class="sxs-lookup"><span data-stu-id="fe98f-132">For instance, when **Player6.openState** retrieves 2, that value corresponds to the Visual Basic constant **nsLoadingNSC**, meaning the Player is loading a station file with a .nsc file name extension.</span></span> <span data-ttu-id="fe98f-133">Но когда проигрыватель Windows Media 7 или более поздней версии свойства объектной модели объекта **Player. опенстате** получает 2, это значение соответствует состоянию плайлистлокатинг, означающее, что проигрыватель Windows Media пытается выполнить поиск списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="fe98f-133">But when the Windows Media Player 7 or later object model property **Player.openState** retrieves 2, that value corresponds to the state PlaylistLocating, meaning Windows Media Player is attempting to locate a playlist.</span></span> <span data-ttu-id="fe98f-134">Кроме того, свойство **Player6. опенстате** может извлекать семь различных значений, в то время как свойство **Player** проигрывателя Windows Media 7 или более поздней версии может получить 22 различных значения.</span><span class="sxs-lookup"><span data-stu-id="fe98f-134">Additionally, the **Player6.openState** property can retrieve seven different values, while the Windows Media Player 7 or later **Player.openState** property can retrieve 22 different values.</span></span> <span data-ttu-id="fe98f-135">Не забудьте обратиться к Справочнику по объектной модели для создания сценариев пакета SDK проигрывателя Windows Media при пересмотре кода для использования другой версии объектной модели.</span><span class="sxs-lookup"><span data-stu-id="fe98f-135">Be sure to refer to the Object Model Reference for Scripting section of the Windows Media Player SDK when revising code to use a different object model version.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fe98f-136">См. также</span><span class="sxs-lookup"><span data-stu-id="fe98f-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fe98f-137">**Сведения об объектной модели проигрывателя**</span><span class="sxs-lookup"><span data-stu-id="fe98f-137">**About the Player Object Model**</span></span>](about-the-player-object-model.md)
</dt> <dt>

[<span data-ttu-id="fe98f-138">**Справочник по объектной модели для создания сценариев**</span><span class="sxs-lookup"><span data-stu-id="fe98f-138">**Object Model Reference for Scripting**</span></span>](object-model-reference-for-scripting.md)
</dt> <dt>

[<span data-ttu-id="fe98f-139">**Руководством по миграции объектной модели**</span><span class="sxs-lookup"><span data-stu-id="fe98f-139">**Object Model Migration Guide**</span></span>](object-model-migration-guide.md)
</dt> </dl>

 

 




