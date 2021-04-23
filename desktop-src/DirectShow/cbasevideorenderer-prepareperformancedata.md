---
description: Метод Препареперформанцедата задает \_ значения m трлате и m \_ трфраме текущего кадра.
ms.assetid: c4c5701b-eccd-4259-a1d1-7c5000f6b2df
title: Кбасевидеорендерер. Препареперформанцедата, метод (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.PreparePerformanceData
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 12dd61dee7416ce8ca7ac07cba62cbc769df5973
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105656966"
---
# <a name="cbasevideorendererprepareperformancedata-method"></a><span data-ttu-id="8ce6a-103">Кбасевидеорендерер. Препареперформанцедата, метод</span><span class="sxs-lookup"><span data-stu-id="8ce6a-103">CBaseVideoRenderer.PreparePerformanceData method</span></span>

<span data-ttu-id="8ce6a-104">`PreparePerformanceData`Метод задает значения **m \_ трлате** и **m \_ трфраме** для текущего кадра.</span><span class="sxs-lookup"><span data-stu-id="8ce6a-104">The `PreparePerformanceData` method sets the **m\_trLate** and **m\_trFrame** values of the current frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ce6a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8ce6a-105">Syntax</span></span>


```C++
void PreparePerformanceData(
   int trLate,
   int trFrame
);
```



## <a name="parameters"></a><span data-ttu-id="8ce6a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8ce6a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ce6a-107">*трлате*</span><span class="sxs-lookup"><span data-stu-id="8ce6a-107">*trLate*</span></span> 
</dt> <dd>

<span data-ttu-id="8ce6a-108">Значение, указывающее, насколько поздно образец превысил время его выполнения в ссылочных единицах времени.</span><span class="sxs-lookup"><span data-stu-id="8ce6a-108">Value indicating how late the sample was beyond its due time, in reference time units.</span></span>

</dd> <dt>

<span data-ttu-id="8ce6a-109">*трфраме*</span><span class="sxs-lookup"><span data-stu-id="8ce6a-109">*trFrame*</span></span> 
</dt> <dd>

<span data-ttu-id="8ce6a-110">Время между кадрами, в ссылочных единицах времени.</span><span class="sxs-lookup"><span data-stu-id="8ce6a-110">Interframe time, in reference time units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ce6a-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8ce6a-111">Return value</span></span>

<span data-ttu-id="8ce6a-112">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="8ce6a-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8ce6a-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8ce6a-113">Remarks</span></span>

<span data-ttu-id="8ce6a-114">Эта функция члена устанавливает **m \_ трлате** в значение *трлате* и **m \_ трфраме** в значение *трфраме*.</span><span class="sxs-lookup"><span data-stu-id="8ce6a-114">This member function sets **m\_trLate** to the value of *trLate* and **m\_trFrame** to the value of *trFrame*.</span></span>

<span data-ttu-id="8ce6a-115">Когда функция-член [**кбасевидеорендерер:: рекордфрамелатенесс**](cbasevideorenderer-recordframelateness.md) вызывается из [**Кбасевидеорендерер:: онрендерстарт**](cbasevideorenderer-onrenderstart.md) или [**кбасевидеорендерер:: OnDirectRender**](cbasevideorenderer-ondirectrender.md), она передает значения **m \_ trLate** и **m \_ trFrame** для обновления статистики.</span><span class="sxs-lookup"><span data-stu-id="8ce6a-115">When the [**CBaseVideoRenderer::RecordFrameLateness**](cbasevideorenderer-recordframelateness.md) member function is called from either [**CBaseVideoRenderer::OnRenderStart**](cbasevideorenderer-onrenderstart.md) or [**CBaseVideoRenderer::OnDirectRender**](cbasevideorenderer-ondirectrender.md), it passes the values of **m\_trLate** and **m\_trFrame** for it to update the statistics.</span></span> <span data-ttu-id="8ce6a-116">`PreparePerformanceData` вызывается из [**кбасевидеорендерер:: онваитенд**](cbasevideorenderer-onwaitend.md) для задания этих значений элементов данных.</span><span class="sxs-lookup"><span data-stu-id="8ce6a-116">`PreparePerformanceData` is called from [**CBaseVideoRenderer::OnWaitEnd**](cbasevideorenderer-onwaitend.md) to set these data member values.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ce6a-117">Требования</span><span class="sxs-lookup"><span data-stu-id="8ce6a-117">Requirements</span></span>



| <span data-ttu-id="8ce6a-118">Требование</span><span class="sxs-lookup"><span data-stu-id="8ce6a-118">Requirement</span></span> | <span data-ttu-id="8ce6a-119">Значение</span><span class="sxs-lookup"><span data-stu-id="8ce6a-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ce6a-120">Header</span><span class="sxs-lookup"><span data-stu-id="8ce6a-120">Header</span></span><br/>  | <dl> <span data-ttu-id="8ce6a-121"><dt>Ренбасе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8ce6a-121"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="8ce6a-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="8ce6a-122">Library</span></span><br/> | <dl> <span data-ttu-id="8ce6a-123"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="8ce6a-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ce6a-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8ce6a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ce6a-125">**Класс Кбасевидеорендерер**</span><span class="sxs-lookup"><span data-stu-id="8ce6a-125">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




