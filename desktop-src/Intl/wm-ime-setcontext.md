---
description: Отправляется в приложение при активации окна. Окно получает это сообщение через функцию WindowProc.
ms.assetid: ba1e7877-1612-4f2f-aced-0dd982352ad6
title: Сообщение WM_IME_SETCONTEXT (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b36cb1e80127d1a451dabcc457dc364a27878ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263114"
---
# <a name="wm_ime_setcontext-message"></a>\_Сообщение SETCONTEXT редактора IME WM \_

Отправляется в приложение при активации окна. Окно получает это сообщение через функцию [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
LRESULT CALLBACK WindowProc(
  HWND  hwnd,  
  WM_IME_SETCONTEXT,  
  WPARAM wParam,      
  LPARAM lParam      
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*HWND* 
</dt> <dd>

Маркер для окна.

</dd> <dt>

*wParam* 
</dt> <dd>

**Значение true** , если окно активно, и **false** в противном случае.

</dd> <dt>

*lParam* 
</dt> <dd>

Параметры отображения. Этот параметр может иметь одно или несколько из следующих значений.



| Значение                                                                                                                                                                                                   | Значение                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <span id="ISC_SHOWUICOMPOSITIONWINDOW"></span><span id="isc_showuicompositionwindow"></span><dl> <dt>**ISC \_ шовуикомпоситионвиндов**</dt> </dl> | Отображение окна "композиция" по пользовательскому интерфейсу.<br/>          |
| <span id="ISC_SHOWUIGUIDWINDOW"></span><span id="isc_showuiguidwindow"></span><dl> <dt>**ISC \_ шовуигуидвиндов**</dt> </dl>                      | Отображение окна "Guide" по пользовательскому интерфейсу.<br/>                |
| <span id="ISC_SHOWUISOFTKBD"></span><span id="isc_showuisoftkbd"></span><dl> <dt>**ISC \_ шовуисофткбд**</dt> </dl>                               | Отображение экранной клавиатуры в окне пользовательского интерфейса.<br/>               |
| <span id="ISC_SHOWUICANDIDATEWINDOW"></span><span id="isc_showuicandidatewindow"></span><dl> <dt>**ISC \_ шовуикандидатевиндов**</dt> </dl>       | Отображение окна кандидатов с индексом 0 в окне пользовательского интерфейса.<br/> |
| <dl> <dt>ISC \_ шовуикандидатевиндов << 1</dt> </dl>                                                                                        | Отображение окна кандидатов с индексом 1 в окне пользовательского интерфейса.<br/> |
| <dl> <dt>ISC \_ шовуикандидатевиндов << 2</dt> </dl>                                                                                        | Отображение окна кандидатов с индексом 2 в окне пользовательского интерфейса.<br/> |
| <dl> <dt>ISC \_ шовуикандидатевиндов << 3</dt> </dl>                                                                                        | Отображение окна кандидатов с индексом 3 в окне пользовательского интерфейса.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение, возвращаемое [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) или [**иммисуимессаже**](/windows/desktop/api/Imm/nf-imm-immisuimessagea).

## <a name="remarks"></a>Комментарии

Если приложение создало окно IME, оно должно вызывать [**иммисуимессаже**](/windows/desktop/api/Imm/nf-imm-immisuimessagea). В противном случае оно должно передать это сообщение в [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).

Если приложение рисует окно композиции, то окно IME по умолчанию не обязательно отображает окно его композиции. В этом случае приложение должно очистить значение **ISC \_ шовуикомпоситионвиндов** из параметра *lParam* перед передачей сообщения в [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) или [**иммисуимессаже**](/windows/desktop/api/Imm/nf-imm-immisuimessagea). Чтобы отобразить определенное окно пользовательского интерфейса, приложение должно удалить соответствующее значение, чтобы редактор IME не отображал его.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                                                                                                                |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                                                                                                      |
| Заголовок<br/>                   | <dl> <dt>Winuser. h (включает Windows. h); </dt> <dt>IMM. h (включение Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Диспетчер метода ввода](input-method-manager.md)
</dt> <dt>

[Сообщения диспетчера методов ввода](input-method-manager-messages.md)
</dt> <dt>

[**иммисуимессаже**](/windows/desktop/api/Imm/nf-imm-immisuimessagea)
</dt> </dl>

 

 
