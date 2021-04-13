---
title: Сообщение WM_CHARTOITEM (Winuser. h)
description: Отправляется списком со стилем ФУНТа \_ ванткэйбоардинпут в ответ на \_ сообщение WM char.
ms.assetid: f941c00b-b836-4f1b-b8cf-8ac2b0704af3
keywords:
- Элементы управления Windows для WM_CHARTOITEM сообщений
topic_type:
- apiref
api_name:
- WM_CHARTOITEM
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2dc9df55dcf9f507cb57e91fe0214eab94c53f22
ms.sourcegitcommit: ac62be2f60f757f61ea647a95c168c9841ffabac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/10/2021
ms.locfileid: "104353915"
---
# <a name="wm_chartoitem-message"></a>\_Сообщение ЧАРТОИТЕМ WM

Отправляется списком со стилем [**фунта \_ ванткэйбоардинпут**](list-box-styles.md) в ответ на сообщение [**WM \_ char**](/windows/desktop/inputdev/wm-char) .


```C++
WM_CHARTOITEM

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

[**Ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) задает код символа нажатой пользователем клавиши. [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) задает текущую позиции курсора.

</dd> <dt>

*lParam* 
</dt> <dd>

Обработайте с списком.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращаемое значение указывает действие, выполненное приложением в ответ на сообщение. Возвращаемое значение-1 или-2 означает, что приложение обработало все аспекты выбора элемента и не требует дальнейших действий по списку. Возвращаемое значение 0 или больше Указывает отсчитываемый от нуля индекс элемента в списке и указывает, что поле списка должно выполнять действие по умолчанию для указанного элемента.

## <a name="remarks"></a>Комментарии

Функция [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) возвращает значение-1.

Это сообщение могут получить только рисуемые владельцем списки, у которых нет стиля [**фунта \_ хасстрингс**](list-box-styles.md) .

Если процедура диалогового окна обрабатывает это сообщение, необходимо привести требуемое возвращаемое значение к **логическому** типу и вернуть значение напрямую. Значение *\_ мсгресулт DWL* , заданное функцией [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) , игнорируется.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                                           |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (включение Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Ссылки**
</dt> <dt>

[**WM \_ вкэйтоитем**](wm-vkeytoitem.md)
</dt> <dt>

**Другие ресурсы**
</dt> <dt>

[**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**WM \_ char**](/windows/desktop/inputdev/wm-char)
</dt> </dl>

 

