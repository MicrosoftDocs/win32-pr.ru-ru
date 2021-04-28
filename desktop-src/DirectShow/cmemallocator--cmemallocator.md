---
description: Метод деструктора Кмемаллокатор. ~ Кмемаллокатор.
ms.assetid: e0a04d93-fb77-4dc1-9bc8-7d3965bc6803
title: Деструктор Кмемаллокатор. ~ Кмемаллокатор (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMemAllocator.~CMemAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 43b0505ee34df72ab82e4204b08440ac1a2558b5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095412"
---
# <a name="cmemallocatorcmemallocator-destructor"></a><span data-ttu-id="0c6a0-103">Деструктор Кмемаллокатор. ~ Кмемаллокатор</span><span class="sxs-lookup"><span data-stu-id="0c6a0-103">CMemAllocator.~CMemAllocator destructor</span></span>

<span data-ttu-id="0c6a0-104">Метод деструктора.</span><span class="sxs-lookup"><span data-stu-id="0c6a0-104">Destructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c6a0-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0c6a0-105">Syntax</span></span>


```C++
~CMemAllocator();
```



## <a name="remarks"></a><span data-ttu-id="0c6a0-106">Remarks</span><span class="sxs-lookup"><span data-stu-id="0c6a0-106">Remarks</span></span>

<span data-ttu-id="0c6a0-107">Этот метод переопределяет деструктор базового класса для вызова [**кбасеаллокатор::D екоммит**](cbaseallocator-decommit.md) и [**Кмемаллокатор:: реаллифри**](cmemallocator-reallyfree.md).</span><span class="sxs-lookup"><span data-stu-id="0c6a0-107">This method overrides the base-class destructor to call [**CBaseAllocator::Decommit**](cbaseallocator-decommit.md) and [**CMemAllocator::ReallyFree**](cmemallocator-reallyfree.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0c6a0-108">Требования</span><span class="sxs-lookup"><span data-stu-id="0c6a0-108">Requirements</span></span>



| <span data-ttu-id="0c6a0-109">Требование</span><span class="sxs-lookup"><span data-stu-id="0c6a0-109">Requirement</span></span> | <span data-ttu-id="0c6a0-110">Значение</span><span class="sxs-lookup"><span data-stu-id="0c6a0-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c6a0-111">Header</span><span class="sxs-lookup"><span data-stu-id="0c6a0-111">Header</span></span><br/>  | <dl> <span data-ttu-id="0c6a0-112"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0c6a0-112"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="0c6a0-113">Библиотека</span><span class="sxs-lookup"><span data-stu-id="0c6a0-113">Library</span></span><br/> | <dl> <span data-ttu-id="0c6a0-114"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="0c6a0-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0c6a0-115">См. также</span><span class="sxs-lookup"><span data-stu-id="0c6a0-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c6a0-116">**Класс Кмемаллокатор**</span><span class="sxs-lookup"><span data-stu-id="0c6a0-116">**CMemAllocator Class**</span></span>](cmemallocator.md)
</dt> </dl>

 

 




