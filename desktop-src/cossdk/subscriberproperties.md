---
description: Содержит объект для каждого свойства подписчика для родительской коллекции Субскриптионсфоркомпонент.
ms.assetid: 58c9edbd-1128-4b8c-bb5a-528c212aa6a7
title: Коллекция Субскриберпропертиес
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SubscriberProperties
api_type:
- COM
api_location: ''
ms.openlocfilehash: 7c7a563e3fd3e917812426e34debd87bfd534b46
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895738"
---
# <a name="subscriberproperties-collection"></a>Коллекция Субскриберпропертиес

Содержит объект для каждого свойства подписчика для родительской коллекции [**субскриптионсфоркомпонент**](subscriptionsforcomponent.md) .

Эта коллекция поддерживает методы [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) и [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) объекта [**комадминкаталогколлектион**](comadmincatalogcollection.md) .

## <a name="members"></a>Элементы

Коллекция **субскриберпропертиес** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , но не содержит дополнительных элементов.

## <a name="related-collections"></a>Связанные коллекции

Можно переходить от этой коллекции к любой из следующих коллекций:

-   [**ErrorInfo**](errorinfo.md)
-   [**PropertyInfo**](propertyinfo.md)
-   [**релатедколлектионинфо**](relatedcollectioninfo.md)

Вы можете переходить к этой коллекции из следующих коллекций:

-   [**субскриптионсфоркомпонент**](subscriptionsforcomponent.md)

## <a name="properties"></a>Свойства

Объект [**комадминкаталогобжект**](comadmincatalogobject.md) в коллекции поддерживает следующие свойства:

-   [Name](#name)
-   [Значение](#value)

### <a name="name"></a>Имя



| Ввод | Значение |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Описание    | Имя свойства. Лишние пробелы в начале и конце строки удаляются. Это свойство возвращается при вызове метода свойства [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) или [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) для объекта этой коллекции. |
| Access         | Флагом writeonce                                                                                                                                                                                                                                                              |
| Тип           | Строка                                                                                                                                                                                                                                                                 |
| По умолчанию        | "Создать свойство"                                                                                                                                                                                                                                                         |
| Минимальная система | Windows 2000                                                                                                                                                                                                                                                           |



 

### <a name="value"></a>Значение



| Ввод | Значение |
|----------------|---------------------------|
| Описание    | Значение для свойства. |
| Access         | ReadWrite                 |
| Тип           | Variant                   |
| Значение по умолчанию        | Н/Д                       |
| Минимальная система | Windows 2000              |



 

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Коллекции администрирования COM+](com--administration-collections.md)
</dt> </dl>

 

 
