---
title: Интерфейс Иресултпроперти (Вдсшаредидл. h)
description: Предоставляет свойства результата.
ms.assetid: 58d8c516-47c6-4cae-b46c-5127baf3054d
keywords:
- устаревшие функции среды Windows интерфейса иресултпроперти
- устаревшие функции среды Windows интерфейса иресултпроперти, описание
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
ms.openlocfilehash: efba214aaaadec2cfad52db02f9f4f18d289b0b3ee9df37ee60295d5499241e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118754587"
---
# <a name="iresultproperty-interface"></a>Интерфейс Иресултпроперти

> [!NOTE]
> Windows настольный поиск 2. x — это устаревшая технология, которая изначально была доступна в качестве надстройки для Windows XP и Windows Server 2003. в более поздних выпусках используйте вместо этого [API Windows поиска](../search/-search-reference-entry-page.md) . 

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



 

## <a name="remarks"></a>Remarks

Это элементы, возвращающие свойства.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP с пакетом обновления 2 (SP2) \[ только классические приложения\]<br/>                                      |
| Минимальная версия сервера<br/> | Windows Только для настольных приложений сервера 2003 с пакетом обновления 1 \[\]<br/>                             |
| Распространяемые компоненты<br/>          | Windows Поиск на рабочем столе (WDS) 3,0<br/>                                               |
| Header<br/>                   | <dl> <dt>Вдсшаредидл. h</dt> </dl> |



 

