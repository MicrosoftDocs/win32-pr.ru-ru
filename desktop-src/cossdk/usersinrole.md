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
ms.openlocfilehash: 1b73c495a1af1dec9114e5a59274e457c1d09694
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105542"
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

### <a name="user"></a>Пользователь



| Ввод | Значение |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Описание    | Имя пользователя. Это свойство возвращается при вызове метода свойства [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) или [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) для объекта этой коллекции. |
| Access         | Флагом writeonce                                                                                                                                                                             |
| Тип           | Строка                                                                                                                                                                                |
| По умолчанию        | "Новый пользователь"                                                                                                                                                                            |
| Минимальная система | Windows 2000                                                                                                                                                                          |



 

## <a name="see-also"></a>См. также

<dl> <dt>

[Коллекции администрирования COM+](com--administration-collections.md)
</dt> </dl>

 

 
