---
description: Метод Free освобождает всю буферную память. Этот метод вызывается, когда фильтр-владелец отменяет распределитель, после освобождения последнего примера носителя.
ms.assetid: dd1e6c4d-762a-4caf-902b-015c6c9fdb4d
title: Метод Кбасеаллокатор. Free (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.Free
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3534eac01a6769e090c8c808f16cc6ad5c6b84c1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668549"
---
# <a name="cbaseallocatorfree-method"></a><span data-ttu-id="78141-104">Кбасеаллокатор. Free, метод</span><span class="sxs-lookup"><span data-stu-id="78141-104">CBaseAllocator.Free method</span></span>

<span data-ttu-id="78141-105">`Free`Метод освобождает всю буферную память.</span><span class="sxs-lookup"><span data-stu-id="78141-105">The `Free` method releases all of the buffer memory.</span></span> <span data-ttu-id="78141-106">Этот метод вызывается, когда фильтр-владелец отменяет распределитель, после освобождения последнего примера носителя.</span><span class="sxs-lookup"><span data-stu-id="78141-106">This method is called when the owning filter decommits the allocator, after the last media sample is released.</span></span>

## <a name="syntax"></a><span data-ttu-id="78141-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="78141-107">Syntax</span></span>


```C++
virtual void Free() = 0;
```



## <a name="parameters"></a><span data-ttu-id="78141-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="78141-108">Parameters</span></span>

<span data-ttu-id="78141-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="78141-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="78141-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="78141-110">Return value</span></span>

<span data-ttu-id="78141-111">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="78141-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="78141-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="78141-112">Remarks</span></span>

<span data-ttu-id="78141-113">После вызова метода [**uncommit**](cbaseallocator-decommit.md) распределитель вызывает этот метод при освобождении последнего примера носителя.</span><span class="sxs-lookup"><span data-stu-id="78141-113">After the [**Decommit**](cbaseallocator-decommit.md) method is called, the allocator calls this method when it releases the last media sample.</span></span> <span data-ttu-id="78141-114">Производный класс должен реализовывать этот метод.</span><span class="sxs-lookup"><span data-stu-id="78141-114">The derived class must implement this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="78141-115">Требования</span><span class="sxs-lookup"><span data-stu-id="78141-115">Requirements</span></span>



| <span data-ttu-id="78141-116">Требование</span><span class="sxs-lookup"><span data-stu-id="78141-116">Requirement</span></span> | <span data-ttu-id="78141-117">Значение</span><span class="sxs-lookup"><span data-stu-id="78141-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="78141-118">Header</span><span class="sxs-lookup"><span data-stu-id="78141-118">Header</span></span><br/>  | <dl> <span data-ttu-id="78141-119"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="78141-119"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="78141-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="78141-120">Library</span></span><br/> | <dl> <span data-ttu-id="78141-121"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="78141-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="78141-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="78141-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78141-123">**Класс Кбасеаллокатор**</span><span class="sxs-lookup"><span data-stu-id="78141-123">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 




