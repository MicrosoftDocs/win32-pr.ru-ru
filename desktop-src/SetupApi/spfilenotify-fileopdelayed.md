---
description: Уведомление СПФИЛЕНОТИФИ \_ филеопделайед отправляется сетупинсталлфиликс или сетупкоммитфилекуеуе в подпрограммы обратного вызова, когда файл был отложен, так как файл уже используется. Операция будет обработана при следующей перезагрузке системы.
ms.assetid: a0b38e2b-2390-49e5-b288-77c31636e696
title: Сообщение SPFILENOTIFY_FILEOPDELAYED (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38975506ff998ec09c4549ec95d9ddb620466cf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908811"
---
# <a name="spfilenotify_fileopdelayed-message"></a>\_Сообщение спфиленотифи филеопделайед

Уведомление **спфиленотифи \_ филеопделайед** отправляется [**сетупинсталлфиликс**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfileexa) или [**сетупкоммитфилекуеуе**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) в подпрограммы обратного вызова, когда файл был отложен, так как файл уже используется. Операция будет обработана при следующей перезагрузке системы.


```C++
SPFILENOTIFY_FILEOPDELAYED
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Параметр1* 
</dt> <dd>

Указатель на структуру [**FilePath**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) .

Если отложенная операция является операцией копирования файлов, структура [**filePaths**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) содержит следующие сведения.



| Элемент FILEPATHs | Значение                                |
|------------------|--------------------------------------|
| **Win32Error**   | БЕЗ \_ ошибок                            |
| **Флаги**        | \_копирование филеоп                         |
| **Источник**       | Полный путь к временному файлу.     |
| **Целевой объект**       | Полный путь к фактическому целевому файлу. |



 

Этот временный файл будет скопирован в целевой каталог при перезагрузке системы. Функции установки автоматически создают путь для временного файла.

Если отложенная операция является операцией удаления файла, структура [**filePaths**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) содержит следующие сведения.



| Элемент FILEPATHs | Значение                                |
|------------------|--------------------------------------|
| **Win32Error**   | БЕЗ \_ ошибок                            |
| **Флаги**        | ФИЛЕОП \_ Удаление                       |
| **Источник**       | NULL                                 |
| **Целевой объект**       | Полный путь к удаляемому файлу. |



 

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

[**сетупинсталлфиле**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilea)
</dt> <dt>

[**сетупинсталлфиликс**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfileexa)
</dt> <dt>

[**сетупинсталлфроминфсектион**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona)
</dt> </dl>

 

 




