---
description: Метод Жетмедиатипе извлекает предпочтительный тип мультимедиа.
ms.assetid: 85605885-adb5-4f13-91af-48bf74684eca
title: Ксаурцестреам. Жетмедиатипе, метод (Source. h) — параметр Пмедиатипе
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
ms.openlocfilehash: 8306da8451d4af7da8ce4f4c7d4d3f6fd367e1ec
ms.sourcegitcommit: 4d4a6e9ad5de37e467cd3164276771b71e1f113f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/05/2021
ms.locfileid: "106389187"
---
# <a name="csourcestreamgetmediatype-method-sourceh"></a><span data-ttu-id="224f6-103">Метод Ксаурцестреам. Жетмедиатипе (Source. h)</span><span class="sxs-lookup"><span data-stu-id="224f6-103">CSourceStream.GetMediaType method (Source.h)</span></span>

<span data-ttu-id="224f6-104">`GetMediaType`Метод извлекает предпочтительный тип мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="224f6-104">The `GetMediaType` method retrieves a preferred media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="224f6-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="224f6-105">Syntax</span></span>


```C++
virtual HRESULT GetMediaType(
   CMediaType *pMediaType
);
```



## <a name="parameters"></a><span data-ttu-id="224f6-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="224f6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="224f6-107">*пмедиатипе*</span><span class="sxs-lookup"><span data-stu-id="224f6-107">*pMediaType*</span></span> 
</dt> <dd>

<span data-ttu-id="224f6-108">Указатель на объект [**кмедиатипе**](cmediatype.md) , который получает тип мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="224f6-108">Pointer to a [**CMediaType**](cmediatype.md) object that receives the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="224f6-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="224f6-109">Return value</span></span>

<span data-ttu-id="224f6-110">Возвращает одно из значений **HRESULT** , приведенных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="224f6-110">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="224f6-111">Код возврата</span><span class="sxs-lookup"><span data-stu-id="224f6-111">Return code</span></span>                                                                                            | <span data-ttu-id="224f6-112">Описание</span><span class="sxs-lookup"><span data-stu-id="224f6-112">Description</span></span>                      |
|--------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="224f6-113"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="224f6-113"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="224f6-114">Успешно.</span><span class="sxs-lookup"><span data-stu-id="224f6-114">Success.</span></span><br/>              |
| <dl> <span data-ttu-id="224f6-115"><dt>**VFW \_ S \_ больше \_ \_ элементов**</dt></span><span class="sxs-lookup"><span data-stu-id="224f6-115"><dt>**VFW\_S\_NO\_MORE\_ITEMS**</dt></span></span> </dl> | <span data-ttu-id="224f6-116">Индекс вне допустимого диапазона.</span><span class="sxs-lookup"><span data-stu-id="224f6-116">Index out of range.</span></span><br/>   |
| <dl> <span data-ttu-id="224f6-117"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="224f6-117"><dt>**E\_INVALIDARG**</dt></span></span> </dl>           | <span data-ttu-id="224f6-118">Индекс меньше нуля.</span><span class="sxs-lookup"><span data-stu-id="224f6-118">Index less than zero.</span></span><br/> |
| <dl> <span data-ttu-id="224f6-119"><dt>**\_непредвиденная E**</dt></span><span class="sxs-lookup"><span data-stu-id="224f6-119"><dt>**E\_UNEXPECTED**</dt></span></span> </dl>           | <span data-ttu-id="224f6-120">Непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="224f6-120">Unexpected error.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="224f6-121">Remarks</span><span class="sxs-lookup"><span data-stu-id="224f6-121">Remarks</span></span>

<span data-ttu-id="224f6-122">Существует две версии этого метода.</span><span class="sxs-lookup"><span data-stu-id="224f6-122">There are two versions of this method.</span></span> <span data-ttu-id="224f6-123">Одна версия переопределяет метод [**кбасепин:: жетмедиатипе**](cbasepin-getmediatype.md) и принимает значение индекса в качестве параметра.</span><span class="sxs-lookup"><span data-stu-id="224f6-123">One version overrides the [**CBasePin::GetMediaType**](cbasepin-getmediatype.md) method and takes an index value as a parameter.</span></span> <span data-ttu-id="224f6-124">Другая версия предназначена для получения одного типа мультимедиа, поэтому в нем отсутствует параметр index.</span><span class="sxs-lookup"><span data-stu-id="224f6-124">The other version is designed to retrieve a single media type, so it lacks the index parameter.</span></span>

<span data-ttu-id="224f6-125">Метод с одним параметром возвращает E \_ непредвиденное значение.</span><span class="sxs-lookup"><span data-stu-id="224f6-125">The single-parameter method returns E\_UNEXPECTED.</span></span> <span data-ttu-id="224f6-126">Метод с двумя параметрами проверяет, что параметр *интерфейс* равен нулю, а затем вызывает версию с одним параметром.</span><span class="sxs-lookup"><span data-stu-id="224f6-126">The two-parameter method verifies that the *iPosition* parameter is zero and then calls the single-parameter version.</span></span> <span data-ttu-id="224f6-127">В зависимости от числа типов носителей, поддерживаемых ПИН-кодом, необходимо переопределить один из следующих методов:</span><span class="sxs-lookup"><span data-stu-id="224f6-127">Depending on the number of media types the pin supports, you must override one of these methods:</span></span>

-   <span data-ttu-id="224f6-128">Если ПИН-код поддерживает ровно один тип носителя, переопределите версию с одним параметром.</span><span class="sxs-lookup"><span data-stu-id="224f6-128">If the pin supports exactly one media type, override the single-parameter version.</span></span> <span data-ttu-id="224f6-129">Укажите тип носителя, который поддерживает ПИН-код.</span><span class="sxs-lookup"><span data-stu-id="224f6-129">Fill in the media type that the pin supports.</span></span>
-   <span data-ttu-id="224f6-130">Если ПИН-код поддерживает более одного типа носителей, переопределите версию с двумя параметрами.</span><span class="sxs-lookup"><span data-stu-id="224f6-130">If the pin supports more than one media type, override the two-parameter version.</span></span> <span data-ttu-id="224f6-131">Также Переопределите метод [**ксаурцестреам:: чеккмедиатипе**](csourcestream-checkmediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="224f6-131">Also override the [**CSourceStream::CheckMediaType**](csourcestream-checkmediatype.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="224f6-132">Требования</span><span class="sxs-lookup"><span data-stu-id="224f6-132">Requirements</span></span>



| <span data-ttu-id="224f6-133">Требование</span><span class="sxs-lookup"><span data-stu-id="224f6-133">Requirement</span></span> | <span data-ttu-id="224f6-134">Значение</span><span class="sxs-lookup"><span data-stu-id="224f6-134">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="224f6-135">Заголовок</span><span class="sxs-lookup"><span data-stu-id="224f6-135">Header</span></span><br/>  | <dl> <span data-ttu-id="224f6-136"><dt>Source. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="224f6-136"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="224f6-137">Библиотека</span><span class="sxs-lookup"><span data-stu-id="224f6-137">Library</span></span><br/> | <dl> <span data-ttu-id="224f6-138"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="224f6-138"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="224f6-139">См. также</span><span class="sxs-lookup"><span data-stu-id="224f6-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="224f6-140">**Класс Ксаурцестреам**</span><span class="sxs-lookup"><span data-stu-id="224f6-140">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




