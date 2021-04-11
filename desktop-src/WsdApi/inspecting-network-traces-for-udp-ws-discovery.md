---
description: Любой анализатор сетевых пакетов, который может отображать необработанные пакеты, может использоваться для проверки пакетов WS-Discovery UDP. Рекомендуется Microsoft Network Monitor 3 (Netmon). Дополнительные сведения о netmon см. в статье Загрузка Netmon и примеры DPWS Filters.
ms.assetid: f12f9847-b87f-4d5f-bee3-4d219f9ad898
title: Проверка трассировки сети для UDP-WS-Discovery
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f85f4acd79588ef48c7f8e1ace2a44c9a3458475
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104264791"
---
# <a name="inspecting-network-traces-for-udp-ws-discovery"></a><span data-ttu-id="2c988-105">Проверка трассировки сети для UDP-WS-Discovery</span><span class="sxs-lookup"><span data-stu-id="2c988-105">Inspecting Network Traces for UDP WS-Discovery</span></span>

<span data-ttu-id="2c988-106">Любой анализатор сетевых пакетов, который может отображать необработанные пакеты, может использоваться для проверки пакетов WS-Discovery UDP.</span><span class="sxs-lookup"><span data-stu-id="2c988-106">Any network packet analyzer that can display raw packets can be used to inspect UDP WS-Discovery packets.</span></span> <span data-ttu-id="2c988-107">Рекомендуется Microsoft Network Monitor 3 (Netmon).</span><span class="sxs-lookup"><span data-stu-id="2c988-107">Microsoft Network Monitor 3 (Netmon) is recommended.</span></span> <span data-ttu-id="2c988-108">Дополнительные сведения о netmon см. в статье [Загрузка Netmon и примеры DPWS Filters](downloading-netmon-and-sample-dpws-filters.md).</span><span class="sxs-lookup"><span data-stu-id="2c988-108">For more information about Netmon, see [Downloading Netmon and Sample DPWS Filters](downloading-netmon-and-sample-dpws-filters.md).</span></span>

<span data-ttu-id="2c988-109">**Проверка трассировки сети для протокола UDP WS-Discovery**</span><span class="sxs-lookup"><span data-stu-id="2c988-109">**To inspect network traces for UDP WS-Discovery**</span></span>

1.  <span data-ttu-id="2c988-110">Настройте узел и клиент для работы по сети (то есть убедитесь, что узел и клиент будут работать на разных компьютерах).</span><span class="sxs-lookup"><span data-stu-id="2c988-110">Configure the host and client to run across the network (that is, make sure that the host and client will operate on different machines).</span></span>
2.  <span data-ttu-id="2c988-111">Установите анализатор пакетов (Netmon) на клиенте или на узле.</span><span class="sxs-lookup"><span data-stu-id="2c988-111">Install the packet analyzer (Netmon) on either the client or the host.</span></span>
3.  <span data-ttu-id="2c988-112">Настройте анализатор пакетов для записи трафика на сетевом адаптере, соединяющем узел и клиент.</span><span class="sxs-lookup"><span data-stu-id="2c988-112">Configure the packet analyzer to capture traffic on the network adapter connecting the host and the client.</span></span>
4.  <span data-ttu-id="2c988-113">Воспроизведите ошибку, запустив узел и клиент или нажав клавишу F5 в обозревателе сети.</span><span class="sxs-lookup"><span data-stu-id="2c988-113">Reproduce the failure by starting the host and client or by pressing F5 in the Network Explorer.</span></span>
5.  <span data-ttu-id="2c988-114">Отфильтруйте результаты, чтобы изолировать WS-Discoveryный трафик.</span><span class="sxs-lookup"><span data-stu-id="2c988-114">Filter the results to isolate WS-Discovery traffic.</span></span> <span data-ttu-id="2c988-115">Чтобы просмотреть примеры фильтров Netmon, см. [статью Загрузка Netmon и примеры DPWS Filters](downloading-netmon-and-sample-dpws-filters.md).</span><span class="sxs-lookup"><span data-stu-id="2c988-115">To view sample Netmon filters, see [Downloading Netmon and Sample DPWS Filters](downloading-netmon-and-sample-dpws-filters.md).</span></span>
    > [!Note]  
    > <span data-ttu-id="2c988-116">Это необязательный шаг.</span><span class="sxs-lookup"><span data-stu-id="2c988-116">This step is optional.</span></span>

     

6.  <span data-ttu-id="2c988-117">Убедитесь, что сообщения, передаваемые между клиентом и узлом, соответствуют основным требованиям к трафику.</span><span class="sxs-lookup"><span data-stu-id="2c988-117">Verify that messages sent between client and host meet basic traffic requirements.</span></span>

