---
description: Уведомляет приложение о завершении ранее запланированного запроса подключения или отключения к устройству MTP/Bluetooth.
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
ms.openlocfilehash: 922169b7e17335c47425665bb9a9e54891e68723
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911140"
---
# <a name="iconnectionrequestcallbackoncomplete-method"></a>Метод Иконнектионрекуесткаллбакк:: OnComplete

Метод **OnComplete** уведомляет приложение о завершении ранее запланированного запроса подключения или отключения к устройству MTP/Bluetooth

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



 

## <a name="remarks"></a>Комментарии

Приложение реализует интерфейс [**иконнектионрекуесткаллбакк**](iconnectionrequestcallback.md) для получения уведомлений о завершенных запросах и отмены ожидающих запросов.

Портативные устройства Windows (WPD) вызывают этот метод, чтобы уведомить приложение о завершении ранее запланированного запроса. Каждый запрос можно относить и отменять с помощью обратного вызова, предоставленного приложением. Поэтому, если приложению нужно отправить несколько запросов одновременно с помощью одного и того же объекта [**ипортабледевицеконнектор**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector) , каждому запросу должен быть передан уникальный объект [**иконнектионрекуесткаллбакк**](iconnectionrequestcallback.md) в качестве входного параметра для методов [**Ипортабледевицеконнектор:: Connect**](/windows/desktop/api/portabledeviceconnectapi/nf-portabledeviceconnectapi-iportabledeviceconnector-connect) и [**ипортабледевицеконнектор::D соединения**](/windows/desktop/api/portabledeviceconnectapi/nf-portabledeviceconnectapi-iportabledeviceconnector-disconnect) .

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

[**иконнектионрекуесткаллбакк**](iconnectionrequestcallback.md)
</dt> </dl>

 

 




