---
description: AppSequence сведения, содержащиеся в сообщениях WS-Discovery объявлений и ответах (Привет, ProbeMatch и Ресолвематчес).
ms.assetid: f54eaa09-7ce8-4948-a0c5-edf2d054f6d5
title: Правила проверки AppSequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ea44c1ee2d157608ddd1756e71d7183f310df87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544815"
---
# <a name="appsequence-validation-rules"></a><span data-ttu-id="4515e-103">Правила проверки AppSequence</span><span class="sxs-lookup"><span data-stu-id="4515e-103">AppSequence Validation Rules</span></span>

<span data-ttu-id="4515e-104">AppSequence сведения, содержащиеся в сообщениях WS-Discovery объявлений и ответах ([Привет](hello-message.md), [ProbeMatch](probematches-message.md)и [ресолвематчес](resolvematches-message.md)).</span><span class="sxs-lookup"><span data-stu-id="4515e-104">AppSequence information contained in WS-Discovery announcement and response messages ([Hello](hello-message.md), [ProbeMatches](probematches-message.md), and [ResolveMatches](resolvematches-message.md)).</span></span> <span data-ttu-id="4515e-105">Эти сведения обрабатываются и проверяются WSDAPI, прежде чем эти сообщения передаются в компоненты выше стека (например, сетевой обозреватель или приложение, вызывающее в WSDAPI).</span><span class="sxs-lookup"><span data-stu-id="4515e-105">This information is processed and validated by WSDAPI before these messages are passed on to components above the stack (such as Network Explorer or an application calling into WSDAPI).</span></span>

<span data-ttu-id="4515e-106">В следующем коде XML показан пример элемента AppSequence.</span><span class="sxs-lookup"><span data-stu-id="4515e-106">The following XML shows a sample AppSequence element.</span></span> <span data-ttu-id="4515e-107">Префикс WSD ссылается на пространство имен `https://schemas.xmlsoap.org/ws/2005/04/discovery` .</span><span class="sxs-lookup"><span data-stu-id="4515e-107">The wsd prefix refers to the namespace `https://schemas.xmlsoap.org/ws/2005/04/discovery`.</span></span>

``` syntax
<wsd:AppSequence InstanceId="2"
    SequenceId="urn:uuid:369a7d7b-5f87-48a4-aa9a-189edf2a8772"
    MessageNumber="21">
</wsd:AppSequence>
```

<span data-ttu-id="4515e-108">WSDAPI игнорирует устаревшие сообщения.</span><span class="sxs-lookup"><span data-stu-id="4515e-108">WSDAPI ignores stale messages.</span></span> <span data-ttu-id="4515e-109">Для каждого устройства (уникально идентифицируемого адресом конечной точки в теле SOAP) протокол WSDAPI игнорирует все сообщения с AppSequence MessageNumber ниже последнего отображаемого сообщения.</span><span class="sxs-lookup"><span data-stu-id="4515e-109">For each device (uniquely identified by the Endpoint Address in the SOAP Body), WSDAPI ignores any messages with an AppSequence MessageNumber lower than the last message seen.</span></span>

<span data-ttu-id="4515e-110">WSDAPI игнорирует устаревшие объявления Ксаддр.</span><span class="sxs-lookup"><span data-stu-id="4515e-110">WSDAPI ignores stale XAddr announcements.</span></span> <span data-ttu-id="4515e-111">Если значение InstanceId AppSequence меньше, чем последний замеченный InstanceId, то WSDAPI игнорирует Ксаддрс, объявленный в теле SOAP.</span><span class="sxs-lookup"><span data-stu-id="4515e-111">If the AppSequence InstanceId is lower than the last InstanceId seen, WSDAPI ignores the XAddrs advertised in the SOAP body.</span></span> <span data-ttu-id="4515e-112">Кроме того, если InstanceId совпадает с предыдущим, но Метадатаверсион меньше, чем последний Метадатаверсион, то WSDAPI игнорирует Ксаддрс.</span><span class="sxs-lookup"><span data-stu-id="4515e-112">Also, if the InstanceId is the same as previous but the MetadataVersion is lower than the last MetadataVersion, WSDAPI ignores the XAddrs.</span></span>

<span data-ttu-id="4515e-113">WSDAPI игнорирует дублирующиеся WS-Discovery сообщения.</span><span class="sxs-lookup"><span data-stu-id="4515e-113">WSDAPI ignores duplicate WS-Discovery messages.</span></span> <span data-ttu-id="4515e-114">Если в WSDAPI отправляется два одинаковых WS-Discovery сообщений, то обрабатываются только первые полученные.</span><span class="sxs-lookup"><span data-stu-id="4515e-114">If two identical WS-Discovery messages are sent to WSDAPI, only the first received will be processed.</span></span> <span data-ttu-id="4515e-115">Обычно это относится только к приложениям, которые напрямую вызывают интерфейсы [**ивсдисковерипублишер**](/windows/desktop/api/WsdDisco/nn-wsddisco-iwsdiscoverypublisher) или [**ивсдисковерипровидер**](/windows/desktop/api/WsdDisco/nn-wsddisco-iwsdiscoveryprovider) .</span><span class="sxs-lookup"><span data-stu-id="4515e-115">This is typically only relevant for applications that call directly into the [**IWSDiscoveryPublisher**](/windows/desktop/api/WsdDisco/nn-wsddisco-iwsdiscoverypublisher) or [**IWSDiscoveryProvider**](/windows/desktop/api/WsdDisco/nn-wsddisco-iwsdiscoveryprovider) interfaces.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4515e-116">См. также</span><span class="sxs-lookup"><span data-stu-id="4515e-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4515e-117">Шаблоны сообщений обнаружения и обмена метаданными</span><span class="sxs-lookup"><span data-stu-id="4515e-117">Discovery and Metadata Exchange Message Patterns</span></span>](discovery-and-metadata-exchange-message-patterns.md)
</dt> </dl>

 

 



