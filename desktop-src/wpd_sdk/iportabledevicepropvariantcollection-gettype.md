---
description: Метод GetType Извлекает тип данных элементов в коллекции.
ms.assetid: 2e389090-74ef-47af-9490-a4820d925246
title: 'Метод Ипортабледевицепропвариантколлектион:: GetType (Портабледевицетипес. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDevicePropVariantCollection.GetType
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 0c29e47cd08b5c31012df92ca04e018d38f7adb7f8802ec534682289852f518b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118963743"
---
# <a name="iportabledevicepropvariantcollectiongettype-method"></a>Метод Ипортабледевицепропвариантколлектион:: GetType

Метод **GetType** Извлекает тип данных элементов в коллекции.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetType(
  [out] VARTYPE *pvt
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ПВТ* \[ заполняет\]
</dt> <dd>

Значение перечисления **VarType** SDK платформы, указывающее тип данных всех элементов в коллекции.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Метод возвращает **значение HRESULT**. Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.



| Код возврата                                                                               | Описание                                          |
|-------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>      | Метод выполнен успешно.<br/>                     |
| <dl> <dt>**\_указатель E**</dt> </dl> | Обязательный аргумент-указатель имеет **значение NULL**.<br/> |



 

## <a name="remarks"></a>Remarks

Все элементы, хранящиеся в **ипортабледевицепропвариантколлектион** , имеют один и тот же тип.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>Портабледевицетипес. h</dt> </dl>   |
| Библиотека<br/> | <dl> <dt>Портабледевицегуидс. lib</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейс Ипортабледевицепропвариантколлектион**](iportabledevicepropvariantcollection.md)
</dt> </dl>

 

 




