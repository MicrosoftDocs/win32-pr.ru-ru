---
description: Система передает \_ событие ДБТ девицекуериремове Device, чтобы запросить разрешение на удаление устройства или носителя.
ms.assetid: a0e9aa57-da0e-4e9c-99d0-5502040d2664
title: Событие DBT_DEVICEQUERYREMOVE (ДБТ. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b8c9dbdee13318f9a664582fdba8f9e3f9bfc5f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655858"
---
# <a name="dbt_devicequeryremove-event"></a><span data-ttu-id="a415b-103">\_Событие ДБТ девицекуериремове</span><span class="sxs-lookup"><span data-stu-id="a415b-103">DBT\_DEVICEQUERYREMOVE event</span></span>

<span data-ttu-id="a415b-104">Система передает \_ событие ДБТ девицекуериремове Device, чтобы запросить разрешение на удаление устройства или носителя.</span><span class="sxs-lookup"><span data-stu-id="a415b-104">The system broadcasts the DBT\_DEVICEQUERYREMOVE device event to request permission to remove a device or piece of media.</span></span> <span data-ttu-id="a415b-105">Это сообщение является последней возможностью для подготовки приложений и драйверов к удалению.</span><span class="sxs-lookup"><span data-stu-id="a415b-105">This message is the last chance for applications and drivers to prepare for this removal.</span></span> <span data-ttu-id="a415b-106">Однако любое приложение может отклонить этот запрос и отменить операцию.</span><span class="sxs-lookup"><span data-stu-id="a415b-106">However, any application can deny this request and cancel the operation.</span></span>

<span data-ttu-id="a415b-107">Чтобы транслировать это событие устройства, система использует сообщение [**WM \_ девицечанже**](wm-devicechange.md) с параметром *wParam* Set ДБТ \_ девицекуериремове и *lParam* Set, как описано ниже.</span><span class="sxs-lookup"><span data-stu-id="a415b-107">To broadcast this device event, the system uses the [**WM\_DEVICECHANGE**](wm-devicechange.md) message with *wParam* set to DBT\_DEVICEQUERYREMOVE and *lParam* set as described following.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd,       // handle to window
  UINT uMsg,       // WM_DEVICECHANGE
  WPARAM wParam,   // device-change event
  LPARAM lParam    // event-specific data
);
```



## <a name="parameters"></a><span data-ttu-id="a415b-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="a415b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a415b-109">*HWND*</span><span class="sxs-lookup"><span data-stu-id="a415b-109">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="a415b-110">Дескриптор окна.</span><span class="sxs-lookup"><span data-stu-id="a415b-110">A handle to a window.</span></span>

</dd> <dt>

<span data-ttu-id="a415b-111">*Uiacp*</span><span class="sxs-lookup"><span data-stu-id="a415b-111">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="a415b-112">Идентификатор сообщения [**WM \_ девицечанже**](wm-devicechange.md) .</span><span class="sxs-lookup"><span data-stu-id="a415b-112">The [**WM\_DEVICECHANGE**](wm-devicechange.md) message identifier.</span></span>

</dd> <dt>

<span data-ttu-id="a415b-113">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a415b-113">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a415b-114">Задайте для параметра значение ДБТ \_ девицекуериремове.</span><span class="sxs-lookup"><span data-stu-id="a415b-114">Set to DBT\_DEVICEQUERYREMOVE.</span></span>

</dd> <dt>

<span data-ttu-id="a415b-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a415b-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a415b-116">Указатель на структуру, идентифицирующую удаляемое устройство.</span><span class="sxs-lookup"><span data-stu-id="a415b-116">A pointer to a structure identifying the device to remove.</span></span> <span data-ttu-id="a415b-117">Структура состоит из независимого от событий заголовка, за которым следуют элементы, зависящие от события, которые описывают устройство.</span><span class="sxs-lookup"><span data-stu-id="a415b-117">The structure consists of an event-independent header, followed by event-dependent members that describe the device.</span></span> <span data-ttu-id="a415b-118">Чтобы использовать эту структуру, рассматривайте структуру как [**\_ \_ HDR**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) -структуру для разработки вещания, а затем проверьте ее член **дбч \_ типа устройства** , чтобы определить тип устройства.</span><span class="sxs-lookup"><span data-stu-id="a415b-118">To use this structure, treat the structure as a [**DEV\_BROADCAST\_HDR**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) structure, then check its **dbch\_devicetype** member to determine the device type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a415b-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a415b-119">Return value</span></span>

<span data-ttu-id="a415b-120">Возвращает **значение true** , чтобы предоставить разрешение на удаление устройства.</span><span class="sxs-lookup"><span data-stu-id="a415b-120">Return **TRUE** to grant permission to remove a device.</span></span>

<span data-ttu-id="a415b-121">Верните ШИРОКОВЕЩАТЕЛЬный \_ запрос \_ Deny, чтобы запретить разрешение на удаление устройства.</span><span class="sxs-lookup"><span data-stu-id="a415b-121">Return BROADCAST\_QUERY\_DENY to deny permission to remove a device.</span></span>

## <a name="remarks"></a><span data-ttu-id="a415b-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a415b-122">Remarks</span></span>

<span data-ttu-id="a415b-123">Необходимо закрыть все дескрипторы устройства, иначе удаление устройства завершится ошибкой.</span><span class="sxs-lookup"><span data-stu-id="a415b-123">You must close all handles to the device or the device removal will fail.</span></span>

## <a name="examples"></a><span data-ttu-id="a415b-124">Примеры</span><span class="sxs-lookup"><span data-stu-id="a415b-124">Examples</span></span>

<span data-ttu-id="a415b-125">Пример см. в разделе [Обработка запроса на удаление устройства](processing-a-request-to-remove-a-device.md).</span><span class="sxs-lookup"><span data-stu-id="a415b-125">For an example, see [Processing a Request to Remove a Device](processing-a-request-to-remove-a-device.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a415b-126">Требования</span><span class="sxs-lookup"><span data-stu-id="a415b-126">Requirements</span></span>



| <span data-ttu-id="a415b-127">Требование</span><span class="sxs-lookup"><span data-stu-id="a415b-127">Requirement</span></span> | <span data-ttu-id="a415b-128">Значение</span><span class="sxs-lookup"><span data-stu-id="a415b-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="a415b-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a415b-129">Minimum supported client</span></span><br/> | <span data-ttu-id="a415b-130">Windows XP</span><span class="sxs-lookup"><span data-stu-id="a415b-130">Windows XP</span></span><br/>                                                            |
| <span data-ttu-id="a415b-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a415b-131">Minimum supported server</span></span><br/> | <span data-ttu-id="a415b-132">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a415b-132">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="a415b-133">Header</span><span class="sxs-lookup"><span data-stu-id="a415b-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="a415b-134"><dt>ДБТ. h</dt></span><span class="sxs-lookup"><span data-stu-id="a415b-134"><dt>Dbt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a415b-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a415b-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a415b-136">События устройства</span><span class="sxs-lookup"><span data-stu-id="a415b-136">Device Events</span></span>](device-events.md)
</dt> <dt>

[<span data-ttu-id="a415b-137">События управления устройствами</span><span class="sxs-lookup"><span data-stu-id="a415b-137">Device Management Events</span></span>](device-management-events.md)
</dt> <dt>

[<span data-ttu-id="a415b-138">**расвещание для разработки в \_ \_ HDR**</span><span class="sxs-lookup"><span data-stu-id="a415b-138">**DEV\_BROADCAST\_HDR**</span></span>](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr)
</dt> <dt>

[<span data-ttu-id="a415b-139">**WM \_ девицечанже**</span><span class="sxs-lookup"><span data-stu-id="a415b-139">**WM\_DEVICECHANGE**</span></span>](wm-devicechange.md)
</dt> </dl>

 

 




