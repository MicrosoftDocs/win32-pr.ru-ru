---
description: Метод Жетмедиатипе извлекает предпочтительный тип мультимедиа по значению индекса.
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
ms.openlocfilehash: e52a5bc3b6a2b931a8592372e2ef636863c50ef6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105676057"
---
# <a name="ctransformoutputpingetmediatype-method"></a><span data-ttu-id="ae0bf-103">Ктрансформаутпутпин. Жетмедиатипе, метод</span><span class="sxs-lookup"><span data-stu-id="ae0bf-103">CTransformOutputPin.GetMediaType method</span></span>

<span data-ttu-id="ae0bf-104">`GetMediaType`Метод получает предпочтительный тип мультимедиа по значению индекса.</span><span class="sxs-lookup"><span data-stu-id="ae0bf-104">The `GetMediaType` method retrieves a preferred media type, by index value.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae0bf-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ae0bf-105">Syntax</span></span>


```C++
HRESULT GetMediaType(
   int        iPosition,
   CMediaType *pMediaType
);
```



## <a name="parameters"></a><span data-ttu-id="ae0bf-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ae0bf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae0bf-107">*Интерфейс*</span><span class="sxs-lookup"><span data-stu-id="ae0bf-107">*iPosition*</span></span> 
</dt> <dd>

<span data-ttu-id="ae0bf-108">Значение индекса, начинающееся с нуля.</span><span class="sxs-lookup"><span data-stu-id="ae0bf-108">Zero-based index value.</span></span>

</dd> <dt>

<span data-ttu-id="ae0bf-109">*пмедиатипе*</span><span class="sxs-lookup"><span data-stu-id="ae0bf-109">*pMediaType*</span></span> 
</dt> <dd>

<span data-ttu-id="ae0bf-110">Указатель на объект [**кмедиатипе**](cmediatype.md) , который получает тип мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="ae0bf-110">Pointer to a [**CMediaType**](cmediatype.md) object that receives the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ae0bf-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ae0bf-111">Return value</span></span>

<span data-ttu-id="ae0bf-112">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ae0bf-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="ae0bf-113">Возможные значения включают в себя, показанные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="ae0bf-113">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="ae0bf-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="ae0bf-114">Return code</span></span>                                                                                            | <span data-ttu-id="ae0bf-115">Описание</span><span class="sxs-lookup"><span data-stu-id="ae0bf-115">Description</span></span>                   |
|--------------------------------------------------------------------------------------------------------|-------------------------------|
| <dl> <span data-ttu-id="ae0bf-116"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="ae0bf-116"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="ae0bf-117">Успешно</span><span class="sxs-lookup"><span data-stu-id="ae0bf-117">Success</span></span><br/>            |
| <dl> <span data-ttu-id="ae0bf-118"><dt>**VFW \_ S \_ больше \_ \_ элементов**</dt></span><span class="sxs-lookup"><span data-stu-id="ae0bf-118"><dt>**VFW\_S\_NO\_MORE\_ITEMS**</dt></span></span> </dl> | <span data-ttu-id="ae0bf-119">Индекс вне допустимого диапазона</span><span class="sxs-lookup"><span data-stu-id="ae0bf-119">Index out of range</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ae0bf-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ae0bf-120">Remarks</span></span>

<span data-ttu-id="ae0bf-121">Этот метод переопределяет метод [**кбасепин:: жетмедиатипе**](cbasepin-getmediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="ae0bf-121">This method overrides the [**CBasePin::GetMediaType**](cbasepin-getmediatype.md) method.</span></span> <span data-ttu-id="ae0bf-122">Если входной ПИН-код фильтра не соединен, метод возвращает VFW s больше \_ \_ \_ \_ элементов.</span><span class="sxs-lookup"><span data-stu-id="ae0bf-122">If the filter's input pin is not connected, the method returns VFW\_S\_NO\_MORE\_ITEMS.</span></span> <span data-ttu-id="ae0bf-123">В противном случае он вызывает метод [**ктрансформфилтер:: жетмедиатипе**](ctransformfilter-getmediatype.md) фильтра для получения типа мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="ae0bf-123">Otherwise, it calls the filter's [**CTransformFilter::GetMediaType**](ctransformfilter-getmediatype.md) method to retrieve the media type.</span></span> <span data-ttu-id="ae0bf-124">Метод **ктрансформфилтер:: жетмедиатипе** является чистым виртуальным; производный класс фильтра должен переопределять его.</span><span class="sxs-lookup"><span data-stu-id="ae0bf-124">The **CTransformFilter::GetMediaType** method is pure virtual; the filter's derived class must override it.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae0bf-125">Требования</span><span class="sxs-lookup"><span data-stu-id="ae0bf-125">Requirements</span></span>



| <span data-ttu-id="ae0bf-126">Требование</span><span class="sxs-lookup"><span data-stu-id="ae0bf-126">Requirement</span></span> | <span data-ttu-id="ae0bf-127">Значение</span><span class="sxs-lookup"><span data-stu-id="ae0bf-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae0bf-128">Header</span><span class="sxs-lookup"><span data-stu-id="ae0bf-128">Header</span></span><br/>  | <dl> <span data-ttu-id="ae0bf-129"><dt>Трансфрм. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ae0bf-129"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="ae0bf-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ae0bf-130">Library</span></span><br/> | <dl> <span data-ttu-id="ae0bf-131"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="ae0bf-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




