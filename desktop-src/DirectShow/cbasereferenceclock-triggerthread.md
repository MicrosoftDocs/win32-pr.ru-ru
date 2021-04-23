---
description: Метод Тригжерсреад пробуждает рабочий поток, который обрабатывает планирование.
ms.assetid: 296a6b59-fc52-4f5e-8a19-6b534a253a6e
title: Кбасереференцеклокк. Тригжерсреад, метод (Рефклокк. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.TriggerThread
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1f18b4f7dee15ea95046091da006f537830fcbb7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669195"
---
# <a name="cbasereferenceclocktriggerthread-method"></a><span data-ttu-id="b97b7-103">Кбасереференцеклокк. Тригжерсреад, метод</span><span class="sxs-lookup"><span data-stu-id="b97b7-103">CBaseReferenceClock.TriggerThread method</span></span>

<span data-ttu-id="b97b7-104">`TriggerThread`Метод пробуждает рабочий поток, который обрабатывает планирование.</span><span class="sxs-lookup"><span data-stu-id="b97b7-104">The `TriggerThread` method wakes up the worker thread that handles scheduling.</span></span>

## <a name="syntax"></a><span data-ttu-id="b97b7-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b97b7-105">Syntax</span></span>


```C++
void TriggerThread();
```



## <a name="parameters"></a><span data-ttu-id="b97b7-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b97b7-106">Parameters</span></span>

<span data-ttu-id="b97b7-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="b97b7-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b97b7-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b97b7-108">Return value</span></span>

<span data-ttu-id="b97b7-109">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="b97b7-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b97b7-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b97b7-110">Remarks</span></span>

<span data-ttu-id="b97b7-111">Часы используют рабочий поток, который вызывает метод [**камсчедуле:: Advise**](camschedule-advise.md) в соответствующее время.</span><span class="sxs-lookup"><span data-stu-id="b97b7-111">The clock uses a worker thread that calls the [**CAMSchedule::Advise**](camschedule-advise.md) method at appropriate times.</span></span> <span data-ttu-id="b97b7-112">Производный класс может вызвать `TriggerThread` , чтобы вывести поток из спящего режима.</span><span class="sxs-lookup"><span data-stu-id="b97b7-112">The derived class can call `TriggerThread` to wake up the thread.</span></span>

## <a name="requirements"></a><span data-ttu-id="b97b7-113">Требования</span><span class="sxs-lookup"><span data-stu-id="b97b7-113">Requirements</span></span>



| <span data-ttu-id="b97b7-114">Требование</span><span class="sxs-lookup"><span data-stu-id="b97b7-114">Requirement</span></span> | <span data-ttu-id="b97b7-115">Значение</span><span class="sxs-lookup"><span data-stu-id="b97b7-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b97b7-116">Header</span><span class="sxs-lookup"><span data-stu-id="b97b7-116">Header</span></span><br/>  | <dl> <span data-ttu-id="b97b7-117"><dt>Рефклокк. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b97b7-117"><dt>Refclock.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="b97b7-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="b97b7-118">Library</span></span><br/> | <dl> <span data-ttu-id="b97b7-119"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="b97b7-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b97b7-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b97b7-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b97b7-121">**Класс Кбасереференцеклокк**</span><span class="sxs-lookup"><span data-stu-id="b97b7-121">**CBaseReferenceClock Class**</span></span>](cbasereferenceclock.md)
</dt> </dl>

 

 




