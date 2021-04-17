---
description: Уведомление СПФИЛЕНОТИФИ \_ таржетневер отправляется в подсистему обратного вызова, если копируемый файл был поставлен в очередь с \_ \_ указанными флагами SP Copy новее или SP \_ Copy \_ Force более поздней \_ версии, а более новая версия файла уже существует в целевом каталоге.
ms.assetid: 93bcd610-f75d-4900-841c-f67946af5c4a
title: Сообщение SPFILENOTIFY_TARGETNEWER (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c432515a5ce0e9a1eddb8ea6e92f7376c318b4f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663563"
---
# <a name="spfilenotify_targetnewer-message"></a>\_Сообщение спфиленотифи таржетневер

Уведомление **спфиленотифи \_ таржетневер** отправляется в подсистему обратного вызова, если копируемый файл был поставлен в очередь с \_ \_ указанными флагами SP Copy новее или SP \_ Copy \_ Force более поздней \_ версии, а более новая версия файла уже существует в целевом каталоге. Его можно отправить в подпрограммы обратного вызова отдельно или ORed вместе с [**спфиленотифи \_ лангмисматч**](spfilenotify-langmismatch.md) и/или [**спфиленотифи \_ таржетексистс**](spfilenotify-targetexists.md).


```C++
SPFILENOTIFY_TARGETNEWER
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Параметр1* 
</dt> <dd>

Указатель на структуру [**FilePath**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) , содержащую сведения о путях для исходных и целевых файлов.

</dd> <dt>

*Param2* 
</dt> <dd>

Этот параметр не используется, если это уведомление не объединено с помощью оператора или с [**спфиленотифи \_ лангмисматч**](spfilenotify-langmismatch.md).

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

 

 




