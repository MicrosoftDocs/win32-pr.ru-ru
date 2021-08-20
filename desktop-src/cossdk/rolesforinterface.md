---
description: Содержит объект для каждой роли, назначенной интерфейсу, к которому относится коллекция. Роли уже должны быть назначены на уровне приложения.
ms.assetid: f5c1dc9a-13da-4504-a244-4ce8058240b8
title: Коллекция Ролесфоринтерфаце
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RolesForInterface
api_type:
- COM
api_location: ''
ms.openlocfilehash: 296a024f81973436898b5e7ca226467583b0ba103d6ceff9fb74d9fe330e626c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117915955"
---
# <a name="rolesforinterface-collection"></a>Коллекция Ролесфоринтерфаце

Содержит объект для каждой роли, назначенной интерфейсу, к которому относится коллекция. Роли уже должны быть назначены на уровне приложения.

Эта коллекция поддерживает методы [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) и [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) объекта [**комадминкаталогколлектион**](comadmincatalogcollection.md) .

## <a name="members"></a>Элементы

Коллекция **ролесфоринтерфаце** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , но не содержит дополнительных элементов.

## <a name="related-collections"></a>Связанные коллекции

Можно переходить от этой коллекции к любой из следующих коллекций:

-   [**ErrorInfo**](errorinfo.md)
-   [**PropertyInfo**](propertyinfo.md)
-   [**релатедколлектионинфо**](relatedcollectioninfo.md)

Вы можете переходить к этой коллекции из следующих коллекций:

-   [**интерфацесфоркомпонент**](interfacesforcomponent.md)

## <a name="properties"></a>Свойства

Объект [**комадминкаталогобжект**](comadmincatalogobject.md) в коллекции поддерживает следующие свойства:

-   [Имя](#name)

### <a name="name"></a>Имя



| Ввод | Значение |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Описание:    | Имя роли. Уже должна быть назначена приложению роли (отображается в коллекции ролей). Лишние пробелы в начале и конце строки удаляются. Это свойство возвращается при вызове метода свойства [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) или [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) для объекта этой коллекции. |
| Доступ         | Флагом writeonce                                                                                                                                                                                                                                                                                                                                           |
| Тип           | Строка                                                                                                                                                                                                                                                                                                                                              |
| По умолчанию        | "Создать роль"                                                                                                                                                                                                                                                                                                                                          |
| Минимальная система | Windows 2000                                                                                                                                                                                                                                                                                                                                        |



 

## <a name="see-also"></a>См. также

<dl> <dt>

[Коллекции администрирования COM+](com--administration-collections.md)
</dt> </dl>

 

 
