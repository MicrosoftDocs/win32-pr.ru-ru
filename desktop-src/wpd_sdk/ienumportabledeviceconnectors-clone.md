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
ms.openlocfilehash: 53b9c49b5bf36571409cd49026d5d08fced80c3e43aee63d844abd481e51aa3b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055334"
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



 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>                                                                                                                             |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                                                                              |
| Заголовок<br/>                   | <dl> <dt>Девпкэй. h; </dt> <dt>Портабледевицеконнектапи. h</dt> </dl> |
| IDL<br/>                      | <dl> <dt>Портабледевицеконнектапи. idl</dt> </dl>                                                                |
| Библиотека<br/>                  | <dl> <dt>Портабледевицегуидс. lib</dt> </dl>                                                                     |



## <a name="see-also"></a>См. также

<dl> <dt>

[**иенумпортабледевицеконнекторс**](ienumportabledeviceconnectors.md)
</dt> </dl>

 

 




