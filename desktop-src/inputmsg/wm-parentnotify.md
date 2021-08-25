---
title: Сообщение WM_PARENTNOTIFY
description: Отправляется в окно при возникновении значительных действий в окне-потомке.
ms.assetid: 4bdc37da-227c-4be1-bf0b-99704caa1444
keywords:
- WM_PARENTNOTIFY сообщения и уведомления о входе
topic_type:
- apiref
api_name:
- WM_PARENTNOTIFY
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 5de0845f906e72a42fa8d9a290c6cd8ac16cc0e96cae21ac25b3e9d7810309e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829574"
---
# <a name="wm_parentnotify-message"></a>Сообщение WM_PARENTNOTIFY

Отправляется в окно при возникновении значительных действий в окне-потомке. Теперь это сообщение расширено для включения события [**WM_POINTERDOWN**](wm-pointerdown.md) . При создании дочернего окна система отправляет [**WM_PARENTNOTIFY**](/previous-versions/windows/desktop/inputmsg/wm-parentnotify) непосредственно перед функцией [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) или [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) , которая создает окно. При уничтожении дочернего окна система отправляет сообщение перед любой обработкой, чтобы уничтожить окно.

Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .

> \[! Существенно\]  
> Для классических приложений следует учитывать DPI. Если приложение не поддерживает DPI, экранные координаты, содержащиеся в сообщениях указателя и связанных структурах, могут выглядеть неточными из-за виртуализации DPI. Виртуализация DPI обеспечивает автоматическую поддержку масштабирования для приложений, которые не поддерживают DPI и активны по умолчанию (пользователи могут отключить его). Дополнительные сведения см. в статье [написание приложений Win32 с высоким разрешением](/previous-versions//dd464660(v=vs.85)).

 


```C++
#define WM_PARENTNOTIFY             0x0210
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Младшее слово параметра *wParam* указывает событие, для которого будет уведомлен родительский объект. Значение слова высокого порядка зависит от значения младшего слова. Этот параметр может принимать одно из указанных ниже значений.



| ЛОВОРД (*wParam*)                                                                                                                                                                                                             | Значение                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WM_CREATE"></span><span id="wm_create"></span><dl> <dt>**WM_CREATE**</dt> <dt>0x0001</dt> </dl>                | Создается дочернее окно.<br/> HIWORD (*wParam*) — это идентификатор дочернего окна.<br/> *lParam* — это маркер дочернего окна.<br/>                                                                                                                                                                                                                          |
| <span id="WM_DESTROY"></span><span id="wm_destroy"></span><dl> <dt>**WM_DESTROY**</dt> <dt>0x0002</dt> </dl>             | Дочернее окно уничтожается.<br/> HIWORD (*wParam*) — это идентификатор дочернего окна.<br/> *lParam* — это маркер дочернего окна.<br/>                                                                                                                                                                                                                        |
| <span id="WM_LBUTTONDOWN"></span><span id="wm_lbuttondown"></span><dl> <dt>**WM_LBUTTONDOWN**</dt> <dt>0x0201</dt> </dl> | Пользователь поместил курсор над дочерним окном и щелкнул левую кнопку мыши.<br/> HIWORD (*wParam*) не определен.<br/> *lParam* — это слово в виде нижнего порядка по оси x, а координата y курсора — это слово в высоком порядке.<br/>                                                                                                       |
| <span id="WM_MBUTTONDOWN"></span><span id="wm_mbuttondown"></span><dl> <dt>**WM_MBUTTONDOWN**</dt> <dt>0x0207</dt> </dl> | Пользователь поместил курсор над дочерним окном и щелкнул среднюю кнопку мыши.<br/> HIWORD (*wParam*) не определен.<br/> *lParam* — это слово в виде нижнего порядка по оси x, а координата y курсора — это слово в высоком порядке.<br/>                                                                                                     |
| <span id="WM_RBUTTONDOWN"></span><span id="wm_rbuttondown"></span><dl> <dt>**WM_RBUTTONDOWN**</dt> <dt>0x0204</dt> </dl> | Пользователь поместил курсор над дочерним окном и щелкнул правой кнопкой мыши.<br/> HIWORD (*wParam*) не определен.<br/> *lParam* — это слово в виде нижнего порядка по оси x, а координата y курсора — это слово в высоком порядке.<br/>                                                                                                      |
| <span id="WM_XBUTTONDOWN"></span><span id="wm_xbuttondown"></span><dl> <dt>**WM_XBUTTONDOWN**</dt> <dt>0x020B</dt> </dl> | Пользователь поместил курсор над дочерним окном и щелкнул первую или вторую кнопку X.<br/> HIWORD (*wParam*) указывает, какая кнопка была нажата. Этот параметр может принимать одно из следующих значений: XBUTTON1 или XBUTTON2.<br/> *lParam* — это слово в виде нижнего порядка по оси x, а координата y курсора — это слово в высоком порядке.<br/> |
| <span id="WM_POINTERDOWN"></span><span id="wm_pointerdown"></span><dl> <dt>**WM_POINTERDOWN**</dt> <dt>0x0246</dt> </dl> | Указатель сделал связь с дочерним окном.<br/> HIWORD (*wParam*) содержит идентификатор указателя, создавшего событие [**WM_POINTERDOWN**](wm-pointerdown.md) .<br/>                                                                                                                                                                                            |



 

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

Если приложение обрабатывает это сообщение, оно возвращает ноль.

Если приложение не обрабатывает это сообщение, оно вызывает [**дефвиндовпрок**](/windows/win32/api/winuser/nf-winuser-defwindowproca).

## <a name="remarks"></a>Remarks

Это сообщение также отправляется во все окна предков дочернего окна, включая окно верхнего уровня.

Все дочерние окна, кроме тех, которые имеют расширенный стиль окна **WS_EX_NOPARENTNOTIFY** , отправляют это сообщение в родительские окна. По умолчанию дочерние окна в диалоговом окне имеют стиль **WS_EX_NOPARENTNOTIFY** , если только не вызвана функция [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) для создания дочернего окна без этого стиля.

Это уведомление предоставляет в качестве предка дочернего окна возможность проверить сведения о указателе и, при необходимости, захватить указатель с помощью функций захвата указателя.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ только классические приложения\]<br/>                                                               |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ только классические приложения\]<br/>                                                     |
| Заголовок<br/>                   | <dl> <dt>Winuser. h (включает Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Сообщения](messages.md)
</dt> <dt>

[**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa)
</dt> <dt>

[**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa)
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**WM_CREATE**](../winmsg/wm-create.md)
</dt> <dt>

[**WM_DESTROY**](../winmsg/wm-destroy.md)
</dt> <dt>

[**WM_LBUTTONDOWN**](../inputdev/wm-lbuttondown.md)
</dt> <dt>

[**WM_MBUTTONDOWN**](../inputdev/wm-mbuttondown.md)
</dt> <dt>

[**WM_RBUTTONDOWN**](../inputdev/wm-rbuttondown.md)
</dt> <dt>

[**WM_XBUTTONDOWN**](../inputdev/wm-xbuttondown.md)
</dt> </dl>

 

