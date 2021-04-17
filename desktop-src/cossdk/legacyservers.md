---
description: Идентично коллекции Инпроксерверс, за исключением того, что эта коллекция также включает локальные серверы.
ms.assetid: b185f568-ec97-4710-b744-5d69e71d6f60
title: Коллекция Легацисерверс
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LegacyServers
api_type:
- COM
api_location: ''
ms.openlocfilehash: 2ea542fa539ea1eb1cceae0f4cb8ba8dc2012085
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673117"
---
# <a name="legacyservers-collection"></a>Коллекция Легацисерверс

Идентично коллекции [**инпроксерверс**](inprocservers.md) , за исключением того, что эта коллекция также включает локальные серверы.

Эта коллекция не поддерживает методы [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) и [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) объекта [**комадминкаталогколлектион**](comadmincatalogcollection.md) .

## <a name="members"></a>Элементы

Коллекция **легацисерверс** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , но не содержит дополнительных элементов.

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

 

 
