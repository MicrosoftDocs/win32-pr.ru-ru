---
description: Система передает \_ событие ДБТ девицеремовепендинг Device, когда устройство или носитель удаляется и больше не доступны для использования.
ms.assetid: 28cb4481-8961-4896-9608-afccba9a2bfe
title: Событие DBT_DEVICEREMOVEPENDING (ДБТ. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 421851dc46d905ae85941b92df6649ccb504ee50
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141514"
---
# <a name="dbt_deviceremovepending-event"></a><span data-ttu-id="6f415-103">\_Событие ДБТ девицеремовепендинг</span><span class="sxs-lookup"><span data-stu-id="6f415-103">DBT\_DEVICEREMOVEPENDING event</span></span>

<span data-ttu-id="6f415-104">Система передает \_ событие ДБТ девицеремовепендинг Device, когда устройство или носитель удаляется и больше не доступны для использования.</span><span class="sxs-lookup"><span data-stu-id="6f415-104">The system broadcasts the DBT\_DEVICEREMOVEPENDING device event when a device or piece of media is being removed and is no longer available for use.</span></span>

<span data-ttu-id="6f415-105">Чтобы транслировать это событие устройства, система использует сообщение [**WM \_ девицечанже**](wm-devicechange.md) с параметром *wParam* Set ДБТ \_ девицеремовепендинг и *lParam* Set, как описано ниже.</span><span class="sxs-lookup"><span data-stu-id="6f415-105">To broadcast this device event, the system uses the [**WM\_DEVICECHANGE**](wm-devicechange.md) message with *wParam* set to DBT\_DEVICEREMOVEPENDING and *lParam* set as described following.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd,       // handle to window
  UINT uMsg,       // WM_DEVICECHANGE
  WPARAM wParam,   // device-change event
  LPARAM lParam    // event-specific data
);
```



## <a name="parameters"></a><span data-ttu-id="6f415-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6f415-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f415-107">*HWND*</span><span class="sxs-lookup"><span data-stu-id="6f415-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="6f415-108">Дескриптор окна.</span><span class="sxs-lookup"><span data-stu-id="6f415-108">A handle to a window.</span></span>

</dd> <dt>

<span data-ttu-id="6f415-109">*Uiacp*</span><span class="sxs-lookup"><span data-stu-id="6f415-109">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="6f415-110">Идентификатор сообщения [**WM \_ девицечанже**](wm-devicechange.md) .</span><span class="sxs-lookup"><span data-stu-id="6f415-110">The [**WM\_DEVICECHANGE**](wm-devicechange.md) message identifier.</span></span>

</dd> <dt>

<span data-ttu-id="6f415-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6f415-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6f415-112">Задайте для параметра значение ДБТ \_ девицеремовепендинг.</span><span class="sxs-lookup"><span data-stu-id="6f415-112">Set to DBT\_DEVICEREMOVEPENDING.</span></span>

</dd> <dt>

<span data-ttu-id="6f415-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6f415-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6f415-114">Указатель на структуру, идентифицирующую устройство.</span><span class="sxs-lookup"><span data-stu-id="6f415-114">A pointer to a structure identifying the device.</span></span> <span data-ttu-id="6f415-115">Структура состоит из независимого от событий заголовка, за которым следуют элементы, зависящие от события, которые описывают устройство.</span><span class="sxs-lookup"><span data-stu-id="6f415-115">The structure consists of an event-independent header, followed by event-dependent members that describe the device.</span></span> <span data-ttu-id="6f415-116">Чтобы использовать эту структуру, рассматривайте структуру как [**\_ \_ HDR**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) -структуру для разработки вещания, а затем проверьте ее член **дбч \_ типа устройства** , чтобы определить тип устройства.</span><span class="sxs-lookup"><span data-stu-id="6f415-116">To use this structure, treat the structure as a [**DEV\_BROADCAST\_HDR**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) structure, then check its **dbch\_devicetype** member to determine the device type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6f415-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6f415-117">Return value</span></span>

<span data-ttu-id="6f415-118">Возвращает **значение true**.</span><span class="sxs-lookup"><span data-stu-id="6f415-118">Return **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="6f415-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6f415-119">Remarks</span></span>

<span data-ttu-id="6f415-120">Система может транслировать \_ сообщение ДБТ девицеремовепендинг, не отправляя соответствующее сообщение [ДБТ \_ девицекуериремове](dbt-devicequeryremove.md) .</span><span class="sxs-lookup"><span data-stu-id="6f415-120">The system may broadcast a DBT\_DEVICEREMOVEPENDING message without sending a corresponding [DBT\_DEVICEQUERYREMOVE](dbt-devicequeryremove.md) message.</span></span> <span data-ttu-id="6f415-121">В таких случаях приложения и драйверы должны быть восстановлены после потери устройства, как лучше.</span><span class="sxs-lookup"><span data-stu-id="6f415-121">In such cases, the applications and drivers must recover from the loss of the device as best they can.</span></span>

## <a name="examples"></a><span data-ttu-id="6f415-122">Примеры</span><span class="sxs-lookup"><span data-stu-id="6f415-122">Examples</span></span>

<span data-ttu-id="6f415-123">Пример см. в разделе [Обработка запроса на удаление устройства](processing-a-request-to-remove-a-device.md).</span><span class="sxs-lookup"><span data-stu-id="6f415-123">For an example, see [Processing a Request to Remove a Device](processing-a-request-to-remove-a-device.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6f415-124">Требования</span><span class="sxs-lookup"><span data-stu-id="6f415-124">Requirements</span></span>



| <span data-ttu-id="6f415-125">Требование</span><span class="sxs-lookup"><span data-stu-id="6f415-125">Requirement</span></span> | <span data-ttu-id="6f415-126">Значение</span><span class="sxs-lookup"><span data-stu-id="6f415-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="6f415-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6f415-127">Minimum supported client</span></span><br/> | <span data-ttu-id="6f415-128">Windows XP</span><span class="sxs-lookup"><span data-stu-id="6f415-128">Windows XP</span></span><br/>                                                            |
| <span data-ttu-id="6f415-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6f415-129">Minimum supported server</span></span><br/> | <span data-ttu-id="6f415-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6f415-130">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="6f415-131">Header</span><span class="sxs-lookup"><span data-stu-id="6f415-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="6f415-132"><dt>ДБТ. h</dt></span><span class="sxs-lookup"><span data-stu-id="6f415-132"><dt>Dbt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6f415-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6f415-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f415-134">События устройства</span><span class="sxs-lookup"><span data-stu-id="6f415-134">Device Events</span></span>](device-events.md)
</dt> <dt>

[<span data-ttu-id="6f415-135">События управления устройствами</span><span class="sxs-lookup"><span data-stu-id="6f415-135">Device Management Events</span></span>](device-management-events.md)
</dt> <dt>

[<span data-ttu-id="6f415-136">**расвещание для разработки в \_ \_ HDR**</span><span class="sxs-lookup"><span data-stu-id="6f415-136">**DEV\_BROADCAST\_HDR**</span></span>](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr)
</dt> <dt>

[<span data-ttu-id="6f415-137">**WM \_ девицечанже**</span><span class="sxs-lookup"><span data-stu-id="6f415-137">**WM\_DEVICECHANGE**</span></span>](wm-devicechange.md)
</dt> </dl>

 

 




