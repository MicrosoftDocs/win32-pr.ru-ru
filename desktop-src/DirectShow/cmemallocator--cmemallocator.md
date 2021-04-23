---
description: Метод деструктора.
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
ms.openlocfilehash: d49046eccd8d7ef71c4eeb4c75acffbf90f7d826
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665499"
---
# <a name="cmemallocatorcmemallocator-destructor"></a><span data-ttu-id="cb113-103">Деструктор Кмемаллокатор. ~ Кмемаллокатор</span><span class="sxs-lookup"><span data-stu-id="cb113-103">CMemAllocator.~CMemAllocator destructor</span></span>

<span data-ttu-id="cb113-104">Метод деструктора.</span><span class="sxs-lookup"><span data-stu-id="cb113-104">Destructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb113-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cb113-105">Syntax</span></span>


```C++
~CMemAllocator();
```



## <a name="remarks"></a><span data-ttu-id="cb113-106">Примечания</span><span class="sxs-lookup"><span data-stu-id="cb113-106">Remarks</span></span>

<span data-ttu-id="cb113-107">Этот метод переопределяет деструктор базового класса для вызова [**кбасеаллокатор::D екоммит**](cbaseallocator-decommit.md) и [**Кмемаллокатор:: реаллифри**](cmemallocator-reallyfree.md).</span><span class="sxs-lookup"><span data-stu-id="cb113-107">This method overrides the base-class destructor to call [**CBaseAllocator::Decommit**](cbaseallocator-decommit.md) and [**CMemAllocator::ReallyFree**](cmemallocator-reallyfree.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="cb113-108">Требования</span><span class="sxs-lookup"><span data-stu-id="cb113-108">Requirements</span></span>



| <span data-ttu-id="cb113-109">Требование</span><span class="sxs-lookup"><span data-stu-id="cb113-109">Requirement</span></span> | <span data-ttu-id="cb113-110">Значение</span><span class="sxs-lookup"><span data-stu-id="cb113-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb113-111">Header</span><span class="sxs-lookup"><span data-stu-id="cb113-111">Header</span></span><br/>  | <dl> <span data-ttu-id="cb113-112"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cb113-112"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="cb113-113">Библиотека</span><span class="sxs-lookup"><span data-stu-id="cb113-113">Library</span></span><br/> | <dl> <span data-ttu-id="cb113-114"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="cb113-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb113-115">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cb113-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb113-116">**Класс Кмемаллокатор**</span><span class="sxs-lookup"><span data-stu-id="cb113-116">**CMemAllocator Class**</span></span>](cmemallocator.md)
</dt> </dl>

 

 




