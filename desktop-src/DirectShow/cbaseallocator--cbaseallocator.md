---
description: Метод деструктора.
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
ms.openlocfilehash: 53587482c5d9cf8f5a772453f220c7633c17d383
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105656839"
---
# <a name="cbaseallocatorcbaseallocator-destructor"></a><span data-ttu-id="2f8f9-103">Деструктор Кбасеаллокатор. ~ Кбасеаллокатор</span><span class="sxs-lookup"><span data-stu-id="2f8f9-103">CBaseAllocator.~CBaseAllocator destructor</span></span>

<span data-ttu-id="2f8f9-104">Метод деструктора.</span><span class="sxs-lookup"><span data-stu-id="2f8f9-104">Destructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f8f9-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2f8f9-105">Syntax</span></span>


```C++
~CBaseAllocator();
```



## <a name="remarks"></a><span data-ttu-id="2f8f9-106">Примечания</span><span class="sxs-lookup"><span data-stu-id="2f8f9-106">Remarks</span></span>

<span data-ttu-id="2f8f9-107">Всегда вызывайте метод [**кбасеаллокатор::D екоммит**](cbaseallocator-decommit.md) перед уничтожением объекта.</span><span class="sxs-lookup"><span data-stu-id="2f8f9-107">Always call the [**CBaseAllocator::Decommit**](cbaseallocator-decommit.md) method before destroying the object.</span></span> <span data-ttu-id="2f8f9-108">Деструктор базового класса не может вызвать метод **uncommit**, так как этот метод вызывает чистый виртуальный метод [**Кбасеаллокатор:: Free**](cbaseallocator-free.md).</span><span class="sxs-lookup"><span data-stu-id="2f8f9-108">The base-class destructor cannot call **Decommit**, because that method calls the pure virtual method [**CBaseAllocator::Free**](cbaseallocator-free.md).</span></span> <span data-ttu-id="2f8f9-109">Производные классы должны переопределять этот деструктор и вызывать метод **uncommit**.</span><span class="sxs-lookup"><span data-stu-id="2f8f9-109">Derived classes should override this destructor and call **Decommit**.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f8f9-110">Требования</span><span class="sxs-lookup"><span data-stu-id="2f8f9-110">Requirements</span></span>



| <span data-ttu-id="2f8f9-111">Требование</span><span class="sxs-lookup"><span data-stu-id="2f8f9-111">Requirement</span></span> | <span data-ttu-id="2f8f9-112">Значение</span><span class="sxs-lookup"><span data-stu-id="2f8f9-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f8f9-113">Header</span><span class="sxs-lookup"><span data-stu-id="2f8f9-113">Header</span></span><br/>  | <dl> <span data-ttu-id="2f8f9-114"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2f8f9-114"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="2f8f9-115">Библиотека</span><span class="sxs-lookup"><span data-stu-id="2f8f9-115">Library</span></span><br/> | <dl> <span data-ttu-id="2f8f9-116"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="2f8f9-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f8f9-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2f8f9-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f8f9-118">**Класс Кбасеаллокатор**</span><span class="sxs-lookup"><span data-stu-id="2f8f9-118">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 




