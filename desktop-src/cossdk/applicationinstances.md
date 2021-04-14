---
description: Получает сведения о выполняющихся приложениях.
ms.assetid: 148e42aa-e99e-4fa2-8b74-a7ebf82b99d0
title: Коллекция Аппликатионинстанцес
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ApplicationInstances
api_type:
- COM
api_location: ''
ms.openlocfilehash: 56680a81cc564466dc3586bf0381cf4db97f914b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496125"
---
# <a name="applicationinstances-collection"></a>Коллекция Аппликатионинстанцес

Получает сведения о выполняющихся приложениях.

Эта коллекция поддерживает методы [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) и [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) объекта [**комадминкаталогколлектион**](comadmincatalogcollection.md) .

## <a name="members"></a>Элементы

Коллекция **аппликатионинстанцес** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , но не содержит дополнительных элементов.

## <a name="related-collections"></a>Связанные коллекции

Можно переходить от этой коллекции к любой из следующих коллекций:

-   [**ErrorInfo**](errorinfo.md)
-   [**PropertyInfo**](propertyinfo.md)
-   [**релатедколлектионинфо**](relatedcollectioninfo.md)

Вы можете переходить к этой коллекции из следующих коллекций:

-   [**Приложения**](applications.md)
-   [**Корневой**](root.md)

## <a name="properties"></a>Свойства

Объект [**комадминкаталогобжект**](comadmincatalogobject.md) в коллекции поддерживает следующие свойства:

-   [Приложение](#applicationinstances-collection)
-   [хасрециклед](#hasrecycled)
-   [InstanceID](#instanceid)
-   [IsPaused](#ispaused)
-   [PartitionID](#partitionid)
-   [ProcessID](#processid)

### <a name="application"></a>Приложение



| Ввод | Значение |
|----------------|-------------------------------------|
| Описание    | ИДЕНТИФИКАТОР выполняющегося приложения. |
| Access         | ReadOnly                            |
| Тип           | Строка                              |
| По умолчанию        | Н/Д                                 |
| Минимальная система | Windows XP                          |



 

### <a name="hasrecycled"></a>хасрециклед



| Ввод | Значение |
|----------------|---------------------------------------------------------------|
| Описание    | Указывает, был ли перезапущен экземпляр приложения. |
| Access         | ReadOnly                                                      |
| Тип           | Bool                                                          |
| Значение по умолчанию        | Неверно                                                         |
| Минимальная система | Windows XP                                                    |



 

### <a name="instanceid"></a>InstanceID



| Ввод | Значение |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Описание    | Глобальный уникальный идентификатор для экземпляра приложения. Это свойство возвращается при вызове метода свойства [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) или [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) для объекта этой коллекции. |
| Access         | ReadOnly                                                                                                                                                                                                                            |
| Тип           | Строка                                                                                                                                                                                                                              |
| По умолчанию        | Н/Д                                                                                                                                                                                                                                 |
| Минимальная система | Windows XP                                                                                                                                                                                                                          |



 

### <a name="ispaused"></a>IsPaused



| Ввод | Значение |
|----------------|-----------------------------------------------------------------|
| Описание    | Указывает, приостановлен ли экземпляр приложения в данный момент. |
| Access         | ReadOnly                                                        |
| Тип           | Bool                                                            |
| Значение по умолчанию        | Неверно                                                           |
| Минимальная система | Windows XP                                                      |



 

### <a name="partitionid"></a>PartitionID



| Ввод | Значение |
|----------------|-------------------------------------------------|
| Описание    | ИДЕНТИФИКАТОР раздела, который используется приложением. |
| Access         | ReadOnly                                        |
| Тип           | Строка                                          |
| По умолчанию        | Н/Д                                             |
| Минимальная система | Windows XP                                      |



 

### <a name="processid"></a>ProcessID



| Ввод | Значение |
|----------------|---------------------------------------------|
| Описание    | Идентификатор процесса экземпляра приложения. |
| Access         | ReadOnly                                    |
| Тип           | Строка                                      |
| По умолчанию        | Н/Д                                         |
| Минимальная система | Windows XP                                  |



 

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Коллекции администрирования COM+](com--administration-collections.md)
</dt> </dl>

 

 
