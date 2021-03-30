---
title: Сообщение WM_DRAWITEM (Winuser. h)
description: Посылается родительскому окну рисуемой владельцем кнопки, поля со списком, списка или меню при изменении визуального элемента кнопки, поля со списком, списка или меню.
ms.assetid: e54bae5e-10d6-43b0-a766-1b270c8873a9
keywords:
- Элементы управления Windows для WM_DRAWITEM сообщений
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
ms.openlocfilehash: d5bd6465a560a0590ed9f5b483afae4c0d72d637
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802171"
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

## <a name="remarks"></a>Комментарии

По умолчанию функция [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) рисует прямоугольник фокуса для элемента списка, рисуемого владельцем.

Элемент *итемактион* структуры [**дравитемструкт**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) указывает операцию рисования, которую должно выполнить приложение.

Перед возвратом из обработки этого сообщения приложение должно убедиться, что контекст устройства, определенный членом *HDC* структуры [**дравитемструкт**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) , находится в состоянии по умолчанию.

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

[**дравитемструкт**](/windows/win32/api/winuser/ns-winuser-drawitemstruct)
</dt> <dt>

**Другие ресурсы**
</dt> <dt>

[**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> </dl>

 

