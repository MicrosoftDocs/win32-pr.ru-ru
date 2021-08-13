---
description: Содержит список внутрипроцессного серверов, зарегистрированных в системе для 32-разрядных компонентов на 64-разрядных компьютерах. Он содержит объект для каждого компонента.
ms.assetid: 4dbcf059-b09b-4a65-95c9-3a4735c252c3
title: Коллекция Вовинпроксерверс
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WOWInprocServers
api_type:
- COM
api_location: ''
ms.openlocfilehash: d85abf322d34d03c0f5e8863b5434343946b676e477e18077c82d83de78cafb5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118545575"
---
# <a name="wowinprocservers-collection"></a>Коллекция Вовинпроксерверс

Содержит список внутрипроцессного серверов, зарегистрированных в системе для 32-разрядных компонентов на 64-разрядных компьютерах. Он содержит объект для каждого компонента.

Эта коллекция поддерживает метод [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) объекта [**комадминкаталогколлектион**](comadmincatalogcollection.md) , но не метод [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) . Чтобы установить или импортировать компоненты в приложение, используйте методы для объекта [**комадминкаталог**](comadmincatalog.md) .

## <a name="members"></a>Элементы

Коллекция **вовинпроксерверс** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , но не содержит дополнительных элементов.

## <a name="related-collections"></a>Связанные коллекции

Можно переходить от этой коллекции к любой из следующих коллекций:

-   [**PropertyInfo**](propertyinfo.md)
-   [**релатедколлектионинфо**](relatedcollectioninfo.md)

Вы можете переходить к этой коллекции из следующих коллекций:

-   [**Корневой**](root.md)

## <a name="properties"></a>Свойства

Объект [**комадминкаталогобжект**](comadmincatalogobject.md) в коллекции поддерживает следующие свойства:

-   [ЭТОМУ](#clsid)
-   [InprocServer32](#inprocserver32)
-   [ProgID:](#progid)

### <a name="clsid"></a>CLSID



| Ввод | Значение |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Описание    | Идентификатор GUID для компонента. Это свойство возвращается при вызове метода свойства [**ключа**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) для объекта этой коллекции. |
| Доступ         | ReadOnly                                                                                                                                                  |
| Тип           | Строка                                                                                                                                                    |
| По умолчанию        | Н/Д                                                                                                                                                       |
| Минимальная система | Windows XP                                                                                                                                                |



 

### <a name="inprocserver32"></a>InprocServer32



| Ввод | Значение |
|----------------|----------------------------------|
| Описание    | Путь к файлу для компонента. |
| Доступ         | ReadOnly                         |
| Тип           | Строка                           |
| По умолчанию        | Н/Д                              |
| Минимальная система | Windows XP                       |



 

### <a name="progid"></a>ProgID:



| Ввод | Значение |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Описание    | Имя, идентифицирующее компонент. Это свойство возвращается при вызове метода свойства [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) для объекта этой коллекции. |
| Доступ         | ReadOnly                                                                                                                                                            |
| Тип           | Строка                                                                                                                                                              |
| По умолчанию        | Н/Д                                                                                                                                                                 |
| Минимальная система | Windows XP                                                                                                                                                          |



 

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Коллекции администрирования COM+](com--administration-collections.md)
</dt> </dl>

 

 
