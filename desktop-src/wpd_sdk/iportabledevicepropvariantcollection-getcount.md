---
description: Метод NOCOUNT извлекает количество элементов в этой коллекции.
ms.assetid: b7c8acd2-67f2-47d3-b42a-26aa701fd613
title: 'Метод Ипортабледевицепропвариантколлектион:: NOCOUNT (Портабледевицетипес. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDevicePropVariantCollection.GetCount
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: d3a06cb5d89bc09a35a58f9269ba19c488c11e0f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105721017"
---
# <a name="iportabledevicepropvariantcollectiongetcount-method"></a>Метод Ипортабледевицепропвариантколлектион:: NOCOUNT

Метод **NOCOUNT** извлекает количество элементов в этой коллекции.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetCount(
  [in] DWORD *pcElems
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пцелемс* \[ окне\]
</dt> <dd>

Указатель на **DWORD** , содержащий число элементов в коллекции.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Метод возвращает **значение HRESULT**. Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.



| Код возврата                                                                               | Описание                                          |
|-------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>      | Метод выполнен успешно.<br/>                     |
| <dl> <dt>**\_указатель E**</dt> </dl> | Обязательный аргумент-указатель имеет **значение NULL**.<br/> |



 

## <a name="examples"></a>Примеры

Пример использования этого метода см. [в статье получение функциональных категорий, поддерживаемых устройством](retrieving-the-functional-categories-supported-by-a-device.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Портабледевицетипес. h</dt> </dl>   |
| Библиотека<br/> | <dl> <dt>Портабледевицегуидс. lib</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейс Ипортабледевицепропвариантколлектион**](iportabledevicepropvariantcollection.md)
</dt> <dt>

[Получение поддерживаемых событий службы](retrieving-supported-events.md)
</dt> <dt>

[Получение поддерживаемых форматов службы](retrieving-supported-formats.md)
</dt> <dt>

[Получение поддерживаемых методов службы](retrieving-supported-methods.md)
</dt> <dt>

[Получение функциональных категорий, поддерживаемых устройством](retrieving-the-functional-categories-supported-by-a-device.md)
</dt> <dt>

[Задание свойств для нескольких объектов](setting-properties-for-multiple-objects.md)
</dt> </dl>

 

 




