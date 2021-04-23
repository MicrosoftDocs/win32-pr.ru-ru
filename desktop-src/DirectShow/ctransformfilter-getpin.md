---
description: Метод Жетпин извлекает ПИН-код.
ms.assetid: 5d278ef0-e5ce-439e-93b1-fec988c55854
title: Ктрансформфилтер. Жетпин, метод (Трансфрм. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.GetPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 30567db84eefd5471dbbe1fbd2d2e5ed64514ba2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679645"
---
# <a name="ctransformfiltergetpin-method"></a><span data-ttu-id="244d9-103">Ктрансформфилтер. Жетпин, метод</span><span class="sxs-lookup"><span data-stu-id="244d9-103">CTransformFilter.GetPin method</span></span>

<span data-ttu-id="244d9-104">`GetPin`Метод извлекает ПИН-код.</span><span class="sxs-lookup"><span data-stu-id="244d9-104">The `GetPin` method retrieves a pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="244d9-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="244d9-105">Syntax</span></span>


```C++
virtual CBasePin* GetPin(
   int n
);
```



## <a name="parameters"></a><span data-ttu-id="244d9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="244d9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="244d9-107">*n*</span><span class="sxs-lookup"><span data-stu-id="244d9-107">*n*</span></span> 
</dt> <dd>

<span data-ttu-id="244d9-108">Номер указанного пин-кода, индексируемого от нуля.</span><span class="sxs-lookup"><span data-stu-id="244d9-108">Number of the specified pin, indexed from zero.</span></span> <span data-ttu-id="244d9-109">В этом фильтре закреплением 0 является закрепление ввода, а закреплением 1 является выходной ПИН-код.</span><span class="sxs-lookup"><span data-stu-id="244d9-109">On this filter, pin 0 is the input pin, and pin 1 is the output pin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="244d9-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="244d9-110">Return value</span></span>

<span data-ttu-id="244d9-111">Возвращает указатель на объект [**кбасепин**](cbasepin.md) , который реализует ПИН-код, или **значение NULL** , если метод завершается с ошибкой.</span><span class="sxs-lookup"><span data-stu-id="244d9-111">Returns a pointer to the [**CBasePin**](cbasepin.md) object that implements the pin, or **NULL** if the method fails.</span></span>

## <a name="remarks"></a><span data-ttu-id="244d9-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="244d9-112">Remarks</span></span>

<span data-ttu-id="244d9-113">Этот метод реализует чистый виртуальный метод [**кбасефилтер:: жетпин**](cbasefilter-getpin.md) .</span><span class="sxs-lookup"><span data-stu-id="244d9-113">This method implements the pure virtual [**CBaseFilter::GetPin**](cbasefilter-getpin.md) method.</span></span> <span data-ttu-id="244d9-114">При первом вызове метода он создает оба ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="244d9-114">The first time the method is called, it creates both pins.</span></span>

<span data-ttu-id="244d9-115">Этот метод не увеличивает счетчик ссылок на возвращенном ПИН-коде, поэтому возвращенный ПИН-код не содержит необработанных ссылок.</span><span class="sxs-lookup"><span data-stu-id="244d9-115">This method does not increment the reference count on the returned pin, so the returned pin does not have an outstanding reference count.</span></span> <span data-ttu-id="244d9-116">Если вызывающему объекту необходимо разместить ссылку на ПИН-код, он должен вызвать метод **IUnknown:: AddRef** для ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="244d9-116">If the caller needs to keep a reference on the pin, it should call the **IUnknown::AddRef** method on the pin.</span></span>

<span data-ttu-id="244d9-117">Если фильтр использует ПИН-коды [**ктрансформинпутпин**](ctransforminputpin.md) и [**ктрансформаутпутпин**](ctransformoutputpin.md) по умолчанию, то, вероятно, вам не нужно переопределять этот метод.</span><span class="sxs-lookup"><span data-stu-id="244d9-117">If the filter uses the default [**CTransformInputPin**](ctransforminputpin.md) and [**CTransformOutputPin**](ctransformoutputpin.md) pins, you probably do not need to override this method.</span></span> <span data-ttu-id="244d9-118">Однако если фильтр использует ПИН-коды, расширяющие эти классы, необходимо переопределить этот метод для создания ПИН-кодов этого типа.</span><span class="sxs-lookup"><span data-stu-id="244d9-118">If the filter uses pins that extend those classes, however, you must override this method to create pins of that type.</span></span>

## <a name="requirements"></a><span data-ttu-id="244d9-119">Требования</span><span class="sxs-lookup"><span data-stu-id="244d9-119">Requirements</span></span>



| <span data-ttu-id="244d9-120">Требование</span><span class="sxs-lookup"><span data-stu-id="244d9-120">Requirement</span></span> | <span data-ttu-id="244d9-121">Значение</span><span class="sxs-lookup"><span data-stu-id="244d9-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="244d9-122">Header</span><span class="sxs-lookup"><span data-stu-id="244d9-122">Header</span></span><br/>  | <dl> <span data-ttu-id="244d9-123"><dt>Трансфрм. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="244d9-123"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="244d9-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="244d9-124">Library</span></span><br/> | <dl> <span data-ttu-id="244d9-125"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="244d9-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="244d9-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="244d9-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="244d9-127">**Класс Ктрансформфилтер**</span><span class="sxs-lookup"><span data-stu-id="244d9-127">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




