---
Description: Сообщение WM \_ Paint отправляется, когда система или другое приложение выполняет запрос на закрасить часть окна приложения.
ms.assetid: afebaa07-cf00-47db-a919-46436f164881
title: Сообщение WM_PAINT (Winuser. h)
ms.topic: reference
ms.custom: snippet-project
ms.date: 05/31/2018
ms.openlocfilehash: b13e1779fb54a3db7905cb8fc738ef45558400f5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "104987506"
---
# <a name="wm_paint-message"></a>\_Сообщение WM Paint

Сообщение **WM \_ Paint** отправляется, когда система или другое приложение выполняет запрос на закрасить часть окна приложения. Сообщение отправляется, когда вызывается функция [**упдатевиндов**](/windows/desktop/api/Winuser/nf-winuser-updatewindow) или [**Редраввиндов**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow) или функция [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) , когда приложение получает сообщение **WM \_ Paint** с помощью функции WITH [**Message**](/windows/win32/api/winuser/nf-winuser-getmessage) или [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) .

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

Этот параметр не используется.

</dd> <dt>

*lParam* 
</dt> <dd>

Этот параметр не используется.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Приложение возвращает нуль, если обрабатывает это сообщение.

## <a name="example"></a>Например, .

```c
LRESULT CALLBACK WindowProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    switch (uMsg)
    {
    case WM_DESTROY:
        PostQuitMessage(0);
        return 0;

    case WM_PAINT:
        {
            PAINTSTRUCT ps;
            HDC hdc = BeginPaint(hwnd, &ps);

            // All painting occurs here, between BeginPaint and EndPaint.
            FillRect(hdc, &ps.rcPaint, (HBRUSH) (COLOR_WINDOW+1));
            EndPaint(hwnd, &ps);
        }
        return 0;
    }

    return DefWindowProc(hwnd, uMsg, wParam, lParam);
}

```

Пример из [классической выборки Windows](https://github.com/microsoft/Windows-classic-samples/blob/18cbd05ee44455cd7552804dcf2c9d6db619b412/Samples/Win7Samples/begin/LearnWin32/HelloWorld/cpp/main.cpp) на сайте GitHub.

## <a name="remarks"></a>Примечания

Сообщение **WM \_ Paint** создается системой и не должно отправляться приложением. Чтобы заставить окно нарисоваться в конкретном контексте устройства, используйте сообщение [**WM \_ Print**](wm-print.md) или [**WM \_ принтклиент**](wm-printclient.md) . Обратите внимание, что для этого требуется, чтобы целевое окно поддерживало сообщение **WM \_ принтклиент** . Большинство стандартных элементов управления поддерживают сообщение **WM \_ принтклиент** .

Функция [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  проверяет регион обновления. Функция также может отправить сообщение [**WM \_ нкпаинт**](wm-ncpaint.md) в оконную процедуру, если рамка окна должна быть окрашена, и отправить сообщение [**WM \_ ерасебкгнд**](../winmsg/wm-erasebkgnd.md) , если фон окна необходимо стереть.

Система отправляет это сообщение при отсутствии других сообщений в очереди сообщений приложения. [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) определяет, куда отправить сообщение; [**Сообщение о выправке определяет,**](/windows/win32/api/winuser/nf-winuser-getmessage) какое сообщение следует отправлять. Функция **onmessage** возвращает сообщение **WM \_ Paint** , если в очереди сообщений приложения нет других сообщений, а **DispatchMessage** отправляет сообщение в соответствующую процедуру окна.

Окно может получить внутренние сообщения рисования в результате вызова [**редраввиндов**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow) с \_ установленным флагом РДВ интерналпаинт. В этом случае в окне может отсутствовать регион обновления. Приложение может вызвать функцию [**жетупдатерект**](/windows/desktop/api/Winuser/nf-winuser-getupdaterect) , чтобы определить, имеет ли окно регион обновления. Если **жетупдатерект** возвращает ноль, приложению не нужно вызывать функции [**бегинпаинт**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) и [**ендпаинт**](/windows/desktop/api/Winuser/nf-winuser-endpaint) .

Приложение должно проверять все необходимое внутреннее оформление, просматривая внутренние структуры данных для каждого сообщения **WM \_ Paint** , так как сообщение **WM \_ Paint** могло быть вызвано ненулевым регионом обновления и вызовом [**редраввиндов**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow) с \_ установленным флагом РДВ интерналпаинт.

Система отправляет внутреннее сообщение **WM \_ Paint** только один раз. После того как внутреннее сообщение **WM \_ Paint** [**возвращается из метода**](/windows/win32/api/winuser/nf-winuser-getmessage) [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) или отправляется в окно с помощью [**упдатевиндов**](/windows/desktop/api/Winuser/nf-winuser-updatewindow), система не отправляет или не передает последующие сообщения **WM \_ Paint** до тех пор, пока окно не станет недействительным или пока не будет вызван [**редраввиндов**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow) с \_ установленным флагом РДВ интерналпаинт.

Для некоторых стандартных элементов управления обработка сообщений **WM \_ Paint** по умолчанию проверяет параметр *wParam* . Если параметр *wParam* не равен null, то элемент управления предполагает, что значение является HDC и рисует его с помощью контекста устройства.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                               |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                     |
| Заголовок<br/>                   | <dl> <dt>Winuser. h (включение Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Общие сведения о рисовании и рисовании](painting-and-drawing.md)
</dt> <dt>

[Рисование и рисование сообщений](painting-and-drawing-messages.md)
</dt> <dt>

[**бегинпаинт**](/windows/desktop/api/Winuser/nf-winuser-beginpaint)
</dt> <dt>

[**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage)
</dt> <dt>

[**ендпаинт**](/windows/desktop/api/Winuser/nf-winuser-endpaint)
</dt> <dt>

[**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage)
</dt> <dt>

[**жетупдатерект**](/windows/desktop/api/Winuser/nf-winuser-getupdaterect)
</dt> <dt>

[**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea)
</dt> <dt>

[**редраввиндов**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow)
</dt> <dt>

[**упдатевиндов**](/windows/desktop/api/Winuser/nf-winuser-updatewindow)
</dt> <dt>

[**WM \_ ерасебкгнд**](../winmsg/wm-erasebkgnd.md)
</dt> <dt>

[**WM \_ нкпаинт**](wm-ncpaint.md)
</dt> <dt>

[**\_Печать WM**](wm-print.md)
</dt> <dt>

[**WM \_ принтклиент**](wm-printclient.md)
</dt> </dl>

 

 
