---
description: Содержит список внутрипроцессного серверов, зарегистрированных в системе. Он содержит объект для каждого компонента, зарегистрированного как внутрипроцессный сервер.
ms.assetid: 10434de7-c5e3-4fb0-8472-2a581607fcc0
title: Коллекция Инпроксерверс
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InprocServers
api_type:
- COM
api_location: ''
ms.openlocfilehash: 737627c99ac92a96883750bfc43dc3e2a9364d87
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105710701"
---
# <a name="inprocservers-collection"></a>Коллекция Инпроксерверс

Содержит список внутрипроцессного серверов, зарегистрированных в системе. Он содержит объект для каждого компонента, зарегистрированного как внутрипроцессный сервер.

Эта коллекция поддерживает метод [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) объекта [**комадминкаталогколлектион**](comadmincatalogcollection.md) , но не метод [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) . Чтобы установить или импортировать компоненты в приложение, используйте методы для объекта [**комадминкаталог**](comadmincatalog.md) .

## <a name="members"></a>Элементы

Коллекция **инпроксерверс** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , но не содержит дополнительных элементов.

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
| Access         | ReadOnly                                                                                                                                                  |
| Тип           | Строка                                                                                                                                                    |
| По умолчанию        | Н/Д                                                                                                                                                       |
| Минимальная система | Windows 2000                                                                                                                                              |



 

### <a name="inprocserver32"></a>InprocServer32



| Ввод | Значение |
|----------------|----------------------------------|
| Описание    | Путь к файлу для компонента. |
| Access         | ReadOnly                         |
| Тип           | Строка                           |
| По умолчанию        | Н/Д                              |
| Минимальная система | Windows 2000                     |



 

### <a name="progid"></a>ProgID:



| Ввод | Значение |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Описание    | Имя, идентифицирующее компонент. Это свойство возвращается при вызове метода свойства [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) для объекта этой коллекции. |
| Access         | ReadOnly                                                                                                                                                            |
| Тип           | Строка                                                                                                                                                              |
| По умолчанию        | Н/Д                                                                                                                                                                 |
| Минимальная система | Windows 2000                                                                                                                                                        |



 

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Коллекции администрирования COM+](com--administration-collections.md)
</dt> </dl>

 

 
