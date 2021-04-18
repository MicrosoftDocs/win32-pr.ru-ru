---
description: Уведомляет приложения о низком питании от аккумулятора.
ms.assetid: ef24b8cf-d801-4452-a03c-3f2bdbdd7e5d
title: Событие PBT_APMBATTERYLOW (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64884f9bb01e37883e1be61b2de88862e8b119fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673804"
---
# <a name="pbt_apmbatterylow-event"></a><span data-ttu-id="5d016-103">\_Событие ПБТ апмбаттерилов</span><span class="sxs-lookup"><span data-stu-id="5d016-103">PBT\_APMBATTERYLOW event</span></span>

<span data-ttu-id="5d016-104">\[ПБТ \_ апмбаттерилов доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="5d016-104">\[PBT\_APMBATTERYLOW is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="5d016-105">Поддержка этого события была удалена в Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="5d016-105">Support for this event was removed in Windows Vista.</span></span> <span data-ttu-id="5d016-106">Вместо этого используйте [ПБТ \_ апмповерстатусчанже](pbt-apmpowerstatuschange.md) .\]</span><span class="sxs-lookup"><span data-stu-id="5d016-106">Use [PBT\_APMPOWERSTATUSCHANGE](pbt-apmpowerstatuschange.md) instead.\]</span></span>

<span data-ttu-id="5d016-107">Уведомляет приложения о низком питании от аккумулятора.</span><span class="sxs-lookup"><span data-stu-id="5d016-107">Notifies applications that the battery power is low.</span></span>

<span data-ttu-id="5d016-108">Окно получает это событие через сообщение [**WM \_ поверброадкаст**](wm-powerbroadcast.md) .</span><span class="sxs-lookup"><span data-stu-id="5d016-108">A window receives this event through the [**WM\_POWERBROADCAST**](wm-powerbroadcast.md) message.</span></span> <span data-ttu-id="5d016-109">Параметры *wParam* и *lParam* задаются, как описано ниже.</span><span class="sxs-lookup"><span data-stu-id="5d016-109">The *wParam* and *lParam* parameters are set as described following.</span></span>


```C++
LRESULT 
CALLBACK 
WindowProc( HWND   hwnd,    // handle to window
            UINT   uMsg,    // WM_POWERBROADCAST
            WPARAM wParam,  // PBT_APMBATTERYLOW
            LPARAM lParam); // zero
```



## <a name="parameters"></a><span data-ttu-id="5d016-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="5d016-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d016-111">*HWND*</span><span class="sxs-lookup"><span data-stu-id="5d016-111">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="5d016-112">Маркер окна.</span><span class="sxs-lookup"><span data-stu-id="5d016-112">A handle to the window.</span></span>

<span data-ttu-id="5d016-113"></dd> <dt>*uiacp*</dt> </span><span class="sxs-lookup"><span data-stu-id="5d016-113"></dd> <dt>*uMsg* </dt> </span></span><dd> 

| <span data-ttu-id="5d016-114">Значение</span><span class="sxs-lookup"><span data-stu-id="5d016-114">Value</span></span>                                                                                                                                                                                                                                                                   | <span data-ttu-id="5d016-115">Значение</span><span class="sxs-lookup"><span data-stu-id="5d016-115">Meaning</span></span>                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span id="WM_POWERBROADCAST"></span><span id="wm_powerbroadcast"></span><dl> <span data-ttu-id="5d016-116"><dt>**[**WM \_ ПОВЕРБРОАДКАСТ**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span><span class="sxs-lookup"><span data-stu-id="5d016-116"><dt>**[**WM\_POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span></span> </dl> | <span data-ttu-id="5d016-117">Идентификатор сообщения.</span><span class="sxs-lookup"><span data-stu-id="5d016-117">Message identifier.</span></span><br/> |



 

<span data-ttu-id="5d016-118"></dd> <dt>*wParam*</dt> </span><span class="sxs-lookup"><span data-stu-id="5d016-118"></dd> <dt>*wParam* </dt> </span></span><dd> 

| <span data-ttu-id="5d016-119">Значение</span><span class="sxs-lookup"><span data-stu-id="5d016-119">Value</span></span>                                                                                                                                                                                                                                  | <span data-ttu-id="5d016-120">Значение</span><span class="sxs-lookup"><span data-stu-id="5d016-120">Meaning</span></span>                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="PBT_APMBATTERYLOW"></span><span id="pbt_apmbatterylow"></span><dl> <span data-ttu-id="5d016-121"><dt>**ПБТ \_ АПМБАТТЕРИЛОВ**</dt> <dt>9 (0x9)</dt></span><span class="sxs-lookup"><span data-stu-id="5d016-121"><dt>**PBT\_APMBATTERYLOW**</dt> <dt>9 (0x9)</dt></span></span> </dl> | <span data-ttu-id="5d016-122">Идентификатор события.</span><span class="sxs-lookup"><span data-stu-id="5d016-122">Event identifier.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="5d016-123">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5d016-123">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5d016-124">Зарезервировано, должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="5d016-124">Reserved, must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d016-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5d016-125">Return value</span></span>

<span data-ttu-id="5d016-126">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="5d016-126">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5d016-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5d016-127">Remarks</span></span>

<span data-ttu-id="5d016-128">Это событие является широковещательным, если BIOS системы APM сообщает о низком уведомлении аккумулятора APM.</span><span class="sxs-lookup"><span data-stu-id="5d016-128">This event is broadcast when a system's APM BIOS signals an APM battery low notification.</span></span> <span data-ttu-id="5d016-129">Поскольку некоторые реализации APM BIOS не предоставляют уведомления о низком уровне заряда, это событие может никогда не транслироваться на некоторые компьютеры.</span><span class="sxs-lookup"><span data-stu-id="5d016-129">Because some APM BIOS implementations do not provide notifications when batteries are low, this event may never be broadcast on some computers.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d016-130">Требования</span><span class="sxs-lookup"><span data-stu-id="5d016-130">Requirements</span></span>



| <span data-ttu-id="5d016-131">Требование</span><span class="sxs-lookup"><span data-stu-id="5d016-131">Requirement</span></span> | <span data-ttu-id="5d016-132">Значение</span><span class="sxs-lookup"><span data-stu-id="5d016-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5d016-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5d016-133">Minimum supported client</span></span><br/> | <span data-ttu-id="5d016-134">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="5d016-134">Windows XP \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="5d016-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5d016-135">Minimum supported server</span></span><br/> | <span data-ttu-id="5d016-136">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="5d016-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="5d016-137">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="5d016-137">End of client support</span></span><br/>    | <span data-ttu-id="5d016-138">Windows XP</span><span class="sxs-lookup"><span data-stu-id="5d016-138">Windows XP</span></span><br/>                                                                                    |
| <span data-ttu-id="5d016-139">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="5d016-139">End of server support</span></span><br/>    | <span data-ttu-id="5d016-140">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="5d016-140">Windows Server 2003</span></span><br/>                                                                           |
| <span data-ttu-id="5d016-141">Header</span><span class="sxs-lookup"><span data-stu-id="5d016-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="5d016-142"><dt>WinUser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5d016-142"><dt>WinUser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d016-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5d016-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d016-144">События управления питанием</span><span class="sxs-lookup"><span data-stu-id="5d016-144">Power Management Events</span></span>](power-management-events.md)
</dt> <dt>

[<span data-ttu-id="5d016-145">**WM \_ поверброадкаст**</span><span class="sxs-lookup"><span data-stu-id="5d016-145">**WM\_POWERBROADCAST**</span></span>](wm-powerbroadcast.md)
</dt> </dl>

 

 




