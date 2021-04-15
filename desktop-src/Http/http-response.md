---
title: HTTP_RESPONSE (HTTP. h)
description: Версия структуры HTTP- \_ ответа зависит от версии очереди запросов, используемой в качестве приведенной в очереди запросов HTTP-сервера версии 1,0. это структура HTTP- \_ запроса \_ v1. API HTTP-сервера версия 2,0 очередь запросов. это структура HTTP- \_ запроса \_ v2.
ms.assetid: F94646C0-7293-4543-842B-F08D8C7E2247
keywords:
- HTTP_RESPONSE
- HTTP_RESPONSE
- PHTTP_RESPONSE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a8445021aa61b94ae83a55937b1db5ca4e3c577
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415273"
---
# <a name="http_response"></a>HTTP- \_ ответ

Версия структуры **\_ ответа HTTP** зависит от версии очереди запросов, используемой следующим образом:

-   API HTTP-сервера версия 1,0 очередь запросов: это структура [**HTTP- \_ запроса \_ v1**](/windows/desktop/api/Http/ns-http-http_request_v1) .
-   API HTTP-сервера версия 2,0 очередь запросов: это структура [**HTTP- \_ запроса \_ v2**](/windows/desktop/api/Http/ns-http-http_request_v2) .

Не используйте [**HTTP- \_ запрос \_ v1**](/windows/desktop/api/Http/ns-http-http_request_v1) и [**HTTP- \_ запрос \_ v2**](/windows/desktop/api/Http/ns-http-http_request_v2) непосредственно в коде; использование **HTTP- \_ ответа** гарантирует правильную версию структуры на основе версии очереди запросов.


```C++
typedef HTTP_REQUEST_V1 HTTP_RESPONSE;
typedef HTTP_REQUEST_V2 HTTP_RESPONSE;
typedef HTTP_RESPONSE* PHTTP_RESPONSE;
```



<dl> <dt>

**HTTP- \_ ответ**
</dt> <dd>

Запрос был получен из очереди запросов v1.

</dd> <dt>

**HTTP- \_ ответ**
</dt> <dd>

Запрос был получен из очереди запросов v2.

</dd> <dt>

**\_ответ ФТТП**
</dt> <dd>

Указатель на структуру **HTTP- \_ ответа** .

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                    |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                              |
| Header<br/>                   | <dl> <dt>HTTP. h</dt> </dl> |



 

 





