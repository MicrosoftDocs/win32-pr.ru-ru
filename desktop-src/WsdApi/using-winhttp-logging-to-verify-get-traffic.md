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
# <a name="using-winhttp-logging-to-verify-get-traffic"></a><span data-ttu-id="389d1-104">Использование ведения журнала WinHTTP для проверки получения трафика</span><span class="sxs-lookup"><span data-stu-id="389d1-104">Using WinHTTP Logging to Verify Get Traffic</span></span>

<span data-ttu-id="389d1-105">Если универсальный узел и клиент выполняются успешно, но фактический узел и клиент по-прежнему завершаются сбоем, возможно, запрос метаданных не инициируется.</span><span class="sxs-lookup"><span data-stu-id="389d1-105">If the generic host and client succeed but the actual host and client still fail, it is possible that the metadata request is not being initiated.</span></span> <span data-ttu-id="389d1-106">Ведение журнала [WinHTTP](/windows/desktop/WinHttp/winhttp-start-page) можно использовать для проверки того, что исходящие сообщения создаются и отправляются правильно.</span><span class="sxs-lookup"><span data-stu-id="389d1-106">[WinHTTP](/windows/desktop/WinHttp/winhttp-start-page) logging can be used to verify that outbound messages are being generated and sent correctly.</span></span>

