---
title: Объект мультимедиа
description: Объект мультимедиа предоставляет способ задания или извлечения свойств элемента мультимедиа с помощью следующих свойств и методов.
ms.assetid: 45c1c760-808b-4d11-8e6b-057a2ca685d0
keywords:
- Проигрыватель Windows Media, мультимедийный объект
topic_type:
- apiref
api_name:
- Media Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 88eff6ee0a97e63df6a0c073ef18425cbb576e85
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "105691412"
---
# <a name="media-object"></a><span data-ttu-id="51d79-104">Объект мультимедиа</span><span class="sxs-lookup"><span data-stu-id="51d79-104">Media Object</span></span>

<span data-ttu-id="51d79-105">Объект **мультимедиа** предоставляет способ задания или извлечения свойств элемента мультимедиа с помощью следующих свойств и методов.</span><span class="sxs-lookup"><span data-stu-id="51d79-105">The **Media** object provides a way to specify or retrieve properties of a media item, using the following properties and methods.</span></span>

<span data-ttu-id="51d79-106">Объект **мультимедиа** поддерживает следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="51d79-106">The **Media** object supports the following properties.</span></span>



| <span data-ttu-id="51d79-107">Свойство</span><span class="sxs-lookup"><span data-stu-id="51d79-107">Property</span></span>                                         | <span data-ttu-id="51d79-108">Описание</span><span class="sxs-lookup"><span data-stu-id="51d79-108">Description</span></span>                                                                                        |
|--------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="51d79-109">аттрибутекаунт</span><span class="sxs-lookup"><span data-stu-id="51d79-109">attributeCount</span></span>](media-attributecount.md)       | <span data-ttu-id="51d79-110">Возвращает количество атрибутов, которые могут быть запрошены или заданы для элемента мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="51d79-110">Retrieves the number of attributes that can be queried and/or set for the media item.</span></span>              |
| [<span data-ttu-id="51d79-111">duration</span><span class="sxs-lookup"><span data-stu-id="51d79-111">duration</span></span>](media-duration.md)                   | <span data-ttu-id="51d79-112">Возвращает длительность текущего элемента мультимедиа в секундах.</span><span class="sxs-lookup"><span data-stu-id="51d79-112">Retrieves the duration in seconds of the current media item.</span></span>                                       |
| [<span data-ttu-id="51d79-113">дуратионстринг</span><span class="sxs-lookup"><span data-stu-id="51d79-113">durationString</span></span>](media-durationstring.md)       | <span data-ttu-id="51d79-114">Извлекает **строковое** значение, указывающее длительность текущего элемента мультимедиа в формате чч: мм: СС.</span><span class="sxs-lookup"><span data-stu-id="51d79-114">Retrieves a **String** value indicating the duration of the current media item in HH:MM:SS format.</span></span> |
| [<span data-ttu-id="51d79-115">error</span><span class="sxs-lookup"><span data-stu-id="51d79-115">error</span></span>](media-error.md)                         | <span data-ttu-id="51d79-116">Извлекает объект [ерроритем](erroritem-object.md) , если у элемента мультимедиа есть условие ошибки.</span><span class="sxs-lookup"><span data-stu-id="51d79-116">Retrieves an [ErrorItem](erroritem-object.md) object if the media item has an error condition.</span></span>    |
| [<span data-ttu-id="51d79-117">имажесаурцехеигхт</span><span class="sxs-lookup"><span data-stu-id="51d79-117">imageSourceHeight</span></span>](media-imagesourceheight.md) | <span data-ttu-id="51d79-118">Извлекает высоту текущего элемента мультимедиа в пикселях.</span><span class="sxs-lookup"><span data-stu-id="51d79-118">Retrieves the height of the current media item in pixels.</span></span>                                          |
| [<span data-ttu-id="51d79-119">имажесаурцевидс</span><span class="sxs-lookup"><span data-stu-id="51d79-119">imageSourceWidth</span></span>](media-imagesourcewidth.md)   | <span data-ttu-id="51d79-120">Получает ширину текущего элемента мультимедиа в пикселях.</span><span class="sxs-lookup"><span data-stu-id="51d79-120">Retrieves the width of the current media item in pixels.</span></span>                                           |
| [<span data-ttu-id="51d79-121">маркеркаунт</span><span class="sxs-lookup"><span data-stu-id="51d79-121">markerCount</span></span>](media-markercount.md)             | <span data-ttu-id="51d79-122">Возвращает количество маркеров в элементе мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="51d79-122">Retrieves the number of markers in the media item.</span></span>                                                 |
| [<span data-ttu-id="51d79-123">name</span><span class="sxs-lookup"><span data-stu-id="51d79-123">name</span></span>](media-name.md)                           | <span data-ttu-id="51d79-124">Указывает или получает имя элемента мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="51d79-124">Specifies or retrieves the name of the media item.</span></span>                                                 |
| [<span data-ttu-id="51d79-125">саурцеурл</span><span class="sxs-lookup"><span data-stu-id="51d79-125">sourceURL</span></span>](media-sourceurl.md)                 | <span data-ttu-id="51d79-126">Извлекает URL-адрес элемента мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="51d79-126">Retrieves the URL of the media item.</span></span>                                                               |



 

