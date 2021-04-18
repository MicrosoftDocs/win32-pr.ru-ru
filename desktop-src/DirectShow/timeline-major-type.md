---
description: '\_Перечисление основных типов временной шкалы \_ задает основной тип объекта.'
ms.assetid: 1a5fde83-2a0a-4bcf-bffe-340a9d914885
title: Перечисление TIMELINE_MAJOR_TYPE (Кедит. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TIMELINE_MAJOR_TYPE
api_type:
- HeaderDef
api_location:
- Qedit.h
ms.openlocfilehash: 25c3e829aa73d1da78c110ffd148fb0ebaaebdd9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685213"
---
# <a name="timeline_major_type-enumeration"></a><span data-ttu-id="22be0-103">\_Перечисление основных типов временной шкалы \_</span><span class="sxs-lookup"><span data-stu-id="22be0-103">TIMELINE\_MAJOR\_TYPE enumeration</span></span>

> [!Note]  
> <span data-ttu-id="22be0-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="22be0-104">\[Deprecated.</span></span> <span data-ttu-id="22be0-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="22be0-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="22be0-106">`TIMELINE_MAJOR_TYPE`Перечисление указывает основной тип объекта.</span><span class="sxs-lookup"><span data-stu-id="22be0-106">The `TIMELINE_MAJOR_TYPE` enumeration specifies the major type of an object.</span></span>

## <a name="syntax"></a><span data-ttu-id="22be0-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="22be0-107">Syntax</span></span>


```C++
typedef enum  { 
  TIMELINE_MAJOR_TYPE_COMPOSITE   = 1,
  TIMELINE_MAJOR_TYPE_TRACK       = 2,
  TIMELINE_MAJOR_TYPE_SOURCE      = 4,
  TIMELINE_MAJOR_TYPE_TRANSITION  = 8,
  TIMELINE_MAJOR_TYPE_EFFECT      = 16,
  TIMELINE_MAJOR_TYPE_GROUP       = 128
} TIMELINE_MAJOR_TYPE;
```



## <a name="constants"></a><span data-ttu-id="22be0-108">Константы</span><span class="sxs-lookup"><span data-stu-id="22be0-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="22be0-109"><span id="TIMELINE_MAJOR_TYPE_COMPOSITE"></span><span id="timeline_major_type_composite"></span>**\_ \_ составной основной тип временной шкалы \_**</span><span class="sxs-lookup"><span data-stu-id="22be0-109"><span id="TIMELINE_MAJOR_TYPE_COMPOSITE"></span><span id="timeline_major_type_composite"></span>**TIMELINE\_MAJOR\_TYPE\_COMPOSITE**</span></span>
</dt> <dd>

<span data-ttu-id="22be0-110">Составной объект.</span><span class="sxs-lookup"><span data-stu-id="22be0-110">Composite object.</span></span> <span data-ttu-id="22be0-111">Содержит одну или несколько дорожек.</span><span class="sxs-lookup"><span data-stu-id="22be0-111">Holds one or more tracks.</span></span>

</dd> <dt>

<span data-ttu-id="22be0-112"><span id="TIMELINE_MAJOR_TYPE_TRACK"></span><span id="timeline_major_type_track"></span>**\_Основная \_ запись типа \_ временной шкалы**</span><span class="sxs-lookup"><span data-stu-id="22be0-112"><span id="TIMELINE_MAJOR_TYPE_TRACK"></span><span id="timeline_major_type_track"></span>**TIMELINE\_MAJOR\_TYPE\_TRACK**</span></span>
</dt> <dd>

<span data-ttu-id="22be0-113">Объект Track.</span><span class="sxs-lookup"><span data-stu-id="22be0-113">Track object.</span></span> <span data-ttu-id="22be0-114">Содержит один или несколько источников.</span><span class="sxs-lookup"><span data-stu-id="22be0-114">Holds one or more sources.</span></span>

</dd> <dt>

<span data-ttu-id="22be0-115"><span id="TIMELINE_MAJOR_TYPE_SOURCE"></span><span id="timeline_major_type_source"></span>**\_источник основных \_ типов временной шкалы \_**</span><span class="sxs-lookup"><span data-stu-id="22be0-115"><span id="TIMELINE_MAJOR_TYPE_SOURCE"></span><span id="timeline_major_type_source"></span>**TIMELINE\_MAJOR\_TYPE\_SOURCE**</span></span>
</dt> <dd>

<span data-ttu-id="22be0-116">Исходный объект.</span><span class="sxs-lookup"><span data-stu-id="22be0-116">Source object.</span></span> <span data-ttu-id="22be0-117">Содержит ссылку на источник мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="22be0-117">Contains a reference to a media source.</span></span>

</dd> <dt>

<span data-ttu-id="22be0-118"><span id="TIMELINE_MAJOR_TYPE_TRANSITION"></span><span id="timeline_major_type_transition"></span>**\_Переход на основной \_ тип \_ временной шкалы**</span><span class="sxs-lookup"><span data-stu-id="22be0-118"><span id="TIMELINE_MAJOR_TYPE_TRANSITION"></span><span id="timeline_major_type_transition"></span>**TIMELINE\_MAJOR\_TYPE\_TRANSITION**</span></span>
</dt> <dd>

<span data-ttu-id="22be0-119">Объект перехода.</span><span class="sxs-lookup"><span data-stu-id="22be0-119">Transition object.</span></span> <span data-ttu-id="22be0-120">Определяет переход между составными элементами, дорожками или источниками.</span><span class="sxs-lookup"><span data-stu-id="22be0-120">Defines a transition between composites, tracks, or sources.</span></span>

</dd> <dt>

<span data-ttu-id="22be0-121"><span id="TIMELINE_MAJOR_TYPE_EFFECT"></span><span id="timeline_major_type_effect"></span>**\_результат основного \_ типа временной шкалы \_**</span><span class="sxs-lookup"><span data-stu-id="22be0-121"><span id="TIMELINE_MAJOR_TYPE_EFFECT"></span><span id="timeline_major_type_effect"></span>**TIMELINE\_MAJOR\_TYPE\_EFFECT**</span></span>
</dt> <dd>

<span data-ttu-id="22be0-122">Объект Effect.</span><span class="sxs-lookup"><span data-stu-id="22be0-122">Effect object.</span></span> <span data-ttu-id="22be0-123">Определяет однонаправленный результат, применяемый к составному, отслеживающему или исходному объекту.</span><span class="sxs-lookup"><span data-stu-id="22be0-123">Defines a single-input effect to be applied to a composite, track, or source object.</span></span>

</dd> <dt>

<span data-ttu-id="22be0-124"><span id="TIMELINE_MAJOR_TYPE_GROUP"></span><span id="timeline_major_type_group"></span>**\_Основная \_ группа типов \_ временной шкалы**</span><span class="sxs-lookup"><span data-stu-id="22be0-124"><span id="TIMELINE_MAJOR_TYPE_GROUP"></span><span id="timeline_major_type_group"></span>**TIMELINE\_MAJOR\_TYPE\_GROUP**</span></span>
</dt> <dd>

<span data-ttu-id="22be0-125">Объект группы.</span><span class="sxs-lookup"><span data-stu-id="22be0-125">Group object.</span></span> <span data-ttu-id="22be0-126">Содержит одну или несколько дорожек заданного типа.</span><span class="sxs-lookup"><span data-stu-id="22be0-126">Contains one or more tracks of a given type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="22be0-127">Требования</span><span class="sxs-lookup"><span data-stu-id="22be0-127">Requirements</span></span>



| <span data-ttu-id="22be0-128">Требование</span><span class="sxs-lookup"><span data-stu-id="22be0-128">Requirement</span></span> | <span data-ttu-id="22be0-129">Значение</span><span class="sxs-lookup"><span data-stu-id="22be0-129">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="22be0-130">Header</span><span class="sxs-lookup"><span data-stu-id="22be0-130">Header</span></span><br/> | <dl> <span data-ttu-id="22be0-131"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="22be0-131"><dt>Qedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22be0-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="22be0-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22be0-133">**иамтимелине**</span><span class="sxs-lookup"><span data-stu-id="22be0-133">**IAMTimeline**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="22be0-134">**Иамтимелинекомп:: Жеткаунтофтипе**</span><span class="sxs-lookup"><span data-stu-id="22be0-134">**IAMTimelineComp::GetCountOfType**</span></span>](iamtimelinecomp-getcountoftype.md)
</dt> <dt>

[<span data-ttu-id="22be0-135">**Иамтимелинеобж:: Жеттимелинетипе**</span><span class="sxs-lookup"><span data-stu-id="22be0-135">**IAMTimelineObj::GetTimelineType**</span></span>](iamtimelineobj-gettimelinetype.md)
</dt> </dl>

 

 




