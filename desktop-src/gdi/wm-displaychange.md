---
description: Сообщение WM \_ дисплайчанже отправляется всем окнам при изменении разрешения экрана.
ms.assetid: 5a6111fd-648e-41a9-aaf8-e5d93f5d54cd
title: Сообщение WM_DISPLAYCHANGE (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d28f5708618ada0d766b140f01ff81a9427f443abb89cf41ba2c743223fbc70
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119037442"
---
# <a name="wm_displaychange-message"></a>\_Сообщение ДИСПЛАЙЧАНЖЕ WM

Сообщение **WM \_ дисплайчанже** отправляется всем окнам при изменении разрешения экрана.

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

Новая глубина изображения для дисплея в битах на пиксель.

</dd> <dt>

*lParam* 
</dt> <dd>

Слово нижнего порядка задает горизонтальное разрешение экрана.

Слово в высоком порядке указывает вертикальное разрешение экрана.

</dd> </dl>

## <a name="remarks"></a>Remarks

Это сообщение отправляется только в окна верхнего уровня. Для всех остальных окон, которые он публикует.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                               |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                     |
| Заголовок<br/>                   | <dl> <dt>Winuser. h (включает Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Общие сведения о рисовании и рисовании](painting-and-drawing.md)
</dt> <dt>

[Рисование и рисование сообщений](painting-and-drawing-messages.md)
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> </dl>

 

 
