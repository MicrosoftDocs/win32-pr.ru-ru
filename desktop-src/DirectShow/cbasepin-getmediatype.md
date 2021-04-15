---
description: Метод Жетмедиатипе извлекает предпочтительный тип мультимедиа по значению индекса.
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
ms.openlocfilehash: 9c54c5cd769a8efa0c720c7050cca45b00b8209e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669473"
---
# <a name="cbasepingetmediatype-method"></a><span data-ttu-id="7fbbb-103">Кбасепин. Жетмедиатипе, метод</span><span class="sxs-lookup"><span data-stu-id="7fbbb-103">CBasePin.GetMediaType method</span></span>

<span data-ttu-id="7fbbb-104">`GetMediaType`Метод получает предпочтительный тип мультимедиа по значению индекса.</span><span class="sxs-lookup"><span data-stu-id="7fbbb-104">The `GetMediaType` method retrieves a preferred media type, by index value.</span></span>

## <a name="syntax"></a><span data-ttu-id="7fbbb-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7fbbb-105">Syntax</span></span>


```C++
virtual HRESULT GetMediaType(
   int        iPosition,
   CMediaType *pMediaType
);
```



## <a name="parameters"></a><span data-ttu-id="7fbbb-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7fbbb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7fbbb-107">*Интерфейс*</span><span class="sxs-lookup"><span data-stu-id="7fbbb-107">*iPosition*</span></span> 
</dt> <dd>

<span data-ttu-id="7fbbb-108">Значение индекса, начинающееся с нуля.</span><span class="sxs-lookup"><span data-stu-id="7fbbb-108">Zero-based index value.</span></span>

</dd> <dt>

<span data-ttu-id="7fbbb-109">*пмедиатипе*</span><span class="sxs-lookup"><span data-stu-id="7fbbb-109">*pMediaType*</span></span> 
</dt> <dd>

<span data-ttu-id="7fbbb-110">Указатель на объект [**кмедиатипе**](cmediatype.md) , который получает тип мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="7fbbb-110">Pointer to a [**CMediaType**](cmediatype.md) object that receives the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7fbbb-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7fbbb-111">Return value</span></span>

<span data-ttu-id="7fbbb-112">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="7fbbb-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="7fbbb-113">Возможные значения перечислены в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="7fbbb-113">Possible values include those in the following table.</span></span>



| <span data-ttu-id="7fbbb-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="7fbbb-114">Return code</span></span>                                                                                            | <span data-ttu-id="7fbbb-115">Описание</span><span class="sxs-lookup"><span data-stu-id="7fbbb-115">Description</span></span>                      |
|--------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="7fbbb-116"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="7fbbb-116"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="7fbbb-117">Успешно.</span><span class="sxs-lookup"><span data-stu-id="7fbbb-117">Success.</span></span><br/>              |
| <dl> <span data-ttu-id="7fbbb-118"><dt>**VFW \_ S \_ больше \_ \_ элементов**</dt></span><span class="sxs-lookup"><span data-stu-id="7fbbb-118"><dt>**VFW\_S\_NO\_MORE\_ITEMS**</dt></span></span> </dl> | <span data-ttu-id="7fbbb-119">Индекс вне допустимого диапазона.</span><span class="sxs-lookup"><span data-stu-id="7fbbb-119">Index out of range.</span></span><br/>   |
| <dl> <span data-ttu-id="7fbbb-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="7fbbb-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl>           | <span data-ttu-id="7fbbb-121">Индекс меньше нуля.</span><span class="sxs-lookup"><span data-stu-id="7fbbb-121">Index less than zero.</span></span><br/> |
| <dl> <span data-ttu-id="7fbbb-122"><dt>**\_непредвиденная E**</dt></span><span class="sxs-lookup"><span data-stu-id="7fbbb-122"><dt>**E\_UNEXPECTED**</dt></span></span> </dl>           | <span data-ttu-id="7fbbb-123">Непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="7fbbb-123">Unexpected error.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="7fbbb-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7fbbb-124">Remarks</span></span>

<span data-ttu-id="7fbbb-125">В списке предпочтительных типов мультимедиа для ПИН-кода этот метод возвращает тип со значением индекса *интерфейс*.</span><span class="sxs-lookup"><span data-stu-id="7fbbb-125">From the pin's list of preferred media types, this method returns the type with an index value of *iPosition*.</span></span> <span data-ttu-id="7fbbb-126">Класс [**ценуммедиатипес**](cenummediatypes.md) вызывает этот метод для перечисления предпочтительных типов мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="7fbbb-126">The [**CEnumMediaTypes**](cenummediatypes.md) class calls this method to enumerate preferred media types.</span></span>

<span data-ttu-id="7fbbb-127">Базовый класс возвращает E \_ непредвиденное значение.</span><span class="sxs-lookup"><span data-stu-id="7fbbb-127">The base class returns E\_UNEXPECTED.</span></span> <span data-ttu-id="7fbbb-128">Переопределите этот метод в производном классе.</span><span class="sxs-lookup"><span data-stu-id="7fbbb-128">Override this method in your derived class.</span></span>

## <a name="requirements"></a><span data-ttu-id="7fbbb-129">Требования</span><span class="sxs-lookup"><span data-stu-id="7fbbb-129">Requirements</span></span>



| <span data-ttu-id="7fbbb-130">Требование</span><span class="sxs-lookup"><span data-stu-id="7fbbb-130">Requirement</span></span> | <span data-ttu-id="7fbbb-131">Значение</span><span class="sxs-lookup"><span data-stu-id="7fbbb-131">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7fbbb-132">Header</span><span class="sxs-lookup"><span data-stu-id="7fbbb-132">Header</span></span><br/>  | <dl> <span data-ttu-id="7fbbb-133"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7fbbb-133"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="7fbbb-134">Библиотека</span><span class="sxs-lookup"><span data-stu-id="7fbbb-134">Library</span></span><br/> | <dl> <span data-ttu-id="7fbbb-135"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="7fbbb-135"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7fbbb-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7fbbb-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7fbbb-137">**Класс Кбасепин**</span><span class="sxs-lookup"><span data-stu-id="7fbbb-137">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




