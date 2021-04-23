---
description: Метод TimerCallback является методом обратного вызова для события таймера конца потока.
ms.assetid: ed43d07a-1ece-43ab-8753-ab14fa388946
title: Кбасерендерер. TimerCallback, метод (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.TimerCallback
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cfa59ca6bed0539caa7eb650458c168999b0de5a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657987"
---
# <a name="cbaserenderertimercallback-method"></a><span data-ttu-id="e9a01-103">Кбасерендерер. TimerCallback, метод</span><span class="sxs-lookup"><span data-stu-id="e9a01-103">CBaseRenderer.TimerCallback method</span></span>

<span data-ttu-id="e9a01-104">`TimerCallback`Метод является методом обратного вызова для события конца потока.</span><span class="sxs-lookup"><span data-stu-id="e9a01-104">The `TimerCallback` method is a callback method for the end-of-stream timer event.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9a01-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e9a01-105">Syntax</span></span>


```C++
void TimerCallback();
```



## <a name="parameters"></a><span data-ttu-id="e9a01-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e9a01-106">Parameters</span></span>

<span data-ttu-id="e9a01-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="e9a01-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e9a01-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e9a01-108">Return value</span></span>

<span data-ttu-id="e9a01-109">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="e9a01-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e9a01-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e9a01-110">Remarks</span></span>

<span data-ttu-id="e9a01-111">Метод [**кбасерендерер:: сендендофстреам**](cbaserenderer-sendendofstream.md) использует событие Timer для планирования \_ уведомлений о завершении EC.</span><span class="sxs-lookup"><span data-stu-id="e9a01-111">The [**CBaseRenderer::SendEndOfStream**](cbaserenderer-sendendofstream.md) method uses a timer event to schedule EC\_COMPLETE notifications.</span></span> <span data-ttu-id="e9a01-112">Метод **кбасерендерер:: TimerCallback** является функцией обратного вызова для события таймера.</span><span class="sxs-lookup"><span data-stu-id="e9a01-112">The **CBaseRenderer::TimerCallback** method is the callback function for the timer event.</span></span> <span data-ttu-id="e9a01-113">`TimerCallback`Метод вызывает **сендендофстреам** еще раз, и **сендендофстреам** определяет, следует ли отправить \_ уведомление о завершении EC или задать другой таймер.</span><span class="sxs-lookup"><span data-stu-id="e9a01-113">The `TimerCallback` method calls **SendEndOfStream** again, and **SendEndOfStream** determines whether to send the EC\_COMPLETE notification or set another timer.</span></span>

<span data-ttu-id="e9a01-114">Метод [**кбасерендерер:: ресетендофстреамтимер**](cbaserenderer-resetendofstreamtimer.md) отменяет событие таймера.</span><span class="sxs-lookup"><span data-stu-id="e9a01-114">The [**CBaseRenderer::ResetEndOfStreamTimer**](cbaserenderer-resetendofstreamtimer.md) method cancels the timer event.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9a01-115">Требования</span><span class="sxs-lookup"><span data-stu-id="e9a01-115">Requirements</span></span>



| <span data-ttu-id="e9a01-116">Требование</span><span class="sxs-lookup"><span data-stu-id="e9a01-116">Requirement</span></span> | <span data-ttu-id="e9a01-117">Значение</span><span class="sxs-lookup"><span data-stu-id="e9a01-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9a01-118">Header</span><span class="sxs-lookup"><span data-stu-id="e9a01-118">Header</span></span><br/>  | <dl> <span data-ttu-id="e9a01-119"><dt>Ренбасе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e9a01-119"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e9a01-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e9a01-120">Library</span></span><br/> | <dl> <span data-ttu-id="e9a01-121"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="e9a01-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9a01-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e9a01-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9a01-123">**Класс Кбасерендерер**</span><span class="sxs-lookup"><span data-stu-id="e9a01-123">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




