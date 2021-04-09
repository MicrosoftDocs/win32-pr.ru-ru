---
title: Сообщение TB_MARKBUTTON (Коммктрл. h)
description: Задает состояние выделения для данной кнопки в элементе управления ToolBar.
ms.assetid: cba0e2d2-40a7-4e20-a1ef-d5f5444c96d9
keywords:
- Элементы управления Windows для TB_MARKBUTTON сообщений
topic_type:
- apiref
api_name:
- TB_MARKBUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d42983f5fb0ef6e62716cefa2fa8db4fca87fa4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071858"
---
# <a name="tb_markbutton-message"></a>\_Сообщение МАРКБУТТОН ТБ

Задает состояние выделения для данной кнопки в элементе управления ToolBar.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Идентификатор команды для кнопки панели инструментов.

</dd> <dt>

*lParam* 
</dt> <dd>

[**Ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) — это **логическое** значение, указывающее новое состояние выделения. Если **значение — true**, кнопка выделяется. Если задано **значение false**, кнопка будет иметь состояние по умолчанию.

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) должен быть равен нулю.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает ненулевое значение в случае успеха или ноль в противном случае.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

