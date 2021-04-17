---
description: Любой анализатор сетевых пакетов, который может отображать необработанные пакеты, может использоваться для проверки запросов на обмен метаданными HTTP. Рекомендуется Microsoft Network Monitor 3 (Netmon). Дополнительные сведения о netmon см. в статье Загрузка Netmon и примеры DPWS Filters.
ms.assetid: 9b124117-06e7-4637-9863-0f9650861526
title: Проверка трассировки сети для приложений с помощью направленного обнаружения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98a424117896c18a5fcf84c883ba824b8223ef01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693588"
---
# <a name="inspecting-network-traces-for-applications-using-directed-discovery"></a><span data-ttu-id="e9a2e-105">Проверка трассировки сети для приложений с помощью направленного обнаружения</span><span class="sxs-lookup"><span data-stu-id="e9a2e-105">Inspecting Network Traces for Applications Using Directed Discovery</span></span>

<span data-ttu-id="e9a2e-106">Любой анализатор сетевых пакетов, который может отображать необработанные пакеты, может использоваться для проверки запросов на обмен метаданными HTTP.</span><span class="sxs-lookup"><span data-stu-id="e9a2e-106">Any network packet analyzer that can display raw packets can be used to inspect HTTP metadata exchange requests.</span></span> <span data-ttu-id="e9a2e-107">Рекомендуется Microsoft Network Monitor 3 (Netmon).</span><span class="sxs-lookup"><span data-stu-id="e9a2e-107">Microsoft Network Monitor 3 (Netmon) is recommended.</span></span> <span data-ttu-id="e9a2e-108">Дополнительные сведения о netmon см. в статье [Загрузка Netmon и примеры DPWS Filters](downloading-netmon-and-sample-dpws-filters.md).</span><span class="sxs-lookup"><span data-stu-id="e9a2e-108">For more information about Netmon, see [Downloading Netmon and Sample DPWS Filters](downloading-netmon-and-sample-dpws-filters.md).</span></span>

<span data-ttu-id="e9a2e-109">**Проверка трассировки сети для направленного обнаружения**</span><span class="sxs-lookup"><span data-stu-id="e9a2e-109">**To inspect network traces for directed discovery**</span></span>

1.  <span data-ttu-id="e9a2e-110">Настройте узел и клиент для работы по сети (то есть убедитесь, что узел и клиент будут работать на разных компьютерах).</span><span class="sxs-lookup"><span data-stu-id="e9a2e-110">Configure the host and client to run across the network (that is, make sure that the host and client will operate on different machines).</span></span>
2.  <span data-ttu-id="e9a2e-111">Установите анализатор пакетов (Netmon) на клиенте или на узле.</span><span class="sxs-lookup"><span data-stu-id="e9a2e-111">Install the packet analyzer (Netmon) on either the client or the host.</span></span>
3.  <span data-ttu-id="e9a2e-112">Настройте анализатор пакетов для записи трафика на сетевом адаптере, соединяющем узел и клиент.</span><span class="sxs-lookup"><span data-stu-id="e9a2e-112">Configure the packet analyzer to capture traffic on the network adapter connecting the host and the client.</span></span>
4.  <span data-ttu-id="e9a2e-113">Воспроизведите ошибку, запустив узел и клиент или нажав клавишу F5 в обозревателе сети.</span><span class="sxs-lookup"><span data-stu-id="e9a2e-113">Reproduce the failure by starting the host and client or by pressing F5 in the Network Explorer.</span></span>
5.  <span data-ttu-id="e9a2e-114">Отфильтруйте результаты, чтобы изолировать WS-Discovery и трафик обмена метаданными.</span><span class="sxs-lookup"><span data-stu-id="e9a2e-114">Filter the results to isolate WS-Discovery and metadata exchange traffic.</span></span> <span data-ttu-id="e9a2e-115">Чтобы просмотреть примеры фильтров Netmon, см. [статью Загрузка Netmon и примеры DPWS Filters](downloading-netmon-and-sample-dpws-filters.md).</span><span class="sxs-lookup"><span data-stu-id="e9a2e-115">To view sample Netmon filters, see [Downloading Netmon and Sample DPWS Filters](downloading-netmon-and-sample-dpws-filters.md).</span></span>
    > [!Note]  
    > <span data-ttu-id="e9a2e-116">Это необязательный шаг.</span><span class="sxs-lookup"><span data-stu-id="e9a2e-116">This step is optional.</span></span>

     

6.  <span data-ttu-id="e9a2e-117">Убедитесь, что сообщения, передаваемые между клиентом и узлом, соответствуют основным требованиям к трафику.</span><span class="sxs-lookup"><span data-stu-id="e9a2e-117">Verify that messages sent between client and host meet basic traffic requirements.</span></span>

## <a name="verifying-that-messages-meet-traffic-requirements"></a><span data-ttu-id="e9a2e-118">Проверка соответствия сообщений требованиям к трафику</span><span class="sxs-lookup"><span data-stu-id="e9a2e-118">Verifying that messages meet traffic requirements</span></span>

