---
title: Интерфейс Ивмпмедиаколлектион (VB и C) (WMP. h)
description: Предоставляет методы, которые можно использовать для Организации большой коллекции элементов мультимедиа.
ms.assetid: a9e3d466-7dcf-4f1b-ba6f-9d166a35f03d
keywords:
- проигрыватель Windows Media интерфейса ивмпмедиаколлектион (VB и C)
- проигрыватель Windows Media интерфейса ивмпмедиаколлектион (VB и C), описание
topic_type:
- apiref
api_name:
- IWMPMediaCollection (VB and C )
- IWMPMediaCollection (VB and C ).isDeleted
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce15616b2059802610360b52d5af9bfa8d56b56b7ed06129bb849de567e22e26
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119468454"
---
# <a name="iwmpmediacollection-vb-and-c-interface"></a>Интерфейс Ивмпмедиаколлектион (VB и C#)

Предоставляет методы, которые можно использовать для Организации большой коллекции элементов мультимедиа.

## <a name="members"></a>Элементы

Интерфейс **ивмпмедиаколлектион (VB и C#)** имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **ивмпмедиаколлектион (VB и C#)** содержит следующие методы.



| Метод                                                                                                                       | Описание                                                                                                                                   |
|:-----------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------|
| [**add**](wmplibiwmpmediacollection-iwmpmediacollection-add--vb-and-c.md)                                                   | Добавляет новый элемент мультимедиа или список воспроизведения в библиотеку.<br/>                                                                                  |
| [**жеталл**](wmplibiwmpmediacollection-iwmpmediacollection-getall--vb-and-c.md)                                             | Возвращает интерфейс **ивмпплайлист** , соответствующий списку воспроизведения, содержащему все элементы мультимедиа в библиотеке.<br/>               |
| [**жетаттрибутестрингколлектион**](wmplibiwmpmediacollection-iwmpmediacollection-getattributestringcollection--vb-and-c.md) | Возвращает интерфейс **ивмпстрингколлектион** , представляющий набор всех значений для указанного атрибута в типе мультимедиа.<br/> |
| [**жетбялбум**](wmplibiwmpmediacollection-iwmpmediacollection-getbyalbum--vb-and-c.md)                                     | Возвращает интерфейс **ивмпплайлист** , предоставляющий доступ к элементам мультимедиа из указанного альбома.<br/>                                |
| [**жетбяттрибуте**](wmplibiwmpmediacollection-iwmpmediacollection-getbyattribute--vb-and-c.md)                             | Возвращает интерфейс **ивмпплайлист** , соответствующий указанному атрибуту, имеющему указанное значение.<br/>                      |
| [**жетбяусор**](wmplibiwmpmediacollection-iwmpmediacollection-getbyauthor--vb-and-c.md)                                   | Возвращает интерфейс **ивмпплайлист** , предоставляющий доступ к элементам мультимедиа по указанному автору.<br/>                             |
| [**жетбиженре**](wmplibiwmpmediacollection-iwmpmediacollection-getbygenre--vb-and-c.md)                                     | Возвращает интерфейс **ивмпплайлист** , предоставляющий доступ к элементам мультимедиа указанного жанра.<br/>                                  |
| [**жетбинаме**](wmplibiwmpmediacollection-iwmpmediacollection-getbyname--vb-and-c.md)                                       | Возвращает интерфейс **ивмпплайлист** , предоставляющий доступ к элементам мультимедиа с указанным именем.<br/>                                 |
| [**жетмедиаатом**](wmplibiwmpmediacollection-iwmpmediacollection-getmediaatom--vb-and-c.md)                                 | Возвращает индекс указанного атрибута.<br/>                                                                                        |
| **isDeleted**                                                                                                                | Больше не поддерживается.<br/>                                                                                                               |
| [**отменит**](wmplibiwmpmediacollection-iwmpmediacollection-remove--vb-and-c.md)                                             | Удаляет указанный элемент мультимедиа из коллекции носителей.<br/>                                                                        |
| [**сетделетед**](wmplibiwmpmediacollection-iwmpmediacollection-setdeleted--vb-and-c.md)                                     | Перемещает указанный элемент мультимедиа в папку Удаленные элементы.<br/>                                                                        |



 

Получите интерфейс **ивмпмедиаколлектион** , используя следующие свойства, доступ к которым осуществляется через следующий объект или интерфейс.



| Объект или интерфейс                                               | Свойство                                                                           |
|-------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [аксвиндовсмедиаплайер](axwindowsmediaplayer-object--vb-and-c.md) | [**медиаколлектион**](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md) |
| [**ивмплибрари**](iwmplibrary--vb-and-c.md)                      | [**медиаколлектион**](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md) |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>WMP. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**интерфейсы для Visual Basic .net и C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[**Интерфейс IWMPMediaCollection2**](iwmpmediacollection2--vb-and-c.md)
</dt> <dt>

[**Интерфейс Ивмпплайлист (VB и C#)**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**Интерфейс Ивмпстрингколлектион (VB и C#)**](iwmpstringcollection--vb-and-c.md)
</dt> </dl>

 

 





