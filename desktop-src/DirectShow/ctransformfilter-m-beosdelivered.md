---
description: Флаг, указывающий, отправил ли фильтр уведомление об окончании потока.
ms.assetid: 93f897de-04bb-4de4-a612-39b27c7d6f6c
title: 'Элемент Ктрансформфилтер:: m_bEOSDelivered (Трансфрм. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bEOSDelivered
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f24b87f9808c53b5f64f66031a8ee2a4e9449089
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657754"
---
# <a name="ctransformfilterm_beosdelivered-member"></a><span data-ttu-id="2258f-103">Элемент Ктрансформфилтер:: m \_ беосделиверед</span><span class="sxs-lookup"><span data-stu-id="2258f-103">CTransformFilter::m\_bEOSDelivered member</span></span>

<span data-ttu-id="2258f-104">Флаг, указывающий, отправил ли фильтр уведомление об окончании потока.</span><span class="sxs-lookup"><span data-stu-id="2258f-104">Flag that indicates whether the filter has sent an end-of-stream notification.</span></span>

## <a name="syntax"></a><span data-ttu-id="2258f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2258f-105">Syntax</span></span>


```C++
BOOL m_bEOSDelivered;
```



## <a name="remarks"></a><span data-ttu-id="2258f-106">Примечания</span><span class="sxs-lookup"><span data-stu-id="2258f-106">Remarks</span></span>

<span data-ttu-id="2258f-107">Если фильтр приостанавливается, когда у него нет входного соединения, то он отправляет уведомление о завершении потока и устанавливает для этого флага **значение true**.</span><span class="sxs-lookup"><span data-stu-id="2258f-107">If the filter pauses when it does not have an input connection, it sends an end-of-stream notification downstream and sets this flag to **TRUE**.</span></span> <span data-ttu-id="2258f-108">Уведомление о завершении потока гарантирует, что нисходящий фильтр не ждет выборки.</span><span class="sxs-lookup"><span data-stu-id="2258f-108">The end-of-stream notification ensures that the downstream filter does not wait for samples.</span></span> <span data-ttu-id="2258f-109">Обратите внимание, что метод [**EndOfStream**](ctransformfilter-endofstream.md) фильтра не устанавливает этот флаг.</span><span class="sxs-lookup"><span data-stu-id="2258f-109">Note that the filter's [**EndOfStream**](ctransformfilter-endofstream.md) method does not set this flag.</span></span>

## <a name="requirements"></a><span data-ttu-id="2258f-110">Требования</span><span class="sxs-lookup"><span data-stu-id="2258f-110">Requirements</span></span>



| <span data-ttu-id="2258f-111">Требование</span><span class="sxs-lookup"><span data-stu-id="2258f-111">Requirement</span></span> | <span data-ttu-id="2258f-112">Значение</span><span class="sxs-lookup"><span data-stu-id="2258f-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2258f-113">Header</span><span class="sxs-lookup"><span data-stu-id="2258f-113">Header</span></span><br/>  | <dl> <span data-ttu-id="2258f-114"><dt>Трансфрм. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2258f-114"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="2258f-115">Библиотека</span><span class="sxs-lookup"><span data-stu-id="2258f-115">Library</span></span><br/> | <dl> <span data-ttu-id="2258f-116"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="2258f-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2258f-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2258f-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2258f-118">**Класс Ктрансформфилтер**</span><span class="sxs-lookup"><span data-stu-id="2258f-118">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




