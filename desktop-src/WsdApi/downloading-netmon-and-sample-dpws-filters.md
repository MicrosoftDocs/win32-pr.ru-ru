---
description: Microsoft Network Monitor 3 (Netmon) — анализатор пакетов, используемый для проверки сетевого трафика.
ms.assetid: 015a6a6d-9e07-4f22-b931-dcce77051bef
title: Загрузка Netmon и примеров фильтров DPWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47790b26164ec0ed2792d1d1e1f2ad4ba5d77d38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692818"
---
# <a name="downloading-netmon-and-sample-dpws-filters"></a><span data-ttu-id="75901-103">Загрузка Netmon и примеров фильтров DPWS</span><span class="sxs-lookup"><span data-stu-id="75901-103">Downloading Netmon and Sample DPWS Filters</span></span>

<span data-ttu-id="75901-104">Microsoft Network Monitor 3 (Netmon) — анализатор пакетов, используемый для проверки сетевого трафика.</span><span class="sxs-lookup"><span data-stu-id="75901-104">Microsoft Network Monitor 3 (Netmon) is a packet analyzer used to inspect network traffic.</span></span> <span data-ttu-id="75901-105">Сетевой монитор должен быть скачан перед действиями по устранению неполадок, описанных в статье [Проверка трассировки сети для протокола UDP WS-Discovery](inspecting-network-traces-for-udp-ws-discovery.md) и [Проверка трассировки сети для обмена метаданными HTTP](inspecting-network-traces-for-http-metadata-exchange.md) .</span><span class="sxs-lookup"><span data-stu-id="75901-105">Netmon must be downloaded before the troubleshooting steps given in [Inspecting Network Traces for UDP WS-Discovery](inspecting-network-traces-for-udp-ws-discovery.md) and [Inspecting Network Traces for HTTP Metadata Exchange](inspecting-network-traces-for-http-metadata-exchange.md) can be followed.</span></span> <span data-ttu-id="75901-106">После загрузки netmon можно использовать фильтры DPWS, помогающие изолировать интересующий вас трафик.</span><span class="sxs-lookup"><span data-stu-id="75901-106">After Netmon has been downloaded, DPWS filters can be used to help isolate traffic of interest.</span></span>

## <a name="downloading-netmon"></a><span data-ttu-id="75901-107">Загрузка Netmon</span><span class="sxs-lookup"><span data-stu-id="75901-107">Downloading Netmon</span></span>

