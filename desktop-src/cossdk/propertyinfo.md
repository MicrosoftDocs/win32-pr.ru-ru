---
description: Извлекает сведения о свойствах, поддерживаемых указанной коллекцией.
ms.assetid: 5e3963c0-6769-4b5b-8636-2d8c98a8776b
title: Коллекция PropertyInfo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PropertyInfo
api_type:
- COM
api_location: ''
ms.openlocfilehash: cf5c354711ec9ca34af1809707a7a869d39a3026ca5cb7ca11d2245c02be049b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118547610"
---
# <a name="propertyinfo-collection"></a>Коллекция PropertyInfo

Извлекает сведения о свойствах, поддерживаемых указанной коллекцией. Коллекция **PropertyInfo** доступна из любого объекта [**комадминкаталогколлектион**](comadmincatalogcollection.md) с помощью метода [**IsCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) . Коллекция **PropertyInfo** содержит по одному объекту для каждого свойства, которое поддерживается исходной коллекцией.

## <a name="members"></a>Элементы

Коллекция **PropertyInfo** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , но не содержит дополнительных элементов.

## <a name="related-collections"></a>Связанные коллекции

Можно переходить от этой коллекции к любой из следующих коллекций:

-   **PropertyInfo**
-   [**релатедколлектионинфо**](relatedcollectioninfo.md)

Можно переходить к этой коллекции из каждой коллекции.

## <a name="properties"></a>Свойства

Объект [**комадминкаталогобжект**](comadmincatalogobject.md) в коллекции поддерживает следующие свойства:

-   [Имя](#name)

### <a name="name"></a>Имя



| Ввод | Значение |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Описание    | Имя свойства. Это свойство возвращается при вызове метода свойства [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) или [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) для объекта этой коллекции. |
| Доступ         | ReadOnly                                                                                                                                                                                         |
| Тип           | Строка                                                                                                                                                                                           |
| По умолчанию        | None                                                                                                                                                                                             |
| Минимальная система | Windows 2000                                                                                                                                                                                     |



 

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Коллекции администрирования COM+](com--administration-collections.md)
</dt> </dl>

 

 
