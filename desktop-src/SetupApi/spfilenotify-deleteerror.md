---
description: Уведомление СПФИЛЕНОТИФИ \_ делетиррор отправляется в подпрограммы обратного вызова при возникновении ошибки во время операции удаления файла.
ms.assetid: b98b62f0-0b59-430e-966d-c1447026b696
title: Сообщение SPFILENOTIFY_DELETEERROR (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 035b61120bd1343b43c9b6f6d74246eab33cb430
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081528"
---
# <a name="spfilenotify_deleteerror-message"></a>\_Сообщение спфиленотифи делетиррор

Уведомление **спфиленотифи \_ делетиррор** отправляется в подпрограммы обратного вызова при возникновении ошибки во время операции удаления файла.


```C++
SPFILENOTIFY_DELETEERROR
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Параметр1* 
</dt> <dd>

Указатель на структуру [**FilePath**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) .

</dd> <dt>

*Param2* 
</dt> <dd>

Не используется.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Подпрограммы обратного вызова должны возвращать одно из следующих значений.



| Код возврата                                                                                  | Описание                                                                                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**прервать ФИЛЕОП \_**</dt> </dl> | Обработка очереди должна быть отменена. [**Сетупкоммитфилекуеуе**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) возвращает ноль, а [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) Возвращает расширенные сведения об ошибке, такие как ошибка \_ отмены (если пользователь был отменен) или ошибка \_ не \_ хватает \_ памяти.<br/> |
| <dl> <dt>**ФИЛЕОП \_ Повтор**</dt> </dl> | Пользователь пытается выполнить операцию удаления еще раз.<br/>                                                                                                                                                                                                                 |
| <dl> <dt>**ФИЛЕОП \_ пропустить**</dt> </dl>  | Пользователь пропускает операцию удаления файла.<br/>                                                                                                                                                                                                                    |



 

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

[**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)
</dt> <dt>

[**сетупкоммитфилекуеуе**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[**сетупдефаулткуеуекаллбакк**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> </dl>

 

