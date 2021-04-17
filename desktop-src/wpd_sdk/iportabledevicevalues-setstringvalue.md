---
description: Метод SetStringValue добавляет новое строковое значение (Type VT \_ LPWSTR) или перезаписывает существующий.
ms.assetid: a6eba2b9-de18-431e-874e-af68695e8d3f
title: 'Метод Ипортабледевицевалуес:: SetStringValue (Портабледевицетипес. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetStringValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 163b5cd81ce8da64fc6d9f4304de5783b248522f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704265"
---
# <a name="iportabledevicevaluessetstringvalue-method"></a>Метод Ипортабледевицевалуес:: SetStringValue

Метод **SetStringValue** добавляет новое строковое значение (Type VT \_ LPWSTR) или перезаписывает существующий.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetStringValue(
  [in] REFPROPERTYKEY key,
  [in] LPCWSTR        Value
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ключ* \[ окне\]
</dt> <dd>

Объект **рефпропертикэй** , указывающий элемент для создания или перезаписи.

</dd> <dt>

*Значение* \[ окне\]
</dt> <dd>

Объект **лпквстр** , указывающий новое значение. Строка копируется, поэтому вызывающий объект может освободить память, выделенную для этого значения, после вызова этого метода.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Метод возвращает **значение HRESULT**. Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.



| Код возврата                                                                          | Описание                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl> | Метод выполнен успешно.<br/> |



 

## <a name="remarks"></a>Комментарии

Любая существующая память ключа будет выпущена соответствующим образом.

## <a name="examples"></a>Примеры

Пример использования этого метода см. в разделе [Указание сведений о клиенте](specifying-client-information.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Портабледевицетипес. h</dt> </dl>   |
| Библиотека<br/> | <dl> <dt>Портабледевицегуидс. lib</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Добавление ресурса в объект](adding-a-resource-to-an-object.md)
</dt> <dt>

[**Интерфейс Ипортабледевицевалуес**](iportabledevicevalues.md)
</dt> <dt>

[**Ипортабледевицевалуес:: GetStringValue**](iportabledevicevalues-getstringvalue.md)
</dt> <dt>

[Задание свойств для одного объекта](setting-properties-for-a-single-object.md)
</dt> <dt>

[Задание свойств для нескольких объектов](setting-properties-for-multiple-objects.md)
</dt> <dt>

[Указание сведений о клиенте](specifying-client-information.md)
</dt> <dt>

[Запись свойств содержимого объекта](writing-content-object-properties.md)
</dt> </dl>

 

 




