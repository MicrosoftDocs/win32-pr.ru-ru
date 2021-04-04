---
description: Уведомление СПФИЛЕНОТИФИ \_ куеуескан \_ ex отправляется в подпрограммы обратного вызова с помощью сетупсканфилекуеуе для каждого узла в подочереди копирования очереди файлов.
ms.assetid: 293e63f9-9567-4ea7-b7e5-e5046c8a704b
title: Сообщение SPFILENOTIFY_QUEUESCAN_EX (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0e18cf1cdb1cd007dcf46793d2d018dedd80037
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908808"
---
# <a name="spfilenotify_queuescan_ex-message"></a>\_Сообщение спфиленотифи куеуескан \_ ex

Уведомление **спфиленотифи \_ куеуескан \_ ex** отправляется в подпрограммы обратного вызова с помощью [**сетупсканфилекуеуе**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) для каждого узла в подочереди копирования очереди файлов. Это происходит только в том случае, если функция **сетупсканфилекуеуе** была вызвана указанием флага СПК \_ Scan \_ использовать \_ каллбаккекс.


```C++
SPFILENOTIFY_QUEUESCAN_EX
  Param1 = (PFILEPATHS) Filepaths;
            
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Параметр1* 
</dt> <dd>

Указатель на структуру [**FilePath**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) . **Целевой** элемент — это имя файла целевого файла в системе. **Исходный** элемент — это ожидаемый путь к исходному файлу. Элемент **Win32Error** является ошибкой подписывания.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Подпрограмма обратного вызова должна возвращать [код системной ошибки](/windows/desktop/Debug/system-error-codes).

Если подпрограммы обратного вызова не возвращают \_ ошибок, сканирование очереди продолжится. Если процедура возвращает любой другой код ошибки, сканирование очереди будет прервано, а [**сетупсканфилекуеуе**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) возвращает значение false.

> [!Note]  
> Это уведомление не обрабатывается функцией [**сетупдефаулткуеуекаллбакк**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka) .

 

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

[**сетупсканфилекуеуе**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea)
</dt> </dl>

 

