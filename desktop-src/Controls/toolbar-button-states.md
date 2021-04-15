---
title: Состояния кнопок панели инструментов (Коммктрл. h)
description: В этом разделе перечислены состояния, которые может иметь кнопка панели инструментов.
ms.assetid: 422e0d81-bd80-45dc-b843-82fc5d5c2a9a
topic_type:
- apiref
api_name:
- TBSTATE_CHECKED
- TBSTATE_ELLIPSES
- TBSTATE_ENABLED
- TBSTATE_HIDDEN
- TBSTATE_INDETERMINATE
- TBSTATE_MARKED
- TBSTATE_PRESSED
- TBSTATE_WRAP
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45262197c4432d9e3bb5c0884b3f76c986e4acfe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648683"
---
# <a name="toolbar-button-states"></a>Состояния кнопок панели инструментов

В этом разделе перечислены состояния, которые может иметь кнопка панели инструментов.



| Константа                                                                                                                                                                              | Описание                                                                                                                                           |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TBSTATE_CHECKED"></span><span id="tbstate_checked"></span><dl> <dt>**ТБСТАТЕ \_ Проверено**</dt> </dl>                   | Кнопка имеет стиль [**\_ проверки тбстиле**](toolbar-control-and-button-styles.md) и нажата.<br/>                   |
| <span id="TBSTATE_ELLIPSES"></span><span id="tbstate_ellipses"></span><dl> <dt>**ТБСТАТЕ \_ многоточия**</dt> </dl>                | [Версия 4,70](common-control-versions.md). Текст кнопки обрезан и отображается многоточие.<br/>                                    |
| <span id="TBSTATE_ENABLED"></span><span id="tbstate_enabled"></span><dl> <dt>**ТБСТАТЕ \_ включен**</dt> </dl>                   | Кнопка принимает введенные пользователем данные. Кнопка, которая не имеет этого состояния, отображается серым цветом.<br/>                                                           |
| <span id="TBSTATE_HIDDEN"></span><span id="tbstate_hidden"></span><dl> <dt>**ТБСТАТЕ \_ скрыто**</dt> </dl>                      | Кнопка невидима и не может принимать данные, вводимые пользователем.<br/>                                                                                   |
| <span id="TBSTATE_INDETERMINATE"></span><span id="tbstate_indeterminate"></span><dl> <dt>**ТБСТАТЕ \_ неопределенный**</dt> </dl> | Кнопка неактивна.<br/>                                                                                                                      |
| <span id="TBSTATE_MARKED"></span><span id="tbstate_marked"></span><dl> <dt>**ТБСТАТЕ \_ помечено**</dt> </dl>                      | [Версия 4,71](common-control-versions.md). Кнопка помечена. Интерпретация помеченного элемента зависит от приложения. <br/> |
| <span id="TBSTATE_PRESSED"></span><span id="tbstate_pressed"></span><dl> <dt>**ТБСТАТЕ \_ нажата**</dt> </dl>                   | Нажата кнопка.<br/>                                                                                                               |
| <span id="TBSTATE_WRAP"></span><span id="tbstate_wrap"></span><dl> <dt>**ТБСТАТЕ \_ Перенос**</dt> </dl>                            | За кнопкой следует разрыв строки. Кнопка также должна иметь \_ состояние тбстате Enabled (включено).<br/>                                              |



## <a name="remarks"></a>Комментарии

Панель инструментов может иметь сочетание состояний.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





