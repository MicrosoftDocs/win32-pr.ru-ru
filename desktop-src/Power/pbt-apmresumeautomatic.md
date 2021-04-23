---
description: Уведомляет приложения о том, что система возобновляет работу из спящего режима или гибернации. Это событие отправляется при каждом возобновлении системы и не указывает, имеется ли пользователь.
ms.assetid: cd331f79-b64d-479e-aea8-5118ccc87224
title: Событие PBT_APMRESUMEAUTOMATIC (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a7a481dee356c85b3831fcace0c1ff127b0b276
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909688"
---
# <a name="pbt_apmresumeautomatic-event"></a><span data-ttu-id="95ce7-104">\_Событие ПБТ апмресумеаутоматик</span><span class="sxs-lookup"><span data-stu-id="95ce7-104">PBT\_APMRESUMEAUTOMATIC event</span></span>

<span data-ttu-id="95ce7-105">Уведомляет приложения о том, что система возобновляет работу из спящего режима или гибернации.</span><span class="sxs-lookup"><span data-stu-id="95ce7-105">Notifies applications that the system is resuming from sleep or hibernation.</span></span> <span data-ttu-id="95ce7-106">Это событие отправляется при каждом возобновлении системы и не указывает, имеется ли пользователь.</span><span class="sxs-lookup"><span data-stu-id="95ce7-106">This event is delivered every time the system resumes and does not indicate whether a user is present.</span></span>

<span data-ttu-id="95ce7-107">Окно получает это событие через сообщение [**WM \_ поверброадкаст**](wm-powerbroadcast.md) .</span><span class="sxs-lookup"><span data-stu-id="95ce7-107">A window receives this event through the [**WM\_POWERBROADCAST**](wm-powerbroadcast.md) message.</span></span> <span data-ttu-id="95ce7-108">Параметры *wParam* и *lParam* задаются, как описано ниже.</span><span class="sxs-lookup"><span data-stu-id="95ce7-108">The *wParam* and *lParam* parameters are set as described following.</span></span>

> [!Note]  
> <span data-ttu-id="95ce7-109">В системах Windows 10 версии 1507 или более поздней, если система возобновляет работу из спящего режима для немедленного перехода в спящий режим, это событие не доставляется.</span><span class="sxs-lookup"><span data-stu-id="95ce7-109">In Windows 10, version 1507 systems or later, if the system is resuming from sleep only to immediately enter hibernation, this event is not delivered.</span></span> <span data-ttu-id="95ce7-110">В этом случае сообщение [**WM \_ поверброадкаст**](wm-powerbroadcast.md) не отправляется.</span><span class="sxs-lookup"><span data-stu-id="95ce7-110">A [**WM\_POWERBROADCAST**](wm-powerbroadcast.md) message is not sent in this case.</span></span>

 


```C++
LRESULT 
CALLBACK 
WindowProc( HWND hwnd,      // handle to window
            UINT uMsg,      // WM_POWERBROADCAST
            WPARAM wParam,  // PBT_APMRESUMEAUTOMATIC
            LPARAM lParam); // zero
```



## <a name="parameters"></a><span data-ttu-id="95ce7-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="95ce7-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95ce7-112">*HWND*</span><span class="sxs-lookup"><span data-stu-id="95ce7-112">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="95ce7-113">Маркер для окна.</span><span class="sxs-lookup"><span data-stu-id="95ce7-113">A handle to window.</span></span>

<span data-ttu-id="95ce7-114"></dd> <dt>*uiacp*</dt> </span><span class="sxs-lookup"><span data-stu-id="95ce7-114"></dd> <dt>*uMsg* </dt> </span></span><dd> 

| <span data-ttu-id="95ce7-115">Значение</span><span class="sxs-lookup"><span data-stu-id="95ce7-115">Value</span></span>                                                                                                                                                                                                                                                                   | <span data-ttu-id="95ce7-116">Значение</span><span class="sxs-lookup"><span data-stu-id="95ce7-116">Meaning</span></span>                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span id="WM_POWERBROADCAST"></span><span id="wm_powerbroadcast"></span><dl> <span data-ttu-id="95ce7-117"><dt>**[**WM \_ ПОВЕРБРОАДКАСТ**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span><span class="sxs-lookup"><span data-stu-id="95ce7-117"><dt>**[**WM\_POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span></span> </dl> | <span data-ttu-id="95ce7-118">Идентификатор сообщения.</span><span class="sxs-lookup"><span data-stu-id="95ce7-118">Message identifier.</span></span><br/> |



 

<span data-ttu-id="95ce7-119"></dd> <dt>*wParam*</dt> </span><span class="sxs-lookup"><span data-stu-id="95ce7-119"></dd> <dt>*wParam* </dt> </span></span><dd> 

| <span data-ttu-id="95ce7-120">Значение</span><span class="sxs-lookup"><span data-stu-id="95ce7-120">Value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="95ce7-121">Значение</span><span class="sxs-lookup"><span data-stu-id="95ce7-121">Meaning</span></span>                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="PBT_APMRESUMEAUTOMATIC"></span><span id="pbt_apmresumeautomatic"></span><dl> <span data-ttu-id="95ce7-122"><dt>**ПБТ \_ АПМРЕСУМЕАУТОМАТИК**</dt> <dt>18 (0x12)</dt></span><span class="sxs-lookup"><span data-stu-id="95ce7-122"><dt>**PBT\_APMRESUMEAUTOMATIC**</dt> <dt>18 (0x12)</dt></span></span> </dl> | <span data-ttu-id="95ce7-123">Идентификатор события.</span><span class="sxs-lookup"><span data-stu-id="95ce7-123">Event identifier.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="95ce7-124">*lParam*</span><span class="sxs-lookup"><span data-stu-id="95ce7-124">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="95ce7-125">Процессу должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="95ce7-125">Reserved; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95ce7-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="95ce7-126">Return value</span></span>

<span data-ttu-id="95ce7-127">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="95ce7-127">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="95ce7-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="95ce7-128">Remarks</span></span>

<span data-ttu-id="95ce7-129">Если система обнаруживает какие-либо действия пользователя после вещания ПБТ \_ апмресумеаутоматик, она пересылает событие [ПБТ \_ апмресумесуспенд](pbt-apmresumesuspend.md) , чтобы дать приложениям возможность возобновить полное взаимодействие с пользователем.</span><span class="sxs-lookup"><span data-stu-id="95ce7-129">If the system detects any user activity after broadcasting PBT\_APMRESUMEAUTOMATIC, it will broadcast a [PBT\_APMRESUMESUSPEND](pbt-apmresumesuspend.md) event to let applications know they can resume full interaction with the user.</span></span>

## <a name="requirements"></a><span data-ttu-id="95ce7-130">Требования</span><span class="sxs-lookup"><span data-stu-id="95ce7-130">Requirements</span></span>



| <span data-ttu-id="95ce7-131">Требование</span><span class="sxs-lookup"><span data-stu-id="95ce7-131">Requirement</span></span> | <span data-ttu-id="95ce7-132">Значение</span><span class="sxs-lookup"><span data-stu-id="95ce7-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="95ce7-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="95ce7-133">Minimum supported client</span></span><br/> | <span data-ttu-id="95ce7-134">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="95ce7-134">Windows XP \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="95ce7-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="95ce7-135">Minimum supported server</span></span><br/> | <span data-ttu-id="95ce7-136">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="95ce7-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="95ce7-137">Header</span><span class="sxs-lookup"><span data-stu-id="95ce7-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="95ce7-138"><dt>WinUser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="95ce7-138"><dt>WinUser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95ce7-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="95ce7-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95ce7-140">События пробуждения системы</span><span class="sxs-lookup"><span data-stu-id="95ce7-140">System Wake-up Events</span></span>](system-wake-up-events.md)
</dt> <dt>

[<span data-ttu-id="95ce7-141">События управления питанием</span><span class="sxs-lookup"><span data-stu-id="95ce7-141">Power Management Events</span></span>](power-management-events.md)
</dt> <dt>

[<span data-ttu-id="95ce7-142">ПБТ \_ апмресумесуспенд</span><span class="sxs-lookup"><span data-stu-id="95ce7-142">PBT\_APMRESUMESUSPEND</span></span>](pbt-apmresumesuspend.md)
</dt> <dt>

[<span data-ttu-id="95ce7-143">**WM \_ поверброадкаст**</span><span class="sxs-lookup"><span data-stu-id="95ce7-143">**WM\_POWERBROADCAST**</span></span>](wm-powerbroadcast.md)
</dt> </dl>

 

 




