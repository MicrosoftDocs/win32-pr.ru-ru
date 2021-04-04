---
title: Сообщение WM_CTLCOLORSCROLLBAR (Winuser. h)
description: Сообщение WM \_ ктлколорскроллбар отправляется в родительское окно элемента управления "полоса прокрутки", когда элемент управления собирается для рисования.
ms.assetid: 35832a23-96f1-42cb-a986-06726bf2a124
keywords:
- Элементы управления Windows для WM_CTLCOLORSCROLLBAR сообщений
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
ms.openlocfilehash: a3f8282e8e15bf1d1a668e1f57e17048f0babac2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988591"
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

## <a name="remarks"></a>Комментарии

Если приложение возвращает созданную кисть (например, с помощью функции [**креатесолидбруш**](/windows/desktop/api/wingdi/nf-wingdi-createsolidbrush) или [**креатебрушиндирект**](/windows/desktop/api/wingdi/nf-wingdi-createbrushindirect) ), приложение должно освободить кисть. Если приложение возвращает системную кисть (например, которая была получена функцией [**жетстоккобжект**](/windows/desktop/api/wingdi/nf-wingdi-getstockobject) или [**жетсисколорбруш**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) ), приложению не нужно освобождать эту кисть.

По умолчанию функция [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) выбирает системные цвета по умолчанию для элемента управления "полоса прокрутки".

Сообщение **WM \_ ктлколорскроллбар** никогда не отправляется между потоками; оно отправляется только в том же потоке.

Если процедура диалогового окна обрабатывает это сообщение, необходимо привести требуемое возвращаемое значение к типу **int \_ ptr** и вернуть значение напрямую. Если процедура диалогового окна возвращает **значение false**, выполняется обработка сообщений по умолчанию. \_Значение МСГРЕСУЛТ DWL, заданное функцией [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) , игнорируется.

Сообщение **WM \_ ктлколорскроллбар** используется только дочерними элементами управления "полоса прокрутки". Полосы прокрутки, присоединенные к окну (WS \_ Scroll и WS \_ VSCROLL), не создают это сообщение. Чтобы настроить внешний вид полос прокрутки, присоединенных к окну, используйте функции плоской полосы прокрутки.

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

 

