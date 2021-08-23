---
description: 'Метод Ипортабледевицепропвариантколлектион:: GetAt — метод GetAt извлекает элемент из коллекции по индексу, начинающимся с нуля.'
ms.assetid: c7119ba6-e6fc-4cb6-a8ab-3bf7b6bfe850
title: 'Метод Ипортабледевицепропвариантколлектион:: GetAt (Портабледевицетипес. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDevicePropVariantCollection.GetAt
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 02fa273b3bedea78884e15d2dedb5b7d2f675c78330c735e3bfb1896bc9d5199
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118963733"
---
# <a name="iportabledevicepropvariantcollectiongetat-method"></a>Метод Ипортабледевицепропвариантколлектион:: GetAt

Метод **GetAt** извлекает элемент из коллекции по индексу, начинающимся с нуля.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetAt(
  [in]  const DWORD       dwIndex,
  [out]       PROPVARIANT *pValue
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*двиндекс* \[ окне\]
</dt> <dd>

Значение **типа DWORD** , содержащее Отсчитываемый от нуля индекс извлекаемого элемента.

</dd> <dt>

*pValue* \[ заполняет\]
</dt> <dd>

Указатель на структуру **пропвариант** . Вызывающий объект отвечает за освобождение этой памяти путем вызова **пропвариантклеар**.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Метод возвращает **значение HRESULT**. Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.



| Код возврата                                                                                  | Описание                                               |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>         | Метод выполнен успешно.<br/>                          |
| <dl> <dt>**\_указатель E**</dt> </dl>    | Обязательный аргумент-указатель имеет **значение NULL**.<br/>      |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Переданный индекс был вне допустимого диапазона.<br/> |



 

## <a name="examples"></a>Примеры

Пример использования этого метода см. [в статье получение функциональных категорий, поддерживаемых устройством](retrieving-the-functional-categories-supported-by-a-device.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>Портабледевицетипес. h</dt> </dl>   |
| Библиотека<br/> | <dl> <dt>Портабледевицегуидс. lib</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейс Ипортабледевицепропвариантколлектион**](iportabledevicepropvariantcollection.md)
</dt> <dt>

[Получение идентификатора объекта из постоянного уникального идентификатора](retrieving-an-object-identifier-from-a-persistent-unique-identifier.md)
</dt> <dt>

[Получение поддерживаемых событий службы](retrieving-supported-events.md)
</dt> <dt>

[Получение поддерживаемых форматов службы](retrieving-supported-formats.md)
</dt> <dt>

[Получение поддерживаемых методов службы](retrieving-supported-methods.md)
</dt> <dt>

[Получение типов содержимого, поддерживаемых устройством](retrieving-the-content-types-supported-by-a-device.md)
</dt> <dt>

[Получение функциональных категорий, поддерживаемых устройством](retrieving-the-functional-categories-supported-by-a-device.md)
</dt> <dt>

[Получение идентификаторов функциональных объектов для устройства](retrieving-the-functional-object-identifiers-for-a-device.md)
</dt> <dt>

[Получение возможностей отрисовки, поддерживаемых устройством](retrieving-the-rendering-capabilities-supported-by-a-device.md)
</dt> <dt>

[Задание свойств для нескольких объектов](setting-properties-for-multiple-objects.md)
</dt> </dl>

 

 




