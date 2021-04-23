---
description: Любой анализатор сетевых пакетов, который может отображать необработанные пакеты, может использоваться для проверки запросов на обмен метаданными HTTP. Рекомендуется Microsoft Network Monitor 3 (Netmon). Дополнительные сведения о netmon см. в статье Загрузка Netmon и примеры DPWS Filters.
ms.assetid: b3b6c4d1-5fa3-41fb-ae1d-067638e385b0
title: Проверка трассировки сети для обмена метаданными HTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c9993c542789b7f11eb35344dd6b0b03bfbafc3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263908"
---
# <a name="inspecting-network-traces-for-http-metadata-exchange"></a><span data-ttu-id="8243c-105">Проверка трассировки сети для обмена метаданными HTTP</span><span class="sxs-lookup"><span data-stu-id="8243c-105">Inspecting Network Traces for HTTP Metadata Exchange</span></span>

<span data-ttu-id="8243c-106">Любой анализатор сетевых пакетов, который может отображать необработанные пакеты, может использоваться для проверки запросов на обмен метаданными HTTP.</span><span class="sxs-lookup"><span data-stu-id="8243c-106">Any network packet analyzer that can display raw packets can be used to inspect HTTP metadata exchange requests.</span></span> <span data-ttu-id="8243c-107">Рекомендуется Microsoft Network Monitor 3 (Netmon).</span><span class="sxs-lookup"><span data-stu-id="8243c-107">Microsoft Network Monitor 3 (Netmon) is recommended.</span></span> <span data-ttu-id="8243c-108">Дополнительные сведения о netmon см. в статье [Загрузка Netmon и примеры DPWS Filters](downloading-netmon-and-sample-dpws-filters.md).</span><span class="sxs-lookup"><span data-stu-id="8243c-108">For more information about Netmon, see [Downloading Netmon and Sample DPWS Filters](downloading-netmon-and-sample-dpws-filters.md).</span></span>

<span data-ttu-id="8243c-109">Эта диагностическая процедура может не быть полезной для клиентов и узлов, использующих безопасный канал для обмена данными, так как содержимое сообщения зашифровано.</span><span class="sxs-lookup"><span data-stu-id="8243c-109">This diagnostic procedure may not be as useful for clients and hosts using a secure channel for communications because the message contents are encrypted.</span></span>

<span data-ttu-id="8243c-110">**Проверка трассировки сети для обмена метаданными HTTP**</span><span class="sxs-lookup"><span data-stu-id="8243c-110">**To inspect network traces for HTTP metadata exchange**</span></span>

1.  <span data-ttu-id="8243c-111">Настройте узел и клиент для работы по сети (то есть убедитесь, что узел и клиент будут работать на разных компьютерах).</span><span class="sxs-lookup"><span data-stu-id="8243c-111">Configure the host and client to run across the network (that is, make sure that the host and client will operate on different machines).</span></span>
2.  <span data-ttu-id="8243c-112">Установите анализатор пакетов (Netmon) на клиенте или на узле.</span><span class="sxs-lookup"><span data-stu-id="8243c-112">Install the packet analyzer (Netmon) on either the client or the host.</span></span>
3.  <span data-ttu-id="8243c-113">Настройте анализатор пакетов для записи трафика на сетевом адаптере, соединяющем узел и клиент.</span><span class="sxs-lookup"><span data-stu-id="8243c-113">Configure the packet analyzer to capture traffic on the network adapter connecting the host and the client.</span></span>
4.  <span data-ttu-id="8243c-114">Воспроизведите ошибку, запустив узел и клиент или нажав клавишу F5 в обозревателе сети.</span><span class="sxs-lookup"><span data-stu-id="8243c-114">Reproduce the failure by starting the host and client or by pressing F5 in the Network Explorer.</span></span>
5.  <span data-ttu-id="8243c-115">Отфильтруйте результаты, чтобы изолировать WS-Discovery и трафик обмена метаданными.</span><span class="sxs-lookup"><span data-stu-id="8243c-115">Filter the results to isolate WS-Discovery and metadata exchange traffic.</span></span> <span data-ttu-id="8243c-116">Чтобы просмотреть примеры фильтров Netmon, см. [статью Загрузка Netmon и примеры DPWS Filters](downloading-netmon-and-sample-dpws-filters.md).</span><span class="sxs-lookup"><span data-stu-id="8243c-116">To view sample Netmon filters, see [Downloading Netmon and Sample DPWS Filters](downloading-netmon-and-sample-dpws-filters.md).</span></span>
    > [!Note]  
    > <span data-ttu-id="8243c-117">Это необязательный шаг.</span><span class="sxs-lookup"><span data-stu-id="8243c-117">This step is optional.</span></span>

     

6.  <span data-ttu-id="8243c-118">Убедитесь, что сообщения, передаваемые между клиентом и узлом, соответствуют основным требованиям к трафику.</span><span class="sxs-lookup"><span data-stu-id="8243c-118">Verify that messages sent between client and host meet basic traffic requirements.</span></span>

