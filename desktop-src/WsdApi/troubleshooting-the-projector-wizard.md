---
description: Список диагностических процедур, используемых при устранении неполадок мастера проекторов.
ms.assetid: 54efc88c-0b8e-4652-8655-817a288863d1
title: Устранение неполадок мастера проекторов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3776e86d3a156fa86873900aa9e804df9830ec64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692265"
---
# <a name="troubleshooting-the-projector-wizard"></a><span data-ttu-id="22e62-103">Устранение неполадок мастера проекторов</span><span class="sxs-lookup"><span data-stu-id="22e62-103">Troubleshooting the Projector Wizard</span></span>

<span data-ttu-id="22e62-104">Мастер проекторов:</span><span class="sxs-lookup"><span data-stu-id="22e62-104">The Projector Wizard:</span></span>

-   <span data-ttu-id="22e62-105">Всегда использует UDP-WS-Discovery для обнаружения устройств</span><span class="sxs-lookup"><span data-stu-id="22e62-105">Always uses UDP WS-Discovery for device discovery</span></span>
-   <span data-ttu-id="22e62-106">Всегда использует HTTP для обмена метаданными</span><span class="sxs-lookup"><span data-stu-id="22e62-106">Always uses HTTP for metadata exchange</span></span>
-   <span data-ttu-id="22e62-107">Иногда использует направленное обнаружение</span><span class="sxs-lookup"><span data-stu-id="22e62-107">Sometimes uses directed discovery</span></span>

<span data-ttu-id="22e62-108">Следующие процедуры диагностики следует использовать (по порядку) для выявления проблем мастера проекторов.</span><span class="sxs-lookup"><span data-stu-id="22e62-108">The following diagnostic procedures should be used (in order) to help identify problems with the Projector Wizard.</span></span>

<span data-ttu-id="22e62-109">**Устранение неполадок мастера проекторов**</span><span class="sxs-lookup"><span data-stu-id="22e62-109">**To troubleshoot the Projector Wizard**</span></span>

1.  <span data-ttu-id="22e62-110">Если используется направленное обнаружение, [Устранение неполадок с помощью направленного обнаружения](troubleshooting-applications-using-directed-discovery.md).</span><span class="sxs-lookup"><span data-stu-id="22e62-110">If directed discovery is used, [troubleshoot directed discovery](troubleshooting-applications-using-directed-discovery.md).</span></span>
2.  <span data-ttu-id="22e62-111">[Проверьте параметры адаптера и брандмауэра](inspecting-adapter-and-firewall-settings.md).</span><span class="sxs-lookup"><span data-stu-id="22e62-111">[Inspect adapter and firewall settings](inspecting-adapter-and-firewall-settings.md).</span></span>
3.  <span data-ttu-id="22e62-112">[Используйте универсальный узел и клиент для протокола UDP WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md).</span><span class="sxs-lookup"><span data-stu-id="22e62-112">[Use a generic host and client for UDP WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md).</span></span>
4.  <span data-ttu-id="22e62-113">[Используйте клиент отладки WSD для проверки многоадресного трафика](using-wsddebug-client-to-verify-multicast-traffic.md).</span><span class="sxs-lookup"><span data-stu-id="22e62-113">[Use WSD Debug Client to verify multicast traffic](using-wsddebug-client-to-verify-multicast-traffic.md).</span></span>
5.  <span data-ttu-id="22e62-114">[Проверьте сетевые трассировки для протокола UDP WS-Discovery](inspecting-network-traces-for-udp-ws-discovery.md).</span><span class="sxs-lookup"><span data-stu-id="22e62-114">[Inspect network traces for UDP WS-Discovery](inspecting-network-traces-for-udp-ws-discovery.md).</span></span>
6.  <span data-ttu-id="22e62-115">[Используйте универсальный узел и клиент для обмена метаданными HTTP](using-a-generic-host-and-client-for-http-metadata-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="22e62-115">[Use a generic host and client for HTTP metadata exchange](using-a-generic-host-and-client-for-http-metadata-exchange.md).</span></span>
7.  <span data-ttu-id="22e62-116">[Используйте ведение журнала WinHTTP для проверки получения трафика](using-winhttp-logging-to-verify-get-traffic.md).</span><span class="sxs-lookup"><span data-stu-id="22e62-116">[Use WinHTTP logging to verify Get traffic](using-winhttp-logging-to-verify-get-traffic.md).</span></span>
8.  <span data-ttu-id="22e62-117">[Проверьте сетевые трассировки для обмена метаданными HTTP](inspecting-network-traces-for-http-metadata-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="22e62-117">[Inspect network traces for HTTP metadata exchange](inspecting-network-traces-for-http-metadata-exchange.md).</span></span>

<span data-ttu-id="22e62-118">Если источник проблемы не удается определить с помощью описанных выше процедур диагностики, следуйте инструкциям в статьях [Включение трассировки WSDAPI](enabling-wsdapi-tracing.md) и обратитесь в службу поддержки Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="22e62-118">If the source of the problem cannot be identified using the above diagnostic procedures, follow the directions in [Enabling WSDAPI Tracing](enabling-wsdapi-tracing.md) and contact Microsoft support.</span></span>

## <a name="related-topics"></a><span data-ttu-id="22e62-119">См. также</span><span class="sxs-lookup"><span data-stu-id="22e62-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="22e62-120">начало работы с разрешениями WSDAPI</span><span class="sxs-lookup"><span data-stu-id="22e62-120">Getting Started with WSDAPI Troubleshooting</span></span>](getting-started-with-wsdapi-troubleshooting.md)
</dt> </dl>

 

 



