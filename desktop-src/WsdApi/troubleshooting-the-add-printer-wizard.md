---
description: Список диагностических процедур, используемых при устранении неполадок мастера добавления принтера.
ms.assetid: 3ffee09b-e980-4a14-97ad-270444457dd7
title: Устранение неполадок мастера добавления принтера
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3b0054758e3ec721598ad279a073a32862af368
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692804"
---
# <a name="troubleshooting-the-add-printer-wizard"></a><span data-ttu-id="c7b27-103">Устранение неполадок мастера добавления принтера</span><span class="sxs-lookup"><span data-stu-id="c7b27-103">Troubleshooting the Add Printer Wizard</span></span>

<span data-ttu-id="c7b27-104">Мастер добавления принтера:</span><span class="sxs-lookup"><span data-stu-id="c7b27-104">The Add Printer Wizard:</span></span>

-   <span data-ttu-id="c7b27-105">Всегда использует UDP-WS-Discovery для обнаружения устройств</span><span class="sxs-lookup"><span data-stu-id="c7b27-105">Always uses UDP WS-Discovery for device discovery</span></span>
-   <span data-ttu-id="c7b27-106">Всегда инициирует подключение HTTP или HTTPS для обмена метаданными</span><span class="sxs-lookup"><span data-stu-id="c7b27-106">Always initiates a HTTP or HTTPS connection for metadata exchange</span></span>
-   <span data-ttu-id="c7b27-107">Иногда использует направленное обнаружение</span><span class="sxs-lookup"><span data-stu-id="c7b27-107">Sometimes uses directed discovery</span></span>
-   <span data-ttu-id="c7b27-108">Иногда использует безопасный канал (HTTPS) для обмена метаданными</span><span class="sxs-lookup"><span data-stu-id="c7b27-108">Sometimes uses a secure channel (HTTPS) for metadata exchange</span></span>

<span data-ttu-id="c7b27-109">Следующие процедуры диагностики следует использовать (по порядку) для выявления проблем с мастером добавления принтера.</span><span class="sxs-lookup"><span data-stu-id="c7b27-109">The following diagnostic procedures should be used (in order) to help identify problems with the Add Printer Wizard.</span></span>

<span data-ttu-id="c7b27-110">**Устранение неполадок мастера добавления принтера**</span><span class="sxs-lookup"><span data-stu-id="c7b27-110">**To troubleshoot the Add Printer Wizard**</span></span>

1.  <span data-ttu-id="c7b27-111">Если используется направленное обнаружение, [Устранение неполадок с помощью направленного обнаружения](troubleshooting-applications-using-directed-discovery.md).</span><span class="sxs-lookup"><span data-stu-id="c7b27-111">If directed discovery is used, [troubleshoot directed discovery](troubleshooting-applications-using-directed-discovery.md).</span></span>
2.  <span data-ttu-id="c7b27-112">[Проверьте параметры адаптера и брандмауэра](inspecting-adapter-and-firewall-settings.md).</span><span class="sxs-lookup"><span data-stu-id="c7b27-112">[Inspect adapter and firewall settings](inspecting-adapter-and-firewall-settings.md).</span></span>
3.  <span data-ttu-id="c7b27-113">[Используйте универсальный узел и клиент для протокола UDP WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md).</span><span class="sxs-lookup"><span data-stu-id="c7b27-113">[Use a generic host and client for UDP WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md).</span></span>
4.  <span data-ttu-id="c7b27-114">[Используйте клиент отладки WSD для проверки многоадресного трафика](using-wsddebug-client-to-verify-multicast-traffic.md).</span><span class="sxs-lookup"><span data-stu-id="c7b27-114">[Use WSD Debug Client to verify multicast traffic](using-wsddebug-client-to-verify-multicast-traffic.md).</span></span>
5.  <span data-ttu-id="c7b27-115">[Проверьте сетевые трассировки для протокола UDP WS-Discovery](inspecting-network-traces-for-udp-ws-discovery.md).</span><span class="sxs-lookup"><span data-stu-id="c7b27-115">[Inspect network traces for UDP WS-Discovery](inspecting-network-traces-for-udp-ws-discovery.md).</span></span>
6.  <span data-ttu-id="c7b27-116">[Используйте универсальный узел и клиент для обмена метаданными HTTP](using-a-generic-host-and-client-for-http-metadata-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="c7b27-116">[Use a generic host and client for HTTP metadata exchange](using-a-generic-host-and-client-for-http-metadata-exchange.md).</span></span>
7.  <span data-ttu-id="c7b27-117">[Используйте ведение журнала WinHTTP для проверки получения трафика](using-winhttp-logging-to-verify-get-traffic.md).</span><span class="sxs-lookup"><span data-stu-id="c7b27-117">[Use WinHTTP logging to verify Get traffic](using-winhttp-logging-to-verify-get-traffic.md).</span></span>
8.  <span data-ttu-id="c7b27-118">[Проверьте сетевые трассировки для обмена метаданными HTTP](inspecting-network-traces-for-http-metadata-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="c7b27-118">[Inspect network traces for HTTP metadata exchange](inspecting-network-traces-for-http-metadata-exchange.md).</span></span>

<span data-ttu-id="c7b27-119">Если источник проблемы не удается определить с помощью описанных выше процедур диагностики, следуйте инструкциям в статьях [Включение трассировки WSDAPI](enabling-wsdapi-tracing.md) и обратитесь в службу поддержки Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="c7b27-119">If the source of the problem cannot be identified using the above diagnostic procedures, follow the directions in [Enabling WSDAPI Tracing](enabling-wsdapi-tracing.md) and contact Microsoft support.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c7b27-120">См. также</span><span class="sxs-lookup"><span data-stu-id="c7b27-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c7b27-121">начало работы с разрешениями WSDAPI</span><span class="sxs-lookup"><span data-stu-id="c7b27-121">Getting Started with WSDAPI Troubleshooting</span></span>](getting-started-with-wsdapi-troubleshooting.md)
</dt> <dt>

[<span data-ttu-id="c7b27-122">Устранение неполадок в приложениях с помощью направленного обнаружения</span><span class="sxs-lookup"><span data-stu-id="c7b27-122">Troubleshooting Applications Using Directed Discovery</span></span>](troubleshooting-applications-using-directed-discovery.md)
</dt> </dl>

 

 



