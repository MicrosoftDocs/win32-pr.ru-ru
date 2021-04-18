---
description: Количество буферов для предоставления.
ms.assetid: 73f87b14-4346-4909-bd1e-c4981cde403d
title: 'Элемент Кбасеаллокатор:: m_lCount (Амфилтер. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_lCount
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 16ab469db1d50007bd3aa55ab692c51aa7600452
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657600"
---
# <a name="cbaseallocatorm_lcount-member"></a><span data-ttu-id="74c97-103">Элемент Кбасеаллокатор:: m \_ lCount</span><span class="sxs-lookup"><span data-stu-id="74c97-103">CBaseAllocator::m\_lCount member</span></span>

<span data-ttu-id="74c97-104">Количество буферов для предоставления.</span><span class="sxs-lookup"><span data-stu-id="74c97-104">Number of buffers to provide.</span></span> <span data-ttu-id="74c97-105">Это значение задается методом [**кбасеаллокатор:: SetProperties**](cbaseallocator-setproperties.md) .</span><span class="sxs-lookup"><span data-stu-id="74c97-105">The [**CBaseAllocator::SetProperties**](cbaseallocator-setproperties.md) method sets this value.</span></span> <span data-ttu-id="74c97-106">Буферы не выделяются, пока не будет вызван метод [**кбасеаллокатор:: Commit**](cbaseallocator-commit.md) .</span><span class="sxs-lookup"><span data-stu-id="74c97-106">The buffers are not allocated until the [**CBaseAllocator::Commit**](cbaseallocator-commit.md) method is called.</span></span> <span data-ttu-id="74c97-107">Текущее число выделенных буферов задается переменной-членом [**кбасеаллокатор:: m \_ лаллокатед**](cbaseallocator-m-lallocated.md) .</span><span class="sxs-lookup"><span data-stu-id="74c97-107">The current number of allocated buffers is specified by the [**CBaseAllocator::m\_lAllocated**](cbaseallocator-m-lallocated.md) member variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="74c97-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="74c97-108">Syntax</span></span>


```C++
long m_lCount;
```



## <a name="requirements"></a><span data-ttu-id="74c97-109">Требования</span><span class="sxs-lookup"><span data-stu-id="74c97-109">Requirements</span></span>



| <span data-ttu-id="74c97-110">Требование</span><span class="sxs-lookup"><span data-stu-id="74c97-110">Requirement</span></span> | <span data-ttu-id="74c97-111">Значение</span><span class="sxs-lookup"><span data-stu-id="74c97-111">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="74c97-112">Header</span><span class="sxs-lookup"><span data-stu-id="74c97-112">Header</span></span><br/>  | <dl> <span data-ttu-id="74c97-113"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="74c97-113"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="74c97-114">Библиотека</span><span class="sxs-lookup"><span data-stu-id="74c97-114">Library</span></span><br/> | <dl> <span data-ttu-id="74c97-115"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="74c97-115"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="74c97-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="74c97-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74c97-117">**Класс Кбасеаллокатор**</span><span class="sxs-lookup"><span data-stu-id="74c97-117">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 




