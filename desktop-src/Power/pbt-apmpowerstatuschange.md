---
description: Уведомляет приложения об изменении состояния питания компьютера, например о переключении питания от аккумулятора к A/C.
ms.assetid: dc56fee3-e0df-4f8e-8a41-92460279280a
title: Событие PBT_APMPOWERSTATUSCHANGE (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18ed67f7ba064d44614196da4190ce18a996bd5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104264505"
---
# <a name="pbt_apmpowerstatuschange-event"></a><span data-ttu-id="94500-103">\_Событие ПБТ апмповерстатусчанже</span><span class="sxs-lookup"><span data-stu-id="94500-103">PBT\_APMPOWERSTATUSCHANGE event</span></span>

<span data-ttu-id="94500-104">Уведомляет приложения об изменении состояния питания компьютера, например о переключении питания от аккумулятора к A/C.</span><span class="sxs-lookup"><span data-stu-id="94500-104">Notifies applications of a change in the power status of the computer, such as a switch from battery power to A/C.</span></span> <span data-ttu-id="94500-105">Это событие возникает также, если уровень заряда батареи становится ниже заданного пользователем порога или изменяется на заданную величину в процентах.</span><span class="sxs-lookup"><span data-stu-id="94500-105">The system also broadcasts this event when remaining battery power slips below the threshold specified by the user or if the battery power changes by a specified percentage.</span></span>

<span data-ttu-id="94500-106">Окно получает это событие через сообщение [**WM \_ поверброадкаст**](wm-powerbroadcast.md) .</span><span class="sxs-lookup"><span data-stu-id="94500-106">A window receives this event through the [**WM\_POWERBROADCAST**](wm-powerbroadcast.md) message.</span></span> <span data-ttu-id="94500-107">Параметры *wParam* и *lParam* задаются, как описано ниже.</span><span class="sxs-lookup"><span data-stu-id="94500-107">The *wParam* and *lParam* parameters are set as described following.</span></span>


```C++
LRESULT 
CALLBACK 
WindowProc( HWND hwnd,      // handle to window
            UINT uMsg,      // WM_POWERBROADCAST
            WPARAM wParam,  // PBT_APMPOWERSTATUSCHANGE
            LPARAM lParam); // zero
```



## <a name="parameters"></a><span data-ttu-id="94500-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="94500-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="94500-109">*HWND*</span><span class="sxs-lookup"><span data-stu-id="94500-109">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="94500-110">Маркер для окна.</span><span class="sxs-lookup"><span data-stu-id="94500-110">A handle to window.</span></span>

<span data-ttu-id="94500-111"></dd> <dt>*uiacp*</dt> </span><span class="sxs-lookup"><span data-stu-id="94500-111"></dd> <dt>*uMsg* </dt> </span></span><dd> 

| <span data-ttu-id="94500-112">Значение</span><span class="sxs-lookup"><span data-stu-id="94500-112">Value</span></span>                                                                                                                                                                                                                                                                   | <span data-ttu-id="94500-113">Значение</span><span class="sxs-lookup"><span data-stu-id="94500-113">Meaning</span></span>                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span id="WM_POWERBROADCAST"></span><span id="wm_powerbroadcast"></span><dl> <span data-ttu-id="94500-114"><dt>**[**WM \_ ПОВЕРБРОАДКАСТ**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span><span class="sxs-lookup"><span data-stu-id="94500-114"><dt>**[**WM\_POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span></span> </dl> | <span data-ttu-id="94500-115">Идентификатор сообщения.</span><span class="sxs-lookup"><span data-stu-id="94500-115">Message identifier.</span></span><br/> |



 

<span data-ttu-id="94500-116"></dd> <dt>*wParam*</dt> </span><span class="sxs-lookup"><span data-stu-id="94500-116"></dd> <dt>*wParam* </dt> </span></span><dd> 

| <span data-ttu-id="94500-117">Значение</span><span class="sxs-lookup"><span data-stu-id="94500-117">Value</span></span>                                                                                                                                                                                                                                                        | <span data-ttu-id="94500-118">Значение</span><span class="sxs-lookup"><span data-stu-id="94500-118">Meaning</span></span>                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="PBT_APMPOWERSTATUSCHANGE"></span><span id="pbt_apmpowerstatuschange"></span><dl> <span data-ttu-id="94500-119"><dt>**ПБТ \_ АПМПОВЕРСТАТУСЧАНЖЕ**</dt> <dt>10 (0xA)</dt></span><span class="sxs-lookup"><span data-stu-id="94500-119"><dt>**PBT\_APMPOWERSTATUSCHANGE**</dt> <dt>10 (0xA)</dt></span></span> </dl> | <span data-ttu-id="94500-120">Идентификатор события.</span><span class="sxs-lookup"><span data-stu-id="94500-120">Event identifier.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="94500-121">*lParam*</span><span class="sxs-lookup"><span data-stu-id="94500-121">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="94500-122">Процессу должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="94500-122">Reserved; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="94500-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="94500-123">Return value</span></span>

<span data-ttu-id="94500-124">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="94500-124">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="94500-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="94500-125">Remarks</span></span>

<span data-ttu-id="94500-126">Приложение должно обработать это событие, вызвав функцию [**GetSystemPowerStatus**](/windows/desktop/api/Winbase/nf-winbase-getsystempowerstatus) для получения текущего состояния питания компьютера.</span><span class="sxs-lookup"><span data-stu-id="94500-126">An application should process this event by calling the [**GetSystemPowerStatus**](/windows/desktop/api/Winbase/nf-winbase-getsystempowerstatus) function to retrieve the current power status of the computer.</span></span> <span data-ttu-id="94500-127">В частности, приложение должно проверять члены **аклинестатус**, **баттерифлаг**, **Баттерилифетиме** и **баттерилифеперцент** структуры [**Power System \_ \_ Status**](/windows/desktop/api/Winbase/ns-winbase-system_power_status) для любых изменений.</span><span class="sxs-lookup"><span data-stu-id="94500-127">In particular, the application should check the **ACLineStatus**, **BatteryFlag**, **BatteryLifeTime**, and **BatteryLifePercent** members of the [**SYSTEM\_POWER\_STATUS**](/windows/desktop/api/Winbase/ns-winbase-system_power_status) structure for any changes.</span></span> <span data-ttu-id="94500-128">Это событие может возникать, когда время работы аккумулятора падает менее чем за 5 минут или когда процент времени работы батареи падает ниже 10% или если время работы батареи изменяется на 3 процента.</span><span class="sxs-lookup"><span data-stu-id="94500-128">This event can occur when battery life drops to less than 5 minutes, or when the percentage of battery life drops below 10 percent, or if the battery life changes by 3 percent.</span></span>

## <a name="requirements"></a><span data-ttu-id="94500-129">Требования</span><span class="sxs-lookup"><span data-stu-id="94500-129">Requirements</span></span>



| <span data-ttu-id="94500-130">Требование</span><span class="sxs-lookup"><span data-stu-id="94500-130">Requirement</span></span> | <span data-ttu-id="94500-131">Значение</span><span class="sxs-lookup"><span data-stu-id="94500-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="94500-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="94500-132">Minimum supported client</span></span><br/> | <span data-ttu-id="94500-133">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="94500-133">Windows XP \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="94500-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="94500-134">Minimum supported server</span></span><br/> | <span data-ttu-id="94500-135">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="94500-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="94500-136">Header</span><span class="sxs-lookup"><span data-stu-id="94500-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="94500-137"><dt>WinUser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="94500-137"><dt>WinUser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94500-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="94500-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94500-139">Состояние питания системы</span><span class="sxs-lookup"><span data-stu-id="94500-139">System Power Status</span></span>](system-power-status.md)
</dt> <dt>

[<span data-ttu-id="94500-140">События управления питанием</span><span class="sxs-lookup"><span data-stu-id="94500-140">Power Management Events</span></span>](power-management-events.md)
</dt> <dt>

[<span data-ttu-id="94500-141">**GetSystemPowerStatus**</span><span class="sxs-lookup"><span data-stu-id="94500-141">**GetSystemPowerStatus**</span></span>](/windows/desktop/api/Winbase/nf-winbase-getsystempowerstatus)
</dt> <dt>

[<span data-ttu-id="94500-142">**\_состояние питания \_ системы**</span><span class="sxs-lookup"><span data-stu-id="94500-142">**SYSTEM\_POWER\_STATUS**</span></span>](/windows/desktop/api/Winbase/ns-winbase-system_power_status)
</dt> <dt>

[<span data-ttu-id="94500-143">**WM \_ поверброадкаст**</span><span class="sxs-lookup"><span data-stu-id="94500-143">**WM\_POWERBROADCAST**</span></span>](wm-powerbroadcast.md)
</dt> </dl>

 

 




