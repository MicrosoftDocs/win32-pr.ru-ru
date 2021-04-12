---
description: Если универсальный узел и клиент выполняются успешно, но фактический узел и клиент по-прежнему завершаются сбоем, возможно, запрос метаданных не инициируется. Ведение журнала WinHTTP можно использовать для проверки того, что исходящие сообщения создаются и отправляются правильно.
ms.assetid: ab4568bd-fc05-4e2a-ac8c-f035e6583a36
title: Использование ведения журнала WinHTTP для проверки получения трафика
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 448e4a127baf90a64291cbd14477c424270b332d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104264639"
---
# <a name="using-winhttp-logging-to-verify-get-traffic"></a>Использование ведения журнала WinHTTP для проверки получения трафика

Если универсальный узел и клиент выполняются успешно, но фактический узел и клиент по-прежнему завершаются сбоем, возможно, запрос метаданных не инициируется. Ведение журнала [WinHTTP](/windows/desktop/WinHttp/winhttp-start-page) можно использовать для проверки того, что исходящие сообщения создаются и отправляются правильно.

Клиентские приложения на основе WSDAPI используют [WinHTTP](/windows/desktop/WinHttp/winhttp-start-page) для подключения к устройствам. На узлах устройств на базе WSDAPI не используется WinHTTP. Кроме того, некоторые сторонние прокси не используют WinHTTP. При устранении неполадок с узлом или прокси-сервером, который не использует WinHTTP, пропустите эту диагностическую процедуру и продолжите устранение неполадок, выполнив процедуры, описанные в разделе [Проверка трассировки сети для обмена метаданными HTTP](inspecting-network-traces-for-http-metadata-exchange.md).

В журнале [WinHTTP](/windows/desktop/WinHttp/winhttp-start-page) не отображается весь трафик на уровне TCP. Перейдите к [анализу сетевых трассировок для обмена метаданными HTTP](inspecting-network-traces-for-http-metadata-exchange.md) , если трафик, помимо трафика HTTP, интересен.

**Использование ведения журнала WinHTTP для проверки получения трафика**

1.  [Запишите журналы WinHTTP.](capturing-winhttp-logs.md)
2.  Запустите Блокнот или другой текстовый редактор. Текстовый редактор должен запускаться от имени администратора.
3.  Откройте файл журнала WinHTTP.
4.  Убедитесь, что были отправлены необходимые HTTP-запросы и сообщения метаданных.

Если сообщение [Get](get--metadata-exchange--http-request-and-message.md) для узла найдено в журналах WinHTTP, запросы метаданных отправляются на WinHTTP успешно. Продолжайте устранение неполадок, выполнив процедуры, описанные в статье [Проверка трассировки сети для обмена метаданными HTTP](inspecting-network-traces-for-http-metadata-exchange.md).

Если не удается найти сообщение [Get](get--metadata-exchange--http-request-and-message.md) для узла в журналах WinHTTP, запрос метаданных не инициируется. Это может произойти, когда узел публикует недопустимый Ксаддрс. Убедитесь, что Ксаддрс на узле соответствуют [правилам проверки ксаддр](xaddr-validation-rules.md).

## <a name="verifying-that-the-required-http-requests-and-metadata-messages-were-sent"></a>Проверка отправки необходимых HTTP-запросов и сообщений метаданных

Для успешного обмена метаданными должны выполняться следующие события.

-   Клиент WSDAPI создает исходящий HTTP-запрос. Этот запрос отправляется на узел WSDAPI.
-   Клиент отправляет сообщение [Get](get--metadata-exchange--http-request-and-message.md) на узел.

Эти события фиксируются в журналах WinHTTP.

В следующем фрагменте файла журнала WinHTTP показан исходящий HTTP-запрос, созданный клиентом WSDAPI.

