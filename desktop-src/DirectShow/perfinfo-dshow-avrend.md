---
description: Структура ПЕРФИНФО \_ DSHOW \_ авренд содержит данные для события трассировки типа GUID \_ видеоренд. VMR регистрирует это событие непосредственно перед отрисовкой кадра.
ms.assetid: 95deda21-0ef4-4bf0-9fa3-826a813757b9
title: Структура PERFINFO_DSHOW_AVREND (Перфструкт. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PERFINFO_DSHOW_AVREND
api_type:
- HeaderDef
api_location:
- Perfstruct.h
ms.openlocfilehash: ee2d944d086f9c1a4ea7944f023321dfbc06d547
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689283"
---
# <a name="perfinfo_dshow_avrend-structure"></a><span data-ttu-id="7cbca-103">\_ \_ Структура авренд перфинфо DSHOW</span><span class="sxs-lookup"><span data-stu-id="7cbca-103">PERFINFO\_DSHOW\_AVREND structure</span></span>

<span data-ttu-id="7cbca-104">`PERFINFO_DSHOW_AVREND`Структура содержит данные для события трассировки типа GUID \_ видеоренд.</span><span class="sxs-lookup"><span data-stu-id="7cbca-104">The `PERFINFO_DSHOW_AVREND` structure contains data for a trace event of type GUID\_VIDEOREND.</span></span>

<span data-ttu-id="7cbca-105">VMR регистрирует это событие непосредственно перед отрисовкой кадра.</span><span class="sxs-lookup"><span data-stu-id="7cbca-105">The VMR logs this event immediately before rendering a frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="7cbca-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7cbca-106">Syntax</span></span>


```C++
typedef struct PERFINFO_DSHOW_AVREND {
  ULONGLONG cycleCounter;
  ULONGLONG dshowClock;
  ULONGLONG sampleTime;
} PERFINFO_DSHOW_AVREND, *PPERFINFO_DSHOW_AVREND;
```



## <a name="members"></a><span data-ttu-id="7cbca-107">Члены</span><span class="sxs-lookup"><span data-stu-id="7cbca-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="7cbca-108">**циклекаунтер**</span><span class="sxs-lookup"><span data-stu-id="7cbca-108">**cycleCounter**</span></span>
</dt> <dd>

<span data-ttu-id="7cbca-109">Последнее число циклов тактовой разницы (инструкция RDTSC).</span><span class="sxs-lookup"><span data-stu-id="7cbca-109">Latest clock cycle count (RDTSC instruction).</span></span>

</dd> <dt>

<span data-ttu-id="7cbca-110">**дшовклокк**</span><span class="sxs-lookup"><span data-stu-id="7cbca-110">**dshowClock**</span></span>
</dt> <dd>

<span data-ttu-id="7cbca-111">Текущее время ссылки, возвращаемое методом [**иреференцеклокк:: Time**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) .</span><span class="sxs-lookup"><span data-stu-id="7cbca-111">Current reference time, as returned by the [**IReferenceClock::GetTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) method.</span></span>

</dd> <dt>

<span data-ttu-id="7cbca-112">**самплетиме**</span><span class="sxs-lookup"><span data-stu-id="7cbca-112">**sampleTime**</span></span>
</dt> <dd>

<span data-ttu-id="7cbca-113">Время начала примера.</span><span class="sxs-lookup"><span data-stu-id="7cbca-113">Start time of the sample.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7cbca-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7cbca-114">Remarks</span></span>

<span data-ttu-id="7cbca-115">Чтобы включить это событие, необходимо задать \_ флаг дксмперф видеоренд в параметре *енаблефлаг* при вызове **енаблетраце**.</span><span class="sxs-lookup"><span data-stu-id="7cbca-115">To enable this event, you must set the DXMPERF\_VIDEOREND flag in the *EnableFlag* parameter when you call **EnableTrace**.</span></span> <span data-ttu-id="7cbca-116">Этот флаг определен в файле заголовка Дксмперф. h, который включен в базовые классы DirectShow.</span><span class="sxs-lookup"><span data-stu-id="7cbca-116">This flag is defined in the header file Dxmperf.h, which is included in the DirectShow base classes.</span></span>

<span data-ttu-id="7cbca-117">Чтобы заносить это событие из фильтра DirectShow, используйте макрос **перфлог \_ видеоренд** , который определен в дксмперф. h.</span><span class="sxs-lookup"><span data-stu-id="7cbca-117">To log this event from a DirectShow filter, use the **PERFLOG\_VIDEOREND** macro, which is defined in Dxmperf.h.</span></span>

## <a name="requirements"></a><span data-ttu-id="7cbca-118">Требования</span><span class="sxs-lookup"><span data-stu-id="7cbca-118">Requirements</span></span>



| <span data-ttu-id="7cbca-119">Требование</span><span class="sxs-lookup"><span data-stu-id="7cbca-119">Requirement</span></span> | <span data-ttu-id="7cbca-120">Значение</span><span class="sxs-lookup"><span data-stu-id="7cbca-120">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7cbca-121">Header</span><span class="sxs-lookup"><span data-stu-id="7cbca-121">Header</span></span><br/> | <dl> <span data-ttu-id="7cbca-122"><dt>Перфструкт. h</dt></span><span class="sxs-lookup"><span data-stu-id="7cbca-122"><dt>Perfstruct.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7cbca-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7cbca-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7cbca-124">Структуры DirectShow</span><span class="sxs-lookup"><span data-stu-id="7cbca-124">DirectShow Structures</span></span>](directshow-structures.md)
</dt> <dt>

[<span data-ttu-id="7cbca-125">Трассировка событий в DirectShow</span><span class="sxs-lookup"><span data-stu-id="7cbca-125">Event Tracing in DirectShow</span></span>](event-tracing-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="7cbca-126">Идентификаторы GUID событий трассировки</span><span class="sxs-lookup"><span data-stu-id="7cbca-126">Trace Event GUIDs</span></span>](trace-guids.md)
</dt> </dl>

 

 