<span data-ttu-id="e9a2e-119">WSDAPI клиенты и узлы должны отправить сообщения, соответствующие следующим критериям.</span><span class="sxs-lookup"><span data-stu-id="e9a2e-119">WSDAPI clients and hosts must send messages that conform to the following criteria.</span></span> <span data-ttu-id="e9a2e-120">Общие сведения о шаблонах сообщений см. в статье [шаблоны сообщений обнаружения и обмена метаданными](discovery-and-metadata-exchange-message-patterns.md).</span><span class="sxs-lookup"><span data-stu-id="e9a2e-120">For general information about message patterns, see [Discovery and Metadata Exchange Message Patterns](discovery-and-metadata-exchange-message-patterns.md).</span></span>

-   <span data-ttu-id="e9a2e-121">Сообщения [пробы](probe-message.md) должны отправляться по протоколу HTTP или HTTPS, обычно к порту 5357 или 5358.</span><span class="sxs-lookup"><span data-stu-id="e9a2e-121">[Probe](probe-message.md) messages must be sent by HTTP or HTTPS, usually to port 5357 or 5358.</span></span>
-   <span data-ttu-id="e9a2e-122">Элемент **types** сообщения [пробы](probe-message.md) должен присутствовать и не должен быть пустым.</span><span class="sxs-lookup"><span data-stu-id="e9a2e-122">The **Types** element of a [Probe](probe-message.md) message must be present and must not be empty.</span></span> <span data-ttu-id="e9a2e-123">Он должен содержать типы, на которые будет отвечать узел.</span><span class="sxs-lookup"><span data-stu-id="e9a2e-123">It must contain the types to which a host will respond.</span></span>
-   <span data-ttu-id="e9a2e-124">Сообщение [ProbeMatch](probematches-message.md) должно быть отправлено на порт HTTP или HTTPS, с которого была отправлена [проба](probe-message.md) .</span><span class="sxs-lookup"><span data-stu-id="e9a2e-124">A [ProbeMatches](probematches-message.md) message must be sent to the HTTP or HTTPS port from which the [Probe](probe-message.md) was sent.</span></span>
-   <span data-ttu-id="e9a2e-125">Элемент очистки сообщения [ProbeMatch](probematches-message.md) должен **быть указан и** не должен быть пустым.</span><span class="sxs-lookup"><span data-stu-id="e9a2e-125">The **RelatesTo** element of a [ProbeMatches](probematches-message.md) message must be present and must not be empty.</span></span> <span data-ttu-id="e9a2e-126">Его значение должно соответствовать значению элемента **MessageId** из соответствующего сообщения [зонда](probe-message.md) .</span><span class="sxs-lookup"><span data-stu-id="e9a2e-126">Its value must match the value of the **MessageId** element from the corresponding [Probe](probe-message.md) message.</span></span>
-   <span data-ttu-id="e9a2e-127">Если элемент **ксаддрс** был добавлен в сообщение [ProbeMatch](probematches-message.md) , необходимо проверить предоставленные транспортные адреса.</span><span class="sxs-lookup"><span data-stu-id="e9a2e-127">If an **XAddrs** element was included in the [ProbeMatches](probematches-message.md) message, the supplied transport addresses must be validated.</span></span> <span data-ttu-id="e9a2e-128">Дополнительные сведения см. в разделе [правила проверки ксаддр](xaddr-validation-rules.md).</span><span class="sxs-lookup"><span data-stu-id="e9a2e-128">For more information, see [XAddr Validation Rules](xaddr-validation-rules.md).</span></span>
-   <span data-ttu-id="e9a2e-129">Сообщение [ProbeMatch](probematches-message.md) должно быть отправлено в течение 4 секунд соответствующего [проверочного](probe-message.md) сообщения.</span><span class="sxs-lookup"><span data-stu-id="e9a2e-129">A [ProbeMatches](probematches-message.md) message must be sent within 4 seconds of the corresponding [Probe](probe-message.md) message.</span></span> <span data-ttu-id="e9a2e-130">Брандмауэр Windows может удалить сообщение ProbeMatch, отправленное более 4 секунд после сообщения пробы.</span><span class="sxs-lookup"><span data-stu-id="e9a2e-130">The Windows Firewall may drop a ProbeMatches message sent more than 4 seconds after a Probe message.</span></span>
-   <span data-ttu-id="e9a2e-131">Если в сообщение [ProbeMatch](probematches-message.md) не включался элемент **ксаддрс** , а клиент или узел отправит HTTP-сообщение (например, запрос на [Получение](get--metadata-exchange--http-request-and-message.md) метаданных или сообщение службы), то клиент или узел должен отправить сообщение с [разрешением](resolve-message.md) по протоколу HTTP или HTTPS.</span><span class="sxs-lookup"><span data-stu-id="e9a2e-131">If no **XAddrs** element was included in the [ProbeMatches](probematches-message.md) message, and the client or host will send an HTTP message (such as a [Get](get--metadata-exchange--http-request-and-message.md) metadata exchange request or a service message), then the client or host must send a [Resolve](resolve-message.md) message by HTTP or HTTPS.</span></span> <span data-ttu-id="e9a2e-132">Это сообщение обычно отправляется на порт 5357 или 5358.</span><span class="sxs-lookup"><span data-stu-id="e9a2e-132">This message is usually sent to port 5357 or 5358.</span></span>
-   <span data-ttu-id="e9a2e-133">Если отправляется сообщение с [разрешением](resolve-message.md) , то сообщение [ресолвематчес](resolvematches-message.md) должно быть отправлено на порт HTTP или HTTPS, с которого было отправлено сообщение разрешения.</span><span class="sxs-lookup"><span data-stu-id="e9a2e-133">If a [Resolve](resolve-message.md) message is sent, then a [ResolveMatches](resolvematches-message.md) message must be sent to the HTTP or HTTPS port from which the Resolve message was sent.</span></span>
-   <span data-ttu-id="e9a2e-134">Сообщение [ресолвематчес](resolvematches-message.md) должно быть отправлено в течение 4 секунд соответствующего сообщения о [разрешении](resolve-message.md) .</span><span class="sxs-lookup"><span data-stu-id="e9a2e-134">A [ResolveMatches](resolvematches-message.md) message must be sent within 4 seconds of the corresponding [Resolve](resolve-message.md) message.</span></span> <span data-ttu-id="e9a2e-135">Брандмауэр Windows может удалить Ресолвематчесмессаже, отправленный после сообщения с разрешением более 4 секунд.</span><span class="sxs-lookup"><span data-stu-id="e9a2e-135">The Windows Firewall may drop a ResolveMatchesmessage sent more than 4 seconds after a Resolve message.</span></span>

