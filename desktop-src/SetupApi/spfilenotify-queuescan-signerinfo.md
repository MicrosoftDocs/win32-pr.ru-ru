---
description: '\_ \_ Уведомление SIGNERINFO спфиленотифи куеуескан отправляется в подпрограммы обратного вызова сетупсканфилекуеуе для каждого узла в подочереди копирования очереди файлов.'
ms.assetid: 5b22e8ba-9a18-461b-bad7-b2d76f83d7f3
title: Сообщение SPFILENOTIFY_QUEUESCAN_SIGNERINFO (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e29bf9e9c7e0ab76303d8c2fb21a0109ec60358f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103998872"
---
# <a name="spfilenotify_queuescan_signerinfo-message"></a>СПФИЛЕНОТИФИ \_ куеуескан \_ SIGNERINFO сообщение

Уведомление **\_ \_ SIGNERINFO спфиленотифи куеуескан** отправляется в подпрограммы обратного вызова [**сетупсканфилекуеуе**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) для каждого узла в подочереди копирования очереди файлов. Это происходит только в том случае, если функция **сетупсканфилекуеуе** была вызвана указанием флага СПК \_ Scan \_ использовать \_ обратный вызов \_ SIGNERINFO. Доступно начиная с Windows XP.


```C++
SPFILENOTIFY_QUEUESCAN_SIGNERINFO
  Param1 = (PFILEPATHS_SIGNERINFO) Filepaths;
            
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Параметр1* 
</dt> <dd>

Указатель на структуру [**\_ SIGNERINFO filePaths**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_signerinfo_a) . **Целевой** элемент — это имя файла целевого файла в системе. **Исходный** элемент — это ожидаемый путь к исходному файлу. Элемент **Win32Error** является ошибкой подписывания. Сведения о сигнатуре возвращаются, если подпрограммы обратного вызова возвращают **Win32Error**= = No \_ Error. Член **дигиталсигнер** — это цифровой подписывающий. Версия является членом **версии** . **Каталогфиле** — это файл каталога.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Подпрограмма обратного вызова должна возвращать [код системной ошибки](/windows/desktop/Debug/system-error-codes).

Если подпрограмма обратного вызова не возвращает \_ ошибку, сканирование очереди продолжится и возвращает значение, если процедура возвращает любой другой код ошибки, сканирование очереди прерывается, а [**Сетупсканфилекуеуе**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) возвращает **false**.

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

 

