---
title: Сообщение WM_DRAWITEM (Winuser. h)
description: Посылается родительскому окну рисуемой владельцем кнопки, поля со списком, списка или меню при изменении визуального элемента кнопки, поля со списком, списка или меню.
ms.assetid: e54bae5e-10d6-43b0-a766-1b270c8873a9
keywords:
- элементы управления Windows сообщений WM_DRAWITEM
topic_type:
- apiref
api_name:
- WM_DRAWITEM
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f5d4b2addfa2de5f8c76ded636ca29a96fb3af7e0ab4157d25ac26a78c462c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957523"
---
# <a name="wm_drawitem-message"></a>\_Сообщение DRAWITEM WM

Посылается родительскому окну рисуемой владельцем кнопки, поля со списком, списка или меню при изменении визуального элемента кнопки, поля со списком, списка или меню.

Окно получает это сообщение через функцию [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
WM_DRAWITEM

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Указывает идентификатор элемента управления, который отправил сообщение **WM \_ DRAWITEM** . Если сообщение было отправлено меню, этот параметр равен нулю.

</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**дравитемструкт**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) , содержащую сведения о рисуемом элементе, и требуемый тип рисования.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если приложение обрабатывает это сообщение, оно должно возвращать **значение true**.

## <a name="remarks"></a>Remarks

По умолчанию функция [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) рисует прямоугольник фокуса для элемента списка, рисуемого владельцем.

Элемент *итемактион* структуры [**дравитемструкт**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) указывает операцию рисования, которую должно выполнить приложение.

Перед возвратом из обработки этого сообщения приложение должно убедиться, что контекст устройства, определенный членом *HDC* структуры [**дравитемструкт**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) , находится в состоянии по умолчанию.

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

[**дравитемструкт**](/windows/win32/api/winuser/ns-winuser-drawitemstruct)
</dt> <dt>

**Другие ресурсы**
</dt> <dt>

[**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> </dl>

 

