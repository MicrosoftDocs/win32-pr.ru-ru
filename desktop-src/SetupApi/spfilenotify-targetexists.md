---
description: Уведомление СПФИЛЕНОТИФИ \_ таржетексистс отправляется в подпрограммы обратного вызова, если копируемый файл был помещен в очередь с \_ \_ флагом обновления нуверврите и этот файл уже существует в целевом каталоге.
ms.assetid: 5c6e0c59-0340-4aa6-94db-8d9a5d202758
title: Сообщение SPFILENOTIFY_TARGETEXISTS (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1d0c1a1ffba520789113b0dc78246657a4fe324
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104423982"
---
# <a name="spfilenotify_targetexists-message"></a>\_Сообщение спфиленотифи таржетексистс

Уведомление **спфиленотифи \_ таржетексистс** отправляется в подпрограммы обратного вызова, если копируемый файл был помещен в очередь с \_ \_ флагом обновления нуверврите и этот файл уже существует в целевом каталоге. Его можно отправить в подпрограммы обратного вызова отдельно или в сочетании с помощью оператора OR с уведомлениями [**спфиленотифи \_ лангмисматч**](spfilenotify-langmismatch.md) и/или [**спфиленотифи \_ таржетневер**](spfilenotify-targetnewer.md) .


```C++
SPFILENOTIFY_TARGETEXISTS
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Параметр1* 
</dt> <dd>

Указатель на структуру [**FilePath**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) , содержащую сведения о путях для исходного и целевого файлов.

</dd> <dt>

*Param2* 
</dt> <dd>

Этот параметр не используется, если это уведомление не объединено с помощью оператора или с уведомлением [**спфиленотифи \_ лангмисматч**](spfilenotify-langmismatch.md) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Подпрограммы обратного вызова должны возвращать одно из следующих значений.



| Код возврата                                                                          | Описание                                            |
|--------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <dt>**УСЛОВИЯ**</dt> </dl>  | Перезапишите файл в целевом каталоге.<br/> |
| <dl> <dt>**ISFALSE**</dt> </dl> | Пропустить текущую операцию копирования.<br/>            |



 

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
</dt> <dt>

[**сетупинсталлфиле**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilea)
</dt> <dt>

[**сетупинсталлфиликс**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfileexa)
</dt> <dt>

[**сетупинсталлфроминфсектион**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona)
</dt> </dl>

 

 




