---
description: Метод Пикаллокатор возвращает указатель на распределитель контакта. Метод не увеличивает значение счетчика ссылок в интерфейсе.
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
ms.openlocfilehash: 805de37e2df2bf5a198107eea69d9107e799598c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675145"
---
# <a name="ctransinplaceoutputpinpeekallocator-method"></a><span data-ttu-id="463b2-104">Ктрансинплацеаутпутпин. Пикаллокатор, метод</span><span class="sxs-lookup"><span data-stu-id="463b2-104">CTransInPlaceOutputPin.PeekAllocator method</span></span>

<span data-ttu-id="463b2-105">`PeekAllocator`Метод возвращает указатель на распределитель контакта.</span><span class="sxs-lookup"><span data-stu-id="463b2-105">The `PeekAllocator` method returns a pointer to the pin's allocator.</span></span> <span data-ttu-id="463b2-106">Метод не увеличивает значение счетчика ссылок в интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="463b2-106">The method does not increment the reference count on the interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="463b2-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="463b2-107">Syntax</span></span>


```C++
IMemAllocator* PeekAllocator();
```



## <a name="parameters"></a><span data-ttu-id="463b2-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="463b2-108">Parameters</span></span>

<span data-ttu-id="463b2-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="463b2-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="463b2-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="463b2-110">Return value</span></span>

<span data-ttu-id="463b2-111">Возвращает переменную члена [**кбасеаутпутпин:: m \_ паллокатор**](cbaseoutputpin-m-pallocator.md) .</span><span class="sxs-lookup"><span data-stu-id="463b2-111">Returns the [**CBaseOutputPin::m\_pAllocator**](cbaseoutputpin-m-pallocator.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="463b2-112">Требования</span><span class="sxs-lookup"><span data-stu-id="463b2-112">Requirements</span></span>



| <span data-ttu-id="463b2-113">Требование</span><span class="sxs-lookup"><span data-stu-id="463b2-113">Requirement</span></span> | <span data-ttu-id="463b2-114">Значение</span><span class="sxs-lookup"><span data-stu-id="463b2-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="463b2-115">Header</span><span class="sxs-lookup"><span data-stu-id="463b2-115">Header</span></span><br/>  | <dl> <span data-ttu-id="463b2-116"><dt>Трансип. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="463b2-116"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="463b2-117">Библиотека</span><span class="sxs-lookup"><span data-stu-id="463b2-117">Library</span></span><br/> | <dl> <span data-ttu-id="463b2-118"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="463b2-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="463b2-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="463b2-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="463b2-120">**Класс Ктрансинплацеаутпутпин**</span><span class="sxs-lookup"><span data-stu-id="463b2-120">**CTransInPlaceOutputPin Class**</span></span>](ctransinplaceoutputpin.md)
</dt> </dl>

 

 




