---
title: Ибасикдевице IpAddresses, метод
description: Возвращает вектор IP-адресов.
ms.assetid: F48B91DC-3AE2-462F-835B-292BF86904B3
keywords:
- API потоковой передачи мультимедиа метода IpAddresses
- API потоковой передачи мультимедиа метода IpAddresses, интерфейс Ибасикдевице
- API потоковой передачи мультимедиа интерфейса Ибасикдевице, метод IpAddresses
topic_type:
- apiref
api_name:
- IBasicDevice.IpAddresses
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: dc997abb24c007e9e3e4d5c8028762daaca20e434ca4e3ab22fb278f567f998c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119847684"
---
# <a name="ibasicdeviceipaddresses-method"></a>Метод Ибасикдевице:: IpAddresses

Возвращает вектор IP-адресов.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT IpAddresses(
  [out] IVector< HSTRING > **value
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*значение* \[ заполняет\]
</dt> <dd>

Получает перечисляемую коллекцию указателей на IP-адреса.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Метод возвращает **значение HRESULT**. Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.



| Код возврата                                                                          | Описание                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl> | Метод выполнен успешно.<br/> |



 

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ибасикдевице**](ibasicdevice.md)
</dt> </dl>

 

 





