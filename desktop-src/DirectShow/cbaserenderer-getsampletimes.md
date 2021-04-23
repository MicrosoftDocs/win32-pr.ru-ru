---
description: Метод Жетсамплетимес извлекает метки времени из образца.
ms.assetid: a8fead22-a12c-489d-9c42-d5b61f480c25
title: Кбасерендерер. Жетсамплетимес, метод (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.GetSampleTimes
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6c389c2ea55ddb15c59fe30e03f392d68aa3b5ac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657057"
---
# <a name="cbaserenderergetsampletimes-method"></a><span data-ttu-id="71c94-103">Кбасерендерер. Жетсамплетимес, метод</span><span class="sxs-lookup"><span data-stu-id="71c94-103">CBaseRenderer.GetSampleTimes method</span></span>

<span data-ttu-id="71c94-104">`GetSampleTimes`Метод извлекает метки времени из образца.</span><span class="sxs-lookup"><span data-stu-id="71c94-104">The `GetSampleTimes` method retrieves the time stamps from a sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="71c94-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="71c94-105">Syntax</span></span>


```C++
virtual HRESULT GetSampleTimes(
   IMediaSample   *pMediaSample,
   REFERENCE_TIME *pStartTime,
   REFERENCE_TIME *pEndTime
);
```



## <a name="parameters"></a><span data-ttu-id="71c94-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="71c94-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71c94-107">*пмедиасампле*</span><span class="sxs-lookup"><span data-stu-id="71c94-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="71c94-108">Указатель на интерфейс [**имедиасампле**](/windows/desktop/api/Strmif/nn-strmif-imediasample) образца.</span><span class="sxs-lookup"><span data-stu-id="71c94-108">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> <dt>

<span data-ttu-id="71c94-109">*пстарттиме*</span><span class="sxs-lookup"><span data-stu-id="71c94-109">*pStartTime*</span></span> 
</dt> <dd>

<span data-ttu-id="71c94-110">Указатель на переменную, которая получает время начала.</span><span class="sxs-lookup"><span data-stu-id="71c94-110">Pointer to a variable that receives the start time.</span></span>

</dd> <dt>

<span data-ttu-id="71c94-111">*пендтиме*</span><span class="sxs-lookup"><span data-stu-id="71c94-111">*pEndTime*</span></span> 
</dt> <dd>

<span data-ttu-id="71c94-112">Указатель на переменную, которая получает время окончания.</span><span class="sxs-lookup"><span data-stu-id="71c94-112">Pointer to a variable that receives the end time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71c94-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="71c94-113">Return value</span></span>

<span data-ttu-id="71c94-114">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="71c94-114">Returns an **HRESULT** value.</span></span> <span data-ttu-id="71c94-115">Возможные значения включают в себя, показанные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="71c94-115">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="71c94-116">Код возврата</span><span class="sxs-lookup"><span data-stu-id="71c94-116">Return code</span></span>                                                                                                    | <span data-ttu-id="71c94-117">Описание</span><span class="sxs-lookup"><span data-stu-id="71c94-117">Description</span></span>                                                                        |
|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="71c94-118"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="71c94-118"><dt>**S\_OK**</dt></span></span> </dl>                           | <span data-ttu-id="71c94-119">Пример должен быть визуализирован немедленно.</span><span class="sxs-lookup"><span data-stu-id="71c94-119">The sample should be rendered immediately.</span></span><br/>                              |
| <dl> <span data-ttu-id="71c94-120"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="71c94-120"><dt>**S\_FALSE**</dt></span></span> </dl>                        | <span data-ttu-id="71c94-121">Пример должен быть запланирован для подготовки к просмотру на основе меток времени.</span><span class="sxs-lookup"><span data-stu-id="71c94-121">The sample should be scheduled for rendering, based on the time stamps.</span></span><br/> |
| <dl> <span data-ttu-id="71c94-122"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="71c94-122"><dt>**E\_FAIL**</dt></span></span> </dl>                         | <span data-ttu-id="71c94-123">Не выводите этот пример.</span><span class="sxs-lookup"><span data-stu-id="71c94-123">Do not render this sample.</span></span><br/>                                              |
| <dl> <span data-ttu-id="71c94-124"><dt>**время начала работы с VFW \_ E \_ \_ \_ после \_ окончания**</dt></span><span class="sxs-lookup"><span data-stu-id="71c94-124"><dt>**VFW\_E\_START\_TIME\_AFTER\_END**</dt></span></span> </dl> | <span data-ttu-id="71c94-125">Неправильная отметка времени: время окончания предшествует времени начала.</span><span class="sxs-lookup"><span data-stu-id="71c94-125">Bad time stamp: The end time is earlier than the start time.</span></span><br/>            |



 

## <a name="remarks"></a><span data-ttu-id="71c94-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="71c94-126">Remarks</span></span>

<span data-ttu-id="71c94-127">Фильтр вызывает этот метод, чтобы определить, как он должен работать с примером.</span><span class="sxs-lookup"><span data-stu-id="71c94-127">The filter calls this method to determine how it should handle a sample.</span></span> <span data-ttu-id="71c94-128">Если возвращаемое значение равно S \_ , то фильтр немедленно выводит пример.</span><span class="sxs-lookup"><span data-stu-id="71c94-128">If the return value is S\_OK, the filter renders the sample immediately.</span></span> <span data-ttu-id="71c94-129">Если возвращаемое значение равно S \_ , то фильтр планирует подготовку к просмотру на основе меток времени.</span><span class="sxs-lookup"><span data-stu-id="71c94-129">If the return value is S\_FALSE, the filter schedules the sample for rendering, based on the time stamps.</span></span> <span data-ttu-id="71c94-130">Если возвращаемое значение является кодом ошибки, то фильтр отклоняет выборку.</span><span class="sxs-lookup"><span data-stu-id="71c94-130">If the return value is an error code, the filter rejects the sample.</span></span>

<span data-ttu-id="71c94-131">Этот метод возвращает значение \_ ОК, если в образце нет штампов времени или если фильтр не имеет контрольного времени.</span><span class="sxs-lookup"><span data-stu-id="71c94-131">This method returns S\_OK if the sample has no time stamps, or if the filter does not have a reference clock.</span></span> <span data-ttu-id="71c94-132">В противном случае возвращается значение метода [**кбасерендерер:: шаулддравсампленов**](cbaserenderer-shoulddrawsamplenow.md) .</span><span class="sxs-lookup"><span data-stu-id="71c94-132">Otherwise, it returns the value of the [**CBaseRenderer::ShouldDrawSampleNow**](cbaserenderer-shoulddrawsamplenow.md) method.</span></span> <span data-ttu-id="71c94-133">В базовом классе **шаулддравсампленов** всегда возвращает значение S \_ false.</span><span class="sxs-lookup"><span data-stu-id="71c94-133">In the base class, **ShouldDrawSampleNow** always returns S\_FALSE.</span></span> <span data-ttu-id="71c94-134">Производный класс может переопределить это поведение.</span><span class="sxs-lookup"><span data-stu-id="71c94-134">The derived class can override this behavior.</span></span> <span data-ttu-id="71c94-135">Например, если производный класс реализует управление качеством, он может вернуть «E \_ не удалось удалить образец».</span><span class="sxs-lookup"><span data-stu-id="71c94-135">For example, if the derived class implements quality control management, it might return E\_FAIL to drop a sample.</span></span>

## <a name="requirements"></a><span data-ttu-id="71c94-136">Требования</span><span class="sxs-lookup"><span data-stu-id="71c94-136">Requirements</span></span>



| <span data-ttu-id="71c94-137">Требование</span><span class="sxs-lookup"><span data-stu-id="71c94-137">Requirement</span></span> | <span data-ttu-id="71c94-138">Значение</span><span class="sxs-lookup"><span data-stu-id="71c94-138">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="71c94-139">Header</span><span class="sxs-lookup"><span data-stu-id="71c94-139">Header</span></span><br/>  | <dl> <span data-ttu-id="71c94-140"><dt>Ренбасе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="71c94-140"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="71c94-141">Библиотека</span><span class="sxs-lookup"><span data-stu-id="71c94-141">Library</span></span><br/> | <dl> <span data-ttu-id="71c94-142"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="71c94-142"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71c94-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="71c94-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71c94-144">**Класс Кбасерендерер**</span><span class="sxs-lookup"><span data-stu-id="71c94-144">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




