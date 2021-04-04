---
title: Идевицеконтроллер Качеддевицес, метод
description: Извлекает коллекцию указателей интерфейса Ибасикдевице, представляющих кэшированное представление всех обнаруживаемых устройств DLNA. | Идевицеконтроллер Качеддевицес, метод
ms.assetid: 94C2A7FF-5AF8-4F13-BBA5-54ED78C3BBF6
keywords:
- API потоковой передачи мультимедиа метода Качеддевицес
- API потоковой передачи мультимедиа метода Качеддевицес, интерфейс Идевицеконтроллер
- API потоковой передачи мультимедиа интерфейса Идевицеконтроллер, метод Качеддевицес
topic_type:
- apiref
api_name:
- IDeviceController.CachedDevices
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 69be1faea277fa8999ae5ddf3658aaa61a1116b9
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104000280"
---
# <a name="idevicecontrollercacheddevices-method"></a>Метод Идевицеконтроллер:: Качеддевицес

Извлекает коллекцию указателей интерфейса [**ибасикдевице**](ibasicdevice.md) , представляющих кэшированное представление всех обнаруживаемых устройств DLNA.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT CachedDevices(
  [out] IVector< IBasicDevice > **value
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*значение* \[ заполняет\]
</dt> <dd>

Получает перечисляемую коллекцию указателей интерфейса [**ибасикдевице**](ibasicdevice.md) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Метод возвращает **значение HRESULT**. Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.



| Код возврата                                                                          | Описание                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl> | Метод выполнен успешно.<br/> |



 

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**идевицеконтроллер**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-idevicecontroller)
</dt> </dl>

 

