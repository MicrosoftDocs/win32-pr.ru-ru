---
description: 'Метод Адвисепериодик создает периодические запросы рекомендаций. Этот метод реализует метод Иреференцеклокк:: Адвисепериодик.'
ms.assetid: ddaf0861-df11-4008-8e9c-a0c53929cd3f
title: Кбасереференцеклокк. Адвисепериодик, метод (Рефклокк. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.AdvisePeriodic
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a582e05756e8d034e5b2d0a1cd8f7eb569dbb842
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668924"
---
# <a name="cbasereferenceclockadviseperiodic-method"></a><span data-ttu-id="7cbbd-104">Кбасереференцеклокк. Адвисепериодик, метод</span><span class="sxs-lookup"><span data-stu-id="7cbbd-104">CBaseReferenceClock.AdvisePeriodic method</span></span>

<span data-ttu-id="7cbbd-105">`AdvisePeriodic`Метод создает периодические запросы рекомендаций.</span><span class="sxs-lookup"><span data-stu-id="7cbbd-105">The `AdvisePeriodic` method creates a periodic advise request.</span></span> <span data-ttu-id="7cbbd-106">Этот метод реализует метод [**иреференцеклокк:: адвисепериодик**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-adviseperiodic) .</span><span class="sxs-lookup"><span data-stu-id="7cbbd-106">This method implements the [**IReferenceClock::AdvisePeriodic**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-adviseperiodic) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="7cbbd-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7cbbd-107">Syntax</span></span>


```C++
HRESULT AdvisePeriodic(
   REFERENCE_TIME StartTime,
   REFERENCE_TIME PeriodTime,
   HSEMAPHORE     hSemaphore,
   DWORD_PTR      *pdwAdviseToken
);
```



## <a name="parameters"></a><span data-ttu-id="7cbbd-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="7cbbd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7cbbd-109">*StartTime*</span><span class="sxs-lookup"><span data-stu-id="7cbbd-109">*StartTime*</span></span> 
</dt> <dd>

<span data-ttu-id="7cbbd-110">Время первого уведомления в единицах с 100 нс.</span><span class="sxs-lookup"><span data-stu-id="7cbbd-110">Time of the first notification, in 100-nanosecond units.</span></span> <span data-ttu-id="7cbbd-111">Должно быть больше нуля и меньше максимального \_ времени.</span><span class="sxs-lookup"><span data-stu-id="7cbbd-111">Must be greater than zero and less than MAX\_TIME.</span></span>

</dd> <dt>

<span data-ttu-id="7cbbd-112">*периодтиме*</span><span class="sxs-lookup"><span data-stu-id="7cbbd-112">*PeriodTime*</span></span> 
</dt> <dd>

<span data-ttu-id="7cbbd-113">Время между уведомлениями (в 100-наносекундных единицах).</span><span class="sxs-lookup"><span data-stu-id="7cbbd-113">Time between notifications, in 100-nanosecond units.</span></span> <span data-ttu-id="7cbbd-114">Должен быть больше нуля.</span><span class="sxs-lookup"><span data-stu-id="7cbbd-114">Must be greater than zero.</span></span>

</dd> <dt>

<span data-ttu-id="7cbbd-115">*хсемафоре*</span><span class="sxs-lookup"><span data-stu-id="7cbbd-115">*hSemaphore*</span></span> 
</dt> <dd>

<span data-ttu-id="7cbbd-116">Обработчик для семафора, созданного вызывающим объектом.</span><span class="sxs-lookup"><span data-stu-id="7cbbd-116">Handle to a semaphore, created by the caller.</span></span>

</dd> <dt>

<span data-ttu-id="7cbbd-117">*пдвадвисетокен*</span><span class="sxs-lookup"><span data-stu-id="7cbbd-117">*pdwAdviseToken*</span></span> 
</dt> <dd>

<span data-ttu-id="7cbbd-118">Указатель на переменную, которая получает идентификатор для запроса Advise.</span><span class="sxs-lookup"><span data-stu-id="7cbbd-118">Pointer to a variable that receives an identifier for the advise request.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7cbbd-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7cbbd-119">Return value</span></span>

<span data-ttu-id="7cbbd-120">Возвращает одно из значений **HRESULT** , приведенных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="7cbbd-120">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="7cbbd-121">Код возврата</span><span class="sxs-lookup"><span data-stu-id="7cbbd-121">Return code</span></span>                                                                                   | <span data-ttu-id="7cbbd-122">Описание</span><span class="sxs-lookup"><span data-stu-id="7cbbd-122">Description</span></span>                          |
|-----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <span data-ttu-id="7cbbd-123"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="7cbbd-123"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="7cbbd-124">Успешно</span><span class="sxs-lookup"><span data-stu-id="7cbbd-124">Success</span></span><br/>                   |
| <dl> <span data-ttu-id="7cbbd-125"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="7cbbd-125"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="7cbbd-126">Недопустимые значения времени</span><span class="sxs-lookup"><span data-stu-id="7cbbd-126">Invalid time values</span></span><br/>       |
| <dl> <span data-ttu-id="7cbbd-127"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="7cbbd-127"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="7cbbd-128">Failure</span><span class="sxs-lookup"><span data-stu-id="7cbbd-128">Failure</span></span><br/>                   |
| <dl> <span data-ttu-id="7cbbd-129"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="7cbbd-129"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="7cbbd-130">**Пустой** аргумент указателя</span><span class="sxs-lookup"><span data-stu-id="7cbbd-130">**NULL** pointer argument</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="7cbbd-131">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7cbbd-131">Remarks</span></span>

<span data-ttu-id="7cbbd-132">Во время каждого уведомления часы освобождают семафор, указанный в параметре *хсемафоре* .</span><span class="sxs-lookup"><span data-stu-id="7cbbd-132">At each notification time, the clock releases the semaphore specified in the *hSemaphore* parameter.</span></span> <span data-ttu-id="7cbbd-133">Если дальнейшие уведомления не требуются, вызовите метод [**кбасереференцеклокк:: unadvise**](cbasereferenceclock-unadvise.md) и передайте значение *пдвадвисетокен* , возвращенное этим вызовом.</span><span class="sxs-lookup"><span data-stu-id="7cbbd-133">When no further notifications are required, call the [**CBaseReferenceClock::Unadvise**](cbasereferenceclock-unadvise.md) method and pass the *pdwAdviseToken* value returned from this call.</span></span>

## <a name="requirements"></a><span data-ttu-id="7cbbd-134">Требования</span><span class="sxs-lookup"><span data-stu-id="7cbbd-134">Requirements</span></span>



| <span data-ttu-id="7cbbd-135">Требование</span><span class="sxs-lookup"><span data-stu-id="7cbbd-135">Requirement</span></span> | <span data-ttu-id="7cbbd-136">Значение</span><span class="sxs-lookup"><span data-stu-id="7cbbd-136">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7cbbd-137">Header</span><span class="sxs-lookup"><span data-stu-id="7cbbd-137">Header</span></span><br/>  | <dl> <span data-ttu-id="7cbbd-138"><dt>Рефклокк. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7cbbd-138"><dt>Refclock.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="7cbbd-139">Библиотека</span><span class="sxs-lookup"><span data-stu-id="7cbbd-139">Library</span></span><br/> | <dl> <span data-ttu-id="7cbbd-140"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="7cbbd-140"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7cbbd-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7cbbd-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7cbbd-142">**Класс Кбасереференцеклокк**</span><span class="sxs-lookup"><span data-stu-id="7cbbd-142">**CBaseReferenceClock Class**</span></span>](cbasereferenceclock.md)
</dt> </dl>

 

 