``` syntax
16:51:47.893 ::*0000004* :: WinHttpSendRequest(0x36aae0, "", 0, 0x0, 0, 658, 0)
16:51:47.893 ::*0000004* :: WinHttpSendRequest() returning TRUE
16:51:47.897 ::*0000004* :: sending data:
16:51:47.897 ::*0000004* :: 226 (0xe2) bytes
16:51:47.897 ::*0000004* :: <<<<-------- HTTP stream follows below ----------------------------------------------->>>>
16:51:47.897 ::*0000004* :: POST /dbe17c74-3b21-4f52-addc-b84b444f73a0 HTTP/1.1
16:51:47.897 ::*0000004* :: Content-Type: application/soap+xml
16:51:47.897 ::*0000004* :: User-Agent: WSDAPI
16:51:47.897 ::*0000004* :: Host: 192.168.0.1:5357
16:51:47.897 ::*0000004* :: Content-Length: 658
16:51:47.897 ::*0000004* :: Connection: Keep-Alive
16:51:47.897 ::*0000004* :: Cache-Control: no-cache
16:51:47.897 ::*0000004* :: Pragma: no-cache
16:51:47.897 ::*0000004* :: 
16:51:47.897 ::*0000004* :: 
16:51:47.897 ::*0000004* :: <<<<-------- End ----------------------------------------------->>>>
```

В следующем фрагменте файла журнала WinHTTP показано сообщение [Get](get--metadata-exchange--http-request-and-message.md) . Это сообщение должно следовать сразу за HTTP-запросом.

``` syntax
16:51:47.898 ::*0000004* :: WinHttpWriteData(0x36aae0, 0x11aa7c4, 658, 0x0)
16:51:47.899 ::*0000004* :: sending data:
16:51:47.899 ::*0000004* :: 658 (0x292) bytes
16:51:47.899 ::*0000004* :: <<<<-------- HTTP stream follows below ----------------------------------------------->>>>
16:51:47.899 ::*0000004* :: <?xml version="1.0" encoding="utf-8" ?>
16:51:47.899 ::*0000004* :: <soap:Envelope xmlns:soap="https://www.w3.org/2003/05/soap-envelope" xmlns:wsa="https://schemas.xmlsoap.org/ws/2004/08/addressing"><soap:Header><wsa:To>urn:uuid:dbe17c74-3b21-4f52-addc-b84b444f73a0</wsa:To><wsa:Action>https://schemas.xmlsoap.org/ws/2004/09/transfer/Get</wsa:Action><wsa:MessageID>urn:uuid:8506ac50-3646-4621-9680-86f484d87909</wsa:MessageID><wsa:ReplyTo><wsa:Address>https://schemas.xmlsoap.org/ws/2004/08/addressing/role/anonymous</wsa:Address></wsa:ReplyTo><wsa:From><wsa:Address>urn:uuid:b32467b5-e7ee-4ae3-8a8e-f5aa417c23b6</wsa:Address></wsa:From></soap:Header><soap:Body></soap:Body></soap:Envelope>
16:51:47.899 ::*0000004* :: <<<<-------- End ----------------------------------------------->>>>
16:51:47.899 ::*0000004* :: WinHttpWriteData() returning TRUE
```

Элемент **Action** ( `<wsa:Action>https://schemas.xmlsoap.org/ws/2004/09/transfer/Get</wsa:Action>` ) определяет сообщение как сообщение [Get](get--metadata-exchange--http-request-and-message.md) . Убедитесь, что значение элемента **to** (например, `<wsa:To>urn:uuid:dbe17c74-3b21-4f52-addc-b84b444f73a0</wsa:To>` ) соответствует идентификатору устройства, объявленному УЗЛОМ в исходном UDP-WS-Discovery сообщениях. ИДЕНТИФИКАТОР устройства, объявленный узлом, можно проверить с помощью узла отладки WSD. Дополнительные сведения см. в разделе [Использование универсального узла и клиента для протокола UDP WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md).

Кроме того, ответ узла на запрос метаданных можно найти в журналах WinHTTP клиента. Узел создает сообщение [GetResponse](getresponse--metadata-exchange--message.md) в ответ на сообщение [Get](get--metadata-exchange--http-request-and-message.md) клиента.

