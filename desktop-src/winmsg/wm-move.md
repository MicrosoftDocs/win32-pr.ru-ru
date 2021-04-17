---
description: Посылается после перемещения окна.
ms.assetid: 552ddc26-fe63-449b-8c82-bb927a2c1c41
title: Сообщение WM_MOVE (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56004ec47266a50bf2ac82a828b9046c84a8ebfb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673824"
---
# <a name="wm_move-message"></a>\_Сообщение о перемещении WM

Посылается после перемещения окна.

Окно получает это сообщение через функцию [**WindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) .


```C++
#define WM_MOVE                         0x0003
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Этот параметр не используется.

</dd> <dt>

*lParam* 
</dt> <dd>

Координаты x и y верхнего левого угла клиентской области окна. Слово низкого порядка содержит координату по оси x, в то время как слово с высоким порядком содержит координату y.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **lResult**

Если приложение обрабатывает это сообщение, оно должно вернуть ноль.

## <a name="remarks"></a>Комментарии

Параметры задаются в экранных координатах для перекрывающихся и всплывающих окон, а также в координатах родительского клиента для дочерних окон.

В следующем примере показано, как получить расположение из параметра *lParam* .


```
xPos = (int)(short) LOWORD(lParam);   // horizontal position 
yPos = (int)(short) HIWORD(lParam);   // vertical position 
```



Можно также использовать макрос [**макепоинтс**](/windows/win32/api/wingdi/nf-wingdi-makepoints) для преобразования параметра *lParam* в структуру [**points**](/previous-versions//dd162808(v=vs.85)) .

Функция [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) отправляет сообщения **WM \_ size** и **WM \_ Move** при обработке сообщения [**WM \_ виндовпосчанжед**](wm-windowposchanged.md) .
Сообщения **WM \_ size** и **WM \_ Move** не отправляются, если приложение обрабатывает сообщение **WM \_ виндовпосчанжед** без вызова **дефвиндовпрок**.

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

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**WM \_ виндовпосчанжед**](wm-windowposchanged.md)
</dt> <dt>

**Зрения**
</dt> <dt>

[Windows](windows.md)
</dt> <dt>

**Другие ресурсы**
</dt> <dt>

[**макепоинтс**](/windows/win32/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

[**ТОЧКИ**](/previous-versions//dd162808(v=vs.85))
</dt> </dl>

 

 
