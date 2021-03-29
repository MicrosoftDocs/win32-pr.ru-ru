---
description: Метод Аддадвисепаккет добавляет запрос advise в список ожидающих запросов.
ms.assetid: 138d8404-7d28-47cc-91b4-4733a113ac7a
title: Камсчедуле. Аддадвисепаккет, метод (Дссчедуле. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMSchedule.AddAdvisePacket
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5dd9586b09586c12f1a30f45b512336831372295
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668787"
---
# <a name="camscheduleaddadvisepacket-method"></a><span data-ttu-id="73e65-103">Камсчедуле. Аддадвисепаккет, метод</span><span class="sxs-lookup"><span data-stu-id="73e65-103">CAMSchedule.AddAdvisePacket method</span></span>

<span data-ttu-id="73e65-104">`AddAdvisePacket`Метод добавляет запрос advise в список ожидающих запросов.</span><span class="sxs-lookup"><span data-stu-id="73e65-104">The `AddAdvisePacket` method adds an advise request to the list of pending requests.</span></span>

## <a name="syntax"></a><span data-ttu-id="73e65-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="73e65-105">Syntax</span></span>


```C++
DWORD_PTR AddAdvisePacket(
  [ref] const REFERENCE_TIME &time1,
  [ref] const REFERENCE_TIME &time2,
              HANDLE         hNotify,
              BOOL           bPeriodic
);
```



## <a name="parameters"></a><span data-ttu-id="73e65-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="73e65-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73e65-107">*time1* \[ ЗНАЧ\]</span><span class="sxs-lookup"><span data-stu-id="73e65-107">*time1* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="73e65-108">Запрошенное время для уведомления.</span><span class="sxs-lookup"><span data-stu-id="73e65-108">Requested time for the advise.</span></span>

</dd> <dt>

<span data-ttu-id="73e65-109">*time2* \[ ЗНАЧ\]</span><span class="sxs-lookup"><span data-stu-id="73e65-109">*time2* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="73e65-110">Для периодических запросов рекомендаций — время между уведомлениями.</span><span class="sxs-lookup"><span data-stu-id="73e65-110">For periodic advise requests, the time between notifications.</span></span> <span data-ttu-id="73e65-111">Этот параметр игнорируется, если *бпериодик* имеет **значение false**.</span><span class="sxs-lookup"><span data-stu-id="73e65-111">This parameter is ignored if *bPeriodic* is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="73e65-112">*хнотифи*</span><span class="sxs-lookup"><span data-stu-id="73e65-112">*hNotify*</span></span> 
</dt> <dd>

<span data-ttu-id="73e65-113">Обработчик для семафора, если *бпериодик* имеет **значение true**, или обрабатывает событие, если *бпериодик* имеет **значение false**.</span><span class="sxs-lookup"><span data-stu-id="73e65-113">Handle to a semaphore if *bPeriodic* is **TRUE**, or handle to an event if *bPeriodic* is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="73e65-114">*бпериодик*</span><span class="sxs-lookup"><span data-stu-id="73e65-114">*bPeriodic*</span></span> 
</dt> <dd>

<span data-ttu-id="73e65-115">Логическое значение, указывающее, следует ли добавить периодическое уведомление или одно уведомление.</span><span class="sxs-lookup"><span data-stu-id="73e65-115">Boolean value that specifies whether to add a periodic notification or a one-shot notification.</span></span> <span data-ttu-id="73e65-116">**Значение true** показывает, что уведомление является периодическим; параметр *time2* указывает время между уведомлениями.</span><span class="sxs-lookup"><span data-stu-id="73e65-116">If **TRUE**, the notification is periodic; the *time2* parameter specifies the time between notifications.</span></span> <span data-ttu-id="73e65-117">Если **значение равно false**, уведомление возникает только один раз.</span><span class="sxs-lookup"><span data-stu-id="73e65-117">If **FALSE**, the notification occurs only once.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="73e65-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="73e65-118">Return value</span></span>

<span data-ttu-id="73e65-119">Возвращает идентификатор для запроса advise ("cookie").</span><span class="sxs-lookup"><span data-stu-id="73e65-119">Returns an identifier for the advise request (the "cookie").</span></span> <span data-ttu-id="73e65-120">Если метод завершается с ошибкой, возвращаемое значение равно нулю.</span><span class="sxs-lookup"><span data-stu-id="73e65-120">If the method fails, the return value is zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="73e65-121">Требования</span><span class="sxs-lookup"><span data-stu-id="73e65-121">Requirements</span></span>



| <span data-ttu-id="73e65-122">Требование</span><span class="sxs-lookup"><span data-stu-id="73e65-122">Requirement</span></span> | <span data-ttu-id="73e65-123">Значение</span><span class="sxs-lookup"><span data-stu-id="73e65-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="73e65-124">Header</span><span class="sxs-lookup"><span data-stu-id="73e65-124">Header</span></span><br/>  | <dl> <span data-ttu-id="73e65-125"><dt>Дссчедуле. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="73e65-125"><dt>Dsschedule.h (include Streams.h)</dt></span></span> </dl>                                                                                |
| <span data-ttu-id="73e65-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="73e65-126">Library</span></span><br/> | <dl> <span data-ttu-id="73e65-127"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="73e65-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73e65-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="73e65-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73e65-129">**Класс Камсчедуле**</span><span class="sxs-lookup"><span data-stu-id="73e65-129">**CAMSchedule Class**</span></span>](camschedule.md)
</dt> </dl>

 

 