В следующем фрагменте файла журнала WinHTTP показано входящее сообщение [GetResponse](getresponse--metadata-exchange--message.md) , полученное клиентом WSDAPI.

``` syntax
16:51:47.899 ::*0000004* :: WinHttpReceiveResponse(0x36aae0, 0x0)
16:51:47.899 ::*0000004* :: WinHttpReceiveResponse() returning TRUE
16:51:47.899 ::*Session* :: DllMain(0x73fc0000, DLL_THREAD_ATTACH, 0x0)
16:51:47.902 ::*0000004* :: received data:
16:51:47.902 ::*0000004* :: 1024 (0x400) bytes
16:51:47.902 ::*0000004* :: <<<<-------- HTTP stream follows below ----------------------------------------------->>>>
16:51:47.902 ::*0000004* :: HTTP/1.1 200 
16:51:47.902 ::*0000004* :: Content-Type: application/soap+xml
16:51:47.902 ::*0000004* :: Server: Microsoft-HTTPAPI/2.0
16:51:47.902 ::*0000004* :: Date: Fri, 15 Jun 2007 23:51:47 GMT
16:51:47.905 ::*0000004* :: Content-Length: 2228
16:51:47.905 ::*0000004* :: 
16:51:47.905 ::*0000004* :: <?xml version="1.0" encoding="utf-8" ?>
16:51:47.905 ::*0000004* :: <soap:Envelope xmlns:soap="https://www.w3.org/2003/05/soap-envelope" xmlns:wsa="https://schemas.xmlsoap.org/ws/2004/08/addressing" xmlns:wsx="https://schemas.xmlsoap.org/ws/2004/09/mex" xmlns:wsdp="https://schemas.xmlsoap.org/ws/2006/02/devprof" xmlns:un0="http://schemas.microsoft.com/windows/pnpx/2005/10" xmlns:pub="http://schemas.microsoft.com/windows/pub/2005/07"><soap:Header><wsa:To>https://schemas.xmlsoap.org/ws/2004/08/addressing/role/anonymous</wsa:To><wsa:Action>https://schemas.xmlsoap.org/ws/2004/09/transfer/GetResponse</wsa:Action><wsa:MessageID>urn:uuid:2884cbcc-2848-4c35-9327-5ab5451a8729</wsa:MessageID><wsa:RelatesTo>urn:uuid:8506ac50-3646-4621-9680-86f484d87909</wsa:RelatesTo></soap:Header><soap:Body><wsx:Metadata><wsx:MetadataSection Dialect="https://schemas.xmlsoap.org/ws/2006/02/devprof/ThisDevice"><wsdp:ThisDevice><wsd
16:51:47.905 ::*0000004* :: <<<<-------- End ----------------------------------------------->>>>
```

Элемент **Action** ( `<wsa:Action>https://schemas.xmlsoap.org/ws/2004/09/transfer/GetResponse</wsa:Action>` ) определяет сообщение как сообщение с [ответом](getresponse--metadata-exchange--message.md) . Убедитесь, что **значение элемента текст** сообщения о неответе совпадает со значением элемента **MessageId** сообщения [Get](get--metadata-exchange--http-request-and-message.md) . В этом примере значение элемента «Автотекст **» (** `<wsa:RelatesTo>urn:uuid:8506ac50-3646-4621-9680-86f484d87909</wsa:RelatesTo>` ) совпадает со значением элемента **MessageId** сообщения Get ( `<wsa:MessageID>urn:uuid:8506ac50-3646-4621-9680-86f484d87909</wsa:MessageID>` ).

## <a name="related-topics"></a>См. также

<dl> <dt>

[Известен](/windows/desktop/WinHttp/winhttp-start-page)
</dt> <dt>

[Запись журналов WinHTTP](capturing-winhttp-logs.md)
</dt> <dt>

[Процедуры диагностики WSDAPI](wsdapi-diagnostic-procedures.md)
</dt> <dt>

[начало работы с разрешениями WSDAPI](getting-started-with-wsdapi-troubleshooting.md)
</dt> </dl>

 

 
