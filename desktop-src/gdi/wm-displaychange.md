---
description: Сообщение WM \_ дисплайчанже отправляется всем окнам при изменении разрешения экрана.
ms.assetid: 5a6111fd-648e-41a9-aaf8-e5d93f5d54cd
title: Сообщение WM_DISPLAYCHANGE (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 682612529fd40b22481612bb26a954bec45e3901
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104264121"
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

## <a name="remarks"></a>Примечания

Это сообщение отправляется только в окна верхнего уровня. Для всех остальных окон, которые он публикует.

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

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> </dl>

 

 
