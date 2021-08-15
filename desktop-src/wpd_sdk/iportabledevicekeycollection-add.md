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
ms.openlocfilehash: 6aa28a7a8a6439f27a095033d35e8b066c1488af13d1ade921f16c4143843adf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118194724"
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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>Портабледевицетипес. h</dt> </dl>   |
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

 

 




