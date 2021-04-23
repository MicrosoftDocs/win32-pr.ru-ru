---
description: Метод Пикаллокатор возвращает указатель на распределитель контакта. Метод не увеличивает значение счетчика ссылок в интерфейсе.
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
ms.openlocfilehash: 22358dd776a0536cfbae819ec7cace02dd1775a3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675159"
---
# <a name="ctransinplaceinputpinpeekallocator-method"></a><span data-ttu-id="eab93-104">Ктрансинплацеинпутпин. Пикаллокатор, метод</span><span class="sxs-lookup"><span data-stu-id="eab93-104">CTransInPlaceInputPin.PeekAllocator method</span></span>

<span data-ttu-id="eab93-105">`PeekAllocator`Метод возвращает указатель на распределитель контакта.</span><span class="sxs-lookup"><span data-stu-id="eab93-105">The `PeekAllocator` method returns a pointer to the pin's allocator.</span></span> <span data-ttu-id="eab93-106">Метод не увеличивает значение счетчика ссылок в интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="eab93-106">The method does not increment the reference count on the interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="eab93-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="eab93-107">Syntax</span></span>


```C++
IMemAllocator* PeekAllocator();
```



## <a name="parameters"></a><span data-ttu-id="eab93-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="eab93-108">Parameters</span></span>

<span data-ttu-id="eab93-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="eab93-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="eab93-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="eab93-110">Return value</span></span>

<span data-ttu-id="eab93-111">Возвращает переменную члена [**кбасеинпутпин:: m \_ паллокатор**](cbaseinputpin-m-pallocator.md) .</span><span class="sxs-lookup"><span data-stu-id="eab93-111">Returns the [**CBaseInputPin::m\_pAllocator**](cbaseinputpin-m-pallocator.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="eab93-112">Требования</span><span class="sxs-lookup"><span data-stu-id="eab93-112">Requirements</span></span>



| <span data-ttu-id="eab93-113">Требование</span><span class="sxs-lookup"><span data-stu-id="eab93-113">Requirement</span></span> | <span data-ttu-id="eab93-114">Значение</span><span class="sxs-lookup"><span data-stu-id="eab93-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eab93-115">Header</span><span class="sxs-lookup"><span data-stu-id="eab93-115">Header</span></span><br/>  | <dl> <span data-ttu-id="eab93-116"><dt>Трансип. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="eab93-116"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="eab93-117">Библиотека</span><span class="sxs-lookup"><span data-stu-id="eab93-117">Library</span></span><br/> | <dl> <span data-ttu-id="eab93-118"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="eab93-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eab93-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="eab93-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eab93-120">**Класс Ктрансинплацеинпутпин**</span><span class="sxs-lookup"><span data-stu-id="eab93-120">**CTransInPlaceInputPin Class**</span></span>](ctransinplaceinputpin.md)
</dt> </dl>

 

 




