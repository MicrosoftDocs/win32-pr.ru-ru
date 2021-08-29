---
title: Сообщение WM_HSCROLL (Winuser. h)
description: Сообщение WM \_ HSCROLL отправляется в окно при возникновении события прокрутки в стандартной горизонтальной полосе прокрутки окна.
ms.assetid: 197e522f-defd-4356-8521-5b5dfda596da
keywords:
- элементы управления Windows сообщений WM_HSCROLL
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
ms.openlocfilehash: 965ac6841149934142fc4624ad14e327d4b524288c78e9f22fbf1e935c0a1e77
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957503"
---
# <a name="wm_hscroll-message"></a>\_Сообщение HSCROLL WM

Сообщение **WM \_ HSCROLL** отправляется в окно при возникновении события прокрутки в стандартной горизонтальной полосе прокрутки окна. Это сообщение также отправляется владельцу горизонтальной полосы прокрутки при возникновении события прокрутки в элементе управления.

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

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) указывает текущее расположение поля прокрутки, если [**ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) является SB \_ сумбпоситион или SB \_ сумбтракк; в противном случае это слово не используется.

[**Ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) указывает значение полосы прокрутки, которое указывает на запрос прокрутки пользователя. Это слово может принимать одно из следующих значений.



| Значение                                                                                                                                                                  | Значение                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SB_ENDSCROLL"></span><span id="sb_endscroll"></span><dl> <dt>**SB \_ ендскролл**</dt> </dl>             | Завершает прокрутку.<br/>                                                                                                                                                                                                   |
| <span id="SB_LEFT"></span><span id="sb_left"></span><dl> <dt>**поsb, \_ слева**</dt> </dl>                            | Выполняет прокрутку к верхнему левому краю.<br/>                                                                                                                                                                                     |
| <span id="SB_RIGHT"></span><span id="sb_right"></span><dl> <dt>**SB \_ right**</dt> </dl>                         | Прокручивает вниз до нижнего правого.<br/>                                                                                                                                                                                    |
| <span id="SB_LINELEFT"></span><span id="sb_lineleft"></span><dl> <dt>**SB \_ линелефт**</dt> </dl>                | Прокрутка влево на одну единицу.<br/>                                                                                                                                                                                      |
| <span id="SB_LINERIGHT"></span><span id="sb_lineright"></span><dl> <dt>**SB \_ линеригхт**</dt> </dl>             | Выполняет прокрутку вправо на одну единицу.<br/>                                                                                                                                                                                     |
| <span id="SB_PAGELEFT"></span><span id="sb_pageleft"></span><dl> <dt>**SB \_ пажелефт**</dt> </dl>                | Прокрутка влево по ширине окна.<br/>                                                                                                                                                                       |
| <span id="SB_PAGERIGHT"></span><span id="sb_pageright"></span><dl> <dt>**SB \_ пажеригхт**</dt> </dl>             | Прокрутка вправо по ширине окна.<br/>                                                                                                                                                                      |
| <span id="SB_THUMBPOSITION"></span><span id="sb_thumbposition"></span><dl> <dt>**SB \_ сумбпоситион**</dt> </dl> | Пользователь переместил бегунок (бегунок) и отпустил кнопку мыши. [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) указывает на позиции ползунка в конце операции перетаскивания.<br/>                          |
| <span id="SB_THUMBTRACK"></span><span id="sb_thumbtrack"></span><dl> <dt>**SB \_ сумбтракк**</dt> </dl>          | Пользователь перетаскивает полосу прокрутки. Это сообщение отправляется повторно, пока пользователь не отпускает кнопку мыши. [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) указывает на то, куда переместился ползунок полосы прокрутки.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Если сообщение отправляется элементом управления "полоса прокрутки", этот параметр является маркером элемента управления "полоса прокрутки". Если сообщение отправляется стандартной полосой прокрутки, этот параметр имеет **значение NULL**.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если приложение обрабатывает это сообщение, оно должно вернуть ноль.

## <a name="remarks"></a>Remarks

\_Код запроса SB сумбтракк обычно используется приложениями, которые предоставляют отзыв по мере того, как пользователь перетаскивает ползунок.

Если приложение прокручивает содержимое окна, оно также должно сбрасывать в качестве значения поля прокрутки с помощью функции [**сетскроллпос**](/windows/desktop/api/Winuser/nf-winuser-setscrollpos) .

Обратите внимание, что сообщение **WM \_ HSCROLL** содержит только 16 бит данных о положении поля прокрутки. Поэтому приложения, которые используют только **WM \_ HSCROLL** (и [**WM \_ VSCROLL**](wm-vscroll.md)) для данных о положении прокрутки, имеют практически максимальное значение 65 535.

Однако, поскольку функции [**сетскроллинфо**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo), [**сетскроллпос**](/windows/desktop/api/Winuser/nf-winuser-setscrollpos), [**сетскроллранже**](/windows/desktop/api/Winuser/nf-winuser-setscrollrange), [**жетскроллинфо**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo), [**жетскроллпос**](/windows/desktop/api/Winuser/nf-winuser-getscrollpos)и [**жетскроллранже**](/windows/desktop/api/Winuser/nf-winuser-getscrollrange) поддерживают 32-битные данные о положении полосы прокрутки, существует способ обойти 16-разрядное препятствие сообщений **WM \_ HSCROLL** и [**WM \_ VSCROLL**](wm-vscroll.md) . Описание метода см. в разделе **жетскроллинфо** .

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

[**WM \_ HSCROLL (TrackBar)**](wm-hscroll--trackbar-.md)
</dt> <dt>

[**WM \_ VSCROLL**](wm-vscroll.md)
</dt> </dl>

 

