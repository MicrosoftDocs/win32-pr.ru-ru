---
description: Список диагностических процедур, используемых при устранении неполадок клиентов обнаружения функций.
ms.assetid: e488882a-fadd-4150-89ef-b958c3df34c6
title: Устранение неполадок клиентов обнаружения функций
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a44c17b269a604efa1f5f999dff22211cee24f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811399"
---
# <a name="troubleshooting-function-discovery-clients"></a><span data-ttu-id="19e1f-103">Устранение неполадок клиентов обнаружения функций</span><span class="sxs-lookup"><span data-stu-id="19e1f-103">Troubleshooting Function Discovery Clients</span></span>

<span data-ttu-id="19e1f-104">Клиенты обнаружения функций:</span><span class="sxs-lookup"><span data-stu-id="19e1f-104">Function Discovery clients:</span></span>

-   <span data-ttu-id="19e1f-105">Всегда использовать WS-Discovery UDP для обнаружения устройств</span><span class="sxs-lookup"><span data-stu-id="19e1f-105">Always use UDP WS-Discovery for device discovery</span></span>
-   <span data-ttu-id="19e1f-106">Всегда инициируйте подключения по протоколу HTTP или HTTPS для обмена метаданными</span><span class="sxs-lookup"><span data-stu-id="19e1f-106">Always initiate HTTP or HTTPS connections for metadata exchange</span></span>
-   <span data-ttu-id="19e1f-107">Иногда используется направленное обнаружение</span><span class="sxs-lookup"><span data-stu-id="19e1f-107">Sometimes use directed discovery</span></span>
-   <span data-ttu-id="19e1f-108">Иногда для обмена метаданными используется безопасный канал (HTTPS)</span><span class="sxs-lookup"><span data-stu-id="19e1f-108">Sometimes use a secure channel (HTTPS) for metadata exchange</span></span>

<span data-ttu-id="19e1f-109">В следующем списке показана типичная последовательность сообщений, отправленных и полученных клиентами обнаружения функций.</span><span class="sxs-lookup"><span data-stu-id="19e1f-109">The following list shows the typical sequence of messages sent and received by Function Discovery clients.</span></span> <span data-ttu-id="19e1f-110">Не все сообщения являются обязательными.</span><span class="sxs-lookup"><span data-stu-id="19e1f-110">Not all messages are mandatory.</span></span>

1.  <span data-ttu-id="19e1f-111">Клиент отправляет [пробное](probe-message.md) сообщение для обнаружения устройств и служб.</span><span class="sxs-lookup"><span data-stu-id="19e1f-111">The client sends a [Probe](probe-message.md) message to discover devices and services.</span></span> <span data-ttu-id="19e1f-112">Если клиент использует направленное обнаружение, это сообщение отправляется по протоколу HTTP или HTTPS; в противном случае сообщение отправляется с помощью многоадресной рассылки UDP на порт 3702.</span><span class="sxs-lookup"><span data-stu-id="19e1f-112">If the client is using directed discovery then this message is sent over HTTP or HTTPS; otherwise, the message is sent by UDP multicast to port 3702.</span></span>
2.  <span data-ttu-id="19e1f-113">Клиент получает сообщения [ProbeMatch](probematches-message.md) от соответствующих устройств или служб.</span><span class="sxs-lookup"><span data-stu-id="19e1f-113">The client receives [ProbeMatches](probematches-message.md) messages from matching devices or services.</span></span> <span data-ttu-id="19e1f-114">Сообщения направленного обнаружения отправляются по протоколу HTTP или HTTPS; в противном случае эти сообщения отправляются по UDP-адресу и исходят с порта 3702.</span><span class="sxs-lookup"><span data-stu-id="19e1f-114">Directed discovery messages are sent over HTTP or HTTPS; otherwise, these messages are sent by UDP unicast and originate from port 3702.</span></span>
3.  <span data-ttu-id="19e1f-115">Если в сообщении ProbeMatch не было указано ни одного Ксаддрс, клиент отправит сообщение с [разрешением](resolve-message.md) по многоадресной рассылке UDP на порт 3702.</span><span class="sxs-lookup"><span data-stu-id="19e1f-115">If no XAddrs were included in the ProbeMatches message, then the client will send a [Resolve](resolve-message.md) message by UDP multicast to port 3702.</span></span>
4.  <span data-ttu-id="19e1f-116">Если сообщение с [разрешением](resolve-message.md) было отправлено, клиент получает сообщение [ресолвематчес](resolvematches-message.md) от соответствующих служб.</span><span class="sxs-lookup"><span data-stu-id="19e1f-116">If a [Resolve](resolve-message.md) message was sent, then the client receives a [ResolveMatches](resolvematches-message.md) message from matching services.</span></span> <span data-ttu-id="19e1f-117">Это сообщение отправляется по адресу UDP с порта 3702 на порт, в котором было создано сообщение разрешения.</span><span class="sxs-lookup"><span data-stu-id="19e1f-117">This message is sent by UDP unicast from port 3702 to the port where the Resolve message originated.</span></span>
5.  <span data-ttu-id="19e1f-118">Клиент отправляет сообщение [Get](get--metadata-exchange--http-request-and-message.md) для запроса метаданных от устройства или службы.</span><span class="sxs-lookup"><span data-stu-id="19e1f-118">The client sends a [Get](get--metadata-exchange--http-request-and-message.md) message to request metadata from the device or service.</span></span> <span data-ttu-id="19e1f-119">Это сообщение отправляется по протоколу HTTP или HTTPS.</span><span class="sxs-lookup"><span data-stu-id="19e1f-119">This message is sent by HTTP or HTTPS.</span></span>
6.  <span data-ttu-id="19e1f-120">Клиент получает сообщение [GetResponse](getresponse--metadata-exchange--message.md) с метаданными устройства или службы.</span><span class="sxs-lookup"><span data-stu-id="19e1f-120">The client receives a [GetResponse](getresponse--metadata-exchange--message.md) message with the device or service metadata.</span></span> <span data-ttu-id="19e1f-121">Это сообщение отправляется по протоколу HTTP или HTTPS.</span><span class="sxs-lookup"><span data-stu-id="19e1f-121">This message is sent by HTTP or HTTPS.</span></span>

