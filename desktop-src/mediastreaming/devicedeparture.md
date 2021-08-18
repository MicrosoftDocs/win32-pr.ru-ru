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
ms.openlocfilehash: 496fa0fcae3cba51228b37b5f06eb9b06c416322aad22f77be542274088eae32
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119712954"
---
# <a name="devicedeparture-event"></a>Событие Девицедепартуре

Происходит при удалении нового устройства из списка устройств, возвращенных методом [**качеддевицес**](idevicecontroller-cacheddevices.md) .

## <a name="syntax"></a>Синтаксис


```C++
void DeviceDeparture();
```



## <a name="parameters"></a>Параметры

У этого события нет параметров.

## <a name="return-value"></a>Возвращаемое значение

Это событие не возвращает значение.

## <a name="remarks"></a>Remarks

Для обработки уведомлений из этого события Зарегистрируйте функцию обработчика событий [**девицеконтроллерфиндерхандлер**](/previous-versions/windows/desktop/legacy/hh828843(v=vs.85)) с помощью метода [**Add \_ девицедепартуре**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-idevicecontroller-add_devicedeparture) . Чтобы отменить регистрацию обработчика событий, используйте метод [**Remove \_ девицедепартуре**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-idevicecontroller-remove_devicedeparture) .

 

 