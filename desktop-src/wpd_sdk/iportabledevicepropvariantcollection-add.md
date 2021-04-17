---
description: Метод Add добавляет элемент в коллекцию.
ms.assetid: e9e8975f-f9b8-4940-b967-020cf3812582
title: 'Метод Ипортабледевицепропвариантколлектион:: Add (Портабледевицетипес. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDevicePropVariantCollection.Add
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: d9d5b4ee664d2fbbcc78550b1af5a48874d153d6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708347"
---
# <a name="iportabledevicepropvariantcollectionadd-method"></a>Метод Ипортабледевицепропвариантколлектион:: Add

Метод **Add** добавляет элемент в коллекцию.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Add(
  [in] const PROPVARIANT *pValue
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*pValue* \[ окне\]
</dt> <dd>

Указатель на новый объект **пропвариант** для добавления в коллекцию. Этот метод копирует **пропвариант** в коллекцию, поэтому необходимо освободить локальную копию переменной путем вызова **пропвариантклеар** после вызова этого метода.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Метод возвращает **значение HRESULT**. Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.



| Код возврата                                                                          | Описание                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl> | Метод выполнен успешно.<br/> |



 

## <a name="remarks"></a>Комментарии

Если VARTYPE для *pValue* является VT \_ Vector или VT \_ UI1, установка и извлечение буфера со **значением NULL** или нулевым размером не поддерживается. Например, не допускаются значения pValue. Кауб. Пелемс = **null** или pValue. Кауб. целемс = 0.

Если вызывающий объект пытается добавить элемент другого объекта VARTYPE, содержащегося в коллекции, и значение ПРОПВАРИАНТ не может быть изменено этим интерфейсом автоматически, этот метод завершится ошибкой. Чтобы изменить тип коллекции вручную, вызовите метод [**ипортабледевицепропвариантколлектион:: ChangeType**](iportabledevicepropvariantcollection-changetype.md).

## <a name="examples"></a>Примеры

Пример использования этого метода см. в разделе [Получение идентификатора объекта из постоянного уникального идентификатора](retrieving-an-object-identifier-from-a-persistent-unique-identifier.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Портабледевицетипес. h</dt> </dl>   |
| Библиотека<br/> | <dl> <dt>Портабледевицегуидс. lib</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейс Ипортабледевицепропвариантколлектион**](iportabledevicepropvariantcollection.md)
</dt> <dt>

[Перемещение содержимого на устройстве](moving-content-on-the-device.md)
</dt> <dt>

[Получение идентификатора объекта из постоянного уникального идентификатора](retrieving-an-object-identifier-from-a-persistent-unique-identifier.md)
</dt> </dl>

 

 




