---
description: В \_ \_ \_ перечислении флагов поиска декстерф Track указываются граничные условия для поиска объекта на временной шкале.
ms.assetid: 9a66ea17-5c2c-41fd-8a7b-c9918b10c8c9
title: Перечисление DEXTERF_TRACK_SEARCH_FLAGS (Кедит. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DEXTERF_TRACK_SEARCH_FLAGS
api_type:
- HeaderDef
api_location:
- Qedit.h
ms.openlocfilehash: 09923d6be01bdf4a213db645a34b038dda15d86f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105652093"
---
# <a name="dexterf_track_search_flags-enumeration"></a><span data-ttu-id="580f3-103">\_ \_ \_ Перечисление флагов поиска декстерф Track</span><span class="sxs-lookup"><span data-stu-id="580f3-103">DEXTERF\_TRACK\_SEARCH\_FLAGS enumeration</span></span>

> [!Note]  
> <span data-ttu-id="580f3-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="580f3-104">\[Deprecated.</span></span> <span data-ttu-id="580f3-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="580f3-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="580f3-106">`DEXTERF_TRACK_SEARCH_FLAGS`Перечисление задает граничные условия для поиска объекта на временной шкале.</span><span class="sxs-lookup"><span data-stu-id="580f3-106">The `DEXTERF_TRACK_SEARCH_FLAGS` enumeration specifies the boundary conditions on a search for an object in the timeline.</span></span>

## <a name="syntax"></a><span data-ttu-id="580f3-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="580f3-107">Syntax</span></span>


```C++
typedef enum  { 
  DEXTERF_BOUNDING    = -1,
  DEXTERF_EXACTLY_AT  = 0,
  DEXTERF_FORWARDS    = 1
} DEXTERF_TRACK_SEARCH_FLAGS;
```



## <a name="constants"></a><span data-ttu-id="580f3-108">Константы</span><span class="sxs-lookup"><span data-stu-id="580f3-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="580f3-109"><span id="DEXTERF_BOUNDING"></span><span id="dexterf_bounding"></span>**ДЕКСТЕРФное \_ ограничение**</span><span class="sxs-lookup"><span data-stu-id="580f3-109"><span id="DEXTERF_BOUNDING"></span><span id="dexterf_bounding"></span>**DEXTERF\_BOUNDING**</span></span>
</dt> <dd>

<span data-ttu-id="580f3-110">Поиск объекта, охватывающего указанное время.</span><span class="sxs-lookup"><span data-stu-id="580f3-110">Search for an object that spans the specified time.</span></span>

</dd> <dt>

<span data-ttu-id="580f3-111"><span id="DEXTERF_EXACTLY_AT"></span><span id="dexterf_exactly_at"></span>**ДЕКСТЕРФ \_ \_ в точности**</span><span class="sxs-lookup"><span data-stu-id="580f3-111"><span id="DEXTERF_EXACTLY_AT"></span><span id="dexterf_exactly_at"></span>**DEXTERF\_EXACTLY\_AT**</span></span>
</dt> <dd>

<span data-ttu-id="580f3-112">Поиск объекта, который запускается точно в указанное время.</span><span class="sxs-lookup"><span data-stu-id="580f3-112">Search for an object that starts exactly at the specified time.</span></span>

</dd> <dt>

<span data-ttu-id="580f3-113"><span id="DEXTERF_FORWARDS"></span><span id="dexterf_forwards"></span>**Пересылка ДЕКСТЕРФ \_**</span><span class="sxs-lookup"><span data-stu-id="580f3-113"><span id="DEXTERF_FORWARDS"></span><span id="dexterf_forwards"></span>**DEXTERF\_FORWARDS**</span></span>
</dt> <dd>

<span data-ttu-id="580f3-114">Поиск объекта, запускаемого в указанное время или позже.</span><span class="sxs-lookup"><span data-stu-id="580f3-114">Search for an object that starts at the specified time or later.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="580f3-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="580f3-115">Remarks</span></span>

<span data-ttu-id="580f3-116">Эти условия границ приведены в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="580f3-116">These boundary conditions are summarized in the following table.</span></span>



| <span data-ttu-id="580f3-117">Значение перечисления</span><span class="sxs-lookup"><span data-stu-id="580f3-117">Enumeration value</span></span>    | <span data-ttu-id="580f3-118">Условие границы</span><span class="sxs-lookup"><span data-stu-id="580f3-118">Boundary condition</span></span>                        |
|----------------------|-------------------------------------------|
| <span data-ttu-id="580f3-119">ДЕКСТЕРФное \_ ограничение</span><span class="sxs-lookup"><span data-stu-id="580f3-119">DEXTERF\_BOUNDING</span></span>    | <span data-ttu-id="580f3-120"><запуска = время > Тиместоп</span><span class="sxs-lookup"><span data-stu-id="580f3-120">Start <= TimeStop > Time</span></span><br/> |
| <span data-ttu-id="580f3-121">ДЕКСТЕРФ \_ \_ в точности</span><span class="sxs-lookup"><span data-stu-id="580f3-121">DEXTERF\_EXACTLY\_AT</span></span> | <span data-ttu-id="580f3-122">Начало = = время</span><span class="sxs-lookup"><span data-stu-id="580f3-122">Start == Time</span></span>                             |
| <span data-ttu-id="580f3-123">Пересылка ДЕКСТЕРФ \_</span><span class="sxs-lookup"><span data-stu-id="580f3-123">DEXTERF\_FORWARDS</span></span>    | <span data-ttu-id="580f3-124">>запуска = время</span><span class="sxs-lookup"><span data-stu-id="580f3-124">Start >= Time</span></span>                          |



 

-   <span data-ttu-id="580f3-125">Начало: время начала полученного объекта.</span><span class="sxs-lookup"><span data-stu-id="580f3-125">Start: start time of the retrieved object.</span></span>
-   <span data-ttu-id="580f3-126">Прерывать: время окончания полученного объекта.</span><span class="sxs-lookup"><span data-stu-id="580f3-126">Stop: stop time of the retrieved object.</span></span>
-   <span data-ttu-id="580f3-127">Время: указанное время поиска.</span><span class="sxs-lookup"><span data-stu-id="580f3-127">Time: specified search time.</span></span>

## <a name="requirements"></a><span data-ttu-id="580f3-128">Требования</span><span class="sxs-lookup"><span data-stu-id="580f3-128">Requirements</span></span>



| <span data-ttu-id="580f3-129">Требование</span><span class="sxs-lookup"><span data-stu-id="580f3-129">Requirement</span></span> | <span data-ttu-id="580f3-130">Значение</span><span class="sxs-lookup"><span data-stu-id="580f3-130">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="580f3-131">Header</span><span class="sxs-lookup"><span data-stu-id="580f3-131">Header</span></span><br/> | <dl> <span data-ttu-id="580f3-132"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="580f3-132"><dt>Qedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="580f3-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="580f3-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="580f3-134">**Иамтимелинетракк:: Жетсркаттиме**</span><span class="sxs-lookup"><span data-stu-id="580f3-134">**IAMTimelineTrack::GetSrcAtTime**</span></span>](iamtimelinetrack-getsrcattime.md)
</dt> </dl>

 

 




