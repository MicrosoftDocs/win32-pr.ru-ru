---
description: Метод Жетмедиатипе извлекает предпочтительный тип мультимедиа. Этот метод использует параметры *интерфейс* и *пмедиатипе* .
ms.assetid: c5c5f498-a9a3-4ce7-8cf5-941397aa649d
title: Ксаурцестреам. Жетмедиатипе, метод (Source. h) — параметры интерфейс и Пмедиатипе
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
ms.openlocfilehash: 9d8936f08b952af069812859736a6a13ea9c0e4e
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/02/2021
ms.locfileid: "106187941"
---
# <a name="csourcestreamgetmediatype-method-sourceh---iposition-and-pmediatype-parameters"></a><span data-ttu-id="3c8bb-104">Ксаурцестреам. Жетмедиатипе, метод (Source. h) — параметры интерфейс и Пмедиатипе</span><span class="sxs-lookup"><span data-stu-id="3c8bb-104">CSourceStream.GetMediaType method (Source.h) - iPosition and pMediaType parameters</span></span>

<span data-ttu-id="3c8bb-105">Метод **жетмедиатипе** извлекает предпочтительный тип мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="3c8bb-105">The **GetMediaType** method retrieves a preferred media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c8bb-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3c8bb-106">Syntax</span></span>


```C++
virtual HRESULT GetMediaType(
   int        iPosition,
   CMediaType *pMediaType
);
```



## <a name="parameters"></a><span data-ttu-id="3c8bb-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="3c8bb-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c8bb-108">*Интерфейс*</span><span class="sxs-lookup"><span data-stu-id="3c8bb-108">*iPosition*</span></span> 
</dt> <dd>

<span data-ttu-id="3c8bb-109">Значение индекса, начинающееся с нуля.</span><span class="sxs-lookup"><span data-stu-id="3c8bb-109">Zero-based index value.</span></span>

</dd> <dt>

<span data-ttu-id="3c8bb-110">*пмедиатипе*</span><span class="sxs-lookup"><span data-stu-id="3c8bb-110">*pMediaType*</span></span> 
</dt> <dd>

<span data-ttu-id="3c8bb-111">Указатель на объект [**кмедиатипе**](cmediatype.md) , который получает тип мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="3c8bb-111">Pointer to a [**CMediaType**](cmediatype.md) object that receives the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c8bb-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3c8bb-112">Return value</span></span>

<span data-ttu-id="3c8bb-113">Возвращает одно из значений **HRESULT** , приведенных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="3c8bb-113">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="3c8bb-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="3c8bb-114">Return code</span></span>                                                                                            | <span data-ttu-id="3c8bb-115">Описание</span><span class="sxs-lookup"><span data-stu-id="3c8bb-115">Description</span></span>                      |
|--------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="3c8bb-116"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="3c8bb-116"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="3c8bb-117">Успешно.</span><span class="sxs-lookup"><span data-stu-id="3c8bb-117">Success.</span></span><br/>              |
| <dl> <span data-ttu-id="3c8bb-118"><dt>**VFW \_ S \_ больше \_ \_ элементов**</dt></span><span class="sxs-lookup"><span data-stu-id="3c8bb-118"><dt>**VFW\_S\_NO\_MORE\_ITEMS**</dt></span></span> </dl> | <span data-ttu-id="3c8bb-119">Индекс вне допустимого диапазона.</span><span class="sxs-lookup"><span data-stu-id="3c8bb-119">Index out of range.</span></span><br/>   |
| <dl> <span data-ttu-id="3c8bb-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="3c8bb-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl>           | <span data-ttu-id="3c8bb-121">Индекс меньше нуля.</span><span class="sxs-lookup"><span data-stu-id="3c8bb-121">Index less than zero.</span></span><br/> |
| <dl> <span data-ttu-id="3c8bb-122"><dt>**\_непредвиденная E**</dt></span><span class="sxs-lookup"><span data-stu-id="3c8bb-122"><dt>**E\_UNEXPECTED**</dt></span></span> </dl>           | <span data-ttu-id="3c8bb-123">Непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="3c8bb-123">Unexpected error.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="3c8bb-124">Remarks</span><span class="sxs-lookup"><span data-stu-id="3c8bb-124">Remarks</span></span>