<span data-ttu-id="51d79-127">Объект **мультимедиа** поддерживает следующие методы.</span><span class="sxs-lookup"><span data-stu-id="51d79-127">The **Media** object supports the following methods.</span></span>



| <span data-ttu-id="51d79-128">Метод</span><span class="sxs-lookup"><span data-stu-id="51d79-128">Method</span></span>                                                       | <span data-ttu-id="51d79-129">Описание</span><span class="sxs-lookup"><span data-stu-id="51d79-129">Description</span></span>                                                                                              |
|--------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="51d79-130">жетаттрибутекаунтбитипе</span><span class="sxs-lookup"><span data-stu-id="51d79-130">getAttributeCountByType</span></span>](media-getattributecountbytype.md) | <span data-ttu-id="51d79-131">Извлекает количество атрибутов, связанных с указанным именем атрибута и языком.</span><span class="sxs-lookup"><span data-stu-id="51d79-131">Retrieves the number of attributes associated with the specified attribute name and language.</span></span>            |
| [<span data-ttu-id="51d79-132">жетаттрибутенаме</span><span class="sxs-lookup"><span data-stu-id="51d79-132">getAttributeName</span></span>](media-getattributename.md)               | <span data-ttu-id="51d79-133">Возвращает имя атрибута, соответствующего указанному индексу.</span><span class="sxs-lookup"><span data-stu-id="51d79-133">Retrieves the name of the attribute corresponding to the specified index.</span></span>                                |
| [<span data-ttu-id="51d79-134">getItemInfo</span><span class="sxs-lookup"><span data-stu-id="51d79-134">getItemInfo</span></span>](media-getiteminfo.md)                         | <span data-ttu-id="51d79-135">Возвращает значение указанного атрибута для элемента мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="51d79-135">Retrieves the value of the specified attribute for the media item.</span></span>                                       |
| [<span data-ttu-id="51d79-136">жетитеминфобятом</span><span class="sxs-lookup"><span data-stu-id="51d79-136">getItemInfoByAtom</span></span>](media-getiteminfobyatom.md)             | <span data-ttu-id="51d79-137">Извлекает значение атрибута с указанным номером индекса.</span><span class="sxs-lookup"><span data-stu-id="51d79-137">Retrieves the value of the attribute with the specified index number.</span></span>                                    |
| [<span data-ttu-id="51d79-138">жетитеминфобитипе</span><span class="sxs-lookup"><span data-stu-id="51d79-138">getItemInfoByType</span></span>](media-getiteminfobytype.md)             | <span data-ttu-id="51d79-139">Извлекает значение атрибута, соответствующего указанному имени атрибута, языку и индексу.</span><span class="sxs-lookup"><span data-stu-id="51d79-139">Retrieves the value of the attribute corresponding to the specified attribute name, language, and index.</span></span> |
| [<span data-ttu-id="51d79-140">жетмаркернаме</span><span class="sxs-lookup"><span data-stu-id="51d79-140">getMarkerName</span></span>](media-getmarkername.md)                     | <span data-ttu-id="51d79-141">Возвращает имя маркера по указанному индексу.</span><span class="sxs-lookup"><span data-stu-id="51d79-141">Retrieves the name of the marker at the specified index.</span></span>                                                 |
| [<span data-ttu-id="51d79-142">жетмаркертиме</span><span class="sxs-lookup"><span data-stu-id="51d79-142">getMarkerTime</span></span>](media-getmarkertime.md)                     | <span data-ttu-id="51d79-143">Возвращает время маркера по указанному индексу.</span><span class="sxs-lookup"><span data-stu-id="51d79-143">Retrieves the time of the marker at the specified index.</span></span>                                                 |
| [<span data-ttu-id="51d79-144">Идентично</span><span class="sxs-lookup"><span data-stu-id="51d79-144">isIdentical</span></span>](media-isidentical.md)                         | <span data-ttu-id="51d79-145">Получает значение, указывающее, совпадает ли указанный объект с текущим объектом.</span><span class="sxs-lookup"><span data-stu-id="51d79-145">Retrieves a value indicating whether the supplied object is the same as the current one.</span></span>                 |
| [<span data-ttu-id="51d79-146">isMemberOf</span><span class="sxs-lookup"><span data-stu-id="51d79-146">isMemberOf</span></span>](media-ismemberof.md)                           | <span data-ttu-id="51d79-147">Получает значение, указывающее, является ли указанный элемент мультимедиа членом указанного списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="51d79-147">Retrieves a value indicating whether the specified media item is a member of the specified playlist.</span></span>     |
| [<span data-ttu-id="51d79-148">исреадонлитем</span><span class="sxs-lookup"><span data-stu-id="51d79-148">isReadOnlyItem</span></span>](media-isreadonlyitem.md)                   | <span data-ttu-id="51d79-149">Извлекает значение, указывающее, можно ли изменять атрибуты указанного элемента мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="51d79-149">Retrieves a value indicating whether the attributes of the specified media item can be edited.</span></span>           |
| [<span data-ttu-id="51d79-150">сетитеминфо</span><span class="sxs-lookup"><span data-stu-id="51d79-150">setItemInfo</span></span>](media-setiteminfo.md)                         | <span data-ttu-id="51d79-151">Задает значение указанного атрибута для элемента мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="51d79-151">Sets the value of the specified attribute for the media item.</span></span>                                            |



 

