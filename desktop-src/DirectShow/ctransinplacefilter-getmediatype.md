---
description: Ктрансинплацефилтер. Жетмедиатипе, метод Жетмедиатипе извлекает предпочтительный тип мультимедиа для выходного ПИН-кода.
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
ms.openlocfilehash: 8678f9b18e40f529da282909015a7c75695770ea
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094812"
---
# <a name="ctransinplacefiltergetmediatype-method"></a><span data-ttu-id="df3e2-103">Ктрансинплацефилтер. Жетмедиатипе, метод</span><span class="sxs-lookup"><span data-stu-id="df3e2-103">CTransInPlaceFilter.GetMediaType method</span></span>

<span data-ttu-id="df3e2-104">`GetMediaType`Метод извлекает предпочтительный тип мультимедиа для выходного контакта.</span><span class="sxs-lookup"><span data-stu-id="df3e2-104">The `GetMediaType` method retrieves a preferred media type for the output pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="df3e2-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="df3e2-105">Syntax</span></span>


```C++
HRESULT GetMediaType(
   int        iPosition,
   CMediaType *pMediaType
);
```



## <a name="parameters"></a><span data-ttu-id="df3e2-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="df3e2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df3e2-107">*Интерфейс*</span><span class="sxs-lookup"><span data-stu-id="df3e2-107">*iPosition*</span></span> 
</dt> <dd>

<span data-ttu-id="df3e2-108">Значение индекса, начинающееся с нуля.</span><span class="sxs-lookup"><span data-stu-id="df3e2-108">Zero-based index value.</span></span>

</dd> <dt>

<span data-ttu-id="df3e2-109">*пмедиатипе*</span><span class="sxs-lookup"><span data-stu-id="df3e2-109">*pMediaType*</span></span> 
</dt> <dd>

<span data-ttu-id="df3e2-110">Указатель на объект [**кмедиатипе**](cmediatype.md) , который получает тип мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="df3e2-110">Pointer to a [**CMediaType**](cmediatype.md) object that receives the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df3e2-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="df3e2-111">Return value</span></span>

<span data-ttu-id="df3e2-112">Возвращает \_ непредвиденное значение E.</span><span class="sxs-lookup"><span data-stu-id="df3e2-112">Returns E\_UNEXPECTED.</span></span>

## <a name="remarks"></a><span data-ttu-id="df3e2-113">Remarks</span><span class="sxs-lookup"><span data-stu-id="df3e2-113">Remarks</span></span>

<span data-ttu-id="df3e2-114">Этот метод переопределяет метод [**ктрансформфилтер:: жетмедиатипе**](ctransformfilter-getmediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="df3e2-114">This method overrides the [**CTransformFilter::GetMediaType**](ctransformfilter-getmediatype.md) method.</span></span> <span data-ttu-id="df3e2-115">В классе **ктрансинплацефилтер** каждый ПИН-код вызывает противоположный подключенный ПИН-код для перечисления предпочтительных типов мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="df3e2-115">In the **CTransInPlaceFilter** class, each pin calls the opposite connected pin to enumerate preferred media types.</span></span> <span data-ttu-id="df3e2-116">Входной ПИН-код вызывает входной ПИН-код подчиненного фильтра, а выходной закрепление вызывает выходной ПИН-код вышестоящего фильтра.</span><span class="sxs-lookup"><span data-stu-id="df3e2-116">The input pin calls the downstream filter's input pin, and the output pin calls the upstream filter's output pin.</span></span> <span data-ttu-id="df3e2-117">Поэтому метод фильтра никогда не `GetMediaType` вызывается.</span><span class="sxs-lookup"><span data-stu-id="df3e2-117">Therefore, the filter's `GetMediaType` method is never called.</span></span>

## <a name="requirements"></a><span data-ttu-id="df3e2-118">Требования</span><span class="sxs-lookup"><span data-stu-id="df3e2-118">Requirements</span></span>



| <span data-ttu-id="df3e2-119">Требование</span><span class="sxs-lookup"><span data-stu-id="df3e2-119">Requirement</span></span> | <span data-ttu-id="df3e2-120">Значение</span><span class="sxs-lookup"><span data-stu-id="df3e2-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="df3e2-121">Header</span><span class="sxs-lookup"><span data-stu-id="df3e2-121">Header</span></span><br/>  | <dl> <span data-ttu-id="df3e2-122"><dt>Трансип. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="df3e2-122"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="df3e2-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="df3e2-123">Library</span></span><br/> | <dl> <span data-ttu-id="df3e2-124"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="df3e2-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="df3e2-125">См. также</span><span class="sxs-lookup"><span data-stu-id="df3e2-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df3e2-126">**Класс Ктрансинплацефилтер**</span><span class="sxs-lookup"><span data-stu-id="df3e2-126">**CTransInPlaceFilter Class**</span></span>](ctransinplacefilter.md)
</dt> </dl>

 

 




