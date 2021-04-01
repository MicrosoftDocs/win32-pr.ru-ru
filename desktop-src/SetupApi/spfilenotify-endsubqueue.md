---
description: Уведомление СПФИЛЕНОТИФИ \_ ендсубкуеуе отправляется в функцию обратного вызова, когда очередь завершает все операции в подочереди DELETE, Rename или Copy.
ms.assetid: 76bd027a-0f00-46e3-b502-0c97827308a8
title: Сообщение SPFILENOTIFY_ENDSUBQUEUE (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7eadc7546487b308313b7cb31088a22420e27af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081526"
---
# <a name="spfilenotify_endsubqueue-message"></a>\_Сообщение спфиленотифи ендсубкуеуе

Уведомление **спфиленотифи \_ ендсубкуеуе** отправляется в функцию обратного вызова, когда очередь завершает все операции в подочереди DELETE, Rename или Copy.


```C++
SPFILENOTIFY_ENDSUBQUEUE
  Param1 = (UINT) SubQueue;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Параметр1* 
</dt> <dd>

Подочередь, которая была завершена. Этот параметр может принимать одно из следующих значений: ФИЛЕОП \_ DELETE, филеоп \_ Rename или филеоп \_ Copy.

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

 

 




