---
description: Извлекает расширенные сведения об ошибках для методов, связанных с несколькими объектами, таких как заполнение и SaveChanges в объекте Комадминкаталогколлектион, а также методы установки, импорта или экспорта приложений или компонентов в объекте Комадминкаталог.
ms.assetid: cf612fc4-55dd-4706-8c41-2654ca922b9a
title: Коллекция ErrorInfo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ErrorInfo
api_type:
- COM
api_location: ''
ms.openlocfilehash: ebcb4b89eee51b475869cfc62676feda10e53084
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496458"
---
# <a name="errorinfo-collection"></a>Коллекция ErrorInfo

Извлекает расширенные сведения об ошибках для методов, связанных с несколькими объектами, таких как [**Заполнение**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) и [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) в объекте [**комадминкаталогколлектион**](comadmincatalogcollection.md) , а также методы установки, импорта или экспорта приложений или компонентов в объекте [**комадминкаталог**](comadmincatalog.md) .

Используйте метод [**IsCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) для [**комадминкаталогколлектион**](comadmincatalogcollection.md) , чтобы получить доступ к коллекции **errorInfo** , связанной с исходной коллекцией, которая содержит ошибку.

Метод [**IsCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) следует вызывать в **errorInfo** сразу после возникновения ошибки. в противном случае сведения об ошибке теряются.

Эта коллекция не поддерживает методы [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) и [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) объекта [**комадминкаталогколлектион**](comadmincatalogcollection.md) .

## <a name="members"></a>Элементы

Коллекция **errorInfo** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , но не содержит дополнительных элементов.

## <a name="related-collections"></a>Связанные коллекции

Можно переходить от этой коллекции к любой из следующих коллекций:

-   [**PropertyInfo**](propertyinfo.md)
-   [**релатедколлектионинфо**](relatedcollectioninfo.md)

Можно переходить к этой коллекции из каждой коллекции, за исключением **errorInfo**, [**инпроксерверс**](inprocservers.md), [**PropertyInfo**](propertyinfo.md), [**релатедколлектионинфо**](relatedcollectioninfo.md), [**root**](root.md)и [**вовинпроксерверс**](wowinprocservers.md).

## <a name="properties"></a>Свойства

Объект [**комадминкаталогобжект**](comadmincatalogobject.md) в коллекции поддерживает следующие свойства:

-   [ErrorCode](#errorcode)
-   [мажорреф](#majorref)
-   [минорреф](#minorref)
-   [Name](#name)

### <a name="errorcode"></a>ErrorCode



| Ввод | Значение |
|----------------|----------------------------------------|
| Описание    | Код ошибки для объекта или файла. |
| Access         | ReadOnly                               |
| Тип           | Строка                                 |
| По умолчанию        | None                                   |
| Минимальная система | Windows 2000                           |



 

### <a name="majorref"></a>мажорреф



| Ввод | Значение |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Описание    | Значение [**ключевого**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) свойства для объекта, который содержит ошибку. Например, если вызов [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) для коллекции завершается ошибкой для определенного объекта в коллекции, значение **ключевого** свойства для этого объекта указывается как значение мажорреф. Это свойство используется для просмотра элемента, который не удается обновить, или для поиска компонента или библиотеки DLL, которые не удается установить. |
| Access         | ReadOnly                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Тип           | Строка                                                                                                                                                                                                                                                                                                                                                                                                                               |
| По умолчанию        | None                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Минимальная система | Windows 2000                                                                                                                                                                                                                                                                                                                                                                                                                         |



 

### <a name="minorref"></a>минорреф



| Ввод | Значение |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Описание    | Точная спецификация элемента, имеющего ошибку, например имя свойства. Если возникает несколько ошибок или в контекстах, в которых это не применимо, Минорреф имеет значение <Invalid> . |
| Access         | ReadOnly                                                                                                                                                                          |
| Тип           | Строка                                                                                                                                                                            |
| По умолчанию        | None                                                                                                                                                                              |
| Минимальная система | Windows 2000                                                                                                                                                                      |



 

### <a name="name"></a>Имя



| Ввод | Значение |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Описание    | Имя объекта или файла с ошибкой. Это свойство возвращается при вызове метода свойства [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) или [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) для объекта этой коллекции. |
| Access         | ReadOnly                                                                                                                                                                                                                 |
| Тип           | Строка                                                                                                                                                                                                                   |
| По умолчанию        | None                                                                                                                                                                                                                     |
| Минимальная система | Windows 2000                                                                                                                                                                                                             |



 

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Коллекции администрирования COM+](com--administration-collections.md)
</dt> </dl>

 

 
