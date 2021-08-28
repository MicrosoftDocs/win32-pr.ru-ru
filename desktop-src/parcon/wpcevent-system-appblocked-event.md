---
description: Событие системного уровня, формируемое политиками ограничений программного обеспечения (SRP), если приложение заблокировано более безопасными правилами.
ms.assetid: 6772a2c9-35c1-4b75-94e4-baa84af7c0ed
title: Событие WPCEVENT_SYSTEM_APPBLOCKED (Впцевент. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0444cee0a2844ae868923b5cf51923e0024c9de9a2a12ad51e20d8db9fa3b60
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120112724"
---
# <a name="wpcevent_system_appblocked-event"></a>ВПЦЕВЕНТ \_ System \_ аппблоккед, событие

Событие системного уровня, формируемое политиками ограничений программного обеспечения (SRP), если приложение заблокировано более безопасными правилами.


```C++
const EVENT_DESCRIPTOR WPCEVENT_SYSTEM_APPBLOCKED = {0x10, 0x0, 0x10, 0x4, 0x16, 0x10, 0x8000000000000010};
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*TimeStamp* 
</dt> <dd>

Время, когда произошло блокировка.

</dd> <dt>

*UserID* 
</dt> <dd>

Идентификатор безопасности пользователя, пытающегося запустить приложение.

</dd> <dt>

*Путь* 
</dt> <dd>

Путь к приложению, которое пытается запустить пользователь.

</dd> <dt>

*RuleID* 
</dt> <dd>

Идентификатор правила в наборе более безопасных правил родительского контроля, которые блокируют выполнение.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                             |
| Заголовок<br/>                   | <dl> <dt>Впцевент. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Использование API ведения журнала для родительского контроля](using-logging-apis-for-parental-controls.md)
</dt> <dt>

[**WPC \_ args \_ конверсатионинитевент**](/windows/win32/api/wpcevent/ne-wpcevent-wpc_args_conversationinitevent)
</dt> </dl>

 

 