## <a name="verifying-that-messages-meet-traffic-requirements"></a><span data-ttu-id="2c988-118">Проверка соответствия сообщений требованиям к трафику</span><span class="sxs-lookup"><span data-stu-id="2c988-118">Verifying that messages meet traffic requirements</span></span>

<span data-ttu-id="2c988-119">WSDAPI клиенты и узлы должны отправить сообщения, соответствующие следующим критериям.</span><span class="sxs-lookup"><span data-stu-id="2c988-119">WSDAPI clients and hosts must send messages that conform to the following criteria.</span></span> <span data-ttu-id="2c988-120">Общие сведения о шаблонах сообщений см. в статье [шаблоны сообщений обнаружения и обмена метаданными](discovery-and-metadata-exchange-message-patterns.md).</span><span class="sxs-lookup"><span data-stu-id="2c988-120">For general information about message patterns, see [Discovery and Metadata Exchange Message Patterns](discovery-and-metadata-exchange-message-patterns.md).</span></span>

-   <span data-ttu-id="2c988-121">Сообщения [пробы](probe-message.md) должны отправляться с помощью многоадресной рассылки UDP на порт 3702.</span><span class="sxs-lookup"><span data-stu-id="2c988-121">[Probe](probe-message.md) messages must be sent by UDP multicast to port 3702.</span></span>
-   <span data-ttu-id="2c988-122">Элемент **types** сообщения [пробы](probe-message.md) должен присутствовать и не должен быть пустым.</span><span class="sxs-lookup"><span data-stu-id="2c988-122">The **Types** element of a [Probe](probe-message.md) message must be present and must not be empty.</span></span> <span data-ttu-id="2c988-123">Он должен содержать типы, на которые будет отвечать узел.</span><span class="sxs-lookup"><span data-stu-id="2c988-123">It must contain the types to which a host will respond.</span></span>
-   <span data-ttu-id="2c988-124">Сообщение [ProbeMatch](probematches-message.md) должно быть отправлено на UDP-порт, с которого была отправлена [проба](probe-message.md) .</span><span class="sxs-lookup"><span data-stu-id="2c988-124">A [ProbeMatches](probematches-message.md) message must be sent unicast to the UDP port from which the [Probe](probe-message.md) was sent.</span></span>
-   <span data-ttu-id="2c988-125">Элемент очистки сообщения [ProbeMatch](probematches-message.md) должен **быть указан и** не должен быть пустым.</span><span class="sxs-lookup"><span data-stu-id="2c988-125">The **RelatesTo** element of a [ProbeMatches](probematches-message.md) message must be present and must not be empty.</span></span> <span data-ttu-id="2c988-126">Его значение должно соответствовать значению элемента **MessageId** из соответствующего сообщения [зонда](probe-message.md) .</span><span class="sxs-lookup"><span data-stu-id="2c988-126">Its value must match the value of the **MessageId** element from the corresponding [Probe](probe-message.md) message.</span></span>
-   <span data-ttu-id="2c988-127">Если элемент **ксаддрс** был добавлен в сообщение [ProbeMatch](probematches-message.md) , необходимо проверить предоставленные транспортные адреса.</span><span class="sxs-lookup"><span data-stu-id="2c988-127">If an **XAddrs** element was included in the [ProbeMatches](probematches-message.md) message, the supplied transport addresses must be validated.</span></span> <span data-ttu-id="2c988-128">Дополнительные сведения см. в разделе [правила проверки ксаддр](xaddr-validation-rules.md).</span><span class="sxs-lookup"><span data-stu-id="2c988-128">For more information, see [XAddr Validation Rules](xaddr-validation-rules.md).</span></span>
-   <span data-ttu-id="2c988-129">Сообщение [ProbeMatch](probematches-message.md) должно быть отправлено в течение 4 секунд соответствующего [проверочного](probe-message.md) сообщения.</span><span class="sxs-lookup"><span data-stu-id="2c988-129">A [ProbeMatches](probematches-message.md) message must be sent within 4 seconds of the corresponding [Probe](probe-message.md) message.</span></span> <span data-ttu-id="2c988-130">Брандмауэр Windows может удалить сообщение ProbeMatch, отправленное более 4 секунд после сообщения пробы.</span><span class="sxs-lookup"><span data-stu-id="2c988-130">The Windows Firewall may drop a ProbeMatches message sent more than 4 seconds after a Probe message.</span></span>
-   <span data-ttu-id="2c988-131">Если в сообщении [ProbeMatch](probematches-message.md) не было указано ни одного элемента **ксаддрс** , а клиент или узел отправит HTTP-сообщение (например, запрос на [Получение](get--metadata-exchange--http-request-and-message.md) метаданных или сообщение службы), клиент или узел должен отправить сообщение с [разрешением](resolve-message.md) по многоадресной рассылке UDP на порт 3702.</span><span class="sxs-lookup"><span data-stu-id="2c988-131">If no **XAddrs** element was included in the [ProbeMatches](probematches-message.md) message, and the client or host will send an HTTP message (such as a [Get](get--metadata-exchange--http-request-and-message.md) metadata exchange request or a service message), then the client or host must send a [Resolve](resolve-message.md) message by UDP multicast to port 3702.</span></span>
-   <span data-ttu-id="2c988-132">Если отправляется сообщение с [разрешением](resolve-message.md) , сообщение [ресолвематчес](resolvematches-message.md) должно быть отправлено по адресу UDP-порту, с которого было отправлено сообщение разрешения.</span><span class="sxs-lookup"><span data-stu-id="2c988-132">If a [Resolve](resolve-message.md) message is sent, then a [ResolveMatches](resolvematches-message.md) message must be sent unicast to the UDP port from which the Resolve message was sent.</span></span>
-   <span data-ttu-id="2c988-133">Сообщение [ресолвематчес](resolvematches-message.md) должно быть отправлено в течение 4 секунд соответствующего сообщения о [разрешении](resolve-message.md) .</span><span class="sxs-lookup"><span data-stu-id="2c988-133">A [ResolveMatches](resolvematches-message.md) message must be sent within 4 seconds of the corresponding [Resolve](resolve-message.md) message.</span></span> <span data-ttu-id="2c988-134">Брандмауэр Windows может удалить Ресолвематчесмессаже, отправленный после сообщения с разрешением более 4 секунд.</span><span class="sxs-lookup"><span data-stu-id="2c988-134">The Windows Firewall may drop a ResolveMatchesmessage sent more than 4 seconds after a Resolve message.</span></span>

