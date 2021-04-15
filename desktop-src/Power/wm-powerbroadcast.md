---
description: Уведомляет приложения о том, что произошло событие управления питанием.
ms.assetid: 46452909-ac0e-4c06-8542-0b94d00e6556
title: Сообщение WM_POWERBROADCAST (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82f1b273462d8de27c19d715836d168ab8bf8c90
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104545487"
---
# <a name="wm_powerbroadcast-message"></a><span data-ttu-id="94ab9-103">\_Сообщение ПОВЕРБРОАДКАСТ WM</span><span class="sxs-lookup"><span data-stu-id="94ab9-103">WM\_POWERBROADCAST message</span></span>

<span data-ttu-id="94ab9-104">Уведомляет приложения о том, что произошло событие управления питанием.</span><span class="sxs-lookup"><span data-stu-id="94ab9-104">Notifies applications that a power-management event has occurred.</span></span>

<span data-ttu-id="94ab9-105">Окно получает это сообщение через функцию **WindowProc** .</span><span class="sxs-lookup"><span data-stu-id="94ab9-105">A window receives this message through its **WindowProc** function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND   hwnd,    // handle to window
  UINT   uMsg,    // WM_POWERBROADCAST
  WPARAM wParam,  // power-management event
  LPARAM lParam   // function-specific data
);
```



## <a name="parameters"></a><span data-ttu-id="94ab9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="94ab9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="94ab9-107">*HWND*</span><span class="sxs-lookup"><span data-stu-id="94ab9-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="94ab9-108">Маркер для окна.</span><span class="sxs-lookup"><span data-stu-id="94ab9-108">A handle to window.</span></span>

<span data-ttu-id="94ab9-109"></dd> <dt>*uiacp*</dt> </span><span class="sxs-lookup"><span data-stu-id="94ab9-109"></dd> <dt>*uMsg* </dt> </span></span><dd> 

| <span data-ttu-id="94ab9-110">Значение</span><span class="sxs-lookup"><span data-stu-id="94ab9-110">Value</span></span>                                                                                                                                                                                                                                          | <span data-ttu-id="94ab9-111">Значение</span><span class="sxs-lookup"><span data-stu-id="94ab9-111">Meaning</span></span>                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span id="WM_POWERBROADCAST"></span><span id="wm_powerbroadcast"></span><dl> <span data-ttu-id="94ab9-112">\* \* \* \* <dt>WM \_ ПОВЕРБРОАДКАСТ \* \* \* \*</dt> <dt>536 (0x218)</dt></span><span class="sxs-lookup"><span data-stu-id="94ab9-112"><dt>\*\*\*\*WM\_POWERBROADCAST\*\*\*\*</dt> <dt>536 (0x218)</dt></span></span> </dl> | <span data-ttu-id="94ab9-113">Идентификатор сообщения.</span><span class="sxs-lookup"><span data-stu-id="94ab9-113">Message identifier.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="94ab9-114">*wParam*</span><span class="sxs-lookup"><span data-stu-id="94ab9-114">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="94ab9-115">Событие управления питанием.</span><span class="sxs-lookup"><span data-stu-id="94ab9-115">The power-management event.</span></span> <span data-ttu-id="94ab9-116">Этот параметр может быть одним из следующих идентификаторов событий.</span><span class="sxs-lookup"><span data-stu-id="94ab9-116">This parameter can be one of the following event identifiers.</span></span>



| <span data-ttu-id="94ab9-117">Событие</span><span class="sxs-lookup"><span data-stu-id="94ab9-117">Event</span></span>                                                                                                                                                                                                                                                                                        | <span data-ttu-id="94ab9-118">Значение</span><span class="sxs-lookup"><span data-stu-id="94ab9-118">Meaning</span></span>                                                                                                                                                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PBT_APMPOWERSTATUSCHANGE"></span><span id="pbt_apmpowerstatuschange"></span><dl> <span data-ttu-id="94ab9-119"><dt>**[ПБТ \_ АПМПОВЕРСТАТУСЧАНЖЕ](pbt-apmpowerstatuschange.md)**</dt> <dt>10 (0xA)</dt></span><span class="sxs-lookup"><span data-stu-id="94ab9-119"><dt>**[PBT\_APMPOWERSTATUSCHANGE](pbt-apmpowerstatuschange.md)**</dt> <dt>10 (0xA)</dt></span></span> </dl> | <span data-ttu-id="94ab9-120">Состояние питания изменилось.</span><span class="sxs-lookup"><span data-stu-id="94ab9-120">Power status has changed.</span></span><br/>                                                                                                                                                                        |
| <span id="PBT_APMRESUMEAUTOMATIC"></span><span id="pbt_apmresumeautomatic"></span><dl> <span data-ttu-id="94ab9-121"><dt>**[ПБТ \_ АПМРЕСУМЕАУТОМАТИК](pbt-apmresumeautomatic.md)**</dt> <dt>18 (0x12)</dt></span><span class="sxs-lookup"><span data-stu-id="94ab9-121"><dt>**[PBT\_APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md)**</dt> <dt>18 (0x12)</dt></span></span> </dl>        | <span data-ttu-id="94ab9-122">Операция возобновляется автоматически из состояния пониженного энергопотребления.</span><span class="sxs-lookup"><span data-stu-id="94ab9-122">Operation is resuming automatically from a low-power state.</span></span> <span data-ttu-id="94ab9-123">Это сообщение отправляется при каждом возобновлении системы.</span><span class="sxs-lookup"><span data-stu-id="94ab9-123">This message is sent every time the system resumes.</span></span><br/>                                                                                  |
| <span id="PBT_APMRESUMESUSPEND"></span><span id="pbt_apmresumesuspend"></span><dl> <span data-ttu-id="94ab9-124"><dt>**[ПБТ \_ АПМРЕСУМЕСУСПЕНД](pbt-apmresumesuspend.md)**</dt> <dt>7 (0x7)</dt></span><span class="sxs-lookup"><span data-stu-id="94ab9-124"><dt>**[PBT\_APMRESUMESUSPEND](pbt-apmresumesuspend.md)**</dt> <dt>7 (0x7)</dt></span></span> </dl>                  | <span data-ttu-id="94ab9-125">Операция возобновляется из состояния с низким энергопотреблением.</span><span class="sxs-lookup"><span data-stu-id="94ab9-125">Operation is resuming from a low-power state.</span></span> <span data-ttu-id="94ab9-126">Это сообщение отправляется после [ПБТ \_ апмресумеаутоматик](pbt-apmresumeautomatic.md) , если возобновление запускается вводом пользователя, например нажатием клавиши.</span><span class="sxs-lookup"><span data-stu-id="94ab9-126">This message is sent after [PBT\_APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md) if the resume is triggered by user input, such as pressing a key.</span></span><br/> |
| <span id="PBT_APMSUSPEND"></span><span id="pbt_apmsuspend"></span><dl> <span data-ttu-id="94ab9-127"><dt>**[ПБТ \_ АПМСУСПЕНД](pbt-apmsuspend.md)**</dt> <dt>4 (0x4)</dt></span><span class="sxs-lookup"><span data-stu-id="94ab9-127"><dt>**[PBT\_APMSUSPEND](pbt-apmsuspend.md)**</dt> <dt>4 (0x4)</dt></span></span> </dl>                                          | <span data-ttu-id="94ab9-128">Система приостанавливает операцию.</span><span class="sxs-lookup"><span data-stu-id="94ab9-128">System is suspending operation.</span></span><br/>                                                                                                                                                                  |
| <span id="PBT_POWERSETTINGCHANGE"></span><span id="pbt_powersettingchange"></span><dl> <span data-ttu-id="94ab9-129"><dt>**[ПБТ \_ ПОВЕРСЕТТИНГЧАНЖЕ](pbt-powersettingchange.md)**</dt> <dt>32787 (0x8013)</dt></span><span class="sxs-lookup"><span data-stu-id="94ab9-129"><dt>**[PBT\_POWERSETTINGCHANGE](pbt-powersettingchange.md)**</dt> <dt>32787 (0x8013)</dt></span></span> </dl>   | <span data-ttu-id="94ab9-130">Получено событие изменения параметра питания.</span><span class="sxs-lookup"><span data-stu-id="94ab9-130">A power setting change event has been received.</span></span> <br/>                                                                                                                                                 |



 

</dd> <dt>

<span data-ttu-id="94ab9-131">*lParam*</span><span class="sxs-lookup"><span data-stu-id="94ab9-131">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="94ab9-132">Данные, относящиеся к конкретному событию.</span><span class="sxs-lookup"><span data-stu-id="94ab9-132">The event-specific data.</span></span> <span data-ttu-id="94ab9-133">Для большинства событий этот параметр зарезервирован и не используется.</span><span class="sxs-lookup"><span data-stu-id="94ab9-133">For most events, this parameter is reserved and not used.</span></span>

<span data-ttu-id="94ab9-134">Если параметр *wParam* имеет значение [ПБТ \_ поверсеттингчанже](pbt-powersettingchange.md), параметр *lParam* является указателем на структуру [**\_ параметра поверброадкаст**](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting) .</span><span class="sxs-lookup"><span data-stu-id="94ab9-134">If the *wParam* parameter is [PBT\_POWERSETTINGCHANGE](pbt-powersettingchange.md), the *lParam* parameter is a pointer to a [**POWERBROADCAST\_SETTING**](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="94ab9-135">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="94ab9-135">Return value</span></span>

<span data-ttu-id="94ab9-136">Приложение должно возвращать **значение true** , если обрабатывает это сообщение.</span><span class="sxs-lookup"><span data-stu-id="94ab9-136">An application should return **TRUE** if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="94ab9-137">Комментарии</span><span class="sxs-lookup"><span data-stu-id="94ab9-137">Remarks</span></span>

<span data-ttu-id="94ab9-138">Система всегда отправляет сообщение [ПБТ \_ апмресумеаутоматик](pbt-apmresumeautomatic.md) при возобновлении работы системы.</span><span class="sxs-lookup"><span data-stu-id="94ab9-138">The system always sends a [PBT\_APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md) message whenever the system resumes.</span></span> <span data-ttu-id="94ab9-139">Если система возобновляет работу в ответ на ввод пользователя, например нажатие клавиши, система также отправляет сообщение **ПБТ \_ апмресумесуспенд** после отправки ПБТ \_ апмресумеаутоматик.</span><span class="sxs-lookup"><span data-stu-id="94ab9-139">If the system resumes in response to user input such as pressing a key, the system also sends a **PBT\_APMRESUMESUSPEND** message after sending PBT\_APMRESUMEAUTOMATIC.</span></span>

<span data-ttu-id="94ab9-140">**WM \_ Сообщения ПОВЕРБРОАДКАСТ** не различаются между различными состояниями низкого энергопотребления.</span><span class="sxs-lookup"><span data-stu-id="94ab9-140">**WM\_POWERBROADCAST** messages do not distinguish between different low-power states.</span></span> <span data-ttu-id="94ab9-141">Приложение может определить только то, что система входит в состояние пониженного энергопотребления или возобновлена. Он не может определить конкретное состояние электропитания.</span><span class="sxs-lookup"><span data-stu-id="94ab9-141">An application can determine only that the system is entering or has resumed from a low-power state; it cannot determine the specific power state.</span></span> <span data-ttu-id="94ab9-142">Система записывает сведения о переходах о состоянии электропитания в журнал системных событий Windows.</span><span class="sxs-lookup"><span data-stu-id="94ab9-142">The system records details about power state transitions in the Windows System event log.</span></span>

<span data-ttu-id="94ab9-143">Чтобы предотвратить переход системы в режим с низким энергопотреблением в Windows Vista, приложение должно вызвать [**SetThreadExecutionState**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate) , чтобы сообщить системе, что она используется.</span><span class="sxs-lookup"><span data-stu-id="94ab9-143">To prevent the system from transitioning to a low-power state in Windows Vista, an application must call [**SetThreadExecutionState**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate) to inform the system that it is in use.</span></span>

<span data-ttu-id="94ab9-144">Следующие сообщения не поддерживаются в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="94ab9-144">The following messages are not supported on any of the operating systems specified in the Requirements section:</span></span>

- <span data-ttu-id="94ab9-145">PBT_APMQUERYSTANDBY</span><span class="sxs-lookup"><span data-stu-id="94ab9-145">PBT_APMQUERYSTANDBY</span></span>  
- <span data-ttu-id="94ab9-146">PBT_APMQUERYSTANDBYFAILED</span><span class="sxs-lookup"><span data-stu-id="94ab9-146">PBT_APMQUERYSTANDBYFAILED</span></span>  
- <span data-ttu-id="94ab9-147">PBT_APMSTANDBY</span><span class="sxs-lookup"><span data-stu-id="94ab9-147">PBT_APMSTANDBY</span></span>  
- <span data-ttu-id="94ab9-148">PBT_APMRESUMESTANDBY</span><span class="sxs-lookup"><span data-stu-id="94ab9-148">PBT_APMRESUMESTANDBY</span></span>  

## <a name="requirements"></a><span data-ttu-id="94ab9-149">Требования</span><span class="sxs-lookup"><span data-stu-id="94ab9-149">Requirements</span></span>



| <span data-ttu-id="94ab9-150">Требование</span><span class="sxs-lookup"><span data-stu-id="94ab9-150">Requirement</span></span> | <span data-ttu-id="94ab9-151">Значение</span><span class="sxs-lookup"><span data-stu-id="94ab9-151">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="94ab9-152">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="94ab9-152">Minimum supported client</span></span><br/> | <span data-ttu-id="94ab9-153">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="94ab9-153">Windows XP \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="94ab9-154">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="94ab9-154">Minimum supported server</span></span><br/> | <span data-ttu-id="94ab9-155">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="94ab9-155">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="94ab9-156">Header</span><span class="sxs-lookup"><span data-stu-id="94ab9-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="94ab9-157"><dt>WinUser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="94ab9-157"><dt>WinUser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94ab9-158">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="94ab9-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94ab9-159">\_Сообщения ПОВЕРБРОАДКАСТ WM</span><span class="sxs-lookup"><span data-stu-id="94ab9-159">WM\_POWERBROADCAST Messages</span></span>](wm-powerbroadcast-messages.md)
</dt> <dt>

[<span data-ttu-id="94ab9-160">Сообщения управления питанием</span><span class="sxs-lookup"><span data-stu-id="94ab9-160">Power Management Messages</span></span>](power-management-messages.md)
</dt> </dl>

 

 




