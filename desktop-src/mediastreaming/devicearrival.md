---
title: Событие Девицеарривал
description: Происходит при добавлении нового устройства в список устройств, возвращенных методом Качеддевицес.
ms.assetid: C7CB49AE-C05F-4A2A-8A30-4B4BB7C7D9D2
keywords:
- API потоковой передачи мультимедиа для события Девицеарривал
topic_type:
- apiref
api_name:
- DeviceArrival
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79fbdd68ae6c77c6a0f3e7bbd3cf976b5d056987
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103790195"
---
# <a name="devicearrival-event"></a><span data-ttu-id="4270a-104">Событие Девицеарривал</span><span class="sxs-lookup"><span data-stu-id="4270a-104">DeviceArrival event</span></span>

<span data-ttu-id="4270a-105">Происходит при добавлении нового устройства в список устройств, возвращенных методом [**качеддевицес**](idevicecontroller-cacheddevices.md) .</span><span class="sxs-lookup"><span data-stu-id="4270a-105">Occurs when a new device is added to the list of devices returned by the [**CachedDevices**](idevicecontroller-cacheddevices.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="4270a-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4270a-106">Syntax</span></span>


```C++
void DeviceArrival();
```



## <a name="parameters"></a><span data-ttu-id="4270a-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="4270a-107">Parameters</span></span>

<span data-ttu-id="4270a-108">У этого события нет параметров.</span><span class="sxs-lookup"><span data-stu-id="4270a-108">This event has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4270a-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4270a-109">Return value</span></span>

<span data-ttu-id="4270a-110">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="4270a-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4270a-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4270a-111">Remarks</span></span>

<span data-ttu-id="4270a-112">Для обработки уведомлений из этого события Зарегистрируйте функцию обработчика событий [**девицеконтроллерфиндерхандлер**](/previous-versions/windows/desktop/legacy/hh828843(v=vs.85)) с помощью метода [**Add \_ девицеарривал**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-idevicecontroller-add_devicearrival) .</span><span class="sxs-lookup"><span data-stu-id="4270a-112">To handle notifications from this event, register a [**DeviceControllerFinderHandler**](/previous-versions/windows/desktop/legacy/hh828843(v=vs.85)) event handler function using the [**add\_DeviceArrival**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-idevicecontroller-add_devicearrival) method.</span></span> <span data-ttu-id="4270a-113">Чтобы отменить регистрацию обработчика событий, используйте метод [**Remove \_ девицеарривал**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-idevicecontroller-remove_devicearrival) .</span><span class="sxs-lookup"><span data-stu-id="4270a-113">To unregister the event handler, use the [**remove\_DeviceArrival**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-idevicecontroller-remove_devicearrival) method.</span></span>

 

 