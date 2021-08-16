---
title: Сообщение WM_XBUTTONDBLCLK (Winuser. h)
description: Посылается, когда пользователь дважды щелкает первую или вторую кнопку X, пока курсор находится в клиентской области окна.
ms.assetid: 68f7abaf-cf6d-499a-957f-3c4d73cdbdee
keywords:
- WM_XBUTTONDBLCLK ввода сообщений с клавиатуры и мыши
topic_type:
- apiref
api_name:
- WM_XBUTTONDBLCLK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48f15ed64871cee3b5a97ad8067e883d7ad31206896f6b20150acdb490a2f44c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118757153"
---
# <a name="wm_xbuttondblclk-message"></a>\_Сообщение КСБУТТОНДБЛКЛК WM

Посылается, когда пользователь дважды щелкает первую или вторую кнопку X, пока курсор находится в клиентской области окна. Если мышь не захвачена, сообщение отправляется в окно под курсором. В противном случае сообщение отправляется в окно, которое захватывает мышь.

Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_XBUTTONDBLCLK                0x020D
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Слово низкого порядка показывает, не отключены ли различные виртуальные ключи. Это может быть одно или несколько из следующих значений.



| Значение                                                                                                                                                                                                               | Значение                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="MK_CONTROL"></span><span id="mk_control"></span><dl> <dt>**MK \_ Управление**</dt> <dt>0x0008</dt> </dl>    | Нажата клавиша CTRL.<br/>            |
| <span id="MK_LBUTTON"></span><span id="mk_lbutton"></span><dl> <dt>**MK \_ ЛБУТТОН**</dt> <dt>0x0001</dt> </dl>    | Левая кнопка мыши не работает.<br/>   |
| <span id="MK_MBUTTON"></span><span id="mk_mbutton"></span><dl> <dt>**MK \_ МБУТТОН**</dt> <dt>0x0010</dt> </dl>    | Средняя кнопка мыши не работает.<br/> |
| <span id="MK_RBUTTON"></span><span id="mk_rbutton"></span><dl> <dt>**MK \_ РБУТТОН**</dt> <dt>0x0002</dt> </dl>    | Нажата правая кнопка мыши.<br/>  |
| <span id="MK_SHIFT"></span><span id="mk_shift"></span><dl> <dt>**MK \_ SHIFT**</dt> <dt>0x0004</dt> </dl>          | Нажата клавиша SHIFT.<br/>           |
| <span id="MK_XBUTTON1"></span><span id="mk_xbutton1"></span><dl> <dt>**MK \_ XBUTTON1**</dt> <dt>0x0020</dt> </dl> | Первая кнопка X не работает.<br/>      |
| <span id="MK_XBUTTON2"></span><span id="mk_xbutton2"></span><dl> <dt>**MK \_ XBUTTON2**</dt> <dt>0x0040</dt> </dl> | Вторая кнопка X не работает.<br/>     |



 

Слово в высоком порядке указывает на то, какая кнопка была двойным щелчком. Может быть одним из указанных далее.



| Значение                                                                                                                                                                                                     | Значение                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <span id="XBUTTON1"></span><span id="xbutton1"></span><dl> <dt>**XBUTTON1**</dt> <dt>0x0001</dt> </dl> | Первая кнопка X была двойным щелчком.<br/>  |
| <span id="XBUTTON2"></span><span id="xbutton2"></span><dl> <dt>**XBUTTON2**</dt> <dt>0x0002</dt> </dl> | Вторая кнопка X была двойным щелчком.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Слово нижнего порядка Указывает координату x курсора. Координата задается относительно левого верхнего угла клиентской области.

Слово в высоком порядке Указывает координату y курсора. Координата задается относительно левого верхнего угла клиентской области.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если приложение обрабатывает это сообщение, оно должно возвращать **значение true**. Дополнительные сведения об обработке возвращаемого значения см. в разделе "Примечания".

