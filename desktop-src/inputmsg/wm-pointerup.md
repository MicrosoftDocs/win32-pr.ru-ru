---
title: Сообщение WM_POINTERUP
description: Публикуется, когда указатель, который подключается через клиентскую область окна, прерывает контакт.
ms.assetid: 3bdc38da-227c-4be1-bf0b-99704b8a0111
keywords:
- WM_POINTERUP сообщения и уведомления о входе
topic_type:
- apiref
api_name:
- WM_POINTERUP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 5bf811501d189abef127e2b191e159518654650bf569cd2abdad42d7471eb1d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118756802"
---
# <a name="wm_pointerup-message"></a>Сообщение WM_POINTERUP

Публикуется, когда указатель, который подключается через клиентскую область окна, прерывает контакт. Это входное сообщение предназначено для окна, над которым указатель устанавливает контакт, и указатель на этот момент неявно записывается в окно, чтобы окно продолжало принимать входные сообщения, включая **WM_POINTERUP** уведомления для указателя, пока не будет прервано Контактное лицо.

Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .

> \[! Существенно\]  
> Для классических приложений следует учитывать DPI. Если приложение не поддерживает DPI, экранные координаты, содержащиеся в сообщениях указателя и связанных структурах, могут выглядеть неточными из-за виртуализации DPI. Виртуализация DPI обеспечивает автоматическую поддержку масштабирования для приложений, которые не поддерживают DPI и активны по умолчанию (пользователи могут отключить его). Дополнительные сведения см. в статье [написание приложений Win32 с высоким разрешением](/previous-versions//dd464660(v=vs.85)).

 


```C++
#define WM_POINTERUP                  0x0247
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Содержит сведения об указателе. Используйте следующие макросы для получения сведений из параметра wParam.

-   [**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)(wParam): идентификатор указателя.
-   [**IS_POINTER_NEW_WPARAM**](/previous-versions/windows/desktop/api)(wParam): флаг, указывающий, представляет ли данное сообщение первый вход, созданный новым указателем.
-   [**IS_POINTER_INRANGE_WPARAM**](/previous-versions/windows/desktop/api)(wParam): флаг, указывающий, было ли это сообщение создано указателем в течение его времени существования. Этот флаг не установлен для сообщений, указывающих на то, что указатель имеет диапазон обнаружения слева
-   [**IS_POINTER_INCONTACT_WPARAM**](/previous-versions/windows/desktop/api)(wParam): флаг, указывающий, было ли это сообщение создано указателем, который находится в связи с областью окна. Этот флаг не задан для сообщений, указывающих на наведение указателя мыши.
-   [**IS_POINTER_PRIMARY_WPARAM**](/previous-versions/windows/desktop/api)(wParam): указывает, что этот указатель был обозначен как первичный.
-   [**IS_POINTER_FIRSTBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): флаг, указывающий, имеется ли первичное действие.
    -   Это аналогично левой кнопке мыши.
    -   В связи с поверхностью дигитайзера этот набор будет иметь сенсорный указатель.
    -   Этот набор будет иметь указатель пера, если он находится в контакте с поверхностью дигитайзера без нажатия кнопок.
-   [**IS_POINTER_SECONDBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): флаг, указывающий, есть ли вторичное действие.
    -   Это аналогично нажатию кнопки мыши.
    -   Этот набор будет иметь указатель пера, если он в связи с поверхностью дигитайзера нажата кнопка пера.
-   [**IS_POINTER_THIRDBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): флаг, указывающий на наличие одного или нескольких третичных действий на основе типа указателя; приложения, которые хотят реагировать на третичные действия, должны получить информацию, относящуюся к типу указателя, чтобы определить, какие из них нажаты. Например, приложение может определить состояния кнопок пера, вызвав [**жетпоинтерпенинфо**](/previous-versions/windows/desktop/api) и изучив флаги, указывающие состояния кнопок.
-   [**IS_POINTER_FOURTHBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): флаг, указывающий, принял ли указанный указатель четвертое действие. Приложения, которые хотят реагировать на четвертые действия, должны получить сведения, относящиеся к типу указателя, чтобы определить, нажата ли первая расширенная кнопка мыши (XButton1).
-   [**IS_POINTER_FIFTHBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): [**флаг**](pointer-flags-contants.md) , указывающий, принял ли указанный указатель пятое действие. Приложения, которые хотят отвечать на пятое действие, должны получить информацию, относящуюся к типу указателя, чтобы определить, нажата ли вторая кнопка расширенной мыши (XButton2).

    Дополнительные сведения см. в разделе [**Флаги указателя**](pointer-flags-contants.md) .

    > [!Note]  
    > Указатель мыши не имеет установленного флага кнопки. Это аналогично перемещению мыши без кнопок мыши. Приложение может определить состояния кнопок для наведения указателя мыши, например путем вызова [**жетпоинтерпенинфо**](/previous-versions/windows/desktop/api) и проверки флагов, указывающих на состояния кнопок.

     

</dd> <dt>

*lParam* 
</dt> <dd>

Содержит расположение точки указателя.

> [!Note]  
> Так как указатель может установить связь с устройством в нетривиальной области, это расположение может быть упрощено более сложной областью указателя. Когда это возможно, приложение должно использовать полные сведения об области указателя, а не расположение точки.

 

Используйте следующие макросы, чтобы получить физические экранные координаты точки.

-   [**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam)(lParam): координата X (горизонтальная точка).
-   [**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam)(lParam): координата Y (вертикальная точка).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если приложение обрабатывает это сообщение, оно должно вернуть ноль.

Если приложение не обрабатывает это сообщение, оно должно вызывать [**дефвиндовпрок**](/windows/win32/api/winuser/nf-winuser-defwindowproca).

## <a name="remarks"></a>Remarks

> \[! Существенно\]  
> Когда окно теряет указатель и получает уведомление [**WM_POINTERCAPTURECHANGED**](wm-pointercapturechanged.md) , он обычно не будет получать дальнейшие уведомления. По этой причине важно не делать никаких предположений на основе равномерно связанных [**WM_POINTERDOWN**](wm-pointerdown.md) / **WM_POINTERUP** или [**WM_POINTERENTER**](wm-pointerenter.md) / уведомлений [**WM_POINTERLEAVE**](wm-pointerleave.md) .

 

Каждый указатель имеет уникальный идентификатор указателя в течение своего времени существования. Время существования указателя начинается при первом обнаружении.

При обнаружении указателя мыши создается [**WM_POINTERENTER**](wm-pointerenter.md) сообщение. При обнаружении указателя, не являющегося указателем, создается [**WM_POINTERDOWN**](wm-pointerdown.md) сообщение, за которым следует сообщение **WM_POINTERENTER** .

Во время его существования указатель может формировать ряд [**WM_POINTERUPDATE**](wm-pointerupdate.md) сообщений при наведении указателя мыши или в контакте.

Время существования указателя заканчивается, когда он больше не обнаруживается. При этом создается [**WM_POINTERLEAVE**](wm-pointerleave.md) сообщение.

При прерывании указателя задается [**POINTER_FLAG_CANCELED**](pointer-flags-contants.md) .

Сообщение [**WM_POINTERLEAVE**](wm-pointerleave.md) также может быть создано, когда незахваченный указатель перемещается за пределы окна.

Для получения горизонтального и вертикального расположения указателя используйте следующую команду:

Чтобы получить горизонтальное и вертикальное расположение, используйте следующий код:


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam);
```



Макрос [**макепоинтс**](/windows/win32/api/wingdi/nf-wingdi-makepoints) также можно использовать для преобразования параметра lParam в структуру [**points**](/previous-versions//dd162808(v=vs.85)) .

Функцию [**жеткэйстате**](/windows/win32/api/winuser/nf-winuser-getkeystate) можно использовать для определения состояний клавиши модификатора клавиатуры, связанных с этим сообщением. Например, чтобы обнаружить, что нажата клавиша ALT, проверьте, не **жеткэйстате** ли значение 0 (VK_MENU) &lt; .

Если приложение не обрабатывает это сообщение, [**дефвиндовпрок**](/windows/win32/api/winuser/nf-winuser-defwindowproca) может создать одно или несколько [**WM_GESTURE**](../wintouch/wm-gesture.md)сообщений, если последовательность входных данных из этого и, возможно, других указателей распознается как жест. Если жест не распознан, **дефвиндовпрок** может создавать ввод с помощью мыши.

Если приложение выборочно потребляет некоторые входные данные указателя и передает оставшуюся часть в [**дефвиндовпрок**](/windows/win32/api/winuser/nf-winuser-defwindowproca), то результирующее поведение не определено.

Используйте функцию [**жетпоинтеринфо**](/previous-versions/windows/desktop/api) для получения дополнительных сведений, относящихся к этому сообщению.

## <a name="examples"></a>Примеры

В следующем примере кода показано, как получить позиции x и y указателя, связанного с данным сообщением.


```
int xPos = GET_X_LPARAM(lParam);
int yPos = GET_Y_LPARAM(lParam);

// process pointer up, similar to mouse button up
```



В следующем примере кода показано, как получить идентификатор указателя, связанный с этим сообщением.


```
POINTER_INFO pointerInfo;
UINT32       pointerId = GET_POINTERID_WPARAM(wParam);

// Retrieve common pointer information
if (!GetPointerInfo(pointerId, &pointerInfo))
{
    
// failure, call GetLastError()
}
else
{
    // success, process pointerInfo
}


```



В следующем примере кода показано, как управлять различными типами указателей, связанными с этим сообщением.


```c++
POINTER_TOUCH_INFO   touchInfo;
POINTER_PEN_INFO     penInfo;
POINTER_INFO pointerInfo;
UINT32       pointerId = GET_POINTERID_WPARAM(wParam);
POINTER_TYPE pointerType = PT_POINTER;

// default to unhandled to enable call to DefWindowProc
fHandled = FALSE;

if (!GetPointerType(pointerId, &pointerType))
{
    // failure, call GetLastError()
    // set PT_POINTER to fall to default case below
    pointerType = PT_POINTER;
}

switch (pointerType)
{
case PT_TOUCH:
    // Retrieve touch information
    if (!GetPointerTouchInfo(pointerId, &touchInfo))
    {
        // failure, call GetLastError()
    }
    else
    {
        // success, process touchInfo
        // mark as handled to skip call to DefWindowProc
        fHandled = TRUE;
    }
    break;
case PT_PEN:
    // Retrieve pen information
    if (!GetPointerPenInfo(pointerId, &penInfo))
    {
        // failure, call GetLastError()
    }
    else
    {
        // success, process penInfo
        // mark as handled to skip call to DefWindowProc
        fHandled = TRUE;
    }
    break;
default:
    if (!GetPointerInfo(pointerId, &pointerInfo)) 
    {
        // failure.
    } 
    else 
    {
        // success, proceed with pointerInfo.
        fHandled = HandleGenericPointerMessage(&pointerInfo);
    }
    break;
}

```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ только классические приложения\]<br/>                                                               |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ только классические приложения\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (включает Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Сообщения](messages.md)
</dt> <dt>

**Ссылки**
</dt> <dt>

[**Флаги указателя**](pointer-flags-contants.md)
</dt> <dt>

[**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)
</dt> <dt>

[**IS_POINTER_NEW_WPARAM**](/previous-versions/windows/desktop/api)
</dt> <dt>

[**IS_POINTER_INRANGE_WPARAM**](/previous-versions/windows/desktop/api)
</dt> <dt>

[**IS_POINTER_INCONTACT_WPARAM**](/previous-versions/windows/desktop/api)
</dt> <dt>

[**IS_POINTER_PRIMARY_WPARAM**](/previous-versions/windows/desktop/api)
</dt> <dt>

[**IS_POINTER_FIRSTBUTTON_WPARAM**](/previous-versions/windows/desktop/api)
</dt> <dt>

[**IS_POINTER_SECONDBUTTON_WPARAM**](/previous-versions/windows/desktop/api)
</dt> <dt>

[**IS_POINTER_THIRDBUTTON_WPARAM**](/previous-versions/windows/desktop/api)
</dt> <dt>

[**IS_POINTER_FOURTHBUTTON_WPARAM**](/previous-versions/windows/desktop/api)
</dt> <dt>

[**IS_POINTER_FIFTHBUTTON_WPARAM**](/previous-versions/windows/desktop/api)
</dt> </dl>
