---
title: Сообщение WM_CLIPBOARDUPDATE (Winuser. h)
description: Посылается, когда содержимое буфера обмена изменилось.
ms.assetid: 1508aa22-9cf0-40a2-8cb0-ce7c8671df2c
keywords:
- Обмен данными с сообщениями WM_CLIPBOARDUPDATE
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
ms.openlocfilehash: 303110f0d094cfed336a9f92006b3720a0ccc83b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136170"
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

## <a name="remarks"></a>Комментарии

Чтобы зарегистрировать окно для получения этого сообщения, используйте функцию [**аддклипбоардформатлистенер**](/windows/desktop/api/Winuser/nf-winuser-addclipboardformatlistener) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                                           |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (включение Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**аддклипбоардформатлистенер**](/windows/desktop/api/Winuser/nf-winuser-addclipboardformatlistener)
</dt> <dt>

[**ремовеклипбоардформатлистенер**](/windows/desktop/api/Winuser/nf-winuser-removeclipboardformatlistener)
</dt> <dt>

[**жетклипбоардсекуенценумбер**](/windows/desktop/api/Winuser/nf-winuser-getclipboardsequencenumber)
</dt> </dl>

 

 





