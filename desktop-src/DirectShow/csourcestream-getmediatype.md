---
description: Метод Жетмедиатипе извлекает предпочтительный тип мультимедиа.
ms.assetid: c5c5f498-a9a3-4ce7-8cf5-941397aa649d
title: Метод Ксаурцестреам. Жетмедиатипе (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.GetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8475a26bf10ff10993925a5e313c941dcce720bc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657628"
---
# <a name="csourcestreamgetmediatype-method-sourceh"></a><span data-ttu-id="6fd28-103">Метод Ксаурцестреам. Жетмедиатипе (Source. h)</span><span class="sxs-lookup"><span data-stu-id="6fd28-103">CSourceStream.GetMediaType method (Source.h)</span></span>

<span data-ttu-id="6fd28-104">Метод **жетмедиатипе** извлекает предпочтительный тип мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="6fd28-104">The **GetMediaType** method retrieves a preferred media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="6fd28-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6fd28-105">Syntax</span></span>


```C++
virtual HRESULT GetMediaType(
   int        iPosition,
   CMediaType *pMediaType
);
```



## <a name="parameters"></a><span data-ttu-id="6fd28-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6fd28-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6fd28-107">*Интерфейс*</span><span class="sxs-lookup"><span data-stu-id="6fd28-107">*iPosition*</span></span> 
</dt> <dd>

<span data-ttu-id="6fd28-108">Значение индекса, начинающееся с нуля.</span><span class="sxs-lookup"><span data-stu-id="6fd28-108">Zero-based index value.</span></span>

</dd> <dt>

<span data-ttu-id="6fd28-109">*пмедиатипе*</span><span class="sxs-lookup"><span data-stu-id="6fd28-109">*pMediaType*</span></span> 
</dt> <dd>

<span data-ttu-id="6fd28-110">Указатель на объект [**кмедиатипе**](cmediatype.md) , который получает тип мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="6fd28-110">Pointer to a [**CMediaType**](cmediatype.md) object that receives the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6fd28-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6fd28-111">Return value</span></span>

<span data-ttu-id="6fd28-112">Возвращает одно из значений **HRESULT** , приведенных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="6fd28-112">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="6fd28-113">Код возврата</span><span class="sxs-lookup"><span data-stu-id="6fd28-113">Return code</span></span>                                                                                            | <span data-ttu-id="6fd28-114">Описание</span><span class="sxs-lookup"><span data-stu-id="6fd28-114">Description</span></span>                      |
|--------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="6fd28-115"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="6fd28-115"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="6fd28-116">Успешно.</span><span class="sxs-lookup"><span data-stu-id="6fd28-116">Success.</span></span><br/>              |
| <dl> <span data-ttu-id="6fd28-117"><dt>**VFW \_ S \_ больше \_ \_ элементов**</dt></span><span class="sxs-lookup"><span data-stu-id="6fd28-117"><dt>**VFW\_S\_NO\_MORE\_ITEMS**</dt></span></span> </dl> | <span data-ttu-id="6fd28-118">Индекс вне допустимого диапазона.</span><span class="sxs-lookup"><span data-stu-id="6fd28-118">Index out of range.</span></span><br/>   |
| <dl> <span data-ttu-id="6fd28-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="6fd28-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl>           | <span data-ttu-id="6fd28-120">Индекс меньше нуля.</span><span class="sxs-lookup"><span data-stu-id="6fd28-120">Index less than zero.</span></span><br/> |
| <dl> <span data-ttu-id="6fd28-121"><dt>**\_непредвиденная E**</dt></span><span class="sxs-lookup"><span data-stu-id="6fd28-121"><dt>**E\_UNEXPECTED**</dt></span></span> </dl>           | <span data-ttu-id="6fd28-122">Непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="6fd28-122">Unexpected error.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="6fd28-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6fd28-123">Remarks</span></span>

<span data-ttu-id="6fd28-124">Существует две версии этого метода.</span><span class="sxs-lookup"><span data-stu-id="6fd28-124">There are two versions of this method.</span></span> <span data-ttu-id="6fd28-125">Одна версия переопределяет метод [**кбасепин:: жетмедиатипе**](cbasepin-getmediatype.md) и принимает значение индекса в качестве параметра.</span><span class="sxs-lookup"><span data-stu-id="6fd28-125">One version overrides the [**CBasePin::GetMediaType**](cbasepin-getmediatype.md) method and takes an index value as a parameter.</span></span> <span data-ttu-id="6fd28-126">Другая версия предназначена для получения одного типа мультимедиа, поэтому в нем отсутствует параметр index.</span><span class="sxs-lookup"><span data-stu-id="6fd28-126">The other version is designed to retrieve a single media type, so it lacks the index parameter.</span></span>

<span data-ttu-id="6fd28-127">Метод с одним параметром возвращает E \_ непредвиденное значение.</span><span class="sxs-lookup"><span data-stu-id="6fd28-127">The single-parameter method returns E\_UNEXPECTED.</span></span> <span data-ttu-id="6fd28-128">Метод с двумя параметрами проверяет, что параметр *интерфейс* равен нулю, а затем вызывает версию с одним параметром.</span><span class="sxs-lookup"><span data-stu-id="6fd28-128">The two-parameter method verifies that the *iPosition* parameter is zero and then calls the single-parameter version.</span></span> <span data-ttu-id="6fd28-129">В зависимости от числа типов носителей, поддерживаемых ПИН-кодом, необходимо переопределить один из следующих методов:</span><span class="sxs-lookup"><span data-stu-id="6fd28-129">Depending on the number of media types the pin supports, you must override one of these methods:</span></span>

-   <span data-ttu-id="6fd28-130">Если ПИН-код поддерживает ровно один тип носителя, переопределите версию с одним параметром.</span><span class="sxs-lookup"><span data-stu-id="6fd28-130">If the pin supports exactly one media type, override the single-parameter version.</span></span> <span data-ttu-id="6fd28-131">Укажите тип носителя, который поддерживает ПИН-код.</span><span class="sxs-lookup"><span data-stu-id="6fd28-131">Fill in the media type that the pin supports.</span></span>
-   <span data-ttu-id="6fd28-132">Если ПИН-код поддерживает более одного типа носителей, переопределите версию с двумя параметрами.</span><span class="sxs-lookup"><span data-stu-id="6fd28-132">If the pin supports more than one media type, override the two-parameter version.</span></span> <span data-ttu-id="6fd28-133">Также Переопределите метод [**ксаурцестреам:: чеккмедиатипе**](csourcestream-checkmediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="6fd28-133">Also override the [**CSourceStream::CheckMediaType**](csourcestream-checkmediatype.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="6fd28-134">Требования</span><span class="sxs-lookup"><span data-stu-id="6fd28-134">Requirements</span></span>



| <span data-ttu-id="6fd28-135">Требование</span><span class="sxs-lookup"><span data-stu-id="6fd28-135">Requirement</span></span> | <span data-ttu-id="6fd28-136">Значение</span><span class="sxs-lookup"><span data-stu-id="6fd28-136">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6fd28-137">Header</span><span class="sxs-lookup"><span data-stu-id="6fd28-137">Header</span></span><br/>  | <dl> <span data-ttu-id="6fd28-138"><dt>Source. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6fd28-138"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="6fd28-139">Библиотека</span><span class="sxs-lookup"><span data-stu-id="6fd28-139">Library</span></span><br/> | <dl> <span data-ttu-id="6fd28-140"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="6fd28-140"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6fd28-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6fd28-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6fd28-142">**Класс Ксаурцестреам**</span><span class="sxs-lookup"><span data-stu-id="6fd28-142">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




