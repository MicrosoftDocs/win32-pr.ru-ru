---
title: Код уведомления WM_VSCROLL (TrackBar) (Winuser. h)
description: Сообщение WM \_ VSCROLL отправляется владельцу элемента управления "вертикальная прокрутка" при изменении положения ползунка. Окно получает это сообщение через функцию WindowProc.
ms.assetid: E491E210-9605-4ABB-A667-471830DA7C2B
keywords:
- коды уведомлений WM_VSCROLL (Trackbar) Windows элементов управления
topic_type:
- apiref
api_name:
- WM_HSCROLL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0dabd6c3c50588c4a9052b0829473352940f0027a1c12d0f3bbc6334e5f13b08
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119077658"
---
# <a name="wm_vscroll-trackbar-notification-code"></a>\_Код уведомления WM VSCROLL (TrackBar)

Сообщение **WM \_ VSCROLL** отправляется владельцу элемента управления "вертикальная прокрутка" при изменении положения ползунка.

Окно получает это сообщение через функцию [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
WM_HSCROLL

    WPARAM wParam
    LPARAM lParam; 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) указывает текущее положение ползунка, если [**ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) — ТБ \_ сумбпоситион или ТБ \_ сумбтракк. Для всех остальных кодов уведомлений слово в высоком порядке имеет нулевое значение; Отправьте сообщение [**ТБМ \_ жетпос**](tbm-getpos.md) , чтобы определить положение ползунка.

[**Ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) указывает код уведомления, указывающий на взаимодействие пользователя с TrackBar. Это слово может принимать одно из следующих значений.



| Значение                                                                                                                                                                  | Значение                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TB_BOTTOM"></span><span id="tb_bottom"></span><dl> <dt>**\_Нижняя ТБ**</dt> </dl>                      | Пользователь нажал на конец ключа ([**VK \_ End**](/windows/desktop/inputdev/virtual-key-codes)).<br/>                                                                                          |
| <span id="TB_ENDTRACK"></span><span id="tb_endtrack"></span><dl> <dt>**\_ЕНДТРАКК ТБ**</dt> </dl>                | Значение TrackBar получило [**WM \_ KEYUP**](/windows/desktop/inputdev/wm-keyup), означающее, что пользователь освободил ключ, который отправил соответствующий виртуальный код клавиши. <br/>                                           |
| <span id="TB_LINEDOWN"></span><span id="tb_linedown"></span><dl> <dt>**\_ЛИНЕДОВН ТБ**</dt> </dl>                | Пользователь нажал клавишу Стрелка вправо ([**VK \_ right**](/windows/desktop/inputdev/virtual-key-codes)) или стрелка вниз ([**VK \_ Down**](/windows/desktop/inputdev/virtual-key-codes)).<br/> |
| <span id="TB_LINEUP"></span><span id="tb_lineup"></span><dl> <dt>**Разметка \_ ТБ**</dt> </dl>                      | Пользователь нажал клавишу Стрелка влево ([**VK \_ Left**](/windows/desktop/inputdev/virtual-key-codes)) или стрелка вверх ([**VK \_ up**](/windows/desktop/inputdev/virtual-key-codes)).<br/>             |
| <span id="TB_PAGEDOWN"></span><span id="tb_pagedown"></span><dl> <dt>**\_PageDown ТБ**</dt> </dl>                | Пользователь щелкнул канал ниже или справа от ползунка ([**VK \_ Далее**](/windows/desktop/inputdev/virtual-key-codes)).<br/>                                                   |
| <span id="TB_PAGEUP"></span><span id="tb_pageup"></span><dl> <dt>**\_PageUp ТБ**</dt> </dl>                      | Пользователь щелкнул канал выше или слева от ползунка ([**VK \_ ранее**](/windows/desktop/inputdev/virtual-key-codes)).<br/>                                                 |
| <span id="TB_THUMBPOSITION"></span><span id="tb_thumbposition"></span><dl> <dt>**\_СУМБПОСИТИОН ТБ**</dt> </dl> | Значение TrackBar, полученное от [**WM \_ лбуттонуп**](/windows/desktop/inputdev/wm-lbuttonup) , после \_ кода уведомления сумбтракк ТБ.<br/>                                                                   |
| <span id="TB_THUMBTRACK"></span><span id="tb_thumbtrack"></span><dl> <dt>**\_СУМБТРАКК ТБ**</dt> </dl>          | Пользователь переместил ползунок.<br/>                                                                                                                                                     |
| <span id="TB_TOP"></span><span id="tb_top"></span><dl> <dt>**\_верхний ТБ**</dt> </dl>                               | Пользователь нажал на ДОМАШНЮЮ клавишу ([**VK \_ Home**](/windows/desktop/inputdev/virtual-key-codes)). <br/>                                                                                     |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Маркер для элемента управления TrackBar.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если приложение обрабатывает это сообщение, оно должно вернуть ноль.

## <a name="remarks"></a>Remarks

\_Код СУМБТРАКК ТБ обычно используется приложениями, которые предоставляют отзыв по мере того, как пользователь перетаскивает ползунок.

Обратите внимание, что сообщение **WM \_ VSCROLL** содержит только 16 бит данных о положении. Таким же, приложения, которые используют только **WM \_ VSCROLL** (и [**WM \_ HSCROLL**](wm-hscroll--trackbar-.md)) для данных о положении ползунка, имеют практически максимальное значение положения 65 535.

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

[**WM \_ HSCROLL**](wm-hscroll--trackbar-.md)
</dt> </dl>

 

