---
title: Сообщение WM_NCRBUTTONDBLCLK (Winuser. h)
description: Размещается, когда пользователь дважды щелкает правую кнопку мыши, когда курсор находится внутри неклиентской области окна. Это сообщение отправляется в окно, содержащее курсор. Если окно захвачено мышью, это сообщение не отправляется.
ms.assetid: 20d62b05-07de-49da-b160-29fa1f5067fa
keywords:
- WM_NCRBUTTONDBLCLK ввода сообщений с клавиатуры и мыши
topic_type:
- apiref
api_name:
- WM_NCRBUTTONDBLCLK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9af62a21da645a265e5264ffae47ad8cb0907ec6fb0106cfb9e7cee97b7f42e3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119666304"
---
# <a name="wm_ncrbuttondblclk-message"></a>\_Сообщение НКРБУТТОНДБЛКЛК WM

Размещается, когда пользователь дважды щелкает правую кнопку мыши, когда курсор находится внутри неклиентской области окна. Это сообщение отправляется в окно, содержащее курсор. Если окно захвачено мышью, это сообщение не отправляется.

Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_NCRBUTTONDBLCLK              0x00A6
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

Для получения сообщений **\_ нкрбуттондблклк WM** в окне не требуется стиль **CS \_ дблклкс** .

Система создает сообщение **WM \_ нкрбуттондблклк** , когда пользователь нажимает, отпускает и снова нажимает правую кнопку мыши в пределах предельного времени двойного щелчка системы. Двойной щелчок правой кнопкой мыши на самом деле приводит к созданию четырех сообщений: [**WM \_ нкрбуттондовн**](wm-ncrbuttondown.md), [**WM \_ Нкрбуттонуп**](wm-ncrbuttonup.md), **WM \_ нкрбуттондблклк** и **WM \_ нкрбуттонуп** .

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

[**WM \_ нкрбуттондовн**](wm-ncrbuttondown.md)
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

 

