---
title: Код уведомления EN_ALIGNRTL (RichEdit. h)
description: Сообщает родительскому окну элемента управления Rich Edit, что направление абзаца изменилось на справа налево. Форматированный элемент управления "поле ввода" отправляет этот код уведомления в виде \_ командного сообщения WM.
ms.assetid: 2db5fd49-9ecd-49d7-8199-1706648255ca
keywords:
- EN_ALIGNRTL кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- EN_ALIGNRTL
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fac2adaa629d00ef940f02f1ed69eb778cdc7813
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489987"
---
# <a name="en_alignrtl-notification-code"></a>\_Код уведомления EN алигнртл

Сообщает родительскому окну элемента управления Rich Edit, что направление абзаца изменилось на справа налево. Форматированный элемент управления "поле ввода" отправляет этот код уведомления в [**виде \_ командного сообщения WM**](/windows/desktop/menurc/wm-command) .


```C++
EN_ALIGNRTL

    WPARAM wParam
    LPARAM lParam;
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

[**Ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) содержит идентификатор элемента управления Rich Edit. [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) указывает код уведомления.

</dd> <dt>

*lParam* 
</dt> <dd>

Обработчик для элемента управления Rich Edit.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот код уведомления не возвращает значение.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Ссылки**
</dt> <dt>

[**EN \_ алигнлтр**](en-alignltr.md)
</dt> <dt>

**Другие ресурсы**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**\_команда WM**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

