---
description: Метод Ваитфоррендертиме ожидает время показа текущего образца.
ms.assetid: a6acb780-48df-4f73-adcb-cfa4e54b19ac
title: Кбасерендерер. Ваитфоррендертиме, метод (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.WaitForRenderTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 43a537728ca0874fa1dfd69b4712bcc97cf23850
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105656856"
---
# <a name="cbaserendererwaitforrendertime-method"></a><span data-ttu-id="bce64-103">Кбасерендерер. Ваитфоррендертиме, метод</span><span class="sxs-lookup"><span data-stu-id="bce64-103">CBaseRenderer.WaitForRenderTime method</span></span>

<span data-ttu-id="bce64-104">`WaitForRenderTime`Метод ожидает время показа текущего образца.</span><span class="sxs-lookup"><span data-stu-id="bce64-104">The `WaitForRenderTime` method waits for the current sample's presentation time.</span></span>

## <a name="syntax"></a><span data-ttu-id="bce64-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bce64-105">Syntax</span></span>


```C++
virtual HRESULT WaitForRenderTime();
```



## <a name="parameters"></a><span data-ttu-id="bce64-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="bce64-106">Parameters</span></span>

<span data-ttu-id="bce64-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="bce64-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="bce64-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bce64-108">Return value</span></span>

<span data-ttu-id="bce64-109">Возвращает одно из следующих значений **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="bce64-109">Returns one of the following **HRESULT** values.</span></span>



| <span data-ttu-id="bce64-110">Код возврата</span><span class="sxs-lookup"><span data-stu-id="bce64-110">Return code</span></span>                                                                                           | <span data-ttu-id="bce64-111">Описание</span><span class="sxs-lookup"><span data-stu-id="bce64-111">Description</span></span>                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <span data-ttu-id="bce64-112"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="bce64-112"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="bce64-113">Успешно.</span><span class="sxs-lookup"><span data-stu-id="bce64-113">Success.</span></span><br/>                                                       |
| <dl> <span data-ttu-id="bce64-114"><dt>**\_ \_ изменение состояния VFW \_ E**</dt></span><span class="sxs-lookup"><span data-stu-id="bce64-114"><dt>**VFW\_E\_STATE\_CHANGED**</dt></span></span> </dl> | <span data-ttu-id="bce64-115">Состояние фильтра изменилось до того, как было получено время презентации.</span><span class="sxs-lookup"><span data-stu-id="bce64-115">The filter state changed before the presentation time arrived.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="bce64-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bce64-116">Remarks</span></span>

<span data-ttu-id="bce64-117">Этот метод ожидает, пока не произойдет одно из следующих событий:</span><span class="sxs-lookup"><span data-stu-id="bce64-117">This method waits until one of the following occurs:</span></span>

-   <span data-ttu-id="bce64-118">Получено время презентации в примере, после чего образец можно визуализировать.</span><span class="sxs-lookup"><span data-stu-id="bce64-118">The sample's presentation time arrives, at which point the sample can be rendered.</span></span>
-   <span data-ttu-id="bce64-119">Фильтр останавливает или начинает запись данных.</span><span class="sxs-lookup"><span data-stu-id="bce64-119">The filter stops or begins flushing data.</span></span>

<span data-ttu-id="bce64-120">При наступлении времени презентации отображается событие [**кбасерендерер:: m \_ рендеревент**](cbaserenderer-m-renderevent.md) .</span><span class="sxs-lookup"><span data-stu-id="bce64-120">If the presentation time arrives, the [**CBaseRenderer::m\_RenderEvent**](cbaserenderer-m-renderevent.md) event is signaled.</span></span> <span data-ttu-id="bce64-121">При изменении состояния происходит сигнал о событии [**кбасерендерер:: m \_ среадсигнал**](cbaserenderer-m-threadsignal.md) .</span><span class="sxs-lookup"><span data-stu-id="bce64-121">If the state changes, the [**CBaseRenderer::m\_ThreadSignal**](cbaserenderer-m-threadsignal.md) event is signaled.</span></span> <span data-ttu-id="bce64-122">Этот метод ожидает оба события.</span><span class="sxs-lookup"><span data-stu-id="bce64-122">This method waits on both events.</span></span> <span data-ttu-id="bce64-123">Производный класс может переопределить этот метод для ожидания дополнительных событий, если это необходимо.</span><span class="sxs-lookup"><span data-stu-id="bce64-123">The derived class can override this method to wait on additional events, if necessary.</span></span>

<span data-ttu-id="bce64-124">Этот метод вызывает метод [**кбасерендерер:: онваитстарт**](cbaserenderer-onwaitstart.md) , когда начинается ожидание, и метод [**Кбасерендерер:: онваитенд**](cbaserenderer-onwaitend.md) по завершении ожидания.</span><span class="sxs-lookup"><span data-stu-id="bce64-124">This method calls the [**CBaseRenderer::OnWaitStart**](cbaserenderer-onwaitstart.md) method when the wait begins, and the [**CBaseRenderer::OnWaitEnd**](cbaserenderer-onwaitend.md) method when the wait is done.</span></span> <span data-ttu-id="bce64-125">Ни один из методов не выполняет никаких действий в базовом классе, но производный класс может их переопределить.</span><span class="sxs-lookup"><span data-stu-id="bce64-125">Neither method does anything in the base class, but the derived class can override them.</span></span>

## <a name="requirements"></a><span data-ttu-id="bce64-126">Требования</span><span class="sxs-lookup"><span data-stu-id="bce64-126">Requirements</span></span>



| <span data-ttu-id="bce64-127">Требование</span><span class="sxs-lookup"><span data-stu-id="bce64-127">Requirement</span></span> | <span data-ttu-id="bce64-128">Значение</span><span class="sxs-lookup"><span data-stu-id="bce64-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bce64-129">Header</span><span class="sxs-lookup"><span data-stu-id="bce64-129">Header</span></span><br/>  | <dl> <span data-ttu-id="bce64-130"><dt>Ренбасе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bce64-130"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="bce64-131">Библиотека</span><span class="sxs-lookup"><span data-stu-id="bce64-131">Library</span></span><br/> | <dl> <span data-ttu-id="bce64-132"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="bce64-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bce64-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bce64-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bce64-134">**Класс Кбасерендерер**</span><span class="sxs-lookup"><span data-stu-id="bce64-134">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




