---
description: Система передает \_ событие ДБТ девицекуериремовефаилед Device, когда запрос на удаление устройства или носителя был отменен.
ms.assetid: a24916a9-b67a-4622-b9f3-4b4f26bf4d6b
title: Событие DBT_DEVICEQUERYREMOVEFAILED (ДБТ. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 848c7378cdbac95729eee70c70a1e323373b8e85
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895878"
---
# <a name="dbt_devicequeryremovefailed-event"></a><span data-ttu-id="dc87a-103">\_Событие ДБТ девицекуериремовефаилед</span><span class="sxs-lookup"><span data-stu-id="dc87a-103">DBT\_DEVICEQUERYREMOVEFAILED event</span></span>

<span data-ttu-id="dc87a-104">Система передает \_ событие ДБТ девицекуериремовефаилед Device, когда запрос на удаление устройства или носителя был отменен.</span><span class="sxs-lookup"><span data-stu-id="dc87a-104">The system broadcasts the DBT\_DEVICEQUERYREMOVEFAILED device event when a request to remove a device or piece of media has been canceled.</span></span>

<span data-ttu-id="dc87a-105">Чтобы транслировать это событие устройства, система использует сообщение [**WM \_ девицечанже**](wm-devicechange.md) с параметром *wParam* Set ДБТ \_ девицекуериремовефаилед и *lParam* Set, как описано ниже.</span><span class="sxs-lookup"><span data-stu-id="dc87a-105">To broadcast this device event, the system uses the [**WM\_DEVICECHANGE**](wm-devicechange.md) message with *wParam* set to DBT\_DEVICEQUERYREMOVEFAILED and *lParam* set as described following.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd,       // handle to window
  UINT uMsg,       // WM_DEVICECHANGE
  WPARAM wParam,   // device-change event
  LPARAM lParam    // event-specific data
);
```



## <a name="parameters"></a><span data-ttu-id="dc87a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="dc87a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc87a-107">*HWND*</span><span class="sxs-lookup"><span data-stu-id="dc87a-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="dc87a-108">Дескриптор окна.</span><span class="sxs-lookup"><span data-stu-id="dc87a-108">A handle to a window.</span></span>

</dd> <dt>

<span data-ttu-id="dc87a-109">*Uiacp*</span><span class="sxs-lookup"><span data-stu-id="dc87a-109">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="dc87a-110">Идентификатор сообщения [**WM \_ девицечанже**](wm-devicechange.md) .</span><span class="sxs-lookup"><span data-stu-id="dc87a-110">The [**WM\_DEVICECHANGE**](wm-devicechange.md) message identifier.</span></span>

</dd> <dt>

<span data-ttu-id="dc87a-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="dc87a-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dc87a-112">Задайте для параметра значение ДБТ \_ девицекуериремовефаилед.</span><span class="sxs-lookup"><span data-stu-id="dc87a-112">Set to DBT\_DEVICEQUERYREMOVEFAILED.</span></span>

</dd> <dt>

<span data-ttu-id="dc87a-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="dc87a-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dc87a-114">Указатель на структуру, идентифицирующую устройство.</span><span class="sxs-lookup"><span data-stu-id="dc87a-114">A pointer to a structure identifying the device.</span></span> <span data-ttu-id="dc87a-115">Структура состоит из независимого от событий заголовка, за которым следуют элементы, зависящие от события, которые описывают устройство.</span><span class="sxs-lookup"><span data-stu-id="dc87a-115">The structure consists of an event-independent header, followed by event-dependent members that describe the device.</span></span> <span data-ttu-id="dc87a-116">Чтобы использовать эту структуру, рассматривайте структуру как [**\_ \_ HDR**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) -структуру для разработки вещания, а затем проверьте ее член **дбч \_ типа устройства** , чтобы определить тип устройства.</span><span class="sxs-lookup"><span data-stu-id="dc87a-116">To use this structure, treat the structure as a [**DEV\_BROADCAST\_HDR**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) structure, then check its **dbch\_devicetype** member to determine the device type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dc87a-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dc87a-117">Return value</span></span>

<span data-ttu-id="dc87a-118">Возвращает **значение true**.</span><span class="sxs-lookup"><span data-stu-id="dc87a-118">Return **TRUE**.</span></span>

## <a name="examples"></a><span data-ttu-id="dc87a-119">Примеры</span><span class="sxs-lookup"><span data-stu-id="dc87a-119">Examples</span></span>

<span data-ttu-id="dc87a-120">Пример см. в разделе [Обработка запроса на удаление устройства](processing-a-request-to-remove-a-device.md).</span><span class="sxs-lookup"><span data-stu-id="dc87a-120">For an example, see [Processing a Request to Remove a Device](processing-a-request-to-remove-a-device.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="dc87a-121">Требования</span><span class="sxs-lookup"><span data-stu-id="dc87a-121">Requirements</span></span>



| <span data-ttu-id="dc87a-122">Требование</span><span class="sxs-lookup"><span data-stu-id="dc87a-122">Requirement</span></span> | <span data-ttu-id="dc87a-123">Значение</span><span class="sxs-lookup"><span data-stu-id="dc87a-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="dc87a-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="dc87a-124">Minimum supported client</span></span><br/> | <span data-ttu-id="dc87a-125">Windows XP</span><span class="sxs-lookup"><span data-stu-id="dc87a-125">Windows XP</span></span><br/>                                                            |
| <span data-ttu-id="dc87a-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="dc87a-126">Minimum supported server</span></span><br/> | <span data-ttu-id="dc87a-127">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="dc87a-127">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="dc87a-128">Header</span><span class="sxs-lookup"><span data-stu-id="dc87a-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="dc87a-129"><dt>ДБТ. h</dt></span><span class="sxs-lookup"><span data-stu-id="dc87a-129"><dt>Dbt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc87a-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dc87a-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc87a-131">События устройства</span><span class="sxs-lookup"><span data-stu-id="dc87a-131">Device Events</span></span>](device-events.md)
</dt> <dt>

[<span data-ttu-id="dc87a-132">События управления устройствами</span><span class="sxs-lookup"><span data-stu-id="dc87a-132">Device Management Events</span></span>](device-management-events.md)
</dt> <dt>

[<span data-ttu-id="dc87a-133">**расвещание для разработки в \_ \_ HDR**</span><span class="sxs-lookup"><span data-stu-id="dc87a-133">**DEV\_BROADCAST\_HDR**</span></span>](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr)
</dt> <dt>

[<span data-ttu-id="dc87a-134">**WM \_ девицечанже**</span><span class="sxs-lookup"><span data-stu-id="dc87a-134">**WM\_DEVICECHANGE**</span></span>](wm-devicechange.md)
</dt> </dl>

 

 




