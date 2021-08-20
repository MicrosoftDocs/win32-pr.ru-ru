---
title: Сообщение WM_CHARTOITEM (Winuser. h)
description: Отправляется списком со стилем ФУНТа \_ ванткэйбоардинпут в ответ на \_ сообщение WM char.
ms.assetid: f941c00b-b836-4f1b-b8cf-8ac2b0704af3
keywords:
- элементы управления Windows сообщений WM_CHARTOITEM
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
ms.openlocfilehash: 4f3809ae800cfc753925e7c27d87f970ce56c10d90ace7c23e87b46f3e0067fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957533"
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

## <a name="remarks"></a>Remarks

Функция [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) возвращает значение-1.

Это сообщение могут получить только рисуемые владельцем списки, у которых нет стиля [**фунта \_ хасстрингс**](list-box-styles.md) .

Если процедура диалогового окна обрабатывает это сообщение, необходимо привести требуемое возвращаемое значение к **логическому** типу и вернуть значение напрямую. Значение *\_ мсгресулт DWL* , заданное функцией [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) , игнорируется.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                                           |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                                     |
| Заголовок<br/>                   | <dl> <dt>Winuser. h (включает Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также

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

 

