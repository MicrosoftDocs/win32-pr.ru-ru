---
description: Содержит объект для каждого пользователя секции.
ms.assetid: baec56ae-be8a-42a7-90bc-1db7c5cd7fe2
title: Коллекция Партитионусерс
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PartitionUsers
api_type:
- COM
api_location: ''
ms.openlocfilehash: 1521642879037938451decd873a9aa14211ce296
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701267"
---
# <a name="partitionusers-collection"></a>Коллекция Партитионусерс

Содержит объект для каждого пользователя секции.

Эта коллекция поддерживает методы [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) и [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) объекта [**комадминкаталогколлектион**](comadmincatalogcollection.md) .

## <a name="members"></a>Элементы

Коллекция **партитионусерс** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , но не содержит дополнительных элементов.

## <a name="related-collections"></a>Связанные коллекции

Можно переходить от этой коллекции к любой из следующих коллекций:

-   [**ErrorInfo**](errorinfo.md)
-   [**PropertyInfo**](propertyinfo.md)
-   [**релатедколлектионинфо**](relatedcollectioninfo.md)

Вы можете переходить к этой коллекции из следующих коллекций:

-   [**Корневой**](root.md)

## <a name="properties"></a>Свойства

Объект [**комадминкаталогобжект**](comadmincatalogobject.md) в коллекции поддерживает следующие свойства:

-   [AccountName](#accountname)
-   [дефаултпартитионид](#defaultpartitionid)

### <a name="accountname"></a>AccountName



| Ввод | Значение |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Описание    | Имя учетной записи пользователя раздела. Это свойство возвращается при вызове метода свойства [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) или [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) для объекта этой коллекции. |
| Access         | Флагом writeonce                                                                                                                                                                                                    |
| Тип           | Строка                                                                                                                                                                                                       |
| По умолчанию        | "Новый пользователь"                                                                                                                                                                                                   |
| Минимальная система | Windows Server 2003                                                                                                                                                                                          |



 

### <a name="defaultpartitionid"></a>дефаултпартитионид



| Ввод | Значение |
|----------------|--------------------------------------------------------------------|
| Описание    | Глобальный уникальный идентификатор базового раздела приложения. |
| Access         | ReadWrite                                                          |
| Тип           | Строка                                                             |
| По умолчанию        | {41E90F3E-56C1-4633-81C3-6E8BAC8BDD70}                             |
| Минимальная система | Windows Server 2003                                                |



 

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Коллекции администрирования COM+](com--administration-collections.md)
</dt> </dl>

 

 
