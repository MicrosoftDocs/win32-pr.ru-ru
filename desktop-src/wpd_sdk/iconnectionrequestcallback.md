---
description: Определяет один метод обратного вызова.
ms.assetid: 579f7a29-cd98-4d97-9f8e-9b786897df1c
title: Интерфейс Иконнектионрекуесткаллбакк (Девпкэй. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IConnectionRequestCallback
api_type:
- COM
api_location:
- PortableDeviceGuids.lib
- PortableDeviceGuids.dll
ms.openlocfilehash: aca827de068ce221f013f03b35f88fd76a030dd4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999608"
---
# <a name="iconnectionrequestcallback-interface"></a>Интерфейс Иконнектионрекуесткаллбакк

Интерфейс **иконнектионрекуесткаллбакк** определяет один метод обратного вызова. Приложение для переносных устройств Windows (WPD) реализует этот необязательный интерфейс модели COM для получения уведомлений о завершенных запросах и отмене ожидающих запросов. Запросы отправляются с помощью методов [**ипортабледевицеконнектор:: Connect**](/windows/desktop/api/portabledeviceconnectapi/nf-portabledeviceconnectapi-iportabledeviceconnector-connect) и [**ипортабледевицеконнектор::D соединения**](/windows/desktop/api/portabledeviceconnectapi/nf-portabledeviceconnectapi-iportabledeviceconnector-disconnect) .

## <a name="members"></a>Элементы

Интерфейс **иконнектионрекуесткаллбакк** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **Иконнектионрекуесткаллбакк** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **иконнектионрекуесткаллбакк** содержит следующие методы.



| Метод                                                      | Описание                                                                           |
|:------------------------------------------------------------|:--------------------------------------------------------------------------------------|
| [**OnComplete**](iconnectionrequestcallback-oncomplete.md) | Уведомляет приложение о завершении ранее запланированного запроса.<br/> |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 7\]<br/>                                                                                                                             |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                                                                              |
| Header<br/>                   | <dl> <dt>Девпкэй. h; </dt> <dt>Портабледевицеконнектапи. h</dt> </dl> |
| IDL<br/>                      | <dl> <dt>Портабледевицеконнектапи. idl</dt> </dl>                                                                |
| Библиотека<br/>                  | <dl> <dt>Портабледевицегуидс. lib</dt> </dl>                                                                     |



 

