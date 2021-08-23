---
description: Извлекает сведения о других коллекциях, связанных с коллекцией, из которой она вызывается.
ms.assetid: daea5b23-6a13-46f4-89c8-0d93b614311e
title: Коллекция Релатедколлектионинфо
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RelatedCollectionInfo
api_type:
- COM
api_location: ''
ms.openlocfilehash: 45e9e0f0e251bc9b0772d5def40fec148d541964d34e4f1dda954825f456468b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119637094"
---
# <a name="relatedcollectioninfo-collection"></a>Коллекция Релатедколлектионинфо

Извлекает сведения о других коллекциях, связанных с коллекцией, из которой она вызывается. Коллекция **релатедколлектионинфо** доступна из любого объекта [**комадминкаталогколлектион**](comadmincatalogcollection.md) с помощью метода [**IsCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) . Коллекция **релатедколлектионинфо** содержит по одному объекту для каждой коллекции, доступной из исходной коллекции. Связанные коллекции соответствуют иерархии коллекции средств администрирования служб компонентов.

Эта коллекция не поддерживает методы [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) и [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) объекта [**комадминкаталогколлектион**](comadmincatalogcollection.md) .

## <a name="members"></a>Элементы

Коллекция **релатедколлектионинфо** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , но не содержит дополнительных элементов.

## <a name="related-collections"></a>Связанные коллекции

Можно переходить от этой коллекции к любой из следующих коллекций:

-   [**PropertyInfo**](propertyinfo.md)
-   **релатедколлектионинфо**

Можно переходить к этой коллекции из каждой коллекции.

## <a name="properties"></a>Свойства

Объект [**комадминкаталогобжект**](comadmincatalogobject.md) в коллекции поддерживает следующие свойства:

-   [Имя](#name)

### <a name="name"></a>Имя



| Ввод | Значение |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Описание    | Имя связанной коллекции. Это свойство возвращается при вызове метода свойства [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) или [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) для объекта этой коллекции. |
| Доступ         | ReadOnly                                                                                                                                                                                                   |
| Тип           | Строка                                                                                                                                                                                                     |
| По умолчанию        | None                                                                                                                                                                                                       |
| Минимальная система | Windows 2000                                                                                                                                                                                               |



 

## <a name="see-also"></a>См. также

<dl> <dt>

[Коллекции администрирования COM+](com--administration-collections.md)
</dt> </dl>

 

 
