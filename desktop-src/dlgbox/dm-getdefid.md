---
title: Сообщение DM_GETDEFID (Winuser. h)
description: Извлекает идентификатор элемента управления "Кнопка" по умолчанию для диалогового окна.
ms.assetid: 9f00a494-f5a2-4c4e-a9fc-2220d9326eb9
keywords:
- DM_GETDEFID диалоговых окон сообщений
topic_type:
- apiref
api_name:
- DM_GETDEFID
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6898ed6484a66e1c0d5fa498b0352498c0a57fbe91a74f738e2c6438511aef21
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118785826"
---
# <a name="dm_getdefid-message"></a>\_Сообщение ЖЕТДЕФИД DM

Извлекает идентификатор элемента управления "Кнопка" по умолчанию для диалогового окна.


```C++
#define WM_USER              0x0400
#define DM_GETDEFID         (WM_USER+0)
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

Если существует кнопка отправки по умолчанию, то в верхнем порядке слово возвращаемого значения будет содержаться значение **DC \_ хасдефид** , а в слове с низким порядком — идентификатор элемента управления. В противном случае возвращаемое значение равно нулю.

## <a name="remarks"></a>Remarks

Функция [**дефдлгпрок**](/windows/desktop/api/Winuser/nf-winuser-defdlgprocw) обрабатывает это сообщение.

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

[**дефдлгпрок**](/windows/desktop/api/Winuser/nf-winuser-defdlgprocw)
</dt> <dt>

[**\_СЕТДЕФИД DM**](dm-setdefid.md)
</dt> <dt>

**Зрения**
</dt> <dt>

[Диалоговые окна](dialog-boxes.md)
</dt> </dl>

 

 





