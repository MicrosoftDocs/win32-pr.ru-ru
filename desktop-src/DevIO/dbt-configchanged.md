---
description: Система передает \_ событие ДБТ конфигчанжед Device, чтобы указать, что текущая конфигурация изменилась из-за закрепления или отстыковки. Приложение или драйвер, в котором хранятся данные в реестре в \_ текущем \_ ключе конфигурации hKey, должны обновлять данные.
ms.assetid: e5e33970-b17e-4723-98aa-e242f90fe4e7
title: Событие DBT_CONFIGCHANGED (ДБТ. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d242832378ba9ca3d3006965719942aa41ecff93
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262631"
---
# <a name="dbt_configchanged-event"></a><span data-ttu-id="4dce0-104">\_Событие ДБТ конфигчанжед</span><span class="sxs-lookup"><span data-stu-id="4dce0-104">DBT\_CONFIGCHANGED event</span></span>

<span data-ttu-id="4dce0-105">Система передает \_ событие ДБТ конфигчанжед Device, чтобы указать, что текущая конфигурация изменилась из-за закрепления или отстыковки.</span><span class="sxs-lookup"><span data-stu-id="4dce0-105">The system broadcasts the DBT\_CONFIGCHANGED device event to indicate that the current configuration has changed, due to a dock or undock.</span></span> <span data-ttu-id="4dce0-106">Приложение или драйвер, в котором хранятся данные в реестре в \_ текущем \_ ключе конфигурации hKey, должны обновлять данные.</span><span class="sxs-lookup"><span data-stu-id="4dce0-106">An application or driver that stores data in the registry under the HKEY\_CURRENT\_CONFIG key should update the data.</span></span>

<span data-ttu-id="4dce0-107">Чтобы транслировать это событие устройства, система использует сообщение [**WM \_ девицечанже**](wm-devicechange.md) с параметром *wParam* , установленным в значение ДБТ \_ конфигчанжед и *lParam* , равным нулю.</span><span class="sxs-lookup"><span data-stu-id="4dce0-107">To broadcast this device event, the system uses the [**WM\_DEVICECHANGE**](wm-devicechange.md) message with *wParam* set to DBT\_CONFIGCHANGED and *lParam* set to zero.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd,       // handle to window
  UINT uMsg,       // WM_DEVICECHANGE
  WPARAM wParam,   // device-change event
  LPARAM lParam    // event-specific data
);
```



## <a name="parameters"></a><span data-ttu-id="4dce0-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="4dce0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4dce0-109">*HWND*</span><span class="sxs-lookup"><span data-stu-id="4dce0-109">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="4dce0-110">Дескриптор окна.</span><span class="sxs-lookup"><span data-stu-id="4dce0-110">A handle to a window.</span></span>

</dd> <dt>

<span data-ttu-id="4dce0-111">*Uiacp*</span><span class="sxs-lookup"><span data-stu-id="4dce0-111">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="4dce0-112">Идентификатор сообщения [**WM \_ девицечанже**](wm-devicechange.md) .</span><span class="sxs-lookup"><span data-stu-id="4dce0-112">The [**WM\_DEVICECHANGE**](wm-devicechange.md) message identifier.</span></span>

</dd> <dt>

<span data-ttu-id="4dce0-113">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4dce0-113">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4dce0-114">Задайте для параметра значение ДБТ \_ конфигчанжед.</span><span class="sxs-lookup"><span data-stu-id="4dce0-114">Set to DBT\_CONFIGCHANGED.</span></span>

</dd> <dt>

<span data-ttu-id="4dce0-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4dce0-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4dce0-116">Задайте нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="4dce0-116">Set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4dce0-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4dce0-117">Return value</span></span>

<span data-ttu-id="4dce0-118">Возвращает **значение true**.</span><span class="sxs-lookup"><span data-stu-id="4dce0-118">Return **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="4dce0-119">Требования</span><span class="sxs-lookup"><span data-stu-id="4dce0-119">Requirements</span></span>



| <span data-ttu-id="4dce0-120">Требование</span><span class="sxs-lookup"><span data-stu-id="4dce0-120">Requirement</span></span> | <span data-ttu-id="4dce0-121">Значение</span><span class="sxs-lookup"><span data-stu-id="4dce0-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="4dce0-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4dce0-122">Minimum supported client</span></span><br/> | <span data-ttu-id="4dce0-123">Windows XP</span><span class="sxs-lookup"><span data-stu-id="4dce0-123">Windows XP</span></span><br/>                                                            |
| <span data-ttu-id="4dce0-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4dce0-124">Minimum supported server</span></span><br/> | <span data-ttu-id="4dce0-125">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="4dce0-125">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="4dce0-126">Header</span><span class="sxs-lookup"><span data-stu-id="4dce0-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="4dce0-127"><dt>ДБТ. h</dt></span><span class="sxs-lookup"><span data-stu-id="4dce0-127"><dt>Dbt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4dce0-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4dce0-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4dce0-129">События устройства</span><span class="sxs-lookup"><span data-stu-id="4dce0-129">Device Events</span></span>](device-events.md)
</dt> <dt>

[<span data-ttu-id="4dce0-130">События управления устройствами</span><span class="sxs-lookup"><span data-stu-id="4dce0-130">Device Management Events</span></span>](device-management-events.md)
</dt> <dt>

[<span data-ttu-id="4dce0-131">**WM \_ девицечанже**</span><span class="sxs-lookup"><span data-stu-id="4dce0-131">**WM\_DEVICECHANGE**</span></span>](wm-devicechange.md)
</dt> </dl>

 

 




