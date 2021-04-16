---
description: Указатель на критическую секцию, используемый для сериализации изменений состояния.
ms.assetid: 4fecd9a6-54df-49d7-bf2f-5dcaef919ad7
title: 'Элемент Кбасефилтер:: m_pLock (Амфилтер. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_pLock
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 40b2f6ece048fc6463fda0a22792d57839d59e55
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657183"
---
# <a name="cbasefilterm_plock-member"></a><span data-ttu-id="32635-103">Элемент Кбасефилтер:: m \_ плокк</span><span class="sxs-lookup"><span data-stu-id="32635-103">CBaseFilter::m\_pLock member</span></span>

<span data-ttu-id="32635-104">Указатель на критическую секцию, используемый для сериализации изменений состояния.</span><span class="sxs-lookup"><span data-stu-id="32635-104">Pointer to a critical section that is used to serialize state changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="32635-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="32635-105">Syntax</span></span>


```C++
CCritSec *m_pLock;
```



## <a name="remarks"></a><span data-ttu-id="32635-106">Примечания</span><span class="sxs-lookup"><span data-stu-id="32635-106">Remarks</span></span>

<span data-ttu-id="32635-107">Эта переменная инициализируется в конструкторе класса. см. раздел [**кбасефилтер:: кбасефилтер**](cbasefilter-cbasefilter.md).</span><span class="sxs-lookup"><span data-stu-id="32635-107">This variable is initialized in the class constructor; see [**CBaseFilter::CBaseFilter**](cbasefilter-cbasefilter.md).</span></span>

<span data-ttu-id="32635-108">Держите этот критический раздел во время переходов между состояниями или когда метод обращается к состоянию за несколько операций.</span><span class="sxs-lookup"><span data-stu-id="32635-108">Hold this critical section during state transitions, or when a method accesses the state over several operations.</span></span> <span data-ttu-id="32635-109">Базовый класс содержит критическую секцию в следующих методах:</span><span class="sxs-lookup"><span data-stu-id="32635-109">The base class holds the critical section in the following methods:</span></span>

-   [<span data-ttu-id="32635-110">**Кбасефилтер:: Финдпин**</span><span class="sxs-lookup"><span data-stu-id="32635-110">**CBaseFilter::FindPin**</span></span>](cbasefilter-findpin.md)
-   [<span data-ttu-id="32635-111">**Кбасефилтер:: Жетсинксаурце**</span><span class="sxs-lookup"><span data-stu-id="32635-111">**CBaseFilter::GetSyncSource**</span></span>](cbasefilter-getsyncsource.md)
-   [<span data-ttu-id="32635-112">**Кбасефилтер:: Жоинфилтерграф**</span><span class="sxs-lookup"><span data-stu-id="32635-112">**CBaseFilter::JoinFilterGraph**</span></span>](cbasefilter-joinfiltergraph.md)
-   [<span data-ttu-id="32635-113">**Кбасефилтер:: @ Active**</span><span class="sxs-lookup"><span data-stu-id="32635-113">**CBaseFilter::IsActive**</span></span>](cbasefilter-isactive.md)
-   [<span data-ttu-id="32635-114">**Кбасефилтер:: Сетсинксаурце**</span><span class="sxs-lookup"><span data-stu-id="32635-114">**CBaseFilter::SetSyncSource**</span></span>](cbasefilter-setsyncsource.md)
-   [<span data-ttu-id="32635-115">**Кбасефилтер::P Аусе**</span><span class="sxs-lookup"><span data-stu-id="32635-115">**CBaseFilter::Pause**</span></span>](cbasefilter-pause.md)
-   [<span data-ttu-id="32635-116">**Кбасефилтер:: Run**</span><span class="sxs-lookup"><span data-stu-id="32635-116">**CBaseFilter::Run**</span></span>](cbasefilter-run.md)
-   [<span data-ttu-id="32635-117">**Кбасефилтер:: останавливаться**</span><span class="sxs-lookup"><span data-stu-id="32635-117">**CBaseFilter::Stop**</span></span>](cbasefilter-stop.md)

<span data-ttu-id="32635-118">Не держите этот критический раздел во время операций потоковой передачи (то есть при доставке образцов в нисходящий фильтр).</span><span class="sxs-lookup"><span data-stu-id="32635-118">Do not hold this critical section during streaming operations (that is, when delivering samples to a downstream filter).</span></span> <span data-ttu-id="32635-119">Сериализация операций потоковой передачи с использованием другой критической секции.</span><span class="sxs-lookup"><span data-stu-id="32635-119">Serialize streaming operations using a different critical section.</span></span> <span data-ttu-id="32635-120">В противном случае это может привести к взаимоблокировке.</span><span class="sxs-lookup"><span data-stu-id="32635-120">Otherwise, it can cause deadlock.</span></span>

## <a name="requirements"></a><span data-ttu-id="32635-121">Требования</span><span class="sxs-lookup"><span data-stu-id="32635-121">Requirements</span></span>



| <span data-ttu-id="32635-122">Требование</span><span class="sxs-lookup"><span data-stu-id="32635-122">Requirement</span></span> | <span data-ttu-id="32635-123">Значение</span><span class="sxs-lookup"><span data-stu-id="32635-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="32635-124">Header</span><span class="sxs-lookup"><span data-stu-id="32635-124">Header</span></span><br/>  | <dl> <span data-ttu-id="32635-125"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="32635-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="32635-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="32635-126">Library</span></span><br/> | <dl> <span data-ttu-id="32635-127"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="32635-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32635-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="32635-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32635-129">**Класс Кбасефилтер**</span><span class="sxs-lookup"><span data-stu-id="32635-129">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> <dt>

[<span data-ttu-id="32635-130">Потоки и критические разделы</span><span class="sxs-lookup"><span data-stu-id="32635-130">Threads and Critical Sections</span></span>](threads-and-critical-sections.md)
</dt> </dl>

 

 




