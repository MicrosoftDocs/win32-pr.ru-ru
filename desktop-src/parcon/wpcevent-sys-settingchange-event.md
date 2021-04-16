---
description: Событие системного уровня, созданное при изменении параметров родительского контроля.
ms.assetid: 2540c3cc-96d0-4e01-a525-4da4a857cb58
title: Событие WPCEVENT_SYS_SETTINGCHANGE (Впцевент. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ea0efb4d68fabcb5f9216c4ccf3bb923ee0ff54
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712853"
---
# <a name="wpcevent_sys_settingchange-event"></a>\_ \_ Событие сеттингчанже впцевент sys

Событие системного уровня, созданное при изменении параметров родительского контроля.


```C++
const EVENT_DESCRIPTOR WPCEVENT_SYS_SETTINGCHANGE = {0x1, 0x0, 0x10, 0x4, 0x15, 0x1, 0x8000000000000010};
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Класс* 
</dt> <dd>

Класс, создающий событие.

</dd> <dt>

*Параметр* 
</dt> <dd>

Значение перечисления **\_ параметров WPC** .

</dd> <dt>

*Владелец* 
</dt> <dd>

Идентификатор безопасности пользователя, создающего событие.

</dd> <dt>

*олдвал* 
</dt> <dd>

Предыдущее значение этого параметра, если оно было удалено или изменено.

</dd> <dt>

*неввал* 
</dt> <dd>

Новое значение этого параметра, если оно добавлено или изменено.

</dd> <dt>

*Причина* 
</dt> <dd>

Значение перечисления [**впкфлаг \_**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) , которое указывает сведения о том, какие события заблокированы и какие элементы управления будут использоваться.

</dd> <dt>

*Необязательный* 
</dt> <dd>

Необязательное поле.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                             |
| Header<br/>                   | <dl> <dt>Впцевент. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Использование API ведения журнала для родительского контроля](using-logging-apis-for-parental-controls.md)
</dt> <dt>

[**WPC \_ args \_ конверсатионинитевент**](/windows/win32/api/wpcevent/ne-wpcevent-wpc_args_conversationinitevent)
</dt> </dl>

 

 




