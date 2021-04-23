---
description: Метод Счедулесампле планирует пример для подготовки к просмотру.
ms.assetid: 08c218d1-6d0a-4c66-bbde-a39e5d31561c
title: Кбасерендерер. Счедулесампле, метод (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.ScheduleSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c340e54f35b353820b128681cfbc0c5798d38849
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657859"
---
# <a name="cbaserendererschedulesample-method"></a><span data-ttu-id="b6a9d-103">Кбасерендерер. Счедулесампле, метод</span><span class="sxs-lookup"><span data-stu-id="b6a9d-103">CBaseRenderer.ScheduleSample method</span></span>

<span data-ttu-id="b6a9d-104">`ScheduleSample`Метод планирует пример для отрисовки.</span><span class="sxs-lookup"><span data-stu-id="b6a9d-104">The `ScheduleSample` method schedules a sample for rendering.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6a9d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b6a9d-105">Syntax</span></span>


```C++
virtual BOOL ScheduleSample(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a><span data-ttu-id="b6a9d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b6a9d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6a9d-107">*пмедиасампле*</span><span class="sxs-lookup"><span data-stu-id="b6a9d-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="b6a9d-108">Указатель на интерфейс [**имедиасампле**](/windows/desktop/api/Strmif/nn-strmif-imediasample) образца.</span><span class="sxs-lookup"><span data-stu-id="b6a9d-108">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6a9d-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b6a9d-109">Return value</span></span>

<span data-ttu-id="b6a9d-110">Возвращает **значение true** , если образец был запланирован, или **значение false** , если образец был удален.</span><span class="sxs-lookup"><span data-stu-id="b6a9d-110">Returns **TRUE** if the sample was scheduled, or **FALSE** if the sample was dropped.</span></span>

## <a name="remarks"></a><span data-ttu-id="b6a9d-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b6a9d-111">Remarks</span></span>

<span data-ttu-id="b6a9d-112">Этот метод сначала определяет, должен ли образец быть визуализирован немедленно, визуализирован в будущем или удален.</span><span class="sxs-lookup"><span data-stu-id="b6a9d-112">This method first determines whether the sample should be rendered immediately, rendered in the future, or dropped.</span></span> <span data-ttu-id="b6a9d-113">(Для этого вызывается метод [**кбасерендерер:: жетсамплетимес**](cbaserenderer-getsampletimes.md) .) Если образец должен быть визуализирован немедленно, метод сигнализирует о событии [**кбасерендерер:: m \_ рендеревент**](cbaserenderer-m-renderevent.md) .</span><span class="sxs-lookup"><span data-stu-id="b6a9d-113">(To do so, it calls the [**CBaseRenderer::GetSampleTimes**](cbaserenderer-getsampletimes.md) method.) If the sample should be rendered immediately, the method signals the [**CBaseRenderer::m\_RenderEvent**](cbaserenderer-m-renderevent.md) event.</span></span> <span data-ttu-id="b6a9d-114">Если образец должен быть визуализирован в будущем, метод вызывает метод [**иреференцеклокк:: адвисетиме**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-advisetime) для планирования.</span><span class="sxs-lookup"><span data-stu-id="b6a9d-114">If the sample should be rendered in the future, the method calls the [**IReferenceClock::AdviseTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-advisetime) method for scheduling.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6a9d-115">Требования</span><span class="sxs-lookup"><span data-stu-id="b6a9d-115">Requirements</span></span>



| <span data-ttu-id="b6a9d-116">Требование</span><span class="sxs-lookup"><span data-stu-id="b6a9d-116">Requirement</span></span> | <span data-ttu-id="b6a9d-117">Значение</span><span class="sxs-lookup"><span data-stu-id="b6a9d-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6a9d-118">Header</span><span class="sxs-lookup"><span data-stu-id="b6a9d-118">Header</span></span><br/>  | <dl> <span data-ttu-id="b6a9d-119"><dt>Ренбасе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b6a9d-119"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b6a9d-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="b6a9d-120">Library</span></span><br/> | <dl> <span data-ttu-id="b6a9d-121"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="b6a9d-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b6a9d-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b6a9d-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6a9d-123">**Класс Кбасерендерер**</span><span class="sxs-lookup"><span data-stu-id="b6a9d-123">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




