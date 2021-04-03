---
description: Запрашивает разрешение на приостановку работы компьютера. Приложение, предоставляющее такое разрешение, должно предварительно выполнить все необходимые действия для приостановки работы.
ms.assetid: 83cb0fdc-437e-4d03-87f0-6a416281c0d5
title: Событие PBT_APMQUERYSUSPEND (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 277e4faf7617037b917dedab3193e421a381166a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909691"
---
# <a name="pbt_apmquerysuspend-event"></a><span data-ttu-id="e9eeb-104">\_Событие ПБТ апмкуерисуспенд</span><span class="sxs-lookup"><span data-stu-id="e9eeb-104">PBT\_APMQUERYSUSPEND event</span></span>

<span data-ttu-id="e9eeb-105">\[ПБТ \_ апмкуерисуспенд доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="e9eeb-105">\[PBT\_APMQUERYSUSPEND is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="e9eeb-106">Поддержка этого события была удалена в Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e9eeb-106">Support for this event was removed in Windows Vista.</span></span> <span data-ttu-id="e9eeb-107">Вместо этого используйте [**SetThreadExecutionState**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate) .\]</span><span class="sxs-lookup"><span data-stu-id="e9eeb-107">Use [**SetThreadExecutionState**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate) instead.\]</span></span>

<span data-ttu-id="e9eeb-108">Запрашивает разрешение на приостановку работы компьютера.</span><span class="sxs-lookup"><span data-stu-id="e9eeb-108">Requests permission to suspend the computer.</span></span> <span data-ttu-id="e9eeb-109">Приложение, предоставляющее такое разрешение, должно предварительно выполнить все необходимые действия для приостановки работы.</span><span class="sxs-lookup"><span data-stu-id="e9eeb-109">An application that grants permission should carry out preparations for the suspension before returning.</span></span>

<span data-ttu-id="e9eeb-110">Окно получает это событие через сообщение [**WM \_ поверброадкаст**](wm-powerbroadcast.md) .</span><span class="sxs-lookup"><span data-stu-id="e9eeb-110">A window receives this event through the [**WM\_POWERBROADCAST**](wm-powerbroadcast.md) message.</span></span> <span data-ttu-id="e9eeb-111">Параметры *wParam* и *lParam* задаются, как описано ниже.</span><span class="sxs-lookup"><span data-stu-id="e9eeb-111">The *wParam* and *lParam* parameters are set as described following.</span></span>


```C++
LRESULT 
CALLBACK 
WindowProc( HWND   hwnd,    // handle to window
            UINT   uMsg,    // WM_POWERBROADCAST
            WPARAM wParam,  // PBT_APMQUERYSUSPEND
            LPARAM lParam); // action flags
```



## <a name="parameters"></a><span data-ttu-id="e9eeb-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="e9eeb-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9eeb-113">*HWND*</span><span class="sxs-lookup"><span data-stu-id="e9eeb-113">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="e9eeb-114">Маркер для окна.</span><span class="sxs-lookup"><span data-stu-id="e9eeb-114">A handle to window.</span></span>

<span data-ttu-id="e9eeb-115"></dd> <dt>*uiacp*</dt> </span><span class="sxs-lookup"><span data-stu-id="e9eeb-115"></dd> <dt>*uMsg* </dt> </span></span><dd> 

| <span data-ttu-id="e9eeb-116">Значение</span><span class="sxs-lookup"><span data-stu-id="e9eeb-116">Value</span></span>                                                                                                                                                                                                                                                                   | <span data-ttu-id="e9eeb-117">Значение</span><span class="sxs-lookup"><span data-stu-id="e9eeb-117">Meaning</span></span>                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span id="WM_POWERBROADCAST"></span><span id="wm_powerbroadcast"></span><dl> <span data-ttu-id="e9eeb-118"><dt>**[**WM \_ ПОВЕРБРОАДКАСТ**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span><span class="sxs-lookup"><span data-stu-id="e9eeb-118"><dt>**[**WM\_POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span></span> </dl> | <span data-ttu-id="e9eeb-119">Идентификатор сообщения.</span><span class="sxs-lookup"><span data-stu-id="e9eeb-119">Message identifier.</span></span><br/> |



 

<span data-ttu-id="e9eeb-120"></dd> <dt>*wParam*</dt> </span><span class="sxs-lookup"><span data-stu-id="e9eeb-120"></dd> <dt>*wParam* </dt> </span></span><dd> 

| <span data-ttu-id="e9eeb-121">Значение</span><span class="sxs-lookup"><span data-stu-id="e9eeb-121">Value</span></span>                                                                                                                                                                                                                                        | <span data-ttu-id="e9eeb-122">Значение</span><span class="sxs-lookup"><span data-stu-id="e9eeb-122">Meaning</span></span>                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="PBT_APMQUERYSUSPEND"></span><span id="pbt_apmquerysuspend"></span><dl> <span data-ttu-id="e9eeb-123"><dt>**ПБТ \_ АПМКУЕРИСУСПЕНД**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="e9eeb-123"><dt>**PBT\_APMQUERYSUSPEND**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="e9eeb-124">Идентификатор события.</span><span class="sxs-lookup"><span data-stu-id="e9eeb-124">Event identifier.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="e9eeb-125">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e9eeb-125">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e9eeb-126">Флаги действия.</span><span class="sxs-lookup"><span data-stu-id="e9eeb-126">The action flags.</span></span> <span data-ttu-id="e9eeb-127">Если бит 0 равен 1, приложение может запросить у пользователя инструкции по подготовке к приостановке; в противном случае приложение должно подготовиться без взаимодействия с пользователем.</span><span class="sxs-lookup"><span data-stu-id="e9eeb-127">If bit 0 is 1, the application can prompt the user for directions on how to prepare for the suspension; otherwise, the application must prepare without user interaction.</span></span> <span data-ttu-id="e9eeb-128">Все остальные битовые значения зарезервированы.</span><span class="sxs-lookup"><span data-stu-id="e9eeb-128">All other bit values are reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9eeb-129">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e9eeb-129">Return value</span></span>

<span data-ttu-id="e9eeb-130">Для предоставления запроса на приостановку возвращается **значение true** .</span><span class="sxs-lookup"><span data-stu-id="e9eeb-130">Return **TRUE** to grant the request to suspend.</span></span> <span data-ttu-id="e9eeb-131">Чтобы отклонить запрос, возвратите **широковещательный \_ запрос \_ Deny**.</span><span class="sxs-lookup"><span data-stu-id="e9eeb-131">To deny the request, return **BROADCAST\_QUERY\_DENY**.</span></span>

## <a name="remarks"></a><span data-ttu-id="e9eeb-132">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e9eeb-132">Remarks</span></span>

<span data-ttu-id="e9eeb-133">Приложение должно обрабатывать это событие как можно быстрее.</span><span class="sxs-lookup"><span data-stu-id="e9eeb-133">An application should process this event as quickly as possible.</span></span> <span data-ttu-id="e9eeb-134">Приложение может запросить у пользователя инструкции по подготовке к приостановке только в том случае, если установлен бит 0 в параметре *flags* .</span><span class="sxs-lookup"><span data-stu-id="e9eeb-134">The application can prompt the user for directions on how to prepare for suspension only if bit 0 in the *Flags* parameter is set.</span></span> <span data-ttu-id="e9eeb-135">Однако если это сообщение выдается из-за того, что пользователь закрывает крышку ноутбука, запрос пользователя будет невозможен.</span><span class="sxs-lookup"><span data-stu-id="e9eeb-135">However, if this message is issued because the user is closing the laptop lid, it will not be possible to prompt the user.</span></span> <span data-ttu-id="e9eeb-136">Приложения должны учитывать, что пользователь должен иметь определенное поведение при закрытии крышки ноутбука или нажатии кнопки питания и допускать успешность перехода.</span><span class="sxs-lookup"><span data-stu-id="e9eeb-136">Applications should respect that the user expects a certain behavior when they close the laptop lid or press the power button and allow the transition to succeed.</span></span>

<span data-ttu-id="e9eeb-137">Система позволяет приложению приблизительно 20 секунд удалить сообщение [**WM \_ поверброадкаст**](wm-powerbroadcast.md) , которое ОТПРАВЛЯЕТ \_ событие апмкуерисуспенд ПБТ из очереди сообщений приложения.</span><span class="sxs-lookup"><span data-stu-id="e9eeb-137">The system allows approximately 20 seconds for an application to remove the [**WM\_POWERBROADCAST**](wm-powerbroadcast.md) message that is sending the PBT\_APMQUERYSUSPEND event from the application's message queue.</span></span> <span data-ttu-id="e9eeb-138">Если приложение не удаляет сообщение из очереди менее 20 секунд, система предполагает, что приложение находится в состоянии, не отвечающем на запросы, и что приложение соглашается с запросом о спящем режиме.</span><span class="sxs-lookup"><span data-stu-id="e9eeb-138">If an application does not remove the message from its queue in less than 20 seconds, the system will assume that the application is in a non-responsive state, and that the application agrees to the sleep request.</span></span> <span data-ttu-id="e9eeb-139">Операции с приложениями, которые не обрабатывают очереди сообщений, могут быть прерваны.</span><span class="sxs-lookup"><span data-stu-id="e9eeb-139">Applications that do not process their message queues may have their operations interrupted.</span></span> <span data-ttu-id="e9eeb-140">После того как сообщение будет удалено из очереди сообщений, приложению может потребоваться столько времени, сколько необходимо для выполнения необходимых операций перед входом в спящий режим.</span><span class="sxs-lookup"><span data-stu-id="e9eeb-140">After it removes the message from the message queue, an application can take as much time as needed to perform any required operations before entering the sleep state.</span></span> <span data-ttu-id="e9eeb-141">В настоящее время необходимо выполнить любые операции, которые могут занять больше 20 секунд, так как система допускает выполнение операций только через 20 секунд во время обработки [ПБТ \_ апмсуспенд](pbt-apmsuspend.md) .</span><span class="sxs-lookup"><span data-stu-id="e9eeb-141">Any operations that could take longer then 20 seconds should be performed at this time, since the system allows only 20 seconds for operations to complete during [PBT\_APMSUSPEND](pbt-apmsuspend.md) processing.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9eeb-142">Требования</span><span class="sxs-lookup"><span data-stu-id="e9eeb-142">Requirements</span></span>



| <span data-ttu-id="e9eeb-143">Требование</span><span class="sxs-lookup"><span data-stu-id="e9eeb-143">Requirement</span></span> | <span data-ttu-id="e9eeb-144">Значение</span><span class="sxs-lookup"><span data-stu-id="e9eeb-144">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9eeb-145">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e9eeb-145">Minimum supported client</span></span><br/> | <span data-ttu-id="e9eeb-146">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="e9eeb-146">Windows XP \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="e9eeb-147">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e9eeb-147">Minimum supported server</span></span><br/> | <span data-ttu-id="e9eeb-148">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e9eeb-148">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e9eeb-149">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="e9eeb-149">End of client support</span></span><br/>    | <span data-ttu-id="e9eeb-150">Windows XP</span><span class="sxs-lookup"><span data-stu-id="e9eeb-150">Windows XP</span></span><br/>                                                                                    |
| <span data-ttu-id="e9eeb-151">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="e9eeb-151">End of server support</span></span><br/>    | <span data-ttu-id="e9eeb-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e9eeb-152">Windows Server 2003</span></span><br/>                                                                           |
| <span data-ttu-id="e9eeb-153">Header</span><span class="sxs-lookup"><span data-stu-id="e9eeb-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="e9eeb-154"><dt>WinUser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e9eeb-154"><dt>WinUser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9eeb-155">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e9eeb-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9eeb-156">События пробуждения системы</span><span class="sxs-lookup"><span data-stu-id="e9eeb-156">System Wake-up Events</span></span>](system-wake-up-events.md)
</dt> <dt>

[<span data-ttu-id="e9eeb-157">События управления питанием</span><span class="sxs-lookup"><span data-stu-id="e9eeb-157">Power Management Events</span></span>](power-management-events.md)
</dt> <dt>

[<span data-ttu-id="e9eeb-158">ПБТ \_ апмсуспенд</span><span class="sxs-lookup"><span data-stu-id="e9eeb-158">PBT\_APMSUSPEND</span></span>](pbt-apmsuspend.md)
</dt> <dt>

[<span data-ttu-id="e9eeb-159">**WM \_ поверброадкаст**</span><span class="sxs-lookup"><span data-stu-id="e9eeb-159">**WM\_POWERBROADCAST**</span></span>](wm-powerbroadcast.md)
</dt> </dl>

 

 




