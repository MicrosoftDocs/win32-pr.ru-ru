---
title: Интерфейс IWMPMedia2 (VB и C) (WMP. h)
description: Предоставляет доступ к дополнительному свойству элемента мультимедиа.
ms.assetid: 7d9f8304-ae26-4175-b9d4-9f272861ef87
keywords:
- IWMPMedia2 (VB и C) интерфейс проигрывателя Windows Media
- IWMPMedia2 (VB и C) интерфейс проигрывателя Windows Media, описание
topic_type:
- apiref
api_name:
- IWMPMedia2 (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb1a77322e0e6649d9a286c920ccd9ddc77890f3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685099"
---
# <a name="iwmpmedia2-vb-and-c-interface"></a><span data-ttu-id="dc3e8-105">Интерфейс IWMPMedia2 (VB и C#)</span><span class="sxs-lookup"><span data-stu-id="dc3e8-105">IWMPMedia2 (VB and C#) interface</span></span>

<span data-ttu-id="dc3e8-106">Предоставляет доступ к дополнительному свойству элемента мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="dc3e8-106">Provides access to an additional media item property.</span></span>

<span data-ttu-id="dc3e8-107">В дополнение к свойствам и методам, унаследованным от **ивмпмедиа**, интерфейс **IWMPMedia2** предоставляет следующее свойство.</span><span class="sxs-lookup"><span data-stu-id="dc3e8-107">In addition to the properties and methods inherited from **IWMPMedia**, the **IWMPMedia2** interface exposes the following property.</span></span>



| <span data-ttu-id="dc3e8-108">Свойство</span><span class="sxs-lookup"><span data-stu-id="dc3e8-108">Property</span></span>                                                 | <span data-ttu-id="dc3e8-109">Описание</span><span class="sxs-lookup"><span data-stu-id="dc3e8-109">Description</span></span>                                                                   |
|----------------------------------------------------------|-------------------------------------------------------------------------------|
| [<span data-ttu-id="dc3e8-110">Ошибка</span><span class="sxs-lookup"><span data-stu-id="dc3e8-110">Error</span></span>](wmplibiwmpmedia2-iwmpmedia2-error--vb-and-c.md) | <span data-ttu-id="dc3e8-111">Возвращает интерфейс **ивмперроритем** , если в элементе мультимедиа есть условие ошибки.</span><span class="sxs-lookup"><span data-stu-id="dc3e8-111">Gets an **IWMPErrorItem** interface if the media item has an error condition.</span></span> |



 

<span data-ttu-id="dc3e8-112">Получите интерфейс **IWMPMedia2** путем приведения значения, возвращаемого одним из следующих свойств или методов, доступ к которым осуществляется через следующий объект или интерфейс.</span><span class="sxs-lookup"><span data-stu-id="dc3e8-112">Get an **IWMPMedia2** interface by casting the value returned by one of the following properties or methods accessed through the following object or interface.</span></span>



| <span data-ttu-id="dc3e8-113">Объект или интерфейс</span><span class="sxs-lookup"><span data-stu-id="dc3e8-113">Object or interface</span></span>                                               | <span data-ttu-id="dc3e8-114">Свойство или метод</span><span class="sxs-lookup"><span data-stu-id="dc3e8-114">Property or method</span></span>                                                                                                                |
|-------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dc3e8-115">ивмпконтролс</span><span class="sxs-lookup"><span data-stu-id="dc3e8-115">IWMPControls</span></span>](iwmpcontrols--vb-and-c.md)                        | [<span data-ttu-id="dc3e8-116">currentItem</span><span class="sxs-lookup"><span data-stu-id="dc3e8-116">currentItem</span></span>](wmplibiwmpcontrols-iwmpcontrols-currentitem--vb-and-c.md)                                                          |
| [<span data-ttu-id="dc3e8-117">аксвиндовсмедиаплайер</span><span class="sxs-lookup"><span data-stu-id="dc3e8-117">AxWindowsMediaPlayer</span></span>](axwindowsmediaplayer-object--vb-and-c.md) | <span data-ttu-id="dc3e8-118">[куррентмедиа](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md) , [невмедиа](axwmplib-axwindowsmediaplayer-newmedia.md)</span><span class="sxs-lookup"><span data-stu-id="dc3e8-118">[currentMedia](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md) , [newMedia](axwmplib-axwindowsmediaplayer-newmedia.md)</span></span> |
| [<span data-ttu-id="dc3e8-119">ивмпплайлист</span><span class="sxs-lookup"><span data-stu-id="dc3e8-119">IWMPPlaylist</span></span>](iwmpplaylist--vb-and-c.md)                        | <span data-ttu-id="dc3e8-120">[Item](iwmpplaylist-item--vb-and-c.md) ( **Получение \_ элемента** в C#)</span><span class="sxs-lookup"><span data-stu-id="dc3e8-120">[Item](iwmpplaylist-item--vb-and-c.md) ( **get\_Item** in C#)</span></span>                                                                   |



 

## <a name="members"></a><span data-ttu-id="dc3e8-121">Элементы</span><span class="sxs-lookup"><span data-stu-id="dc3e8-121">Members</span></span>

<span data-ttu-id="dc3e8-122">Интерфейс **IWMPMedia2 (VB и C#)** не определяет никаких членов.</span><span class="sxs-lookup"><span data-stu-id="dc3e8-122">The **IWMPMedia2 (VB and C#)** interface does not define any members.</span></span>

## <a name="requirements"></a><span data-ttu-id="dc3e8-123">Требования</span><span class="sxs-lookup"><span data-stu-id="dc3e8-123">Requirements</span></span>



| <span data-ttu-id="dc3e8-124">Требование</span><span class="sxs-lookup"><span data-stu-id="dc3e8-124">Requirement</span></span> | <span data-ttu-id="dc3e8-125">Значение</span><span class="sxs-lookup"><span data-stu-id="dc3e8-125">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="dc3e8-126">Header</span><span class="sxs-lookup"><span data-stu-id="dc3e8-126">Header</span></span><br/> | <dl> <span data-ttu-id="dc3e8-127"><dt>WMP. h</dt></span><span class="sxs-lookup"><span data-stu-id="dc3e8-127"><dt>Wmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc3e8-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dc3e8-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc3e8-129">**Интерфейсы для Visual Basic .NET и C #**</span><span class="sxs-lookup"><span data-stu-id="dc3e8-129">**Interfaces for Visual Basic .NET and C#**</span></span>](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[<span data-ttu-id="dc3e8-130">**Ивмперроритем (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="dc3e8-130">**IWMPErrorItem (VB and C#)**</span></span>](iwmperroritem--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="dc3e8-131">**Интерфейс Ивмпмедиа (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="dc3e8-131">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="dc3e8-132">**Интерфейс IWMPMedia3 (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="dc3e8-132">**IWMPMedia3 Interface (VB and C#)**</span></span>](iwmpmedia3--vb-and-c.md)
</dt> </dl>

 

 





