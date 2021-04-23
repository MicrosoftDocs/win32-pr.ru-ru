---
description: Метод Чеккмедиатипе определяет, принимает ли ПИН-код конкретный тип носителя.
ms.assetid: 2d5f784a-8970-487d-94ef-d96d04f8eb2e
title: Ктрансинплацеинпутпин. Чеккмедиатипе, метод (Трансип. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceInputPin.CheckMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 22f271759bc0ade6b820aed2039bbc16a2cf4a31
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657087"
---
# <a name="ctransinplaceinputpincheckmediatype-method"></a><span data-ttu-id="f4e3d-103">Ктрансинплацеинпутпин. Чеккмедиатипе, метод</span><span class="sxs-lookup"><span data-stu-id="f4e3d-103">CTransInPlaceInputPin.CheckMediaType method</span></span>

<span data-ttu-id="f4e3d-104">`CheckMediaType`Метод определяет, принимает ли ПИН-код конкретный тип носителя.</span><span class="sxs-lookup"><span data-stu-id="f4e3d-104">The `CheckMediaType` method determines if the pin accepts a specific media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4e3d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f4e3d-105">Syntax</span></span>


```C++
HRESULT CheckMediaType(
   const CMediaType *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="f4e3d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f4e3d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f4e3d-107">*состоит*</span><span class="sxs-lookup"><span data-stu-id="f4e3d-107">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="f4e3d-108">Указатель на объект [**кмедиатипе**](cmediatype.md) , который содержит предложенный тип мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="f4e3d-108">Pointer to a [**CMediaType**](cmediatype.md) object that contains the proposed media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f4e3d-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f4e3d-109">Return value</span></span>

<span data-ttu-id="f4e3d-110">\_Если предложенный тип мультимедиа приемлем, возвращается значение S.</span><span class="sxs-lookup"><span data-stu-id="f4e3d-110">Returns S\_OK if the proposed media type is acceptable.</span></span> <span data-ttu-id="f4e3d-111">В противном случае возвращает \_ значение S false или код ошибки.</span><span class="sxs-lookup"><span data-stu-id="f4e3d-111">Otherwise, returns S\_FALSE or an error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f4e3d-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f4e3d-112">Remarks</span></span>

<span data-ttu-id="f4e3d-113">Этот метод переопределяет метод [**ктрансформинпутпин:: чеккмедиатипе**](ctransforminputpin-checkmediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="f4e3d-113">This method overrides the [**CTransformInputPin::CheckMediaType**](ctransforminputpin-checkmediatype.md) method.</span></span> <span data-ttu-id="f4e3d-114">Он вызывает метод [**ктрансформфилтер:: чеккинпуттипе**](ctransformfilter-checkinputtype.md) фильтра для проверки входного типа.</span><span class="sxs-lookup"><span data-stu-id="f4e3d-114">It calls the filter's [**CTransformFilter::CheckInputType**](ctransformfilter-checkinputtype.md) method to check the input type.</span></span> <span data-ttu-id="f4e3d-115">Если выходной ПИН-код подключен, этот метод также вызывает метод [**Ипин:: куерякцепт**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) для входного ПИН-кода нисходящего входа.</span><span class="sxs-lookup"><span data-stu-id="f4e3d-115">If the output pin is connected, this method also calls the [**IPin::QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) method on the downstream input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="f4e3d-116">Требования</span><span class="sxs-lookup"><span data-stu-id="f4e3d-116">Requirements</span></span>



| <span data-ttu-id="f4e3d-117">Требование</span><span class="sxs-lookup"><span data-stu-id="f4e3d-117">Requirement</span></span> | <span data-ttu-id="f4e3d-118">Значение</span><span class="sxs-lookup"><span data-stu-id="f4e3d-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4e3d-119">Header</span><span class="sxs-lookup"><span data-stu-id="f4e3d-119">Header</span></span><br/>  | <dl> <span data-ttu-id="f4e3d-120"><dt>Трансип. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f4e3d-120"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f4e3d-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f4e3d-121">Library</span></span><br/> | <dl> <span data-ttu-id="f4e3d-122"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="f4e3d-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f4e3d-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f4e3d-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4e3d-124">**Класс Ктрансинплацеинпутпин**</span><span class="sxs-lookup"><span data-stu-id="f4e3d-124">**CTransInPlaceInputPin Class**</span></span>](ctransinplaceinputpin.md)
</dt> </dl>

 

 




