---
title: Интерфейс Ивмпплайлистколлектион (VB и C) (WMP. h)
description: Предоставляет методы для управления интерфейсами Ивмпплайлист и Ивмпплайлистаррай в коллекции.
ms.assetid: 19a4e0d7-cb3f-42ec-9acb-7ac0c5837662
keywords:
- Ивмпплайлистколлектион (VB и C) интерфейс проигрывателя Windows Media
- Ивмпплайлистколлектион (VB и C) интерфейс проигрывателя Windows Media, описание
topic_type:
- apiref
api_name:
- IWMPPlaylistCollection (VB and C )
- IWMPPlaylistCollection (VB and C ).setDeleted
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ccc97f9e98838fedc3bd5441d6bfda2da5319dd6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694582"
---
# <a name="iwmpplaylistcollection-vb-and-c-interface"></a><span data-ttu-id="4bfb5-105">Интерфейс Ивмпплайлистколлектион (VB и C#)</span><span class="sxs-lookup"><span data-stu-id="4bfb5-105">IWMPPlaylistCollection (VB and C#) interface</span></span>

<span data-ttu-id="4bfb5-106">Предоставляет методы для управления интерфейсами **ивмпплайлист** и **ивмпплайлистаррай** в коллекции.</span><span class="sxs-lookup"><span data-stu-id="4bfb5-106">Provides methods for manipulating **IWMPPlaylist** and **IWMPPlaylistArray** interfaces in a collection.</span></span>

## <a name="members"></a><span data-ttu-id="4bfb5-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="4bfb5-107">Members</span></span>