<span data-ttu-id="19e1f-122">Следующие процедуры диагностики следует использовать (по порядку) для выявления проблем с клиентом обнаружения функций.</span><span class="sxs-lookup"><span data-stu-id="19e1f-122">The following diagnostic procedures should be used (in order) to help identify problems with a Function Discovery client.</span></span>

<span data-ttu-id="19e1f-123">**Устранение неполадок клиента обнаружения функций**</span><span class="sxs-lookup"><span data-stu-id="19e1f-123">**To troubleshoot a Function Discovery client**</span></span>

1.  <span data-ttu-id="19e1f-124">Если используется направленное обнаружение, [Устранение неполадок с помощью направленного обнаружения](troubleshooting-applications-using-directed-discovery.md).</span><span class="sxs-lookup"><span data-stu-id="19e1f-124">If directed discovery is used, [troubleshoot directed discovery](troubleshooting-applications-using-directed-discovery.md).</span></span>
2.  <span data-ttu-id="19e1f-125">[Проверьте параметры адаптера и брандмауэра](inspecting-adapter-and-firewall-settings.md).</span><span class="sxs-lookup"><span data-stu-id="19e1f-125">[Inspect adapter and firewall settings](inspecting-adapter-and-firewall-settings.md).</span></span>
3.  <span data-ttu-id="19e1f-126">[Используйте универсальный узел и клиент для протокола UDP WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md).</span><span class="sxs-lookup"><span data-stu-id="19e1f-126">[Use a generic host and client for UDP WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md).</span></span>
4.  <span data-ttu-id="19e1f-127">[Используйте клиент отладки WSD для проверки многоадресного трафика](using-wsddebug-client-to-verify-multicast-traffic.md).</span><span class="sxs-lookup"><span data-stu-id="19e1f-127">[Use WSD Debug Client to verify multicast traffic](using-wsddebug-client-to-verify-multicast-traffic.md).</span></span>
5.  <span data-ttu-id="19e1f-128">[Проверьте сетевые трассировки для протокола UDP WS-Discovery](inspecting-network-traces-for-udp-ws-discovery.md).</span><span class="sxs-lookup"><span data-stu-id="19e1f-128">[Inspect network traces for UDP WS-Discovery](inspecting-network-traces-for-udp-ws-discovery.md).</span></span>
6.  <span data-ttu-id="19e1f-129">[Используйте универсальный узел и клиент для обмена метаданными HTTP](using-a-generic-host-and-client-for-http-metadata-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="19e1f-129">[Use a generic host and client for HTTP metadata exchange](using-a-generic-host-and-client-for-http-metadata-exchange.md).</span></span>
7.  <span data-ttu-id="19e1f-130">[Используйте ведение журнала WinHTTP для проверки получения трафика](using-winhttp-logging-to-verify-get-traffic.md).</span><span class="sxs-lookup"><span data-stu-id="19e1f-130">[Use WinHTTP logging to verify Get traffic](using-winhttp-logging-to-verify-get-traffic.md).</span></span>
8.  <span data-ttu-id="19e1f-131">[Проверьте сетевые трассировки для обмена метаданными HTTP](inspecting-network-traces-for-http-metadata-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="19e1f-131">[Inspect network traces for HTTP metadata exchange](inspecting-network-traces-for-http-metadata-exchange.md).</span></span>

<span data-ttu-id="19e1f-132">Если источник проблемы не удается определить с помощью описанных выше процедур диагностики, следуйте инструкциям в статьях [Включение трассировки WSDAPI](enabling-wsdapi-tracing.md) и обратитесь в службу поддержки Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="19e1f-132">If the source of the problem cannot be identified using the above diagnostic procedures, follow the directions in [Enabling WSDAPI Tracing](enabling-wsdapi-tracing.md) and contact Microsoft support.</span></span>

## <a name="related-topics"></a><span data-ttu-id="19e1f-133">См. также</span><span class="sxs-lookup"><span data-stu-id="19e1f-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="19e1f-134">начало работы с разрешениями WSDAPI</span><span class="sxs-lookup"><span data-stu-id="19e1f-134">Getting Started with WSDAPI Troubleshooting</span></span>](getting-started-with-wsdapi-troubleshooting.md)
</dt> </dl>

 

 



