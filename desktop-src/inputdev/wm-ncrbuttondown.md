---
title: Сообщение WM_NCRBUTTONDOWN (Winuser. h)
description: Посылается, когда пользователь нажимает правую кнопку мыши, когда курсор находится внутри неклиентской области окна. Это сообщение отправляется в окно, содержащее курсор. Если окно захвачено мышью, это сообщение не отправляется.
ms.assetid: e75e6a65-afca-42c3-ac8b-f665c7534f2d
keywords:
- WM_NCRBUTTONDOWN ввода сообщений с клавиатуры и мыши
topic_type:
- apiref
api_name:
- WM_NCRBUTTONDOWN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6f416cc0f42ead127d7e72c0f46a291b4c30197
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493068"
---
# <a name="wm_ncrbuttondown-message"></a>\_Сообщение НКРБУТТОНДОВН WM

Посылается, когда пользователь нажимает правую кнопку мыши, когда курсор находится внутри неклиентской области окна. Это сообщение отправляется в окно, содержащее курсор. Если окно захвачено мышью, это сообщение не отправляется.

Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_NCRBUTTONDOWN                0x00A4
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

## <a name="remarks"></a>Комментарии

Можно также использовать макросы [**Get \_ X \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) и [**Get \_ Y \_**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) для извлечения значений координат X и y из *lParam*.


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



> [!IMPORTANT]
> Не используйте макросы [**ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) или [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) для извлечения координат x и y позиции курсора, так как эти макросы возвращают неверные результаты в системах с несколькими мониторами. Системы с несколькими мониторами могут иметь отрицательные координаты x и y, а **ловорд** и **HIWORD** обрабатывают координаты как неподписанные количества.

 

Если это уместно, система отправляет сообщение [**WM \_ сискомманд**](/windows/desktop/menurc/wm-syscommand) в окно.

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

[**ПОЛУЧИТЬ \_ X \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[**ПОЛУЧИТЬ \_ lParam для Y \_**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[**WM \_ нчиттест**](wm-nchittest.md)
</dt> <dt>

[**WM \_ нкрбуттондблклк**](wm-ncrbuttondblclk.md)
</dt> <dt>

[**WM \_ нкрбуттонуп**](wm-ncrbuttonup.md)
</dt> <dt>

[**WM \_ сискомманд**](/windows/desktop/menurc/wm-syscommand)
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

 

