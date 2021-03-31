---
title: Код уведомления EN_ALIGN_LTR_EC (Winuser. h)
description: Посылается, когда пользователь изменяет направление элемента управления Правка на слева направо. Родительское окно элемента управления "поле ввода" получает этот код уведомления через \_ командное сообщение WM.
ms.assetid: 231f9d00-c5a5-445e-9176-201fe1c14a0e
keywords:
- EN_ALIGN_LTR_EC кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- EN_ALIGN_LTR_EC
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4886c68a024005c4b2fddd71e1480b0a3545bdf1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801894"
---
# <a name="en_align_ltr_ec-notification-code"></a>\_ \_ \_ Код уведомления о выровняйте по правому»

Посылается, когда пользователь изменяет направление элемента управления Правка на слева направо. Родительское окно элемента управления "поле ввода" получает этот код уведомления [**через \_ командное сообщение WM**](/windows/desktop/menurc/wm-command) .


```C++
EN_ALIGN_LTR_EC

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

Маркер элемента управления редактирования, отправляющего код уведомления.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Если в системе установлен двунаправленный язык, например арабский или иврит, можно изменить направление элемента управления редактирования с помощью клавиш CTRL + ЛШИФТ (слева направо) и CTRL + РШИФТ (справа налево).

**Расширенное редактирование:** Этот код уведомления не поддерживается.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                                           |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (включение Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_команда WM**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

