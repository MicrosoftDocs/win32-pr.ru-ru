---
description: Событие изменения параметра питания, отправленное с помощью \_ сообщения окна WM поверброадкаст или обратного вызова уведомления хандлерекс для служб.
ms.assetid: 0bcadb85-47c5-48a9-b3f9-f0a1ca60b503
title: Событие PBT_POWERSETTINGCHANGE (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0f38486d2e5cce1cfe541468e548e92353c9837
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909687"
---
# <a name="pbt_powersettingchange-event"></a><span data-ttu-id="789f2-103">\_Событие ПБТ поверсеттингчанже</span><span class="sxs-lookup"><span data-stu-id="789f2-103">PBT\_POWERSETTINGCHANGE event</span></span>

<span data-ttu-id="789f2-104">Событие изменения параметра питания, отправленное с помощью сообщения окна [**WM \_ поверброадкаст**](wm-powerbroadcast.md) или обратного вызова уведомления [**хандлерекс**](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex) для служб.</span><span class="sxs-lookup"><span data-stu-id="789f2-104">Power setting change event sent with a [**WM\_POWERBROADCAST**](wm-powerbroadcast.md) window message or in a [**HandlerEx**](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex) notification callback for services.</span></span>


```C++
LRESULT 
CALLBACK 
WindowProc( HWND hwnd,      // handle to window
            UINT uMsg,      // WM_POWERBROADCAST
            WPARAM wParam,  // PBT_POWERSETTINGCHANGE
            LPARAM lParam); // Pointer to POWERBROADCAST_SETTING
```



## <a name="parameters"></a><span data-ttu-id="789f2-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="789f2-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="789f2-106">*HWND*</span><span class="sxs-lookup"><span data-stu-id="789f2-106">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="789f2-107">Маркер для окна.</span><span class="sxs-lookup"><span data-stu-id="789f2-107">A handle to window.</span></span>

<span data-ttu-id="789f2-108"></dd> <dt>*uiacp*</dt> </span><span class="sxs-lookup"><span data-stu-id="789f2-108"></dd> <dt>*uMsg* </dt> </span></span><dd> 

| <span data-ttu-id="789f2-109">Значение</span><span class="sxs-lookup"><span data-stu-id="789f2-109">Value</span></span>                                                                                                                                                                                                                                                                   | <span data-ttu-id="789f2-110">Значение</span><span class="sxs-lookup"><span data-stu-id="789f2-110">Meaning</span></span>                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span id="WM_POWERBROADCAST"></span><span id="wm_powerbroadcast"></span><dl> <span data-ttu-id="789f2-111"><dt>**[**WM \_ ПОВЕРБРОАДКАСТ**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span><span class="sxs-lookup"><span data-stu-id="789f2-111"><dt>**[**WM\_POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span></span> </dl> | <span data-ttu-id="789f2-112">Идентификатор сообщения.</span><span class="sxs-lookup"><span data-stu-id="789f2-112">Message identifier.</span></span><br/> |



 

<span data-ttu-id="789f2-113"></dd> <dt>*wParam*</dt> </span><span class="sxs-lookup"><span data-stu-id="789f2-113"></dd> <dt>*wParam* </dt> </span></span><dd> 

| <span data-ttu-id="789f2-114">Значение</span><span class="sxs-lookup"><span data-stu-id="789f2-114">Value</span></span>                                                                                                                                                                                                                                                        | <span data-ttu-id="789f2-115">Значение</span><span class="sxs-lookup"><span data-stu-id="789f2-115">Meaning</span></span>                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="PBT_POWERSETTINGCHANGE"></span><span id="pbt_powersettingchange"></span><dl> <span data-ttu-id="789f2-116"><dt>**ПБТ \_ ПОВЕРСЕТТИНГЧАНЖЕ**</dt> <dt>32787 (0x8013)</dt></span><span class="sxs-lookup"><span data-stu-id="789f2-116"><dt>**PBT\_POWERSETTINGCHANGE**</dt> <dt>32787 (0x8013)</dt></span></span> </dl> | <span data-ttu-id="789f2-117">Идентификатор события.</span><span class="sxs-lookup"><span data-stu-id="789f2-117">Event identifier.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="789f2-118">*lParam*</span><span class="sxs-lookup"><span data-stu-id="789f2-118">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="789f2-119">Указатель на структуру [**\_ параметра поверброадкаст**](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting) .</span><span class="sxs-lookup"><span data-stu-id="789f2-119">Pointer to a [**POWERBROADCAST\_SETTING**](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="789f2-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="789f2-120">Return value</span></span>

<span data-ttu-id="789f2-121">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="789f2-121">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="789f2-122">Требования</span><span class="sxs-lookup"><span data-stu-id="789f2-122">Requirements</span></span>



| <span data-ttu-id="789f2-123">Требование</span><span class="sxs-lookup"><span data-stu-id="789f2-123">Requirement</span></span> | <span data-ttu-id="789f2-124">Значение</span><span class="sxs-lookup"><span data-stu-id="789f2-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="789f2-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="789f2-125">Minimum supported client</span></span><br/> | <span data-ttu-id="789f2-126">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="789f2-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="789f2-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="789f2-127">Minimum supported server</span></span><br/> | <span data-ttu-id="789f2-128">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="789f2-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="789f2-129">Header</span><span class="sxs-lookup"><span data-stu-id="789f2-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="789f2-130"><dt>WinUser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="789f2-130"><dt>WinUser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="789f2-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="789f2-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="789f2-132">События управления питанием</span><span class="sxs-lookup"><span data-stu-id="789f2-132">Power Management Events</span></span>](power-management-events.md)
</dt> <dt>

[<span data-ttu-id="789f2-133">**хандлерекс**</span><span class="sxs-lookup"><span data-stu-id="789f2-133">**HandlerEx**</span></span>](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex)
</dt> <dt>

[<span data-ttu-id="789f2-134">**WM \_ поверброадкаст**</span><span class="sxs-lookup"><span data-stu-id="789f2-134">**WM\_POWERBROADCAST**</span></span>](wm-powerbroadcast.md)
</dt> <dt>

[<span data-ttu-id="789f2-135">**\_параметр поверброадкаст**</span><span class="sxs-lookup"><span data-stu-id="789f2-135">**POWERBROADCAST\_SETTING**</span></span>](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting)
</dt> </dl>

 

