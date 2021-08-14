---
title: Сообщение WM_NCMOUSEHOVER (Winuser. h)
description: Отправляется в окно при наведении курсора на неклиентскую область окна в течение периода времени, указанного в предыдущем вызове метода TrackMouseEven.
ms.assetid: ca1afdc2-7884-445e-b9b7-4d7dd5dcea38
keywords:
- WM_NCMOUSEHOVER ввода сообщений с клавиатуры и мыши
topic_type:
- apiref
api_name:
- WM_NCMOUSEHOVER
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 323464d32a2529475823003e51d5bbf0b15c616e32edb0622efe5be7f94dfb4c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119611464"
---
# <a name="wm_ncmousehover-message"></a>\_Сообщение НКМАУСЕХОВЕР WM

Отправляется в окно при наведении курсора на неклиентскую область окна в течение периода времени, указанного в предыдущем вызове метода [**TrackMouseEven**](/windows/win32/api/winuser/nf-winuser-trackmouseevent).

Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_NCMOUSEHOVER                 0x02A0
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Значение проверки попадания, возвращаемое функцией [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) в результате обработки сообщения [**WM \_ нчиттест**](wm-nchittest.md) . Список значений проверки попадания см. в разделе **WM \_ нчиттест**.

</dd> <dt>

*lParam* 
</dt> <dd>

Структура [**точек**](/previous-versions//dd162808(v=vs.85)) , содержащая координаты x и y курсора. Координаты задаются относительно левого верхнего угла экрана.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если приложение обрабатывает это сообщение, оно должно вернуть ноль.

## <a name="remarks"></a>Remarks

Отслеживание наведения при наведении останавливается при создании сообщения. Приложение должно вызвать [**TrackMouseEven**](/windows/win32/api/winuser/nf-winuser-trackmouseevent) еще раз, если требуется дальнейшее отслеживание поведения при наведении указателя мыши.

Можно также использовать макросы [**Get \_ X \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) и [**Get \_ Y \_**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) для извлечения значений координат X и y из *lParam*.


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



> [!IMPORTANT]
> Не используйте макросы [**ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) или [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) для извлечения координат x и y позиции курсора, так как эти макросы возвращают неверные результаты в системах с несколькими мониторами. Системы с несколькими мониторами могут иметь отрицательные координаты x и y, а **ловорд** и **HIWORD** обрабатывают координаты как неподписанные количества.

 

## <a name="requirements"></a>Requirements (Требования)



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

[**ПОЛУЧИТЬ \_ X \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[**ПОЛУЧИТЬ \_ lParam для Y \_**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[**TrackMouseEven**](/windows/win32/api/winuser/nf-winuser-trackmouseevent)
</dt> <dt>

[**TRACKMOUSEEVEN**](/windows/win32/api/winuser/ns-winuser-trackmouseevent)
</dt> <dt>

[**WM \_ нчиттест**](wm-nchittest.md)
</dt> <dt>

[**WM \_ маусеховер**](wm-mousehover.md)
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

 

