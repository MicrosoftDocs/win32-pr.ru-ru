---
title: Атрибуты элемента мультимедиа
description: Атрибуты элемента мультимедиа
ms.assetid: d43addec-e06c-4ef3-9012-3ecf589b105c
keywords:
- Проигрыватель Windows Media, Библиотека
- Объектная модель проигрывателя Windows Media, Библиотека
- Объектная модель, Библиотека
- Проигрыватель Windows Media Mobile, Библиотека для объектной модели
- Элемент управления ActiveX проигрывателя Windows Media, Библиотека для объектной модели
- Элемент управления ActiveX мобильных устройств Windows Media Player, Библиотека для объектной модели
- Элемент управления ActiveX, Библиотека для объектной модели
- Проигрыватель Windows Media, атрибуты для элементов мультимедиа
- Объектная модель проигрывателя Windows Media, атрибуты элементов мультимедиа
- Объектная модель, атрибуты элементов мультимедиа
- Проигрыватель Windows Media Mobile, атрибуты для элементов мультимедиа
- Элемент управления ActiveX проигрывателя Windows Media, атрибуты для элементов мультимедиа
- Элемент управления мобильными устройствами ActiveX проигрывателя Windows Media, атрибуты для элементов мультимедиа
- Элемент управления ActiveX, атрибуты для элементов мультимедиа
- Библиотека проигрывателя Windows Media, атрибуты для элементов мультимедиа
- Библиотека, атрибуты для элементов мультимедиа
- атрибуты, сведения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5ac8595cc07504c9cd3e195431513a1f8565e87
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067940"
---
# <a name="media-item-attributes"></a><span data-ttu-id="0290c-120">Атрибуты элемента мультимедиа</span><span class="sxs-lookup"><span data-stu-id="0290c-120">Media Item Attributes</span></span>

<span data-ttu-id="0290c-121">При просмотре библиотеки в проигрывателе Windows Media обычно отображается большой объем информации об элементе мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="0290c-121">When you look at the library in Windows Media Player, you typically see a great deal of information about a media item.</span></span> <span data-ttu-id="0290c-122">В дополнение к имени звуковой дорожки, например, вы увидите имя альбома, на котором находится дорожка, названия исполнителя и композитора, жанр музыки и т. д.</span><span class="sxs-lookup"><span data-stu-id="0290c-122">In addition to the name of an audio track, for example, you will likely see the name of the album the track is on, the names of the artist and composer, the genre of the music, and so on.</span></span>

<span data-ttu-id="0290c-123">В объектной модели проигрывателя Windows Media эти элементы метаданных называются атрибутами.</span><span class="sxs-lookup"><span data-stu-id="0290c-123">In the Windows Media Player object model, these metadata items are called attributes.</span></span> <span data-ttu-id="0290c-124">Объектная модель содержит свойства и методы, которые можно использовать для запроса элементов мультимедиа и списков воспроизведения для атрибутов.</span><span class="sxs-lookup"><span data-stu-id="0290c-124">The object model includes properties and methods you can use to query media items and playlists for attributes.</span></span> <span data-ttu-id="0290c-125">Затем можно отобразить значения атрибутов в пользовательском интерфейсе, или код может выполнять действия на основе значения атрибута.</span><span class="sxs-lookup"><span data-stu-id="0290c-125">You can then display attribute values in your user interface, or your code can take actions based on the value of an attribute.</span></span>

<span data-ttu-id="0290c-126">В следующих разделах описывается работа с атрибутами элементов мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="0290c-126">The following topics describe working with media item attributes.</span></span>



| <span data-ttu-id="0290c-127">Раздел</span><span class="sxs-lookup"><span data-stu-id="0290c-127">Topic</span></span>                                                                                      | <span data-ttu-id="0290c-128">Описание</span><span class="sxs-lookup"><span data-stu-id="0290c-128">Description</span></span>                                                                                     |
|--------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0290c-129">Основные сведения об источниках атрибутов</span><span class="sxs-lookup"><span data-stu-id="0290c-129">Understanding Attribute Sources</span></span>](understanding-attribute-sources.md)                     | <span data-ttu-id="0290c-130">Описывает, как источник элемента мультимедиа влияет на атрибуты, которые могут быть связаны с ним.</span><span class="sxs-lookup"><span data-stu-id="0290c-130">Describes how the source of a media item affects the attributes that may be associated with it.</span></span> |
| [<span data-ttu-id="0290c-131">Считывание значений атрибутов</span><span class="sxs-lookup"><span data-stu-id="0290c-131">Reading Attribute Values</span></span>](reading-attribute-values.md)                                   | <span data-ttu-id="0290c-132">Показывает методы получения значения атрибута.</span><span class="sxs-lookup"><span data-stu-id="0290c-132">Shows the methods for retrieving the value of an attribute.</span></span>                                     |
| [<span data-ttu-id="0290c-133">Атрибуты с несколькими значениями</span><span class="sxs-lookup"><span data-stu-id="0290c-133">Attributes with Multiple Values</span></span>](attributes-with-multiple-values.md)                     | <span data-ttu-id="0290c-134">Показывает методы получения значения атрибута с несколькими значениями.</span><span class="sxs-lookup"><span data-stu-id="0290c-134">Shows the methods for retrieving the value of a multi-valued attribute.</span></span>                         |
| [<span data-ttu-id="0290c-135">Считывание значений атрибутов с компакт-диска или DVD-диска</span><span class="sxs-lookup"><span data-stu-id="0290c-135">Reading Attribute Values from a CD or DVD</span></span>](reading-attribute-values-from-a-cd-or-dvd.md) | <span data-ttu-id="0290c-136">Предоставляет пример приложения, считывающего все атрибуты элемента мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="0290c-136">Provides a sample application that reads all of the attributes of a media item.</span></span>                 |
| [<span data-ttu-id="0290c-137">Изменение значений атрибутов</span><span class="sxs-lookup"><span data-stu-id="0290c-137">Changing Attribute Values</span></span>](changing-attribute-values.md)                                 | <span data-ttu-id="0290c-138">Показывает метод изменения значения атрибута.</span><span class="sxs-lookup"><span data-stu-id="0290c-138">Shows the method for changing the value of an attribute.</span></span>                                        |
| [<span data-ttu-id="0290c-139">Значения атрибутов для ТВ-содержимого</span><span class="sxs-lookup"><span data-stu-id="0290c-139">Attribute Values for TV Content</span></span>](attribute-values-for-tv-content.md)                     | <span data-ttu-id="0290c-140">Показывает, как указать атрибуты для цифрового видеосодержимого, содержащего ТВ-передачи.</span><span class="sxs-lookup"><span data-stu-id="0290c-140">Shows how to specify attributes for digital video content that contains TV shows.</span></span>               |



 

## <a name="related-topics"></a><span data-ttu-id="0290c-141">См. также</span><span class="sxs-lookup"><span data-stu-id="0290c-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0290c-142">**Атрибуты списка воспроизведения**</span><span class="sxs-lookup"><span data-stu-id="0290c-142">**Playlist Attributes**</span></span>](playlist-attributes.md)
</dt> <dt>

[<span data-ttu-id="0290c-143">**Работа с библиотекой**</span><span class="sxs-lookup"><span data-stu-id="0290c-143">**Working with the Library**</span></span>](working-with-the-library.md)
</dt> </dl>

 

 




