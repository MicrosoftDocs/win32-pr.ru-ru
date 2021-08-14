---
description: Коллекция Усерсинроле — содержит объект для каждого пользователя в роли, к которой относится коллекция.
ms.assetid: e7d9e5e8-1927-42b2-bdd5-0c49a562c31f
title: Коллекция Усерсинроле
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UsersInRole
api_type:
- COM
api_location: ''
ms.openlocfilehash: 21927605b2ac303ec0f568e0648a1f16b04be1c5aa1e7ab44d93f04efae55f6b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119372544"
---
# <a name="usersinrole-collection"></a>Коллекция Усерсинроле

Содержит объект для каждого пользователя в роли, к которой относится коллекция.

Эта коллекция поддерживает методы [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) и [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) объекта [**комадминкаталогколлектион**](comadmincatalogcollection.md) .

## <a name="members"></a>Элементы

Коллекция **усерсинроле** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , но не содержит дополнительных элементов.

## <a name="related-collections"></a>Связанные коллекции

Можно переходить от этой коллекции к любой из следующих коллекций:

-   [**ErrorInfo**](errorinfo.md)
-   [**PropertyInfo**](propertyinfo.md)
-   [**релатедколлектионинфо**](relatedcollectioninfo.md)

Вы можете переходить к этой коллекции из следующих коллекций:

-   [**Роли**](roles.md)

## <a name="properties"></a>Свойства

Объект [**комадминкаталогобжект**](comadmincatalogobject.md) в коллекции поддерживает следующие свойства:

-   [Пользователь](#usersinrole-collection)

### <a name="user"></a>User



| Ввод | Значение |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Описание    | Имя пользователя. Это свойство возвращается при вызове метода свойства [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) или [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) для объекта этой коллекции. |
| Доступ         | Флагом writeonce                                                                                                                                                                             |
| Тип           | Строка                                                                                                                                                                                |
| По умолчанию        | "Новый пользователь"                                                                                                                                                                            |
| Минимальная система | Windows 2000                                                                                                                                                                          |



 

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Коллекции администрирования COM+](com--administration-collections.md)
</dt> </dl>

 

 
