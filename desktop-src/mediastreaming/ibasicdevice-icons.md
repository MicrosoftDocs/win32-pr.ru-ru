---
title: Метод Ибасикдевице значков
description: Возвращает вектор интерфейсов Идевицеикон.
ms.assetid: 0C083AF3-FE22-4A8E-87B7-0FFA7B65ADBD
keywords:
- Значки. метод API потоковой передачи мультимедиа
- Значки. метод API потоковой передачи мультимедиа, интерфейс Ибасикдевице
- API потоковой передачи мультимедиа интерфейса Ибасикдевице, метод значков
topic_type:
- apiref
api_name:
- IBasicDevice.Icons
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6fdb514b2f6ab09a2c0024d37ed32e9968fe08dd7f16aefe40298ac2ba5497c3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060444"
---
# <a name="ibasicdeviceicons-method"></a>Метод Ибасикдевице:: пиктограммы

Возвращает вектор интерфейсов [**идевицеикон**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-ideviceicon) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Icons(
  [out] IVector< IDeviceIcon > **value
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*значение* \[ заполняет\]
</dt> <dd>

Получает перечисляемую коллекцию указателей интерфейса [**идевицеикон**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-ideviceicon) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Метод возвращает **значение HRESULT**. Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.



| Код возврата                                                                          | Описание                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl> | Метод выполнен успешно.<br/> |



 

## <a name="see-also"></a>См. также

<dl> <dt>

[**ибасикдевице**](ibasicdevice.md)
</dt> </dl>

 

