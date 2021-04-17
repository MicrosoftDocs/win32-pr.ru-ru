---
description: Если достигнут конец потока, метод Сендендофстреам планирует \_ событие EC Complete для диспетчера графа фильтров.
ms.assetid: 3c10c956-e352-4796-a8cd-cc69a02066f2
title: Кбасерендерер. Сендендофстреам, метод (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.SendEndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f04e4c8c90796aafb64870a9d59d38b0a33e7435
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665407"
---
# <a name="cbaserenderersendendofstream-method"></a><span data-ttu-id="e0594-103">Кбасерендерер. Сендендофстреам, метод</span><span class="sxs-lookup"><span data-stu-id="e0594-103">CBaseRenderer.SendEndOfStream method</span></span>

<span data-ttu-id="e0594-104">Если достигнут конец потока, `SendEndOfStream` метод планирует \_ событие EC Complete для диспетчера графа фильтров.</span><span class="sxs-lookup"><span data-stu-id="e0594-104">If end-of-stream was reached, the `SendEndOfStream` method schedules an EC\_COMPLETE event for the filter graph manager.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0594-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e0594-105">Syntax</span></span>


```C++
virtual HRESULT SendEndOfStream();
```



## <a name="parameters"></a><span data-ttu-id="e0594-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e0594-106">Parameters</span></span>

<span data-ttu-id="e0594-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="e0594-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e0594-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e0594-108">Return value</span></span>

<span data-ttu-id="e0594-109">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e0594-109">Returns an **HRESULT** value.</span></span> <span data-ttu-id="e0594-110">Возможные значения перечислены в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="e0594-110">Possible values include those in the following table.</span></span>



| <span data-ttu-id="e0594-111">Код возврата</span><span class="sxs-lookup"><span data-stu-id="e0594-111">Return code</span></span>                                                                             | <span data-ttu-id="e0594-112">Описание</span><span class="sxs-lookup"><span data-stu-id="e0594-112">Description</span></span>                                                               |
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e0594-113"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="e0594-113"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="e0594-114">Диспетчер графов фильтров не принимает уведомления о событиях.</span><span class="sxs-lookup"><span data-stu-id="e0594-114">The filter graph manager is not accepting event notifications.</span></span><br/> |
| <dl> <span data-ttu-id="e0594-115"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="e0594-115"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="e0594-116">Успешно.</span><span class="sxs-lookup"><span data-stu-id="e0594-116">Success.</span></span><br/>                                                       |



 

## <a name="remarks"></a><span data-ttu-id="e0594-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e0594-117">Remarks</span></span>

<span data-ttu-id="e0594-118">Фильтр может получить уведомление о завершении потока до времени окончания текущего образца.</span><span class="sxs-lookup"><span data-stu-id="e0594-118">The filter might receive an end-of-stream notification before the current sample's stop time.</span></span> <span data-ttu-id="e0594-119">В этом случае фильтр должен подождать перед тем, как опубликовать уведомление о [**\_ завершении EC**](ec-complete.md) в диспетчере графов фильтров.</span><span class="sxs-lookup"><span data-stu-id="e0594-119">If so, the filter should wait before posting an [**EC\_COMPLETE**](ec-complete.md) notification to the filter graph manager.</span></span>

<span data-ttu-id="e0594-120">Таким образом:</span><span class="sxs-lookup"><span data-stu-id="e0594-120">Therefore:</span></span>

-   <span data-ttu-id="e0594-121">Если фильтр получил уведомление раннего конца потока (EOS), этот метод планирует событие таймера.</span><span class="sxs-lookup"><span data-stu-id="e0594-121">If the filter has received an early end-of-stream (EOS) notification, this method schedules a timer event.</span></span> <span data-ttu-id="e0594-122">Когда событие таймера активировано, фильтр отправляет \_ событие EC Complete.</span><span class="sxs-lookup"><span data-stu-id="e0594-122">When the timer event is activated, the filter posts the EC\_COMPLETE event.</span></span>
-   <span data-ttu-id="e0594-123">Если фильтр получил уведомление EOS, которое не было раньше, этот метод \_ немедленно отправляет событие EC Complete.</span><span class="sxs-lookup"><span data-stu-id="e0594-123">If the filter has received an EOS notification that was not early, this method posts the EC\_COMPLETE event immediately.</span></span>
-   <span data-ttu-id="e0594-124">Если фильтр не имеет ожидающих уведомлений EOS, метод возвращается без выполнения каких-либо действий.</span><span class="sxs-lookup"><span data-stu-id="e0594-124">If the filter does not have any pending EOS notification, the method returns without doing anything.</span></span>

<span data-ttu-id="e0594-125">Метод обратного вызова таймера — [**кбасерендерер:: TimerCallback**](cbaserenderer-timercallback.md).</span><span class="sxs-lookup"><span data-stu-id="e0594-125">The timer callback method is [**CBaseRenderer::TimerCallback**](cbaserenderer-timercallback.md).</span></span> <span data-ttu-id="e0594-126">Для доставки события EC \_ Complete фильтр вызывает метод [**кбасерендерер:: нотифендофстреам**](cbaserenderer-notifyendofstream.md) .</span><span class="sxs-lookup"><span data-stu-id="e0594-126">To deliver the EC\_COMPLETE event, the filter calls the [**CBaseRenderer::NotifyEndOfStream**](cbaserenderer-notifyendofstream.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0594-127">Требования</span><span class="sxs-lookup"><span data-stu-id="e0594-127">Requirements</span></span>



| <span data-ttu-id="e0594-128">Требование</span><span class="sxs-lookup"><span data-stu-id="e0594-128">Requirement</span></span> | <span data-ttu-id="e0594-129">Значение</span><span class="sxs-lookup"><span data-stu-id="e0594-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0594-130">Header</span><span class="sxs-lookup"><span data-stu-id="e0594-130">Header</span></span><br/>  | <dl> <span data-ttu-id="e0594-131"><dt>Ренбасе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e0594-131"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e0594-132">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e0594-132">Library</span></span><br/> | <dl> <span data-ttu-id="e0594-133"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="e0594-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0594-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e0594-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0594-135">**Класс Кбасерендерер**</span><span class="sxs-lookup"><span data-stu-id="e0594-135">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




