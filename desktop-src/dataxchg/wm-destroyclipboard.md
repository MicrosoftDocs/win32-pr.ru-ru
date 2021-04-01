---
title: Сообщение WM_DESTROYCLIPBOARD (Winuser. h)
description: Отправляется владельцу буфера обмена, когда вызов функции Емптиклипбоард очищает буфер обмена. Окно получает это сообщение через функцию WindowProc.
ms.assetid: 9f75b7fb-e9ae-4876-ba99-7db931b9c2ff
keywords:
- Обмен данными с сообщениями WM_DESTROYCLIPBOARD
topic_type:
- apiref
api_name:
- WM_DESTROYCLIPBOARD
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c3e4b6c2e2d378d0f78cee1824b1e4ce17a433a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989384"
---
# <a name="wm_destroyclipboard-message"></a>\_Сообщение ДЕСТРОЙКЛИПБОАРД WM

Отправляется владельцу буфера обмена, когда вызов функции [**емптиклипбоард**](/windows/desktop/api/Winuser/nf-winuser-emptyclipboard) очищает буфер обмена.

Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_DESTROYCLIPBOARD             0x0307
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

[**емптиклипбоард**](/windows/desktop/api/Winuser/nf-winuser-emptyclipboard)
</dt> <dt>

**Зрения**
</dt> <dt>

[Буфер обмена](clipboard.md)
</dt> </dl>

 

