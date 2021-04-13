---
description: Создает копию текущего интерфейса Иенумпортабледевицеконнекторс.
ms.assetid: 64274cb0-1f57-481d-914f-41238cbe2f1b
title: 'Метод Иенумпортабледевицеконнекторс:: Clone (Девпкэй. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPortableDeviceConnectors.Clone
api_type:
- COM
api_location:
- PortableDeviceGuids.lib
- PortableDeviceGuids.dll
ms.openlocfilehash: 0e5273f1c400732c94c7c63918787f5e130a854d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348565"
---
# <a name="ienumportabledeviceconnectorsclone-method"></a>Метод Иенумпортабледевицеконнекторс:: Clone

Метод **clone** создает копию текущего интерфейса [**иенумпортабледевицеконнекторс**](ienumportabledeviceconnectors.md) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Clone(
  [out] IEnumPortableDeviceConnectors **ppEnum
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ппенум* \[ заполняет\]
</dt> <dd>

Адрес указателя на интерфейс [**иенумпортабледевицеконнекторс**](ienumportabledeviceconnectors.md) . Вызывающее приложение должно освободить этот интерфейс, когда он завершит работу с ним.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Метод возвращает **значение HRESULT**. Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.



| Код возврата                                                                          | Описание                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl> | Метод выполнен успешно.<br/> |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 7\]<br/>                                                                                                                             |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                                                                              |
| Header<br/>                   | <dl> <dt>Девпкэй. h; </dt> <dt>Портабледевицеконнектапи. h</dt> </dl> |
| IDL<br/>                      | <dl> <dt>Портабледевицеконнектапи. idl</dt> </dl>                                                                |
| Библиотека<br/>                  | <dl> <dt>Портабледевицегуидс. lib</dt> </dl>                                                                     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**иенумпортабледевицеконнекторс**](ienumportabledeviceconnectors.md)
</dt> </dl>

 

 




