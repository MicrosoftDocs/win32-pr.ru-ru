---
description: Метод Set сигнализирует о событии.
ms.assetid: dfcb1601-aa65-47f5-ae3c-f13fcd7b1398
title: Метод Камевент. Set (Вксутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMEvent.Set
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c9caeed17d42d121ae9263bf6c1fcd011ed573c7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669094"
---
# <a name="cameventset-method"></a><span data-ttu-id="3c3ea-103">Камевент. Set, метод</span><span class="sxs-lookup"><span data-stu-id="3c3ea-103">CAMEvent.Set method</span></span>

<span data-ttu-id="3c3ea-104">`Set`Метод сигнализирует о событии.</span><span class="sxs-lookup"><span data-stu-id="3c3ea-104">The `Set` method signals the event.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c3ea-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3c3ea-105">Syntax</span></span>


```C++
void Set();
```



## <a name="parameters"></a><span data-ttu-id="3c3ea-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3c3ea-106">Parameters</span></span>

<span data-ttu-id="3c3ea-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="3c3ea-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3c3ea-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3c3ea-108">Return value</span></span>

<span data-ttu-id="3c3ea-109">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="3c3ea-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3c3ea-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3c3ea-110">Remarks</span></span>

<span data-ttu-id="3c3ea-111">Поведение зависит от того, является ли объект событием автоматического сброса или событием ручного сброса:</span><span class="sxs-lookup"><span data-stu-id="3c3ea-111">The behavior depends on whether the object is an auto-reset event or a manual-reset event:</span></span>

-   <span data-ttu-id="3c3ea-112">**Автоматический сброс**: Если какие-либо потоки ожидают это событие, один поток освобождается и событие сбрасывается.</span><span class="sxs-lookup"><span data-stu-id="3c3ea-112">**Auto-reset**: If any threads are waiting on this event, one thread is released and the event is reset.</span></span> <span data-ttu-id="3c3ea-113">Если ни один из потоков не ожидает этого события, событие остается сигнальным.</span><span class="sxs-lookup"><span data-stu-id="3c3ea-113">If no threads are waiting on this event, the event remains signaled.</span></span>
-   <span data-ttu-id="3c3ea-114">**Вручную — сброс**: освобождаются все потоки, ожидающие этого события.</span><span class="sxs-lookup"><span data-stu-id="3c3ea-114">**Manual-reset**: All the threads waiting on this event are released.</span></span> <span data-ttu-id="3c3ea-115">Событие остается сигнальным.</span><span class="sxs-lookup"><span data-stu-id="3c3ea-115">The event remains signaled.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c3ea-116">Требования</span><span class="sxs-lookup"><span data-stu-id="3c3ea-116">Requirements</span></span>



| <span data-ttu-id="3c3ea-117">Требование</span><span class="sxs-lookup"><span data-stu-id="3c3ea-117">Requirement</span></span> | <span data-ttu-id="3c3ea-118">Значение</span><span class="sxs-lookup"><span data-stu-id="3c3ea-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c3ea-119">Header</span><span class="sxs-lookup"><span data-stu-id="3c3ea-119">Header</span></span><br/>  | <dl> <span data-ttu-id="3c3ea-120"><dt>Вксутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3c3ea-120"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="3c3ea-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="3c3ea-121">Library</span></span><br/> | <dl> <span data-ttu-id="3c3ea-122"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="3c3ea-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c3ea-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3c3ea-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c3ea-124">**Класс Камевент**</span><span class="sxs-lookup"><span data-stu-id="3c3ea-124">**CAMEvent Class**</span></span>](camevent.md)
</dt> </dl>

 

 




