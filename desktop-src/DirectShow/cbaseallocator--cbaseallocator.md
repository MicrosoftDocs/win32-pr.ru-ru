---
description: Метод деструктора Кбасеаллокатор. ~ Кбасеаллокатор.
ms.assetid: b1e5653f-d72f-4cde-a8c9-d25763434374
title: Деструктор Кбасеаллокатор. ~ Кбасеаллокатор (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.~CBaseAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9a4b754c8937b87a547f4583b3270f5782a6a415
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096422"
---
# <a name="cbaseallocatorcbaseallocator-destructor"></a><span data-ttu-id="dbb95-103">Деструктор Кбасеаллокатор. ~ Кбасеаллокатор</span><span class="sxs-lookup"><span data-stu-id="dbb95-103">CBaseAllocator.~CBaseAllocator destructor</span></span>

<span data-ttu-id="dbb95-104">Метод деструктора.</span><span class="sxs-lookup"><span data-stu-id="dbb95-104">Destructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="dbb95-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dbb95-105">Syntax</span></span>


```C++
~CBaseAllocator();
```



## <a name="remarks"></a><span data-ttu-id="dbb95-106">Remarks</span><span class="sxs-lookup"><span data-stu-id="dbb95-106">Remarks</span></span>

<span data-ttu-id="dbb95-107">Всегда вызывайте метод [**кбасеаллокатор::D екоммит**](cbaseallocator-decommit.md) перед уничтожением объекта.</span><span class="sxs-lookup"><span data-stu-id="dbb95-107">Always call the [**CBaseAllocator::Decommit**](cbaseallocator-decommit.md) method before destroying the object.</span></span> <span data-ttu-id="dbb95-108">Деструктор базового класса не может вызвать метод **uncommit**, так как этот метод вызывает чистый виртуальный метод [**Кбасеаллокатор:: Free**](cbaseallocator-free.md).</span><span class="sxs-lookup"><span data-stu-id="dbb95-108">The base-class destructor cannot call **Decommit**, because that method calls the pure virtual method [**CBaseAllocator::Free**](cbaseallocator-free.md).</span></span> <span data-ttu-id="dbb95-109">Производные классы должны переопределять этот деструктор и вызывать метод **uncommit**.</span><span class="sxs-lookup"><span data-stu-id="dbb95-109">Derived classes should override this destructor and call **Decommit**.</span></span>

## <a name="requirements"></a><span data-ttu-id="dbb95-110">Требования</span><span class="sxs-lookup"><span data-stu-id="dbb95-110">Requirements</span></span>



| <span data-ttu-id="dbb95-111">Требование</span><span class="sxs-lookup"><span data-stu-id="dbb95-111">Requirement</span></span> | <span data-ttu-id="dbb95-112">Значение</span><span class="sxs-lookup"><span data-stu-id="dbb95-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dbb95-113">Header</span><span class="sxs-lookup"><span data-stu-id="dbb95-113">Header</span></span><br/>  | <dl> <span data-ttu-id="dbb95-114"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="dbb95-114"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="dbb95-115">Библиотека</span><span class="sxs-lookup"><span data-stu-id="dbb95-115">Library</span></span><br/> | <dl> <span data-ttu-id="dbb95-116"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="dbb95-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dbb95-117">См. также</span><span class="sxs-lookup"><span data-stu-id="dbb95-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dbb95-118">**Класс Кбасеаллокатор**</span><span class="sxs-lookup"><span data-stu-id="dbb95-118">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 




