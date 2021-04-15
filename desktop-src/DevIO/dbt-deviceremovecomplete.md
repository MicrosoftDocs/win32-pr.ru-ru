---
description: Система передает \_ событие ДБТ девицеремовекомплете Device, когда устройство или носитель физически удаляются.
ms.assetid: e25d35b9-f8f1-4850-996c-e1cb393cca66
title: Событие DBT_DEVICEREMOVECOMPLETE (ДБТ. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16c899d8cee4a0be34829ba0a8edbaf27be71f6c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655857"
---
# <a name="dbt_deviceremovecomplete-event"></a><span data-ttu-id="ea2f0-103">\_Событие ДБТ девицеремовекомплете</span><span class="sxs-lookup"><span data-stu-id="ea2f0-103">DBT\_DEVICEREMOVECOMPLETE event</span></span>

<span data-ttu-id="ea2f0-104">Система передает \_ событие ДБТ девицеремовекомплете Device, когда устройство или носитель физически удаляются.</span><span class="sxs-lookup"><span data-stu-id="ea2f0-104">The system broadcasts the DBT\_DEVICEREMOVECOMPLETE device event when a device or piece of media has been physically removed.</span></span>

<span data-ttu-id="ea2f0-105">Чтобы транслировать это событие устройства, система использует сообщение [**WM \_ девицечанже**](wm-devicechange.md) с параметром *wParam* Set ДБТ \_ девицеремовекомплете и *lParam* Set, как описано ниже.</span><span class="sxs-lookup"><span data-stu-id="ea2f0-105">To broadcast this device event, the system uses the [**WM\_DEVICECHANGE**](wm-devicechange.md) message with *wParam* set to DBT\_DEVICEREMOVECOMPLETE and *lParam* set as described following.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd,       // handle to window
  UINT uMsg,       // WM_DEVICECHANGE
  WPARAM wParam,   // device-change event
  LPARAM lParam    // event-specific data
);
```



## <a name="parameters"></a><span data-ttu-id="ea2f0-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ea2f0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea2f0-107">*HWND*</span><span class="sxs-lookup"><span data-stu-id="ea2f0-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="ea2f0-108">Дескриптор окна.</span><span class="sxs-lookup"><span data-stu-id="ea2f0-108">A handle to a window.</span></span>

</dd> <dt>

<span data-ttu-id="ea2f0-109">*Uiacp*</span><span class="sxs-lookup"><span data-stu-id="ea2f0-109">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="ea2f0-110">Идентификатор сообщения [**WM \_ девицечанже**](wm-devicechange.md) .</span><span class="sxs-lookup"><span data-stu-id="ea2f0-110">The [**WM\_DEVICECHANGE**](wm-devicechange.md) message identifier.</span></span>

</dd> <dt>

<span data-ttu-id="ea2f0-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ea2f0-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ea2f0-112">Задайте значение ДБТ \_ девицеремовекомплете</span><span class="sxs-lookup"><span data-stu-id="ea2f0-112">Set to DBT\_DEVICEREMOVECOMPLETE</span></span>

</dd> <dt>

<span data-ttu-id="ea2f0-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ea2f0-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ea2f0-114">Указатель на структуру, идентифицирующую удаленное устройство.</span><span class="sxs-lookup"><span data-stu-id="ea2f0-114">A pointer to a structure identifying the device removed.</span></span> <span data-ttu-id="ea2f0-115">Структура состоит из независимого от событий заголовка, за которым следуют элементы, зависящие от события, которые описывают устройство.</span><span class="sxs-lookup"><span data-stu-id="ea2f0-115">The structure consists of an event-independent header, followed by event-dependent members that describe the device.</span></span> <span data-ttu-id="ea2f0-116">Чтобы использовать эту структуру, рассматривайте структуру как [**\_ \_ HDR**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) -структуру для разработки вещания, а затем проверьте ее член **дбч \_ типа устройства** , чтобы определить тип устройства.</span><span class="sxs-lookup"><span data-stu-id="ea2f0-116">To use this structure, treat the structure as a [**DEV\_BROADCAST\_HDR**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) structure, then check its **dbch\_devicetype** member to determine the device type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea2f0-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ea2f0-117">Return value</span></span>

<span data-ttu-id="ea2f0-118">Возвращает **значение true**.</span><span class="sxs-lookup"><span data-stu-id="ea2f0-118">Return **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="ea2f0-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ea2f0-119">Remarks</span></span>

<span data-ttu-id="ea2f0-120">Система может транслировать \_ сообщение ДБТ девицеремовекомплете, не отправляя соответствующие сообщения [ДБТ \_ девицекуериремове](dbt-devicequeryremove.md) и [ДБТ \_ девицеремовепендинг](dbt-deviceremovepending.md) .</span><span class="sxs-lookup"><span data-stu-id="ea2f0-120">The system may broadcast a DBT\_DEVICEREMOVECOMPLETE message without sending corresponding [DBT\_DEVICEQUERYREMOVE](dbt-devicequeryremove.md) and [DBT\_DEVICEREMOVEPENDING](dbt-deviceremovepending.md) messages.</span></span> <span data-ttu-id="ea2f0-121">В таких случаях приложения и драйверы должны быть восстановлены после потери устройства, как лучше.</span><span class="sxs-lookup"><span data-stu-id="ea2f0-121">In such cases, the applications and drivers must recover from the loss of the device as best they can.</span></span>

<span data-ttu-id="ea2f0-122">Если носитель удаляется, тип поступающего устройства — это том ( **дбч \_ типа устройства** ДБТ \_ девтип \_ Volume), и изменение влияет на носитель (член **дбкв \_ flags** — дбтф \_ Media).</span><span class="sxs-lookup"><span data-stu-id="ea2f0-122">If media is being removed, the type of device arriving is a volume (the **dbch\_devicetype** member is DBT\_DEVTYP\_VOLUME) and the change effects the media (the **dbcv\_flags** member is DBTF\_MEDIA).</span></span>

## <a name="examples"></a><span data-ttu-id="ea2f0-123">Примеры</span><span class="sxs-lookup"><span data-stu-id="ea2f0-123">Examples</span></span>

<span data-ttu-id="ea2f0-124">Пример см. в разделе [обнаружение вставки или удаления носителя](detecting-media-insertion-or-removal.md) или [Обработка запроса на удаление устройства](processing-a-request-to-remove-a-device.md).</span><span class="sxs-lookup"><span data-stu-id="ea2f0-124">For an example, see [Detecting Media Insertion or Removal](detecting-media-insertion-or-removal.md) or [Processing a Request to Remove a Device](processing-a-request-to-remove-a-device.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ea2f0-125">Требования</span><span class="sxs-lookup"><span data-stu-id="ea2f0-125">Requirements</span></span>



| <span data-ttu-id="ea2f0-126">Требование</span><span class="sxs-lookup"><span data-stu-id="ea2f0-126">Requirement</span></span> | <span data-ttu-id="ea2f0-127">Значение</span><span class="sxs-lookup"><span data-stu-id="ea2f0-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="ea2f0-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ea2f0-128">Minimum supported client</span></span><br/> | <span data-ttu-id="ea2f0-129">Windows XP</span><span class="sxs-lookup"><span data-stu-id="ea2f0-129">Windows XP</span></span><br/>                                                            |
| <span data-ttu-id="ea2f0-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ea2f0-130">Minimum supported server</span></span><br/> | <span data-ttu-id="ea2f0-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ea2f0-131">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="ea2f0-132">Header</span><span class="sxs-lookup"><span data-stu-id="ea2f0-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="ea2f0-133"><dt>ДБТ. h</dt></span><span class="sxs-lookup"><span data-stu-id="ea2f0-133"><dt>Dbt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ea2f0-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ea2f0-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea2f0-135">События устройства</span><span class="sxs-lookup"><span data-stu-id="ea2f0-135">Device Events</span></span>](device-events.md)
</dt> <dt>

[<span data-ttu-id="ea2f0-136">События управления устройствами</span><span class="sxs-lookup"><span data-stu-id="ea2f0-136">Device Management Events</span></span>](device-management-events.md)
</dt> <dt>

[<span data-ttu-id="ea2f0-137">**расвещание для разработки в \_ \_ HDR**</span><span class="sxs-lookup"><span data-stu-id="ea2f0-137">**DEV\_BROADCAST\_HDR**</span></span>](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr)
</dt> <dt>

[<span data-ttu-id="ea2f0-138">**WM \_ девицечанже**</span><span class="sxs-lookup"><span data-stu-id="ea2f0-138">**WM\_DEVICECHANGE**</span></span>](wm-devicechange.md)
</dt> </dl>

 

 




