---
description: Метод Жетмедиатипе извлекает предпочтительный тип мультимедиа для выходного ПИН-кода.
ms.assetid: 9a1b123b-aa8a-4bf0-a926-466ded24e506
title: Ктрансформфилтер. Жетмедиатипе, метод (Трансфрм. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.GetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ba751e291a1ffa8e030be7e77cfd456956718baa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657773"
---
# <a name="ctransformfiltergetmediatype-method"></a><span data-ttu-id="3e9d4-103">Ктрансформфилтер. Жетмедиатипе, метод</span><span class="sxs-lookup"><span data-stu-id="3e9d4-103">CTransformFilter.GetMediaType method</span></span>

<span data-ttu-id="3e9d4-104">`GetMediaType`Метод извлекает предпочтительный тип мультимедиа для выходного контакта.</span><span class="sxs-lookup"><span data-stu-id="3e9d4-104">The `GetMediaType` method retrieves a preferred media type for the output pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e9d4-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3e9d4-105">Syntax</span></span>


```C++
virtual HRESULT GetMediaType(
   int        iPosition,
   CMediaType *pMediaType
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="3e9d4-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3e9d4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e9d4-107">*Интерфейс*</span><span class="sxs-lookup"><span data-stu-id="3e9d4-107">*iPosition*</span></span> 
</dt> <dd>

<span data-ttu-id="3e9d4-108">Значение индекса, начинающееся с нуля.</span><span class="sxs-lookup"><span data-stu-id="3e9d4-108">Zero-based index value.</span></span>

</dd> <dt>

<span data-ttu-id="3e9d4-109">*пмедиатипе*</span><span class="sxs-lookup"><span data-stu-id="3e9d4-109">*pMediaType*</span></span> 
</dt> <dd>

<span data-ttu-id="3e9d4-110">Указатель на объект [**кмедиатипе**](cmediatype.md) , который получает тип мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="3e9d4-110">Pointer to a [**CMediaType**](cmediatype.md) object that receives the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3e9d4-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3e9d4-111">Return value</span></span>

<span data-ttu-id="3e9d4-112">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3e9d4-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="3e9d4-113">Возможные значения включают в себя, показанные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="3e9d4-113">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="3e9d4-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="3e9d4-114">Return code</span></span>                                                                                            | <span data-ttu-id="3e9d4-115">Описание</span><span class="sxs-lookup"><span data-stu-id="3e9d4-115">Description</span></span>                      |
|--------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="3e9d4-116"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="3e9d4-116"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="3e9d4-117">Успешно.</span><span class="sxs-lookup"><span data-stu-id="3e9d4-117">Success.</span></span><br/>              |
| <dl> <span data-ttu-id="3e9d4-118"><dt>**VFW \_ S \_ больше \_ \_ элементов**</dt></span><span class="sxs-lookup"><span data-stu-id="3e9d4-118"><dt>**VFW\_S\_NO\_MORE\_ITEMS**</dt></span></span> </dl> | <span data-ttu-id="3e9d4-119">Индекс вне допустимого диапазона.</span><span class="sxs-lookup"><span data-stu-id="3e9d4-119">Index out of range.</span></span><br/>   |
| <dl> <span data-ttu-id="3e9d4-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="3e9d4-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl>           | <span data-ttu-id="3e9d4-121">Индекс меньше нуля.</span><span class="sxs-lookup"><span data-stu-id="3e9d4-121">Index less than zero.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="3e9d4-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3e9d4-122">Remarks</span></span>

<span data-ttu-id="3e9d4-123">Метод [**ктрансформаутпутпин:: жетмедиатипе**](ctransformoutputpin-getmediatype.md) выходного контакта вызывает этот метод.</span><span class="sxs-lookup"><span data-stu-id="3e9d4-123">The output pin's [**CTransformOutputPin::GetMediaType**](ctransformoutputpin-getmediatype.md) method calls this method.</span></span> <span data-ttu-id="3e9d4-124">Производный класс должен реализовывать этот метод.</span><span class="sxs-lookup"><span data-stu-id="3e9d4-124">The derived class must implement this method.</span></span> <span data-ttu-id="3e9d4-125">Дополнительные сведения см. в разделе [**кбасепин:: жетмедиатипе**](cbasepin-getmediatype.md).</span><span class="sxs-lookup"><span data-stu-id="3e9d4-125">For more information, see [**CBasePin::GetMediaType**](cbasepin-getmediatype.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3e9d4-126">Требования</span><span class="sxs-lookup"><span data-stu-id="3e9d4-126">Requirements</span></span>



| <span data-ttu-id="3e9d4-127">Требование</span><span class="sxs-lookup"><span data-stu-id="3e9d4-127">Requirement</span></span> | <span data-ttu-id="3e9d4-128">Значение</span><span class="sxs-lookup"><span data-stu-id="3e9d4-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e9d4-129">Header</span><span class="sxs-lookup"><span data-stu-id="3e9d4-129">Header</span></span><br/>  | <dl> <span data-ttu-id="3e9d4-130"><dt>Трансфрм. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3e9d4-130"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="3e9d4-131">Библиотека</span><span class="sxs-lookup"><span data-stu-id="3e9d4-131">Library</span></span><br/> | <dl> <span data-ttu-id="3e9d4-132"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="3e9d4-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e9d4-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3e9d4-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e9d4-134">**Класс Ктрансформфилтер**</span><span class="sxs-lookup"><span data-stu-id="3e9d4-134">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




