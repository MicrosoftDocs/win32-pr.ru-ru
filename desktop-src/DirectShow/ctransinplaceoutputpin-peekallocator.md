---
description: Ктрансинплацеаутпутпин. Пикаллокатор, метод Пикаллокатор возвращает указатель на распределитель контакта. Метод не увеличивает значение счетчика ссылок в интерфейсе.
ms.assetid: 3653d472-059c-426c-8e81-4f7cbd1a8ec3
title: Ктрансинплацеаутпутпин. Пикаллокатор, метод (Трансип. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceOutputPin.PeekAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cba87df1c4b9a3391d60e9458387e7b2bd4afd49
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084602"
---
# <a name="ctransinplaceoutputpinpeekallocator-method"></a><span data-ttu-id="24720-104">Ктрансинплацеаутпутпин. Пикаллокатор, метод</span><span class="sxs-lookup"><span data-stu-id="24720-104">CTransInPlaceOutputPin.PeekAllocator method</span></span>

<span data-ttu-id="24720-105">`PeekAllocator`Метод возвращает указатель на распределитель контакта.</span><span class="sxs-lookup"><span data-stu-id="24720-105">The `PeekAllocator` method returns a pointer to the pin's allocator.</span></span> <span data-ttu-id="24720-106">Метод не увеличивает значение счетчика ссылок в интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="24720-106">The method does not increment the reference count on the interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="24720-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="24720-107">Syntax</span></span>


```C++
IMemAllocator* PeekAllocator();
```



## <a name="parameters"></a><span data-ttu-id="24720-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="24720-108">Parameters</span></span>

<span data-ttu-id="24720-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="24720-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="24720-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="24720-110">Return value</span></span>

<span data-ttu-id="24720-111">Возвращает переменную члена [**кбасеаутпутпин:: m \_ паллокатор**](cbaseoutputpin-m-pallocator.md) .</span><span class="sxs-lookup"><span data-stu-id="24720-111">Returns the [**CBaseOutputPin::m\_pAllocator**](cbaseoutputpin-m-pallocator.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="24720-112">Требования</span><span class="sxs-lookup"><span data-stu-id="24720-112">Requirements</span></span>



| <span data-ttu-id="24720-113">Требование</span><span class="sxs-lookup"><span data-stu-id="24720-113">Requirement</span></span> | <span data-ttu-id="24720-114">Значение</span><span class="sxs-lookup"><span data-stu-id="24720-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="24720-115">Header</span><span class="sxs-lookup"><span data-stu-id="24720-115">Header</span></span><br/>  | <dl> <span data-ttu-id="24720-116"><dt>Трансип. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="24720-116"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="24720-117">Библиотека</span><span class="sxs-lookup"><span data-stu-id="24720-117">Library</span></span><br/> | <dl> <span data-ttu-id="24720-118"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="24720-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="24720-119">См. также</span><span class="sxs-lookup"><span data-stu-id="24720-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24720-120">**Класс Ктрансинплацеаутпутпин**</span><span class="sxs-lookup"><span data-stu-id="24720-120">**CTransInPlaceOutputPin Class**</span></span>](ctransinplaceoutputpin.md)
</dt> </dl>

 

 




