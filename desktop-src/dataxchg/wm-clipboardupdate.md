---
title: Сообщение WM_CLIPBOARDUPDATE (Winuser. h)
description: Посылается, когда содержимое буфера обмена изменилось.
ms.assetid: 1508aa22-9cf0-40a2-8cb0-ce7c8671df2c
keywords:
- WM_CLIPBOARDUPDATE Exchange данных сообщений
topic_type:
- apiref
api_name:
- WM_CLIPBOARDUPDATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0483ba43b6b0c660daee74637fd9f9ac8d377a16097b5cfd60632c1b691ead7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118991224"
---
# <a name="wm_clipboardupdate-message"></a>\_Сообщение КЛИПБОАРДУПДАТЕ WM

Посылается, когда содержимое буфера обмена изменилось.


```C++
#define WM_CLIPBOARDUPDATE              0x031D
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Этот параметр не используется и должен быть равен нулю.

</dd> <dt>

*lParam* 
</dt> <dd>

Этот параметр не используется и должен быть равен нулю.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если приложение обрабатывает это сообщение, оно должно вернуть ноль.

## <a name="remarks"></a>Remarks

Чтобы зарегистрировать окно для получения этого сообщения, используйте функцию [**аддклипбоардформатлистенер**](/windows/desktop/api/Winuser/nf-winuser-addclipboardformatlistener) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                                           |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                                     |
| Заголовок<br/>                   | <dl> <dt>Winuser. h (включает Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**аддклипбоардформатлистенер**](/windows/desktop/api/Winuser/nf-winuser-addclipboardformatlistener)
</dt> <dt>

[**ремовеклипбоардформатлистенер**](/windows/desktop/api/Winuser/nf-winuser-removeclipboardformatlistener)
</dt> <dt>

[**жетклипбоардсекуенценумбер**](/windows/desktop/api/Winuser/nf-winuser-getclipboardsequencenumber)
</dt> </dl>

 

 





