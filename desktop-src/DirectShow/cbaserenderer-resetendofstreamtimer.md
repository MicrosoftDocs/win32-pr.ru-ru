---
description: Метод Ресетендофстреамтимер отменяет таймер, планирующий \_ выполнение уведомлений EC.
ms.assetid: 9d423241-1401-4181-8fbf-c409a1e8abdd
title: Кбасерендерер. Ресетендофстреамтимер, метод (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.ResetEndOfStreamTimer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 734673c4e2bd6719179eca00f03a6c2f41061132
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105658045"
---
# <a name="cbaserendererresetendofstreamtimer-method"></a><span data-ttu-id="f8add-103">Кбасерендерер. Ресетендофстреамтимер, метод</span><span class="sxs-lookup"><span data-stu-id="f8add-103">CBaseRenderer.ResetEndOfStreamTimer method</span></span>

<span data-ttu-id="f8add-104">`ResetEndOfStreamTimer`Метод отменяет таймер, планирующий [**\_ выполнение уведомлений EC**](ec-complete.md) .</span><span class="sxs-lookup"><span data-stu-id="f8add-104">The `ResetEndOfStreamTimer` method cancels the timer that schedules [**EC\_COMPLETE**](ec-complete.md) notifications.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8add-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f8add-105">Syntax</span></span>


```C++
void ResetEndOfStreamTimer();
```



## <a name="parameters"></a><span data-ttu-id="f8add-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f8add-106">Parameters</span></span>

<span data-ttu-id="f8add-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="f8add-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f8add-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f8add-108">Return value</span></span>

<span data-ttu-id="f8add-109">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="f8add-109">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8add-110">Требования</span><span class="sxs-lookup"><span data-stu-id="f8add-110">Requirements</span></span>



| <span data-ttu-id="f8add-111">Требование</span><span class="sxs-lookup"><span data-stu-id="f8add-111">Requirement</span></span> | <span data-ttu-id="f8add-112">Значение</span><span class="sxs-lookup"><span data-stu-id="f8add-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8add-113">Header</span><span class="sxs-lookup"><span data-stu-id="f8add-113">Header</span></span><br/>  | <dl> <span data-ttu-id="f8add-114"><dt>Ренбасе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f8add-114"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f8add-115">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f8add-115">Library</span></span><br/> | <dl> <span data-ttu-id="f8add-116"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="f8add-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f8add-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f8add-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8add-118">**Класс Кбасерендерер**</span><span class="sxs-lookup"><span data-stu-id="f8add-118">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> <dt>

[<span data-ttu-id="f8add-119">**Кбасерендерер:: Сендендофстреам**</span><span class="sxs-lookup"><span data-stu-id="f8add-119">**CBaseRenderer::SendEndOfStream**</span></span>](cbaserenderer-sendendofstream.md)
</dt> <dt>

[<span data-ttu-id="f8add-120">**Кбасерендерер:: TimerCallback**</span><span class="sxs-lookup"><span data-stu-id="f8add-120">**CBaseRenderer::TimerCallback**</span></span>](cbaserenderer-timercallback.md)
</dt> </dl>

 

 




