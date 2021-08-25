---
description: Метод ChangeType преобразует все элементы в коллекции в указанный объект VARTYPE.
ms.assetid: b01b6205-c900-4b2e-810f-426e1e71a008
title: 'Метод Ипортабледевицепропвариантколлектион:: ChangeType (Портабледевицетипес. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDevicePropVariantCollection.ChangeType
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: f32670883981abdac56d46424d8ff18d82cf9fbe0e8a3d2222efede797ffb43d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119839334"
---
# <a name="iportabledevicepropvariantcollectionchangetype-method"></a>Метод Ипортабледевицепропвариантколлектион:: ChangeType

Метод **ChangeType** преобразует все элементы в коллекции в указанный объект VarType.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT ChangeType(
  [in] const VARTYPE vt
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*VT* \[ окне\]
</dt> <dd>

Указывает объект **VarType** , для которого необходимо преобразовать все элементы в коллекции. Примерами типов являются VT \_ UI4 и VT \_ UI8.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Метод возвращает **значение HRESULT**. Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.



| Код возврата                                                                          | Описание                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl> | Метод выполнен успешно.<br/> |



 

## <a name="remarks"></a>Remarks

Если этот метод завершается с ошибкой, коллекция может остаться в промежуточном состоянии, при этом некоторые члены преобразовываются и некоторые из них не преобразовываются.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>Портабледевицетипес. h</dt> </dl>   |
| Библиотека<br/> | <dl> <dt>Портабледевицегуидс. lib</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Интерфейс Ипортабледевицепропвариантколлектион**](iportabledevicepropvariantcollection.md)
</dt> </dl>

 

 




