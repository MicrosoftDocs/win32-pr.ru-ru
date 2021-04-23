---
title: Справочник по объектной модели для создания сценариев
description: Справочник по объектной модели для создания сценариев
ms.assetid: a900fd55-2213-46db-84ad-93f199c60182
keywords:
- Проигрыватель Windows Media, объектная модель
- Проигрыватель Windows Media Mobile, объектная модель
- Объектная модель проигрывателя Windows Media, Справочник
- Объектная модель, Справочник
- Элемент управления ActiveX, Справочник
- Элемент управления ActiveX проигрывателя Windows Media, Справочник
- Элемент управления ActiveX проигрывателя Windows Media Mobile, Справочник
- Справочник по объектной модели, написанию сценариев
- Проигрыватель Windows Media, Справочник по сценариям
- Проигрыватель Windows Media Mobile, Справочник по сценариям
- Объектная модель проигрывателя Windows Media, Справочник по сценариям
- Объектная модель, Справочник по сценариям
- Элемент управления ActiveX проигрывателя Windows Media, Справочник по сценариям
- Элемент управления ActiveX проигрывателя Windows Media Mobile, Справочник по сценариям
- Элемент управления ActiveX, Справочник по сценариям
- Справочник по объектной модели сценариев
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f20e5bacf6a1fd93579ce40e8957b7ce7aefae0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105691338"
---
# <a name="object-model-reference-for-scripting"></a><span data-ttu-id="0c021-119">Справочник по объектной модели для создания сценариев</span><span class="sxs-lookup"><span data-stu-id="0c021-119">Object Model Reference for Scripting</span></span>

<span data-ttu-id="0c021-120">В справочнике по объектной модели содержатся подробные сведения об объектной модели элемента управления ActiveX проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="0c021-120">The object model reference for scripting contains detailed information about the Windows Media Player ActiveX control object model.</span></span> <span data-ttu-id="0c021-121">Сведения в этом разделе представлены в стиле, предназначенном для использования с такими языками сценариев, как Microsoft JScript.</span><span class="sxs-lookup"><span data-stu-id="0c021-121">The information in this section is presented in a style designed for use with script languages like Microsoft JScript.</span></span>

> [!Note]  
> <span data-ttu-id="0c021-122">Все методы, свойства и события полностью поддерживаются в проигрывателе Windows Media 10 Mobile или более поздней версии, если явно не указано иное.</span><span class="sxs-lookup"><span data-stu-id="0c021-122">All methods, properties, and events are fully supported in Windows Media Player 10 Mobile or later unless explicitly stated otherwise.</span></span>

 

<span data-ttu-id="0c021-123">Справочник по объектной модели содержит документацию по следующим объектам и связанным с ними методам, свойствам и событиям.</span><span class="sxs-lookup"><span data-stu-id="0c021-123">The object model reference for scripting contains documentation for the following objects and their associated methods, properties, and events.</span></span>



