---
description: Метод Жетмедиатипе извлекает предпочтительный тип мультимедиа для выходного ПИН-кода.
ms.assetid: 1bc6c06d-f399-4b8a-81f2-7fffe4630236
title: Ктрансинплацефилтер. Жетмедиатипе, метод (Трансип. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.GetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d2347e0466a7df848e0f0b2bccec325eedfefc8f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675196"
---
# <a name="ctransinplacefiltergetmediatype-method"></a><span data-ttu-id="22d3c-103">Ктрансинплацефилтер. Жетмедиатипе, метод</span><span class="sxs-lookup"><span data-stu-id="22d3c-103">CTransInPlaceFilter.GetMediaType method</span></span>

<span data-ttu-id="22d3c-104">`GetMediaType`Метод извлекает предпочтительный тип мультимедиа для выходного контакта.</span><span class="sxs-lookup"><span data-stu-id="22d3c-104">The `GetMediaType` method retrieves a preferred media type for the output pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="22d3c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="22d3c-105">Syntax</span></span>


```C++
HRESULT GetMediaType(
   int        iPosition,
   CMediaType *pMediaType
);
```



## <a name="parameters"></a><span data-ttu-id="22d3c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="22d3c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22d3c-107">*Интерфейс*</span><span class="sxs-lookup"><span data-stu-id="22d3c-107">*iPosition*</span></span> 
</dt> <dd>

<span data-ttu-id="22d3c-108">Значение индекса, начинающееся с нуля.</span><span class="sxs-lookup"><span data-stu-id="22d3c-108">Zero-based index value.</span></span>

</dd> <dt>

<span data-ttu-id="22d3c-109">*пмедиатипе*</span><span class="sxs-lookup"><span data-stu-id="22d3c-109">*pMediaType*</span></span> 
</dt> <dd>

<span data-ttu-id="22d3c-110">Указатель на объект [**кмедиатипе**](cmediatype.md) , который получает тип мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="22d3c-110">Pointer to a [**CMediaType**](cmediatype.md) object that receives the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22d3c-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="22d3c-111">Return value</span></span>

<span data-ttu-id="22d3c-112">Возвращает \_ непредвиденное значение E.</span><span class="sxs-lookup"><span data-stu-id="22d3c-112">Returns E\_UNEXPECTED.</span></span>

## <a name="remarks"></a><span data-ttu-id="22d3c-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="22d3c-113">Remarks</span></span>

<span data-ttu-id="22d3c-114">Этот метод переопределяет метод [**ктрансформфилтер:: жетмедиатипе**](ctransformfilter-getmediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="22d3c-114">This method overrides the [**CTransformFilter::GetMediaType**](ctransformfilter-getmediatype.md) method.</span></span> <span data-ttu-id="22d3c-115">В классе **ктрансинплацефилтер** каждый ПИН-код вызывает противоположный подключенный ПИН-код для перечисления предпочтительных типов мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="22d3c-115">In the **CTransInPlaceFilter** class, each pin calls the opposite connected pin to enumerate preferred media types.</span></span> <span data-ttu-id="22d3c-116">Входной ПИН-код вызывает входной ПИН-код подчиненного фильтра, а выходной закрепление вызывает выходной ПИН-код вышестоящего фильтра.</span><span class="sxs-lookup"><span data-stu-id="22d3c-116">The input pin calls the downstream filter's input pin, and the output pin calls the upstream filter's output pin.</span></span> <span data-ttu-id="22d3c-117">Поэтому метод фильтра никогда не `GetMediaType` вызывается.</span><span class="sxs-lookup"><span data-stu-id="22d3c-117">Therefore, the filter's `GetMediaType` method is never called.</span></span>

## <a name="requirements"></a><span data-ttu-id="22d3c-118">Требования</span><span class="sxs-lookup"><span data-stu-id="22d3c-118">Requirements</span></span>



| <span data-ttu-id="22d3c-119">Требование</span><span class="sxs-lookup"><span data-stu-id="22d3c-119">Requirement</span></span> | <span data-ttu-id="22d3c-120">Значение</span><span class="sxs-lookup"><span data-stu-id="22d3c-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="22d3c-121">Header</span><span class="sxs-lookup"><span data-stu-id="22d3c-121">Header</span></span><br/>  | <dl> <span data-ttu-id="22d3c-122"><dt>Трансип. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="22d3c-122"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="22d3c-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="22d3c-123">Library</span></span><br/> | <dl> <span data-ttu-id="22d3c-124"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="22d3c-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22d3c-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="22d3c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22d3c-126">**Класс Ктрансинплацефилтер**</span><span class="sxs-lookup"><span data-stu-id="22d3c-126">**CTransInPlaceFilter Class**</span></span>](ctransinplacefilter.md)
</dt> </dl>

 

 




