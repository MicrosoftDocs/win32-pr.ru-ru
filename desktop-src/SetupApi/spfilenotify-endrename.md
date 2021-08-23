---
description: Уведомление СПФИЛЕНОТИФИ \_ ендренаме отправляется в подпрограммы обратного вызова, когда очередь завершает операцию переименования. Это уведомление отправляется, даже если пользователь отменяет или возникает ошибка.
ms.assetid: 8d5a8d17-de4f-4100-aa72-dfefeb8d4db9
title: Сообщение SPFILENOTIFY_ENDRENAME (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f34ad30cc103e8a13277d3383bad8c2e46409eaabe6f957ace27aebc9759990
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119683124"
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

[**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)
</dt> <dt>

[**сетупкоммитфилекуеуе**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[**сетупдефаулткуеуекаллбакк**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> </dl>

 

 




