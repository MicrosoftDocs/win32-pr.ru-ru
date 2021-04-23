---
description: Метод Сеттимеделта корректирует время внутренних часов.
ms.assetid: 51534c92-5573-4e2a-baeb-b1a82ccf88de
title: Кбасереференцеклокк. Сеттимеделта, метод (Рефклокк. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.SetTimeDelta
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: de58363119dc08c21d2cab0070b438ad6b4331e0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669196"
---
# <a name="cbasereferenceclocksettimedelta-method"></a><span data-ttu-id="4b70b-103">Кбасереференцеклокк. Сеттимеделта, метод</span><span class="sxs-lookup"><span data-stu-id="4b70b-103">CBaseReferenceClock.SetTimeDelta method</span></span>

<span data-ttu-id="4b70b-104">`SetTimeDelta`Метод корректирует время внутренних часов.</span><span class="sxs-lookup"><span data-stu-id="4b70b-104">The `SetTimeDelta` method adjusts the internal clock time.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b70b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4b70b-105">Syntax</span></span>


```C++
HRESULT SetTimeDelta(
  [ref] const REFERENCE_TIME &TimeDelta
);
```



## <a name="parameters"></a><span data-ttu-id="4b70b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4b70b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4b70b-107">*Тимеделта* \[ ЗНАЧ\]</span><span class="sxs-lookup"><span data-stu-id="4b70b-107">*TimeDelta* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="4b70b-108">Сумма для корректировки времени в 100-наносекундных единицах.</span><span class="sxs-lookup"><span data-stu-id="4b70b-108">Amount to adjust the clock time, in 100-nanosecond units.</span></span> <span data-ttu-id="4b70b-109">Положительное значение перемещает часы вперед, а отрицательное значение перемещает часы назад.</span><span class="sxs-lookup"><span data-stu-id="4b70b-109">A positive value moves the clock forward, and a negative value moves the clock backward.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4b70b-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4b70b-110">Return value</span></span>

<span data-ttu-id="4b70b-111">Возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="4b70b-111">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="4b70b-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4b70b-112">Remarks</span></span>

<span data-ttu-id="4b70b-113">Производный класс может использовать этот метод для корректировки внутренних часов, если он отклоняется от устройства, предоставляющего сведения о времени.</span><span class="sxs-lookup"><span data-stu-id="4b70b-113">The derived class can use this method to adjust the internal clock, if it drifts from the device that is providing timing information.</span></span>

<span data-ttu-id="4b70b-114">Метод [**кбасереференцеклокк:: OnTime**](cbasereferenceclock-gettime.md) никогда не возвращает значения по убыванию.</span><span class="sxs-lookup"><span data-stu-id="4b70b-114">The [**CBaseReferenceClock::GetTime**](cbasereferenceclock-gettime.md) method never returns decreasing values.</span></span> <span data-ttu-id="4b70b-115">Если настроить часы назад, функция @ **time** возвращает предыдущее значение до тех пор, пока часы не достигнет этого значения.</span><span class="sxs-lookup"><span data-stu-id="4b70b-115">If you adjust the clock backward, **GetTime** returns the previous value until the clock reaches that value again.</span></span>

## <a name="requirements"></a><span data-ttu-id="4b70b-116">Требования</span><span class="sxs-lookup"><span data-stu-id="4b70b-116">Requirements</span></span>



| <span data-ttu-id="4b70b-117">Требование</span><span class="sxs-lookup"><span data-stu-id="4b70b-117">Requirement</span></span> | <span data-ttu-id="4b70b-118">Значение</span><span class="sxs-lookup"><span data-stu-id="4b70b-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b70b-119">Header</span><span class="sxs-lookup"><span data-stu-id="4b70b-119">Header</span></span><br/>  | <dl> <span data-ttu-id="4b70b-120"><dt>Рефклокк. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4b70b-120"><dt>Refclock.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="4b70b-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="4b70b-121">Library</span></span><br/> | <dl> <span data-ttu-id="4b70b-122"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="4b70b-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4b70b-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4b70b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b70b-124">**Класс Кбасереференцеклокк**</span><span class="sxs-lookup"><span data-stu-id="4b70b-124">**CBaseReferenceClock Class**</span></span>](cbasereferenceclock.md)
</dt> </dl>

 

 




