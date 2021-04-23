---
description: Система передает \_ событие ДБТ куеричанжеконфиг Device, чтобы запросить разрешение на изменение текущей конфигурации (закрепление или Отстыковка). Любое приложение может отклонить этот запрос и отменить изменение.
ms.assetid: 2e452ea7-e2bf-4500-952a-ee7d891533a0
title: Событие DBT_QUERYCHANGECONFIG (ДБТ. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48367da1788ae2985b21fad6e960153008e9ffd2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538891"
---
# <a name="dbt_querychangeconfig-event"></a><span data-ttu-id="2c05d-104">\_Событие ДБТ куеричанжеконфиг</span><span class="sxs-lookup"><span data-stu-id="2c05d-104">DBT\_QUERYCHANGECONFIG event</span></span>

<span data-ttu-id="2c05d-105">Система передает \_ событие ДБТ куеричанжеконфиг Device, чтобы запросить разрешение на изменение текущей конфигурации (закрепление или Отстыковка).</span><span class="sxs-lookup"><span data-stu-id="2c05d-105">The system broadcasts the DBT\_QUERYCHANGECONFIG device event to request permission to change the current configuration (dock or undock).</span></span> <span data-ttu-id="2c05d-106">Любое приложение может отклонить этот запрос и отменить изменение.</span><span class="sxs-lookup"><span data-stu-id="2c05d-106">Any application can deny this request and cancel the change.</span></span>

<span data-ttu-id="2c05d-107">Чтобы транслировать это событие устройства, система использует сообщение [**WM \_ девицечанже**](wm-devicechange.md) с параметром *wParam* , установленным в значение ДБТ \_ куеричанжеконфиг и *lParam* , равным нулю.</span><span class="sxs-lookup"><span data-stu-id="2c05d-107">To broadcast this device event, the system uses the [**WM\_DEVICECHANGE**](wm-devicechange.md) message with *wParam* set to DBT\_QUERYCHANGECONFIG and *lParam* set to zero.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd,       // handle to window
  UINT uMsg,       // WM_DEVICECHANGE
  WPARAM wParam,   // device-change event
  LPARAM lParam    // event-specific data
);
```



## <a name="parameters"></a><span data-ttu-id="2c05d-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="2c05d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c05d-109">*HWND*</span><span class="sxs-lookup"><span data-stu-id="2c05d-109">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="2c05d-110">Дескриптор окна.</span><span class="sxs-lookup"><span data-stu-id="2c05d-110">A handle to a window.</span></span>

</dd> <dt>

<span data-ttu-id="2c05d-111">*Uiacp*</span><span class="sxs-lookup"><span data-stu-id="2c05d-111">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="2c05d-112">Идентификатор сообщения [**WM \_ девицечанже**](wm-devicechange.md) .</span><span class="sxs-lookup"><span data-stu-id="2c05d-112">The [**WM\_DEVICECHANGE**](wm-devicechange.md) message identifier.</span></span>

</dd> <dt>

<span data-ttu-id="2c05d-113">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2c05d-113">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2c05d-114">Задайте для параметра значение ДБТ \_ куеричанжеконфиг.</span><span class="sxs-lookup"><span data-stu-id="2c05d-114">Set to DBT\_QUERYCHANGECONFIG.</span></span>

</dd> <dt>

<span data-ttu-id="2c05d-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2c05d-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2c05d-116">Задайте нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="2c05d-116">Set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c05d-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2c05d-117">Return value</span></span>

<span data-ttu-id="2c05d-118">Возвращает **значение true** , чтобы предоставить разрешение на изменение конфигурации.</span><span class="sxs-lookup"><span data-stu-id="2c05d-118">Return **TRUE** to grant permission to change the configuration.</span></span>

<span data-ttu-id="2c05d-119">Верните ШИРОКОВЕЩАТЕЛЬный \_ запрос \_ Deny, чтобы запретить разрешение на изменение конфигурации.</span><span class="sxs-lookup"><span data-stu-id="2c05d-119">Return BROADCAST\_QUERY\_DENY to deny permission to change the configuration.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c05d-120">Требования</span><span class="sxs-lookup"><span data-stu-id="2c05d-120">Requirements</span></span>



| <span data-ttu-id="2c05d-121">Требование</span><span class="sxs-lookup"><span data-stu-id="2c05d-121">Requirement</span></span> | <span data-ttu-id="2c05d-122">Значение</span><span class="sxs-lookup"><span data-stu-id="2c05d-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="2c05d-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2c05d-123">Minimum supported client</span></span><br/> | <span data-ttu-id="2c05d-124">Windows XP</span><span class="sxs-lookup"><span data-stu-id="2c05d-124">Windows XP</span></span><br/>                                                            |
| <span data-ttu-id="2c05d-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2c05d-125">Minimum supported server</span></span><br/> | <span data-ttu-id="2c05d-126">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2c05d-126">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="2c05d-127">Header</span><span class="sxs-lookup"><span data-stu-id="2c05d-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="2c05d-128"><dt>ДБТ. h</dt></span><span class="sxs-lookup"><span data-stu-id="2c05d-128"><dt>Dbt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c05d-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2c05d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c05d-130">События устройства</span><span class="sxs-lookup"><span data-stu-id="2c05d-130">Device Events</span></span>](device-events.md)
</dt> <dt>

[<span data-ttu-id="2c05d-131">События управления устройствами</span><span class="sxs-lookup"><span data-stu-id="2c05d-131">Device Management Events</span></span>](device-management-events.md)
</dt> <dt>

[<span data-ttu-id="2c05d-132">**WM \_ девицечанже**</span><span class="sxs-lookup"><span data-stu-id="2c05d-132">**WM\_DEVICECHANGE**</span></span>](wm-devicechange.md)
</dt> </dl>

 

 




