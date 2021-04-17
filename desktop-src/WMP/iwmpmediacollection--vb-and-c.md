---
title: Интерфейс Ивмпмедиаколлектион (VB и C) (WMP. h)
description: Предоставляет методы, которые можно использовать для Организации большой коллекции элементов мультимедиа.
ms.assetid: a9e3d466-7dcf-4f1b-ba6f-9d166a35f03d
keywords:
- Ивмпмедиаколлектион (VB и C) интерфейс проигрывателя Windows Media
- Ивмпмедиаколлектион (VB и C) интерфейс проигрывателя Windows Media, описание
topic_type:
- apiref
api_name:
- IWMPMediaCollection (VB and C )
- IWMPMediaCollection (VB and C ).isDeleted
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 424fd45b1fd3d02000a9774ffe75ec87e52dd9c5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689508"
---
# <a name="iwmpmediacollection-vb-and-c-interface"></a><span data-ttu-id="56df6-105">Интерфейс Ивмпмедиаколлектион (VB и C#)</span><span class="sxs-lookup"><span data-stu-id="56df6-105">IWMPMediaCollection (VB and C#) interface</span></span>

<span data-ttu-id="56df6-106">Предоставляет методы, которые можно использовать для Организации большой коллекции элементов мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="56df6-106">Provides methods that can be used to organize a large collection of media items.</span></span>

## <a name="members"></a><span data-ttu-id="56df6-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="56df6-107">Members</span></span>

