---
description: Уведомление СПФИЛЕНОТИФИ \_ стартренаме отправляется в функцию обратного вызова, когда очередь запускает операцию переименования файла.
ms.assetid: 005c1840-6aa9-4e94-bfe7-6a9d53735fd9
title: Сообщение SPFILENOTIFY_STARTRENAME (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36c17d0c70b49ba00b3b16956e7ede5eda43b35b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664076"
---
# <a name="spfilenotify_startrename-message"></a>\_Сообщение спфиленотифи стартренаме

Уведомление **спфиленотифи \_ стартренаме** отправляется в функцию обратного вызова, когда очередь запускает операцию переименования файла.


```C++
SPFILENOTIFY_STARTRENAME
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) Operation;
            
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Параметр1* 
</dt> <dd>

Указатель на структуру [**FilePath**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) .

</dd> <dt>

*Param2* 
</dt> <dd>

Всегда имеет значение ФИЛЕОП \_ Rename.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Подпрограммы обратного вызова должны возвращать одно из следующих значений.



| Код возврата                                                                                  | Описание                                                                                                                                                                                                                                                                                                                                                                     |
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**прервать ФИЛЕОП \_**</dt> </dl> | Прервать фиксацию очереди. Подпрограммы обратного вызова должны вызывать [**сетластеррор**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) для указания причины завершения. [**Сетупкоммитфилекуеуе**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) возвращает **значение false** , и последующий вызов [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) возвращает код ошибки, заданный подпрограммой обратного вызова во время вызова **сетластеррор**.<br/> |
| <dl> <dt>**ФИЛЕОП \_ доит**</dt> </dl>  | Выполните операцию копирования файлов.<br/>                                                                                                                                                                                                                                                                                                                                     |
| <dl> <dt>**ФИЛЕОП \_ пропустить**</dt> </dl>  | Пропустить текущую операцию копирования.<br/>                                                                                                                                                                                                                                                                                                                                     |



 

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

 

