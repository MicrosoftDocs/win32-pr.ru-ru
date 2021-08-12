---
title: Стили элементов управления SysLink (Коммктрл. h)
description: При создании элементов управления SysLink используются следующие константы стиля.
ms.assetid: e9a8c99b-86c4-4385-ae20-b2b78a07b491
topic_type:
- apiref
api_name:
- LWS_TRANSPARENT
- LWS_IGNORERETURN
- LWS_NOPREFIX
- LWS_USEVISUALSTYLE
- LWS_USECUSTOMTEXT
- LWS_RIGHT
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3707a4e7b59811a99cb23ca4ebdbfc8bc2d285c2e8780502241beebb2f7485d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118670551"
---
# <a name="syslink-control-styles"></a>Стили элемента управления SysLink

При создании элементов управления SysLink используются следующие константы стиля.



| Константа                                                                                                                                                                        | Описание                                                                                                                                                               |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LWS_TRANSPARENT"></span><span id="lws_transparent"></span><dl> <dt>**\_прозрачный LWS**</dt> </dl>             | Режим фонового набора прозрачен. <br/>                                                                                                                       |
| <span id="LWS_IGNORERETURN_"></span><span id="lws_ignorereturn_"></span><dl> <dt>**LWS \_ ИГНОРЕРЕТУРН**</dt> </dl>       | Если ссылка имеет фокус клавиатуры и пользователь нажимает клавишу ВВОД, нажатие клавиши игнорируется элементом управления и передается в диалоговое окно хост.<br/>                        |
| <span id="LWS_NOPREFIX"></span><span id="lws_noprefix"></span><dl> <dt>**\_префикс LWS**</dt> </dl>                      | **Windows Vista**. Если текст содержит амперсанд, он обрабатывается как литеральный символ, а не как префикс для сочетания клавиш.<br/>                           |
| <span id="LWS_USEVISUALSTYLE_"></span><span id="lws_usevisualstyle_"></span><dl> <dt>**LWS \_ УСЕВИСУАЛСТИЛЕ**</dt> </dl> | **Windows Vista**. Ссылка отображается в текущем визуальном стиле.<br/>                                                                                          |
| <span id="LWS_USECUSTOMTEXT"></span><span id="lws_usecustomtext"></span><dl> <dt>**\_УСЕКУСТОМТЕКСТ LWS**</dt> </dl>       | **Windows Vista**. При прорисовке элемента управления отправляется уведомление о [NM \_ кустомтекст](nm-customtext.md) , чтобы приложение может предоставить текст динамически.<br/> |
| <span id="LWS_RIGHT"></span><span id="lws_right"></span><dl> <dt>**LWS \_ справа**</dt> </dl>                               | **Windows Vista**. Текст выравнивается по правому краю.<br/>                                                                                                                |



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





