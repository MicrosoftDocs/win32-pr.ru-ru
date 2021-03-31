---
description: Уведомляет приложения о том, что компьютер собирается перейти в приостановленное состояние.
ms.assetid: 61b177a0-4cff-4740-bed8-a46c06c43be8
title: Событие PBT_APMSUSPEND (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2fc6982e00565329c85e06765879b9b72b07fe6a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104264504"
---
# <a name="pbt_apmsuspend-event"></a><span data-ttu-id="644d9-103">\_Событие ПБТ апмсуспенд</span><span class="sxs-lookup"><span data-stu-id="644d9-103">PBT\_APMSUSPEND event</span></span>

<span data-ttu-id="644d9-104">Уведомляет приложения о том, что компьютер собирается перейти в приостановленное состояние.</span><span class="sxs-lookup"><span data-stu-id="644d9-104">Notifies applications that the computer is about to enter a suspended state.</span></span> <span data-ttu-id="644d9-105">Это событие обычно рассылается, если все приложения и устанавливаемые драйверы вернули **значение true** для предыдущего события [ПБТ \_ апмкуерисуспенд](pbt-apmquerysuspend.md) .</span><span class="sxs-lookup"><span data-stu-id="644d9-105">This event is typically broadcast when all applications and installable drivers have returned **TRUE** to a previous [PBT\_APMQUERYSUSPEND](pbt-apmquerysuspend.md) event.</span></span>

<span data-ttu-id="644d9-106">Окно получает это событие через сообщение [**WM \_ поверброадкаст**](wm-powerbroadcast.md) .</span><span class="sxs-lookup"><span data-stu-id="644d9-106">A window receives this event through the [**WM\_POWERBROADCAST**](wm-powerbroadcast.md) message.</span></span> <span data-ttu-id="644d9-107">Параметры *wParam* и *lParam* задаются, как описано ниже.</span><span class="sxs-lookup"><span data-stu-id="644d9-107">The *wParam* and *lParam* parameters are set as described following.</span></span>


```C++
LRESULT 
CALLBACK 
WindowProc( HWND hwnd,      // handle to window
            UINT uMsg,      // WM_POWERBROADCAST
            WPARAM wParam,  // PBT_APMSUSPEND
            LPARAM lParam); // zero
```



## <a name="parameters"></a><span data-ttu-id="644d9-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="644d9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="644d9-109">*HWND*</span><span class="sxs-lookup"><span data-stu-id="644d9-109">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="644d9-110">Маркер для окна.</span><span class="sxs-lookup"><span data-stu-id="644d9-110">A handle to window.</span></span>

<span data-ttu-id="644d9-111"></dd> <dt>*uiacp*</dt> </span><span class="sxs-lookup"><span data-stu-id="644d9-111"></dd> <dt>*uMsg* </dt> </span></span><dd> 

| <span data-ttu-id="644d9-112">Значение</span><span class="sxs-lookup"><span data-stu-id="644d9-112">Value</span></span>                                                                                                                                                                                                                                                                   | <span data-ttu-id="644d9-113">Значение</span><span class="sxs-lookup"><span data-stu-id="644d9-113">Meaning</span></span>                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span id="WM_POWERBROADCAST"></span><span id="wm_powerbroadcast"></span><dl> <span data-ttu-id="644d9-114"><dt>**[**WM \_ ПОВЕРБРОАДКАСТ**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span><span class="sxs-lookup"><span data-stu-id="644d9-114"><dt>**[**WM\_POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span></span> </dl> | <span data-ttu-id="644d9-115">Идентификатор сообщения.</span><span class="sxs-lookup"><span data-stu-id="644d9-115">Message identifier.</span></span><br/> |



 

<span data-ttu-id="644d9-116"></dd> <dt>*wParam*</dt> </span><span class="sxs-lookup"><span data-stu-id="644d9-116"></dd> <dt>*wParam* </dt> </span></span><dd> 

| <span data-ttu-id="644d9-117">Значение</span><span class="sxs-lookup"><span data-stu-id="644d9-117">Value</span></span>                                                                                                                                                                                                                         | <span data-ttu-id="644d9-118">Значение</span><span class="sxs-lookup"><span data-stu-id="644d9-118">Meaning</span></span>                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="PBT_APMSUSPEND"></span><span id="pbt_apmsuspend"></span><dl> <span data-ttu-id="644d9-119"><dt>**ПБТ \_ АПМСУСПЕНД**</dt> <dt>4 (0x4)</dt></span><span class="sxs-lookup"><span data-stu-id="644d9-119"><dt>**PBT\_APMSUSPEND**</dt> <dt>4 (0x4)</dt></span></span> </dl> | <span data-ttu-id="644d9-120">Идентификатор события.</span><span class="sxs-lookup"><span data-stu-id="644d9-120">Event identifier.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="644d9-121">*lParam*</span><span class="sxs-lookup"><span data-stu-id="644d9-121">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="644d9-122">Процессу должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="644d9-122">Reserved; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="644d9-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="644d9-123">Return value</span></span>

<span data-ttu-id="644d9-124">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="644d9-124">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="644d9-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="644d9-125">Remarks</span></span>

<span data-ttu-id="644d9-126">Приложение должно обработать это событие, выполнив все задачи, необходимые для сохранения данных.</span><span class="sxs-lookup"><span data-stu-id="644d9-126">An application should process this event by completing all tasks necessary to save data.</span></span>

<span data-ttu-id="644d9-127">Для того чтобы приложение обрабатывало это уведомление, система предоставляет примерно две секунды.</span><span class="sxs-lookup"><span data-stu-id="644d9-127">The system allows approximately two seconds for an application to handle this notification.</span></span> <span data-ttu-id="644d9-128">Если приложение по-прежнему выполняет операции после истечения времени его выполнения, система может прерывать работу приложения.</span><span class="sxs-lookup"><span data-stu-id="644d9-128">If an application is still performing operations after its time allotment has expired, the system may interrupt the application.</span></span>

## <a name="requirements"></a><span data-ttu-id="644d9-129">Требования</span><span class="sxs-lookup"><span data-stu-id="644d9-129">Requirements</span></span>



| <span data-ttu-id="644d9-130">Требование</span><span class="sxs-lookup"><span data-stu-id="644d9-130">Requirement</span></span> | <span data-ttu-id="644d9-131">Значение</span><span class="sxs-lookup"><span data-stu-id="644d9-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="644d9-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="644d9-132">Minimum supported client</span></span><br/> | <span data-ttu-id="644d9-133">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="644d9-133">Windows XP \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="644d9-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="644d9-134">Minimum supported server</span></span><br/> | <span data-ttu-id="644d9-135">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="644d9-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="644d9-136">Header</span><span class="sxs-lookup"><span data-stu-id="644d9-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="644d9-137"><dt>WinUser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="644d9-137"><dt>WinUser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="644d9-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="644d9-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="644d9-139">Критерии спящего режима системы</span><span class="sxs-lookup"><span data-stu-id="644d9-139">System Sleep Criteria</span></span>](system-sleep-criteria.md)
</dt> <dt>

[<span data-ttu-id="644d9-140">События пробуждения системы</span><span class="sxs-lookup"><span data-stu-id="644d9-140">System Wake-up Events</span></span>](system-wake-up-events.md)
</dt> <dt>

[<span data-ttu-id="644d9-141">События управления питанием</span><span class="sxs-lookup"><span data-stu-id="644d9-141">Power Management Events</span></span>](power-management-events.md)
</dt> <dt>

[<span data-ttu-id="644d9-142">ПБТ \_ апмкуерисуспенд</span><span class="sxs-lookup"><span data-stu-id="644d9-142">PBT\_APMQUERYSUSPEND</span></span>](pbt-apmquerysuspend.md)
</dt> <dt>

[<span data-ttu-id="644d9-143">**сетсистемповерстате**</span><span class="sxs-lookup"><span data-stu-id="644d9-143">**SetSystemPowerState**</span></span>](/windows/desktop/api/WinBase/nf-winbase-setsystempowerstate)
</dt> <dt>

[<span data-ttu-id="644d9-144">**WM \_ поверброадкаст**</span><span class="sxs-lookup"><span data-stu-id="644d9-144">**WM\_POWERBROADCAST**</span></span>](wm-powerbroadcast.md)
</dt> </dl>

 

 