<span data-ttu-id="75901-108">Чтобы скачать NetMon, перейдите по адресу [Microsoft Network Monitor](https://www.microsoft.com/downloads/details.aspx?displaylang=en&FamilyID=983b941d-06cb-4658-b7f6-3088333d062f) и следуйте инструкциям.</span><span class="sxs-lookup"><span data-stu-id="75901-108">To download Netmon, go to [Microsoft Network Monitor](https://www.microsoft.com/downloads/details.aspx?displaylang=en&FamilyID=983b941d-06cb-4658-b7f6-3088333d062f) and follow the instructions.</span></span> <span data-ttu-id="75901-109">Дополнительные сведения о netmon см. в разделе «сведения о сетевой монитор 3,0» в базе знаний справки и поддержки по адресу [https://support.microsoft.com/kb/933741](https://support.microsoft.com/kb/933741) .</span><span class="sxs-lookup"><span data-stu-id="75901-109">For more information about Netmon, see "Information about Network Monitor 3.0" in the Help and Support Knowledge Base at [https://support.microsoft.com/kb/933741](https://support.microsoft.com/kb/933741).</span></span>

## <a name="sample-dpws-filters"></a><span data-ttu-id="75901-110">Примеры фильтров DPWS</span><span class="sxs-lookup"><span data-stu-id="75901-110">Sample DPWS Filters</span></span>

<span data-ttu-id="75901-111">Иногда WS-Discovery и устранение неполадок в обмене метаданными должны происходить в занятой сети.</span><span class="sxs-lookup"><span data-stu-id="75901-111">Sometimes, WS-Discovery and metadata exchange troubleshooting must take place on a busy network.</span></span> <span data-ttu-id="75901-112">Примеры фильтров можно использовать для ограничения выходных данных NetMon на интересующий вас трафик.</span><span class="sxs-lookup"><span data-stu-id="75901-112">The sample filters can be used to help limit the Netmon output to traffic of interest.</span></span> <span data-ttu-id="75901-113">Дополнительные сведения об использовании фильтров Netmon см. в разделе [https://support.microsoft.com/kb/933741](https://support.microsoft.com/kb/933741) .</span><span class="sxs-lookup"><span data-stu-id="75901-113">For more information about using Netmon filters, see [https://support.microsoft.com/kb/933741](https://support.microsoft.com/kb/933741).</span></span>

<span data-ttu-id="75901-114">В следующем примере показан фильтр, ограничивающий вывод для всех широковещательных WS-Discovery трафика.</span><span class="sxs-lookup"><span data-stu-id="75901-114">The following example shows a filter that limits output to all broadcast WS-Discovery traffic.</span></span>

> [!Note]  
> <span data-ttu-id="75901-115">Этот фильтр не записывает трафик из стеков, которые не отвечают на многоадресные WS-Discovery сообщениям, источником которых является порт 3702.</span><span class="sxs-lookup"><span data-stu-id="75901-115">This filter does not capture traffic from stacks that do not respond to multicast WS-Discovery messages that originate at port 3702.</span></span> <span data-ttu-id="75901-116">Если такой стек используется, то этот образец фильтра необходимо изменить перед использованием.</span><span class="sxs-lookup"><span data-stu-id="75901-116">If such a stack is being used, then this sample filter must be modified before use.</span></span>

 

``` syntax
// All broadcast WS-Discovery traffic
UDP.Port == 3702
```

<span data-ttu-id="75901-117">В следующем примере показан фильтр, ограничивающий вывод HTTP-сообщений, отправляемых в стеки WSDAPI на порте по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="75901-117">The following example shows a filter that limits output to HTTP messages sent to WSDAPI stacks on the default port.</span></span>

> [!Note]  
> <span data-ttu-id="75901-118">Службы могут отсылать соответствующие HTTP-сообщения от портов, отличных от 5357.</span><span class="sxs-lookup"><span data-stu-id="75901-118">Services may send relevant HTTP messages from ports other than 5357.</span></span> <span data-ttu-id="75901-119">Если трафик от других портов представляет интерес, этот фильтр необходимо изменить перед использованием.</span><span class="sxs-lookup"><span data-stu-id="75901-119">If traffic from other ports is of interest, then this sample filter must be modified before use.</span></span>

 

``` syntax
// HTTP messages sent to WSDAPI stacks on default port
TCP.Port == 5357
```

<span data-ttu-id="75901-120">В следующем примере показан фильтр, который ограничивает выходные данные трафиком многоадресной рассылки IPv4.</span><span class="sxs-lookup"><span data-stu-id="75901-120">The following example shows a filter that limits output to IPv4 multicast traffic.</span></span>

``` syntax
// All IPv4 multicast traffic
IPv4.DestinationAddress == 239.255.255.250
```

<span data-ttu-id="75901-121">В следующем примере показан фильтр, который ограничивает вывод трафика многоадресной рассылки IPv6.</span><span class="sxs-lookup"><span data-stu-id="75901-121">The following example shows a filter that limits output to IPv6 multicast traffic.</span></span>

``` syntax
// All IPv6 multicast traffic
IPv6.DestinationAddress == FF02::C
```

<span data-ttu-id="75901-122">Некоторые фильтры можно комбинировать для дальнейшего ограничения результатов.</span><span class="sxs-lookup"><span data-stu-id="75901-122">Some filters can be combined to further limit results.</span></span> <span data-ttu-id="75901-123">В следующем примере показан фильтр, ограничивающий вывод на многоадресный трафик IPv4 WS-Discovery.</span><span class="sxs-lookup"><span data-stu-id="75901-123">The following example shows a filter that limits output to IPv4 multicast WS-Discovery traffic.</span></span>

``` syntax
// All IPv4 multicast WS-Discovery traffic
UDP.Port==3702 && IPv4.DestinationAddress=239.255.255.250
```

<span data-ttu-id="75901-124">При использовании этих фильтров соответствующий трафик может быть исключен из результатов Netmon.</span><span class="sxs-lookup"><span data-stu-id="75901-124">When these filters are used, relevant traffic may be excluded from the Netmon results.</span></span> <span data-ttu-id="75901-125">Исключение может возникать, если службы находятся на портах, отличных от портов по умолчанию (5357/5358), а стек DPWS не отвечает на сообщения с помощью порта по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="75901-125">Exclusion can occur when services reside at ports other than the default ports (5357/5358) and when a DPWS stack does not respond to messages using the default port.</span></span> <span data-ttu-id="75901-126">В таких случаях необходимо изменить фильтры перед использованием.</span><span class="sxs-lookup"><span data-stu-id="75901-126">In these cases, the filters must be modified before use.</span></span>

## <a name="related-topics"></a><span data-ttu-id="75901-127">См. также</span><span class="sxs-lookup"><span data-stu-id="75901-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="75901-128">Процедуры диагностики WSDAPI</span><span class="sxs-lookup"><span data-stu-id="75901-128">WSDAPI Diagnostic Procedures</span></span>](wsdapi-diagnostic-procedures.md)
</dt> <dt>

[<span data-ttu-id="75901-129">начало работы с разрешениями WSDAPI</span><span class="sxs-lookup"><span data-stu-id="75901-129">Getting Started with WSDAPI Troubleshooting</span></span>](getting-started-with-wsdapi-troubleshooting.md)
</dt> </dl>

 

 



