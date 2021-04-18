---
description: Уведомление СПФИЛЕНОТИФИ \_ ендренаме отправляется в подпрограммы обратного вызова, когда очередь завершает операцию переименования. Это уведомление отправляется, даже если пользователь отменяет или возникает ошибка.
ms.assetid: 8d5a8d17-de4f-4100-aa72-dfefeb8d4db9
title: Сообщение SPFILENOTIFY_ENDRENAME (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a316d4dfe72ee9eb7d85fdb70eb90e1cf3d3f463
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664525"
---
# <a name="spfilenotify_endrename-message"></a>\_Сообщение спфиленотифи ендренаме

Уведомление **спфиленотифи \_ ендренаме** отправляется в подпрограммы обратного вызова, когда очередь завершает операцию переименования. Это уведомление отправляется, даже если пользователь отменяет или возникает ошибка.


```C++
SPFILENOTIFY_ENDRENAME
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

[**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)
</dt> <dt>

[**сетупкоммитфилекуеуе**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[**сетупдефаулткуеуекаллбакк**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> </dl>

 

 




