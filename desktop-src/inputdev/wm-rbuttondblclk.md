---
title: Сообщение WM_RBUTTONDBLCLK (Winuser. h)
description: Размещается, когда пользователь дважды щелкает правую кнопку мыши, когда курсор находится в клиентской области окна.
ms.assetid: 2db9a947-f052-4738-9fae-6ecaba3de9b9
keywords:
- WM_RBUTTONDBLCLK ввода сообщений с клавиатуры и мыши
topic_type:
- apiref
api_name:
- WM_RBUTTONDBLCLK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4b2ee4722825f0404d590d593a2c7f72c815f8cfd2ad4991b0a604c188bfbfb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829874"
---
# <a name="wm_rbuttondblclk-message"></a>\_Сообщение РБУТТОНДБЛКЛК WM

Размещается, когда пользователь дважды щелкает правую кнопку мыши, когда курсор находится в клиентской области окна. Если мышь не захвачена, сообщение отправляется в окно под курсором. В противном случае сообщение отправляется в окно, которое захватывает мышь.

Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_RBUTTONDBLCLK                0x0206
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Указывает, работают ли различные виртуальные ключи. Этот параметр может принимать одно или несколько следующих значений.



| Значение                                                                                                                                                                                                               | Значение                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="MK_CONTROL"></span><span id="mk_control"></span><dl> <dt>**MK \_ Управление**</dt> <dt>0x0008</dt> </dl>    | Нажата клавиша CTRL.<br/>            |
| <span id="MK_LBUTTON"></span><span id="mk_lbutton"></span><dl> <dt>**MK \_ ЛБУТТОН**</dt> <dt>0x0001</dt> </dl>    | Левая кнопка мыши не работает.<br/>   |
| <span id="MK_MBUTTON"></span><span id="mk_mbutton"></span><dl> <dt>**MK \_ МБУТТОН**</dt> <dt>0x0010</dt> </dl>    | Средняя кнопка мыши не работает.<br/> |
| <span id="MK_RBUTTON"></span><span id="mk_rbutton"></span><dl> <dt>**MK \_ РБУТТОН**</dt> <dt>0x0002</dt> </dl>    | Нажата правая кнопка мыши.<br/>  |
| <span id="MK_SHIFT"></span><span id="mk_shift"></span><dl> <dt>**MK \_ SHIFT**</dt> <dt>0x0004</dt> </dl>          | Нажата клавиша SHIFT.<br/>           |
| <span id="MK_XBUTTON1"></span><span id="mk_xbutton1"></span><dl> <dt>**MK \_ XBUTTON1**</dt> <dt>0x0020</dt> </dl> | Первая кнопка X не работает.<br/>      |
| <span id="MK_XBUTTON2"></span><span id="mk_xbutton2"></span><dl> <dt>**MK \_ XBUTTON2**</dt> <dt>0x0040</dt> </dl> | Вторая кнопка X не работает.<br/>     |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Слово нижнего порядка Указывает координату x курсора. Координата задается относительно левого верхнего угла клиентской области.

Слово в высоком порядке Указывает координату y курсора. Координата задается относительно левого верхнего угла клиентской области.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если приложение обрабатывает это сообщение, оно должно вернуть ноль.

## <a name="remarks"></a>Remarks

Только окна с стилем **CS \_ дблклкс** могут получить сообщения **WM \_ рбуттондблклк** , которые система создает каждый раз, когда пользователь нажимает, отпускает и снова нажимает правую кнопку мыши в пределах предельного времени двойного щелчка системы. Двойной щелчок правой кнопкой мыши на самом деле приводит к созданию четырех сообщений: [**WM \_ рбуттондовн**](wm-rbuttondown.md), [**WM \_ Рбуттонуп**](wm-rbuttonup.md), **WM \_ рбуттондблклк** и **WM \_ рбуттонуп** .

Чтобы получить горизонтальное и вертикальное расположение, используйте следующий код:


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



Как отмечалось выше, координата x находится в низком порядке в **коротком** значении возвращаемого значения; Координата y находится в **высоком порядке (** оба представляют значения *со знаком* , так как они могут принимать отрицательные значения в системах с несколькими мониторами). Если возвращаемое значение присваивается переменной, можно использовать макрос [**макепоинтс**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) для получения структуры [**points**](/previous-versions//dd162808(v=vs.85)) из возвращаемого значения. Для извлечения координат x или y можно также использовать макрос [**Get \_ x \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) или [**Get \_ Y \_**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) .

> [!IMPORTANT]
> Не используйте макросы [**ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) или [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) для извлечения координат x и y позиции курсора, так как эти макросы возвращают неверные результаты в системах с несколькими мониторами. Системы с несколькими мониторами могут иметь отрицательные координаты x и y, а **ловорд** и **HIWORD** обрабатывают координаты как неподписанные количества.

 

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

[**ПОЛУЧИТЬ \_ X \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[**ПОЛУЧИТЬ \_ lParam для Y \_**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[**Захват**](/windows/win32/api/winuser/nf-winuser-getcapture)
</dt> <dt>

[**жетдаублекликктиме**](/windows/win32/api/winuser/nf-winuser-getdoubleclicktime)
</dt> <dt>

[**сеткаптуре**](/windows/win32/api/winuser/nf-winuser-setcapture)
</dt> <dt>

[**сетдаублекликктиме**](/windows/win32/api/winuser/nf-winuser-setdoubleclicktime)
</dt> <dt>

[**WM \_ рбуттондовн**](wm-rbuttondown.md)
</dt> <dt>

[**WM \_ рбуттонуп**](wm-rbuttonup.md)
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

 

