---
title: Идентификаторы объектов (Winuser. h)
description: В этом разделе описываются идентификаторы объектов Microsoft Active Accessibility, 32-разрядные значения, которые указывают категории объектов, доступных в окне.
ms.assetid: dc1603f8-29e5-4acd-817a-c6957feaff6c
topic_type:
- apiref
api_name:
- OBJID_ALERT
- OBJID_CARET
- OBJID_CLIENT
- OBJID_CURSOR
- OBJID_HSCROLL
- OBJID_NATIVEOM
- OBJID_MENU
- OBJID_QUERYCLASSNAMEIDX
- OBJID_SIZEGRIP
- OBJID_SOUND
- OBJID_SYSMENU
- OBJID_TITLEBAR
- OBJID_VSCROLL
- OBJID_WINDOW
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1fa2cf2099c5177be6f295ef6455646762525b26
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105717903"
---
# <a name="object-identifiers-winuserh"></a>Идентификаторы объектов (Winuser. h)

В этом разделе описываются идентификаторы объектов Microsoft Active Accessibility, 32-разрядные значения, которые указывают *категории* объектов, доступных в окне. Серверы Microsoft Active Accessibility и поставщики автоматизации пользовательского интерфейса Майкрософт используют идентификаторы объектов для определения объекта, к которому относится запрос сообщения [**WM \_ GetObject**](wm-getobject.md) .

Клиенты получают эти значения в своей функции обратного вызова [*виневентпрок*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) и используют их для обнаружения частей окна. Серверы используют эти значения для обнаружения соответствующих частей окна при вызове [**нотифивиневент**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) или при ответе на сообщение [**WM \_ GetObject**](wm-getobject.md) .

Серверы могут определять идентификаторы пользовательских объектов для определения других категорий объектов в своих приложениях. Идентификаторам пользовательских объектов должны быть присвоены положительные значения, так как Microsoft Active Accessibility резервирует ноль и все отрицательные значения для следующих стандартных идентификаторов объектов.

Следующие константы определены в файле WinUser. h:



| Константа                                                                                                                                                                                    | Описание                                                                                                                                                                                                                                                                                                                                            |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OBJID_ALERT"></span><span id="objid_alert"></span><dl> <dt>**\_оповещение OBJID**</dt> </dl>                                     | Оповещение, связанное с окном или приложением. Предоставляемые системой окна сообщений являются единственными элементами пользовательского интерфейса, которые отправляют события с этим идентификатором объекта. Серверные приложения не могут использовать функции **акцессиблеобжектфром**_X_ с этим идентификатором объекта. Это известная проблема с Microsoft Active Accessibility.<br/>          |
| <span id="OBJID_CARET"></span><span id="objid_caret"></span><dl> <dt>**OBJID \_ курсор**</dt> </dl>                                     | Строка вставки текста (курсор) в окне.<br/>                                                                                                                                                                                                                                                                                               |
| <span id="OBJID_CLIENT"></span><span id="objid_client"></span><dl> <dt>**\_клиент OBJID**</dt> </dl>                                  | Клиентская область окна. В большинстве случаев операционная система управляет элементами Frame, а клиентский объект содержит все элементы, управляемые приложением. Серверы обрабатывают только сообщения [**WM \_ GetObject**](wm-getobject.md) , в которых *lParam* является OBJID \_ клиентом, OBJID \_ окном или идентификатором настраиваемого объекта.<br/> |
| <span id="OBJID_CURSOR"></span><span id="objid_cursor"></span><dl> <dt>**OBJID \_ курсор**</dt> </dl>                                  | Указатель мыши. В системе имеется только один указатель мыши, который не является дочерним по отношению к какому-либо окну.<br/>                                                                                                                                                                                                                                      |
| <span id="OBJID_HSCROLL"></span><span id="objid_hscroll"></span><dl> <dt>**OBJID \_ HSCROLL**</dt> </dl>                               | Горизонтальная полоса прокрутки окна.<br/>                                                                                                                                                                                                                                                                                                         |
| <span id="OBJID_NATIVEOM"></span><span id="objid_nativeom"></span><dl> <dt>**OBJID \_ нативеом**</dt> </dl>                            | В ответ на этот идентификатор объекта сторонние приложения могут предоставлять собственную объектную модель. Сторонние приложения могут возвращать любой COM-интерфейс в ответ на этот идентификатор объекта.<br/>                                                                                                                                             |
| <span id="OBJID_MENU"></span><span id="objid_menu"></span><dl> <dt>**\_меню OBJID**</dt> </dl>                                        | Строка меню окна.<br/>                                                                                                                                                                                                                                                                                                                      |
| <span id="OBJID_QUERYCLASSNAMEIDX"></span><span id="objid_queryclassnameidx"></span><dl> <dt>**OBJID \_ куерикласснамеидкс**</dt> </dl> | Идентификатор объекта, который Oleacc.dll используется внутренним образом. Дополнительные сведения см. в [приложении F: значения идентификаторов объектов для OBJID \_ куерикласснамеидкс](appendix-f--object-identifier-values-for-objid-queryclassnameidx.md).<br/>                                                                                                                  |
| <span id="OBJID_SIZEGRIP"></span><span id="objid_sizegrip"></span><dl> <dt>**OBJID \_ сизегрип**</dt> </dl>                            | Захват размера окна: необязательный компонент Frame, расположенный в правом нижнем углу рамки окна.<br/>                                                                                                                                                                                                                                  |
| <span id="OBJID_SOUND"></span><span id="objid_sound"></span><dl> <dt>**OBJID \_ звук**</dt> </dl>                                     | Звуковой объект. У объектов Sound нет расположений на экране или дочерних элементов, но у них есть атрибуты Name и State. Они являются дочерними объектами приложения, которое воспроизводит звук.<br/>                                                                                                                                                         |
| <span id="OBJID_SYSMENU"></span><span id="objid_sysmenu"></span><dl> <dt>**OBJID \_ сисмену**</dt> </dl>                               | Системное меню окна.<br/>                                                                                                                                                                                                                                                                                                                   |
| <span id="OBJID_TITLEBAR"></span><span id="objid_titlebar"></span><dl> <dt>**OBJID, \_ заголовок**</dt> </dl>                            | Заголовок окна.<br/>                                                                                                                                                                                                                                                                                                                     |
| <span id="OBJID_VSCROLL"></span><span id="objid_vscroll"></span><dl> <dt>**OBJID \_ VSCROLL**</dt> </dl>                               | Вертикальная полоса прокрутки окна.<br/>                                                                                                                                                                                                                                                                                                           |
| <span id="OBJID_WINDOW"></span><span id="objid_window"></span><dl> <dt>**\_окно OBJID**</dt> </dl>                                  | Само окно, а не дочерний объект.<br/>                                                                                                                                                                                                                                                                                               |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Winuser. h (включение Windows. h)</dt> </dl> |



 

 





