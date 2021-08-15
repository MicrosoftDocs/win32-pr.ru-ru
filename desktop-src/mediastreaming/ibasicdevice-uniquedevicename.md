---
title: Ибасикдевице Уникуедевиценаме, метод
description: Извлекает уникальное имя устройства (УДН) устройства.
ms.assetid: 393EFF96-69E1-4081-905D-D8CC47B5FC4A
keywords:
- API потоковой передачи мультимедиа метода Уникуедевиценаме
- API потоковой передачи мультимедиа метода Уникуедевиценаме, интерфейс Ибасикдевице
- API потоковой передачи мультимедиа интерфейса Ибасикдевице, метод Уникуедевиценаме
topic_type:
- apiref
api_name:
- IBasicDevice.UniqueDeviceName
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7b70fbc2021cf717cdb49d8a222aa33ad4e9213f297364b81af065c3bbeaed99
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972323"
---
# <a name="ibasicdeviceuniquedevicename-method"></a>Метод Ибасикдевице:: Уникуедевиценаме

Извлекает уникальное имя устройства (УДН) устройства.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT UniqueDeviceName(
  [out] HSTRING *value
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*значение* \[ заполняет\]
</dt> <dd>

Получает указатель на УДН модель устройства.

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

 

 





