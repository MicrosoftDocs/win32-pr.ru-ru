---
title: Использование списков автоматического воспроизведения для организации содержимого в библиотеке
description: Использование списков автоматического воспроизведения для организации содержимого в библиотеке
ms.assetid: 118d4357-044f-4986-af51-0c344470e891
keywords:
- Интернет-магазины проигрывателя Windows Media, автоматические списки воспроизведения
- Интернет-магазины, автоматические списки воспроизведения
- Тип 1 Интернет-магазины, автоматические списки воспроизведения
- Тип 2 Интернет-магазинов, автоматические списки воспроизведения
- Интернет-магазины проигрывателя Windows Media, упорядочение содержимого библиотеки
- Интернет-магазины, Организация содержимого библиотеки
- Тип 1 Интернет-магазины, упорядочение содержимого библиотеки
- Тип 2 Интернет-магазинов, упорядочение содержимого библиотеки
- Интернет-магазины проигрывателя Windows Media, Организация содержимого библиотеки
- Интернет-магазины, Организация содержимого библиотеки
- Тип 1 Интернет-магазины, Организация содержимого библиотеки
- Тип 2 Интернет-магазинов, Организация содержимого библиотеки
- Библиотека, упорядочение содержимого
- Организация содержимого библиотеки
- автоматические списки воспроизведения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa53a4b9f56a8aa6425f137ef4a8c43bd8ed1454
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104532249"
---
# <a name="using-auto-playlists-to-organize-content-in-the-library"></a><span data-ttu-id="130f6-118">Использование списков автоматического воспроизведения для организации содержимого в библиотеке</span><span class="sxs-lookup"><span data-stu-id="130f6-118">Using Auto Playlists to Organize Content in the Library</span></span>

<span data-ttu-id="130f6-119">Вы можете использовать автоматические списки воспроизведения для Организации предоставляемого вами содержимого Premium.</span><span class="sxs-lookup"><span data-stu-id="130f6-119">You can use auto playlists to organize premium content you provide.</span></span> <span data-ttu-id="130f6-120">Например, проигрыватель Windows Media можно использовать для создания автоматического списка воспроизведения, содержащего только те данные, которые вы указали как минимум на четыре звезды.</span><span class="sxs-lookup"><span data-stu-id="130f6-120">For example, you could use Windows Media Player to create an auto playlist that contains only content you provided having a user rating of at least four stars.</span></span> <span data-ttu-id="130f6-121">Затем можно добавить автоматический список воспроизведения в библиотеку в проигрывателе Windows Media, чтобы он отображался в узле "приобретенная музыка" узла распространителя содержимого.</span><span class="sxs-lookup"><span data-stu-id="130f6-121">You can then add the auto playlist to the library in Windows Media Player so that it displays in the Purchased Music node under your content distributor node.</span></span>

<span data-ttu-id="130f6-122">Для этого выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="130f6-122">To do this, follow these steps:</span></span>

1.  <span data-ttu-id="130f6-123">Создайте Автоматический список воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="130f6-123">Create the auto playlist.</span></span>
2.  <span data-ttu-id="130f6-124">С помощью проводника Windows перейдите к автоматическому списку воспроизведения и извлеките файл WPL.</span><span class="sxs-lookup"><span data-stu-id="130f6-124">Using Windows Explorer, browse to the auto playlist and retrieve the .wpl file.</span></span>
3.  <span data-ttu-id="130f6-125">С помощью объектной модели проигрывателя Windows Media добавьте автоматический список воспроизведения в библиотеку.</span><span class="sxs-lookup"><span data-stu-id="130f6-125">Using the Windows Media Player object model, add the auto playlist to the library.</span></span>
4.  <span data-ttu-id="130f6-126">Задайте атрибут **WM/контентдистрибутор** для списка воспроизведения в качестве имени ключа распространителя содержимого.</span><span class="sxs-lookup"><span data-stu-id="130f6-126">Set the **WM/ContentDistributor** attribute for the playlist to your content distributor key name.</span></span>
5.  <span data-ttu-id="130f6-127">Установите атрибут **синконли** для списка воспроизведения в значение true.</span><span class="sxs-lookup"><span data-stu-id="130f6-127">Set the **SyncOnly** attribute for the playlist to true.</span></span>

<span data-ttu-id="130f6-128">В следующем примере кода JScript показана функция, которая добавляет автоматический список воспроизведения с именем "Избранные посещения" в узел Proseware в библиотеке:</span><span class="sxs-lookup"><span data-stu-id="130f6-128">The following JScript example code shows a function that adds an auto playlist named "Favorite Hits" to the Proseware node in the library:</span></span>


```C++
function AddWPL()
{
    var pl = Player.mediaCollection.add("c:\\media\\Favorite Hits.wpl");
    pl.setItemInfo("WM/ContentDistributor", "Proseware");
    pl.setItemInfo("SyncOnly", true);
}
```



## <a name="related-topics"></a><span data-ttu-id="130f6-129">См. также</span><span class="sxs-lookup"><span data-stu-id="130f6-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="130f6-130">Сведения об интеграции библиотеки</span><span class="sxs-lookup"><span data-stu-id="130f6-130">About Library Integration</span></span>](download-manager-overview.md)
</dt> <dt>

[<span data-ttu-id="130f6-131">**Сведения, общие для типа 1 и 2 Интернет-магазинов**</span><span class="sxs-lookup"><span data-stu-id="130f6-131">**Information Common to Type 1 and Type 2 Online Stores**</span></span>](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="130f6-132">**Медиаколлектион. Add**</span><span class="sxs-lookup"><span data-stu-id="130f6-132">**MediaCollection.add**</span></span>](mediacollection-add.md)
</dt> <dt>

[<span data-ttu-id="130f6-133">**Список воспроизведения. Сетитеминфо**</span><span class="sxs-lookup"><span data-stu-id="130f6-133">**Playlist.setItemInfo**</span></span>](playlist-setiteminfo.md)
</dt> <dt>

[<span data-ttu-id="130f6-134">**Статические и автоматические списки воспроизведения**</span><span class="sxs-lookup"><span data-stu-id="130f6-134">**Static and Auto Playlists**</span></span>](static-and-auto-playlists.md)
</dt> <dt>

[<span data-ttu-id="130f6-135">**Атрибут Синконли**</span><span class="sxs-lookup"><span data-stu-id="130f6-135">**SyncOnly Attribute**</span></span>](synconly-attribute.md)
</dt> <dt>

[<span data-ttu-id="130f6-136">**Атрибут WM/Контентдистрибутор**</span><span class="sxs-lookup"><span data-stu-id="130f6-136">**WM/ContentDistributor Attribute**</span></span>](wm-contentdistributor-attribute.md)
</dt> <dt>

[<span data-ttu-id="130f6-137">**Работа с библиотекой**</span><span class="sxs-lookup"><span data-stu-id="130f6-137">**Working with the Library**</span></span>](working-with-the-library.md)
</dt> </dl>

 

 