<span data-ttu-id="51d79-152">Доступ к объекту **мультимедиа** осуществляется с помощью следующих свойств и методов.</span><span class="sxs-lookup"><span data-stu-id="51d79-152">The **Media** object is accessed through the following properties and methods.</span></span>



| <span data-ttu-id="51d79-153">Объект</span><span class="sxs-lookup"><span data-stu-id="51d79-153">Object</span></span>                          | <span data-ttu-id="51d79-154">Свойство или метод</span><span class="sxs-lookup"><span data-stu-id="51d79-154">Property or method</span></span>                                                       |
|---------------------------------|--------------------------------------------------------------------------|
| [<span data-ttu-id="51d79-155">Элементы управления</span><span class="sxs-lookup"><span data-stu-id="51d79-155">Controls</span></span>](controls-object.md) | [<span data-ttu-id="51d79-156">currentItem</span><span class="sxs-lookup"><span data-stu-id="51d79-156">currentItem</span></span>](controls-currentitem.md)                                  |
| [<span data-ttu-id="51d79-157">Игрок</span><span class="sxs-lookup"><span data-stu-id="51d79-157">Player</span></span>](player-object.md)     | <span data-ttu-id="51d79-158">[куррентмедиа](player-currentmedia.md), [невмедиа](player-newmedia.md)</span><span class="sxs-lookup"><span data-stu-id="51d79-158">[currentMedia](player-currentmedia.md), [newMedia](player-newmedia.md)</span></span> |
| [<span data-ttu-id="51d79-159">Списком</span><span class="sxs-lookup"><span data-stu-id="51d79-159">Playlist</span></span>](playlist-object.md) | [<span data-ttu-id="51d79-160">Item</span><span class="sxs-lookup"><span data-stu-id="51d79-160">item</span></span>](playlist-item.md)                                                |



 

<span data-ttu-id="51d79-161">Так как это наиболее распространенные средства доступа, *Player*. **куррентмедиа** используется в целях иллюстрации в разделах синтаксиса Reference.</span><span class="sxs-lookup"><span data-stu-id="51d79-161">Because it is the most common means of access, *player*.**currentMedia** is used for purposes of illustration in the reference syntax sections.</span></span>

## <a name="see-also"></a><span data-ttu-id="51d79-162">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="51d79-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51d79-163">**Справочник по объектной модели для создания сценариев**</span><span class="sxs-lookup"><span data-stu-id="51d79-163">**Object Model Reference for Scripting**</span></span>](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




