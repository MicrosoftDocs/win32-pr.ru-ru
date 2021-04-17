---
description: Метод Сетмедиатипе вызывается, когда тип мультимедиа задан на одном из ПИН-кодов фильтра.
ms.assetid: 3e505036-7fa6-42cf-a683-3a39a43d209d
title: Ктрансформфилтер. Сетмедиатипе, метод (Трансфрм. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.SetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 86e9eac76ccc178659935511d75b1676a136a1c4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679633"
---
# <a name="ctransformfiltersetmediatype-method"></a><span data-ttu-id="6bbde-103">Ктрансформфилтер. Сетмедиатипе, метод</span><span class="sxs-lookup"><span data-stu-id="6bbde-103">CTransformFilter.SetMediaType method</span></span>

<span data-ttu-id="6bbde-104">`SetMediaType`Метод вызывается, когда тип мультимедиа задан на одном из ПИН-кодов фильтра.</span><span class="sxs-lookup"><span data-stu-id="6bbde-104">The `SetMediaType` method is called when the media type is set on one of the filter's pins.</span></span>

## <a name="syntax"></a><span data-ttu-id="6bbde-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6bbde-105">Syntax</span></span>


```C++
virtual HRESULT SetMediaType(
         PIN_DIRECTION direction,
   const CMediaType    *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="6bbde-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6bbde-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6bbde-107">*direction*</span><span class="sxs-lookup"><span data-stu-id="6bbde-107">*direction*</span></span> 
</dt> <dd>

<span data-ttu-id="6bbde-108">Член перечисленного типа с [**\_ направлением ПИН-кода**](/windows/win32/api/strmif/ne-strmif-pin_direction) , указывая ПИН-код для фильтра (входные или выходные данные).</span><span class="sxs-lookup"><span data-stu-id="6bbde-108">Member of the [**PIN\_DIRECTION**](/windows/win32/api/strmif/ne-strmif-pin_direction) enumerated type, specifying a pin on the filter (input or output).</span></span>

</dd> <dt>

<span data-ttu-id="6bbde-109">*состоит*</span><span class="sxs-lookup"><span data-stu-id="6bbde-109">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="6bbde-110">Указатель на объект [**кмедиатипе**](cmediatype.md) , указывающий тип мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="6bbde-110">Pointer to a [**CMediaType**](cmediatype.md) object that specifies the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6bbde-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6bbde-111">Return value</span></span>

<span data-ttu-id="6bbde-112">Возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="6bbde-112">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="6bbde-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6bbde-113">Remarks</span></span>

<span data-ttu-id="6bbde-114">Методы [**ктрансформинпутпин:: сетмедиатипе**](ctransforminputpin-setmediatype.md) и [**Ктрансформаутпутпин:: сетмедиатипе**](ctransformoutputpin-setmediatype.md) вызывают этот метод, если задан тип носителя ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="6bbde-114">The [**CTransformInputPin::SetMediaType**](ctransforminputpin-setmediatype.md) and [**CTransformOutputPin::SetMediaType**](ctransformoutputpin-setmediatype.md) methods call this method when a pin's media type is set.</span></span> <span data-ttu-id="6bbde-115">Этот метод не выполняет никаких действий в базовом классе, но производный класс может его переопределить.</span><span class="sxs-lookup"><span data-stu-id="6bbde-115">This method does nothing in the base class, but the derived class can override it.</span></span>

## <a name="requirements"></a><span data-ttu-id="6bbde-116">Требования</span><span class="sxs-lookup"><span data-stu-id="6bbde-116">Requirements</span></span>



| <span data-ttu-id="6bbde-117">Требование</span><span class="sxs-lookup"><span data-stu-id="6bbde-117">Requirement</span></span> | <span data-ttu-id="6bbde-118">Значение</span><span class="sxs-lookup"><span data-stu-id="6bbde-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6bbde-119">Header</span><span class="sxs-lookup"><span data-stu-id="6bbde-119">Header</span></span><br/>  | <dl> <span data-ttu-id="6bbde-120"><dt>Трансфрм. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6bbde-120"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="6bbde-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="6bbde-121">Library</span></span><br/> | <dl> <span data-ttu-id="6bbde-122"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="6bbde-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6bbde-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6bbde-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6bbde-124">**Класс Ктрансформфилтер**</span><span class="sxs-lookup"><span data-stu-id="6bbde-124">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




