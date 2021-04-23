---
description: Уведомляет приложения о том, что BIOS APM сообщил о событии APM OEM.
ms.assetid: 3251ac00-41f1-44e9-a579-fa31e7c7d2ff
title: Событие PBT_APMOEMEVENT (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a99b99bdaf69b1a53a24ad33cd898fd1c806694
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105663113"
---
# <a name="pbt_apmoemevent-event"></a><span data-ttu-id="30861-103">\_Событие ПБТ апмоемевент</span><span class="sxs-lookup"><span data-stu-id="30861-103">PBT\_APMOEMEVENT event</span></span>

<span data-ttu-id="30861-104">\[ПБТ \_ апмоемевент доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="30861-104">\[PBT\_APMOEMEVENT is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="30861-105">Поддержка этого события была удалена в Windows Vista.\]</span><span class="sxs-lookup"><span data-stu-id="30861-105">Support for this event was removed in Windows Vista.\]</span></span>

<span data-ttu-id="30861-106">Уведомляет приложения о том, что BIOS APM сообщил о событии APM OEM.</span><span class="sxs-lookup"><span data-stu-id="30861-106">Notifies applications that the APM BIOS has signaled an APM OEM event.</span></span>

<span data-ttu-id="30861-107">Окно получает это событие через сообщение [**WM \_ поверброадкаст**](wm-powerbroadcast.md) .</span><span class="sxs-lookup"><span data-stu-id="30861-107">A window receives this event through the [**WM\_POWERBROADCAST**](wm-powerbroadcast.md) message.</span></span> <span data-ttu-id="30861-108">Параметры *wParam* и *lParam* задаются, как описано ниже.</span><span class="sxs-lookup"><span data-stu-id="30861-108">The *wParam* and *lParam* parameters are set as described following.</span></span>


```C++
LRESULT 
CALLBACK 
WindowProc( HWND   hwnd,    // handle to window
            UINT   uMsg,    // WM_POWERBROADCAST
            WPARAM wParam,  // PBT_APMOEMEVENT
            LPARAM lParam); // OEM event code
```



## <a name="parameters"></a><span data-ttu-id="30861-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="30861-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30861-110">*HWND*</span><span class="sxs-lookup"><span data-stu-id="30861-110">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="30861-111">Маркер для окна.</span><span class="sxs-lookup"><span data-stu-id="30861-111">A handle to window.</span></span>

<span data-ttu-id="30861-112"></dd> <dt>*uiacp*</dt> </span><span class="sxs-lookup"><span data-stu-id="30861-112"></dd> <dt>*uMsg* </dt> </span></span><dd> 

| <span data-ttu-id="30861-113">Значение</span><span class="sxs-lookup"><span data-stu-id="30861-113">Value</span></span>                                                                                                                                                                                                                                                                   | <span data-ttu-id="30861-114">Значение</span><span class="sxs-lookup"><span data-stu-id="30861-114">Meaning</span></span>                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span id="WM_POWERBROADCAST"></span><span id="wm_powerbroadcast"></span><dl> <span data-ttu-id="30861-115"><dt>**[**WM \_ ПОВЕРБРОАДКАСТ**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span><span class="sxs-lookup"><span data-stu-id="30861-115"><dt>**[**WM\_POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span></span> </dl> | <span data-ttu-id="30861-116">Идентификатор сообщения.</span><span class="sxs-lookup"><span data-stu-id="30861-116">Message identifier.</span></span><br/> |



 

<span data-ttu-id="30861-117"></dd> <dt>*wParam*</dt> </span><span class="sxs-lookup"><span data-stu-id="30861-117"></dd> <dt>*wParam* </dt> </span></span><dd> 

| <span data-ttu-id="30861-118">Значение</span><span class="sxs-lookup"><span data-stu-id="30861-118">Value</span></span>                                                                                                                                                                                                                             | <span data-ttu-id="30861-119">Значение</span><span class="sxs-lookup"><span data-stu-id="30861-119">Meaning</span></span>                      |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="PBT_APMOEMEVENT"></span><span id="pbt_apmoemevent"></span><dl> <span data-ttu-id="30861-120"><dt>**ПБТ \_ АПМОЕМЕВЕНТ**</dt> <dt>11 (0xB)</dt></span><span class="sxs-lookup"><span data-stu-id="30861-120"><dt>**PBT\_APMOEMEVENT**</dt> <dt>11 (0xB)</dt></span></span> </dl> | <span data-ttu-id="30861-121">Идентификатор события.</span><span class="sxs-lookup"><span data-stu-id="30861-121">Event identifier.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="30861-122">*lParam*</span><span class="sxs-lookup"><span data-stu-id="30861-122">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="30861-123">Код события, определяемый изготовителем оборудования и получивший сообщение BIOS системы APM.</span><span class="sxs-lookup"><span data-stu-id="30861-123">The OEM-defined event code that was signaled by the system's APM BIOS.</span></span> <span data-ttu-id="30861-124">Коды событий OEM находятся в диапазоне 0200h-02FFh.</span><span class="sxs-lookup"><span data-stu-id="30861-124">OEM event codes are in the range 0200h - 02FFh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30861-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="30861-125">Return value</span></span>

<span data-ttu-id="30861-126">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="30861-126">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="30861-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="30861-127">Remarks</span></span>

<span data-ttu-id="30861-128">Поскольку не все реализации APM BIOS предоставляют уведомления о событиях OEM, это событие может никогда не транслироваться на некоторые компьютеры.</span><span class="sxs-lookup"><span data-stu-id="30861-128">Because not all APM BIOS implementations provide OEM event notifications, this event may never be broadcast on some computers.</span></span>

## <a name="requirements"></a><span data-ttu-id="30861-129">Требования</span><span class="sxs-lookup"><span data-stu-id="30861-129">Requirements</span></span>



| <span data-ttu-id="30861-130">Требование</span><span class="sxs-lookup"><span data-stu-id="30861-130">Requirement</span></span> | <span data-ttu-id="30861-131">Значение</span><span class="sxs-lookup"><span data-stu-id="30861-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30861-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="30861-132">Minimum supported client</span></span><br/> | <span data-ttu-id="30861-133">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="30861-133">Windows XP \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="30861-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="30861-134">Minimum supported server</span></span><br/> | <span data-ttu-id="30861-135">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="30861-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="30861-136">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="30861-136">End of client support</span></span><br/>    | <span data-ttu-id="30861-137">Windows XP</span><span class="sxs-lookup"><span data-stu-id="30861-137">Windows XP</span></span><br/>                                                                                    |
| <span data-ttu-id="30861-138">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="30861-138">End of server support</span></span><br/>    | <span data-ttu-id="30861-139">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="30861-139">Windows Server 2003</span></span><br/>                                                                           |
| <span data-ttu-id="30861-140">Header</span><span class="sxs-lookup"><span data-stu-id="30861-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="30861-141"><dt>WinUser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="30861-141"><dt>WinUser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30861-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="30861-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30861-143">События управления питанием</span><span class="sxs-lookup"><span data-stu-id="30861-143">Power Management Events</span></span>](power-management-events.md)
</dt> <dt>

[<span data-ttu-id="30861-144">**WM \_ поверброадкаст**</span><span class="sxs-lookup"><span data-stu-id="30861-144">**WM\_POWERBROADCAST**</span></span>](wm-powerbroadcast.md)
</dt> </dl>

 

 




