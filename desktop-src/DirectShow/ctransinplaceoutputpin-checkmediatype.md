---
description: Ктрансинплацеаутпутпин. Чеккмедиатипе, метод Чеккмедиатипе определяет, принимает ли ПИН-код конкретный тип носителя.
ms.assetid: be720021-ef7b-4281-a9f4-93abbdafc75d
title: Ктрансинплацеаутпутпин. Чеккмедиатипе, метод (Трансип. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceOutputPin.CheckMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 66cd29758e0b2d63db88db8b998cc79ec12efdd9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094722"
---
# <a name="ctransinplaceoutputpincheckmediatype-method"></a><span data-ttu-id="65d75-103">Ктрансинплацеаутпутпин. Чеккмедиатипе, метод</span><span class="sxs-lookup"><span data-stu-id="65d75-103">CTransInPlaceOutputPin.CheckMediaType method</span></span>

<span data-ttu-id="65d75-104">`CheckMediaType`Метод определяет, принимает ли ПИН-код конкретный тип носителя.</span><span class="sxs-lookup"><span data-stu-id="65d75-104">The `CheckMediaType` method determines if the pin accepts a specific media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="65d75-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="65d75-105">Syntax</span></span>


```C++
HRESULT CheckMediaType(
   const CMediaType *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="65d75-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="65d75-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65d75-107">*состоит*</span><span class="sxs-lookup"><span data-stu-id="65d75-107">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="65d75-108">Указатель на объект [**кмедиатипе**](cmediatype.md) , который содержит предложенный тип мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="65d75-108">Pointer to a [**CMediaType**](cmediatype.md) object that contains the proposed media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65d75-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="65d75-109">Return value</span></span>

<span data-ttu-id="65d75-110">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="65d75-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="65d75-111">Возможные значения включают в себя, показанные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="65d75-111">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="65d75-112">Код возврата</span><span class="sxs-lookup"><span data-stu-id="65d75-112">Return code</span></span>                                                                                                | <span data-ttu-id="65d75-113">Описание</span><span class="sxs-lookup"><span data-stu-id="65d75-113">Description</span></span>                         |
|------------------------------------------------------------------------------------------------------------|-------------------------------------|
| <dl> <span data-ttu-id="65d75-114"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="65d75-114"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="65d75-115">Успешно.</span><span class="sxs-lookup"><span data-stu-id="65d75-115">Success.</span></span><br/>                 |
| <dl> <span data-ttu-id="65d75-116"><dt>**\_тип VFW \_ E \_ не \_ принят**</dt></span><span class="sxs-lookup"><span data-stu-id="65d75-116"><dt>**VFW\_E\_TYPE\_NOT\_ACCEPTED**</dt></span></span> </dl> | <span data-ttu-id="65d75-117">Тип носителя не принят.</span><span class="sxs-lookup"><span data-stu-id="65d75-117">Media type not accepted.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="65d75-118">Remarks</span><span class="sxs-lookup"><span data-stu-id="65d75-118">Remarks</span></span>

<span data-ttu-id="65d75-119">Этот метод переопределяет метод [**ктрансформаутпутпин:: чеккмедиатипе**](ctransformoutputpin-checkmediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="65d75-119">This method overrides the [**CTransformOutputPin::CheckMediaType**](ctransformoutputpin-checkmediatype.md) method.</span></span>

<span data-ttu-id="65d75-120">Если фильтр уже потоковая передача и использует два распределителя, этот метод отклоняет любые изменения формата.</span><span class="sxs-lookup"><span data-stu-id="65d75-120">If the filter is already streaming and is using two allocators, this method rejects any format changes.</span></span> <span data-ttu-id="65d75-121">В противном случае этот метод вызывает метод [**ктрансформфилтер:: чеккинпуттипе**](ctransformfilter-checkinputtype.md) фильтра для проверки типа мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="65d75-121">Otherwise, this method calls the filter's [**CTransformFilter::CheckInputType**](ctransformfilter-checkinputtype.md) method to check the media type.</span></span> <span data-ttu-id="65d75-122">Если входной ПИН-код подключен, он также вызывает метод [**Ипин:: куерякцепт**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) для выходного ПИН-кода вышестоящего выхода.</span><span class="sxs-lookup"><span data-stu-id="65d75-122">If the input pin is connected, it also calls the [**IPin::QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) method on the upstream output pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="65d75-123">Требования</span><span class="sxs-lookup"><span data-stu-id="65d75-123">Requirements</span></span>



| <span data-ttu-id="65d75-124">Требование</span><span class="sxs-lookup"><span data-stu-id="65d75-124">Requirement</span></span> | <span data-ttu-id="65d75-125">Значение</span><span class="sxs-lookup"><span data-stu-id="65d75-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="65d75-126">Header</span><span class="sxs-lookup"><span data-stu-id="65d75-126">Header</span></span><br/>  | <dl> <span data-ttu-id="65d75-127"><dt>Трансип. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="65d75-127"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="65d75-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="65d75-128">Library</span></span><br/> | <dl> <span data-ttu-id="65d75-129"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="65d75-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65d75-130">См. также</span><span class="sxs-lookup"><span data-stu-id="65d75-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65d75-131">**Класс Ктрансинплацеаутпутпин**</span><span class="sxs-lookup"><span data-stu-id="65d75-131">**CTransInPlaceOutputPin Class**</span></span>](ctransinplaceoutputpin.md)
</dt> </dl>

 

 




