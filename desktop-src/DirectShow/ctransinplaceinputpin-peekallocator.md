---
description: Ктрансинплацеинпутпин. Пикаллокатор, метод Пикаллокатор возвращает указатель на распределитель контакта. Метод не увеличивает значение счетчика ссылок в интерфейсе.
ms.assetid: 67f1b872-4ae2-4fbe-9240-801ef8ae1e5b
title: Ктрансинплацеинпутпин. Пикаллокатор, метод (Трансип. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceInputPin.PeekAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f7a5f7cb0fbe754890b1d7930bb54c6fca47afa5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084672"
---
# <a name="ctransinplaceinputpinpeekallocator-method"></a><span data-ttu-id="b7823-104">Ктрансинплацеинпутпин. Пикаллокатор, метод</span><span class="sxs-lookup"><span data-stu-id="b7823-104">CTransInPlaceInputPin.PeekAllocator method</span></span>

<span data-ttu-id="b7823-105">`PeekAllocator`Метод возвращает указатель на распределитель контакта.</span><span class="sxs-lookup"><span data-stu-id="b7823-105">The `PeekAllocator` method returns a pointer to the pin's allocator.</span></span> <span data-ttu-id="b7823-106">Метод не увеличивает значение счетчика ссылок в интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="b7823-106">The method does not increment the reference count on the interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7823-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b7823-107">Syntax</span></span>


```C++
IMemAllocator* PeekAllocator();
```



## <a name="parameters"></a><span data-ttu-id="b7823-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="b7823-108">Parameters</span></span>

<span data-ttu-id="b7823-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="b7823-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b7823-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b7823-110">Return value</span></span>

<span data-ttu-id="b7823-111">Возвращает переменную члена [**кбасеинпутпин:: m \_ паллокатор**](cbaseinputpin-m-pallocator.md) .</span><span class="sxs-lookup"><span data-stu-id="b7823-111">Returns the [**CBaseInputPin::m\_pAllocator**](cbaseinputpin-m-pallocator.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7823-112">Требования</span><span class="sxs-lookup"><span data-stu-id="b7823-112">Requirements</span></span>



| <span data-ttu-id="b7823-113">Требование</span><span class="sxs-lookup"><span data-stu-id="b7823-113">Requirement</span></span> | <span data-ttu-id="b7823-114">Значение</span><span class="sxs-lookup"><span data-stu-id="b7823-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7823-115">Header</span><span class="sxs-lookup"><span data-stu-id="b7823-115">Header</span></span><br/>  | <dl> <span data-ttu-id="b7823-116"><dt>Трансип. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b7823-116"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b7823-117">Библиотека</span><span class="sxs-lookup"><span data-stu-id="b7823-117">Library</span></span><br/> | <dl> <span data-ttu-id="b7823-118"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="b7823-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7823-119">См. также</span><span class="sxs-lookup"><span data-stu-id="b7823-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7823-120">**Класс Ктрансинплацеинпутпин**</span><span class="sxs-lookup"><span data-stu-id="b7823-120">**CTransInPlaceInputPin Class**</span></span>](ctransinplaceinputpin.md)
</dt> </dl>

 

 




