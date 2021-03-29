---
description: Метод Жетнекстадвисетиме извлекает время следующего запроса Advise.
ms.assetid: 2a376250-fb39-46d7-a5a8-e3a3143cd209
title: Камсчедуле. Жетнекстадвисетиме, метод (Дссчедуле. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMSchedule.GetNextAdviseTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5894ae98666c9134abd4bce96922a5f28d5919b5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668782"
---
# <a name="camschedulegetnextadvisetime-method"></a><span data-ttu-id="1036a-103">Камсчедуле. Жетнекстадвисетиме, метод</span><span class="sxs-lookup"><span data-stu-id="1036a-103">CAMSchedule.GetNextAdviseTime method</span></span>

<span data-ttu-id="1036a-104">`GetNextAdviseTime`Метод извлекает время следующего запроса на выadvise.</span><span class="sxs-lookup"><span data-stu-id="1036a-104">The `GetNextAdviseTime` method retrieves the time of the next advise request.</span></span>

## <a name="syntax"></a><span data-ttu-id="1036a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1036a-105">Syntax</span></span>


```C++
REFERENCE_TIME GetNextAdviseTime();
```



## <a name="parameters"></a><span data-ttu-id="1036a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1036a-106">Parameters</span></span>

<span data-ttu-id="1036a-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="1036a-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1036a-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1036a-108">Return value</span></span>

<span data-ttu-id="1036a-109">Возвращает время ссылки следующего запроса на выходе или максимальное время, в \_ течение которого запросы не планируются.</span><span class="sxs-lookup"><span data-stu-id="1036a-109">Returns the reference time of the next advise request, or MAX\_TIME no requests are scheduled.</span></span>

## <a name="requirements"></a><span data-ttu-id="1036a-110">Требования</span><span class="sxs-lookup"><span data-stu-id="1036a-110">Requirements</span></span>



| <span data-ttu-id="1036a-111">Требование</span><span class="sxs-lookup"><span data-stu-id="1036a-111">Requirement</span></span> | <span data-ttu-id="1036a-112">Значение</span><span class="sxs-lookup"><span data-stu-id="1036a-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1036a-113">Header</span><span class="sxs-lookup"><span data-stu-id="1036a-113">Header</span></span><br/>  | <dl> <span data-ttu-id="1036a-114"><dt>Дссчедуле. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1036a-114"><dt>Dsschedule.h (include Streams.h)</dt></span></span> </dl>                                                                                |
| <span data-ttu-id="1036a-115">Библиотека</span><span class="sxs-lookup"><span data-stu-id="1036a-115">Library</span></span><br/> | <dl> <span data-ttu-id="1036a-116"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="1036a-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1036a-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1036a-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1036a-118">**Класс Камсчедуле**</span><span class="sxs-lookup"><span data-stu-id="1036a-118">**CAMSchedule Class**</span></span>](camschedule.md)
</dt> </dl>

 

 




