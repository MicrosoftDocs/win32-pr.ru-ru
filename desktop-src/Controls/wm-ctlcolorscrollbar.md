---
title: Сообщение WM_CTLCOLORSCROLLBAR (Winuser. h)
description: Сообщение WM \_ ктлколорскроллбар отправляется в родительское окно элемента управления "полоса прокрутки", когда элемент управления собирается для рисования.
ms.assetid: 35832a23-96f1-42cb-a986-06726bf2a124
keywords:
- элементы управления Windows сообщений WM_CTLCOLORSCROLLBAR
topic_type:
- apiref
api_name:
- WM_CTLCOLORSCROLLBAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35dba3394c3d8fd99fef88d6fa1869ea1129d95ae8a82cc33f2935e5688871a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018562"
---
# <a name="wm_ctlcolorscrollbar-message"></a>\_Сообщение КТЛКОЛОРСКРОЛЛБАР WM

Сообщение **WM \_ ктлколорскроллбар** отправляется в родительское окно элемента управления "полоса прокрутки", когда элемент управления собирается для рисования. При ответе на это сообщение родительское окно может использовать маркер контекста отображения, чтобы задать цвет фона для элемента управления полосы прокрутки.

Окно получает это сообщение через функцию [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
WM_CTLCOLORSCROLLBAR

    WPARAM wParam
    LPARAM lParam; 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Обработайте с контекстом устройства для элемента управления "полоса прокрутки".

</dd> <dt>

*lParam* 
</dt> <dd>

Маркер полосы прокрутки.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если приложение обрабатывает это сообщение, оно должно вернуть дескриптор в кисть. Система использует кисть для рисования фона элемента управления полосы прокрутки.

## <a name="remarks"></a>Remarks

Если приложение возвращает созданную кисть (например, с помощью функции [**креатесолидбруш**](/windows/desktop/api/wingdi/nf-wingdi-createsolidbrush) или [**креатебрушиндирект**](/windows/desktop/api/wingdi/nf-wingdi-createbrushindirect) ), приложение должно освободить кисть. Если приложение возвращает системную кисть (например, которая была получена функцией [**жетстоккобжект**](/windows/desktop/api/wingdi/nf-wingdi-getstockobject) или [**жетсисколорбруш**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) ), приложению не нужно освобождать эту кисть.

По умолчанию функция [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) выбирает системные цвета по умолчанию для элемента управления "полоса прокрутки".

Сообщение **WM \_ ктлколорскроллбар** никогда не отправляется между потоками; оно отправляется только в том же потоке.

Если процедура диалогового окна обрабатывает это сообщение, необходимо привести требуемое возвращаемое значение к типу **int \_ ptr** и вернуть значение напрямую. Если процедура диалогового окна возвращает **значение false**, выполняется обработка сообщений по умолчанию. \_Значение МСГРЕСУЛТ DWL, заданное функцией [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) , игнорируется.

Сообщение **WM \_ ктлколорскроллбар** используется только дочерними элементами управления "полоса прокрутки". Полосы прокрутки, присоединенные к окну (WS \_ Scroll и WS \_ VSCROLL), не создают это сообщение. Чтобы настроить внешний вид полос прокрутки, присоединенных к окну, используйте функции плоской полосы прокрутки.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                                           |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                                     |
| Заголовок<br/>                   | <dl> <dt>Winuser. h (включает Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Ссылки**
</dt> <dt>

[**WM \_ ктлколорбтн**](wm-ctlcolorbtn.md)
</dt> <dt>

[**WM \_ ктлколоредит**](wm-ctlcoloredit.md)
</dt> <dt>

[**WM \_ ктлколорлистбокс**](wm-ctlcolorlistbox.md)
</dt> <dt>

[**WM \_ ктлколорстатик**](wm-ctlcolorstatic.md)
</dt> <dt>

**Другие ресурсы**
</dt> <dt>

[**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**реализепалетте**](/windows/desktop/api/wingdi/nf-wingdi-realizepalette)
</dt> <dt>

[**селектпалетте**](/windows/desktop/api/wingdi/nf-wingdi-selectpalette)
</dt> <dt>

[**WM \_ ктлколордлг**](/windows/desktop/dlgbox/wm-ctlcolordlg)
</dt> </dl>

 

