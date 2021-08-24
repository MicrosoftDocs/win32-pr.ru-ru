---
description: Уведомление СПФИЛЕНОТИФИ \_ стартренаме отправляется в функцию обратного вызова, когда очередь запускает операцию переименования файла.
ms.assetid: 005c1840-6aa9-4e94-bfe7-6a9d53735fd9
title: Сообщение SPFILENOTIFY_STARTRENAME (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ec75c84841adf5cb8a187e8d8431f031af74b31f33af7a87e46225b1e9a3464
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119739424"
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
| Минимальная версия клиента<br/> | Windows \[Только классические приложения XP\]<br/>                                           |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Setupapi. h</dt> </dl> |



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

 

