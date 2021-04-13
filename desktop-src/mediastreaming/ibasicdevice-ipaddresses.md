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
ms.openlocfilehash: 0623b6e2e5d96cb0a400ab1e820424b7eecf46c9
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104411772"
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

 

 





