---
description: Посылается в окно после того, как оно выйдет из модального цикла перемещения или изменения размера.
ms.assetid: 3466bfb5-c38d-49d8-a4ab-bf23d09c454c
title: Сообщение WM_EXITSIZEMOVE (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f451e846f2a262a30ccc73121d52c3732dbdfb160fe529535dcf353f077c351
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117849256"
---
# <a name="wm_exitsizemove-message"></a>\_Сообщение ЕКСИТСИЗЕМОВЕ WM

Посылается в окно после того, как оно выйдет из модального цикла перемещения или изменения размера. Окно перемещается в модальный цикл перемещения или изменения размера, когда пользователь щелкает заголовок окна или границу изменения размера, или когда окно передает сообщение [**WM \_ сискомманд**](../menurc/wm-syscommand.md) в функцию [**Дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) , а параметр *wParam* сообщения указывает значение **SC \_ MOV** E или **SC \_ size** . Операция завершается, когда [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) возвращает.

Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_EXITSIZEMOVE                 0x0232
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

Тип: **lResult**

Приложение должно вернуть нуль, если оно обрабатывает это сообщение.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                               |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                     |
| Заголовок<br/>                   | <dl> <dt>Winuser. h (включает Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Ссылки**
</dt> <dt>

[**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**WM \_ ентерсиземове**](wm-entersizemove.md)
</dt> <dt>

**Зрения**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
