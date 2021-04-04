---
title: Сообщение WM_VSCROLL (Winuser. h)
description: Сообщение WM \_ VSCROLL отправляется в окно при возникновении события прокрутки в стандартной вертикальной полосе прокрутки окна.
ms.assetid: 495733b8-1aac-4ff7-b0be-15f14581f41c
keywords:
- Элементы управления Windows для WM_VSCROLL сообщений
topic_type:
- apiref
api_name:
- WM_VSCROLL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12c83888b83e0d5f8d3c77775347ccc9b43a59d5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137547"
---
# <a name="wm_vscroll-message"></a>\_Сообщение VSCROLL WM

Сообщение **WM \_ VSCROLL** отправляется в окно при возникновении события прокрутки в стандартной вертикальной полосе прокрутки окна. Это сообщение также отправляется владельцу вертикальной полосы прокрутки, когда в элементе управления возникает событие прокрутки.

Окно получает это сообщение через функцию [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
WM_VSCROLL

    WPARAM wParam
    LPARAM lParam; 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) указывает текущее расположение поля прокрутки, если [**ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) является SB \_ сумбпоситион или SB \_ сумбтракк; в противном случае это слово не используется.

[**Ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) указывает значение полосы прокрутки, которое указывает на запрос прокрутки пользователя. Этот параметр может принимать одно из указанных ниже значений.



| Значение                                                                                                                                                                  | Значение                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SB_BOTTOM"></span><span id="sb_bottom"></span><dl> <dt>**SB \_ снизу**</dt> </dl>                      | Прокручивает вниз до нижнего правого.<br/>                                                                                                                                                                                    |
| <span id="SB_ENDSCROLL"></span><span id="sb_endscroll"></span><dl> <dt>**SB \_ ендскролл**</dt> </dl>             | Завершает прокрутку.<br/>                                                                                                                                                                                                   |
| <span id="SB_LINEDOWN"></span><span id="sb_linedown"></span><dl> <dt>**SB \_ линедовн**</dt> </dl>                | Прокручивает по одной строке вниз.<br/>                                                                                                                                                                                         |
| <span id="SB_LINEUP"></span><span id="sb_lineup"></span><dl> <dt>**построителя \_**</dt> </dl>                      | Выполняет прокрутку на одну строку вверх.<br/>                                                                                                                                                                                           |
| <span id="SB_PAGEDOWN"></span><span id="sb_pagedown"></span><dl> <dt>**SB \_ PageDown**</dt> </dl>                | Прокручивает одну страницу вниз.<br/>                                                                                                                                                                                         |
| <span id="SB_PAGEUP"></span><span id="sb_pageup"></span><dl> <dt>**SB \_ PageUp**</dt> </dl>                      | Прокручивает на одну страницу вверх.<br/>                                                                                                                                                                                           |
| <span id="SB_THUMBPOSITION"></span><span id="sb_thumbposition"></span><dl> <dt>**SB \_ сумбпоситион**</dt> </dl> | Пользователь переместил бегунок (бегунок) и отпустил кнопку мыши. [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) указывает на позиции ползунка в конце операции перетаскивания.<br/>                          |
| <span id="SB_THUMBTRACK"></span><span id="sb_thumbtrack"></span><dl> <dt>**SB \_ сумбтракк**</dt> </dl>          | Пользователь перетаскивает полосу прокрутки. Это сообщение отправляется повторно, пока пользователь не отпускает кнопку мыши. [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) указывает на то, куда переместился ползунок полосы прокрутки.<br/> |
| <span id="SB_TOP"></span><span id="sb_top"></span><dl> <dt>**SB \_ сверху**</dt> </dl>                               | Выполняет прокрутку к верхнему левому краю.<br/>                                                                                                                                                                                     |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Если сообщение отправляется элементом управления "полоса прокрутки", этот параметр является маркером элемента управления "полоса прокрутки". Если сообщение отправляется стандартной полосой прокрутки, этот параметр имеет **значение NULL**.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если приложение обрабатывает это сообщение, оно должно вернуть ноль.

## <a name="remarks"></a>Комментарии

\_Код запроса SB сумбтракк обычно используется приложениями, которые предоставляют отзыв по мере того, как пользователь перетаскивает ползунок.

Если приложение прокручивает содержимое окна, оно также должно сбрасывать в качестве значения поля прокрутки с помощью функции [**сетскроллпос**](/windows/desktop/api/Winuser/nf-winuser-setscrollpos) .

Обратите внимание, что сообщение **WM \_ VSCROLL** содержит только 16 бит данных о положении поля прокрутки. Поэтому приложения, которые используют только **WM \_ VSCROLL** (и [**WM \_ HSCROLL**](wm-hscroll.md)) для данных о положении прокрутки, имеют практически максимальное значение 65 535.

Однако, поскольку функции [**сетскроллинфо**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo), [**сетскроллпос**](/windows/desktop/api/Winuser/nf-winuser-setscrollpos), [**сетскроллранже**](/windows/desktop/api/Winuser/nf-winuser-setscrollrange), [**жетскроллинфо**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo), [**жетскроллпос**](/windows/desktop/api/Winuser/nf-winuser-getscrollpos)и [**жетскроллранже**](/windows/desktop/api/Winuser/nf-winuser-getscrollrange) поддерживают 32-битные данные о положении полосы прокрутки, существует способ обойти 16-разрядное препятствие сообщений [**WM \_ HSCROLL**](wm-hscroll.md) и **WM \_ VSCROLL** . Описание метода см. в разделе **жетскроллинфо** .

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

[**жетскроллинфо**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo)
</dt> <dt>

[**жетскроллпос**](/windows/desktop/api/Winuser/nf-winuser-getscrollpos)
</dt> <dt>

[**жетскроллранже**](/windows/desktop/api/Winuser/nf-winuser-getscrollrange)
</dt> <dt>

[**сетскроллинфо**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo)
</dt> <dt>

[**сетскроллпос**](/windows/desktop/api/Winuser/nf-winuser-setscrollpos)
</dt> <dt>

[**сетскроллранже**](/windows/desktop/api/Winuser/nf-winuser-setscrollrange)
</dt> <dt>

[**WM \_ HSCROLL**](wm-hscroll.md)
</dt> <dt>

[**WM \_ VSCROLL (TrackBar)**](wm-vscroll--trackbar-.md)
</dt> </dl>

 

