---
title: Код уведомления WM_HSCROLL (TrackBar) (Winuser. h)
description: Сообщение WM \_ HSCROLL отправляется владельцу элемента управления "горизонтальная линейка" при изменении положения ползунка. Окно получает это сообщение через функцию WindowProc.
ms.assetid: EC4AF407-E13F-4562-A0A6-FA109C15101B
keywords:
- Элементы управления Windows для кода уведомления WM_HSCROLL (TrackBar)
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
ms.openlocfilehash: 10727b745900520e8af31561236c8e93eeeb3a81
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071554"
---
# <a name="wm_hscroll-trackbar-notification-code"></a>\_Код уведомления WM HSCROLL (TrackBar)

Сообщение **WM \_ HSCROLL** отправляется владельцу элемента управления "горизонтальная линейка" при изменении положения ползунка.

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

## <a name="remarks"></a>Комментарии

\_Код СУМБТРАКК ТБ обычно используется приложениями, которые предоставляют отзыв по мере того, как пользователь перетаскивает ползунок.

Обратите внимание, что сообщение **WM \_ HSCROLL** содержит только 16 бит данных о положении. Таким же, приложения, которые используют только **WM \_ HSCROLL** (и [**WM \_ VSCROLL**](wm-vscroll--trackbar-.md)) для данных о положении ползунка, имеют практически максимальное значение положения 65 535.

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

[**WM \_ VSCROLL**](wm-vscroll--trackbar-.md)
</dt> </dl>

 

