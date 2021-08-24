---
title: Ибасикдевице Канвакедевицес, метод
description: Возвращает значение, указывающее, может ли устройство пробудиться.
ms.assetid: AAD0597C-AD33-40EE-A5DA-27AC66375D38
keywords:
- API потоковой передачи мультимедиа метода Канвакедевицес
- API потоковой передачи мультимедиа метода Канвакедевицес, интерфейс Ибасикдевице
- API потоковой передачи мультимедиа интерфейса Ибасикдевице, метод Канвакедевицес
topic_type:
- apiref
api_name:
- IBasicDevice.CanWakeDevices
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3ebd0cfe9bf773d78297454d4a7643a74c3d6ea23aea01eeb54cd5c014ce73e0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119847674"
---
# <a name="ibasicdevicecanwakedevices-method"></a>Метод Ибасикдевице:: Канвакедевицес

Возвращает значение, указывающее, может ли устройство пробудиться.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT CanWakeDevices(
  [out] boolean *value
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*значение* \[ заполняет\]
</dt> <dd>

Получает указатель на логическое значение, равное **true** , если устройство может пробудиться.

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

 

 





