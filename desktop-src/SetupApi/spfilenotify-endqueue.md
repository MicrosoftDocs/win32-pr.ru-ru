---
description: Уведомление СПФИЛЕНОТИФИ \_ ендкуеуе отправляется в подпрограммы обратного вызова после завершения всех операций, поставленных в очередь.
ms.assetid: f4540ab6-edea-4f84-b7eb-4ab3f774068b
title: Сообщение SPFILENOTIFY_ENDQUEUE (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f3ed2ca896f91ec09cb49f89731b41c5d099465
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999507"
---
# <a name="spfilenotify_endqueue-message"></a>\_Сообщение спфиленотифи ендкуеуе

Уведомление **спфиленотифи \_ ендкуеуе** отправляется в подпрограммы обратного вызова после завершения всех операций, поставленных в очередь.


```C++
SPFILENOTIFY_ENDQUEUE
  Param1 = (UINT) Result;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Параметр1* 
</dt> <dd>

**Значение true** , если очередь успешно обработана; в противном случае — **значение false** .

</dd> <dt>

*Param2* 
</dt> <dd>

Не используется.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращаемое значение игнорируется.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows XP\]<br/>                                           |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Setupapi. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Обзор](overview.md)
</dt> <dt>

[Уведомления](notifications.md)
</dt> <dt>

[**сетупкоммитфилекуеуе**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[**сетупдефаулткуеуекаллбакк**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> </dl>

 

 




