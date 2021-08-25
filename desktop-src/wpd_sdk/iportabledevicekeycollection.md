---
description: Интерфейс Ипортабледевицекэйколлектион содержит коллекцию значений PROPERTYKEY. Этот интерфейс можно получить из метода или, если требуется новый объект, вызовите Create с помощью CLSID \_ портабледевицекэйколлектион.
ms.assetid: 2460f5bc-6b1c-4e3b-bdb9-faaa6d6c87fd
title: Интерфейс Ипортабледевицекэйколлектион (Портабледевицетипес. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceKeyCollection
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 0f648020ddb82db2a619f75bb125e94c7679f8dd3061ac282fcc0f911a498a77
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119839394"
---
# <a name="iportabledevicekeycollection-interface"></a>Интерфейс Ипортабледевицекэйколлектион

Интерфейс **ипортабледевицекэйколлектион** содержит коллекцию значений **PROPERTYKEY** . Этот интерфейс можно получить из метода или, если требуется новый объект, вызовите **CREATE** с помощью **CLSID \_ портабледевицекэйколлектион**.

## <a name="members"></a>Элементы

Интерфейс **ипортабледевицекэйколлектион** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **Ипортабледевицекэйколлектион** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **ипортабледевицекэйколлектион** содержит следующие методы.



| Метод                                                    | Описание                                                                         |
|:----------------------------------------------------------|:------------------------------------------------------------------------------------|
| [**Включить**](iportabledevicekeycollection-add.md)           | Добавляет ключ свойства в коллекцию.<br/>                                   |
| [**Clear**](iportabledevicekeycollection-clear.md)       | Удаляет все элементы из коллекции.<br/>                                   |
| [**GetAt**](iportabledevicekeycollection-getat.md)       | Извлекает **PROPERTYKEY** из коллекции по индексу.<br/>                |
| [**GetCount**](iportabledevicekeycollection-getcount.md) | Возвращает число ключей в этой коллекции.<br/>                         |
| [**RemoveAt**](iportabledevicekeycollection-removeat.md) | Удаляет элемент, хранящийся в расположении, указанном заданным индексом.<br/> |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>Портабледевицетипес. h</dt> </dl>   |
| Библиотека<br/> | <dl> <dt>Портабледевицегуидс. lib</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейсы коллекции**](collection-interfaces.md)
</dt> </dl>

 

