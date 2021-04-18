---
description: Интерфейс Ипортабледевицевалуесколлектион содержит коллекцию индексируемых от нуля интерфейсов Ипортабледевицевалуес.
ms.assetid: 8bce9d27-f240-41ec-acf4-fefccdd95e9f
title: Интерфейс Ипортабледевицевалуесколлектион (Портабледевицетипес. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValuesCollection
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: cebe15dc9a4f4347eb58563e9b43240464565a4c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105717778"
---
# <a name="iportabledevicevaluescollection-interface"></a>Интерфейс Ипортабледевицевалуесколлектион

Интерфейс **ипортабледевицевалуесколлектион** содержит коллекцию индексируемых от нуля интерфейсов **ипортабледевицевалуес** . Этот интерфейс можно извлечь из метода или, если требуется новый объект, вызвать **CREATE** с помощью **CLSID \_ портабледевицевалуесколлектион**.

## <a name="members"></a>Элементы

Интерфейс **ипортабледевицевалуесколлектион** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **Ипортабледевицевалуесколлектион** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **ипортабледевицевалуесколлектион** содержит следующие методы.



| Метод                                                       | Описание                                                                         |
|:-------------------------------------------------------------|:------------------------------------------------------------------------------------|
| [**Включить**](iportabledevicevaluescollection-add.md)           | Добавляет элемент в коллекцию.<br/>                                           |
| [**Открытым**](iportabledevicevaluescollection-clear.md)       | Освобождает все элементы из коллекции.<br/>                                  |
| [**GetAt**](iportabledevicevaluescollection-getat.md)       | Извлекает элемент из коллекции по индексу, начинающимся с нуля.<br/>             |
| [**GetCount**](iportabledevicevaluescollection-getcount.md) | Возвращает количество элементов в коллекции.<br/>                         |
| [**RemoveAt**](iportabledevicevaluescollection-removeat.md) | Удаляет элемент, хранящийся в расположении, указанном заданным индексом.<br/> |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Портабледевицетипес. h</dt> </dl>   |
| Библиотека<br/> | <dl> <dt>Портабледевицегуидс. lib</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейсы коллекции**](collection-interfaces.md)
</dt> </dl>

 

