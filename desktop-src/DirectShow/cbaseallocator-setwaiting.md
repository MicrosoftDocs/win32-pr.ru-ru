---
description: Метод Сетваитинг увеличивает число ожидающих потоков.
ms.assetid: 4aec6177-fb32-44be-a58e-41a4f4aaf4f2
title: Кбасеаллокатор. Сетваитинг, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.SetWaiting
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 92cba22e128a76f7884050d74a7819142c696dc9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657847"
---
# <a name="cbaseallocatorsetwaiting-method"></a><span data-ttu-id="a21db-103">Кбасеаллокатор. Сетваитинг, метод</span><span class="sxs-lookup"><span data-stu-id="a21db-103">CBaseAllocator.SetWaiting method</span></span>

<span data-ttu-id="a21db-104">`SetWaiting`Метод увеличивает число ожидающих потоков.</span><span class="sxs-lookup"><span data-stu-id="a21db-104">The `SetWaiting` method increments the count of waiting threads.</span></span>

## <a name="syntax"></a><span data-ttu-id="a21db-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a21db-105">Syntax</span></span>


```C++
void SetWaiting();
```



## <a name="parameters"></a><span data-ttu-id="a21db-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a21db-106">Parameters</span></span>

<span data-ttu-id="a21db-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="a21db-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a21db-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a21db-108">Return value</span></span>

<span data-ttu-id="a21db-109">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="a21db-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a21db-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a21db-110">Remarks</span></span>

<span data-ttu-id="a21db-111">Этот метод увеличивает значение переменной члена [**кбасеаллокатор:: m \_ лваитинг**](cbaseallocator-m-lwaiting.md) .</span><span class="sxs-lookup"><span data-stu-id="a21db-111">This method increments the [**CBaseAllocator::m\_lWaiting**](cbaseallocator-m-lwaiting.md) member variable.</span></span> <span data-ttu-id="a21db-112">Если поток заблокирован в методе [**кбасеаллокатор::-buffer**](cbaseallocator-getbuffer.md) , распределитель вызывает метод `SetWaiting` , а затем ожидает сигнала для семафора [**\_ хсем кбасеаллокатор:: m**](cbaseallocator-m-hsem.md) .</span><span class="sxs-lookup"><span data-stu-id="a21db-112">If a thread is blocked in the [**CBaseAllocator::GetBuffer**](cbaseallocator-getbuffer.md) method, the allocator calls `SetWaiting` and then waits for the [**CBaseAllocator::m\_hSem**](cbaseallocator-m-hsem.md) semaphore to be signaled.</span></span> <span data-ttu-id="a21db-113">Метод [**кбасеаллокатор:: релеасебуффер**](cbaseallocator-releasebuffer.md) сигнализирует о семафоре и устанавливает для *m \_ лваитинг* обратно в нуль.</span><span class="sxs-lookup"><span data-stu-id="a21db-113">The [**CBaseAllocator::ReleaseBuffer**](cbaseallocator-releasebuffer.md) method signals the semaphore and sets *m\_lWaiting* back to zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="a21db-114">Требования</span><span class="sxs-lookup"><span data-stu-id="a21db-114">Requirements</span></span>



| <span data-ttu-id="a21db-115">Требование</span><span class="sxs-lookup"><span data-stu-id="a21db-115">Requirement</span></span> | <span data-ttu-id="a21db-116">Значение</span><span class="sxs-lookup"><span data-stu-id="a21db-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a21db-117">Header</span><span class="sxs-lookup"><span data-stu-id="a21db-117">Header</span></span><br/>  | <dl> <span data-ttu-id="a21db-118"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a21db-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="a21db-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a21db-119">Library</span></span><br/> | <dl> <span data-ttu-id="a21db-120"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="a21db-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a21db-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a21db-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a21db-122">**Класс Кбасеаллокатор**</span><span class="sxs-lookup"><span data-stu-id="a21db-122">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 




