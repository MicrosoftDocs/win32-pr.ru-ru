---
description: Система отправляет \_ событие устройства ДБТ CUSTOMEVENT при возникновении пользовательского события, определенного драйвером.
ms.assetid: 6e66fa93-0cd7-4202-83eb-cddc668525ae
title: Событие DBT_CUSTOMEVENT (ДБТ. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 777049a0a94b16450ed9ee8567f3fc6506e47174
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807421"
---
# <a name="dbt_customevent-event"></a><span data-ttu-id="5ebbf-103">\_Событие ДБТ CUSTOMEVENT</span><span class="sxs-lookup"><span data-stu-id="5ebbf-103">DBT\_CUSTOMEVENT event</span></span>

<span data-ttu-id="5ebbf-104">Система отправляет \_ событие устройства ДБТ CUSTOMEVENT при возникновении пользовательского события, определенного драйвером.</span><span class="sxs-lookup"><span data-stu-id="5ebbf-104">The system sends the DBT\_CUSTOMEVENT device event when a driver-defined custom event has occurred.</span></span>

<span data-ttu-id="5ebbf-105">Чтобы транслировать это событие устройства, система использует сообщение [**WM \_ девицечанже**](wm-devicechange.md) с параметром *wParam* Set ДБТ \_ CUSTOMEVENT и *lParam* Set, как описано ниже.</span><span class="sxs-lookup"><span data-stu-id="5ebbf-105">To broadcast this device event, the system uses the [**WM\_DEVICECHANGE**](wm-devicechange.md) message with *wParam* set to DBT\_CUSTOMEVENT and *lParam* set as described following.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd,       // handle to window
  UINT uMsg,       // WM_DEVICECHANGE
  WPARAM wParam,   // device-change event
  LPARAM lParam    // event-specific data
);
```



## <a name="parameters"></a><span data-ttu-id="5ebbf-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="5ebbf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ebbf-107">*HWND*</span><span class="sxs-lookup"><span data-stu-id="5ebbf-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="5ebbf-108">Дескриптор окна.</span><span class="sxs-lookup"><span data-stu-id="5ebbf-108">A handle to a window.</span></span>

</dd> <dt>

<span data-ttu-id="5ebbf-109">*Uiacp*</span><span class="sxs-lookup"><span data-stu-id="5ebbf-109">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="5ebbf-110">Идентификатор сообщения [**WM \_ девицечанже**](wm-devicechange.md) .</span><span class="sxs-lookup"><span data-stu-id="5ebbf-110">The [**WM\_DEVICECHANGE**](wm-devicechange.md) message identifier.</span></span>

</dd> <dt>

<span data-ttu-id="5ebbf-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5ebbf-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5ebbf-112">Задайте для параметра значение ДБТ \_ CUSTOMEVENT.</span><span class="sxs-lookup"><span data-stu-id="5ebbf-112">Set to DBT\_CUSTOMEVENT.</span></span>

</dd> <dt>

<span data-ttu-id="5ebbf-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5ebbf-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5ebbf-114">Указатель на структуру, идентифицирующую устройство.</span><span class="sxs-lookup"><span data-stu-id="5ebbf-114">A pointer to a structure identifying the device.</span></span> <span data-ttu-id="5ebbf-115">Структура состоит из независимого от событий заголовка, за которым следуют элементы, зависящие от события, которые описывают устройство.</span><span class="sxs-lookup"><span data-stu-id="5ebbf-115">The structure consists of an event-independent header, followed by event-dependent members that describe the device.</span></span> <span data-ttu-id="5ebbf-116">Чтобы использовать эту структуру, рассматривайте структуру как [**\_ \_ HDR**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) -структуру для разработки вещания, а затем проверьте ее член **дбч \_ типа устройства** , чтобы определить тип устройства.</span><span class="sxs-lookup"><span data-stu-id="5ebbf-116">To use this structure, treat the structure as a [**DEV\_BROADCAST\_HDR**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) structure, then check its **dbch\_devicetype** member to determine the device type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ebbf-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5ebbf-117">Return value</span></span>

<span data-ttu-id="5ebbf-118">Возвращает **значение true**.</span><span class="sxs-lookup"><span data-stu-id="5ebbf-118">Return **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="5ebbf-119">Требования</span><span class="sxs-lookup"><span data-stu-id="5ebbf-119">Requirements</span></span>



| <span data-ttu-id="5ebbf-120">Требование</span><span class="sxs-lookup"><span data-stu-id="5ebbf-120">Requirement</span></span> | <span data-ttu-id="5ebbf-121">Значение</span><span class="sxs-lookup"><span data-stu-id="5ebbf-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="5ebbf-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5ebbf-122">Minimum supported client</span></span><br/> | <span data-ttu-id="5ebbf-123">Windows XP</span><span class="sxs-lookup"><span data-stu-id="5ebbf-123">Windows XP</span></span><br/>                                                            |
| <span data-ttu-id="5ebbf-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5ebbf-124">Minimum supported server</span></span><br/> | <span data-ttu-id="5ebbf-125">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="5ebbf-125">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="5ebbf-126">Header</span><span class="sxs-lookup"><span data-stu-id="5ebbf-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="5ebbf-127"><dt>ДБТ. h</dt></span><span class="sxs-lookup"><span data-stu-id="5ebbf-127"><dt>Dbt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ebbf-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5ebbf-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ebbf-129">События устройства</span><span class="sxs-lookup"><span data-stu-id="5ebbf-129">Device Events</span></span>](device-events.md)
</dt> <dt>

[<span data-ttu-id="5ebbf-130">События управления устройствами</span><span class="sxs-lookup"><span data-stu-id="5ebbf-130">Device Management Events</span></span>](device-management-events.md)
</dt> <dt>

[<span data-ttu-id="5ebbf-131">**расвещание для разработки в \_ \_ HDR**</span><span class="sxs-lookup"><span data-stu-id="5ebbf-131">**DEV\_BROADCAST\_HDR**</span></span>](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr)
</dt> <dt>

[<span data-ttu-id="5ebbf-132">**WM \_ девицечанже**</span><span class="sxs-lookup"><span data-stu-id="5ebbf-132">**WM\_DEVICECHANGE**</span></span>](wm-devicechange.md)
</dt> </dl>

 

 




