---
description: Посылается после перемещения окна.
ms.assetid: 552ddc26-fe63-449b-8c82-bb927a2c1c41
title: Сообщение WM_MOVE (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84c18d7a4f4411f45a3338a057a60942d01905ccefd25b40ee511d3b8a5d915d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119810474"
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

## <a name="remarks"></a>Remarks

Параметры задаются в экранных координатах для перекрывающихся и всплывающих окон, а также в координатах родительского клиента для дочерних окон.

В следующем примере показано, как получить расположение из параметра *lParam* .


```
xPos = (int)(short) LOWORD(lParam);   // horizontal position 
yPos = (int)(short) HIWORD(lParam);   // vertical position 
```



Можно также использовать макрос [**макепоинтс**](/windows/win32/api/wingdi/nf-wingdi-makepoints) для преобразования параметра *lParam* в структуру [**points**](/previous-versions//dd162808(v=vs.85)) .

Функция [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) отправляет сообщения **WM \_ size** и **WM \_ Move** при обработке сообщения [**WM \_ виндовпосчанжед**](wm-windowposchanged.md) .
Сообщения **WM \_ size** и **WM \_ Move** не отправляются, если приложение обрабатывает сообщение **WM \_ виндовпосчанжед** без вызова **дефвиндовпрок**.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                               |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                     |
| Заголовок<br/>                   | <dl> <dt>Winuser. h (включает Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также

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

 

 
