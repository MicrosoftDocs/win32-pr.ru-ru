---
title: Интерфейс Иресултпроперти (Вдсшаредидл. h)
description: Предоставляет свойства результата.
ms.assetid: 58d8c516-47c6-4cae-b46c-5127baf3054d
keywords:
- Устаревшие функции среды Windows интерфейса Иресултпроперти
- Интерфейс Иресултпроперти устаревшие функции среды Windows, описание
topic_type:
- apiref
api_name:
- IResultProperty
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 716c0b3998171731dea5f976afc266fe81b2c613
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105691878"
---
# <a name="iresultproperty-interface"></a>Интерфейс Иресултпроперти

> [!NOTE]
> Windows Desktop Search 2. x — это устаревшая технология, которая изначально была доступна в качестве надстройки для Windows XP и Windows Server 2003. В более поздних выпусках используйте [API поиска Windows](../search/-search-reference-entry-page.md) . 

Предоставляет свойства результата.

## <a name="members"></a>Элементы

Интерфейс **иресултпроперти** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **Иресултпроперти** также имеет следующие типы членов:

-   [Методы](#methods)
-   [Свойства](#properties)

### <a name="methods"></a>Методы

Интерфейс **иресултпроперти** содержит следующие методы.



| Метод                                                    | Описание                 |
|:----------------------------------------------------------|:----------------------------|
| [**GoBack**](-search-2x-iresultproperty-goback.md)       | Не реализован.<br/> |
| [**GoForward**](-search-2x-iresultproperty-goforward.md) | Не реализован.<br/> |



 

### <a name="properties"></a>Свойства

Интерфейс **иресултпроперти** имеет следующие свойства.



| Свойство                                                                   | Тип доступа          | Описание                                           |
|:---------------------------------------------------------------------------|:---------------------|:------------------------------------------------------|
| [**Заданий**](-search-2x-iresultproperty-datatype.md)<br/>         | Только для чтения<br/> | Тип данных Properties. <br/>                   |
| [**DisplayName**](-search-2x-iresultproperty-displayname.md)<br/>   | Только для чтения<br/> | Локализованное отображаемое имя свойства. <br/>   |
| [**DisplayState**](-search-2x-iresultproperty-displaystate.md)<br/> | Только для чтения<br/> | Висабилити свойства. <br/>               |
| [**Хинтинга**](-search-2x-iresultproperty-hint.md)<br/>                 | Только для чтения<br/> | Специальное значение, используемое для облегчения извлечения данных. <br/> |
| [**индексколумн**](-search-2x-iresultproperty-indexcolumn.md)<br/>   | Только для чтения<br/> | Имя столбца свойств в индексе. <br/>      |
| [**ИД пользователя**](-search-2x-iresultproperty-uid.md)<br/>                   | Только для чтения<br/> | Уникальный идентификатор свойства. <br/>       |



 

## <a name="remarks"></a>Комментарии

Это элементы, возвращающие свойства.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для настольных приложений Windows XP с пакетом обновления 2 \[\]<br/>                                      |
| Минимальная версия сервера<br/> | Только для настольных приложений Windows Server 2003 с пакетом обновления 1 \[\]<br/>                             |
| Распространяемые компоненты<br/>          | Поиск на рабочем столе Windows (WDS) 3,0<br/>                                               |
| Header<br/>                   | <dl> <dt>Вдсшаредидл. h</dt> </dl> |



 

