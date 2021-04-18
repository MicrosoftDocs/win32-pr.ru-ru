---
description: Предоставляемые свойства для коллекции Вовлегацисерверс должны быть идентичны коллекции Легацисерверс, за исключением того, что коллекция Вовлегацисерверс отрисовывается из 32-разрядного реестра на 64-разрядных компьютерах.
ms.assetid: 72380276-214c-4f12-b575-deb975d846d3
title: Коллекция Вовлегацисерверс
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WOWLegacyServers
api_type:
- COM
api_location: ''
ms.openlocfilehash: cf417193ea4cea861f585068d139a855f80242a4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701191"
---
# <a name="wowlegacyservers-collection"></a>Коллекция Вовлегацисерверс

Предоставляемые свойства для коллекции **вовлегацисерверс** должны быть идентичны коллекции [**легацисерверс**](legacyservers.md) , за исключением того, что коллекция **вовлегацисерверс** отрисовывается из 32-разрядного реестра на 64-разрядных компьютерах.

Эта коллекция не поддерживает методы [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) и [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) объекта [**комадминкаталогколлектион**](comadmincatalogcollection.md) .

## <a name="members"></a>Элементы

Коллекция **вовлегацисерверс** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , но не содержит дополнительных элементов.

## <a name="related-collections"></a>Связанные коллекции

Можно переходить от этой коллекции к любой из следующих коллекций:

-   [**ErrorInfo**](errorinfo.md)
-   [**PropertyInfo**](propertyinfo.md)
-   [**релатедколлектионинфо**](relatedcollectioninfo.md)

Вы можете переходить к этой коллекции из следующих коллекций:

-   [**Корневой**](root.md)

## <a name="properties"></a>Свойства

Объект [**комадминкаталогобжект**](comadmincatalogobject.md) в коллекции поддерживает следующие свойства:

-   [ClassName](#classname)
-   [ЭТОМУ](#clsid)
-   [InprocServer32](#inprocserver32)
-   [LocalServer32](#localserver32)
-   [ProgID:](#progid)

### <a name="classname"></a>ClassName



| Ввод | Значение |
|----------------|------------------------|
| Описание    | Имя класса. |
| Access         | ReadOnly               |
| Тип           | Строка                 |
| По умолчанию        | Н/Д                    |
| Минимальная система | Windows XP             |



 

### <a name="clsid"></a>CLSID



| Ввод | Значение |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Описание    | Идентификатор GUID для компонента. Это свойство возвращается при вызове метода свойства [**ключа**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) для объекта этой коллекции. |
| Access         | ReadOnly                                                                                                                                                  |
| Тип           | Строка                                                                                                                                                    |
| По умолчанию        | Н/Д                                                                                                                                                       |
| Минимальная система | Windows XP                                                                                                                                                |



 

### <a name="inprocserver32"></a>InprocServer32



| Ввод | Значение |
|----------------|----------------------------------|
| Описание    | Путь к файлу для компонента. |
| Access         | ReadOnly                         |
| Тип           | Строка                           |
| По умолчанию        | Н/Д                              |
| Минимальная система | Windows XP                       |



 

### <a name="localserver32"></a>LocalServer32



| Ввод | Значение |
|----------------|---------------------------------------------------------------|
| Описание    | Указывает полный путь к 32-битному локальному серверному приложению. |
| Access         | ReadOnly                                                      |
| Тип           | Строка                                                        |
| По умолчанию        | Н/Д                                                           |
| Минимальная система | Windows XP                                                    |



 

### <a name="progid"></a>ProgID:



| Ввод | Значение |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Описание    | Имя, идентифицирующее компонент. Это свойство возвращается при вызове метода свойства [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) для объекта этой коллекции. |
| Access         | ReadOnly                                                                                                                                                            |
| Тип           | Строка                                                                                                                                                              |
| По умолчанию        | Н/Д                                                                                                                                                                 |
| Минимальная система | Windows XP                                                                                                                                                          |



 

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Коллекции администрирования COM+](com--administration-collections.md)
</dt> </dl>

 

 