## <a name="verifying-that-messages-meet-traffic-requirements"></a><span data-ttu-id="8243c-119">Проверка соответствия сообщений требованиям к трафику</span><span class="sxs-lookup"><span data-stu-id="8243c-119">Verifying that messages meet traffic requirements</span></span>

<span data-ttu-id="8243c-120">WSDAPI клиенты и узлы должны отправить сообщения, соответствующие следующим критериям.</span><span class="sxs-lookup"><span data-stu-id="8243c-120">WSDAPI clients and hosts must send messages that conform to the following criteria.</span></span> <span data-ttu-id="8243c-121">Общие сведения о шаблонах сообщений см. в статье [шаблоны сообщений обнаружения и обмена метаданными](discovery-and-metadata-exchange-message-patterns.md).</span><span class="sxs-lookup"><span data-stu-id="8243c-121">For general information about message patterns, see [Discovery and Metadata Exchange Message Patterns](discovery-and-metadata-exchange-message-patterns.md).</span></span>

-   <span data-ttu-id="8243c-122">Сообщения должны удовлетворять требованиям к трафику, приведенным в разделе [Проверка трассировки сети для протокола UDP WS-Discovery](inspecting-network-traces-for-udp-ws-discovery.md), если только это не является абсолютно уверенным, что WS-Discovery не используется для обмена метаданными.</span><span class="sxs-lookup"><span data-stu-id="8243c-122">Messages must meet the traffic requirements provided in the topic [Inspecting Network Traces for UDP WS-Discovery](inspecting-network-traces-for-udp-ws-discovery.md), unless it is absolutely certain that WS-Discovery is not being used for metadata exchange.</span></span>
-   <span data-ttu-id="8243c-123">Должно быть установлено TCP-соединение между клиентом и первым транспортным адресом, указанным в элементе **ксаддрс** сообщения [ProbeMatch](probematches-message.md) или [ресолвематчес](resolvematches-message.md) .</span><span class="sxs-lookup"><span data-stu-id="8243c-123">A TCP connection must be established between the client and the first transport address provided in the **XAddrs** element of a [ProbeMatches](probematches-message.md) or [ResolveMatches](resolvematches-message.md) message.</span></span> <span data-ttu-id="8243c-124">В следующем списке показан типичный обмен пакетами, используемый для установления TCP-соединения.</span><span class="sxs-lookup"><span data-stu-id="8243c-124">The following list shows a typical packet exchange used to establish a TCP connection.</span></span>
    -   <span data-ttu-id="8243c-125">Клиент отправляет пакет TCP SYN на узел с указанным портом.</span><span class="sxs-lookup"><span data-stu-id="8243c-125">The client sends a TCP SYN packet to the host at a specified port.</span></span>
    -   <span data-ttu-id="8243c-126">Узел отправляет клиенту пакет TCP SYN/ACK.</span><span class="sxs-lookup"><span data-stu-id="8243c-126">The host sends a TCP SYN/ACK packet to the client.</span></span>
    -   <span data-ttu-id="8243c-127">Клиент отправляет пакет TCP ACK узлу по указанному порту.</span><span class="sxs-lookup"><span data-stu-id="8243c-127">The client sends a TCP ACK packet to the host at a specified port.</span></span>

    <span data-ttu-id="8243c-128">После отправки клиентом пакета TCP ACK устанавливается подключение TCP.</span><span class="sxs-lookup"><span data-stu-id="8243c-128">Once the client has sent a TCP ACK packet, the TCP connection is established.</span></span> <span data-ttu-id="8243c-129">Обратите внимание, что обмен сообщениями не произойдет, если подключение TCP было установлено ранее.</span><span class="sxs-lookup"><span data-stu-id="8243c-129">Note that this message exchange will not occur if a TCP connection has previously been established.</span></span>
