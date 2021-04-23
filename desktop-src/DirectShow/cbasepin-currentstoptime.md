---
description: 'Метод Куррентстоптиме извлекает время окончания сегмента, заданное методом Кбасепин:: Невсегмент.'
ms.assetid: 2066c4a5-2d39-4a2e-b2d6-48c615862aec
title: Кбасепин. Куррентстоптиме, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.CurrentStopTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 74fb25184bbcd0778268f74a4c40ccfb0722287f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657330"
---
# <a name="cbasepincurrentstoptime-method"></a><span data-ttu-id="4e380-103">Кбасепин. Куррентстоптиме, метод</span><span class="sxs-lookup"><span data-stu-id="4e380-103">CBasePin.CurrentStopTime method</span></span>

<span data-ttu-id="4e380-104">`CurrentStopTime`Метод получает время окончания сегмента, заданное методом [**кбасепин:: невсегмент**](cbasepin-newsegment.md) .</span><span class="sxs-lookup"><span data-stu-id="4e380-104">The `CurrentStopTime` method retrieves the segment stop time, set by the [**CBasePin::NewSegment**](cbasepin-newsegment.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e380-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4e380-105">Syntax</span></span>


```C++
REFERENCE_TIME CurrentStopTime();
```



## <a name="parameters"></a><span data-ttu-id="4e380-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4e380-106">Parameters</span></span>

<span data-ttu-id="4e380-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="4e380-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4e380-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4e380-108">Return value</span></span>

<span data-ttu-id="4e380-109">Возвращает значение [**кбасепин:: m \_ тстоп**](cbasepin-m-tstop.md).</span><span class="sxs-lookup"><span data-stu-id="4e380-109">Returns the value of [**CBasePin::m\_tStop**](cbasepin-m-tstop.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4e380-110">Требования</span><span class="sxs-lookup"><span data-stu-id="4e380-110">Requirements</span></span>



| <span data-ttu-id="4e380-111">Требование</span><span class="sxs-lookup"><span data-stu-id="4e380-111">Requirement</span></span> | <span data-ttu-id="4e380-112">Значение</span><span class="sxs-lookup"><span data-stu-id="4e380-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e380-113">Header</span><span class="sxs-lookup"><span data-stu-id="4e380-113">Header</span></span><br/>  | <dl> <span data-ttu-id="4e380-114"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4e380-114"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="4e380-115">Библиотека</span><span class="sxs-lookup"><span data-stu-id="4e380-115">Library</span></span><br/> | <dl> <span data-ttu-id="4e380-116"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="4e380-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e380-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4e380-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e380-118">**Класс Кбасепин**</span><span class="sxs-lookup"><span data-stu-id="4e380-118">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




