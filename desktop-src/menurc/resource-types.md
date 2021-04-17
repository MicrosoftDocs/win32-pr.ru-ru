---
title: Типы ресурсов (Winuser. h)
description: Ниже перечислены предопределенные типы ресурсов.
ms.assetid: 8d27f79a-8165-4565-a975-f25b2344efdc
topic_type:
- apiref
api_name:
- RT_ACCELERATOR
- RT_ANICURSOR
- RT_ANIICON
- RT_BITMAP
- RT_CURSOR
- RT_DIALOG
- RT_DLGINCLUDE
- RT_FONT
- RT_FONTDIR
- RT_GROUP_CURSOR
- RT_GROUP_ICON
- RT_HTML
- RT_ICON
- RT_MANIFEST
- RT_MENU
- RT_MESSAGETABLE
- RT_PLUGPLAY
- RT_RCDATA
- RT_STRING
- RT_VERSION
- RT_VXD
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 595f1d459f645d26014a644d0e2b7cb608f4c6db
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708523"
---
# <a name="resource-types"></a>Типы ресурсов

Ниже перечислены предопределенные типы ресурсов.



| Константа/значение                                                                                                                                                                                                                                                           | Описание                                                                                                                                                                                                                                                                                      |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RT_ACCELERATOR"></span><span id="rt_accelerator"></span><dl> <dt>**RT \_ УСКОРИТЕЛь**</dt> <dt>макеинтресаурце (9)</dt> </dl>                                 | Таблица сочетаний клавиш.<br/>                                                                                                                                                                                                                                                                    |
| <span id="RT_ANICURSOR"></span><span id="rt_anicursor"></span><dl> <dt>**RT \_ АНИКУРСОР**</dt> <dt>макеинтресаурце (21)</dt> </dl>                                      | Анимированный курсор.<br/>                                                                                                                                                                                                                                                                      |
| <span id="RT_ANIICON"></span><span id="rt_aniicon"></span><dl> <dt>**RT \_ АНИИКОН**</dt> <dt>макеинтресаурце (22)</dt> </dl>                                            | Анимированный значок.<br/>                                                                                                                                                                                                                                                                        |
| <span id="RT_BITMAP"></span><span id="rt_bitmap"></span><dl> <dt>**RT \_ ТОЧЕЧный рисунок**</dt> <dt>макеинтресаурце (2)</dt> </dl>                                                | Ресурс точечного рисунка.<br/>                                                                                                                                                                                                                                                                      |
| <span id="RT_CURSOR"></span><span id="rt_cursor"></span><dl> <dt>**RT \_ Макеинтресаурце КУРСОРа**</dt> <dt>(1)</dt> </dl>                                                | Зависимый от оборудования ресурс курсора.<br/>                                                                                                                                                                                                                                                   |
| <span id="RT_DIALOG"></span><span id="rt_dialog"></span><dl> <dt>**RT \_ ДИАЛОГОВое окно**</dt> <dt>макеинтресаурце (5)</dt> </dl>                                                | Диалоговое окно.<br/>                                                                                                                                                                                                                                                                           |
| <span id="RT_DLGINCLUDE"></span><span id="rt_dlginclude"></span><dl> <dt>**RT \_ ДЛГИНКЛУДЕ**</dt> <dt>макеинтресаурце (17)</dt> </dl>                                   | Позволяет средству редактирования ресурсов связать строку с RC-файлом. Как правило, строка представляет собой имя файла заголовка, который предоставляет символьные имена. Компилятор ресурсов анализирует строку, но в противном случае игнорирует значение. Например, <br/> `1 DLGINCLUDE "MyFile.h"`<br/> |
| <span id="RT_FONT"></span><span id="rt_font"></span><dl> <dt>**RT \_ FONT**</dt> <dt>макеинтресаурце (8)</dt> </dl>                                                      | Ресурс шрифта.<br/>                                                                                                                                                                                                                                                                        |
| <span id="RT_FONTDIR"></span><span id="rt_fontdir"></span><dl> <dt>**RT \_ ФОНТДИР**</dt> <dt>макеинтресаурце (7)</dt> </dl>                                             | Ресурс каталога шрифтов.<br/>                                                                                                                                                                                                                                                              |
| <span id="RT_GROUP_CURSOR"></span><span id="rt_group_cursor"></span><dl> <dt>**RT \_ ГРУППИРОВАНие \_ курсора**</dt> <dt>МАКЕИНТРЕСАУРЦЕ ((ulong \_ PTR) (RT \_ cursor) + 11)</dt> </dl> | Аппаратно-независимый ресурс курсора.<br/>                                                                                                                                                                                                                                                 |
| <span id="RT_GROUP_ICON"></span><span id="rt_group_icon"></span><dl> <dt>**RT \_ \_Значок группы**</dt> <dt>МАКЕИНТРЕСАУРЦЕ ((ulong \_ PTR) ( \_ значок RT) + 11)</dt> </dl>         | Аппаратно-независимый ресурс значка.<br/>                                                                                                                                                                                                                                                   |
| <span id="RT_HTML"></span><span id="rt_html"></span><dl> <dt>**RT \_ Макеинтресаурце HTML**</dt> <dt>(23)</dt> </dl>                                                     | Ресурс HTML.<br/>                                                                                                                                                                                                                                                                        |
| <span id="RT_ICON"></span><span id="rt_icon"></span><dl> <dt>**RT \_ ЗНАЧОК**</dt> <dt>макеинтресаурце (3)</dt> </dl>                                                      | Аппаратно зависимый ресурс значка.<br/>                                                                                                                                                                                                                                                     |
| <span id="RT_MANIFEST"></span><span id="rt_manifest"></span><dl> <dt>**RT \_ Макеинтресаурце МАНИФЕСТа**</dt> <dt>(24)</dt> </dl>                                         | Манифест параллельной сборки.<br/>                                                                                                                                                                                                                                                       |
| <span id="RT_MENU"></span><span id="rt_menu"></span><dl> <dt>**RT \_ Макеинтресаурце меню**</dt> <dt>(4)</dt> </dl>                                                      | Ресурс меню.<br/>                                                                                                                                                                                                                                                                        |
| <span id="RT_MESSAGETABLE"></span><span id="rt_messagetable"></span><dl> <dt>**RT \_ МЕССАЖЕТАБЛЕ**</dt> <dt>макеинтресаурце (11)</dt> </dl>                             | Запись в таблице сообщений.<br/>                                                                                                                                                                                                                                                                  |
| <span id="RT_PLUGPLAY"></span><span id="rt_plugplay"></span><dl> <dt>**RT \_ ПЛУГПЛАЙ**</dt> <dt>макеинтресаурце (19)</dt> </dl>                                         | Самонастраивающийся ресурс.<br/>                                                                                                                                                                                                                                                               |
| <span id="RT_RCDATA"></span><span id="rt_rcdata"></span><dl> <dt>**RT \_ RCDATA**</dt> <dt>макеинтресаурце (10)</dt> </dl>                                               | Определяемый приложением ресурс (необработанные данные).<br/>                                                                                                                                                                                                                                              |
| <span id="RT_STRING"></span><span id="rt_string"></span><dl> <dt>**RT \_ STRING**</dt> <dt>макеинтресаурце (6)</dt> </dl>                                                | Запись строкового таблицы.<br/>                                                                                                                                                                                                                                                                   |
| <span id="RT_VERSION"></span><span id="rt_version"></span><dl> <dt>**RT \_ Версия**</dt> <dt>макеинтресаурце (16)</dt> </dl>                                            | Ресурс версии.<br/>                                                                                                                                                                                                                                                                     |
| <span id="RT_VXD"></span><span id="rt_vxd"></span><dl> <dt>**RT \_ VXD**</dt> <dt>макеинтресаурце (20)</dt> </dl>                                                        | VxD.<br/>                                                                                                                                                                                                                                                                                  |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|--------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Winuser. h</dt> </dl> |



 

 





