---
description: Уведомляет приложения о том, что система, как правило, является персональным компьютером с питанием от аккумулятора, перейдет в режим приостановки.
ms.assetid: ceaa5ca4-799e-4801-96cd-aeea3dfd7d52
title: Сообщение WM_POWER (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc53fd165ee1cefe8970f85daea04b931a673b33
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673784"
---
# <a name="wm_power-message"></a><span data-ttu-id="e7e45-103">\_Сообщение о питании WM</span><span class="sxs-lookup"><span data-stu-id="e7e45-103">WM\_POWER message</span></span>

<span data-ttu-id="e7e45-104">Уведомляет приложения о том, что система, как правило, является персональным компьютером с питанием от аккумулятора, перейдет в режим приостановки.</span><span class="sxs-lookup"><span data-stu-id="e7e45-104">Notifies applications that the system, typically a battery-powered personal computer, is about to enter a suspended mode.</span></span>

> [!Note]  
> <span data-ttu-id="e7e45-105">Сообщение **\_ Power WM** устарело.</span><span class="sxs-lookup"><span data-stu-id="e7e45-105">The **WM\_POWER** message is obsolete.</span></span> <span data-ttu-id="e7e45-106">Он предоставляется только для обеспечения совместимости с 16-разрядными приложениями на базе Windows.</span><span class="sxs-lookup"><span data-stu-id="e7e45-106">It is provided only for compatibility with 16-bit Windows-based applications.</span></span> <span data-ttu-id="e7e45-107">Приложения должны использовать сообщение [**WM \_ поверброадкаст**](wm-powerbroadcast.md) .</span><span class="sxs-lookup"><span data-stu-id="e7e45-107">Applications should use the [**WM\_POWERBROADCAST**](wm-powerbroadcast.md) message.</span></span>

 

<span data-ttu-id="e7e45-108">Окно получает это сообщение через функцию **WindowProc** .</span><span class="sxs-lookup"><span data-stu-id="e7e45-108">A window receives this message through its **WindowProc** function.</span></span>


```C++
LRESULT CALLBACK WindowProc
  HWND   hwnd,    // handle to window
  UINT   uMsg,    // WM_POWER
  WPARAM wParam,  // power-event notification
  LPARAM lParam   // not used
); 
```



## <a name="parameters"></a><span data-ttu-id="e7e45-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="e7e45-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7e45-110">*HWND*</span><span class="sxs-lookup"><span data-stu-id="e7e45-110">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="e7e45-111">Маркер для окна.</span><span class="sxs-lookup"><span data-stu-id="e7e45-111">A handle to window.</span></span>

</dd> <dt>

<span data-ttu-id="e7e45-112">*Uiacp*</span><span class="sxs-lookup"><span data-stu-id="e7e45-112">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="e7e45-113">Идентификатор сообщения о **\_ питании WM** .</span><span class="sxs-lookup"><span data-stu-id="e7e45-113">The **WM\_POWER** message identifier.</span></span>

</dd> <dt>

<span data-ttu-id="e7e45-114">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e7e45-114">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e7e45-115">Уведомление о событии питания.</span><span class="sxs-lookup"><span data-stu-id="e7e45-115">The power-event notification.</span></span> <span data-ttu-id="e7e45-116">Этот параметр может принимать одно из указанных ниже значений.</span><span class="sxs-lookup"><span data-stu-id="e7e45-116">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="e7e45-117">Значение</span><span class="sxs-lookup"><span data-stu-id="e7e45-117">Value</span></span>                                                                                                                                                                        | <span data-ttu-id="e7e45-118">Значение</span><span class="sxs-lookup"><span data-stu-id="e7e45-118">Meaning</span></span>                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PWR_CRITICALRESUME"></span><span id="pwr_criticalresume"></span><dl> <span data-ttu-id="e7e45-119"><dt>**PWR \_ критикалресуме**</dt></span><span class="sxs-lookup"><span data-stu-id="e7e45-119"><dt>**PWR\_CRITICALRESUME**</dt></span></span> </dl> | <span data-ttu-id="e7e45-120">Указывает, что система возобновляет работу после входа в приостановленный режим без предварительной широковещательной передачи в приложение сообщения **\_ суспендрекуест** с уведомлением.</span><span class="sxs-lookup"><span data-stu-id="e7e45-120">Indicates that the system is resuming operation after entering suspended mode without first broadcasting a **PWR\_SUSPENDREQUEST** notification message to the application.</span></span> <span data-ttu-id="e7e45-121">Приложение должно выполнять все необходимые действия по восстановлению.</span><span class="sxs-lookup"><span data-stu-id="e7e45-121">An application should perform any necessary recovery actions.</span></span><br/>                                                   |
| <span id="PWR_SUSPENDREQUEST"></span><span id="pwr_suspendrequest"></span><dl> <span data-ttu-id="e7e45-122"><dt>**PWR \_ суспендрекуест**</dt></span><span class="sxs-lookup"><span data-stu-id="e7e45-122"><dt>**PWR\_SUSPENDREQUEST**</dt></span></span> </dl> | <span data-ttu-id="e7e45-123">Указывает, что система собирается перейти в режим приостановки.</span><span class="sxs-lookup"><span data-stu-id="e7e45-123">Indicates that the system is about to enter suspended mode.</span></span><br/>                                                                                                                                                                                                                                 |
| <span id="PWR_SUSPENDRESUME"></span><span id="pwr_suspendresume"></span><dl> <span data-ttu-id="e7e45-124"><dt>**PWR \_ суспендресуме**</dt></span><span class="sxs-lookup"><span data-stu-id="e7e45-124"><dt>**PWR\_SUSPENDRESUME**</dt></span></span> </dl>    | <span data-ttu-id="e7e45-125">Указывает, что система возобновляет работу после перехода в режим отложенного режима, что означает, что система передает в приложение сообщение уведомления **PWR \_ суспендрекуест** , прежде чем система была приостановлена.</span><span class="sxs-lookup"><span data-stu-id="e7e45-125">Indicates that the system is resuming operation after having entered suspended mode normally that is, the system broadcast a **PWR\_SUSPENDREQUEST** notification message to the application before the system was suspended.</span></span> <span data-ttu-id="e7e45-126">Приложение должно выполнять все необходимые действия по восстановлению.</span><span class="sxs-lookup"><span data-stu-id="e7e45-126">An application should perform any necessary recovery actions.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="e7e45-127">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e7e45-127">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e7e45-128">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="e7e45-128">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7e45-129">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e7e45-129">Return value</span></span>

<span data-ttu-id="e7e45-130">Значение, возвращаемое приложением, зависит от значения параметра *wParam* .</span><span class="sxs-lookup"><span data-stu-id="e7e45-130">The value an application returns depends on the value of the *wParam* parameter.</span></span> <span data-ttu-id="e7e45-131">Если параметр *wParam* равен **PWR \_ суспендрекуест**, возвращаемое значение — **PWR \_ завершается сбоем** , чтобы предотвратить переход системы в состояние SUSPENDED; в противном случае — **PWR \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="e7e45-131">If *wParam* is **PWR\_SUSPENDREQUEST**, the return value is **PWR\_FAIL** to prevent the system from entering the suspended state; otherwise, it is **PWR\_OK**.</span></span> <span data-ttu-id="e7e45-132">Если параметр *wParam* равен **PWR \_ суспендресуме** или **PWR \_ критикалресуме**, возвращаемое значение равно нулю.</span><span class="sxs-lookup"><span data-stu-id="e7e45-132">If *wParam* is **PWR\_SUSPENDRESUME** or **PWR\_CRITICALRESUME**, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="e7e45-133">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e7e45-133">Remarks</span></span>

<span data-ttu-id="e7e45-134">Это сообщение передается только в приложение, которое работает в системе, которая соответствует спецификации расширенного управления питанием (APM) Basic (BIOS).</span><span class="sxs-lookup"><span data-stu-id="e7e45-134">This message is broadcast only to an application that is running on a system that conforms to the Advanced Power Management (APM) basic input/output system (BIOS) specification.</span></span> <span data-ttu-id="e7e45-135">Сообщение транслируется драйвером управления питанием в каждое окно, возвращаемое функцией **EnumWindows** .</span><span class="sxs-lookup"><span data-stu-id="e7e45-135">The message is broadcast by the power-management driver to each window returned by the **EnumWindows** function.</span></span>

<span data-ttu-id="e7e45-136">Режим приостановки — это состояние, в котором происходит наибольшее количество энергосбережения, но сохраняются все операционные данные и параметры.</span><span class="sxs-lookup"><span data-stu-id="e7e45-136">The suspended mode is the state in which the greatest amount of power savings occurs, but all operational data and parameters are preserved.</span></span> <span data-ttu-id="e7e45-137">Содержимое памяти произвольного доступа (ОЗУ) сохраняется, но многие устройства, скорее всего, будут отключены.</span><span class="sxs-lookup"><span data-stu-id="e7e45-137">Random-access memory (RAM) contents are preserved, but many devices are likely to be turned off.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7e45-138">Требования</span><span class="sxs-lookup"><span data-stu-id="e7e45-138">Requirements</span></span>



| <span data-ttu-id="e7e45-139">Требование</span><span class="sxs-lookup"><span data-stu-id="e7e45-139">Requirement</span></span> | <span data-ttu-id="e7e45-140">Значение</span><span class="sxs-lookup"><span data-stu-id="e7e45-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7e45-141">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e7e45-141">Minimum supported client</span></span><br/> | <span data-ttu-id="e7e45-142">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="e7e45-142">Windows XP \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="e7e45-143">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e7e45-143">Minimum supported server</span></span><br/> | <span data-ttu-id="e7e45-144">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e7e45-144">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e7e45-145">Header</span><span class="sxs-lookup"><span data-stu-id="e7e45-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="e7e45-146"><dt>WinUser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e7e45-146"><dt>WinUser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7e45-147">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e7e45-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7e45-148">**WM \_ поверброадкаст**</span><span class="sxs-lookup"><span data-stu-id="e7e45-148">**WM\_POWERBROADCAST**</span></span>](wm-powerbroadcast.md)
</dt> </dl>

 

 




