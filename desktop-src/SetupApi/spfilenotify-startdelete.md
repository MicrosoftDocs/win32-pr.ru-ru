---
description: Уведомление СПФИЛЕНОТИФИ \_ стартделете отправляется в функцию обратного вызова, когда очередь начинает операцию удаления файла.
ms.assetid: 244714ad-dde7-4b5a-b3f3-78aa4cc901f5
title: Сообщение SPFILENOTIFY_STARTDELETE (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a4a0d362a1c1c3824154fb02e0bb9cf01b24d16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546386"
---
# <a name="spfilenotify_startdelete-message"></a>\_Сообщение спфиленотифи стартделете

Уведомление **спфиленотифи \_ стартделете** отправляется в функцию обратного вызова, когда очередь начинает операцию удаления файла.


```C++
SPFILENOTIFY_STARTDELETE
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

Всегда имеет значение ФИЛЕОП \_ Delete.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Подпрограммы обратного вызова должны возвращать одно из следующих значений.



| Код возврата                                                                                  | Описание                                                                                                                                                                                                                                                                                                                                                                  |
|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**прервать ФИЛЕОП \_**</dt> </dl> | Прервать фиксацию очереди. Подпрограммы обратного вызова должны вызывать [**сетластеррор**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) для указания причины прерывания. [**Сетупкоммитфилекуеуе**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) возвращает **значение false** , и последующий вызов [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) возвращает код ошибки, заданный подпрограммой обратного вызова во время вызова **сетластеррор**.<br/> |
| <dl> <dt>**ФИЛЕОП \_ доит**</dt> </dl>  | Выполните операцию копирования файлов.<br/>                                                                                                                                                                                                                                                                                                                                  |
| <dl> <dt>**ФИЛЕОП \_ пропустить**</dt> </dl>  | Пропустить текущую операцию копирования.<br/>                                                                                                                                                                                                                                                                                                                                  |



 

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

 

