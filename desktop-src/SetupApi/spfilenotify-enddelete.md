---
description: Уведомление СПФИЛЕНОТИФИ \_ ендделете возвращается в подпрограммы обратного вызова, когда очередь завершает операцию удаления. Это уведомление отправляется, даже если пользователь отменяет или возникает ошибка.
ms.assetid: 78859854-8411-4c51-9c3c-628315cf1c41
title: Сообщение SPFILENOTIFY_ENDDELETE (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4ee4762dc33f8b8ec16a6be273cb42f41aeafce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664528"
---
# <a name="spfilenotify_enddelete-message"></a>\_Сообщение спфиленотифи ендделете

Уведомление **спфиленотифи \_ ендделете** возвращается в подпрограммы обратного вызова, когда очередь завершает операцию удаления. Это уведомление отправляется, даже если пользователь отменяет или возникает ошибка.


```C++
SPFILENOTIFY_ENDDELETE
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Параметр1* 
</dt> <dd>

Указатель на структуру [**FilePath**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) . Элемент **Win32Error** структуры **filePaths** указывает результат операции копирования.

</dd> <dt>

*Param2* 
</dt> <dd>

Не используется.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Код возврата игнорируется.

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

 

 