-   <span data-ttu-id="8243c-130">Клиент должен отправить допустимый запрос [Get](get--metadata-exchange--http-request-and-message.md) HTTP и сообщение.</span><span class="sxs-lookup"><span data-stu-id="8243c-130">The client must send a valid [Get](get--metadata-exchange--http-request-and-message.md) HTTP request and message.</span></span>
-   <span data-ttu-id="8243c-131">Узел должен прослушиваться по URL-пути, указанному в запросе [Get](get--metadata-exchange--http-request-and-message.md) HTTP.</span><span class="sxs-lookup"><span data-stu-id="8243c-131">The host must be listening on the URL path specified in the [Get](get--metadata-exchange--http-request-and-message.md) HTTP request.</span></span>
-   <span data-ttu-id="8243c-132">Элемент **to** сообщения [получения](get--metadata-exchange--http-request-and-message.md) метаданных должен быть указан и не пуст.</span><span class="sxs-lookup"><span data-stu-id="8243c-132">The **To** element of a [Get](get--metadata-exchange--http-request-and-message.md) metadata message must be present and not empty.</span></span> <span data-ttu-id="8243c-133">Значение элемента **to** должно соответствовать одному из адресов конечной точки узла.</span><span class="sxs-lookup"><span data-stu-id="8243c-133">The value of the **To** element must match one of the host's endpoint addresses.</span></span> <span data-ttu-id="8243c-134">Адрес конечной точки узла обычно объявляется в сообщении [ProbeMatch](probematches-message.md) или [ресолвематчес](resolvematches-message.md) .</span><span class="sxs-lookup"><span data-stu-id="8243c-134">A host's endpoint address is typically advertised in a [ProbeMatches](probematches-message.md) or [ResolveMatches](resolvematches-message.md) message.</span></span>
-   <span data-ttu-id="8243c-135">Узел должен отправить допустимый заголовок ответа HTTP.</span><span class="sxs-lookup"><span data-stu-id="8243c-135">The host must send a valid HTTP response header.</span></span> <span data-ttu-id="8243c-136">Если первоначальный запрос был успешным, заголовок ответа должен содержать код состояния HTTP/1.1 200.</span><span class="sxs-lookup"><span data-stu-id="8243c-136">If the initial request was successful, the response header should contain the HTTP/1.1 200 status code.</span></span>
-   <span data-ttu-id="8243c-137">Узел должен отправить допустимое сообщение [GetResponse](getresponse--metadata-exchange--message.md) .</span><span class="sxs-lookup"><span data-stu-id="8243c-137">The host must send a valid [GetResponse](getresponse--metadata-exchange--message.md) message.</span></span>
-   <span data-ttu-id="8243c-138">Элемент **очистки** сообщения [GetResponse](getresponse--metadata-exchange--message.md) должен присутствовать и не должен быть пустым.</span><span class="sxs-lookup"><span data-stu-id="8243c-138">The **RelatesTo** element of a [GetResponse](getresponse--metadata-exchange--message.md) message must be present and must not be empty.</span></span> <span data-ttu-id="8243c-139">Его значение должно соответствовать значению элемента **MessageId** из соответствующего сообщения [Get](get--metadata-exchange--http-request-and-message.md) .</span><span class="sxs-lookup"><span data-stu-id="8243c-139">Its value must match the value of the **MessageId** element from the corresponding [Get](get--metadata-exchange--http-request-and-message.md) message.</span></span>

<span data-ttu-id="8243c-140">Если HTTP-запросы или сообщения обмена метаданными, отправленные программой, не соответствуют этим требованиям к трафику, причина проблемы была идентифицирована успешно и дальнейшие действия по устранению неполадок не требуются.</span><span class="sxs-lookup"><span data-stu-id="8243c-140">If the HTTP requests or metadata exchange messages sent by the program do not conform to these traffic requirements, the cause of the problem has been successfully identified and no further troubleshooting steps are necessary.</span></span> <span data-ttu-id="8243c-141">Перепишите программу таким образом, чтобы она создавала согласованные сообщения и запросы и повторно протестировать программу.</span><span class="sxs-lookup"><span data-stu-id="8243c-141">Rewrite the program so that it generates conformant messages and requests and retest the program.</span></span>

<span data-ttu-id="8243c-142">Если источник проблемы по-прежнему не удается определить, обратитесь за помощью в службу поддержки Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="8243c-142">If the source of the problem still cannot be identified, contact Microsoft support for assistance.</span></span> <span data-ttu-id="8243c-143">Перед обращением в службу поддержки собирайте соответствующие файлы журналов, чтобы определить основную причину проблемы.</span><span class="sxs-lookup"><span data-stu-id="8243c-143">Before contacting support, collect the appropriate log files to help identify the root cause of the problem.</span></span> <span data-ttu-id="8243c-144">Дополнительные сведения см. в разделе [Включение трассировки WSDAPI](enabling-wsdapi-tracing.md).</span><span class="sxs-lookup"><span data-stu-id="8243c-144">For more information, see [Enabling WSDAPI Tracing](enabling-wsdapi-tracing.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="8243c-145">См. также</span><span class="sxs-lookup"><span data-stu-id="8243c-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8243c-146">Процедуры диагностики WSDAPI</span><span class="sxs-lookup"><span data-stu-id="8243c-146">WSDAPI Diagnostic Procedures</span></span>](wsdapi-diagnostic-procedures.md)
</dt> <dt>

[<span data-ttu-id="8243c-147">начало работы с разрешениями WSDAPI</span><span class="sxs-lookup"><span data-stu-id="8243c-147">Getting Started with WSDAPI Troubleshooting</span></span>](getting-started-with-wsdapi-troubleshooting.md)
</dt> <dt>

[<span data-ttu-id="8243c-148">Загрузка Netmon и примеров фильтров DPWS</span><span class="sxs-lookup"><span data-stu-id="8243c-148">Downloading Netmon and Sample DPWS Filters</span></span>](downloading-netmon-and-sample-dpws-filters.md)
</dt> </dl>

 

 



