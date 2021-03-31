---
title: Сообщение WM_POINTERDOWN
description: Публикуется, когда указатель устанавливает связь с клиентской областью окна.
ms.assetid: 3bdc37da-227c-4be1-bf0b-99704b8ac000
keywords:
- WM_POINTERDOWN сообщения и уведомления о входе
topic_type:
- apiref
api_name:
- WM_POINTERDOWN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 051e7f0aa08305e4c38d7eefec94483fd11f3bdf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136683"
---
# <a name="wm_pointerdown-message"></a>Сообщение WM_POINTERDOWN

Публикуется, когда указатель устанавливает связь с клиентской областью окна. Это входное сообщение предназначено для окна, для которого указатель устанавливает контакт, и указатель неявно записывается в окно, чтобы окно продолжало принимать входные данные для указателя до тех пор, пока не будет прервано Контактное лицо.

Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .

> \[! Существенно\]  
> Для классических приложений следует учитывать DPI. Если приложение не поддерживает DPI, экранные координаты, содержащиеся в сообщениях указателя и связанных структурах, могут выглядеть неточными из-за виртуализации DPI. Виртуализация DPI обеспечивает автоматическую поддержку масштабирования для приложений, которые не поддерживают DPI и активны по умолчанию (пользователи могут отключить его). Дополнительные сведения см. в статье [написание приложений Win32 с высоким разрешением](/previous-versions//dd464660(v=vs.85)).

 


```C++
#define WM_POINTERDOWN                   0x0246
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

## <a name="remarks"></a>Комментарии

> \[! Существенно\]  
> Когда окно теряет указатель и получает уведомление [**WM_POINTERCAPTURECHANGED**](wm-pointercapturechanged.md) , он обычно не будет получать дальнейшие уведомления. По этой причине важно не делать никаких предположений на основе равномерно связанных **WM_POINTERDOWN** / [**WM_POINTERUP**](wm-pointerup.md) или [**WM_POINTERENTER**](wm-pointerenter.md) / уведомлений [**WM_POINTERLEAVE**](wm-pointerleave.md) .

 

Каждый указатель имеет уникальный идентификатор указателя в течение своего времени существования. Время существования указателя начинается при первом обнаружении.

При обнаружении указателя мыши создается [**WM_POINTERENTER**](wm-pointerenter.md) сообщение. При обнаружении указателя, не являющегося указателем, создается **WM_POINTERDOWN** сообщение, за которым следует сообщение **WM_POINTERENTER** .

Во время его существования указатель может формировать ряд [**WM_POINTERUPDATE**](wm-pointerupdate.md) сообщений при наведении указателя мыши или в контакте.

Время существования указателя заканчивается, когда он больше не обнаруживается. При этом создается [**WM_POINTERLEAVE**](wm-pointerleave.md) сообщение.

При прерывании указателя задается [**POINTER_FLAG_CANCELED**](pointer-flags-contants.md) .

Сообщение [**WM_POINTERLEAVE**](wm-pointerleave.md) также может быть создано, когда незахваченный указатель перемещается за пределы окна.

Для получения горизонтального и вертикального расположения указателя используйте следующую команду:


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam);
```



Чтобы преобразовать параметр lParam в структуру [**points**](/previous-versions//dd162808(v=vs.85)) , используйте макрос [**макепоинтс**](/windows/win32/api/wingdi/nf-wingdi-makepoints) .

Чтобы получить дополнительные сведения, связанные с сообщением, используйте функцию [**жетпоинтеринфо**](/previous-versions/windows/desktop/api) .

Чтобы определить состояния клавиш для модификатора клавиатуры, связанные с этим сообщением, используйте функцию [**жеткэйстате**](/windows/win32/api/winuser/nf-winuser-getkeystate) . Например, чтобы обнаружить, что нажата клавиша ALT, проверьте, не Жеткэйстате ли значение 0 (VK_MENU) &lt; .

Обратите внимание, что если приложение не обрабатывает это сообщение, [**дефвиндовпрок**](/windows/win32/api/winuser/nf-winuser-defwindowproca) может создать одно или несколько [**WM_GESTURE**](../wintouch/wm-gesture.md) сообщений, если последовательность входных данных из этого и, возможно, других указателей распознается как жест. Если жест не распознан, **дефвиндовпрок** может создавать ввод с помощью мыши.

Если приложение выборочно потребляет некоторые входные данные указателя и передает оставшуюся часть в [**дефвиндовпрок**](/windows/win32/api/winuser/nf-winuser-defwindowproca), то результирующее поведение не определено.

Когда окно теряет указатель и получает уведомление [**WM_POINTERCAPTURECHANGED**](wm-pointercapturechanged.md) , обычно он не получает дальнейшие уведомления. Поэтому важно, чтобы окно не принимало никаких предположений о состоянии указателя, независимо от того, будет ли он равномерно связываться с или вводить или ОСТАВЛЯТЬ уведомления.

## <a name="examples"></a>Примеры

В следующем примере кода показано, как использовать [**IS_POINTER_FIRSTBUTTON_WPARAM**](/previous-versions/windows/desktop/api), [**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam), [**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam)и [**IS_POINTER_SECONDBUTTON_WPARAM**](/previous-versions/windows/desktop/api)для получения соответствующих сведений, связанных с сообщением **WM_POINTERDOWN** .


```
int xPos = GET_X_LPARAM(lParam);
int yPos = GET_Y_LPARAM(lParam);

if (IS_POINTER_PRIMARYBUTTON_WPARAM(wParam))
{
    // process pointer down, similar to mouse left button down
}
else if (IS_POINTER_SECONDARYBUTTON_WPARAM(wParam))
{
    // process pointer down, similar to mouse right button down
}
```



В следующем примере кода показано, как использовать [**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api) для получения идентификатора указателя из **WM_POINTERDOWN** сообщения.


```
POINTER_INFO pointerInfo;
UINT32       pointerId = GET_POINTERID_WPARAM(wParam);

// Retrieve common pointer information
if (!GetPointerInfo(pointerId, &amp;pointerInfo))
{
    // failure, call GetLastError()
}
else
{
    // success, process pointerInfo
}
```



В следующем примере кода показано, как управлять различными типами указателей, такими как сенсорный ввод, перо или указывающие устройства по умолчанию.


```
POINTER_TOUCH_INFO   touchInfo;
POINTER_PEN_INFO     penInfo;
POINTER_INFO         pointerInfo;
UINT32               pointerId = GET_POINTERID_WPARAM(wParam);
POINTER_TYPE         pointerType = PT_POINTER;

// default to unhandled to enable call to DefWindowProc
fHandled = FALSE;

if (!GetPointerType(pointerId, &amp;pointerType))
{
    // failure, call GetLastError()
    // set PT_POINTER to fall to default case below
    pointerType = PT_POINTER;
}

switch (pointerType)
{
case PT_TOUCH:
    // Retrieve touch information
    if (!GetPointerTouchInfo(pointerId, &amp;touchInfo))
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
    if (!GetPointerPenInfo(pointerId, &amp;penInfo))
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
    if (!GetPointerInfo(pointerId, &amp;pointerInfo)) 
    {
        // failure.
    } 
    else 
    {
        // success, proceed with pointerInfo.
        fHandled = HandleGenericPointerMessage(&amp;pointerInfo);
    }
    break;
}

```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 8\]<br/>                                                               |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2012\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (включение Windows. h)</dt> </dl> |



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

 

