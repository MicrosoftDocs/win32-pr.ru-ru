---
description: Система передает \_ событие ДБТ девнодес \_ Changed Device, когда устройство было добавлено или удалено из системы. Приложения, поддерживающие списки устройств в системе, должны обновлять свои списки.
ms.assetid: 62acc633-7dad-4792-a5a2-1f95356479d1
title: Событие DBT_DEVNODES_CHANGED (ДБТ. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1450e9a87d541e5df3d9a9286e48601697e6aaae
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141511"
---
# <a name="dbt_devnodes_changed-event"></a><span data-ttu-id="c5a70-104">\_ \_ Событие изменения ДБТ девнодес</span><span class="sxs-lookup"><span data-stu-id="c5a70-104">DBT\_DEVNODES\_CHANGED event</span></span>

<span data-ttu-id="c5a70-105">Система передает \_ событие ДБТ девнодес \_ Changed Device, когда устройство было добавлено или удалено из системы.</span><span class="sxs-lookup"><span data-stu-id="c5a70-105">The system broadcasts the DBT\_DEVNODES\_CHANGED device event when a device has been added to or removed from the system.</span></span> <span data-ttu-id="c5a70-106">Приложения, поддерживающие списки устройств в системе, должны обновлять свои списки.</span><span class="sxs-lookup"><span data-stu-id="c5a70-106">Applications that maintain lists of devices in the system should refresh their lists.</span></span>

<span data-ttu-id="c5a70-107">Чтобы транслировать это событие устройства, система использует сообщение [**WM \_ девицечанже**](wm-devicechange.md) с параметром *wParam* , установленным в ДБТ \_ Девнодес \_ Changed, и параметр *lParam* имеет значение 0.</span><span class="sxs-lookup"><span data-stu-id="c5a70-107">To broadcast this device event, the system uses the [**WM\_DEVICECHANGE**](wm-devicechange.md) message with *wParam* set to DBT\_DEVNODES\_CHANGED and *lParam* set to zero.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd,       // handle to window
  UINT uMsg,       // WM_DEVICECHANGE
  WPARAM wParam,   // device-change event
  LPARAM lParam    // event-specific data
);
```



## <a name="parameters"></a><span data-ttu-id="c5a70-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="c5a70-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5a70-109">*HWND*</span><span class="sxs-lookup"><span data-stu-id="c5a70-109">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="c5a70-110">Дескриптор окна.</span><span class="sxs-lookup"><span data-stu-id="c5a70-110">A handle to a window.</span></span>

</dd> <dt>

<span data-ttu-id="c5a70-111">*Uiacp*</span><span class="sxs-lookup"><span data-stu-id="c5a70-111">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="c5a70-112">Идентификатор сообщения [**WM \_ девицечанже**](wm-devicechange.md) .</span><span class="sxs-lookup"><span data-stu-id="c5a70-112">The [**WM\_DEVICECHANGE**](wm-devicechange.md) message identifier.</span></span>

</dd> <dt>

<span data-ttu-id="c5a70-113">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c5a70-113">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c5a70-114">Задайте значение ДБТ \_ девнодес \_ изменено.</span><span class="sxs-lookup"><span data-stu-id="c5a70-114">Set to DBT\_DEVNODES\_CHANGED.</span></span>

</dd> <dt>

<span data-ttu-id="c5a70-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c5a70-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c5a70-116">Задайте нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="c5a70-116">Set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5a70-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c5a70-117">Return value</span></span>

<span data-ttu-id="c5a70-118">Возвращает **значение true**.</span><span class="sxs-lookup"><span data-stu-id="c5a70-118">Return **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="c5a70-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c5a70-119">Remarks</span></span>

<span data-ttu-id="c5a70-120">Дополнительные сведения о том, какое устройство было добавлено или удалено из системы, не существует.</span><span class="sxs-lookup"><span data-stu-id="c5a70-120">There is no additional information about which device has been added to or removed from the system.</span></span> <span data-ttu-id="c5a70-121">Приложения, для которых требуется дополнительная информация, должны регистрироваться для уведомления устройства с помощью функции [**регистердевиценотификатион**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa) .</span><span class="sxs-lookup"><span data-stu-id="c5a70-121">Applications that require more information should register for device notification using the [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5a70-122">Требования</span><span class="sxs-lookup"><span data-stu-id="c5a70-122">Requirements</span></span>



| <span data-ttu-id="c5a70-123">Требование</span><span class="sxs-lookup"><span data-stu-id="c5a70-123">Requirement</span></span> | <span data-ttu-id="c5a70-124">Значение</span><span class="sxs-lookup"><span data-stu-id="c5a70-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="c5a70-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c5a70-125">Minimum supported client</span></span><br/> | <span data-ttu-id="c5a70-126">Windows XP</span><span class="sxs-lookup"><span data-stu-id="c5a70-126">Windows XP</span></span><br/>                                                            |
| <span data-ttu-id="c5a70-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c5a70-127">Minimum supported server</span></span><br/> | <span data-ttu-id="c5a70-128">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c5a70-128">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="c5a70-129">Header</span><span class="sxs-lookup"><span data-stu-id="c5a70-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="c5a70-130"><dt>ДБТ. h</dt></span><span class="sxs-lookup"><span data-stu-id="c5a70-130"><dt>Dbt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5a70-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c5a70-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5a70-132">События устройства</span><span class="sxs-lookup"><span data-stu-id="c5a70-132">Device Events</span></span>](device-events.md)
</dt> <dt>

[<span data-ttu-id="c5a70-133">События управления устройствами</span><span class="sxs-lookup"><span data-stu-id="c5a70-133">Device Management Events</span></span>](device-management-events.md)
</dt> <dt>

[<span data-ttu-id="c5a70-134">**расвещание для разработки в \_ \_ HDR**</span><span class="sxs-lookup"><span data-stu-id="c5a70-134">**DEV\_BROADCAST\_HDR**</span></span>](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr)
</dt> <dt>

[<span data-ttu-id="c5a70-135">**WM \_ девицечанже**</span><span class="sxs-lookup"><span data-stu-id="c5a70-135">**WM\_DEVICECHANGE**</span></span>](wm-devicechange.md)
</dt> </dl>

 

 




