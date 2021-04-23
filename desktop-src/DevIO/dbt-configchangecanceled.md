---
description: Система передает \_ событие ДБТ конфигчанжеканцелед Device, когда запрос на изменение текущей конфигурации (закрепления или отстыковки) был отменен.
ms.assetid: b4b1455c-9a04-4fa0-a3fa-ed991f278c0c
title: Событие DBT_CONFIGCHANGECANCELED (ДБТ. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97944daa698808c55f88bc377c9bf1c59c1217fb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895882"
---
# <a name="dbt_configchangecanceled-event"></a><span data-ttu-id="95cc9-103">\_Событие ДБТ конфигчанжеканцелед</span><span class="sxs-lookup"><span data-stu-id="95cc9-103">DBT\_CONFIGCHANGECANCELED event</span></span>

<span data-ttu-id="95cc9-104">Система передает \_ событие ДБТ конфигчанжеканцелед Device, когда запрос на изменение текущей конфигурации (закрепления или отстыковки) был отменен.</span><span class="sxs-lookup"><span data-stu-id="95cc9-104">The system broadcasts the DBT\_CONFIGCHANGECANCELED device event when a request to change the current configuration (dock or undock) has been canceled.</span></span>

<span data-ttu-id="95cc9-105">Чтобы транслировать это событие устройства, система использует сообщение [**WM \_ девицечанже**](wm-devicechange.md) с параметром *wParam* , установленным в значение ДБТ \_ конфигчанжеканцелед и *lParam* , равным нулю.</span><span class="sxs-lookup"><span data-stu-id="95cc9-105">To broadcast this device event, the system uses the [**WM\_DEVICECHANGE**](wm-devicechange.md) message with *wParam* set to DBT\_CONFIGCHANGECANCELED and *lParam* set to zero.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd,       // handle to window
  UINT uMsg,       // WM_DEVICECHANGE
  WPARAM wParam,   // device-change event
  LPARAM lParam    // event-specific data
);
```



## <a name="parameters"></a><span data-ttu-id="95cc9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="95cc9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95cc9-107">*HWND*</span><span class="sxs-lookup"><span data-stu-id="95cc9-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="95cc9-108">Дескриптор окна.</span><span class="sxs-lookup"><span data-stu-id="95cc9-108">A handle to a window.</span></span>

</dd> <dt>

<span data-ttu-id="95cc9-109">*Uiacp*</span><span class="sxs-lookup"><span data-stu-id="95cc9-109">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="95cc9-110">Идентификатор сообщения [**WM \_ девицечанже**](wm-devicechange.md) .</span><span class="sxs-lookup"><span data-stu-id="95cc9-110">The [**WM\_DEVICECHANGE**](wm-devicechange.md) message identifier.</span></span>

</dd> <dt>

<span data-ttu-id="95cc9-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="95cc9-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="95cc9-112">Задайте для параметра значение ДБТ \_ конфигчанжеканцелед.</span><span class="sxs-lookup"><span data-stu-id="95cc9-112">Set to DBT\_CONFIGCHANGECANCELED.</span></span>

</dd> <dt>

<span data-ttu-id="95cc9-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="95cc9-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="95cc9-114">Задайте нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="95cc9-114">Set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95cc9-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="95cc9-115">Return value</span></span>

<span data-ttu-id="95cc9-116">Возвращает **значение true**.</span><span class="sxs-lookup"><span data-stu-id="95cc9-116">Return **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="95cc9-117">Требования</span><span class="sxs-lookup"><span data-stu-id="95cc9-117">Requirements</span></span>



| <span data-ttu-id="95cc9-118">Требование</span><span class="sxs-lookup"><span data-stu-id="95cc9-118">Requirement</span></span> | <span data-ttu-id="95cc9-119">Значение</span><span class="sxs-lookup"><span data-stu-id="95cc9-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="95cc9-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="95cc9-120">Minimum supported client</span></span><br/> | <span data-ttu-id="95cc9-121">Windows XP</span><span class="sxs-lookup"><span data-stu-id="95cc9-121">Windows XP</span></span><br/>                                                            |
| <span data-ttu-id="95cc9-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="95cc9-122">Minimum supported server</span></span><br/> | <span data-ttu-id="95cc9-123">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="95cc9-123">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="95cc9-124">Header</span><span class="sxs-lookup"><span data-stu-id="95cc9-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="95cc9-125"><dt>ДБТ. h</dt></span><span class="sxs-lookup"><span data-stu-id="95cc9-125"><dt>Dbt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95cc9-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="95cc9-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95cc9-127">События устройства</span><span class="sxs-lookup"><span data-stu-id="95cc9-127">Device Events</span></span>](device-events.md)
</dt> <dt>

[<span data-ttu-id="95cc9-128">События управления устройствами</span><span class="sxs-lookup"><span data-stu-id="95cc9-128">Device Management Events</span></span>](device-management-events.md)
</dt> <dt>

[<span data-ttu-id="95cc9-129">**WM \_ девицечанже**</span><span class="sxs-lookup"><span data-stu-id="95cc9-129">**WM\_DEVICECHANGE**</span></span>](wm-devicechange.md)
</dt> </dl>

 

 




