---
title: Интерфейс IWMPPlaylist (VB и C) (Wmp.h)
description: Предоставляет свойства и методы для Организации и управления элементами мультимедиа в списке воспроизведения, а также для работы с ними. Интерфейс Ивмпплайлист предоставляет следующие свойства.
ms.assetid: c3f4f9dd-eb5f-493a-b8d0-22e70c63a2d1
keywords:
- проигрыватель Windows Media интерфейса ивмпплайлист (VB и C)
- проигрыватель Windows Media интерфейса ивмпплайлист (VB и C), описание
topic_type:
- apiref
api_name:
- IWMPPlaylist (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3fc1d8be09596d89dd87748811846d6dee1e8af8f28bebec56fa852c42ed6bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118119017"
---
# <a name="iwmpplaylist-vb-and-c-interface"></a>Интерфейс Ивмпплайлист (VB и C#)

Предоставляет свойства и методы для Организации и управления элементами мультимедиа в списке воспроизведения, а также для работы с ними.

Интерфейс **ивмпплайлист** предоставляет следующие свойства.

## <a name="members"></a>Элементы

Интерфейс **ивмпплайлист (VB и C#)** имеет следующие типы членов:

-   [Методы](#methods)
-   [Свойства](#properties)

### <a name="methods"></a>Методы

Интерфейс **ивмпплайлист (VB и C#)** содержит следующие методы.



| Метод                                                                       | Описание                                                             |
|:-----------------------------------------------------------------------------|:------------------------------------------------------------------------|
| [**аппендитем**](wmplibiwmpplaylist-iwmpplaylist-appenditem--vb-and-c.md)   | Добавляет элемент мультимедиа в конец списка воспроизведения.<br/>                |
| [**открытым**](iwmpplaylist-iwmpplaylist-clear--vb-and-c.md)                   | Зарезервировано для последующего использования.<br/>                                     |
| [**getItemInfo**](wmplibiwmpplaylist-iwmpplaylist-getiteminfo--vb-and-c.md) | Возвращает значение атрибута списка воспроизведения, указанного по имени.<br/> |
| [**insertItem**](wmplibiwmpplaylist-iwmpplaylist-insertitem--vb-and-c.md)   | Вставляет элемент мультимедиа в указанное место в списке воспроизведения.<br/>  |
| [**мовеитем**](wmplibiwmpplaylist-iwmpplaylist-moveitem--vb-and-c.md)       | Изменяет расположение элемента мультимедиа в списке воспроизведения.<br/>        |
| [**removeItem**](wmplibiwmpplaylist-iwmpplaylist-removeitem--vb-and-c.md)   | Удаляет указанный элемент мультимедиа из списка воспроизведения.<br/>          |
| [**сетитеминфо**](wmplibiwmpplaylist-iwmpplaylist-setiteminfo--vb-and-c.md) | Задает значение атрибута списка воспроизведения.<br/>                      |



 

### <a name="properties"></a>Свойства

Интерфейс **ивмпплайлист (VB и C#)** имеет следующие свойства.



| Свойство                                                                                      | Тип доступа           | Описание                                                                                                                                         |
|:----------------------------------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**аттрибутекаунт**](wmplibiwmpplaylist-iwmpplaylist-attributecount--vb-and-c.md)<br/> | Только для чтения<br/>  | Возвращает число атрибутов, связанных с списком воспроизведения.<br/>                                                                                |
| [**attributeName**](iwmpplaylist-attributename--vb-and-c.md)<br/>                      | Только для чтения<br/>  | Возвращает имя атрибута списка воспроизведения, указанного индексом. В C# это метод "Get \_ attributeName".<br/>                               |
| [**расчета**](wmplibiwmpplaylist-iwmpplaylist-count--vb-and-c.md)<br/>                   | Только для чтения<br/>  | Возвращает число элементов мультимедиа в списке воспроизведения.<br/>                                                                                            |
| [**Идентично**](iwmpplaylist-isidentical--vb-and-c.md)<br/>                          | Только для чтения<br/>  | Возвращает значение, указывающее, идентичен ли указанный список воспроизведения текущему списку воспроизведения. В C# это \_ метод Get одинаковы.<br/> |
| [**Компонент**](iwmpplaylist-item--vb-and-c.md)<br/>                                        | Только для чтения<br/>  | Возвращает интерфейс для элемента мультимедиа по указанному индексу. В C# это \_ метод Get Item.<br/>                                         |
| [**безымян**](wmplibiwmpplaylist-iwmpplaylist-name--vb-and-c.md)<br/>                     | Чтение/запись<br/> | Возвращает или задает имя списка воспроизведения.<br/>                                                                                                   |



 

Получите интерфейс **ивмпплайлист** , используя следующие свойства или методы, доступ к которым осуществляется через следующий объект или интерфейс.



| Объект или интерфейс                                                | Свойство или метод                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ивмпкдром**](iwmpcdrom--vb-and-c.md)                           | [**Список воспроизведения**](wmplibiwmpcdrom-iwmpcdrom-playlist--vb-and-c.md)                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| [**ивмпмедиаколлектион**](iwmpmediacollection--vb-and-c.md)       | [**жеталл**](wmplibiwmpmediacollection-iwmpmediacollection-getall--vb-and-c.md), [**жетбялбум**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmediacollection-getbyalbum), [**жетбяттрибуте**](wmplibiwmpmediacollection-iwmpmediacollection-getbyattribute--vb-and-c.md), [**жетбяусор**](wmplibiwmpmediacollection-iwmpmediacollection-getbyauthor--vb-and-c.md), [**жетбиженре**](wmplibiwmpmediacollection-iwmpmediacollection-getbygenre--vb-and-c.md), [**жетбинаме**](wmplibiwmpmediacollection-iwmpmediacollection-getbyname--vb-and-c.md) |
| [аксвиндовсмедиаплайер](axwindowsmediaplayer-object--vb-and-c.md)  | [**куррентплайлист**](axwmplib-axwindowsmediaplayer-currentplaylist--vb-and-c.md), [ **невплайлист**](axwmplib-axwindowsmediaplayer-newplaylist.md)                                                                                                                                                                                                                                                                                                                                                                   |
| [**ивмпплайлистаррай**](iwmpplaylistarray--vb-and-c.md)           | [**Компонент**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplaylistarray-item)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [**ивмпплайлистколлектион**](iwmpplaylistcollection--vb-and-c.md) | [**невплайлист**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplaylistcollection-newplaylist)                                                                                                                                                                                                                                                                                                                                                                                                                                                              |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>WMP. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**интерфейсы для Visual Basic .net и C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> </dl>

 

 





