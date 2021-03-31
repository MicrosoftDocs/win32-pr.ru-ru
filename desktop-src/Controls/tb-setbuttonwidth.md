---
title: Сообщение TB_SETBUTTONWIDTH (Коммктрл. h)
description: Задает минимальную и максимальную ширину кнопок в элементе управления ToolBar.
ms.assetid: 3311216a-e0b2-48bb-bad7-0a04185573cf
keywords:
- Элементы управления Windows для TB_SETBUTTONWIDTH сообщений
topic_type:
- apiref
api_name:
- TB_SETBUTTONWIDTH
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e105770d72e90108b9c31311f77599520cecea8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135951"
---
# <a name="tb_setbuttonwidth-message"></a>\_Сообщение СЕТБУТТОНВИДС ТБ

Задает минимальную и максимальную ширину кнопок в элементе управления ToolBar.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Должен равняться нулю.

</dd> <dt>

*lParam* 
</dt> <dd>

[**Ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) задает минимальную ширину кнопки в пикселях. Кнопки панели инструментов никогда не будут более узкими, чем это значение.

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) задает максимальную ширину кнопки в пикселях. Если текст кнопки слишком широк, элемент управления отображает его с помощью точек многоточия.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает ненулевое значение в случае успеха или ноль в противном случае.

## <a name="remarks"></a>Комментарии

Используйте **ТБ \_ сетбуттонвидс** , чтобы задать максимальную и минимальную допустимую ширину для кнопок перед их добавлением. Чтобы задать фактический размер кнопок, используйте [**\_ сетбуттонсизе ТБ**](tb-setbuttonsize.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