<span data-ttu-id="56df6-108">Интерфейс **ивмпмедиаколлектион (VB и C#)** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="56df6-108">The **IWMPMediaCollection (VB and C#)** interface has these types of members:</span></span>

-   [<span data-ttu-id="56df6-109">Методы</span><span class="sxs-lookup"><span data-stu-id="56df6-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="56df6-110">Методы</span><span class="sxs-lookup"><span data-stu-id="56df6-110">Methods</span></span>

<span data-ttu-id="56df6-111">Интерфейс **ивмпмедиаколлектион (VB и C#)** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="56df6-111">The **IWMPMediaCollection (VB and C#)** interface has these methods.</span></span>



| <span data-ttu-id="56df6-112">Метод</span><span class="sxs-lookup"><span data-stu-id="56df6-112">Method</span></span>                                                                                                                       | <span data-ttu-id="56df6-113">Описание</span><span class="sxs-lookup"><span data-stu-id="56df6-113">Description</span></span>                                                                                                                                   |
|:-----------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="56df6-114">**add**</span><span class="sxs-lookup"><span data-stu-id="56df6-114">**add**</span></span>](wmplibiwmpmediacollection-iwmpmediacollection-add--vb-and-c.md)                                                   | <span data-ttu-id="56df6-115">Добавляет новый элемент мультимедиа или список воспроизведения в библиотеку.</span><span class="sxs-lookup"><span data-stu-id="56df6-115">Adds a new media item or playlist to the library.</span></span><br/>                                                                                  |
| [<span data-ttu-id="56df6-116">**жеталл**</span><span class="sxs-lookup"><span data-stu-id="56df6-116">**getAll**</span></span>](wmplibiwmpmediacollection-iwmpmediacollection-getall--vb-and-c.md)                                             | <span data-ttu-id="56df6-117">Возвращает интерфейс **ивмпплайлист** , соответствующий списку воспроизведения, содержащему все элементы мультимедиа в библиотеке.</span><span class="sxs-lookup"><span data-stu-id="56df6-117">Returns an **IWMPPlaylist** interface that corresponds to the playlist that contains all media items in the library.</span></span><br/>               |
| [<span data-ttu-id="56df6-118">**жетаттрибутестрингколлектион**</span><span class="sxs-lookup"><span data-stu-id="56df6-118">**getAttributeStringCollection**</span></span>](wmplibiwmpmediacollection-iwmpmediacollection-getattributestringcollection--vb-and-c.md) | <span data-ttu-id="56df6-119">Возвращает интерфейс **ивмпстрингколлектион** , представляющий набор всех значений для указанного атрибута в типе мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="56df6-119">Returns an **IWMPStringCollection** interface that represents the set of all values for a specified attribute within a media type.</span></span><br/> |
| [<span data-ttu-id="56df6-120">**жетбялбум**</span><span class="sxs-lookup"><span data-stu-id="56df6-120">**getByAlbum**</span></span>](wmplibiwmpmediacollection-iwmpmediacollection-getbyalbum--vb-and-c.md)                                     | <span data-ttu-id="56df6-121">Возвращает интерфейс **ивмпплайлист** , предоставляющий доступ к элементам мультимедиа из указанного альбома.</span><span class="sxs-lookup"><span data-stu-id="56df6-121">Returns an **IWMPPlaylist** interface that provides access to media items from the specified album.</span></span><br/>                                |
| [<span data-ttu-id="56df6-122">**жетбяттрибуте**</span><span class="sxs-lookup"><span data-stu-id="56df6-122">**getByAttribute**</span></span>](wmplibiwmpmediacollection-iwmpmediacollection-getbyattribute--vb-and-c.md)                             | <span data-ttu-id="56df6-123">Возвращает интерфейс **ивмпплайлист** , соответствующий указанному атрибуту, имеющему указанное значение.</span><span class="sxs-lookup"><span data-stu-id="56df6-123">Returns an **IWMPPlaylist** interface that corresponds to the specified attribute having the specified value.</span></span><br/>                      |
| [<span data-ttu-id="56df6-124">**жетбяусор**</span><span class="sxs-lookup"><span data-stu-id="56df6-124">**getByAuthor**</span></span>](wmplibiwmpmediacollection-iwmpmediacollection-getbyauthor--vb-and-c.md)                                   | <span data-ttu-id="56df6-125">Возвращает интерфейс **ивмпплайлист** , предоставляющий доступ к элементам мультимедиа по указанному автору.</span><span class="sxs-lookup"><span data-stu-id="56df6-125">Returns an **IWMPPlaylist** interface that provides access to the media items by the specified author.</span></span><br/>                             |
| [<span data-ttu-id="56df6-126">**жетбиженре**</span><span class="sxs-lookup"><span data-stu-id="56df6-126">**getByGenre**</span></span>](wmplibiwmpmediacollection-iwmpmediacollection-getbygenre--vb-and-c.md)                                     | <span data-ttu-id="56df6-127">Возвращает интерфейс **ивмпплайлист** , предоставляющий доступ к элементам мультимедиа указанного жанра.</span><span class="sxs-lookup"><span data-stu-id="56df6-127">Returns an **IWMPPlaylist** interface that provides access to media items of the specified genre.</span></span><br/>                                  |
| [<span data-ttu-id="56df6-128">**жетбинаме**</span><span class="sxs-lookup"><span data-stu-id="56df6-128">**getByName**</span></span>](wmplibiwmpmediacollection-iwmpmediacollection-getbyname--vb-and-c.md)                                       | <span data-ttu-id="56df6-129">Возвращает интерфейс **ивмпплайлист** , предоставляющий доступ к элементам мультимедиа с указанным именем.</span><span class="sxs-lookup"><span data-stu-id="56df6-129">Returns an **IWMPPlaylist** interface that provides access to media items with the specified name.</span></span><br/>                                 |
| [<span data-ttu-id="56df6-130">**жетмедиаатом**</span><span class="sxs-lookup"><span data-stu-id="56df6-130">**getMediaAtom**</span></span>](wmplibiwmpmediacollection-iwmpmediacollection-getmediaatom--vb-and-c.md)                                 | <span data-ttu-id="56df6-131">Возвращает индекс указанного атрибута.</span><span class="sxs-lookup"><span data-stu-id="56df6-131">Returns the index of a specified attribute.</span></span><br/>                                                                                        |
| <span data-ttu-id="56df6-132">**isDeleted**</span><span class="sxs-lookup"><span data-stu-id="56df6-132">**isDeleted**</span></span>                                                                                                                | <span data-ttu-id="56df6-133">Больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="56df6-133">No longer supported.</span></span><br/>                                                                                                               |
| [<span data-ttu-id="56df6-134">**отменит**</span><span class="sxs-lookup"><span data-stu-id="56df6-134">**remove**</span></span>](wmplibiwmpmediacollection-iwmpmediacollection-remove--vb-and-c.md)                                             | <span data-ttu-id="56df6-135">Удаляет указанный элемент мультимедиа из коллекции носителей.</span><span class="sxs-lookup"><span data-stu-id="56df6-135">Removes the specified media item from the media collection.</span></span><br/>                                                                        |
| [<span data-ttu-id="56df6-136">**сетделетед**</span><span class="sxs-lookup"><span data-stu-id="56df6-136">**setDeleted**</span></span>](wmplibiwmpmediacollection-iwmpmediacollection-setdeleted--vb-and-c.md)                                     | <span data-ttu-id="56df6-137">Перемещает указанный элемент мультимедиа в папку Удаленные элементы.</span><span class="sxs-lookup"><span data-stu-id="56df6-137">Moves the specified media item to the deleted items folder.</span></span><br/>                                                                        |



 

<span data-ttu-id="56df6-138">Получите интерфейс **ивмпмедиаколлектион** , используя следующие свойства, доступ к которым осуществляется через следующий объект или интерфейс.</span><span class="sxs-lookup"><span data-stu-id="56df6-138">Get an **IWMPMediaCollection** interface by using the following properties accessed through the following object or interface.</span></span>



| <span data-ttu-id="56df6-139">Объект или интерфейс</span><span class="sxs-lookup"><span data-stu-id="56df6-139">Object or interface</span></span>                                               | <span data-ttu-id="56df6-140">Свойство</span><span class="sxs-lookup"><span data-stu-id="56df6-140">Property</span></span>                                                                           |
|-------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="56df6-141">аксвиндовсмедиаплайер</span><span class="sxs-lookup"><span data-stu-id="56df6-141">AxWindowsMediaPlayer</span></span>](axwindowsmediaplayer-object--vb-and-c.md) | [<span data-ttu-id="56df6-142">**медиаколлектион**</span><span class="sxs-lookup"><span data-stu-id="56df6-142">**mediaCollection**</span></span>](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md) |
| [<span data-ttu-id="56df6-143">**ивмплибрари**</span><span class="sxs-lookup"><span data-stu-id="56df6-143">**IWMPLibrary**</span></span>](iwmplibrary--vb-and-c.md)                      | [<span data-ttu-id="56df6-144">**медиаколлектион**</span><span class="sxs-lookup"><span data-stu-id="56df6-144">**mediaCollection**</span></span>](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md) |



 

## <a name="requirements"></a><span data-ttu-id="56df6-145">Требования</span><span class="sxs-lookup"><span data-stu-id="56df6-145">Requirements</span></span>



| <span data-ttu-id="56df6-146">Требование</span><span class="sxs-lookup"><span data-stu-id="56df6-146">Requirement</span></span> | <span data-ttu-id="56df6-147">Значение</span><span class="sxs-lookup"><span data-stu-id="56df6-147">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="56df6-148">Header</span><span class="sxs-lookup"><span data-stu-id="56df6-148">Header</span></span><br/> | <dl> <span data-ttu-id="56df6-149"><dt>WMP. h</dt></span><span class="sxs-lookup"><span data-stu-id="56df6-149"><dt>Wmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56df6-150">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="56df6-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56df6-151">**Интерфейсы для Visual Basic .NET и C #**</span><span class="sxs-lookup"><span data-stu-id="56df6-151">**Interfaces for Visual Basic .NET and C#**</span></span>](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[<span data-ttu-id="56df6-152">**Интерфейс IWMPMediaCollection2**</span><span class="sxs-lookup"><span data-stu-id="56df6-152">**IWMPMediaCollection2 Interface**</span></span>](iwmpmediacollection2--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="56df6-153">**Интерфейс Ивмпплайлист (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="56df6-153">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="56df6-154">**Интерфейс Ивмпстрингколлектион (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="56df6-154">**IWMPStringCollection Interface (VB and C#)**</span></span>](iwmpstringcollection--vb-and-c.md)
</dt> </dl>

 

 





