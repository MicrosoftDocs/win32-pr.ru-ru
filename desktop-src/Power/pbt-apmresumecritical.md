---
description: Уведомляет приложения о том, что система возобновила работу.
ms.assetid: f2997905-26c9-4884-ae79-64df5ce6bc55
title: Событие PBT_APMRESUMECRITICAL (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ef4a76e163f2e61e723f4df6572254e8ef89b40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105663112"
---
# <a name="pbt_apmresumecritical-event"></a><span data-ttu-id="192ee-103">\_Событие ПБТ апмресумекритикал</span><span class="sxs-lookup"><span data-stu-id="192ee-103">PBT\_APMRESUMECRITICAL event</span></span>

<span data-ttu-id="192ee-104">\[ПБТ \_ апмресумекритикал доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="192ee-104">\[PBT\_APMRESUMECRITICAL is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="192ee-105">Поддержка этого события была удалена в Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="192ee-105">Support for this event was removed in Windows Vista.</span></span> <span data-ttu-id="192ee-106">Вместо этого используйте [ПБТ \_ апмресумеаутоматик](pbt-apmresumeautomatic.md) .\]</span><span class="sxs-lookup"><span data-stu-id="192ee-106">Use [PBT\_APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md) instead.\]</span></span>

<span data-ttu-id="192ee-107">Уведомляет приложения о том, что система возобновила работу.</span><span class="sxs-lookup"><span data-stu-id="192ee-107">Notifies applications that the system has resumed operation.</span></span> <span data-ttu-id="192ee-108">Это событие может означать, что некоторые или все приложения не получили событие [ \_ апмсуспенд ПБТ](pbt-apmsuspend.md) .</span><span class="sxs-lookup"><span data-stu-id="192ee-108">This event can indicate that some or all applications did not receive a [PBT\_APMSUSPEND](pbt-apmsuspend.md) event.</span></span> <span data-ttu-id="192ee-109">Например, это событие можно транслировать после критической приостановки, вызванного неисправным аккумулятором.</span><span class="sxs-lookup"><span data-stu-id="192ee-109">For example, this event can be broadcast after a critical suspension caused by a failing battery.</span></span>

<span data-ttu-id="192ee-110">Окно получает это событие через сообщение [**WM \_ поверброадкаст**](wm-powerbroadcast.md) .</span><span class="sxs-lookup"><span data-stu-id="192ee-110">A window receives this event through the [**WM\_POWERBROADCAST**](wm-powerbroadcast.md) message.</span></span> <span data-ttu-id="192ee-111">Параметры *wParam* и *lParam* задаются, как описано ниже.</span><span class="sxs-lookup"><span data-stu-id="192ee-111">The *wParam* and *lParam* parameters are set as described following.</span></span>


```C++
LRESULT 
CALLBACK 
WindowProc( HWND   hwnd,    // handle to window
            UINT   uMsg,    // WM_POWERBROADCAST
            WPARAM wParam,  // PBT_APMRESUMECRITICAL
            LPARAM lParam); // zero
```



## <a name="parameters"></a><span data-ttu-id="192ee-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="192ee-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="192ee-113">*HWND*</span><span class="sxs-lookup"><span data-stu-id="192ee-113">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="192ee-114">Маркер для окна.</span><span class="sxs-lookup"><span data-stu-id="192ee-114">A handle to window.</span></span>

<span data-ttu-id="192ee-115"></dd> <dt>*uiacp*</dt> </span><span class="sxs-lookup"><span data-stu-id="192ee-115"></dd> <dt>*uMsg* </dt> </span></span><dd> 

| <span data-ttu-id="192ee-116">Значение</span><span class="sxs-lookup"><span data-stu-id="192ee-116">Value</span></span>                                                                                                                                                                                                                                                                   | <span data-ttu-id="192ee-117">Значение</span><span class="sxs-lookup"><span data-stu-id="192ee-117">Meaning</span></span>                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span id="WM_POWERBROADCAST"></span><span id="wm_powerbroadcast"></span><dl> <span data-ttu-id="192ee-118"><dt>**[**WM \_ ПОВЕРБРОАДКАСТ**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span><span class="sxs-lookup"><span data-stu-id="192ee-118"><dt>**[**WM\_POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span></span> </dl> | <span data-ttu-id="192ee-119">Идентификатор сообщения.</span><span class="sxs-lookup"><span data-stu-id="192ee-119">Message identifier.</span></span><br/> |



 

<span data-ttu-id="192ee-120"></dd> <dt>*wParam*</dt> </span><span class="sxs-lookup"><span data-stu-id="192ee-120"></dd> <dt>*wParam* </dt> </span></span><dd> 

| <span data-ttu-id="192ee-121">Значение</span><span class="sxs-lookup"><span data-stu-id="192ee-121">Value</span></span>                                                                                                                                                                                                                                              | <span data-ttu-id="192ee-122">Значение</span><span class="sxs-lookup"><span data-stu-id="192ee-122">Meaning</span></span>                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="PBT_APMRESUMECRITICAL"></span><span id="pbt_apmresumecritical"></span><dl> <span data-ttu-id="192ee-123"><dt>**ПБТ \_ АПМРЕСУМЕКРИТИКАЛ**</dt> <dt>6 (0x6)</dt></span><span class="sxs-lookup"><span data-stu-id="192ee-123"><dt>**PBT\_APMRESUMECRITICAL**</dt> <dt>6 (0x6)</dt></span></span> </dl> | <span data-ttu-id="192ee-124">Идентификатор события.</span><span class="sxs-lookup"><span data-stu-id="192ee-124">Event identifier.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="192ee-125">*lParam*</span><span class="sxs-lookup"><span data-stu-id="192ee-125">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="192ee-126">Процессу должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="192ee-126">Reserved; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="192ee-127">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="192ee-127">Return value</span></span>

<span data-ttu-id="192ee-128">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="192ee-128">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="192ee-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="192ee-129">Remarks</span></span>

<span data-ttu-id="192ee-130">Так как критическая приостановка происходит без предварительного уведомления, ранее доступные ресурсы и данные могут отсутствовать, когда приложение получит это событие.</span><span class="sxs-lookup"><span data-stu-id="192ee-130">Because a critical suspension occurs without prior notification, resources and data previously available may not be present when the application receives this event.</span></span> <span data-ttu-id="192ee-131">Приложение должно попытаться восстановить свое состояние до оптимальной способности.</span><span class="sxs-lookup"><span data-stu-id="192ee-131">The application should attempt to restore its state to the best of its ability.</span></span> <span data-ttu-id="192ee-132">В критической приостановке система поддерживает состояние DRAM и локальные жесткие диски, но может не поддерживать сетевые подключения.</span><span class="sxs-lookup"><span data-stu-id="192ee-132">While in a critical suspension, the system maintains the state of the DRAM and local hard disks, but may not maintain net connections.</span></span> <span data-ttu-id="192ee-133">Приложению может потребоваться принять меры относительно файлов, открытых в сети до критической приостановки.</span><span class="sxs-lookup"><span data-stu-id="192ee-133">An application may need to take action with respect to files that were open on the network before critical suspension.</span></span>

## <a name="requirements"></a><span data-ttu-id="192ee-134">Требования</span><span class="sxs-lookup"><span data-stu-id="192ee-134">Requirements</span></span>



| <span data-ttu-id="192ee-135">Требование</span><span class="sxs-lookup"><span data-stu-id="192ee-135">Requirement</span></span> | <span data-ttu-id="192ee-136">Значение</span><span class="sxs-lookup"><span data-stu-id="192ee-136">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="192ee-137">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="192ee-137">Minimum supported client</span></span><br/> | <span data-ttu-id="192ee-138">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="192ee-138">Windows XP \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="192ee-139">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="192ee-139">Minimum supported server</span></span><br/> | <span data-ttu-id="192ee-140">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="192ee-140">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="192ee-141">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="192ee-141">End of client support</span></span><br/>    | <span data-ttu-id="192ee-142">Windows XP</span><span class="sxs-lookup"><span data-stu-id="192ee-142">Windows XP</span></span><br/>                                                                                    |
| <span data-ttu-id="192ee-143">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="192ee-143">End of server support</span></span><br/>    | <span data-ttu-id="192ee-144">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="192ee-144">Windows Server 2003</span></span><br/>                                                                           |
| <span data-ttu-id="192ee-145">Header</span><span class="sxs-lookup"><span data-stu-id="192ee-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="192ee-146"><dt>WinUser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="192ee-146"><dt>WinUser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="192ee-147">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="192ee-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="192ee-148">События пробуждения системы</span><span class="sxs-lookup"><span data-stu-id="192ee-148">System Wake-up Events</span></span>](system-wake-up-events.md)
</dt> <dt>

[<span data-ttu-id="192ee-149">События управления питанием</span><span class="sxs-lookup"><span data-stu-id="192ee-149">Power Management Events</span></span>](power-management-events.md)
</dt> <dt>

[<span data-ttu-id="192ee-150">**WM \_ поверброадкаст**</span><span class="sxs-lookup"><span data-stu-id="192ee-150">**WM\_POWERBROADCAST**</span></span>](wm-powerbroadcast.md)
</dt> </dl>

 

 




