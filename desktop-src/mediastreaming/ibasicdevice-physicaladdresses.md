---
title: Ибасикдевице Фисикаладдрессес, метод
description: Возвращает вектор физических адресов.
ms.assetid: 85F48EE3-14A1-46DA-A3C3-F94A8A43CF92
keywords:
- API потоковой передачи мультимедиа метода Фисикаладдрессес
- API потоковой передачи мультимедиа метода Фисикаладдрессес, интерфейс Ибасикдевице
- API потоковой передачи мультимедиа интерфейса Ибасикдевице, метод Фисикаладдрессес
topic_type:
- apiref
api_name:
- IBasicDevice.PhysicalAddresses
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2f1cd87435c78e1f6877d1bb6afd1b38981b05dc
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104333891"
---
# <a name="ibasicdevicephysicaladdresses-method"></a>Ибасикдевице: метод:P Хисикаладдрессес

Возвращает вектор физических адресов.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT PhysicalAddresses(
  [out] IVector< HSTRING > **value
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*значение* \[ заполняет\]
</dt> <dd>

Получает перечисляемую коллекцию указателей на физические адреса.

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

 

 





