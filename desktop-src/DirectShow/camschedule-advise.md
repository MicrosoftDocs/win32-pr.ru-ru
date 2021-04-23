---
description: Метод advise отправляет все запросы, запланированные на указанное время или ранее.
ms.assetid: 09ea84b7-517a-4ea6-9e03-0d9cd8f72e1f
title: Метод Камсчедуле. Advise (Дссчедуле. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMSchedule.Advise
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 70880243cef294ebe747463cd11737027faf9277
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668786"
---
# <a name="camscheduleadvise-method"></a><span data-ttu-id="66fd0-103">Камсчедуле. Advise, метод</span><span class="sxs-lookup"><span data-stu-id="66fd0-103">CAMSchedule.Advise method</span></span>

<span data-ttu-id="66fd0-104">`Advise`Метод отправляет все запросы, запланированные на указанное время или ранее.</span><span class="sxs-lookup"><span data-stu-id="66fd0-104">The `Advise` method dispatches all requests that are scheduled for a specified time or earlier.</span></span>

## <a name="syntax"></a><span data-ttu-id="66fd0-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="66fd0-105">Syntax</span></span>


```C++
REFERENCE_TIME Advise(
  [ref] const REFERENCE_TIME &rtTime
);
```



## <a name="parameters"></a><span data-ttu-id="66fd0-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="66fd0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66fd0-107">*рттиме* \[ ЗНАЧ\]</span><span class="sxs-lookup"><span data-stu-id="66fd0-107">*rtTime* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="66fd0-108">Значение, указывающее текущее время ссылки.</span><span class="sxs-lookup"><span data-stu-id="66fd0-108">Value that specifies the current reference time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66fd0-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="66fd0-109">Return value</span></span>

<span data-ttu-id="66fd0-110">Возвращает время ссылки следующего запланированного запроса на выполе или максимальное \_ время, если не осталось ничего.</span><span class="sxs-lookup"><span data-stu-id="66fd0-110">Returns the reference time of the next scheduled advise request, or MAX\_TIME if there are none left.</span></span>

## <a name="remarks"></a><span data-ttu-id="66fd0-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="66fd0-111">Remarks</span></span>

<span data-ttu-id="66fd0-112">Когда часы вызывают этот метод, он указывает текущее время ссылки.</span><span class="sxs-lookup"><span data-stu-id="66fd0-112">When the clock calls this method, it specifies the current reference time.</span></span> <span data-ttu-id="66fd0-113">Планировщик определяет, какие запросы на выступающий истек срок действия, если они есть, и отправляет их.</span><span class="sxs-lookup"><span data-stu-id="66fd0-113">The scheduler determines which advise requests have expired, if any, and dispatches them.</span></span> <span data-ttu-id="66fd0-114">Если срок действия одноразового запроса истекает, Планировщик удаляет его.</span><span class="sxs-lookup"><span data-stu-id="66fd0-114">If a one-shot request expires, the scheduler deletes it.</span></span> <span data-ttu-id="66fd0-115">Если срок действия периодического запроса истекает, планировщик повторно планирует его для следующего времени.</span><span class="sxs-lookup"><span data-stu-id="66fd0-115">If a periodic request expires, the scheduler re-schedules it for the next advise time.</span></span> <span data-ttu-id="66fd0-116">Метод возвращает время следующего ожидающего запроса.</span><span class="sxs-lookup"><span data-stu-id="66fd0-116">The method returns the time of the next pending request.</span></span>

<span data-ttu-id="66fd0-117">Чтобы отправить запрос advise, планировщик сигнализирует о событии или семафоре, указанном в параметре *хнотифи* метода [**Камсчедуле:: аддадвисепаккет**](camschedule-addadvisepacket.md) .</span><span class="sxs-lookup"><span data-stu-id="66fd0-117">To dispatch an advise request, the scheduler signals the event or semaphore given in the *hNotify* parameter of the [**CAMSchedule::AddAdvisePacket**](camschedule-addadvisepacket.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="66fd0-118">Требования</span><span class="sxs-lookup"><span data-stu-id="66fd0-118">Requirements</span></span>



| <span data-ttu-id="66fd0-119">Требование</span><span class="sxs-lookup"><span data-stu-id="66fd0-119">Requirement</span></span> | <span data-ttu-id="66fd0-120">Значение</span><span class="sxs-lookup"><span data-stu-id="66fd0-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="66fd0-121">Header</span><span class="sxs-lookup"><span data-stu-id="66fd0-121">Header</span></span><br/>  | <dl> <span data-ttu-id="66fd0-122"><dt>Дссчедуле. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="66fd0-122"><dt>Dsschedule.h (include Streams.h)</dt></span></span> </dl>                                                                                |
| <span data-ttu-id="66fd0-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="66fd0-123">Library</span></span><br/> | <dl> <span data-ttu-id="66fd0-124"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="66fd0-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66fd0-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="66fd0-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66fd0-126">**Класс Камсчедуле**</span><span class="sxs-lookup"><span data-stu-id="66fd0-126">**CAMSchedule Class**</span></span>](camschedule.md)
</dt> </dl>

 

 




