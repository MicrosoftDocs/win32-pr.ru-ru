---
description: Коллекция Ролесфорпартитион всегда связана с объектом в коллекции секций. Он содержит объект для каждой роли, назначенной секции, к которой она относится.
ms.assetid: 56985f55-d6e8-4066-b6d5-21c62d4278ce
title: Коллекция Ролесфорпартитион
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RolesForPartition
api_type:
- COM
api_location: ''
ms.openlocfilehash: c97d524e3fc516086db3a815396d6d59f9369b31
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141207"
---
# <a name="rolesforpartition-collection"></a>Коллекция Ролесфорпартитион

Коллекция **ролесфорпартитион** всегда связана с объектом в коллекции [**секций**](partitions.md) . Он содержит объект для каждой роли, назначенной секции, к которой она относится.

Эта коллекция не поддерживает методы [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) и [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) объекта [**комадминкаталогколлектион**](comadmincatalogcollection.md) .

## <a name="members"></a>Элементы

Коллекция **ролесфорпартитион** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , но не содержит дополнительных элементов.

## <a name="related-collections"></a>Связанные коллекции

Можно переходить от этой коллекции к любой из следующих коллекций:

-   [**ErrorInfo**](errorinfo.md)
-   [**PropertyInfo**](propertyinfo.md)
-   [**релатедколлектионинфо**](relatedcollectioninfo.md)
-   [**усерсинпартитионроле**](usersinpartitionrole.md)

Вы можете переходить к этой коллекции из следующих коллекций:

-   [**Секции**](partitions.md)

## <a name="properties"></a>Свойства

Объект [**комадминкаталогобжект**](comadmincatalogobject.md) в коллекции поддерживает следующие свойства:

-   [Описание](#description)
-   [Имя](#name)

### <a name="description"></a>Описание



| Ввод | Значение |
|----------------|----------------------------|
| Описание    | Описание роли. |
| Access         | ReadOnly                   |
| Тип           | Строка                     |
| По умолчанию        | ""                         |
| Минимальная система | Windows Server 2003        |



 

### <a name="name"></a>Имя



| Ввод | Значение |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Описание    | Имя роли. Лишние пробелы в начале и конце строки удаляются. Это свойство возвращается при вызове метода свойства [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) или [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) для объекта этой коллекции. |
| Access         | ReadOnly                                                                                                                                                                                                                                                    |
| Тип           | Строка                                                                                                                                                                                                                                                      |
| По умолчанию        | ""                                                                                                                                                                                                                                                          |
| Минимальная система | Windows Server 2003                                                                                                                                                                                                                                         |



 

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Коллекции администрирования COM+](com--administration-collections.md)
</dt> </dl>

 

 
