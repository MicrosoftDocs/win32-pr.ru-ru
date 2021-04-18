---
description: Метод Add добавляет ключ свойства в коллекцию.
ms.assetid: 640ef1c4-2843-48dd-a30a-9a2ef9de35b9
title: 'Метод Ипортабледевицекэйколлектион:: Add (Портабледевицетипес. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceKeyCollection.Add
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: e43fea25a08969b2ae8169884d51ddc46f8c7136
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718107"
---
# <a name="iportabledevicekeycollectionadd-method"></a>Метод Ипортабледевицекэйколлектион:: Add

Метод **Add** добавляет ключ свойства в коллекцию.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Add(
  [in] REFPROPERTYKEY Key
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Ключ* \[ окне\]
</dt> <dd>

Объект **рефпропертикэй** , добавляемый в коллекцию. Этот метод копирует ключ в коллекцию, чтобы можно было освободить локальную переменную после вызова этого метода.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Метод возвращает **значение HRESULT**. Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.



| Код возврата                                                                                   | Описание                                                                       |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>          | Метод выполнен успешно.<br/>                                                  |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Недостаточно памяти для добавления ключа в коллекцию.<br/> |



 

## <a name="examples"></a>Примеры

Пример использования этого метода см. в разделе [Получение свойств для одного объекта](retrieving-properties-for-a-single-object.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Портабледевицетипес. h</dt> </dl>   |
| Библиотека<br/> | <dl> <dt>Портабледевицегуидс. lib</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейс Ипортабледевицекэйколлектион**](iportabledevicekeycollection.md)
</dt> <dt>

[Получение свойств содержимого объекта](retrieving-content-object-properties.md)
</dt> <dt>

[Получение свойств для одного объекта](retrieving-properties-for-a-single-object.md)
</dt> <dt>

[Получение возможностей отрисовки, поддерживаемых устройством](retrieving-the-rendering-capabilities-supported-by-a-device.md)
</dt> </dl>

 

 