<span data-ttu-id="4bfb5-108">Интерфейс **ивмпплайлистколлектион (VB и C#)** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="4bfb5-108">The **IWMPPlaylistCollection (VB and C#)** interface has these types of members:</span></span>

-   [<span data-ttu-id="4bfb5-109">Методы</span><span class="sxs-lookup"><span data-stu-id="4bfb5-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="4bfb5-110">Методы</span><span class="sxs-lookup"><span data-stu-id="4bfb5-110">Methods</span></span>

<span data-ttu-id="4bfb5-111">Интерфейс **ивмпплайлистколлектион (VB и C#)** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="4bfb5-111">The **IWMPPlaylistCollection (VB and C#)** interface has these methods.</span></span>



| <span data-ttu-id="4bfb5-112">Метод</span><span class="sxs-lookup"><span data-stu-id="4bfb5-112">Method</span></span>                                                                                                 | <span data-ttu-id="4bfb5-113">Описание</span><span class="sxs-lookup"><span data-stu-id="4bfb5-113">Description</span></span>                                                                                                                    |
|:-------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4bfb5-114">**жеталл**</span><span class="sxs-lookup"><span data-stu-id="4bfb5-114">**getAll**</span></span>](wmplibiwmpplaylistcollection-iwmpplaylistcollection-getall--vb-and-c.md)                 | <span data-ttu-id="4bfb5-115">Возвращает интерфейс **ивмпплайлистаррай** , который предоставляет доступ ко всем спискам воспроизведения в библиотеке.</span><span class="sxs-lookup"><span data-stu-id="4bfb5-115">Returns an **IWMPPlaylistArray** interface that provides access to all of the playlists in the library.</span></span><br/>             |
| [<span data-ttu-id="4bfb5-116">**жетбинаме**</span><span class="sxs-lookup"><span data-stu-id="4bfb5-116">**getByName**</span></span>](wmplibiwmpplaylistcollection-iwmpplaylistcollection-getbyname--vb-and-c.md)           | <span data-ttu-id="4bfb5-117">Возвращает интерфейс **ивмпплайлистаррай** , предоставляющий доступ к спискам воспроизведения с указанным именем, если таковые имеются.</span><span class="sxs-lookup"><span data-stu-id="4bfb5-117">Returns an **IWMPPlaylistArray** interface that provides access to playlists with the specified name, if any exist.</span></span><br/> |
| [<span data-ttu-id="4bfb5-118">**импортплайлист**</span><span class="sxs-lookup"><span data-stu-id="4bfb5-118">**importPlaylist**</span></span>](wmplibiwmpplaylistcollection-iwmpplaylistcollection-importplaylist--vb-and-c.md) | <span data-ttu-id="4bfb5-119">Добавляет статический список воспроизведения в библиотеку.</span><span class="sxs-lookup"><span data-stu-id="4bfb5-119">Adds a static playlist to the library.</span></span><br/>                                                                              |
| [<span data-ttu-id="4bfb5-120">**isDeleted**</span><span class="sxs-lookup"><span data-stu-id="4bfb5-120">**isDeleted**</span></span>](wmplibiwmpplaylistcollection-iwmpplaylistcollection-isdeleted--vb-and-c.md)           | <span data-ttu-id="4bfb5-121">Возвращает значение, указывающее, находится ли указанный список воспроизведения в папке удаленных элементов.</span><span class="sxs-lookup"><span data-stu-id="4bfb5-121">Returns a value indicating whether the specified playlist is in the deleted items folder.</span></span><br/>                           |
| [<span data-ttu-id="4bfb5-122">**невплайлист**</span><span class="sxs-lookup"><span data-stu-id="4bfb5-122">**newPlaylist**</span></span>](wmplibiwmpplaylistcollection-iwmpplaylistcollection-newplaylist--vb-and-c.md)       | <span data-ttu-id="4bfb5-123">Возвращает интерфейс **ивмпплайлист** для нового пустого списка воспроизведения в библиотеке.</span><span class="sxs-lookup"><span data-stu-id="4bfb5-123">Returns an **IWMPPlaylist** interface for a new, empty playlist in the library.</span></span><br/>                                     |
| [<span data-ttu-id="4bfb5-124">**отменит**</span><span class="sxs-lookup"><span data-stu-id="4bfb5-124">**remove**</span></span>](wmplibiwmpplaylistcollection-iwmpplaylistcollection-remove--vb-and-c.md)                 | <span data-ttu-id="4bfb5-125">Удаляет список воспроизведения из библиотеки.</span><span class="sxs-lookup"><span data-stu-id="4bfb5-125">Removes a playlist from the library.</span></span><br/>                                                                                |
| <span data-ttu-id="4bfb5-126">**сетделетед**</span><span class="sxs-lookup"><span data-stu-id="4bfb5-126">**setDeleted**</span></span>                                                                                         | <span data-ttu-id="4bfb5-127">Больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="4bfb5-127">No longer supported.</span></span><br/>                                                                                                |



 

<span data-ttu-id="4bfb5-128">Получите интерфейс **ивмпплайлистколлектион** с помощью следующего свойства.</span><span class="sxs-lookup"><span data-stu-id="4bfb5-128">Get an **IWMPPlaylistCollection** interface by using the following property.</span></span>



| <span data-ttu-id="4bfb5-129">Объект</span><span class="sxs-lookup"><span data-stu-id="4bfb5-129">Object</span></span>                                                                   | <span data-ttu-id="4bfb5-130">Свойство</span><span class="sxs-lookup"><span data-stu-id="4bfb5-130">Property</span></span>                                                                                 |
|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4bfb5-131">Объект Аксвиндовсмедиаплайер</span><span class="sxs-lookup"><span data-stu-id="4bfb5-131">AxWindowsMediaPlayer Object</span></span>](axwindowsmediaplayer-object--vb-and-c.md) | [<span data-ttu-id="4bfb5-132">**плайлистколлектион**</span><span class="sxs-lookup"><span data-stu-id="4bfb5-132">**playlistCollection**</span></span>](axwmplib-axwindowsmediaplayer-playlistcollection--vb-and-c.md) |



 

## <a name="requirements"></a><span data-ttu-id="4bfb5-133">Требования</span><span class="sxs-lookup"><span data-stu-id="4bfb5-133">Requirements</span></span>



| <span data-ttu-id="4bfb5-134">Требование</span><span class="sxs-lookup"><span data-stu-id="4bfb5-134">Requirement</span></span> | <span data-ttu-id="4bfb5-135">Значение</span><span class="sxs-lookup"><span data-stu-id="4bfb5-135">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="4bfb5-136">Header</span><span class="sxs-lookup"><span data-stu-id="4bfb5-136">Header</span></span><br/> | <dl> <span data-ttu-id="4bfb5-137"><dt>WMP. h</dt></span><span class="sxs-lookup"><span data-stu-id="4bfb5-137"><dt>Wmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4bfb5-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4bfb5-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4bfb5-139">**Интерфейсы для Visual Basic .NET и C #**</span><span class="sxs-lookup"><span data-stu-id="4bfb5-139">**Interfaces for Visual Basic .NET and C#**</span></span>](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[<span data-ttu-id="4bfb5-140">**Интерфейс Ивмпплайлист (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="4bfb5-140">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="4bfb5-141">**Интерфейс Ивмпплайлистаррай (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="4bfb5-141">**IWMPPlaylistArray Interface (VB and C#)**</span></span>](iwmpplaylistarray--vb-and-c.md)
</dt> </dl>

 

 





