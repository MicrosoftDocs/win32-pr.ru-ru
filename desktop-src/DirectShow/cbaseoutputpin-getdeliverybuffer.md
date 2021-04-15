---
description: Метод Жетделиверибуффер извлекает пример носителя, содержащий пустой буфер.
ms.assetid: 5a20c11b-50f8-443e-a4d5-6bcffde741d5
title: Кбасеаутпутпин. Жетделиверибуффер, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.GetDeliveryBuffer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 332fad740c1ea904feee1a437273f21eb4c1def0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669174"
---
# <a name="cbaseoutputpingetdeliverybuffer-method"></a><span data-ttu-id="cd18b-103">Кбасеаутпутпин. Жетделиверибуффер, метод</span><span class="sxs-lookup"><span data-stu-id="cd18b-103">CBaseOutputPin.GetDeliveryBuffer method</span></span>

<span data-ttu-id="cd18b-104">`GetDeliveryBuffer`Метод получает пример носителя, который содержит пустой буфер.</span><span class="sxs-lookup"><span data-stu-id="cd18b-104">The `GetDeliveryBuffer` method retrieves a media sample that contains an empty buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd18b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cd18b-105">Syntax</span></span>


```C++
virtual HRESULT GetDeliveryBuffer(
   IMediaSample   **ppSample,
   REFERENCE_TIME *pStartTime,
   REFERENCE_TIME *pEndTime,
   DWORD          dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="cd18b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="cd18b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd18b-107">*ппсампле*</span><span class="sxs-lookup"><span data-stu-id="cd18b-107">*ppSample*</span></span> 
</dt> <dd>

<span data-ttu-id="cd18b-108">Адрес переменной, которая получает указатель на интерфейс [**имедиасампле**](/windows/desktop/api/Strmif/nn-strmif-imediasample) буфера.</span><span class="sxs-lookup"><span data-stu-id="cd18b-108">Address of a variable that receives a pointer to the buffer's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> <dt>

<span data-ttu-id="cd18b-109">*пстарттиме*</span><span class="sxs-lookup"><span data-stu-id="cd18b-109">*pStartTime*</span></span> 
</dt> <dd>

<span data-ttu-id="cd18b-110">Указатель на время начала выборки или **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="cd18b-110">Pointer to the start time of the sample, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="cd18b-111">*пендтиме*</span><span class="sxs-lookup"><span data-stu-id="cd18b-111">*pEndTime*</span></span> 
</dt> <dd>

<span data-ttu-id="cd18b-112">Указатель на время окончания выборки или **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="cd18b-112">Pointer to the ending time of the sample, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="cd18b-113">*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="cd18b-113">*dwFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="cd18b-114">Побитовое сочетание флагов, поддерживаемых интерфейсом [**имемаллокатор::/buffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) .</span><span class="sxs-lookup"><span data-stu-id="cd18b-114">Bitwise combination of flags supported by the [**IMemAllocator::GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd18b-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cd18b-115">Return value</span></span>

<span data-ttu-id="cd18b-116">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="cd18b-116">Returns an **HRESULT** value.</span></span> <span data-ttu-id="cd18b-117">Возможные значения включают перечисленные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="cd18b-117">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="cd18b-118">Код возврата</span><span class="sxs-lookup"><span data-stu-id="cd18b-118">Return code</span></span>                                                                                   | <span data-ttu-id="cd18b-119">Описание</span><span class="sxs-lookup"><span data-stu-id="cd18b-119">Description</span></span>                        |
|-----------------------------------------------------------------------------------------------|------------------------------------|
| <dl> <span data-ttu-id="cd18b-120"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="cd18b-120"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="cd18b-121">Успешно.</span><span class="sxs-lookup"><span data-stu-id="cd18b-121">Success.</span></span><br/>                |
| <dl> <span data-ttu-id="cd18b-122"><dt>**\_интерфейс E**</dt></span><span class="sxs-lookup"><span data-stu-id="cd18b-122"><dt>**E\_NOINTERFACE**</dt></span></span> </dl> | <span data-ttu-id="cd18b-123">Распределитель недоступен.</span><span class="sxs-lookup"><span data-stu-id="cd18b-123">No allocator available.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="cd18b-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cd18b-124">Remarks</span></span>

<span data-ttu-id="cd18b-125">Этот метод вызывает метод **имемаллокатор::/buffer** для распределителя и передает параметры в этот метод.</span><span class="sxs-lookup"><span data-stu-id="cd18b-125">This method calls the **IMemAllocator::GetBuffer** method on the allocator, and passes the parameters to that method.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd18b-126">Требования</span><span class="sxs-lookup"><span data-stu-id="cd18b-126">Requirements</span></span>



| <span data-ttu-id="cd18b-127">Требование</span><span class="sxs-lookup"><span data-stu-id="cd18b-127">Requirement</span></span> | <span data-ttu-id="cd18b-128">Значение</span><span class="sxs-lookup"><span data-stu-id="cd18b-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd18b-129">Header</span><span class="sxs-lookup"><span data-stu-id="cd18b-129">Header</span></span><br/>  | <dl> <span data-ttu-id="cd18b-130"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cd18b-130"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="cd18b-131">Библиотека</span><span class="sxs-lookup"><span data-stu-id="cd18b-131">Library</span></span><br/> | <dl> <span data-ttu-id="cd18b-132"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="cd18b-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd18b-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cd18b-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd18b-134">**Класс Кбасеаутпутпин**</span><span class="sxs-lookup"><span data-stu-id="cd18b-134">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




