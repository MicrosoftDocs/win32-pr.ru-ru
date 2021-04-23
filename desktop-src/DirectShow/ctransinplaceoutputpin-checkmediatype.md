---
description: Метод Чеккмедиатипе определяет, принимает ли ПИН-код конкретный тип носителя.
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
ms.openlocfilehash: b0a422851bc7e09075076decc39d57b85d1052ab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675155"
---
# <a name="ctransinplaceoutputpincheckmediatype-method"></a><span data-ttu-id="5c813-103">Ктрансинплацеаутпутпин. Чеккмедиатипе, метод</span><span class="sxs-lookup"><span data-stu-id="5c813-103">CTransInPlaceOutputPin.CheckMediaType method</span></span>

<span data-ttu-id="5c813-104">`CheckMediaType`Метод определяет, принимает ли ПИН-код конкретный тип носителя.</span><span class="sxs-lookup"><span data-stu-id="5c813-104">The `CheckMediaType` method determines if the pin accepts a specific media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c813-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5c813-105">Syntax</span></span>


```C++
HRESULT CheckMediaType(
   const CMediaType *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="5c813-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="5c813-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c813-107">*состоит*</span><span class="sxs-lookup"><span data-stu-id="5c813-107">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="5c813-108">Указатель на объект [**кмедиатипе**](cmediatype.md) , который содержит предложенный тип мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="5c813-108">Pointer to a [**CMediaType**](cmediatype.md) object that contains the proposed media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5c813-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5c813-109">Return value</span></span>

<span data-ttu-id="5c813-110">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5c813-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="5c813-111">Возможные значения включают в себя, показанные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="5c813-111">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="5c813-112">Код возврата</span><span class="sxs-lookup"><span data-stu-id="5c813-112">Return code</span></span>                                                                                                | <span data-ttu-id="5c813-113">Описание</span><span class="sxs-lookup"><span data-stu-id="5c813-113">Description</span></span>                         |
|------------------------------------------------------------------------------------------------------------|-------------------------------------|
| <dl> <span data-ttu-id="5c813-114"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="5c813-114"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="5c813-115">Успешно.</span><span class="sxs-lookup"><span data-stu-id="5c813-115">Success.</span></span><br/>                 |
| <dl> <span data-ttu-id="5c813-116"><dt>**\_тип VFW \_ E \_ не \_ принят**</dt></span><span class="sxs-lookup"><span data-stu-id="5c813-116"><dt>**VFW\_E\_TYPE\_NOT\_ACCEPTED**</dt></span></span> </dl> | <span data-ttu-id="5c813-117">Тип носителя не принят.</span><span class="sxs-lookup"><span data-stu-id="5c813-117">Media type not accepted.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="5c813-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5c813-118">Remarks</span></span>

<span data-ttu-id="5c813-119">Этот метод переопределяет метод [**ктрансформаутпутпин:: чеккмедиатипе**](ctransformoutputpin-checkmediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="5c813-119">This method overrides the [**CTransformOutputPin::CheckMediaType**](ctransformoutputpin-checkmediatype.md) method.</span></span>

<span data-ttu-id="5c813-120">Если фильтр уже потоковая передача и использует два распределителя, этот метод отклоняет любые изменения формата.</span><span class="sxs-lookup"><span data-stu-id="5c813-120">If the filter is already streaming and is using two allocators, this method rejects any format changes.</span></span> <span data-ttu-id="5c813-121">В противном случае этот метод вызывает метод [**ктрансформфилтер:: чеккинпуттипе**](ctransformfilter-checkinputtype.md) фильтра для проверки типа мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="5c813-121">Otherwise, this method calls the filter's [**CTransformFilter::CheckInputType**](ctransformfilter-checkinputtype.md) method to check the media type.</span></span> <span data-ttu-id="5c813-122">Если входной ПИН-код подключен, он также вызывает метод [**Ипин:: куерякцепт**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) для выходного ПИН-кода вышестоящего выхода.</span><span class="sxs-lookup"><span data-stu-id="5c813-122">If the input pin is connected, it also calls the [**IPin::QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) method on the upstream output pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="5c813-123">Требования</span><span class="sxs-lookup"><span data-stu-id="5c813-123">Requirements</span></span>



| <span data-ttu-id="5c813-124">Требование</span><span class="sxs-lookup"><span data-stu-id="5c813-124">Requirement</span></span> | <span data-ttu-id="5c813-125">Значение</span><span class="sxs-lookup"><span data-stu-id="5c813-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c813-126">Header</span><span class="sxs-lookup"><span data-stu-id="5c813-126">Header</span></span><br/>  | <dl> <span data-ttu-id="5c813-127"><dt>Трансип. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5c813-127"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="5c813-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="5c813-128">Library</span></span><br/> | <dl> <span data-ttu-id="5c813-129"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="5c813-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c813-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5c813-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c813-131">**Класс Ктрансинплацеаутпутпин**</span><span class="sxs-lookup"><span data-stu-id="5c813-131">**CTransInPlaceOutputPin Class**</span></span>](ctransinplaceoutputpin.md)
</dt> </dl>

 

 




