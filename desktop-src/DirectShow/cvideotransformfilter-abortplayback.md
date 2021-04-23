---
description: Метод Абортплайбакк используется для сигнализации об ошибке потоковой передачи. Он отправляет событие EC \_ еррораборт в Диспетчер графа фильтров и отправляет уведомление о завершении потока.
ms.assetid: b48ec72f-d220-4b27-98fc-88eaa4f663eb
title: Квидеотрансформфилтер. Абортплайбакк, метод (Втранс. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CVideoTransformFilter.AbortPlayback
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 952987dec315408920e92d79003480a01640d14e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105674835"
---
# <a name="cvideotransformfilterabortplayback-method"></a><span data-ttu-id="255a8-104">Квидеотрансформфилтер. Абортплайбакк, метод</span><span class="sxs-lookup"><span data-stu-id="255a8-104">CVideoTransformFilter.AbortPlayback method</span></span>

<span data-ttu-id="255a8-105">`AbortPlayback`Метод используется для сигнализации об ошибке потоковой передачи.</span><span class="sxs-lookup"><span data-stu-id="255a8-105">The `AbortPlayback` method is used to signal a streaming error.</span></span> <span data-ttu-id="255a8-106">Он отправляет событие [**EC \_ Еррораборт**](ec-errorabort.md) в Диспетчер графа фильтров и отправляет уведомление о завершении потока.</span><span class="sxs-lookup"><span data-stu-id="255a8-106">It sends an [**EC\_ERRORABORT**](ec-errorabort.md) event to the Filter Graph Manager, and sends an end-of-stream notification downstream.</span></span>

## <a name="syntax"></a><span data-ttu-id="255a8-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="255a8-107">Syntax</span></span>


```C++
HRESULT AbortPlayback(
   HRESULT hr
);
```



## <a name="parameters"></a><span data-ttu-id="255a8-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="255a8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="255a8-109">*ч*</span><span class="sxs-lookup"><span data-stu-id="255a8-109">*hr*</span></span> 
</dt> <dd>

<span data-ttu-id="255a8-110">Значение **HRESULT** операции, которая завершилась ошибкой.</span><span class="sxs-lookup"><span data-stu-id="255a8-110">**HRESULT** value of the operation that failed.</span></span> <span data-ttu-id="255a8-111">Это значение используется в качестве первого параметра события для \_ события EC еррораборт.</span><span class="sxs-lookup"><span data-stu-id="255a8-111">This value is used as the first event parameter for the EC\_ERRORABORT event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="255a8-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="255a8-112">Return value</span></span>

<span data-ttu-id="255a8-113">Возвращает значение параметра *HR* .</span><span class="sxs-lookup"><span data-stu-id="255a8-113">Returns the value of the *hr* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="255a8-114">Требования</span><span class="sxs-lookup"><span data-stu-id="255a8-114">Requirements</span></span>



| <span data-ttu-id="255a8-115">Требование</span><span class="sxs-lookup"><span data-stu-id="255a8-115">Requirement</span></span> | <span data-ttu-id="255a8-116">Значение</span><span class="sxs-lookup"><span data-stu-id="255a8-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="255a8-117">Header</span><span class="sxs-lookup"><span data-stu-id="255a8-117">Header</span></span><br/>  | <dl> <span data-ttu-id="255a8-118"><dt>Втранс. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="255a8-118"><dt>Vtrans.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="255a8-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="255a8-119">Library</span></span><br/> | <dl> <span data-ttu-id="255a8-120"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="255a8-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="255a8-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="255a8-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="255a8-122">**Класс Квидеотрансформфилтер**</span><span class="sxs-lookup"><span data-stu-id="255a8-122">**CVideoTransformFilter Class**</span></span>](cvideotransformfilter.md)
</dt> </dl>

 

 




