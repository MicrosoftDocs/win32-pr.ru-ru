---
description: Уведомляет приложения о том, что система возобновила работу после приостановки.
ms.assetid: 9058a2ff-9b8e-48e5-accb-4810c8598294
title: Событие PBT_APMRESUMESUSPEND (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d26357215853e0989851b6a9e731340a8dc2e6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105663111"
---
# <a name="pbt_apmresumesuspend-event"></a><span data-ttu-id="2a748-103">\_Событие ПБТ апмресумесуспенд</span><span class="sxs-lookup"><span data-stu-id="2a748-103">PBT\_APMRESUMESUSPEND event</span></span>

<span data-ttu-id="2a748-104">Уведомляет приложения о том, что система возобновила работу после приостановки.</span><span class="sxs-lookup"><span data-stu-id="2a748-104">Notifies applications that the system has resumed operation after being suspended.</span></span>

<span data-ttu-id="2a748-105">Окно получает это событие через сообщение [**WM \_ поверброадкаст**](wm-powerbroadcast.md) .</span><span class="sxs-lookup"><span data-stu-id="2a748-105">A window receives this event through the [**WM\_POWERBROADCAST**](wm-powerbroadcast.md) message.</span></span> <span data-ttu-id="2a748-106">Параметры *wParam* и *lParam* задаются, как описано ниже.</span><span class="sxs-lookup"><span data-stu-id="2a748-106">The *wParam* and *lParam* parameters are set as described following.</span></span>


```C++
LRESULT 
CALLBACK 
WindowProc( HWND hwnd,      // handle to window
            UINT uMsg,      // WM_POWERBROADCAST
            WPARAM wParam,  // PBT_APMRESUMESUSPEND
            LPARAM lParam); // zero
```



## <a name="parameters"></a><span data-ttu-id="2a748-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="2a748-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2a748-108">*HWND*</span><span class="sxs-lookup"><span data-stu-id="2a748-108">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="2a748-109">Маркер для окна.</span><span class="sxs-lookup"><span data-stu-id="2a748-109">A handle to window.</span></span>

<span data-ttu-id="2a748-110"></dd> <dt>*uiacp*</dt> </span><span class="sxs-lookup"><span data-stu-id="2a748-110"></dd> <dt>*uMsg* </dt> </span></span><dd> 

| <span data-ttu-id="2a748-111">Значение</span><span class="sxs-lookup"><span data-stu-id="2a748-111">Value</span></span>                                                                                                                                                                                                                                                                   | <span data-ttu-id="2a748-112">Значение</span><span class="sxs-lookup"><span data-stu-id="2a748-112">Meaning</span></span>                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span id="WM_POWERBROADCAST"></span><span id="wm_powerbroadcast"></span><dl> <span data-ttu-id="2a748-113"><dt>**[**WM \_ ПОВЕРБРОАДКАСТ**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span><span class="sxs-lookup"><span data-stu-id="2a748-113"><dt>**[**WM\_POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span></span> </dl> | <span data-ttu-id="2a748-114">Идентификатор сообщения.</span><span class="sxs-lookup"><span data-stu-id="2a748-114">Message identifier.</span></span><br/> |



 

<span data-ttu-id="2a748-115"></dd> <dt>*wParam*</dt> </span><span class="sxs-lookup"><span data-stu-id="2a748-115"></dd> <dt>*wParam* </dt> </span></span><dd> 

| <span data-ttu-id="2a748-116">Значение</span><span class="sxs-lookup"><span data-stu-id="2a748-116">Value</span></span>                                                                                                                                                                                                                                           | <span data-ttu-id="2a748-117">Значение</span><span class="sxs-lookup"><span data-stu-id="2a748-117">Meaning</span></span>                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="PBT_APMRESUMESUSPEND"></span><span id="pbt_apmresumesuspend"></span><dl> <span data-ttu-id="2a748-118"><dt>**ПБТ \_ АПМРЕСУМЕСУСПЕНД**</dt> <dt>7 (0x7)</dt></span><span class="sxs-lookup"><span data-stu-id="2a748-118"><dt>**PBT\_APMRESUMESUSPEND**</dt> <dt>7 (0x7)</dt></span></span> </dl> | <span data-ttu-id="2a748-119">Идентификатор события.</span><span class="sxs-lookup"><span data-stu-id="2a748-119">Event identifier.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="2a748-120">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2a748-120">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2a748-121">Процессу должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="2a748-121">Reserved; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2a748-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2a748-122">Return value</span></span>

<span data-ttu-id="2a748-123">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="2a748-123">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2a748-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2a748-124">Remarks</span></span>

<span data-ttu-id="2a748-125">Приложение может получать это событие только в том случае, если оно получило событие [ПБТ \_ апмсуспенд](pbt-apmsuspend.md) до того, как компьютер был приостановлен.</span><span class="sxs-lookup"><span data-stu-id="2a748-125">An application can receive this event only if it received the [PBT\_APMSUSPEND](pbt-apmsuspend.md) event before the computer was suspended.</span></span> <span data-ttu-id="2a748-126">В противном случае приложение получит событие [ПБТ \_ апмресумекритикал](pbt-apmresumecritical.md) .</span><span class="sxs-lookup"><span data-stu-id="2a748-126">Otherwise, the application will receive a [PBT\_APMRESUMECRITICAL](pbt-apmresumecritical.md) event.</span></span>

<span data-ttu-id="2a748-127">Если система выходит из системы из-за активности пользователя (например, нажатия кнопки питания) или система обнаруживает взаимодействие пользователя на физической консоли (например, ввод с помощью мыши или клавиатуры) после автоматического пробуждения, система сначала передает событие [ПБТ \_ апмресумеаутоматик](pbt-apmresumeautomatic.md) , а затем передает \_ событие ПБТ апмресумесуспенд.</span><span class="sxs-lookup"><span data-stu-id="2a748-127">If the system wakes due to user activity (such as pressing the power button) or if the system detects user interaction at the physical console (such as mouse or keyboard input) after waking unattended, the system first broadcasts the [PBT\_APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md) event, then it broadcasts the PBT\_APMRESUMESUSPEND event.</span></span> <span data-ttu-id="2a748-128">Кроме того, система включает отображение.</span><span class="sxs-lookup"><span data-stu-id="2a748-128">In addition, the system turns on the display.</span></span> <span data-ttu-id="2a748-129">Приложение должно повторно открывать закрытые файлы, когда система перешла в спящий режим, и подготовиться к вводу данных пользователем.</span><span class="sxs-lookup"><span data-stu-id="2a748-129">Your application should reopen files that it closed when the system entered sleep and prepare for user input.</span></span>

<span data-ttu-id="2a748-130">Если система пробуждается из-за внешнего сигнала пробуждения (удаленного пробуждения), система передает только событие [ПБТ \_ апмресумеаутоматик](pbt-apmresumeautomatic.md) .</span><span class="sxs-lookup"><span data-stu-id="2a748-130">If the system wakes due to an external wake signal (remote wake), the system broadcasts only the [PBT\_APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md) event.</span></span> <span data-ttu-id="2a748-131">Событие ПБТ \_ апмресумесуспенд не отправлено.</span><span class="sxs-lookup"><span data-stu-id="2a748-131">The PBT\_APMRESUMESUSPEND event is not sent.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a748-132">Требования</span><span class="sxs-lookup"><span data-stu-id="2a748-132">Requirements</span></span>



| <span data-ttu-id="2a748-133">Требование</span><span class="sxs-lookup"><span data-stu-id="2a748-133">Requirement</span></span> | <span data-ttu-id="2a748-134">Значение</span><span class="sxs-lookup"><span data-stu-id="2a748-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a748-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2a748-135">Minimum supported client</span></span><br/> | <span data-ttu-id="2a748-136">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="2a748-136">Windows XP \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="2a748-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2a748-137">Minimum supported server</span></span><br/> | <span data-ttu-id="2a748-138">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2a748-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="2a748-139">Header</span><span class="sxs-lookup"><span data-stu-id="2a748-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="2a748-140"><dt>WinUser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2a748-140"><dt>WinUser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2a748-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2a748-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a748-142">События пробуждения системы</span><span class="sxs-lookup"><span data-stu-id="2a748-142">System Wake-up Events</span></span>](system-wake-up-events.md)
</dt> <dt>

[<span data-ttu-id="2a748-143">События управления питанием</span><span class="sxs-lookup"><span data-stu-id="2a748-143">Power Management Events</span></span>](power-management-events.md)
</dt> <dt>

[<span data-ttu-id="2a748-144">ПБТ \_ апмсуспенд</span><span class="sxs-lookup"><span data-stu-id="2a748-144">PBT\_APMSUSPEND</span></span>](pbt-apmsuspend.md)
</dt> <dt>

[<span data-ttu-id="2a748-145">ПБТ \_ апмресумекритикал</span><span class="sxs-lookup"><span data-stu-id="2a748-145">PBT\_APMRESUMECRITICAL</span></span>](pbt-apmresumecritical.md)
</dt> <dt>

[<span data-ttu-id="2a748-146">**WM \_ поверброадкаст**</span><span class="sxs-lookup"><span data-stu-id="2a748-146">**WM\_POWERBROADCAST**</span></span>](wm-powerbroadcast.md)
</dt> </dl>

 

 




