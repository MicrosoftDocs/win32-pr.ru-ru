---
title: Сообщение WM_CONTEXTMENU (Winuser. h)
description: Уведомляет окно, что пользователь щелкнул правой кнопкой мыши в окне.
ms.assetid: e607a61a-0f9b-4d11-b8c0-b01a2e7fb35b
keywords:
- WM_CONTEXTMENU меню сообщений и других ресурсов
topic_type:
- apiref
api_name:
- WM_CONTEXTMENU
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff7764926709bfc8ab6aa95be330a9d45d38bc48
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105710479"
---
# <a name="wm_contextmenu-message"></a>\_Сообщение WM CONTEXTMENU

Уведомляет окно о том, что пользователь хочет отобразить контекстное меню.  Пользователь мог щелкнуть правой кнопкой мыши в окне, нажать Shift + F10 или нажал клавишу приложения (раздел контекстного меню) на некоторых клавиатурах.


```C++
#define WM_CONTEXTMENU                  0x007B
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Указатель на окно, в котором пользователь щелкнул правой кнопкой мыши. Это может быть дочернее окно окна, получающего сообщение. Дополнительные сведения об обработке этого сообщения см. в разделе "Примечания".

</dd> <dt>

*lParam* 
</dt> <dd>

Слово нижнего порядка задает горизонтальное расположение курсора в экранных координатах во время щелчка мышью.

Слово в высоком порядке задает вертикальное расположение курсора в экранных координатах во время щелчка мышью.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Нет возвращаемого значения.

## <a name="remarks"></a>Комментарии

Окно может обработать это сообщение, отображая контекстное меню с помощью функций [**метод TrackPopupMenu**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenu) или [**траккпопупменуекс**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex) . Чтобы получить горизонтальные и вертикальные позиции, используйте следующий код.


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



Если окно не отображает контекстное меню, оно должно передать это сообщение функции [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) . Если окно является дочерним, **дефвиндовпрок** отправляет сообщение родительскому окну. В противном случае **дефвиндовпрок** отображает контекстное меню по умолчанию, если указанное расположение находится в заголовке окна.

[**Дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) создает сообщение **WM \_ CONTEXTMENU** при обработке сообщения [**WM \_ рбуттонуп**](/windows/desktop/inputdev/wm-rbuttonup) или [**WM \_ нкрбуттонуп**](/windows/desktop/inputdev/wm-ncrbuttonup) или когда пользователь вводит Shift + F10. Сообщение **WM \_ CONTEXTMENU** также создается, когда пользователь нажимает и отпускает ключ [**VK \_ Apps**](/windows/desktop/inputdev/virtual-key-codes) .

Если контекстное меню создается на основе клавиатуры, например, если пользователь вводит SHIFT + F10, координаты x и y равны-1, и приложение должно отобразить контекстное меню в месте текущего выделения, а не в (Кспос, ИПОС).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                               |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                     |
| Заголовок<br/>                   | <dl> <dt>Winuser. h (включение Windows. h)</dt> </dl> |



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

[**Метод TrackPopupMenu**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenu)
</dt> <dt>

[**траккпопупменуекс**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex)
</dt> <dt>

[**WM \_ нкрбуттонуп**](/windows/desktop/inputdev/wm-ncrbuttonup)
</dt> <dt>

[**WM \_ рбуттонуп**](/windows/desktop/inputdev/wm-rbuttonup)
</dt> <dt>

**Зрения**
</dt> <dt>

[Меню](menus.md)
</dt> </dl>

 

