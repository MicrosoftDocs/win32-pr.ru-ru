---
description: Извлекает сведения о импортированных приложениях.
ms.assetid: 9ed4bc3f-3490-4c36-ba94-bc803886a4d2
title: Коллекция Филесфоримпорт
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FilesForImport
api_type:
- COM
api_location: ''
ms.openlocfilehash: 8e7ba3b0bd44cf2f6bb40ecf89f86dd68c21cf3c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141992"
---
# <a name="filesforimport-collection"></a>Коллекция Филесфоримпорт

Извлекает сведения о импортированных приложениях.

Эта коллекция поддерживает методы [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) и [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) объекта [**комадминкаталогколлектион**](comadmincatalogcollection.md) .

## <a name="members"></a>Элементы

Коллекция **филесфоримпорт** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , но не содержит дополнительных элементов.

## <a name="related-collections"></a>Связанные коллекции

Можно переходить от этой коллекции к любой из следующих коллекций:

-   [**ErrorInfo**](errorinfo.md)
-   [**PropertyInfo**](propertyinfo.md)
-   [**релатедколлектионинфо**](relatedcollectioninfo.md)

Вы можете переходить к этой коллекции из следующих коллекций:

-   [**Корневой**](root.md)

## <a name="properties"></a>Свойства

Объект [**комадминкаталогобжект**](comadmincatalogobject.md) в коллекции поддерживает следующие свойства:

-   [аппликатионфиленаме](#applicationfilename)
-   [ApplicationName](#applicationname)
-   [Описание](#partitiondescription)
-   [FileName](#applicationfilename)
-   [хасусерс](#hasusers)
-   [IsProxy](#isproxy)
-   [Служба](#isservice)
-   [партитиондескриптион](#partitiondescription)
-   [PartitionID](#partitionid)
-   [Имя раздела](#partitionname)

### <a name="applicationfilename"></a>аппликатионфиленаме



| Ввод | Значение |
|----------------|------------------------------------------------------------------------------|
| Описание    | Имя MSI файла, содержащего приложение, которое можно импортировать. |
| Access         | ReadOnly                                                                     |
| Тип           | Строка                                                                       |
| По умолчанию        | Н/Д                                                                          |
| Минимальная система | Windows XP                                                                   |



 

### <a name="applicationname"></a>ApplicationName



| Ввод | Значение |
|----------------|------------------------------|
| Описание    | Имя приложения. |
| Access         | ReadOnly                     |
| Тип           | Строка                       |
| По умолчанию        | ""                           |
| Минимальная система | Windows XP                   |



 

### <a name="description"></a>Описание



| Ввод | Значение |
|----------------|-----------------------------------|
| Описание    | Описание приложения. |
| Access         | ReadOnly                          |
| Тип           | Строка                            |
| По умолчанию        | ""                                |
| Минимальная система | Windows XP                        |



 

### <a name="filename"></a>FileName



| Ввод | Значение |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Описание    | Имя файла DLL или EXE, содержащего приложение. Это свойство возвращается при вызове метода свойства [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) или [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) для объекта этой коллекции. |
| Access         | ReadOnly                                                                                                                                                                                                                              |
| Тип           | Строка                                                                                                                                                                                                                                |
| По умолчанию        | ""                                                                                                                                                                                                                                    |
| Минимальная система | Windows XP                                                                                                                                                                                                                            |



 

### <a name="hasusers"></a>хасусерс



| Ввод | Значение |
|----------------|--------------------------------------------------|
| Описание    | Указывает, есть ли у приложения пользователи. |
| Access         | ReadOnly                                         |
| Тип           | Bool                                             |
| Значение по умолчанию        | Неверно                                            |
| Минимальная система | Windows XP                                       |



 

### <a name="isproxy"></a>IsProxy



| Ввод | Значение |
|----------------|-----------------------------------------------|
| Описание    | Указывает, является ли приложение прокси-сервером. |
| Access         | ReadOnly                                      |
| Тип           | Bool                                          |
| Значение по умолчанию        | Неверно                                         |
| Минимальная система | Windows XP                                    |



 

### <a name="isservice"></a>Служба



| Ввод | Значение |
|----------------|-------------------------------------------------|
| Описание    | Указывает, является ли приложение службой. |
| Access         | ReadOnly                                        |
| Тип           | Bool                                            |
| Значение по умолчанию        | Неверно                                           |
| Минимальная система | Windows XP                                      |



 

### <a name="partitiondescription"></a>партитиондескриптион



| Ввод | Значение |
|----------------|-----------------------------------------------|
| Описание    | Описание раздела приложения. |
| Access         | ReadOnly                                      |
| Тип           | Строка                                        |
| По умолчанию        | ""                                            |
| Минимальная система | Windows Server 2003                           |



 

### <a name="partitionid"></a>PartitionID



| Ввод | Значение |
|----------------|------------------------------------------|
| Описание    | Идентификатор GUID раздела приложения. |
| Access         | ReadOnly                                 |
| Тип           | Строка                                   |
| По умолчанию        | ""                                       |
| Минимальная система | Windows Server 2003                      |



 

### <a name="partitionname"></a>Имя раздела



| Ввод | Значение |
|----------------|------------------------------------------|
| Описание    | Имя раздела приложения. |
| Access         | ReadOnly                                 |
| Тип           | Строка                                   |
| По умолчанию        | ""                                       |
| Минимальная система | Windows Server 2003                      |



 

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Коллекции администрирования COM+](com--administration-collections.md)
</dt> </dl>

 

 
