---
description: Сообщает приложениям, что разрешение на приостановку компьютера было отклонено.
ms.assetid: 0f68628f-9d38-45ca-9487-95bf62075e00
title: Событие PBT_APMQUERYSUSPENDFAILED (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1544cd5ed94ae0228c739e2ddb576b0bd77146eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673803"
---
# <a name="pbt_apmquerysuspendfailed-event"></a><span data-ttu-id="31019-103">\_Событие ПБТ апмкуерисуспендфаилед</span><span class="sxs-lookup"><span data-stu-id="31019-103">PBT\_APMQUERYSUSPENDFAILED event</span></span>

<span data-ttu-id="31019-104">\[ПБТ \_ апмкуерисуспендфаилед доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="31019-104">\[PBT\_APMQUERYSUSPENDFAILED is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="31019-105">Поддержка этого события была удалена в Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="31019-105">Support for this event was removed in Windows Vista.</span></span> <span data-ttu-id="31019-106">Вместо этого используйте [**SetThreadExecutionState**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate) .\]</span><span class="sxs-lookup"><span data-stu-id="31019-106">Use [**SetThreadExecutionState**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate) instead.\]</span></span>

<span data-ttu-id="31019-107">Сообщает приложениям, что разрешение на приостановку компьютера было отклонено.</span><span class="sxs-lookup"><span data-stu-id="31019-107">Notifies applications that permission to suspend the computer was denied.</span></span> <span data-ttu-id="31019-108">Это событие является широковещательным, если какое-либо приложение или драйвер вернули **широковещательный \_ запрос \_** на предыдущее событие [ПБТ \_ апмкуерисуспенд](pbt-apmquerysuspend.md) .</span><span class="sxs-lookup"><span data-stu-id="31019-108">This event is broadcast if any application or driver returned **BROADCAST\_QUERY\_DENY** to a previous [PBT\_APMQUERYSUSPEND](pbt-apmquerysuspend.md) event.</span></span>

<span data-ttu-id="31019-109">Окно получает это событие через сообщение [**WM \_ поверброадкаст**](wm-powerbroadcast.md) .</span><span class="sxs-lookup"><span data-stu-id="31019-109">A window receives this event through the [**WM\_POWERBROADCAST**](wm-powerbroadcast.md) message.</span></span> <span data-ttu-id="31019-110">Параметры *wParam* и *lParam* задаются, как описано ниже.</span><span class="sxs-lookup"><span data-stu-id="31019-110">The *wParam* and *lParam* parameters are set as described following.</span></span>


```C++
LRESULT 
CALLBACK 
WindowProc( HWND   hwnd,    // handle to window
            UINT   uMsg,    // WM_POWERBROADCAST
            WPARAM wParam,  // PBT_APMQUERYSUSPENDFAILED
            LPARAM lParam); // zero
```



## <a name="parameters"></a><span data-ttu-id="31019-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="31019-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31019-112">*HWND*</span><span class="sxs-lookup"><span data-stu-id="31019-112">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="31019-113">Маркер для окна.</span><span class="sxs-lookup"><span data-stu-id="31019-113">A handle to window.</span></span>

<span data-ttu-id="31019-114"></dd> <dt>*uiacp*</dt> </span><span class="sxs-lookup"><span data-stu-id="31019-114"></dd> <dt>*uMsg* </dt> </span></span><dd> 

| <span data-ttu-id="31019-115">Значение</span><span class="sxs-lookup"><span data-stu-id="31019-115">Value</span></span>                                                                                                                                                                                                                                                                   | <span data-ttu-id="31019-116">Значение</span><span class="sxs-lookup"><span data-stu-id="31019-116">Meaning</span></span>                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span id="WM_POWERBROADCAST"></span><span id="wm_powerbroadcast"></span><dl> <span data-ttu-id="31019-117"><dt>**[**WM \_ ПОВЕРБРОАДКАСТ**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span><span class="sxs-lookup"><span data-stu-id="31019-117"><dt>**[**WM\_POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span></span> </dl> | <span data-ttu-id="31019-118">Идентификатор сообщения.</span><span class="sxs-lookup"><span data-stu-id="31019-118">Message identifier.</span></span><br/> |



 

<span data-ttu-id="31019-119"></dd> <dt>*wParam*</dt> </span><span class="sxs-lookup"><span data-stu-id="31019-119"></dd> <dt>*wParam* </dt> </span></span><dd> 

| <span data-ttu-id="31019-120">Значение</span><span class="sxs-lookup"><span data-stu-id="31019-120">Value</span></span>                                                                                                                                                                                                                                                          | <span data-ttu-id="31019-121">Значение</span><span class="sxs-lookup"><span data-stu-id="31019-121">Meaning</span></span>                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="PBT_APMQUERYSUSPENDFAILED"></span><span id="pbt_apmquerysuspendfailed"></span><dl> <span data-ttu-id="31019-122"><dt>**ПБТ \_ АПМКУЕРИСУСПЕНДФАИЛЕД**</dt> <dt>2 (0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="31019-122"><dt>**PBT\_APMQUERYSUSPENDFAILED**</dt> <dt>2 (0x2)</dt></span></span> </dl> | <span data-ttu-id="31019-123">Идентификатор события.</span><span class="sxs-lookup"><span data-stu-id="31019-123">Event identifier.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="31019-124">*lParam*</span><span class="sxs-lookup"><span data-stu-id="31019-124">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="31019-125">Процессу должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="31019-125">Reserved; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31019-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="31019-126">Return value</span></span>

<span data-ttu-id="31019-127">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="31019-127">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="31019-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="31019-128">Remarks</span></span>

<span data-ttu-id="31019-129">Приложения обычно реагируют на это событие путем возобновления нормальной работы.</span><span class="sxs-lookup"><span data-stu-id="31019-129">Applications typically respond to this event by resuming normal operation.</span></span>

## <a name="requirements"></a><span data-ttu-id="31019-130">Требования</span><span class="sxs-lookup"><span data-stu-id="31019-130">Requirements</span></span>



| <span data-ttu-id="31019-131">Требование</span><span class="sxs-lookup"><span data-stu-id="31019-131">Requirement</span></span> | <span data-ttu-id="31019-132">Значение</span><span class="sxs-lookup"><span data-stu-id="31019-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31019-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="31019-133">Minimum supported client</span></span><br/> | <span data-ttu-id="31019-134">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="31019-134">Windows XP \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="31019-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="31019-135">Minimum supported server</span></span><br/> | <span data-ttu-id="31019-136">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="31019-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="31019-137">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="31019-137">End of client support</span></span><br/>    | <span data-ttu-id="31019-138">Windows XP</span><span class="sxs-lookup"><span data-stu-id="31019-138">Windows XP</span></span><br/>                                                                                    |
| <span data-ttu-id="31019-139">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="31019-139">End of server support</span></span><br/>    | <span data-ttu-id="31019-140">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="31019-140">Windows Server 2003</span></span><br/>                                                                           |
| <span data-ttu-id="31019-141">Header</span><span class="sxs-lookup"><span data-stu-id="31019-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="31019-142"><dt>WinUser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="31019-142"><dt>WinUser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31019-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="31019-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31019-144">Управление питанием</span><span class="sxs-lookup"><span data-stu-id="31019-144">Power Management</span></span>](power-management-portal.md)
</dt> <dt>

[<span data-ttu-id="31019-145">События управления питанием</span><span class="sxs-lookup"><span data-stu-id="31019-145">Power Management Events</span></span>](power-management-events.md)
</dt> <dt>

[<span data-ttu-id="31019-146">ПБТ \_ апмкуерисуспенд</span><span class="sxs-lookup"><span data-stu-id="31019-146">PBT\_APMQUERYSUSPEND</span></span>](pbt-apmquerysuspend.md)
</dt> <dt>

[<span data-ttu-id="31019-147">**WM \_ поверброадкаст**</span><span class="sxs-lookup"><span data-stu-id="31019-147">**WM\_POWERBROADCAST**</span></span>](wm-powerbroadcast.md)
</dt> </dl>

 

 




