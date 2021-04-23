---
title: Событие Девицедепартуре
description: Происходит при удалении нового устройства из списка устройств, возвращенных методом Качеддевицес.
ms.assetid: 10451878-e685-4042-9f92-ba3a408c4da0
keywords:
- API потоковой передачи мультимедиа для события Девицедепартуре
topic_type:
- apiref
api_name:
- DeviceDeparture
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e225afcbe8b373b22584eaa3d9fcb09e1eff29c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "105710273"
---
# <a name="devicedeparture-event"></a><span data-ttu-id="32702-104">Событие Девицедепартуре</span><span class="sxs-lookup"><span data-stu-id="32702-104">DeviceDeparture event</span></span>

<span data-ttu-id="32702-105">Происходит при удалении нового устройства из списка устройств, возвращенных методом [**качеддевицес**](idevicecontroller-cacheddevices.md) .</span><span class="sxs-lookup"><span data-stu-id="32702-105">Occurs when a new device is removed from the list of devices returned by the [**CachedDevices**](idevicecontroller-cacheddevices.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="32702-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="32702-106">Syntax</span></span>


```C++
void DeviceDeparture();
```



## <a name="parameters"></a><span data-ttu-id="32702-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="32702-107">Parameters</span></span>

<span data-ttu-id="32702-108">У этого события нет параметров.</span><span class="sxs-lookup"><span data-stu-id="32702-108">This event has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="32702-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="32702-109">Return value</span></span>

<span data-ttu-id="32702-110">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="32702-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="32702-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="32702-111">Remarks</span></span>

<span data-ttu-id="32702-112">Для обработки уведомлений из этого события Зарегистрируйте функцию обработчика событий [**девицеконтроллерфиндерхандлер**](/previous-versions/windows/desktop/legacy/hh828843(v=vs.85)) с помощью метода [**Add \_ девицедепартуре**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-idevicecontroller-add_devicedeparture) .</span><span class="sxs-lookup"><span data-stu-id="32702-112">To handle notifications from this event, register a [**DeviceControllerFinderHandler**](/previous-versions/windows/desktop/legacy/hh828843(v=vs.85)) event handler function using the [**add\_DeviceDeparture**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-idevicecontroller-add_devicedeparture) method.</span></span> <span data-ttu-id="32702-113">Чтобы отменить регистрацию обработчика событий, используйте метод [**Remove \_ девицедепартуре**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-idevicecontroller-remove_devicedeparture) .</span><span class="sxs-lookup"><span data-stu-id="32702-113">To unregister the event handler, use the [**remove\_DeviceDeparture**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-idevicecontroller-remove_devicedeparture) method.</span></span>

 

 