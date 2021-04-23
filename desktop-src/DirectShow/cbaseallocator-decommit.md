---
description: Метод uncommit отменяет выделение распределителя. Этот метод реализует метод Имемаллокатор::D екоммит.
ms.assetid: 0c8d44e0-17ea-4f7f-be44-f9ae2e34fbef
title: Метод Кбасеаллокатор. uncommit (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.Decommit
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 613af805f1c04a7bf375755ff8f3adba7b70be18
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657341"
---
# <a name="cbaseallocatordecommit-method"></a><span data-ttu-id="be4e2-104">Кбасеаллокатор. uncommit, метод</span><span class="sxs-lookup"><span data-stu-id="be4e2-104">CBaseAllocator.Decommit method</span></span>

<span data-ttu-id="be4e2-105">Метод отменяет `Decommit` выделение распределителя.</span><span class="sxs-lookup"><span data-stu-id="be4e2-105">The `Decommit` method decommits the allocator.</span></span> <span data-ttu-id="be4e2-106">Этот метод реализует метод [**имемаллокатор::D екоммит**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-decommit) .</span><span class="sxs-lookup"><span data-stu-id="be4e2-106">This method implements the [**IMemAllocator::Decommit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-decommit) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="be4e2-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="be4e2-107">Syntax</span></span>


```C++
HRESULT Decommit();
```



## <a name="parameters"></a><span data-ttu-id="be4e2-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="be4e2-108">Parameters</span></span>

<span data-ttu-id="be4e2-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="be4e2-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="be4e2-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="be4e2-110">Return value</span></span>

<span data-ttu-id="be4e2-111">Возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="be4e2-111">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="be4e2-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="be4e2-112">Remarks</span></span>

<span data-ttu-id="be4e2-113">После вызова этого метода вызовы метода [**кбасеаллокатор::-buffer**](cbaseallocator-getbuffer.md) завершатся ошибкой.</span><span class="sxs-lookup"><span data-stu-id="be4e2-113">After this method is called, calls to the [**CBaseAllocator::GetBuffer**](cbaseallocator-getbuffer.md) method will fail.</span></span> <span data-ttu-id="be4e2-114">После выпуска образцов они возвращаются в бесплатный список.</span><span class="sxs-lookup"><span data-stu-id="be4e2-114">As samples are released, they get returned to the free list.</span></span> <span data-ttu-id="be4e2-115">Когда возвращается последняя выборка, распределитель вызывает метод [**кбасеаллокатор:: Free**](cbaseallocator-free.md) , который освобождает выделенную память.</span><span class="sxs-lookup"><span data-stu-id="be4e2-115">When the last sample is returned, the allocator calls the [**CBaseAllocator::Free**](cbaseallocator-free.md) method, which releases the allocated memory.</span></span> <span data-ttu-id="be4e2-116">(В базовом классе **Free** является чисто виртуальным методом.)</span><span class="sxs-lookup"><span data-stu-id="be4e2-116">(In the base class, **Free** is a pure virtual method.)</span></span>

<span data-ttu-id="be4e2-117">Кроме того, этот метод освобождает все потоки, заблокированные в вызовах метода **buffer** .</span><span class="sxs-lookup"><span data-stu-id="be4e2-117">In addition, this method releases any threads that are blocked on **GetBuffer** calls.</span></span> <span data-ttu-id="be4e2-118">Вызовы метода " **buffer** " завершаются ошибкой.</span><span class="sxs-lookup"><span data-stu-id="be4e2-118">The calls to **GetBuffer** fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="be4e2-119">Требования</span><span class="sxs-lookup"><span data-stu-id="be4e2-119">Requirements</span></span>



| <span data-ttu-id="be4e2-120">Требование</span><span class="sxs-lookup"><span data-stu-id="be4e2-120">Requirement</span></span> | <span data-ttu-id="be4e2-121">Значение</span><span class="sxs-lookup"><span data-stu-id="be4e2-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be4e2-122">Header</span><span class="sxs-lookup"><span data-stu-id="be4e2-122">Header</span></span><br/>  | <dl> <span data-ttu-id="be4e2-123"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="be4e2-123"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="be4e2-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="be4e2-124">Library</span></span><br/> | <dl> <span data-ttu-id="be4e2-125"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="be4e2-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be4e2-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="be4e2-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be4e2-127">**Класс Кбасеаллокатор**</span><span class="sxs-lookup"><span data-stu-id="be4e2-127">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 




