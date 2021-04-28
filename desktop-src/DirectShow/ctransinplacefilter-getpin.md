---
description: Ктрансинплацефилтер. Жетпин, метод Жетпин извлекает ПИН-код.
ms.assetid: d8e4973b-2af4-4141-ab2e-ea2159cd51be
title: Ктрансинплацефилтер. Жетпин, метод (Трансип. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.GetPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1075f2a14c58b085b73f2e4283458286c118a7ae
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084772"
---
# <a name="ctransinplacefiltergetpin-method"></a><span data-ttu-id="da217-103">Ктрансинплацефилтер. Жетпин, метод</span><span class="sxs-lookup"><span data-stu-id="da217-103">CTransInPlaceFilter.GetPin method</span></span>

<span data-ttu-id="da217-104">`GetPin`Метод извлекает ПИН-код.</span><span class="sxs-lookup"><span data-stu-id="da217-104">The `GetPin` method retrieves a pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="da217-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="da217-105">Syntax</span></span>


```C++
virtual CBasePin* GetPin(
   int n
);
```



## <a name="parameters"></a><span data-ttu-id="da217-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="da217-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da217-107">*n*</span><span class="sxs-lookup"><span data-stu-id="da217-107">*n*</span></span> 
</dt> <dd>

<span data-ttu-id="da217-108">Номер указанного пин-кода, индексируемого от нуля.</span><span class="sxs-lookup"><span data-stu-id="da217-108">Number of the specified pin, indexed from zero.</span></span> <span data-ttu-id="da217-109">В этом фильтре закреплением 0 является закрепление ввода, а закреплением 1 является выходной ПИН-код.</span><span class="sxs-lookup"><span data-stu-id="da217-109">On this filter, pin 0 is the input pin, and pin 1 is the output pin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da217-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="da217-110">Return value</span></span>

<span data-ttu-id="da217-111">Возвращает указатель на объект [**кбасепин**](cbasepin.md) , который реализует ПИН-код, или **значение NULL** , если метод завершается с ошибкой.</span><span class="sxs-lookup"><span data-stu-id="da217-111">Returns a pointer to the [**CBasePin**](cbasepin.md) object that implements the pin, or **NULL** if the method fails.</span></span>

## <a name="remarks"></a><span data-ttu-id="da217-112">Remarks</span><span class="sxs-lookup"><span data-stu-id="da217-112">Remarks</span></span>

<span data-ttu-id="da217-113">Этот метод переопределяет метод [**ктрансформфилтер:: жетпин**](ctransformfilter-getpin.md) .</span><span class="sxs-lookup"><span data-stu-id="da217-113">This method overrides the [**CTransformFilter::GetPin**](ctransformfilter-getpin.md) method.</span></span> <span data-ttu-id="da217-114">При первом вызове метода он создает оба ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="da217-114">The first time the method is called, it creates both pins.</span></span>

<span data-ttu-id="da217-115">Этот метод не увеличивает счетчик ссылок на возвращенном ПИН-коде, поэтому возвращенный ПИН-код не содержит необработанных ссылок.</span><span class="sxs-lookup"><span data-stu-id="da217-115">This method does not increment the reference count on the returned pin, so the returned pin does not have an outstanding reference count.</span></span> <span data-ttu-id="da217-116">Если вызывающему объекту необходимо разместить ссылку на ПИН-код, он должен вызвать метод **IUnknown:: AddRef** для ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="da217-116">If the caller needs to keep a reference on the pin, it should call the **IUnknown::AddRef** method on the pin.</span></span>

<span data-ttu-id="da217-117">Если фильтр использует ПИН-коды [**ктрансинплацеинпутпин**](ctransinplaceinputpin.md) и [**ктрансинплацеаутпутпин**](ctransinplaceoutputpin.md) по умолчанию, то, вероятно, вам не нужно переопределять этот метод.</span><span class="sxs-lookup"><span data-stu-id="da217-117">If the filter uses the default [**CTransInPlaceInputPin**](ctransinplaceinputpin.md) and [**CTransInPlaceOutputPin**](ctransinplaceoutputpin.md) pins, you probably do not need to override this method.</span></span> <span data-ttu-id="da217-118">Однако если фильтр использует ПИН-коды, расширяющие эти классы, необходимо переопределить этот метод для создания ПИН-кодов этого типа.</span><span class="sxs-lookup"><span data-stu-id="da217-118">If the filter uses pins that extend those classes, however, you must override this method to create pins of that type.</span></span>

## <a name="requirements"></a><span data-ttu-id="da217-119">Требования</span><span class="sxs-lookup"><span data-stu-id="da217-119">Requirements</span></span>



| <span data-ttu-id="da217-120">Требование</span><span class="sxs-lookup"><span data-stu-id="da217-120">Requirement</span></span> | <span data-ttu-id="da217-121">Значение</span><span class="sxs-lookup"><span data-stu-id="da217-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da217-122">Header</span><span class="sxs-lookup"><span data-stu-id="da217-122">Header</span></span><br/>  | <dl> <span data-ttu-id="da217-123"><dt>Трансип. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="da217-123"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="da217-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="da217-124">Library</span></span><br/> | <dl> <span data-ttu-id="da217-125"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="da217-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da217-126">См. также</span><span class="sxs-lookup"><span data-stu-id="da217-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da217-127">**Класс Ктрансинплацефилтер**</span><span class="sxs-lookup"><span data-stu-id="da217-127">**CTransInPlaceFilter Class**</span></span>](ctransinplacefilter.md)
</dt> </dl>

 

 




