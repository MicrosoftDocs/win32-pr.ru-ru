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
ms.openlocfilehash: ed65c2b1c37eb91f9bf0a0c060fb76b85cd1f5b3d06b6ff1ab795ec89a0db6bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119721214"
---
# <a name="devicearrival-event"></a>Событие Девицеарривал

Происходит при добавлении нового устройства в список устройств, возвращенных методом [**качеддевицес**](idevicecontroller-cacheddevices.md) .

## <a name="syntax"></a>Синтаксис


```C++
void DeviceArrival();
```



## <a name="parameters"></a>Параметры

У этого события нет параметров.

## <a name="return-value"></a>Возвращаемое значение

Это событие не возвращает значение.

## <a name="remarks"></a>Remarks

Для обработки уведомлений из этого события Зарегистрируйте функцию обработчика событий [**девицеконтроллерфиндерхандлер**](/previous-versions/windows/desktop/legacy/hh828843(v=vs.85)) с помощью метода [**Add \_ девицеарривал**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-idevicecontroller-add_devicearrival) . Чтобы отменить регистрацию обработчика событий, используйте метод [**Remove \_ девицеарривал**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-idevicecontroller-remove_devicearrival) .

 

 