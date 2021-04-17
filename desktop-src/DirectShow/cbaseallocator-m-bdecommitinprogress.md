---
description: Флаг, указывающий, выполняется ли операция дефиксации.
ms.assetid: aa008be1-8faa-4dc1-9641-37dcc59ce6c7
title: 'Элемент Кбасеаллокатор:: m_bDecommitInProgress (Амфилтер. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bDecommitInProgress
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 27aaf2766f67ebb77250522346cfe5c76acdf6d1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665369"
---
# <a name="cbaseallocatorm_bdecommitinprogress-member"></a><span data-ttu-id="fb545-103">Элемент Кбасеаллокатор:: m \_ бдекоммитинпрогресс</span><span class="sxs-lookup"><span data-stu-id="fb545-103">CBaseAllocator::m\_bDecommitInProgress member</span></span>

<span data-ttu-id="fb545-104">Флаг, указывающий, выполняется ли операция дефиксации.</span><span class="sxs-lookup"><span data-stu-id="fb545-104">Flag indicating whether a decommit operation is in progress.</span></span> <span data-ttu-id="fb545-105">Значение равно **true** после вызова метода [**кбасеаллокатор::D екоммит**](cbaseallocator-decommit.md) , но до освобождения всех буферов.</span><span class="sxs-lookup"><span data-stu-id="fb545-105">The value is **TRUE** after the [**CBaseAllocator::Decommit**](cbaseallocator-decommit.md) method is called, but before all the buffers have been released.</span></span> <span data-ttu-id="fb545-106">Если значение равно **true**, метод [**кбасеаллокатор::-buffer**](cbaseallocator-getbuffer.md) завершается ошибкой.</span><span class="sxs-lookup"><span data-stu-id="fb545-106">If the value is **TRUE**, the [**CBaseAllocator::GetBuffer**](cbaseallocator-getbuffer.md) method fails.</span></span> <span data-ttu-id="fb545-107">Кроме того, распределитель не должен удалять себя, пока значение равно **true**.</span><span class="sxs-lookup"><span data-stu-id="fb545-107">Also, the allocator should not deleted itself while the value is **TRUE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb545-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fb545-108">Syntax</span></span>


```C++
BOOL m_bDecommitInProgress;
```



## <a name="requirements"></a><span data-ttu-id="fb545-109">Требования</span><span class="sxs-lookup"><span data-stu-id="fb545-109">Requirements</span></span>



| <span data-ttu-id="fb545-110">Требование</span><span class="sxs-lookup"><span data-stu-id="fb545-110">Requirement</span></span> | <span data-ttu-id="fb545-111">Значение</span><span class="sxs-lookup"><span data-stu-id="fb545-111">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb545-112">Header</span><span class="sxs-lookup"><span data-stu-id="fb545-112">Header</span></span><br/>  | <dl> <span data-ttu-id="fb545-113"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fb545-113"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="fb545-114">Библиотека</span><span class="sxs-lookup"><span data-stu-id="fb545-114">Library</span></span><br/> | <dl> <span data-ttu-id="fb545-115"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="fb545-115"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb545-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fb545-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb545-117">**Класс Кбасеаллокатор**</span><span class="sxs-lookup"><span data-stu-id="fb545-117">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 




