---
description: Метод Нотифисампле освобождает все потоки, ожидающие выборки.
ms.assetid: b09c48a0-9cd5-44a7-9267-d2a11e8cde4c
title: Кбасеаллокатор. Нотифисампле, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.NotifySample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: acaf5e45eac6a630d0589e3c8fad106ae29fa3dc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669145"
---
# <a name="cbaseallocatornotifysample-method"></a><span data-ttu-id="8eccc-103">Кбасеаллокатор. Нотифисампле, метод</span><span class="sxs-lookup"><span data-stu-id="8eccc-103">CBaseAllocator.NotifySample method</span></span>

<span data-ttu-id="8eccc-104">`NotifySample`Метод освобождает все потоки, ожидающие выборки.</span><span class="sxs-lookup"><span data-stu-id="8eccc-104">The `NotifySample` method releases any threads that are waiting for samples.</span></span>

## <a name="syntax"></a><span data-ttu-id="8eccc-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8eccc-105">Syntax</span></span>


```C++
void NotifySample();
```



## <a name="parameters"></a><span data-ttu-id="8eccc-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8eccc-106">Parameters</span></span>

<span data-ttu-id="8eccc-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="8eccc-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8eccc-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8eccc-108">Return value</span></span>

<span data-ttu-id="8eccc-109">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="8eccc-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8eccc-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8eccc-110">Remarks</span></span>

<span data-ttu-id="8eccc-111">Если имеются потоки, ожидающие выборки, значение [**кбасеаллокатор:: m \_ лваитинг**](cbaseallocator-m-lwaiting.md) больше нуля.</span><span class="sxs-lookup"><span data-stu-id="8eccc-111">When there are threads waiting for samples, the value of [**CBaseAllocator::m\_lWaiting**](cbaseallocator-m-lwaiting.md) is greater than zero.</span></span> <span data-ttu-id="8eccc-112">Если значение *m \_ лваитинг* больше нуля, этот метод вызывает функцию **ReleaseSemaphore** для семафора [**кбасеаллокатор:: m \_ хсем**](cbaseallocator-m-hsem.md) , активируя все ожидающие потоки.</span><span class="sxs-lookup"><span data-stu-id="8eccc-112">If *m\_lWaiting* is greater than zero, this method calls the **ReleaseSemaphore** function on the [**CBaseAllocator::m\_hSem**](cbaseallocator-m-hsem.md) semaphore, activating any waiting threads.</span></span> <span data-ttu-id="8eccc-113">Он также сбрасывает значение *m \_ лваитинг* до нуля.</span><span class="sxs-lookup"><span data-stu-id="8eccc-113">It also resets *m\_lWaiting* to zero.</span></span>

<span data-ttu-id="8eccc-114">Этот метод вызывается из метода [**кбасеаллокатор:: релеасебуффер**](cbaseallocator-releasebuffer.md) , когда образец возвращается в свободный список. и из метода [**кбасеаллокатор::D екоммит**](cbaseallocator-decommit.md) , когда распределитель является незафиксированным.</span><span class="sxs-lookup"><span data-stu-id="8eccc-114">This method is called from within the [**CBaseAllocator::ReleaseBuffer**](cbaseallocator-releasebuffer.md) method, when a sample is returned to the free list; and from the [**CBaseAllocator::Decommit**](cbaseallocator-decommit.md) method, when the allocator is decommitted.</span></span>

## <a name="requirements"></a><span data-ttu-id="8eccc-115">Требования</span><span class="sxs-lookup"><span data-stu-id="8eccc-115">Requirements</span></span>



| <span data-ttu-id="8eccc-116">Требование</span><span class="sxs-lookup"><span data-stu-id="8eccc-116">Requirement</span></span> | <span data-ttu-id="8eccc-117">Значение</span><span class="sxs-lookup"><span data-stu-id="8eccc-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8eccc-118">Header</span><span class="sxs-lookup"><span data-stu-id="8eccc-118">Header</span></span><br/>  | <dl> <span data-ttu-id="8eccc-119"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8eccc-119"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="8eccc-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="8eccc-120">Library</span></span><br/> | <dl> <span data-ttu-id="8eccc-121"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="8eccc-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8eccc-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8eccc-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8eccc-123">**Класс Кбасеаллокатор**</span><span class="sxs-lookup"><span data-stu-id="8eccc-123">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 




