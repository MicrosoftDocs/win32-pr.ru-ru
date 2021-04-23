---
description: Структура ПЕРФИНФО \_ DSHOW \_ аудиобреак содержит данные для события трассировки типа GUID \_ аудиобреак. Фильтр модуля подготовки отчетов DirectSound регистрирует это событие при разрыве в потоке аудио.
ms.assetid: 9e7abdca-7d4c-4006-997f-9605f8d18e1d
title: Структура PERFINFO_DSHOW_AUDIOBREAK (Перфструкт. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PERFINFO_DSHOW_AUDIOBREAK
api_type:
- HeaderDef
api_location:
- Perfstruct.h
ms.openlocfilehash: 599befea67b28acbedffd5c98ebce84aadf70838
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689285"
---
# <a name="perfinfo_dshow_audiobreak-structure"></a><span data-ttu-id="177d7-103">\_ \_ Структура аудиобреак перфинфо DSHOW</span><span class="sxs-lookup"><span data-stu-id="177d7-103">PERFINFO\_DSHOW\_AUDIOBREAK structure</span></span>

<span data-ttu-id="177d7-104">`PERFINFO_DSHOW_AUDIOBREAK`Структура содержит данные для события трассировки типа GUID \_ аудиобреак.</span><span class="sxs-lookup"><span data-stu-id="177d7-104">The `PERFINFO_DSHOW_AUDIOBREAK` structure contains data for a trace event of type GUID\_AUDIOBREAK.</span></span>

<span data-ttu-id="177d7-105">Фильтр модуля [подготовки отчетов DirectSound](directsound-renderer-filter.md) регистрирует это событие при разрыве в потоке аудио.</span><span class="sxs-lookup"><span data-stu-id="177d7-105">The [DirectSound Renderer](directsound-renderer-filter.md) filter logs this event when there is a break in the audio stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="177d7-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="177d7-106">Syntax</span></span>


```C++
typedef struct PERFINFO_DSHOW_AUDIOBREAK {
  ULONGLONG cycleCounter;
  ULONGLONG dshowClock;
  ULONGLONG sampleTime;
  ULONGLONG sampleDuration;
} PERFINFO_DSHOW_AUDIOBREAK, *PPERFINFO_DSHOW_AUDIOBREAK;
```



## <a name="members"></a><span data-ttu-id="177d7-107">Члены</span><span class="sxs-lookup"><span data-stu-id="177d7-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="177d7-108">**циклекаунтер**</span><span class="sxs-lookup"><span data-stu-id="177d7-108">**cycleCounter**</span></span>
</dt> <dd>

<span data-ttu-id="177d7-109">Последнее число циклов тактовой разницы (инструкция RDTSC).</span><span class="sxs-lookup"><span data-stu-id="177d7-109">Latest clock cycle count (RDTSC instruction).</span></span>

</dd> <dt>

<span data-ttu-id="177d7-110">**дшовклокк**</span><span class="sxs-lookup"><span data-stu-id="177d7-110">**dshowClock**</span></span>
</dt> <dd>

<span data-ttu-id="177d7-111">Текущее расположение записи в буфере DirectSound.</span><span class="sxs-lookup"><span data-stu-id="177d7-111">Current write position in the DirectSound buffer.</span></span>

</dd> <dt>

<span data-ttu-id="177d7-112">**самплетиме**</span><span class="sxs-lookup"><span data-stu-id="177d7-112">**sampleTime**</span></span>
</dt> <dd>

<span data-ttu-id="177d7-113">Начало разрыва звука в буфере DirectSound.</span><span class="sxs-lookup"><span data-stu-id="177d7-113">Start of the audio break in the DirectSound buffer.</span></span>

</dd> <dt>

<span data-ttu-id="177d7-114">**сампледуратион**</span><span class="sxs-lookup"><span data-stu-id="177d7-114">**sampleDuration**</span></span>
</dt> <dd>

<span data-ttu-id="177d7-115">Продолжительность перерыва в миллисекундах.</span><span class="sxs-lookup"><span data-stu-id="177d7-115">Duration of the break, in milliseconds.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="177d7-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="177d7-116">Remarks</span></span>

<span data-ttu-id="177d7-117">Чтобы включить это событие, необходимо задать \_ флаг битов аудиобреак в параметре *енаблефлаг* при вызове **енаблетраце**.</span><span class="sxs-lookup"><span data-stu-id="177d7-117">To enable this event, you must set the AUDIOBREAK\_BIT flag in the *EnableFlag* parameter when you call **EnableTrace**.</span></span> <span data-ttu-id="177d7-118">Этот флаг определен в файле заголовка Дксмперф. h, который включен в базовые классы DirectShow.</span><span class="sxs-lookup"><span data-stu-id="177d7-118">This flag is defined in the header file Dxmperf.h, which is included in the DirectShow base classes.</span></span>

<span data-ttu-id="177d7-119">Чтобы заносить это событие из фильтра DirectShow, используйте макрос **перфлог \_ аудиобреак** , который определен в дксмперф. h.</span><span class="sxs-lookup"><span data-stu-id="177d7-119">To log this event from a DirectShow filter, use the **PERFLOG\_AUDIOBREAK** macro, which is defined in Dxmperf.h.</span></span>

## <a name="requirements"></a><span data-ttu-id="177d7-120">Требования</span><span class="sxs-lookup"><span data-stu-id="177d7-120">Requirements</span></span>



| <span data-ttu-id="177d7-121">Требование</span><span class="sxs-lookup"><span data-stu-id="177d7-121">Requirement</span></span> | <span data-ttu-id="177d7-122">Значение</span><span class="sxs-lookup"><span data-stu-id="177d7-122">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="177d7-123">Header</span><span class="sxs-lookup"><span data-stu-id="177d7-123">Header</span></span><br/> | <dl> <span data-ttu-id="177d7-124"><dt>Перфструкт. h</dt></span><span class="sxs-lookup"><span data-stu-id="177d7-124"><dt>Perfstruct.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="177d7-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="177d7-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="177d7-126">Структуры DirectShow</span><span class="sxs-lookup"><span data-stu-id="177d7-126">DirectShow Structures</span></span>](directshow-structures.md)
</dt> <dt>

[<span data-ttu-id="177d7-127">Трассировка событий в DirectShow</span><span class="sxs-lookup"><span data-stu-id="177d7-127">Event Tracing in DirectShow</span></span>](event-tracing-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="177d7-128">Идентификаторы GUID событий трассировки</span><span class="sxs-lookup"><span data-stu-id="177d7-128">Trace Event GUIDs</span></span>](trace-guids.md)
</dt> </dl>

 

 