<span data-ttu-id="e9a2e-136">Если сообщения, отправленные программой, не соответствуют этим требованиям к сообщениям, причина проблемы была идентифицирована успешно и дальнейшие действия по устранению неполадок не требуются.</span><span class="sxs-lookup"><span data-stu-id="e9a2e-136">If the messages sent by the program do not conform to these message requirements, the cause of the problem has been successfully identified and no further troubleshooting steps are necessary.</span></span> <span data-ttu-id="e9a2e-137">Перепишите программу таким образом, чтобы она создавала согласованные сообщения и повторно протестировать программу.</span><span class="sxs-lookup"><span data-stu-id="e9a2e-137">Rewrite the program so that it generates conformant messages and retest the program.</span></span>

<span data-ttu-id="e9a2e-138">Если источник проблемы по-прежнему не удается определить, обратитесь за помощью в службу поддержки Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="e9a2e-138">If the source of the problem still cannot be identified, contact Microsoft support for assistance.</span></span> <span data-ttu-id="e9a2e-139">Перед обращением в службу поддержки собирайте соответствующие файлы журналов, чтобы определить основную причину проблемы.</span><span class="sxs-lookup"><span data-stu-id="e9a2e-139">Before contacting support, collect the appropriate log files to help identify the root cause of the problem.</span></span> <span data-ttu-id="e9a2e-140">Дополнительные сведения см. в разделе [Включение трассировки WSDAPI](enabling-wsdapi-tracing.md).</span><span class="sxs-lookup"><span data-stu-id="e9a2e-140">For more information, see [Enabling WSDAPI Tracing](enabling-wsdapi-tracing.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e9a2e-141">См. также</span><span class="sxs-lookup"><span data-stu-id="e9a2e-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e9a2e-142">Устранение неполадок в приложениях с помощью направленного обнаружения</span><span class="sxs-lookup"><span data-stu-id="e9a2e-142">Troubleshooting Applications Using Directed Discovery</span></span>](troubleshooting-applications-using-directed-discovery.md)
</dt> <dt>

[<span data-ttu-id="e9a2e-143">Процедуры диагностики WSDAPI</span><span class="sxs-lookup"><span data-stu-id="e9a2e-143">WSDAPI Diagnostic Procedures</span></span>](wsdapi-diagnostic-procedures.md)
</dt> <dt>

[<span data-ttu-id="e9a2e-144">начало работы с разрешениями WSDAPI</span><span class="sxs-lookup"><span data-stu-id="e9a2e-144">Getting Started with WSDAPI Troubleshooting</span></span>](getting-started-with-wsdapi-troubleshooting.md)
</dt> <dt>

[<span data-ttu-id="e9a2e-145">Загрузка Netmon и примеров фильтров DPWS</span><span class="sxs-lookup"><span data-stu-id="e9a2e-145">Downloading Netmon and Sample DPWS Filters</span></span>](downloading-netmon-and-sample-dpws-filters.md)
</dt> </dl>

 

 



