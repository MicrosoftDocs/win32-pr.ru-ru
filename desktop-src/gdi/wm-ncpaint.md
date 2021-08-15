---
description: Сообщение WM \_ нкпаинт отправляется в окно, когда его кадр должен быть окрашен.
ms.assetid: d8a2a8b9-2c5d-484c-be09-67eb33de67c0
title: Сообщение WM_NCPAINT (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6be5fa951d50dbaf8663e34a5d9476ecb62576c203095bed9427dcef44425690
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118978004"
---
# <a name="wm_ncpaint-message"></a>\_Сообщение НКПАИНТ WM

Сообщение **WM \_ нкпаинт** отправляется в окно, когда его кадр должен быть окрашен.

Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd, 
  UINT  uMsg, 
  WPARAM wParam, 
  LPARAM lParam     
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Маркер области обновления окна. Регион обновления обрезается по рамке окна.

</dd> <dt>

*lParam* 
</dt> <dd>

Этот параметр не используется.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Приложение возвращает нуль, если обрабатывает это сообщение.

## <a name="remarks"></a>Remarks

Функция [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) закрашивает рамку окна.

Приложение может перехватить **сообщение \_ нкпаинт WM** и закрасить собственную настраиваемую рамку окна. Область обрезки для окна всегда прямоугольная, даже при изменении формы рамки.

Значение *wParam* можно передать в [**жетдцекс**](/windows/desktop/api/Winuser/nf-winuser-getdcex) , как показано в следующем примере.


```C++
case WM_NCPAINT:
{
    HDC hdc;
    hdc = GetDCEx(hwnd, (HRGN)wParam, DCX_WINDOW|DCX_INTERSECTRGN);
    // Paint into this DC 
    ReleaseDC(hwnd, hdc);
}
```



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                               |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                     |
| Заголовок<br/>                   | <dl> <dt>Winuser. h (включает Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Общие сведения о рисовании и рисовании](painting-and-drawing.md)
</dt> <dt>

[Рисование и рисование сообщений](painting-and-drawing-messages.md)
</dt> <dt>

[**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**жетвиндовдк**](/windows/desktop/api/Winuser/nf-winuser-getwindowdc)
</dt> <dt>

[**WM \_ Paint**](wm-paint.md)
</dt> <dt>

[**жетдцекс**](/windows/desktop/api/Winuser/nf-winuser-getdcex)
</dt> </dl>

 

 
