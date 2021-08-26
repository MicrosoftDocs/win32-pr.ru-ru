---
description: Коллекция Roles всегда связана с объектом в коллекции приложений. Он содержит объект для каждой роли, назначенной приложению, к которому он относится.
ms.assetid: 87f39c2a-ad66-4390-9220-06751dcebd95
title: Коллекция ролей
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Roles
api_type:
- COM
api_location: ''
ms.openlocfilehash: 133477d82f718b992a628bde8af58f22d8d50a9e4974816c7c8f56be7ba8e33f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120029474"
---
# <a name="roles-collection"></a>Коллекция ролей

Коллекция **roles** всегда связана с объектом в коллекции [**приложений**](applications.md) . Он содержит объект для каждой роли, назначенной приложению, к которому он относится.

Эта коллекция поддерживает методы [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) и [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) объекта [**комадминкаталогколлектион**](comadmincatalogcollection.md) .

## <a name="members"></a>Элементы

Коллекция **ролей** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , но не содержит дополнительных элементов.

## <a name="related-collections"></a>Связанные коллекции

Можно переходить от этой коллекции к любой из следующих коллекций:

-   [**ErrorInfo**](errorinfo.md)
-   [**PropertyInfo**](propertyinfo.md)
-   [**релатедколлектионинфо**](relatedcollectioninfo.md)
-   [**усерсинроле**](usersinrole.md)

Вы можете переходить к этой коллекции из следующих коллекций:

-   [**Приложения**](applications.md)

## <a name="properties"></a>Свойства

Объект [**комадминкаталогобжект**](comadmincatalogobject.md) в коллекции поддерживает следующие свойства:

-   [Описание](#description)
-   [Имя](#name)

### <a name="description"></a>Описание



| Ввод | Значение |
|----------------|----------------------------|
| Описание    | Описание роли. |
| Доступ         | ReadWrite                  |
| Тип           | Строка                     |
| По умолчанию        | ""                         |
| Минимальная система | Windows 2000               |



 

### <a name="name"></a>Имя



| Ввод | Значение |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Описание    | Имя роли. Лишние пробелы в начале и конце строки удаляются. Это свойство возвращается при вызове метода свойства [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) или [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) для объекта этой коллекции. |
| Доступ         | Флагом writeonce                                                                                                                                                                                                                                                   |
| Тип           | Строка                                                                                                                                                                                                                                                      |
| По умолчанию        | "Создать роль"                                                                                                                                                                                                                                                  |
| Минимальная система | Windows 2000                                                                                                                                                                                                                                                |



 

## <a name="see-also"></a>См. также

<dl> <dt>

[Коллекции администрирования COM+](com--administration-collections.md)
</dt> </dl>

 

 
