---
description: Уведомление СПФИЛЕНОТИФИ \_ стартсубкуеуе отправляется в функцию обратного вызова, когда очередь начинает обработку операций в подочереди DELETE, Rename или Copy.
ms.assetid: 4f971549-8f79-4995-9796-1177c3a3c416
title: Сообщение SPFILENOTIFY_STARTSUBQUEUE (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30e4f20440c12e7fcd1900cd9762a504a26b907f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664455"
---
# <a name="spfilenotify_startsubqueue-message"></a>\_Сообщение спфиленотифи стартсубкуеуе

Уведомление **спфиленотифи \_ стартсубкуеуе** отправляется в функцию обратного вызова, когда очередь начинает обработку операций в подочереди DELETE, Rename или Copy.


```C++
SPFILENOTIFY_STARTSUBQUEUE
  Param1 = (UINT) SubQueue;
  Param2 = (UINT) NumOperations;
            
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Параметр1* 
</dt> <dd>

Подочередь, которая была запущена. Этот параметр может иметь одно из значений ФИЛЕОП \_ DELETE, филеоп \_ Rename или филеоп \_ Copy.

</dd> <dt>

*Param2* 
</dt> <dd>

Число операций копирования, переименования или удаления файлов во вложенной очереди.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

При возникновении ошибки подпрограммы обратного вызова должны вызвать [**сетластеррор**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror), указав ошибку, а затем вернуть ноль. Функция [**сетупкоммитфилекуеуе**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) вернет **значение false** , а последующий вызов [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) возвратит код ошибки, заданный подпрограммой обратного вызова.

Если ошибка не возникает, подпрограммы обратного вызова должны возвращать ненулевое значение.

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

 

