---
description: Ктрансформаутпутпин. Жетмедиатипе, метод Жетмедиатипе извлекает предпочтительный тип мультимедиа по значению индекса.
ms.assetid: d106e6d1-66ff-4460-9ea2-c93f16116cf4
title: Ктрансформаутпутпин. Жетмедиатипе, метод (Трансфрм. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.GetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1dd0bf38f2fa3be0e077f2509001680bbfc84e15
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094902"
---
# <a name="ctransformoutputpingetmediatype-method"></a><span data-ttu-id="f985e-103">Ктрансформаутпутпин. Жетмедиатипе, метод</span><span class="sxs-lookup"><span data-stu-id="f985e-103">CTransformOutputPin.GetMediaType method</span></span>

<span data-ttu-id="f985e-104">`GetMediaType`Метод получает предпочтительный тип мультимедиа по значению индекса.</span><span class="sxs-lookup"><span data-stu-id="f985e-104">The `GetMediaType` method retrieves a preferred media type, by index value.</span></span>

## <a name="syntax"></a><span data-ttu-id="f985e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f985e-105">Syntax</span></span>


```C++
HRESULT GetMediaType(
   int        iPosition,
   CMediaType *pMediaType
);
```



## <a name="parameters"></a><span data-ttu-id="f985e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f985e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f985e-107">*Интерфейс*</span><span class="sxs-lookup"><span data-stu-id="f985e-107">*iPosition*</span></span> 
</dt> <dd>

<span data-ttu-id="f985e-108">Значение индекса, начинающееся с нуля.</span><span class="sxs-lookup"><span data-stu-id="f985e-108">Zero-based index value.</span></span>

</dd> <dt>

<span data-ttu-id="f985e-109">*пмедиатипе*</span><span class="sxs-lookup"><span data-stu-id="f985e-109">*pMediaType*</span></span> 
</dt> <dd>

<span data-ttu-id="f985e-110">Указатель на объект [**кмедиатипе**](cmediatype.md) , который получает тип мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="f985e-110">Pointer to a [**CMediaType**](cmediatype.md) object that receives the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f985e-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f985e-111">Return value</span></span>

<span data-ttu-id="f985e-112">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f985e-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="f985e-113">Возможные значения включают в себя, показанные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="f985e-113">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="f985e-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="f985e-114">Return code</span></span>                                                                                            | <span data-ttu-id="f985e-115">Описание</span><span class="sxs-lookup"><span data-stu-id="f985e-115">Description</span></span>                   |
|--------------------------------------------------------------------------------------------------------|-------------------------------|
| <dl> <span data-ttu-id="f985e-116"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="f985e-116"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="f985e-117">Успешное завершение</span><span class="sxs-lookup"><span data-stu-id="f985e-117">Success</span></span><br/>            |
| <dl> <span data-ttu-id="f985e-118"><dt>**VFW \_ S \_ больше \_ \_ элементов**</dt></span><span class="sxs-lookup"><span data-stu-id="f985e-118"><dt>**VFW\_S\_NO\_MORE\_ITEMS**</dt></span></span> </dl> | <span data-ttu-id="f985e-119">Индекс вне допустимого диапазона</span><span class="sxs-lookup"><span data-stu-id="f985e-119">Index out of range</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f985e-120">Remarks</span><span class="sxs-lookup"><span data-stu-id="f985e-120">Remarks</span></span>

<span data-ttu-id="f985e-121">Этот метод переопределяет метод [**кбасепин:: жетмедиатипе**](cbasepin-getmediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="f985e-121">This method overrides the [**CBasePin::GetMediaType**](cbasepin-getmediatype.md) method.</span></span> <span data-ttu-id="f985e-122">Если входной ПИН-код фильтра не соединен, метод возвращает VFW s больше \_ \_ \_ \_ элементов.</span><span class="sxs-lookup"><span data-stu-id="f985e-122">If the filter's input pin is not connected, the method returns VFW\_S\_NO\_MORE\_ITEMS.</span></span> <span data-ttu-id="f985e-123">В противном случае он вызывает метод [**ктрансформфилтер:: жетмедиатипе**](ctransformfilter-getmediatype.md) фильтра для получения типа мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="f985e-123">Otherwise, it calls the filter's [**CTransformFilter::GetMediaType**](ctransformfilter-getmediatype.md) method to retrieve the media type.</span></span> <span data-ttu-id="f985e-124">Метод **ктрансформфилтер:: жетмедиатипе** является чистым виртуальным; производный класс фильтра должен переопределять его.</span><span class="sxs-lookup"><span data-stu-id="f985e-124">The **CTransformFilter::GetMediaType** method is pure virtual; the filter's derived class must override it.</span></span>

## <a name="requirements"></a><span data-ttu-id="f985e-125">Требования</span><span class="sxs-lookup"><span data-stu-id="f985e-125">Requirements</span></span>



| <span data-ttu-id="f985e-126">Требование</span><span class="sxs-lookup"><span data-stu-id="f985e-126">Requirement</span></span> | <span data-ttu-id="f985e-127">Значение</span><span class="sxs-lookup"><span data-stu-id="f985e-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f985e-128">Header</span><span class="sxs-lookup"><span data-stu-id="f985e-128">Header</span></span><br/>  | <dl> <span data-ttu-id="f985e-129"><dt>Трансфрм. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f985e-129"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="f985e-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f985e-130">Library</span></span><br/> | <dl> <span data-ttu-id="f985e-131"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="f985e-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




