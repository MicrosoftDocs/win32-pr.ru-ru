---
description: Посылается окну после того, как оно попадает в модальный цикл перемещения или изменения размера.
ms.assetid: fe09db71-2c79-47f2-b575-516e960915d4
title: Сообщение WM_ENTERSIZEMOVE (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfaf27c888311991b88278a9d4e69482efd06111
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702577"
---
# <a name="wm_entersizemove-message"></a>\_Сообщение ЕНТЕРСИЗЕМОВЕ WM

Посылается окну после того, как оно попадает в модальный цикл перемещения или изменения размера. Окно перемещается в модальный цикл перемещения или изменения размера, когда пользователь щелкает заголовок окна или границу изменения размера, или когда окно передает сообщение [**WM \_ сискомманд**](../menurc/wm-syscommand.md) в функцию [**Дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) , а параметр *wParam* сообщения указывает значение **SC \_ Move** или **SC \_ size** . Операция завершается, когда [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) возвращает.

Система отправляет сообщение **WM \_ ентерсиземове** независимо от того, включено ли перетаскивание всех окон.

Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_ENTERSIZEMOVE                0x0231
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
| Заголовок<br/>                   | <dl> <dt>Winuser. h (включение Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Ссылки**
</dt> <dt>

[**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**WM \_ екситсиземове**](wm-exitsizemove.md)
</dt> <dt>

[**WM \_ сискомманд**](../menurc/wm-syscommand.md)
</dt> <dt>

**Зрения**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
