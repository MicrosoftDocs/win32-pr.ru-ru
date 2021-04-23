---
description: Система передает \_ событие ДБТ девицеарривал Device, когда устройство или носитель вставлены и становятся доступными.
ms.assetid: 8e44cb02-cf79-4b19-807e-20cea07362af
title: Событие DBT_DEVICEARRIVAL (ДБТ. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f69c2feec996b4306c271454767ca4e75d1ff855
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496212"
---
# <a name="dbt_devicearrival-event"></a><span data-ttu-id="639ed-103">\_Событие ДБТ девицеарривал</span><span class="sxs-lookup"><span data-stu-id="639ed-103">DBT\_DEVICEARRIVAL event</span></span>

<span data-ttu-id="639ed-104">Система передает \_ событие ДБТ девицеарривал Device, когда устройство или носитель вставлены и становятся доступными.</span><span class="sxs-lookup"><span data-stu-id="639ed-104">The system broadcasts the DBT\_DEVICEARRIVAL device event when a device or piece of media has been inserted and becomes available.</span></span>

<span data-ttu-id="639ed-105">Чтобы транслировать это событие устройства, система использует сообщение [**WM \_ девицечанже**](wm-devicechange.md) с параметром *wParam* Set ДБТ \_ девицеарривал и *lParam* Set, как описано ниже.</span><span class="sxs-lookup"><span data-stu-id="639ed-105">To broadcast this device event, the system uses the [**WM\_DEVICECHANGE**](wm-devicechange.md) message with *wParam* set to DBT\_DEVICEARRIVAL and *lParam* set as described following.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd,       // handle to window
  UINT uMsg,       // WM_DEVICECHANGE
  WPARAM wParam,   // device-change event
  LPARAM lParam    // event-specific data
);
```



## <a name="parameters"></a><span data-ttu-id="639ed-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="639ed-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="639ed-107">*HWND*</span><span class="sxs-lookup"><span data-stu-id="639ed-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="639ed-108">Дескриптор окна.</span><span class="sxs-lookup"><span data-stu-id="639ed-108">A handle to a window.</span></span>

</dd> <dt>

<span data-ttu-id="639ed-109">*Uiacp*</span><span class="sxs-lookup"><span data-stu-id="639ed-109">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="639ed-110">Идентификатор сообщения [**WM \_ девицечанже**](wm-devicechange.md) .</span><span class="sxs-lookup"><span data-stu-id="639ed-110">The [**WM\_DEVICECHANGE**](wm-devicechange.md) message identifier.</span></span>

</dd> <dt>

<span data-ttu-id="639ed-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="639ed-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="639ed-112">Задайте для параметра значение ДБТ \_ девицеарривал.</span><span class="sxs-lookup"><span data-stu-id="639ed-112">Set to DBT\_DEVICEARRIVAL.</span></span>

</dd> <dt>

<span data-ttu-id="639ed-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="639ed-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="639ed-114">Указатель на структуру, идентифицирующую вставленное устройство.</span><span class="sxs-lookup"><span data-stu-id="639ed-114">A pointer to a structure identifying the device inserted.</span></span> <span data-ttu-id="639ed-115">Структура состоит из независимого от событий заголовка, за которым следуют элементы, зависящие от события, которые описывают устройство.</span><span class="sxs-lookup"><span data-stu-id="639ed-115">The structure consists of an event-independent header, followed by event-dependent members that describe the device.</span></span> <span data-ttu-id="639ed-116">Чтобы использовать эту структуру, рассматривайте структуру как [**\_ \_ HDR**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) -структуру для разработки вещания, а затем проверьте ее член **дбч \_ типа устройства** , чтобы определить тип устройства.</span><span class="sxs-lookup"><span data-stu-id="639ed-116">To use this structure, treat the structure as a [**DEV\_BROADCAST\_HDR**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) structure, then check its **dbch\_devicetype** member to determine the device type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="639ed-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="639ed-117">Return value</span></span>

<span data-ttu-id="639ed-118">Возвращает **значение true**.</span><span class="sxs-lookup"><span data-stu-id="639ed-118">Return **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="639ed-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="639ed-119">Remarks</span></span>

<span data-ttu-id="639ed-120">Если вставляется носитель, тип поступающих устройств — это том ( **дбч \_ типа устройства** ДБТ \_ девтип \_ Volume), и изменение влияет на носитель (член **дбкв \_ flags** — дбтф \_ Media).</span><span class="sxs-lookup"><span data-stu-id="639ed-120">If media is being inserted, the type of device arriving is a volume (the **dbch\_devicetype** member is DBT\_DEVTYP\_VOLUME) and the change effects the media (the **dbcv\_flags** member is DBTF\_MEDIA).</span></span>

## <a name="examples"></a><span data-ttu-id="639ed-121">Примеры</span><span class="sxs-lookup"><span data-stu-id="639ed-121">Examples</span></span>

<span data-ttu-id="639ed-122">Пример см. в разделе [обнаружение вставки или удаления носителя](detecting-media-insertion-or-removal.md).</span><span class="sxs-lookup"><span data-stu-id="639ed-122">For an example, see [Detecting Media Insertion or Removal](detecting-media-insertion-or-removal.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="639ed-123">Требования</span><span class="sxs-lookup"><span data-stu-id="639ed-123">Requirements</span></span>



| <span data-ttu-id="639ed-124">Требование</span><span class="sxs-lookup"><span data-stu-id="639ed-124">Requirement</span></span> | <span data-ttu-id="639ed-125">Значение</span><span class="sxs-lookup"><span data-stu-id="639ed-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="639ed-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="639ed-126">Minimum supported client</span></span><br/> | <span data-ttu-id="639ed-127">Windows XP</span><span class="sxs-lookup"><span data-stu-id="639ed-127">Windows XP</span></span><br/>                                                            |
| <span data-ttu-id="639ed-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="639ed-128">Minimum supported server</span></span><br/> | <span data-ttu-id="639ed-129">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="639ed-129">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="639ed-130">Header</span><span class="sxs-lookup"><span data-stu-id="639ed-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="639ed-131"><dt>ДБТ. h</dt></span><span class="sxs-lookup"><span data-stu-id="639ed-131"><dt>Dbt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="639ed-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="639ed-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="639ed-133">События устройства</span><span class="sxs-lookup"><span data-stu-id="639ed-133">Device Events</span></span>](device-events.md)
</dt> <dt>

[<span data-ttu-id="639ed-134">События управления устройствами</span><span class="sxs-lookup"><span data-stu-id="639ed-134">Device Management Events</span></span>](device-management-events.md)
</dt> <dt>

[<span data-ttu-id="639ed-135">**расвещание для разработки в \_ \_ HDR**</span><span class="sxs-lookup"><span data-stu-id="639ed-135">**DEV\_BROADCAST\_HDR**</span></span>](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr)
</dt> <dt>

[<span data-ttu-id="639ed-136">**WM \_ девицечанже**</span><span class="sxs-lookup"><span data-stu-id="639ed-136">**WM\_DEVICECHANGE**</span></span>](wm-devicechange.md)
</dt> </dl>

 

 




