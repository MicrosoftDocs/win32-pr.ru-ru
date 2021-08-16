---
description: сообщает приложению о завершении ранее запланированного Подключение или отключения запроса к устройству MTP/Bluetooth.
ms.assetid: 1588d0ec-0d6a-4379-bfdc-4ba5fdaa4665
title: 'Метод Иконнектионрекуесткаллбакк:: OnComplete (Девпкэй. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IConnectionRequestCallback.OnComplete
api_type:
- COM
api_location:
- PortableDeviceGuids.lib
- PortableDeviceGuids.dll
ms.openlocfilehash: b21248cde95d4b58accb7e629efedfc7c05eef7b08f411e240314a6a07690b3a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117843192"
---
# <a name="iconnectionrequestcallbackoncomplete-method"></a>Метод Иконнектионрекуесткаллбакк:: OnComplete

метод **oncomplete** уведомляет приложение о завершении ранее запланированного Подключение или отключения запроса к устройству MTP/Bluetooth

## <a name="syntax"></a>Синтаксис


```C++
HRESULT OnComplete(
  [in] HRESULT hrStatus
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хрстатус* \[ окне\]
</dt> <dd>

Состояние запроса на подключение или отключение данного устройства.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Метод возвращает **значение HRESULT**. Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.



| Код возврата                                                                          | Описание                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl> | Метод выполнен успешно.<br/> |



 

## <a name="remarks"></a>Remarks

Приложение реализует интерфейс [**иконнектионрекуесткаллбакк**](iconnectionrequestcallback.md) для получения уведомлений о завершенных запросах и отмены ожидающих запросов.

Windows Переносные устройства (WPD) вызывают этот метод, чтобы уведомить приложение о завершении ранее запланированного запроса. Каждый запрос можно относить и отменять с помощью обратного вызова, предоставленного приложением. поэтому, если приложению нужно отправить несколько запросов одновременно с помощью одного и того же объекта [**ипортабледевицеконнектор**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector) , каждому запросу должен быть передан уникальный объект [**иконнектионрекуесткаллбакк**](iconnectionrequestcallback.md) в качестве входного параметра для методов [**ипортабледевицеконнектор:: Подключение**](/windows/desktop/api/portabledeviceconnectapi/nf-portabledeviceconnectapi-iportabledeviceconnector-connect) и [**ипортабледевицеконнектор::D соединения**](/windows/desktop/api/portabledeviceconnectapi/nf-portabledeviceconnectapi-iportabledeviceconnector-disconnect) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>                                                                                                                             |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                                                                              |
| Header<br/>                   | <dl> <dt>Девпкэй. h; </dt> <dt>Портабледевицеконнектапи. h</dt> </dl> |
| IDL<br/>                      | <dl> <dt>Портабледевицеконнектапи. idl</dt> </dl>                                                                |
| Библиотека<br/>                  | <dl> <dt>Портабледевицегуидс. lib</dt> </dl>                                                                     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**иконнектионрекуесткаллбакк**](iconnectionrequestcallback.md)
</dt> </dl>

 

 




