---
description: Сообщение WM \_ синкпаинт используется для синхронизации рисования и предотвращения связывания независимых потоков графического пользовательского интерфейса.
ms.assetid: 4446be4e-e0b9-46ce-95b2-bea876348c25
title: Сообщение WM_SYNCPAINT (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5602e867af9b7ce467e8979c9f341758414ad287
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997642"
---
# <a name="wm_syncpaint-message"></a>\_Сообщение СИНКПАИНТ WM

Сообщение **WM \_ синкпаинт** используется для синхронизации рисования и предотвращения связывания независимых потоков графического пользовательского интерфейса.

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

## <a name="remarks"></a>Примечания

При скрытии, отображении, перемещении или изменении размера окна система может определить, что необходимо отправить сообщение **\_ синкпаинт WM** в окна верхнего уровня других потоков. Приложения должны передавать **WM \_ Синкпаинт** в [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  для обработки. Функция **дефвиндовпрок** отправит сообщение [**WM \_ нкпаинт**](wm-ncpaint.md) в оконную процедуру, если фрейм окна необходимо зарисовывать и отправить сообщение [**WM \_ ерасебкгнд**](../winmsg/wm-erasebkgnd.md) , если фон окна необходимо стереть.

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

[**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**жетдцекс**](/windows/desktop/api/Winuser/nf-winuser-getdcex)
</dt> <dt>

[**жетвиндовдк**](/windows/desktop/api/Winuser/nf-winuser-getwindowdc)
</dt> <dt>

[**WM \_ Paint**](wm-paint.md)
</dt> </dl>

 

 
