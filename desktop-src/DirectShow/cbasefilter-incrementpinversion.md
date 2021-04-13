---
description: Метод Инкремементпинверсион увеличивает номер версии в наборе ПИН-кодов.
ms.assetid: e1b3ec33-104d-4a12-9b11-f8bea09690a7
title: Кбасефилтер. Инкрементпинверсион, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.IncrementPinVersion
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 53e66ccd5bdd34c4767001403439f4372ff2938a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657802"
---
# <a name="cbasefilterincrementpinversion-method"></a><span data-ttu-id="03e35-103">Кбасефилтер. Инкрементпинверсион, метод</span><span class="sxs-lookup"><span data-stu-id="03e35-103">CBaseFilter.IncrementPinVersion method</span></span>

<span data-ttu-id="03e35-104">`IncremementPinVersion`Метод увеличивает номер версии набора ПИН-кодов.</span><span class="sxs-lookup"><span data-stu-id="03e35-104">The `IncremementPinVersion` method increments the version number on the set of pins.</span></span>

## <a name="syntax"></a><span data-ttu-id="03e35-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="03e35-105">Syntax</span></span>


```C++
void IncrementPinVersion();
```



## <a name="parameters"></a><span data-ttu-id="03e35-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="03e35-106">Parameters</span></span>

<span data-ttu-id="03e35-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="03e35-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="03e35-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="03e35-108">Return value</span></span>

<span data-ttu-id="03e35-109">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="03e35-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="03e35-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="03e35-110">Remarks</span></span>

<span data-ttu-id="03e35-111">Этот метод увеличивает значение переменной члена [**кбасефилтер:: m \_ пинверсион**](cbasefilter-m-pinversion.md) .</span><span class="sxs-lookup"><span data-stu-id="03e35-111">This method increments the [**CBaseFilter::m\_PinVersion**](cbasefilter-m-pinversion.md) member variable.</span></span> <span data-ttu-id="03e35-112">Если фильтр динамически создает или уничтожает ПИН-коды, вызывайте этот метод при каждом изменении ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="03e35-112">If the filter dynamically creates or destroys pins, call this method whenever the pins change.</span></span>

## <a name="requirements"></a><span data-ttu-id="03e35-113">Требования</span><span class="sxs-lookup"><span data-stu-id="03e35-113">Requirements</span></span>



| <span data-ttu-id="03e35-114">Требование</span><span class="sxs-lookup"><span data-stu-id="03e35-114">Requirement</span></span> | <span data-ttu-id="03e35-115">Значение</span><span class="sxs-lookup"><span data-stu-id="03e35-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03e35-116">Header</span><span class="sxs-lookup"><span data-stu-id="03e35-116">Header</span></span><br/>  | <dl> <span data-ttu-id="03e35-117"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="03e35-117"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="03e35-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="03e35-118">Library</span></span><br/> | <dl> <span data-ttu-id="03e35-119"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="03e35-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03e35-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="03e35-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03e35-121">**Класс Кбасефилтер**</span><span class="sxs-lookup"><span data-stu-id="03e35-121">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> <dt>

[<span data-ttu-id="03e35-122">**Кбасефилтер:: Жетпинверсион**</span><span class="sxs-lookup"><span data-stu-id="03e35-122">**CBaseFilter::GetPinVersion**</span></span>](cbasefilter-getpinversion.md)
</dt> </dl>

 

 




