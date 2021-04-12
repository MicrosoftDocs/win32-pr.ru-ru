---
description: Набор инструментов отладки, созданный на основе API веб-служб на устройствах (WSDAPI), доступен в Windows SDK и в комплекте драйверов для Windows (WDK).
ms.assetid: bd7efa8b-4f12-4b19-a7df-fa34c6a3444a
title: Инструменты отладки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29965bb85ccfd2daf00612b09bb013ae170dddcd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104156670"
---
# <a name="debugging-tools"></a><span data-ttu-id="46c49-103">Инструменты отладки</span><span class="sxs-lookup"><span data-stu-id="46c49-103">Debugging Tools</span></span>

<span data-ttu-id="46c49-104">Набор инструментов отладки, созданный на основе API веб-служб на устройствах (WSDAPI), доступен в Windows SDK и в комплекте драйверов для Windows (WDK).</span><span class="sxs-lookup"><span data-stu-id="46c49-104">A debugging toolset built on Web Services on Devices API (WSDAPI) is available in the Windows SDK and the Windows Driver Kit (WDK).</span></span> <span data-ttu-id="46c49-105">Эти средства можно использовать для проверки функциональных возможностей пользовательских приложений, написанных на WSDAPI, а также устройств и клиентов, написанных с помощью другого профиля устройства для стеков веб-служб (DPWS).</span><span class="sxs-lookup"><span data-stu-id="46c49-105">These tools can be used to test the functionality of custom applications written on WSDAPI, or devices and clients written using other Device Profile for Web Services (DPWS) stacks.</span></span>

<span data-ttu-id="46c49-106">Средства отладки (всддебуг \_host.exe) и клиент отладки WSD (всддебуг \_client.exe) можно использовать для проверки характеристик клиентов или узлов DPWS.</span><span class="sxs-lookup"><span data-stu-id="46c49-106">The WSD Debug Host (wsddebug\_host.exe) and WSD Debug Client (wsddebug\_client.exe) tools can be used to inspect the characteristics of DPWS clients or hosts.</span></span> <span data-ttu-id="46c49-107">Их также можно использовать для устранения проблем с подключением или конфигурацией.</span><span class="sxs-lookup"><span data-stu-id="46c49-107">They can also be used to troubleshoot connectivity or configuration problems.</span></span> <span data-ttu-id="46c49-108">Дополнительные сведения см. в разделе [руководство по устранению неполадок WSDAPI](wsdapi-troubleshooting-guide.md).</span><span class="sxs-lookup"><span data-stu-id="46c49-108">For more information, see [WSDAPI Troubleshooting Guide](wsdapi-troubleshooting-guide.md).</span></span> <span data-ttu-id="46c49-109">Эти средства доступны только в пакете SDK.</span><span class="sxs-lookup"><span data-stu-id="46c49-109">These tools are only available in the SDK.</span></span> <span data-ttu-id="46c49-110">Средства пакета SDK находятся в следующем каталоге: <Windows SDK Install Folder> \\ bin.</span><span class="sxs-lookup"><span data-stu-id="46c49-110">SDK tools are located in the following directory: <Windows SDK Install Folder>\\Bin.</span></span>

