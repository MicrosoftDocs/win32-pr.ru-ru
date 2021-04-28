---
description: Кбасепин. Жетмедиатипе, метод Жетмедиатипе извлекает предпочтительный тип мультимедиа по значению индекса.
ms.assetid: 96f102b0-e2d1-49a1-84af-aa4622cae2a9
title: Кбасепин. Жетмедиатипе, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.GetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 186f2eddbedf4eb0565a4ca66ff4ed7e5b080090
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099372"
---
# <a name="cbasepingetmediatype-method"></a><span data-ttu-id="d6225-103">Кбасепин. Жетмедиатипе, метод</span><span class="sxs-lookup"><span data-stu-id="d6225-103">CBasePin.GetMediaType method</span></span>

<span data-ttu-id="d6225-104">`GetMediaType`Метод получает предпочтительный тип мультимедиа по значению индекса.</span><span class="sxs-lookup"><span data-stu-id="d6225-104">The `GetMediaType` method retrieves a preferred media type, by index value.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6225-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d6225-105">Syntax</span></span>


```C++
virtual HRESULT GetMediaType(
   int        iPosition,
   CMediaType *pMediaType
);
```



## <a name="parameters"></a><span data-ttu-id="d6225-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d6225-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6225-107">*Интерфейс*</span><span class="sxs-lookup"><span data-stu-id="d6225-107">*iPosition*</span></span> 
</dt> <dd>

<span data-ttu-id="d6225-108">Значение индекса, начинающееся с нуля.</span><span class="sxs-lookup"><span data-stu-id="d6225-108">Zero-based index value.</span></span>

</dd> <dt>

<span data-ttu-id="d6225-109">*пмедиатипе*</span><span class="sxs-lookup"><span data-stu-id="d6225-109">*pMediaType*</span></span> 
</dt> <dd>

<span data-ttu-id="d6225-110">Указатель на объект [**кмедиатипе**](cmediatype.md) , который получает тип мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="d6225-110">Pointer to a [**CMediaType**](cmediatype.md) object that receives the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6225-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d6225-111">Return value</span></span>

<span data-ttu-id="d6225-112">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d6225-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="d6225-113">Возможные значения перечислены в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="d6225-113">Possible values include those in the following table.</span></span>



| <span data-ttu-id="d6225-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="d6225-114">Return code</span></span>                                                                                            | <span data-ttu-id="d6225-115">Описание</span><span class="sxs-lookup"><span data-stu-id="d6225-115">Description</span></span>                      |
|--------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="d6225-116"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="d6225-116"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="d6225-117">Успешно.</span><span class="sxs-lookup"><span data-stu-id="d6225-117">Success.</span></span><br/>              |
| <dl> <span data-ttu-id="d6225-118"><dt>**VFW \_ S \_ больше \_ \_ элементов**</dt></span><span class="sxs-lookup"><span data-stu-id="d6225-118"><dt>**VFW\_S\_NO\_MORE\_ITEMS**</dt></span></span> </dl> | <span data-ttu-id="d6225-119">Индекс вне допустимого диапазона.</span><span class="sxs-lookup"><span data-stu-id="d6225-119">Index out of range.</span></span><br/>   |
| <dl> <span data-ttu-id="d6225-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="d6225-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl>           | <span data-ttu-id="d6225-121">Индекс меньше нуля.</span><span class="sxs-lookup"><span data-stu-id="d6225-121">Index less than zero.</span></span><br/> |
| <dl> <span data-ttu-id="d6225-122"><dt>**\_непредвиденная E**</dt></span><span class="sxs-lookup"><span data-stu-id="d6225-122"><dt>**E\_UNEXPECTED**</dt></span></span> </dl>           | <span data-ttu-id="d6225-123">Непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="d6225-123">Unexpected error.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="d6225-124">Remarks</span><span class="sxs-lookup"><span data-stu-id="d6225-124">Remarks</span></span>

<span data-ttu-id="d6225-125">В списке предпочтительных типов мультимедиа для ПИН-кода этот метод возвращает тип со значением индекса *интерфейс*.</span><span class="sxs-lookup"><span data-stu-id="d6225-125">From the pin's list of preferred media types, this method returns the type with an index value of *iPosition*.</span></span> <span data-ttu-id="d6225-126">Класс [**ценуммедиатипес**](cenummediatypes.md) вызывает этот метод для перечисления предпочтительных типов мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="d6225-126">The [**CEnumMediaTypes**](cenummediatypes.md) class calls this method to enumerate preferred media types.</span></span>

<span data-ttu-id="d6225-127">Базовый класс возвращает E \_ непредвиденное значение.</span><span class="sxs-lookup"><span data-stu-id="d6225-127">The base class returns E\_UNEXPECTED.</span></span> <span data-ttu-id="d6225-128">Переопределите этот метод в производном классе.</span><span class="sxs-lookup"><span data-stu-id="d6225-128">Override this method in your derived class.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6225-129">Требования</span><span class="sxs-lookup"><span data-stu-id="d6225-129">Requirements</span></span>



| <span data-ttu-id="d6225-130">Требование</span><span class="sxs-lookup"><span data-stu-id="d6225-130">Requirement</span></span> | <span data-ttu-id="d6225-131">Значение</span><span class="sxs-lookup"><span data-stu-id="d6225-131">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6225-132">Header</span><span class="sxs-lookup"><span data-stu-id="d6225-132">Header</span></span><br/>  | <dl> <span data-ttu-id="d6225-133"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d6225-133"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="d6225-134">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d6225-134">Library</span></span><br/> | <dl> <span data-ttu-id="d6225-135"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="d6225-135"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d6225-136">См. также</span><span class="sxs-lookup"><span data-stu-id="d6225-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6225-137">**Класс Кбасепин**</span><span class="sxs-lookup"><span data-stu-id="d6225-137">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




