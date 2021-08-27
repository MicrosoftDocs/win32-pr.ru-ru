---
description: Уведомление СПФИЛЕНОТИФИ \_ старткуеуе отправляется в подпрограммы обратного вызова при запуске процесса обязательства очереди.
ms.assetid: 682c2ce0-0c82-402c-a487-db5f2c377f3f
title: Сообщение SPFILENOTIFY_STARTQUEUE (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a40d4fedde850d975edd697423339c686fe697911b9bef2fdc252baffda0158f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073214"
---
# <a name="spfilenotify_startqueue-message"></a>\_Сообщение спфиленотифи старткуеуе

Уведомление **спфиленотифи \_ старткуеуе** отправляется в подпрограммы обратного вызова при запуске процесса обязательства очереди.


```C++
SPFILENOTIFY_STARTQUEUE
  Param1 = (UINT) OwnerWindow;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Параметр1* 
</dt> <dd>

Обработчик для окна, который должен владеть диалоговыми окнами, создаваемыми подпрограммыми обратного вызова.

</dd> <dt>

*Param2* 
</dt> <dd>

Не используется.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

При возникновении ошибки подпрограммы обратного вызова должны вызвать [**сетластеррор**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror), указав ошибку, а затем вернуть ноль. Функция [**сетупкоммитфилекуеуе**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) вернет **значение false** , а последующий вызов [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) возвратит код ошибки, заданный подпрограммой обратного вызова.

Если ошибка не возникает, подпрограммы обратного вызова должны возвращать ненулевое значение.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения XP\]<br/>                                           |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Setupapi. h</dt> </dl> |



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

 