## <a name="remarks"></a>Remarks

Используйте следующий код, чтобы получить сведения в параметре *wParam* :


```
fwKeys = GET_KEYSTATE_WPARAM (wParam); 
fwButton = GET_XBUTTON_WPARAM (wParam); 
```



Чтобы получить горизонтальное и вертикальное расположение, используйте следующий код:


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



Как отмечалось выше, координата x находится в низком порядке в **коротком** значении возвращаемого значения; Координата y находится в **высоком порядке (** оба представляют значения *со знаком* , так как они могут принимать отрицательные значения в системах с несколькими мониторами). Если возвращаемое значение присваивается переменной, можно использовать макрос [**макепоинтс**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) для получения структуры [**points**](/previous-versions//dd162808(v=vs.85)) из возвращаемого значения. Для извлечения координат x или y можно также использовать макрос [**Get \_ x \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) или [**Get \_ Y \_**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) .

> [!IMPORTANT]
> Не используйте макросы [**ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) или [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) для извлечения координат x и y позиции курсора, так как эти макросы возвращают неверные результаты в системах с несколькими мониторами. Системы с несколькими мониторами могут иметь отрицательные координаты x и y, а **ловорд** и **HIWORD** обрабатывают координаты как неподписанные количества.

 

Только окна с стилем **CS \_ дблклкс** могут получить сообщения **WM \_ ксбуттондблклк** , которые система создает каждый раз, когда пользователь нажимает, отпускает и снова нажимает кнопку X в пределах времени двойного щелчка системы. Двойной щелчок одной из этих кнопок на самом деле приводит к созданию четырех сообщений: [**WM \_ ксбуттондовн**](wm-xbuttondown.md), [**WM \_ Ксбуттонуп**](wm-xbuttonup.md), **WM \_ ксбуттондблклк** и **WM \_ ксбуттонуп** .

В отличие от [**сообщений \_ WM лбуттондблклк**](wm-lbuttondblclk.md), [**WM \_ мбуттондблклк**](wm-mbuttondblclk.md)и [**WM \_ рбуттондблклк**](wm-rbuttondblclk.md) , приложение должно вернуть **значение true** из этого сообщения, если оно обрабатывает его. это позволит программному обеспечению имитировать это сообщение в Windows системах, предшествующих Windows 2000, чтобы определить, обрабатывала ли окно сообщение или вызываемое [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) для его обработки.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                                |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                      |
| Заголовок<br/>                   | <dl> <dt>Winuser. h (включение Виндовскс. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Ссылки**
</dt> <dt>

[**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**ПОЛУЧЕНИЕ \_ кэйстате \_ wParam**](/windows/win32/api/winuser/nf-winuser-get_keystate_wparam)
</dt> <dt>

[**ПОЛУЧИТЬ \_ X \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[**ПОЛУЧЕНИЕ \_ ксбуттон \_ wParam**](/windows/win32/api/winuser/nf-winuser-get_xbutton_wparam)
</dt> <dt>

[**ПОЛУЧИТЬ \_ lParam для Y \_**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[**Захват**](/windows/win32/api/winuser/nf-winuser-getcapture)
</dt> <dt>

[**жетдаублекликктиме**](/windows/win32/api/winuser/nf-winuser-getdoubleclicktime)
</dt> <dt>

[**сетдаублекликктиме**](/windows/win32/api/winuser/nf-winuser-setdoubleclicktime)
</dt> <dt>

[**WM \_ ксбуттондовн**](wm-xbuttondown.md)
</dt> <dt>

[**WM \_ ксбуттонуп**](wm-xbuttonup.md)
</dt> <dt>

**Зрения**
</dt> <dt>

[Ввод с помощью мыши](mouse-input.md)
</dt> <dt>

**Другие ресурсы**
</dt> <dt>

[**макепоинтс**](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

[**ТОЧКИ**](/previous-versions//dd162808(v=vs.85))
</dt> </dl>

 

