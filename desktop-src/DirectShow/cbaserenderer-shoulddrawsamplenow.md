---
description: Метод Шаулддравсампленов определяет, как запланировано Отображение образца.
ms.assetid: 92994f1f-53d5-42d4-90a2-2984b693e4c0
title: Кбасерендерер. Шаулддравсампленов, метод (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.ShouldDrawSampleNow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 27fbf603fd670cac2a39831114a7f141b17ffd2e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657993"
---
# <a name="cbaserenderershoulddrawsamplenow-method"></a><span data-ttu-id="7c76e-103">Кбасерендерер. Шаулддравсампленов, метод</span><span class="sxs-lookup"><span data-stu-id="7c76e-103">CBaseRenderer.ShouldDrawSampleNow method</span></span>

<span data-ttu-id="7c76e-104">`ShouldDrawSampleNow`Метод определяет, как запланировано Отображение образца.</span><span class="sxs-lookup"><span data-stu-id="7c76e-104">The `ShouldDrawSampleNow` method determines how a sample is scheduled for rendering.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c76e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7c76e-105">Syntax</span></span>


```C++
virtual HRESULT ShouldDrawSampleNow(
   IMediaSample   *pMediaSample,
   REFERENCE_TIME *pStartTime,
   REFERENCE_TIME *pEndTime
);
```



## <a name="parameters"></a><span data-ttu-id="7c76e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7c76e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c76e-107">*пмедиасампле*</span><span class="sxs-lookup"><span data-stu-id="7c76e-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="7c76e-108">Указатель на интерфейс [**имедиасампле**](/windows/desktop/api/Strmif/nn-strmif-imediasample) образца.</span><span class="sxs-lookup"><span data-stu-id="7c76e-108">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> <dt>

<span data-ttu-id="7c76e-109">*пстарттиме*</span><span class="sxs-lookup"><span data-stu-id="7c76e-109">*pStartTime*</span></span> 
</dt> <dd>

<span data-ttu-id="7c76e-110">Указатель на переменную, которая содержит время начала выборки.</span><span class="sxs-lookup"><span data-stu-id="7c76e-110">Pointer to a variable that contains the sample's start time.</span></span>

</dd> <dt>

<span data-ttu-id="7c76e-111">*пендтиме*</span><span class="sxs-lookup"><span data-stu-id="7c76e-111">*pEndTime*</span></span> 
</dt> <dd>

<span data-ttu-id="7c76e-112">Указатель на переменную, содержащую время окончания выборки.</span><span class="sxs-lookup"><span data-stu-id="7c76e-112">Pointer to a variable that contains the sample's end time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c76e-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7c76e-113">Return value</span></span>

<span data-ttu-id="7c76e-114">Возвращает \_ значение false.</span><span class="sxs-lookup"><span data-stu-id="7c76e-114">Returns S\_FALSE.</span></span> <span data-ttu-id="7c76e-115">Если производный класс переопределяет этот метод, возвратите одно из значений, приведенных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="7c76e-115">If the derived class overrides this method, return one of the values shown in the following table.</span></span>



| <span data-ttu-id="7c76e-116">Код возврата</span><span class="sxs-lookup"><span data-stu-id="7c76e-116">Return code</span></span>                                                                               | <span data-ttu-id="7c76e-117">Описание</span><span class="sxs-lookup"><span data-stu-id="7c76e-117">Description</span></span>                                                                        |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7c76e-118"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="7c76e-118"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="7c76e-119">Пример должен быть визуализирован немедленно.</span><span class="sxs-lookup"><span data-stu-id="7c76e-119">The sample should be rendered immediately.</span></span><br/>                              |
| <dl> <span data-ttu-id="7c76e-120"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="7c76e-120"><dt>**S\_FALSE**</dt></span></span> </dl>   | <span data-ttu-id="7c76e-121">Пример должен быть запланирован для подготовки к просмотру на основе меток времени.</span><span class="sxs-lookup"><span data-stu-id="7c76e-121">The sample should be scheduled for rendering, based on the time stamps.</span></span><br/> |
| <dl> <span data-ttu-id="7c76e-122"><dt>**Код ошибки**</dt></span><span class="sxs-lookup"><span data-stu-id="7c76e-122"><dt>**Error code**</dt></span></span> </dl> | <span data-ttu-id="7c76e-123">Не выводите этот пример.</span><span class="sxs-lookup"><span data-stu-id="7c76e-123">Do not render this sample.</span></span><br/>                                              |



 

## <a name="remarks"></a><span data-ttu-id="7c76e-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7c76e-124">Remarks</span></span>

<span data-ttu-id="7c76e-125">Метод [**кбасерендерер:: жетсамплетимес**](cbaserenderer-getsampletimes.md) вызывает этот метод.</span><span class="sxs-lookup"><span data-stu-id="7c76e-125">The [**CBaseRenderer::GetSampleTimes**](cbaserenderer-getsampletimes.md) method calls this method.</span></span> <span data-ttu-id="7c76e-126">По умолчанию образцы всегда планируются для отрисовки на основе их штампов времени.</span><span class="sxs-lookup"><span data-stu-id="7c76e-126">By default, samples are always scheduled for rendering based on their time stamps.</span></span> <span data-ttu-id="7c76e-127">Производный класс может переопределить этот метод. Например, для реализации контроля качества.</span><span class="sxs-lookup"><span data-stu-id="7c76e-127">The derived class can override this method; for example, to implement quality control.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c76e-128">Требования</span><span class="sxs-lookup"><span data-stu-id="7c76e-128">Requirements</span></span>



| <span data-ttu-id="7c76e-129">Требование</span><span class="sxs-lookup"><span data-stu-id="7c76e-129">Requirement</span></span> | <span data-ttu-id="7c76e-130">Значение</span><span class="sxs-lookup"><span data-stu-id="7c76e-130">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c76e-131">Header</span><span class="sxs-lookup"><span data-stu-id="7c76e-131">Header</span></span><br/>  | <dl> <span data-ttu-id="7c76e-132"><dt>Ренбасе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7c76e-132"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="7c76e-133">Библиотека</span><span class="sxs-lookup"><span data-stu-id="7c76e-133">Library</span></span><br/> | <dl> <span data-ttu-id="7c76e-134"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="7c76e-134"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c76e-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7c76e-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c76e-136">**Класс Кбасерендерер**</span><span class="sxs-lookup"><span data-stu-id="7c76e-136">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




