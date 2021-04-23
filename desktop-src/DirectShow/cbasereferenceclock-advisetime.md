---
description: 'Метод Адвисетиме создает запрос на одноразовый Совет. Этот метод реализует метод Иреференцеклокк:: Адвисетиме.'
ms.assetid: 4849a04d-35f2-4a24-bf5d-f20e541f5e99
title: Кбасереференцеклокк. Адвисетиме, метод (Рефклокк. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.AdviseTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 326fc5e0939803ab66e0466fbf32351387977019
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657663"
---
# <a name="cbasereferenceclockadvisetime-method"></a><span data-ttu-id="e4b43-104">Кбасереференцеклокк. Адвисетиме, метод</span><span class="sxs-lookup"><span data-stu-id="e4b43-104">CBaseReferenceClock.AdviseTime method</span></span>

<span data-ttu-id="e4b43-105">`AdviseTime`Метод создает одноразовый запрос Advise.</span><span class="sxs-lookup"><span data-stu-id="e4b43-105">The `AdviseTime` method creates a one-shot advise request.</span></span> <span data-ttu-id="e4b43-106">Этот метод реализует метод [**иреференцеклокк:: адвисетиме**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-advisetime) .</span><span class="sxs-lookup"><span data-stu-id="e4b43-106">This method implements the [**IReferenceClock::AdviseTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-advisetime) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4b43-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e4b43-107">Syntax</span></span>


```C++
HRESULT AdviseTime(
   REFERENCE_TIME baseTime,
   REFERENCE_TIME streamTime,
   HEVENT         hEvent,
   DWORD_PTR      *pdwAdviseToken
);
```



## <a name="parameters"></a><span data-ttu-id="e4b43-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="e4b43-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4b43-109">*басетиме*</span><span class="sxs-lookup"><span data-stu-id="e4b43-109">*baseTime*</span></span> 
</dt> <dd>

<span data-ttu-id="e4b43-110">Базовое время ссылки в единицах измерения 100-наносекундных.</span><span class="sxs-lookup"><span data-stu-id="e4b43-110">Base reference time, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="e4b43-111">*стреамтиме*</span><span class="sxs-lookup"><span data-stu-id="e4b43-111">*streamTime*</span></span> 
</dt> <dd>

<span data-ttu-id="e4b43-112">Время смещения потока (в 100-наносекундных единицах).</span><span class="sxs-lookup"><span data-stu-id="e4b43-112">Stream offset time, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="e4b43-113">*хевент*</span><span class="sxs-lookup"><span data-stu-id="e4b43-113">*hEvent*</span></span> 
</dt> <dd>

<span data-ttu-id="e4b43-114">Обработчик события, созданный вызывающим объектом.</span><span class="sxs-lookup"><span data-stu-id="e4b43-114">Handle to an event, created by the caller.</span></span>

</dd> <dt>

<span data-ttu-id="e4b43-115">*пдвадвисетокен*</span><span class="sxs-lookup"><span data-stu-id="e4b43-115">*pdwAdviseToken*</span></span> 
</dt> <dd>

<span data-ttu-id="e4b43-116">Указатель на переменную, которая получает идентификатор для запроса Advise.</span><span class="sxs-lookup"><span data-stu-id="e4b43-116">Pointer to a variable that receives an identifier for the advise request.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4b43-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e4b43-117">Return value</span></span>

<span data-ttu-id="e4b43-118">Возвращает одно из значений **HRESULT** , приведенных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="e4b43-118">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="e4b43-119">Код возврата</span><span class="sxs-lookup"><span data-stu-id="e4b43-119">Return code</span></span>                                                                                   | <span data-ttu-id="e4b43-120">Описание</span><span class="sxs-lookup"><span data-stu-id="e4b43-120">Description</span></span>                          |
|-----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <span data-ttu-id="e4b43-121"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="e4b43-121"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="e4b43-122">Успешно</span><span class="sxs-lookup"><span data-stu-id="e4b43-122">Success</span></span><br/>                   |
| <dl> <span data-ttu-id="e4b43-123"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="e4b43-123"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="e4b43-124">Недопустимые значения времени</span><span class="sxs-lookup"><span data-stu-id="e4b43-124">Invalid time values</span></span><br/>       |
| <dl> <span data-ttu-id="e4b43-125"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="e4b43-125"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="e4b43-126">Failure</span><span class="sxs-lookup"><span data-stu-id="e4b43-126">Failure</span></span><br/>                   |
| <dl> <span data-ttu-id="e4b43-127"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="e4b43-127"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="e4b43-128">**Пустой** аргумент указателя</span><span class="sxs-lookup"><span data-stu-id="e4b43-128">**NULL** pointer argument</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e4b43-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e4b43-129">Remarks</span></span>

<span data-ttu-id="e4b43-130">Этот метод создает Однофакторный запрос advise для ссылочного времени *басетиме*  +  *стреамтиме*.</span><span class="sxs-lookup"><span data-stu-id="e4b43-130">This method creates a one-shot advise request for the reference time *baseTime* + *streamTime*.</span></span> <span data-ttu-id="e4b43-131">Сумма должна быть больше нуля и меньше, чем максимальная \_ Длительность, или метод возвращает E \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="e4b43-131">The sum must be greater than zero and less than MAX\_TIME, or the method returns E\_INVALIDARG.</span></span> <span data-ttu-id="e4b43-132">В запрошенное время часы сигнализирует о событии, указанном в параметре *Хевент* .</span><span class="sxs-lookup"><span data-stu-id="e4b43-132">At the requested time, the clock signals the event specified in the *hEvent* parameter.</span></span>

<span data-ttu-id="e4b43-133">Чтобы отменить уведомление до достижения времени, вызовите метод [**кбасереференцеклокк:: unadvise**](cbasereferenceclock-unadvise.md) и передайте значение *пдвадвисетокен* , возвращенное этим вызовом.</span><span class="sxs-lookup"><span data-stu-id="e4b43-133">To cancel the notification before the time is reached, call the [**CBaseReferenceClock::Unadvise**](cbasereferenceclock-unadvise.md) method and pass the *pdwAdviseToken* value returned from this call.</span></span> <span data-ttu-id="e4b43-134">После получения уведомления часы автоматически очищаются, поэтому нет необходимости вызывать **unadvise**.</span><span class="sxs-lookup"><span data-stu-id="e4b43-134">After the notification has occurred, the clock automatically clears it, so it is not necessary to call **Unadvise**.</span></span> <span data-ttu-id="e4b43-135">Однако это не является ошибкой.</span><span class="sxs-lookup"><span data-stu-id="e4b43-135">However, it is not an error to do so.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4b43-136">Требования</span><span class="sxs-lookup"><span data-stu-id="e4b43-136">Requirements</span></span>



| <span data-ttu-id="e4b43-137">Требование</span><span class="sxs-lookup"><span data-stu-id="e4b43-137">Requirement</span></span> | <span data-ttu-id="e4b43-138">Значение</span><span class="sxs-lookup"><span data-stu-id="e4b43-138">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4b43-139">Header</span><span class="sxs-lookup"><span data-stu-id="e4b43-139">Header</span></span><br/>  | <dl> <span data-ttu-id="e4b43-140"><dt>Рефклокк. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e4b43-140"><dt>Refclock.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="e4b43-141">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e4b43-141">Library</span></span><br/> | <dl> <span data-ttu-id="e4b43-142"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="e4b43-142"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e4b43-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e4b43-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4b43-144">**Класс Кбасереференцеклокк**</span><span class="sxs-lookup"><span data-stu-id="e4b43-144">**CBaseReferenceClock Class**</span></span>](cbasereferenceclock.md)
</dt> </dl>

 

 




