---
description: 'Метод Чеккмедиатипе определяет, принимает ли ПИН-код конкретный тип носителя. Этот метод реализует чистый виртуальный метод Кбасепин:: Чеккмедиатипе.'
ms.assetid: 3db7c74c-a6aa-4b49-b2a5-9bf8db35fd7e
title: Метод Ксаурцестреам. Чеккмедиатипе (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.CheckMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 62f8b6c18613f5c187fc637febd08b74260a1e44
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657445"
---
# <a name="csourcestreamcheckmediatype-method"></a><span data-ttu-id="763d2-104">Ксаурцестреам. Чеккмедиатипе, метод</span><span class="sxs-lookup"><span data-stu-id="763d2-104">CSourceStream.CheckMediaType method</span></span>

<span data-ttu-id="763d2-105">`CheckMediaType`Метод определяет, принимает ли ПИН-код конкретный тип носителя.</span><span class="sxs-lookup"><span data-stu-id="763d2-105">The `CheckMediaType` method determines if the pin accepts a specific media type.</span></span> <span data-ttu-id="763d2-106">Этот метод реализует чистый виртуальный метод [**кбасепин:: чеккмедиатипе**](cbasepin-checkmediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="763d2-106">This method implements the pure virtual [**CBasePin::CheckMediaType**](cbasepin-checkmediatype.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="763d2-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="763d2-107">Syntax</span></span>


```C++
virtual HRESULT CheckMediaType(
   const CMediaType *pMediaType
);
```



## <a name="parameters"></a><span data-ttu-id="763d2-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="763d2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="763d2-109">*пмедиатипе*</span><span class="sxs-lookup"><span data-stu-id="763d2-109">*pMediaType*</span></span> 
</dt> <dd>

<span data-ttu-id="763d2-110">Указатель на объект [**кмедиатипе**](cmediatype.md) , который содержит предложенный тип мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="763d2-110">Pointer to a [**CMediaType**](cmediatype.md) object that contains the proposed media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="763d2-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="763d2-111">Return value</span></span>

<span data-ttu-id="763d2-112">Возвращает одно из значений **HRESULT** , приведенных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="763d2-112">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="763d2-113">Код возврата</span><span class="sxs-lookup"><span data-stu-id="763d2-113">Return code</span></span>                                                                            | <span data-ttu-id="763d2-114">Описание</span><span class="sxs-lookup"><span data-stu-id="763d2-114">Description</span></span>                                          |
|----------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="763d2-115"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="763d2-115"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="763d2-116">Этот ПИН-код поддерживает этот тип носителя.</span><span class="sxs-lookup"><span data-stu-id="763d2-116">This pin supports this media type.</span></span><br/>        |
| <dl> <span data-ttu-id="763d2-117"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="763d2-117"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="763d2-118">ПИН-код не поддерживает этот тип носителя.</span><span class="sxs-lookup"><span data-stu-id="763d2-118">The pin does not support this media type.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="763d2-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="763d2-119">Remarks</span></span>

<span data-ttu-id="763d2-120">По умолчанию ПИН-код поддерживает один тип носителя.</span><span class="sxs-lookup"><span data-stu-id="763d2-120">By default, the pin supports a single media type.</span></span> <span data-ttu-id="763d2-121">Этот метод извлекает поддерживаемый тип, вызывая версию с одним параметром метода [**ксаурцестреам:: жетмедиатипе**](csourcestream-getmediatype.md) и сравнивая его с предложенным типом.</span><span class="sxs-lookup"><span data-stu-id="763d2-121">This method retrieves the supported type by calling the single-parameter version of the [**CSourceStream::GetMediaType**](csourcestream-getmediatype.md) method, and compares it to the proposed type.</span></span> <span data-ttu-id="763d2-122">Если ПИН-код поддерживает более одного типа носителей, Переопределите этот метод.</span><span class="sxs-lookup"><span data-stu-id="763d2-122">If your pin supports more than one media type, override this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="763d2-123">Требования</span><span class="sxs-lookup"><span data-stu-id="763d2-123">Requirements</span></span>



| <span data-ttu-id="763d2-124">Требование</span><span class="sxs-lookup"><span data-stu-id="763d2-124">Requirement</span></span> | <span data-ttu-id="763d2-125">Значение</span><span class="sxs-lookup"><span data-stu-id="763d2-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="763d2-126">Header</span><span class="sxs-lookup"><span data-stu-id="763d2-126">Header</span></span><br/>  | <dl> <span data-ttu-id="763d2-127"><dt>Source. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="763d2-127"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="763d2-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="763d2-128">Library</span></span><br/> | <dl> <span data-ttu-id="763d2-129"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="763d2-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="763d2-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="763d2-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="763d2-131">**Класс Ксаурцестреам**</span><span class="sxs-lookup"><span data-stu-id="763d2-131">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




