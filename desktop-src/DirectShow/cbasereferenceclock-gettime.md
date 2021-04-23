---
description: 'Метод Time извлекает текущее время ссылки. Этот метод реализует метод Иреференцеклокк:: Time.'
ms.assetid: 4e4e5954-b899-4741-8b7c-7bc98a3f0404
title: Метод Кбасереференцеклокк. Time (Рефклокк. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.GetTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a91f0015756d2ccfb545c4039d67434eb6d3c403
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669201"
---
# <a name="cbasereferenceclockgettime-method"></a><span data-ttu-id="83f60-104">Кбасереференцеклокк. метод времени</span><span class="sxs-lookup"><span data-stu-id="83f60-104">CBaseReferenceClock.GetTime method</span></span>

<span data-ttu-id="83f60-105">`GetTime`Метод получает текущее время ссылки.</span><span class="sxs-lookup"><span data-stu-id="83f60-105">The `GetTime` method retrieves the current reference time.</span></span> <span data-ttu-id="83f60-106">Этот метод реализует метод [**иреференцеклокк:: Time**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) .</span><span class="sxs-lookup"><span data-stu-id="83f60-106">This method implements the [**IReferenceClock::GetTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="83f60-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="83f60-107">Syntax</span></span>


```C++
HRESULT GetTime(
   REFERENCE_TIME *pTime
);
```



## <a name="parameters"></a><span data-ttu-id="83f60-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="83f60-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83f60-109">*птиме*</span><span class="sxs-lookup"><span data-stu-id="83f60-109">*pTime*</span></span> 
</dt> <dd>

<span data-ttu-id="83f60-110">Указатель на переменную, которая получает текущее время в единицах измерения 100-наносекундных.</span><span class="sxs-lookup"><span data-stu-id="83f60-110">Pointer to a variable that receives the current time, in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83f60-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="83f60-111">Return value</span></span>

<span data-ttu-id="83f60-112">Возвращает одно из значений **HRESULT** , приведенных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="83f60-112">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="83f60-113">Код возврата</span><span class="sxs-lookup"><span data-stu-id="83f60-113">Return code</span></span>                                                                               | <span data-ttu-id="83f60-114">Описание</span><span class="sxs-lookup"><span data-stu-id="83f60-114">Description</span></span>                                                 |
|-------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <span data-ttu-id="83f60-115"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="83f60-115"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="83f60-116">**Пустой** аргумент указателя.</span><span class="sxs-lookup"><span data-stu-id="83f60-116">**NULL** pointer argument.</span></span><br/>                       |
| <dl> <span data-ttu-id="83f60-117"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="83f60-117"><dt>**S\_FALSE**</dt></span></span> </dl>   | <span data-ttu-id="83f60-118">Возвращенное время совпадает с предыдущим значением.</span><span class="sxs-lookup"><span data-stu-id="83f60-118">Returned time is the same as the previous value.</span></span><br/> |
| <dl> <span data-ttu-id="83f60-119"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="83f60-119"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="83f60-120">Успешно.</span><span class="sxs-lookup"><span data-stu-id="83f60-120">Success.</span></span><br/>                                         |



 

## <a name="remarks"></a><span data-ttu-id="83f60-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="83f60-121">Remarks</span></span>

<span data-ttu-id="83f60-122">Этот метод вызывает метод [**кбасереференцеклокк:: жетприватетиме**](cbasereferenceclock-getprivatetime.md) для определения реального времени.</span><span class="sxs-lookup"><span data-stu-id="83f60-122">This method calls the [**CBaseReferenceClock::GetPrivateTime**](cbasereferenceclock-getprivatetime.md) method to determine the real clock time.</span></span> <span data-ttu-id="83f60-123">Если время, которое строго превышает предыдущее значение, `GetTime` использует время и возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="83f60-123">If the clock time is strictly greater than the previous value, `GetTime` uses the clock time and returns S\_OK.</span></span> <span data-ttu-id="83f60-124">В противном случае `GetTime` использует предыдущее значение и возвращает \_ значение S false.</span><span class="sxs-lookup"><span data-stu-id="83f60-124">Otherwise, `GetTime` uses the previous value and returns S\_FALSE.</span></span> <span data-ttu-id="83f60-125">Таким образом, внутренние часы могут выполняться в течение короткого периода времени, не вызывая обратную ссылку на время выполнения.</span><span class="sxs-lookup"><span data-stu-id="83f60-125">Therefore, the internal clock can run backward for a short period, without causing the reference time to run backward.</span></span> <span data-ttu-id="83f60-126">Вместо этого время ссылки будет занимать одно и то же значение до тех пор, пока не будут перехватываться внутренние часы.</span><span class="sxs-lookup"><span data-stu-id="83f60-126">Instead, the reference time will "stall" at the same value until the internal clock catches up.</span></span>

## <a name="requirements"></a><span data-ttu-id="83f60-127">Требования</span><span class="sxs-lookup"><span data-stu-id="83f60-127">Requirements</span></span>



| <span data-ttu-id="83f60-128">Требование</span><span class="sxs-lookup"><span data-stu-id="83f60-128">Requirement</span></span> | <span data-ttu-id="83f60-129">Значение</span><span class="sxs-lookup"><span data-stu-id="83f60-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="83f60-130">Header</span><span class="sxs-lookup"><span data-stu-id="83f60-130">Header</span></span><br/>  | <dl> <span data-ttu-id="83f60-131"><dt>Рефклокк. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="83f60-131"><dt>Refclock.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="83f60-132">Библиотека</span><span class="sxs-lookup"><span data-stu-id="83f60-132">Library</span></span><br/> | <dl> <span data-ttu-id="83f60-133"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="83f60-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="83f60-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="83f60-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83f60-135">**Класс Кбасереференцеклокк**</span><span class="sxs-lookup"><span data-stu-id="83f60-135">**CBaseReferenceClock Class**</span></span>](cbasereferenceclock.md)
</dt> </dl>

 

 




