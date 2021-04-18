---
description: Интерфейс Ипортабледевицепропвариантколлектион содержит коллекцию индексированных значений ПРОПВАРИАНТ для одного и того же объекта VARTYPE.
ms.assetid: 41224958-a5a0-4e09-8733-d0ae036f68b9
title: Интерфейс Ипортабледевицепропвариантколлектион (Портабледевицетипес. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDevicePropVariantCollection
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 14ba07894c74567487704bb1f63e7242542af313
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105717873"
---
# <a name="iportabledevicepropvariantcollection-interface"></a>Интерфейс Ипортабледевицепропвариантколлектион

Интерфейс **ипортабледевицепропвариантколлектион** содержит коллекцию индексированных значений **пропвариант** для одного и того же объекта VarType. VARTYPE первого элемента, добавляемого в коллекцию, определяет VARTYPE коллекции. Попытка добавить элемент другого объекта VARTYPE может завершиться ошибкой, если значение **пропвариант** не может быть изменено на текущую VarType коллекции. Чтобы изменить VARTYPE коллекции, вызовите метод **ChangeType**.

Этот интерфейс можно получить из метода или, если требуется новый объект, вызовите **CREATE** с помощью **CLSID \_ портабледевицепропвариантколлектион**.

## <a name="members"></a>Элементы

Интерфейс **ипортабледевицепропвариантколлектион** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **Ипортабледевицепропвариантколлектион** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **ипортабледевицепропвариантколлектион** содержит следующие методы.



| Метод                                                                | Описание                                                                         |
|:----------------------------------------------------------------------|:------------------------------------------------------------------------------------|
| [**Включить**](iportabledevicepropvariantcollection-add.md)               | Добавляет элемент в коллекцию.<br/>                                          |
| [**ChangeType**](iportabledevicepropvariantcollection-changetype.md) | Преобразует все элементы в коллекции в указанный объект VARTYPE.<br/>           |
| [**Открытым**](iportabledevicepropvariantcollection-clear.md)           | Освобождает, а затем удаляет все элементы из коллекции.<br/>                  |
| [**GetAt**](iportabledevicepropvariantcollection-getat.md)           | Извлекает элемент из коллекции по индексу, начинающимся с нуля.<br/>             |
| [**GetCount**](iportabledevicepropvariantcollection-getcount.md)     | Возвращает число элементов в этой коллекции.<br/>                        |
| [**GetType**](iportabledevicepropvariantcollection-gettype.md)       | Возвращает тип данных элементов коллекции.<br/>                  |
| [**RemoveAt**](iportabledevicepropvariantcollection-removeat.md)     | Удаляет элемент, хранящийся в расположении, указанном заданным индексом.<br/> |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Портабледевицетипес. h</dt> </dl>   |
| Библиотека<br/> | <dl> <dt>Портабледевицегуидс. lib</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейсы коллекции**](collection-interfaces.md)
</dt> </dl>

 

