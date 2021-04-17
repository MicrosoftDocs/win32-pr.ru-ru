---
description: Структура КУЕРИТАБЛЕ предоставляет список компьютеров, которые в настоящее время используют сетевой монитор для записи сетевых данных.
ms.assetid: b701a6d5-df6d-4ee9-b008-a568a410dc14
title: Структура КУЕРИТАБЛЕ (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- QUERYTABLE
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 2b2976a56b43c55fccb9acb0c593b0dfd37e4404
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673591"
---
# <a name="querytable-structure"></a><span data-ttu-id="15da0-103">Структура КУЕРИТАБЛЕ</span><span class="sxs-lookup"><span data-stu-id="15da0-103">QUERYTABLE structure</span></span>

<span data-ttu-id="15da0-104">Структура **куеритабле** предоставляет список компьютеров, которые в настоящее время используют сетевой монитор для записи сетевых данных.</span><span class="sxs-lookup"><span data-stu-id="15da0-104">The **QUERYTABLE** structure provides a list of the computers that are currently using Network Monitor to capture network data.</span></span>

## <a name="syntax"></a><span data-ttu-id="15da0-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="15da0-105">Syntax</span></span>


```C++
typedef struct _QUERYTABLE {
  DWORD        nStationQueries;
  STATIONQUERY StationQuery[1];
} QUERYTABLE, *LPQUERYTABLE;
```



## <a name="members"></a><span data-ttu-id="15da0-106">Члены</span><span class="sxs-lookup"><span data-stu-id="15da0-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="15da0-107">**нстатионкуериес**</span><span class="sxs-lookup"><span data-stu-id="15da0-107">**nStationQueries**</span></span>
</dt> <dd>

<span data-ttu-id="15da0-108">На входе — максимальное число компьютеров, которые сетевой монитор должны возвращаться.</span><span class="sxs-lookup"><span data-stu-id="15da0-108">On input, the maximum number of computers you want Network Monitor to return.</span></span>

<span data-ttu-id="15da0-109">В выходных данных — число структур [статионкуери](stationquery.md) , возвращенных сетевой монитор.</span><span class="sxs-lookup"><span data-stu-id="15da0-109">On output, the number of [STATIONQUERY](stationquery.md) structures returned by Network Monitor.</span></span> <span data-ttu-id="15da0-110">Каждая структура **статионкуери** представляет компьютер, на котором в данный момент выполняется запись данных.</span><span class="sxs-lookup"><span data-stu-id="15da0-110">Each **STATIONQUERY** structure represents a computer that is currently capturing data.</span></span>

</dd> <dt>

<span data-ttu-id="15da0-111">**статионкуери**</span><span class="sxs-lookup"><span data-stu-id="15da0-111">**StationQuery**</span></span>
</dt> <dd>

<span data-ttu-id="15da0-112">На входе — массив пустых структур [статионкуери](stationquery.md) , содержащих количество элементов, указанных в **нстатионкуериес**.</span><span class="sxs-lookup"><span data-stu-id="15da0-112">On input, an array of empty [STATIONQUERY](stationquery.md) structures that contains the number of elements specified in **nStationQueries**.</span></span>

<span data-ttu-id="15da0-113">На выходе — заполненная [статионкуери](stationquery.md) структура для каждого компьютера, записывающего данные.</span><span class="sxs-lookup"><span data-stu-id="15da0-113">On output, a filled [STATIONQUERY](stationquery.md) structure for each computer that is capturing data.</span></span> <span data-ttu-id="15da0-114">Число заполненных элементов возвращается функцией **нстатионкуериес**.</span><span class="sxs-lookup"><span data-stu-id="15da0-114">The number of filled elements is returned by **nStationQueries**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="15da0-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="15da0-115">Remarks</span></span>

<span data-ttu-id="15da0-116">Память для этой структуры и массива [статионкуери](stationquery.md) должна быть выделена вызывающим приложением и освобождена после того, как сведения больше не нужны.</span><span class="sxs-lookup"><span data-stu-id="15da0-116">The memory for this structure and the [STATIONQUERY](stationquery.md) array must be allocated by the calling application and freed after the information is no longer needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="15da0-117">Требования</span><span class="sxs-lookup"><span data-stu-id="15da0-117">Requirements</span></span>



| <span data-ttu-id="15da0-118">Требование</span><span class="sxs-lookup"><span data-stu-id="15da0-118">Requirement</span></span> | <span data-ttu-id="15da0-119">Значение</span><span class="sxs-lookup"><span data-stu-id="15da0-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="15da0-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="15da0-120">Minimum supported client</span></span><br/> | <span data-ttu-id="15da0-121">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="15da0-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="15da0-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="15da0-122">Minimum supported server</span></span><br/> | <span data-ttu-id="15da0-123">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="15da0-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="15da0-124">Заголовок</span><span class="sxs-lookup"><span data-stu-id="15da0-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="15da0-125"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="15da0-125"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15da0-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="15da0-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15da0-127">Иделайдк:: Куеристатионс</span><span class="sxs-lookup"><span data-stu-id="15da0-127">IDelaydC::QueryStations</span></span>](idelaydc-querystations.md)
</dt> <dt>

[<span data-ttu-id="15da0-128">ИЕСП:: Куеристатионс</span><span class="sxs-lookup"><span data-stu-id="15da0-128">IESP::QueryStations</span></span>](iesp-querystations.md)
</dt> <dt>

[<span data-ttu-id="15da0-129">ИРТК:: Куеристатионс</span><span class="sxs-lookup"><span data-stu-id="15da0-129">IRTC::QueryStations</span></span>](irtc-querystations.md)
</dt> <dt>

[<span data-ttu-id="15da0-130">Истатс:: Куеристатионс</span><span class="sxs-lookup"><span data-stu-id="15da0-130">IStats::QueryStations</span></span>](istats-querystations.md)
</dt> <dt>

[<span data-ttu-id="15da0-131">статионкуери</span><span class="sxs-lookup"><span data-stu-id="15da0-131">STATIONQUERY</span></span>](stationquery.md)
</dt> </dl>

 

 