| <span data-ttu-id="0c021-124">Объект</span><span class="sxs-lookup"><span data-stu-id="0c021-124">Object</span></span>                                              | <span data-ttu-id="0c021-125">Описание</span><span class="sxs-lookup"><span data-stu-id="0c021-125">Description</span></span>                                                                                                                                                                                    |
|-----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0c021-126">ROM</span><span class="sxs-lookup"><span data-stu-id="0c021-126">Cdrom</span></span>](cdrom-object.md)                           | <span data-ttu-id="0c021-127">Методы и свойства для доступа к компакт-диску или DVD-диску на его диске.</span><span class="sxs-lookup"><span data-stu-id="0c021-127">Methods and properties for accessing a CD or DVD in its drive.</span></span>                                                                                                                                 |
| [<span data-ttu-id="0c021-128">кдромколлектион</span><span class="sxs-lookup"><span data-stu-id="0c021-128">CdromCollection</span></span>](cdromcollection-object.md)       | <span data-ttu-id="0c021-129">Методы и свойства для доступа к коллекции компакт-дисков или DVD-дисководов.</span><span class="sxs-lookup"><span data-stu-id="0c021-129">Methods and properties for accessing a collection of CD or DVD drives.</span></span>                                                                                                                         |
| [<span data-ttu-id="0c021-130">клоседкаптион</span><span class="sxs-lookup"><span data-stu-id="0c021-130">ClosedCaption</span></span>](closedcaption-object.md)           | <span data-ttu-id="0c021-131">Свойства для включения субтитров с помощью элемента мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="0c021-131">Properties for including captions with a media item.</span></span>                                                                                                                                           |
| [<span data-ttu-id="0c021-132">Элементы управления</span><span class="sxs-lookup"><span data-stu-id="0c021-132">Controls</span></span>](controls-object.md)                     | <span data-ttu-id="0c021-133">Методы и свойства, представляющие элементы управления транспорта Windows Media Player, такие как воспроизведение, остановка и пауза.</span><span class="sxs-lookup"><span data-stu-id="0c021-133">Methods and properties representing the transport controls of Windows Media Player, such as Play, Stop, and Pause.</span></span>                                                                             |
| [<span data-ttu-id="0c021-134">ОПТИЧЕСКИ</span><span class="sxs-lookup"><span data-stu-id="0c021-134">DVD</span></span>](dvd-object.md)                               | <span data-ttu-id="0c021-135">Свойство, методы и события для работы с DVD-дисками.</span><span class="sxs-lookup"><span data-stu-id="0c021-135">A property, methods, and events for working with DVDs.</span></span>                                                                                                                                         |
| [<span data-ttu-id="0c021-136">Ошибка</span><span class="sxs-lookup"><span data-stu-id="0c021-136">Error</span></span>](error-object.md)                           | <span data-ttu-id="0c021-137">Методы и свойства, предоставляющие доступ к коллекции объектов **ерроритем** .</span><span class="sxs-lookup"><span data-stu-id="0c021-137">Methods and properties providing access to a collection of **ErrorItem** objects.</span></span>                                                                                                              |
| [<span data-ttu-id="0c021-138">ерроритем</span><span class="sxs-lookup"><span data-stu-id="0c021-138">ErrorItem</span></span>](erroritem-object.md)                   | <span data-ttu-id="0c021-139">Свойства, предоставляющие сведения об ошибках.</span><span class="sxs-lookup"><span data-stu-id="0c021-139">Properties that provide information about errors.</span></span>                                                                                                                                              |
| [<span data-ttu-id="0c021-140">Носитель</span><span class="sxs-lookup"><span data-stu-id="0c021-140">Media</span></span>](media-object.md)                           | <span data-ttu-id="0c021-141">Методы и свойства, относящиеся к элементам мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="0c021-141">Methods and properties relating to media items.</span></span>                                                                                                                                                |
| [<span data-ttu-id="0c021-142">медиаколлектион</span><span class="sxs-lookup"><span data-stu-id="0c021-142">MediaCollection</span></span>](mediacollection-object.md)       | <span data-ttu-id="0c021-143">Методы, предоставляющие доступ к коллекции объектов **мультимедиа** .</span><span class="sxs-lookup"><span data-stu-id="0c021-143">Methods that provide access to a collection of **Media** objects.</span></span>                                                                                                                              |
| [<span data-ttu-id="0c021-144">метадатапиктуре</span><span class="sxs-lookup"><span data-stu-id="0c021-144">MetadataPicture</span></span>](metadatapicture-object.md)       | <span data-ttu-id="0c021-145">Свойства для получения сведений о значениях изображения атрибута метаданных **WM/Picture** .</span><span class="sxs-lookup"><span data-stu-id="0c021-145">Properties for retrieving information on the image values of the **WM/Picture** metadata attribute.</span></span>                                                                                            |
| [<span data-ttu-id="0c021-146">метадататекст</span><span class="sxs-lookup"><span data-stu-id="0c021-146">MetadataText</span></span>](metadatatext-object.md)             | <span data-ttu-id="0c021-147">Свойства для получения метаданных для сложных атрибутов текстовых метаданных.</span><span class="sxs-lookup"><span data-stu-id="0c021-147">Properties for retrieving metadata for complex textual metadata attributes.</span></span>                                                                                                                    |
| [<span data-ttu-id="0c021-148">Network</span><span class="sxs-lookup"><span data-stu-id="0c021-148">Network</span></span>](network-object.md)                       | <span data-ttu-id="0c021-149">Свойства, относящиеся к сетевому подключению проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="0c021-149">Properties relating to the network connection of Windows Media Player.</span></span>                                                                                                                         |
| [<span data-ttu-id="0c021-150">Игрок</span><span class="sxs-lookup"><span data-stu-id="0c021-150">Player</span></span>](player-object.md)                         | <span data-ttu-id="0c021-151">Методы, свойства и события, которые проигрыватель Windows Media может программировать для реагирования.</span><span class="sxs-lookup"><span data-stu-id="0c021-151">Methods, properties, and events that Windows Media Player can be programmed to respond to.</span></span>                                                                                                     |
| [<span data-ttu-id="0c021-152">PlayerApplication</span><span class="sxs-lookup"><span data-stu-id="0c021-152">PlayerApplication</span></span>](playerapplication-object.md)   | <span data-ttu-id="0c021-153">Методы и свойства для переключения между удаленным элементом управления проигрывателя Windows Media и полноэкранным режимом проигрывателя.</span><span class="sxs-lookup"><span data-stu-id="0c021-153">Methods and properties for switching between a remoted Windows Media Player control and the full mode of the Player.</span></span> <span data-ttu-id="0c021-154">Может использоваться только с программами C++, которые внедряют элемент управления в удаленный режим.</span><span class="sxs-lookup"><span data-stu-id="0c021-154">Can only be used with C++ programs that embed the control in remote mode.</span></span> |
| [<span data-ttu-id="0c021-155">Списком</span><span class="sxs-lookup"><span data-stu-id="0c021-155">Playlist</span></span>](playlist-object.md)                     | <span data-ttu-id="0c021-156">Методы и свойства для управления списками элементов мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="0c021-156">Methods and properties for manipulating lists of media items.</span></span>                                                                                                                                  |
| [<span data-ttu-id="0c021-157">плайлистаррай</span><span class="sxs-lookup"><span data-stu-id="0c021-157">PlaylistArray</span></span>](playlistarray-object.md)           | <span data-ttu-id="0c021-158">Метод и свойство для доступа к коллекции объектов **списков воспроизведения** по номеру индекса.</span><span class="sxs-lookup"><span data-stu-id="0c021-158">A method and a property for accessing a collection of **Playlist** objects by index number.</span></span>                                                                                                    |
| [<span data-ttu-id="0c021-159">плайлистколлектион</span><span class="sxs-lookup"><span data-stu-id="0c021-159">PlaylistCollection</span></span>](playlistcollection-object.md) | <span data-ttu-id="0c021-160">Методы организации коллекции объектов **списков воспроизведения** .</span><span class="sxs-lookup"><span data-stu-id="0c021-160">Methods for organizing a collection of **Playlist** objects.</span></span>                                                                                                                                   |
| [<span data-ttu-id="0c021-161">Запрос</span><span class="sxs-lookup"><span data-stu-id="0c021-161">Query</span></span>](query-object.md)                           | <span data-ttu-id="0c021-162">Методы изменения составного запроса.</span><span class="sxs-lookup"><span data-stu-id="0c021-162">Methods for modifying a compound query.</span></span>                                                                                                                                                        |
| [<span data-ttu-id="0c021-163">Параметры</span><span class="sxs-lookup"><span data-stu-id="0c021-163">Settings</span></span>](settings-object.md)                     | <span data-ttu-id="0c021-164">Свойства, разрешающие спецификацию или извлечение параметров проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="0c021-164">Properties that allow the specification or retrieval of Windows Media Player settings.</span></span>                                                                                                         |
| [<span data-ttu-id="0c021-165">StringCollection</span><span class="sxs-lookup"><span data-stu-id="0c021-165">StringCollection</span></span>](stringcollection-object.md)     | <span data-ttu-id="0c021-166">Метод и свойство для управления коллекциями строк.</span><span class="sxs-lookup"><span data-stu-id="0c021-166">A method and a property for manipulating collections of strings.</span></span>                                                                                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="0c021-167">См. также</span><span class="sxs-lookup"><span data-stu-id="0c021-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0c021-168">**Справочник по объектной модели проигрывателя Windows Media**</span><span class="sxs-lookup"><span data-stu-id="0c021-168">**Windows Media Player Object Model Reference**</span></span>](windows-media-player-object-model-reference.md)
</dt> </dl>

 

 