<span data-ttu-id="46c49-111">[Средство взаимодействия с базовым взаимодействием (всдбит) WSDAPI](https://msdn.microsoft.com/library/cc264250.aspx) можно использовать для проверки взаимодействия на уровне протокола SOAP или транспортного уровня (то есть обеспечить правильный формат сообщений).</span><span class="sxs-lookup"><span data-stu-id="46c49-111">The [WSDAPI Basic Interoperability Tool (WSDBIT)](https://msdn.microsoft.com/library/cc264250.aspx) can be used to test SOAP-level or transport-level interoperability (that is, ensuring messages are well-formed).</span></span> <span data-ttu-id="46c49-112">Это средство доступно только в WDK.</span><span class="sxs-lookup"><span data-stu-id="46c49-112">This tool is only available in the WDK.</span></span>

## <a name="the-wsd-debug-client"></a><span data-ttu-id="46c49-113">Клиент отладки WSD</span><span class="sxs-lookup"><span data-stu-id="46c49-113">The WSD Debug Client</span></span>

<span data-ttu-id="46c49-114">Клиент отладки WSD (всддебуг \_client.exe) предоставляет интерактивную консоль, которую можно использовать для отправки и получения сообщений WS-Discovery и для получения метаданных.</span><span class="sxs-lookup"><span data-stu-id="46c49-114">The WSD Debug Client (wsddebug\_client.exe) provides an interactive console that can be used to send and receive WS-Discovery messages, and to obtain metadata.</span></span> <span data-ttu-id="46c49-115">Его также можно использовать для создания и использования необработанных многоадресных сообщений.</span><span class="sxs-lookup"><span data-stu-id="46c49-115">It can also be used to generate and consume raw multicast messages.</span></span>

<span data-ttu-id="46c49-116">Клиент отладки WSD работает в одном из трех режимов: многоадресность, обнаружение и метаданные.</span><span class="sxs-lookup"><span data-stu-id="46c49-116">The WSD Debug Client operates in one of three modes: multicast, discovery, and metadata.</span></span>



| <span data-ttu-id="46c49-117">Режим</span><span class="sxs-lookup"><span data-stu-id="46c49-117">Mode</span></span>      | <span data-ttu-id="46c49-118">Описание</span><span class="sxs-lookup"><span data-stu-id="46c49-118">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                          |
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46c49-119">Многоадресная рассылка</span><span class="sxs-lookup"><span data-stu-id="46c49-119">Multicast</span></span> | <span data-ttu-id="46c49-120">В режиме многоадресной рассылки клиент отладки WSD отправляет и получает неформатированные многоадресные сообщения через UDP-порт 3702, как определено в WS.</span><span class="sxs-lookup"><span data-stu-id="46c49-120">In Multicast mode, the WSD Debug Client sends and receives unformatted multicast messages on UDP port 3702, as defined in WS-Discovery.</span></span> <span data-ttu-id="46c49-121">Пользователь может сохранить эти сообщения SOAP в текстовом файле и может изменять и пересылать сообщения с помощью клиента отладки WSD.</span><span class="sxs-lookup"><span data-stu-id="46c49-121">The user may save these SOAP messages in a text file, and may modify and rebroadcast the messages with the WSD Debug Client.</span></span>                                                                                                                                 |
| <span data-ttu-id="46c49-122">Обнаружение</span><span class="sxs-lookup"><span data-stu-id="46c49-122">Discovery</span></span> | <span data-ttu-id="46c49-123">В режиме обнаружения клиент отладки WSD отправляет и получает отформатированные сообщения WS-Discovery.</span><span class="sxs-lookup"><span data-stu-id="46c49-123">In Discovery mode, the WSD Debug Client sends and receives formatted WS-Discovery messages.</span></span> <span data-ttu-id="46c49-124">Он может отображать полученные сообщения [Hello](hello-message.md), [Bye](bye-message.md), [ProbeMatch](probematches-message.md)и [ресолвематчес](resolvematches-message.md) .</span><span class="sxs-lookup"><span data-stu-id="46c49-124">It can display received [Hello](hello-message.md), [Bye](bye-message.md), [ProbeMatches](probematches-message.md), and [ResolveMatches](resolvematches-message.md) messages.</span></span> <span data-ttu-id="46c49-125">Он может передавать сообщения [проб](probe-message.md) по протоколу UDP или HTTP, а также [разрешать](resolve-message.md) сообщения по протоколу UDP.</span><span class="sxs-lookup"><span data-stu-id="46c49-125">It can send [Probe](probe-message.md) messages over UDP or HTTP, and [Resolve](resolve-message.md) messages over UDP.</span></span> |
| <span data-ttu-id="46c49-126">Метаданные</span><span class="sxs-lookup"><span data-stu-id="46c49-126">Metadata</span></span>  | <span data-ttu-id="46c49-127">Помимо реализации всех функций режима обнаружения, режим метаданных также пытается получить метаданные с устройств.</span><span class="sxs-lookup"><span data-stu-id="46c49-127">In addition to implementing all of the features of Discovery mode, Metadata mode also attempts to retrieve metadata from devices.</span></span>                                                                                                                                                                                                                                                                    |



 

<span data-ttu-id="46c49-128">Дополнительные сведения см. в статьях [Использование универсального узла и клиента для обмена метаданными HTTP](using-a-generic-host-and-client-for-http-metadata-exchange.md), [Использование универсального узла и клиента для протокола UDP WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md)и [Использование клиента отладки WSD для проверки многоадресного трафика](using-wsddebug-client-to-verify-multicast-traffic.md).</span><span class="sxs-lookup"><span data-stu-id="46c49-128">For more information, see [Using a Generic Host and Client for HTTP Metadata Exchange](using-a-generic-host-and-client-for-http-metadata-exchange.md), [Using a Generic Host and Client for UDP WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md), and [Using WSD Debug Client to Verify Multicast Traffic](using-wsddebug-client-to-verify-multicast-traffic.md).</span></span>

## <a name="the-wsd-debug-host"></a><span data-ttu-id="46c49-129">Узел отладки WSD</span><span class="sxs-lookup"><span data-stu-id="46c49-129">The WSD Debug Host</span></span>

<span data-ttu-id="46c49-130">Узел отладки WSD (всддебуг \_host.exe) предоставляет интерактивную консоль, используемую для объявления узла, реагирования на запросы клиентов и печати диагностической информации.</span><span class="sxs-lookup"><span data-stu-id="46c49-130">The WSD Debug Host (wsddebug\_host.exe) provides an interactive console used to announce the host, respond to client requests, and print diagnostic information.</span></span>

<span data-ttu-id="46c49-131">Узел отладки WSD работает в одном из двух режимов: обнаружение и метаданные.</span><span class="sxs-lookup"><span data-stu-id="46c49-131">The WSD Debug Host operates in one of two modes: discovery and metadata.</span></span>



| <span data-ttu-id="46c49-132">Режим</span><span class="sxs-lookup"><span data-stu-id="46c49-132">Mode</span></span>      | <span data-ttu-id="46c49-133">Описание</span><span class="sxs-lookup"><span data-stu-id="46c49-133">Description</span></span>                                                                                                                                                                                                                                                       |
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46c49-134">Обнаружение</span><span class="sxs-lookup"><span data-stu-id="46c49-134">Discovery</span></span> | <span data-ttu-id="46c49-135">В режиме обнаружения узел отладки WSD выводит форматированные сообщения WS-Discovery.</span><span class="sxs-lookup"><span data-stu-id="46c49-135">In Discovery mode, the WSD Debug Host prints formatted WS-Discovery messages.</span></span> <span data-ttu-id="46c49-136">Он также отправляет сообщения [Hello](hello-message.md) и [Bye](bye-message.md) и автоматически реагирует на [проверку](probe-message.md) и [разрешение](resolve-message.md) сообщений.</span><span class="sxs-lookup"><span data-stu-id="46c49-136">It also sends [Hello](hello-message.md) and [Bye](bye-message.md) messages, and automatically responds to [Probe](probe-message.md) and [Resolve](resolve-message.md) messages.</span></span> |
| <span data-ttu-id="46c49-137">Метаданные</span><span class="sxs-lookup"><span data-stu-id="46c49-137">Metadata</span></span>  | <span data-ttu-id="46c49-138">Помимо реализации всех функций режима обнаружения, режим метаданных объявляет службу метаданных и позволяет клиентам подключаться и выполнять обмен метаданными.</span><span class="sxs-lookup"><span data-stu-id="46c49-138">In addition to implementing all of the features of Discovery mode, Metadata mode advertises a metadata service and allows clients to connect and perform metadata exchange.</span></span>                                                                                       |



 

<span data-ttu-id="46c49-139">Дополнительные сведения см. в статьях [Использование универсального узла и клиента для обмена метаданными HTTP](using-a-generic-host-and-client-for-http-metadata-exchange.md) и [Использование универсального узла и клиента для протокола UDP WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md).</span><span class="sxs-lookup"><span data-stu-id="46c49-139">For more information, see [Using a Generic Host and Client for HTTP Metadata Exchange](using-a-generic-host-and-client-for-http-metadata-exchange.md) and [Using a Generic Host and Client for UDP WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="46c49-140">См. также</span><span class="sxs-lookup"><span data-stu-id="46c49-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="46c49-141">Разработка приложений WSD в Windows</span><span class="sxs-lookup"><span data-stu-id="46c49-141">WSD Application Development on Windows</span></span>](wsd-application-development-on-windows.md)
</dt> <dt>

[<span data-ttu-id="46c49-142">Средства разработки WSDAPI</span><span class="sxs-lookup"><span data-stu-id="46c49-142">WSDAPI Development Tools</span></span>](wsdapi-development-tools.md)
</dt> <dt>

[<span data-ttu-id="46c49-143">Руководство по устранению неполадок WSDAPI</span><span class="sxs-lookup"><span data-stu-id="46c49-143">WSDAPI Troubleshooting Guide</span></span>](wsdapi-troubleshooting-guide.md)
</dt> </dl>

 

 



