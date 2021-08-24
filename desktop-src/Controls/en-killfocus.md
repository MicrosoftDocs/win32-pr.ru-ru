---
title: Код уведомления EN_KILLFOCUS (Winuser. h)
description: Посылается, когда элемент управления "поле ввода" теряет фокус клавиатуры. Родительское окно элемента управления "поле ввода" получает этот код уведомления через \_ командное сообщение WM.
ms.assetid: c31f4b6c-afed-4506-b98a-65c902b0f63a
keywords:
- EN_KILLFOCUS кода уведомления Windows элементы управления
topic_type:
- apiref
api_name:
- EN_KILLFOCUS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d49aaf72df70737ea9d9e61784918c6da1b6fa90d0b96c294570ae5b657e74ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119697374"
---
# <a name="en_killfocus-notification-code"></a>\_Код уведомления EN киллфокус

Посылается, когда элемент управления "поле ввода" теряет фокус клавиатуры. Родительское окно элемента управления "поле ввода" получает этот код уведомления [**через \_ командное сообщение WM**](/windows/desktop/menurc/wm-command) .


```C++
EN_KILLFOCUS

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

[**Ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) содержит идентификатор элемента управления "поле ввода". [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) указывает код уведомления.

</dd> <dt>

*lParam* 
</dt> <dd>

Обработчик для элемента управления "поле ввода".

</dd> </dl>

## <a name="remarks"></a>Remarks

Родительское окно всегда получает [**\_ командное сообщение WM**](/windows/desktop/menurc/wm-command) для этого события, оно не требует отправки маски уведомления с [**\_ SETEVENTMASK EM**](em-seteventmask.md).

**Расширенное редактирование:** Поддерживается в Microsoft Rich Edit 1,0 и более поздних версиях. Дополнительные сведения о совместимости расширенных версий редактирования с различными версиями системы см. в разделе [Общие сведения об элементах управления редактированием](about-rich-edit-controls.md).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                                           |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                                     |
| Заголовок<br/>                   | <dl> <dt>Winuser. h (включает Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

**Ссылки**
</dt> <dt>

[**" \_ en"**](en-setfocus.md)
</dt> <dt>

**Другие ресурсы**
</dt> <dt>

[**\_команда WM**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