<span data-ttu-id="2c988-135">Если сообщения, отправленные программой, не соответствуют этим требованиям к сообщениям, причина проблемы была идентифицирована успешно и дальнейшие действия по устранению неполадок не требуются.</span><span class="sxs-lookup"><span data-stu-id="2c988-135">If the messages sent by the program do not conform to these message requirements, the cause of the problem has been successfully identified and no further troubleshooting steps are necessary.</span></span> <span data-ttu-id="2c988-136">Перепишите программу таким образом, чтобы она создавала согласованные сообщения и повторно протестировать программу.</span><span class="sxs-lookup"><span data-stu-id="2c988-136">Rewrite the program so that it generates conformant messages and retest the program.</span></span>

<span data-ttu-id="2c988-137">Если источник проблемы по-прежнему не удается определить, обратитесь за помощью в службу поддержки Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="2c988-137">If the source of the problem still cannot be identified, contact Microsoft support for assistance.</span></span> <span data-ttu-id="2c988-138">Перед обращением в службу поддержки собирайте соответствующие файлы журналов, чтобы определить основную причину проблемы.</span><span class="sxs-lookup"><span data-stu-id="2c988-138">Before contacting support, collect the appropriate log files to help identify the root cause of the problem.</span></span> <span data-ttu-id="2c988-139">Дополнительные сведения см. в разделе [Включение трассировки WSDAPI](enabling-wsdapi-tracing.md).</span><span class="sxs-lookup"><span data-stu-id="2c988-139">For more information, see [Enabling WSDAPI Tracing](enabling-wsdapi-tracing.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="2c988-140">См. также</span><span class="sxs-lookup"><span data-stu-id="2c988-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2c988-141">Процедуры диагностики WSDAPI</span><span class="sxs-lookup"><span data-stu-id="2c988-141">WSDAPI Diagnostic Procedures</span></span>](wsdapi-diagnostic-procedures.md)
</dt> <dt>

[<span data-ttu-id="2c988-142">начало работы с разрешениями WSDAPI</span><span class="sxs-lookup"><span data-stu-id="2c988-142">Getting Started with WSDAPI Troubleshooting</span></span>](getting-started-with-wsdapi-troubleshooting.md)
</dt> <dt>

[<span data-ttu-id="2c988-143">Загрузка Netmon и примеров фильтров DPWS</span><span class="sxs-lookup"><span data-stu-id="2c988-143">Downloading Netmon and Sample DPWS Filters</span></span>](downloading-netmon-and-sample-dpws-filters.md)
</dt> </dl>

 

 