<span data-ttu-id="3c8bb-125">Существует две версии этого метода.</span><span class="sxs-lookup"><span data-stu-id="3c8bb-125">There are two versions of this method.</span></span> <span data-ttu-id="3c8bb-126">Одна версия переопределяет метод [**кбасепин:: жетмедиатипе**](cbasepin-getmediatype.md) и принимает значение индекса в качестве параметра.</span><span class="sxs-lookup"><span data-stu-id="3c8bb-126">One version overrides the [**CBasePin::GetMediaType**](cbasepin-getmediatype.md) method and takes an index value as a parameter.</span></span> <span data-ttu-id="3c8bb-127">Другая версия предназначена для получения одного типа мультимедиа, поэтому в нем отсутствует параметр index.</span><span class="sxs-lookup"><span data-stu-id="3c8bb-127">The other version is designed to retrieve a single media type, so it lacks the index parameter.</span></span>

<span data-ttu-id="3c8bb-128">Метод с одним параметром возвращает E \_ непредвиденное значение.</span><span class="sxs-lookup"><span data-stu-id="3c8bb-128">The single-parameter method returns E\_UNEXPECTED.</span></span> <span data-ttu-id="3c8bb-129">Метод с двумя параметрами проверяет, что параметр *интерфейс* равен нулю, а затем вызывает версию с одним параметром.</span><span class="sxs-lookup"><span data-stu-id="3c8bb-129">The two-parameter method verifies that the *iPosition* parameter is zero and then calls the single-parameter version.</span></span> <span data-ttu-id="3c8bb-130">В зависимости от числа типов носителей, поддерживаемых ПИН-кодом, необходимо переопределить один из следующих методов:</span><span class="sxs-lookup"><span data-stu-id="3c8bb-130">Depending on the number of media types the pin supports, you must override one of these methods:</span></span>

-   <span data-ttu-id="3c8bb-131">Если ПИН-код поддерживает ровно один тип носителя, переопределите версию с одним параметром.</span><span class="sxs-lookup"><span data-stu-id="3c8bb-131">If the pin supports exactly one media type, override the single-parameter version.</span></span> <span data-ttu-id="3c8bb-132">Укажите тип носителя, который поддерживает ПИН-код.</span><span class="sxs-lookup"><span data-stu-id="3c8bb-132">Fill in the media type that the pin supports.</span></span>
-   <span data-ttu-id="3c8bb-133">Если ПИН-код поддерживает более одного типа носителей, переопределите версию с двумя параметрами.</span><span class="sxs-lookup"><span data-stu-id="3c8bb-133">If the pin supports more than one media type, override the two-parameter version.</span></span> <span data-ttu-id="3c8bb-134">Также Переопределите метод [**ксаурцестреам:: чеккмедиатипе**](csourcestream-checkmediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="3c8bb-134">Also override the [**CSourceStream::CheckMediaType**](csourcestream-checkmediatype.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c8bb-135">Требования</span><span class="sxs-lookup"><span data-stu-id="3c8bb-135">Requirements</span></span>



| <span data-ttu-id="3c8bb-136">Требование</span><span class="sxs-lookup"><span data-stu-id="3c8bb-136">Requirement</span></span> | <span data-ttu-id="3c8bb-137">Значение</span><span class="sxs-lookup"><span data-stu-id="3c8bb-137">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c8bb-138">Заголовок</span><span class="sxs-lookup"><span data-stu-id="3c8bb-138">Header</span></span>  | <span data-ttu-id="3c8bb-139">Source. h (включение Streams. h)</span><span class="sxs-lookup"><span data-stu-id="3c8bb-139">Source.h (include Streams.h)</span></span>                                                                                    |
| <span data-ttu-id="3c8bb-140">Библиотека</span><span class="sxs-lookup"><span data-stu-id="3c8bb-140">Library</span></span> | <span data-ttu-id="3c8bb-141">Стрмбасе. lib (розничные сборки); Стрмбасд. lib (отладочные сборки)</span><span class="sxs-lookup"><span data-stu-id="3c8bb-141">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="3c8bb-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3c8bb-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c8bb-143">**Класс Ксаурцестреам**</span><span class="sxs-lookup"><span data-stu-id="3c8bb-143">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