<span data-ttu-id="389d1-107">Клиентские приложения на основе WSDAPI используют [WinHTTP](/windows/desktop/WinHttp/winhttp-start-page) для подключения к устройствам.</span><span class="sxs-lookup"><span data-stu-id="389d1-107">WSDAPI-based client applications use [WinHTTP](/windows/desktop/WinHttp/winhttp-start-page) to connect to devices.</span></span> <span data-ttu-id="389d1-108">На узлах устройств на базе WSDAPI не используется WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="389d1-108">WSDAPI-based device hosts do not use WinHTTP.</span></span> <span data-ttu-id="389d1-109">Кроме того, некоторые сторонние прокси не используют WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="389d1-109">Also, some third-party proxies do not use WinHTTP.</span></span> <span data-ttu-id="389d1-110">При устранении неполадок с узлом или прокси-сервером, который не использует WinHTTP, пропустите эту диагностическую процедуру и продолжите устранение неполадок, выполнив процедуры, описанные в разделе [Проверка трассировки сети для обмена метаданными HTTP](inspecting-network-traces-for-http-metadata-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="389d1-110">When troubleshooting a host or proxy that does not use WinHTTP, skip this diagnostic procedure and continue troubleshooting by following the procedures in [Inspecting Network Traces for HTTP Metadata Exchange](inspecting-network-traces-for-http-metadata-exchange.md).</span></span>

<span data-ttu-id="389d1-111">В журнале [WinHTTP](/windows/desktop/WinHttp/winhttp-start-page) не отображается весь трафик на уровне TCP.</span><span class="sxs-lookup"><span data-stu-id="389d1-111">[WinHTTP](/windows/desktop/WinHttp/winhttp-start-page) logging does not show all TCP-level traffic.</span></span> <span data-ttu-id="389d1-112">Перейдите к [анализу сетевых трассировок для обмена метаданными HTTP](inspecting-network-traces-for-http-metadata-exchange.md) , если трафик, помимо трафика HTTP, интересен.</span><span class="sxs-lookup"><span data-stu-id="389d1-112">Skip to [Inspecting Network Traces for HTTP Metadata Exchange](inspecting-network-traces-for-http-metadata-exchange.md) if traffic besides the HTTP traffic is of interest.</span></span>

<span data-ttu-id="389d1-113">**Использование ведения журнала WinHTTP для проверки получения трафика**</span><span class="sxs-lookup"><span data-stu-id="389d1-113">**To use WinHTTP logging to verify Get traffic**</span></span>

1.  [<span data-ttu-id="389d1-114">Запишите журналы WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="389d1-114">Capture the WinHTTP logs.</span></span>](capturing-winhttp-logs.md)
2.  <span data-ttu-id="389d1-115">Запустите Блокнот или другой текстовый редактор.</span><span class="sxs-lookup"><span data-stu-id="389d1-115">Start Notepad or another text editor.</span></span> <span data-ttu-id="389d1-116">Текстовый редактор должен запускаться от имени администратора.</span><span class="sxs-lookup"><span data-stu-id="389d1-116">The text editor must be run as Administrator.</span></span>
3.  <span data-ttu-id="389d1-117">Откройте файл журнала WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="389d1-117">Open the WinHTTP log file.</span></span>
4.  <span data-ttu-id="389d1-118">Убедитесь, что были отправлены необходимые HTTP-запросы и сообщения метаданных.</span><span class="sxs-lookup"><span data-stu-id="389d1-118">Verify that the required HTTP requests and metadata messages were sent.</span></span>

<span data-ttu-id="389d1-119">Если сообщение [Get](get--metadata-exchange--http-request-and-message.md) для узла найдено в журналах WinHTTP, запросы метаданных отправляются на WinHTTP успешно.</span><span class="sxs-lookup"><span data-stu-id="389d1-119">If a [Get](get--metadata-exchange--http-request-and-message.md) message for the host is found in the WinHTTP logs, then the metadata requests are being sent to WinHTTP successfully.</span></span> <span data-ttu-id="389d1-120">Продолжайте устранение неполадок, выполнив процедуры, описанные в статье [Проверка трассировки сети для обмена метаданными HTTP](inspecting-network-traces-for-http-metadata-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="389d1-120">Continue troubleshooting by following the procedures in [Inspecting Network Traces for HTTP Metadata Exchange](inspecting-network-traces-for-http-metadata-exchange.md).</span></span>

<span data-ttu-id="389d1-121">Если не удается найти сообщение [Get](get--metadata-exchange--http-request-and-message.md) для узла в журналах WinHTTP, запрос метаданных не инициируется.</span><span class="sxs-lookup"><span data-stu-id="389d1-121">If a [Get](get--metadata-exchange--http-request-and-message.md) message cannot be found for the host in the WinHTTP logs, then the metadata request is not being initiated.</span></span> <span data-ttu-id="389d1-122">Это может произойти, когда узел публикует недопустимый Ксаддрс.</span><span class="sxs-lookup"><span data-stu-id="389d1-122">This can happen when the host publishes invalid XAddrs.</span></span> <span data-ttu-id="389d1-123">Убедитесь, что Ксаддрс на узле соответствуют [правилам проверки ксаддр](xaddr-validation-rules.md).</span><span class="sxs-lookup"><span data-stu-id="389d1-123">Verify that the XAddrs on the host conform to the [XAddr validation rules](xaddr-validation-rules.md).</span></span>

## <a name="verifying-that-the-required-http-requests-and-metadata-messages-were-sent"></a><span data-ttu-id="389d1-124">Проверка отправки необходимых HTTP-запросов и сообщений метаданных</span><span class="sxs-lookup"><span data-stu-id="389d1-124">Verifying that the required HTTP requests and metadata messages were sent</span></span>

<span data-ttu-id="389d1-125">Для успешного обмена метаданными должны выполняться следующие события.</span><span class="sxs-lookup"><span data-stu-id="389d1-125">The following events must occur for successful metadata exchange:</span></span>

-   <span data-ttu-id="389d1-126">Клиент WSDAPI создает исходящий HTTP-запрос.</span><span class="sxs-lookup"><span data-stu-id="389d1-126">The WSDAPI client generates an outbound HTTP request.</span></span> <span data-ttu-id="389d1-127">Этот запрос отправляется на узел WSDAPI.</span><span class="sxs-lookup"><span data-stu-id="389d1-127">This request is sent to the WSDAPI host.</span></span>
-   <span data-ttu-id="389d1-128">Клиент отправляет сообщение [Get](get--metadata-exchange--http-request-and-message.md) на узел.</span><span class="sxs-lookup"><span data-stu-id="389d1-128">The client sends a [Get](get--metadata-exchange--http-request-and-message.md) message to the host.</span></span>

<span data-ttu-id="389d1-129">Эти события фиксируются в журналах WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="389d1-129">These events are captured in the WinHTTP logs.</span></span>

<span data-ttu-id="389d1-130">В следующем фрагменте файла журнала WinHTTP показан исходящий HTTP-запрос, созданный клиентом WSDAPI.</span><span class="sxs-lookup"><span data-stu-id="389d1-130">The following WinHTTP log file snippet shows an outbound HTTP request generated by a WSDAPI client.</span></span>

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

<span data-ttu-id="389d1-131">В следующем фрагменте файла журнала WinHTTP показано сообщение [Get](get--metadata-exchange--http-request-and-message.md) .</span><span class="sxs-lookup"><span data-stu-id="389d1-131">The following WinHTTP log file snippet shows a [Get](get--metadata-exchange--http-request-and-message.md) message.</span></span> <span data-ttu-id="389d1-132">Это сообщение должно следовать сразу за HTTP-запросом.</span><span class="sxs-lookup"><span data-stu-id="389d1-132">This message should immediately follow the HTTP request.</span></span>

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

<span data-ttu-id="389d1-133">Элемент **Action** ( `<wsa:Action>https://schemas.xmlsoap.org/ws/2004/09/transfer/Get</wsa:Action>` ) определяет сообщение как сообщение [Get](get--metadata-exchange--http-request-and-message.md) .</span><span class="sxs-lookup"><span data-stu-id="389d1-133">The **Action** element (`<wsa:Action>https://schemas.xmlsoap.org/ws/2004/09/transfer/Get</wsa:Action>`) identifies the message as a [Get](get--metadata-exchange--http-request-and-message.md) message.</span></span> <span data-ttu-id="389d1-134">Убедитесь, что значение элемента **to** (например, `<wsa:To>urn:uuid:dbe17c74-3b21-4f52-addc-b84b444f73a0</wsa:To>` ) соответствует идентификатору устройства, объявленному УЗЛОМ в исходном UDP-WS-Discovery сообщениях.</span><span class="sxs-lookup"><span data-stu-id="389d1-134">Verify that the value of the **To** element (for example, `<wsa:To>urn:uuid:dbe17c74-3b21-4f52-addc-b84b444f73a0</wsa:To>`) matches the device ID advertised by the host in the original UDP WS-Discovery messages.</span></span> <span data-ttu-id="389d1-135">ИДЕНТИФИКАТОР устройства, объявленный узлом, можно проверить с помощью узла отладки WSD.</span><span class="sxs-lookup"><span data-stu-id="389d1-135">The device ID advertised by the host can be checked by using the WSD Debug Host.</span></span> <span data-ttu-id="389d1-136">Дополнительные сведения см. в разделе [Использование универсального узла и клиента для протокола UDP WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md).</span><span class="sxs-lookup"><span data-stu-id="389d1-136">For more information, see [Using a Generic Host and Client for UDP WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md).</span></span>

<span data-ttu-id="389d1-137">Кроме того, ответ узла на запрос метаданных можно найти в журналах WinHTTP клиента.</span><span class="sxs-lookup"><span data-stu-id="389d1-137">In addition, the host's response to the metadata request can be found in the client's WinHTTP logs.</span></span> <span data-ttu-id="389d1-138">Узел создает сообщение [GetResponse](getresponse--metadata-exchange--message.md) в ответ на сообщение [Get](get--metadata-exchange--http-request-and-message.md) клиента.</span><span class="sxs-lookup"><span data-stu-id="389d1-138">The host generates a [GetResponse](getresponse--metadata-exchange--message.md) message in response to the client's [Get](get--metadata-exchange--http-request-and-message.md) message.</span></span>

<span data-ttu-id="389d1-139">В следующем фрагменте файла журнала WinHTTP показано входящее сообщение [GetResponse](getresponse--metadata-exchange--message.md) , полученное клиентом WSDAPI.</span><span class="sxs-lookup"><span data-stu-id="389d1-139">The following WinHTTP log file snippet shows an inbound [GetResponse](getresponse--metadata-exchange--message.md) message received by a WSDAPI client.</span></span>

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

<span data-ttu-id="389d1-140">Элемент **Action** ( `<wsa:Action>https://schemas.xmlsoap.org/ws/2004/09/transfer/GetResponse</wsa:Action>` ) определяет сообщение как сообщение с [ответом](getresponse--metadata-exchange--message.md) .</span><span class="sxs-lookup"><span data-stu-id="389d1-140">The **Action** element (`<wsa:Action>https://schemas.xmlsoap.org/ws/2004/09/transfer/GetResponse</wsa:Action>`) identifies the message as a [GetResponse](getresponse--metadata-exchange--message.md) message.</span></span> <span data-ttu-id="389d1-141">Убедитесь, что **значение элемента текст** сообщения о неответе совпадает со значением элемента **MessageId** сообщения [Get](get--metadata-exchange--http-request-and-message.md) .</span><span class="sxs-lookup"><span data-stu-id="389d1-141">Verify that the value of the **RelatesTo** element of the GetResponse message matches the value of the **MessageID** element of the [Get](get--metadata-exchange--http-request-and-message.md) message.</span></span> <span data-ttu-id="389d1-142">В этом примере значение элемента «Автотекст **» (** `<wsa:RelatesTo>urn:uuid:8506ac50-3646-4621-9680-86f484d87909</wsa:RelatesTo>` ) совпадает со значением элемента **MessageId** сообщения Get ( `<wsa:MessageID>urn:uuid:8506ac50-3646-4621-9680-86f484d87909</wsa:MessageID>` ).</span><span class="sxs-lookup"><span data-stu-id="389d1-142">In this example, the value of the **RelatesTo** element (`<wsa:RelatesTo>urn:uuid:8506ac50-3646-4621-9680-86f484d87909</wsa:RelatesTo>`) matches the value of the **MessageID** element of the Get message (`<wsa:MessageID>urn:uuid:8506ac50-3646-4621-9680-86f484d87909</wsa:MessageID>`).</span></span>

## <a name="related-topics"></a><span data-ttu-id="389d1-143">См. также</span><span class="sxs-lookup"><span data-stu-id="389d1-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="389d1-144">Известен</span><span class="sxs-lookup"><span data-stu-id="389d1-144">WinHTTP</span></span>](/windows/desktop/WinHttp/winhttp-start-page)
</dt> <dt>

[<span data-ttu-id="389d1-145">Запись журналов WinHTTP</span><span class="sxs-lookup"><span data-stu-id="389d1-145">Capturing WinHTTP Logs</span></span>](capturing-winhttp-logs.md)
</dt> <dt>

[<span data-ttu-id="389d1-146">Процедуры диагностики WSDAPI</span><span class="sxs-lookup"><span data-stu-id="389d1-146">WSDAPI Diagnostic Procedures</span></span>](wsdapi-diagnostic-procedures.md)
</dt> <dt>

[<span data-ttu-id="389d1-147">начало работы с разрешениями WSDAPI</span><span class="sxs-lookup"><span data-stu-id="389d1-147">Getting Started with WSDAPI Troubleshooting</span></span>](getting-started-with-wsdapi-troubleshooting.md)
</dt> </dl>

 

 
