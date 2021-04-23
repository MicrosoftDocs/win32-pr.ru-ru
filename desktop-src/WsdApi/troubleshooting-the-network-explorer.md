---
description: Список диагностических процедур, используемых при устранении неполадок в сетевом обозревателе.
ms.assetid: 56052a82-d3a6-4749-9010-6796558dcb17
title: Устранение неполадок обозревателя сети
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09afe7acbcb20d706c8645d84c68014b0e33d799
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991106"
---
# <a name="troubleshooting-the-network-explorer"></a><span data-ttu-id="b459f-103">Устранение неполадок обозревателя сети</span><span class="sxs-lookup"><span data-stu-id="b459f-103">Troubleshooting the Network Explorer</span></span>

<span data-ttu-id="b459f-104">Обозреватель сети:</span><span class="sxs-lookup"><span data-stu-id="b459f-104">The Network Explorer:</span></span>

-   <span data-ttu-id="b459f-105">Всегда использует UDP-WS-Discovery для обнаружения устройств</span><span class="sxs-lookup"><span data-stu-id="b459f-105">Always uses UDP WS-Discovery for device discovery</span></span>
-   <span data-ttu-id="b459f-106">Всегда инициирует подключение HTTP или HTTPS для обмена метаданными</span><span class="sxs-lookup"><span data-stu-id="b459f-106">Always initiates a HTTP or HTTPS connection for metadata exchange</span></span>
-   <span data-ttu-id="b459f-107">Иногда использует безопасный канал (HTTPS) для обмена метаданными</span><span class="sxs-lookup"><span data-stu-id="b459f-107">Sometimes uses a secure channel (HTTPS) for metadata exchange</span></span>

<span data-ttu-id="b459f-108">Следующие процедуры диагностики следует использовать (по порядку) для выявления проблем в сетевом обозревателе.</span><span class="sxs-lookup"><span data-stu-id="b459f-108">The following diagnostic procedures should be used (in order) to help identify problems with the Network Explorer.</span></span>

<span data-ttu-id="b459f-109">**Устранение неполадок обозревателя сети**</span><span class="sxs-lookup"><span data-stu-id="b459f-109">**To troubleshoot the Network Explorer**</span></span>

1.  <span data-ttu-id="b459f-110">[Проверьте параметры адаптера и брандмауэра](inspecting-adapter-and-firewall-settings.md).</span><span class="sxs-lookup"><span data-stu-id="b459f-110">[Inspect adapter and firewall settings](inspecting-adapter-and-firewall-settings.md).</span></span>
2.  <span data-ttu-id="b459f-111">[Используйте универсальный узел и клиент для протокола UDP WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md).</span><span class="sxs-lookup"><span data-stu-id="b459f-111">[Use a generic host and client for UDP WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md).</span></span>
3.  <span data-ttu-id="b459f-112">[Используйте клиент отладки WSD для проверки многоадресного трафика](using-wsddebug-client-to-verify-multicast-traffic.md).</span><span class="sxs-lookup"><span data-stu-id="b459f-112">[Use WSD Debug Client to verify multicast traffic](using-wsddebug-client-to-verify-multicast-traffic.md).</span></span>
4.  <span data-ttu-id="b459f-113">[Проверьте сетевые трассировки для протокола UDP WS-Discovery](inspecting-network-traces-for-udp-ws-discovery.md).</span><span class="sxs-lookup"><span data-stu-id="b459f-113">[Inspect network traces for UDP WS-Discovery](inspecting-network-traces-for-udp-ws-discovery.md).</span></span>
5.  <span data-ttu-id="b459f-114">[Используйте универсальный узел и клиент для обмена метаданными HTTP](using-a-generic-host-and-client-for-http-metadata-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="b459f-114">[Use a generic host and client for HTTP metadata exchange](using-a-generic-host-and-client-for-http-metadata-exchange.md).</span></span>
6.  <span data-ttu-id="b459f-115">[Используйте ведение журнала WinHTTP для проверки получения трафика](using-winhttp-logging-to-verify-get-traffic.md).</span><span class="sxs-lookup"><span data-stu-id="b459f-115">[Use WinHTTP logging to verify Get traffic](using-winhttp-logging-to-verify-get-traffic.md).</span></span>
7.  <span data-ttu-id="b459f-116">[Проверьте сетевые трассировки для обмена метаданными HTTP](inspecting-network-traces-for-http-metadata-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="b459f-116">[Inspect network traces for HTTP metadata exchange](inspecting-network-traces-for-http-metadata-exchange.md).</span></span>

<span data-ttu-id="b459f-117">Сетевой обозреватель использует [обнаружение функций](/previous-versions/windows/desktop/fundisc/fd-portal) для перечисления сетевых устройств.</span><span class="sxs-lookup"><span data-stu-id="b459f-117">The Network Explorer uses [Function Discovery](/previous-versions/windows/desktop/fundisc/fd-portal) to enumerate network devices.</span></span> <span data-ttu-id="b459f-118">Дополнительные сведения об устранении неполадок см. в разделе [Устранение неполадок клиентов обнаружения функций](troubleshooting-function-discovery-clients.md).</span><span class="sxs-lookup"><span data-stu-id="b459f-118">For more troubleshooting information, see [Troubleshooting Function Discovery Clients](troubleshooting-function-discovery-clients.md).</span></span>

<span data-ttu-id="b459f-119">Если источник проблемы не удается определить с помощью описанных выше процедур диагностики, следуйте инструкциям в статьях [Включение трассировки WSDAPI](enabling-wsdapi-tracing.md) и обратитесь в службу поддержки Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="b459f-119">If the source of the problem cannot be identified using the above diagnostic procedures, follow the directions in [Enabling WSDAPI Tracing](enabling-wsdapi-tracing.md) and contact Microsoft support.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b459f-120">См. также</span><span class="sxs-lookup"><span data-stu-id="b459f-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b459f-121">начало работы с разрешениями WSDAPI</span><span class="sxs-lookup"><span data-stu-id="b459f-121">Getting Started with WSDAPI Troubleshooting</span></span>](getting-started-with-wsdapi-troubleshooting.md)
</dt> <dt>

[<span data-ttu-id="b459f-122">Устранение неполадок клиентов обнаружения функций</span><span class="sxs-lookup"><span data-stu-id="b459f-122">Troubleshooting Function Discovery Clients</span></span>](troubleshooting-function-discovery-clients.md)
</dt> </dl>

 

 
