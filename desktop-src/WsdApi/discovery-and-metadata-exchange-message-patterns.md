---
description: Профиль устройства для узлов и клиентов веб-служб (DPWS) взаимодействует по сети, используя серию сообщений SOAP по протоколам UDP и HTTP.
ms.assetid: 52282990-d993-4034-a791-2ee7c9c1663d
title: Шаблоны сообщений обнаружения и обмена метаданными
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e9a08852c5f25572daf9932afd2ce4b7e03858a
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/12/2021
ms.locfileid: "104273216"
---
# <a name="discovery-and-metadata-exchange-message-patterns"></a><span data-ttu-id="91592-103">Шаблоны сообщений обнаружения и обмена метаданными</span><span class="sxs-lookup"><span data-stu-id="91592-103">Discovery and Metadata Exchange Message Patterns</span></span>

<span data-ttu-id="91592-104">Профиль устройства для узлов и клиентов веб-служб (DPWS) взаимодействует по сети, используя серию сообщений SOAP по протоколам UDP и HTTP.</span><span class="sxs-lookup"><span data-stu-id="91592-104">Device Profile for Web Services (DPWS) hosts and clients communicate over the network using a series of SOAP messages over UDP and HTTP.</span></span>

<span data-ttu-id="91592-105">На следующей диаграмме представлен обзор ожидаемого трафика UDP и HTTP между узлом DPWS и клиентом.</span><span class="sxs-lookup"><span data-stu-id="91592-105">The following diagram shows an overview of the expected UDP and HTTP traffic between a DPWS host and client.</span></span>

![Схема трафика UDP и HTTP между узлом DPWS и клиентом.](images/ws-discovery-and-metadata-exchange-message-patterns.png)

<span data-ttu-id="91592-107">Сообщения [Hello](hello-message.md), [Bye](bye-message.md), [зонд](probe-message.md), [Resolve](resolve-message.md)и [Get](get--metadata-exchange--http-request-and-message.md) создаются без запроса сети. Эти сообщения используются для объявления состояния устройства или для выдаче запроса на поиск.</span><span class="sxs-lookup"><span data-stu-id="91592-107">[Hello](hello-message.md), [Bye](bye-message.md), [Probe](probe-message.md), [Resolve](resolve-message.md), and [Get](get--metadata-exchange--http-request-and-message.md) messages are all generated without network solicitation; these messages are used to announce device state or to issue a search request.</span></span> <span data-ttu-id="91592-108">Сообщения [ProbeMatch](probematches-message.md), [ресолвематчес](resolvematches-message.md)и [GetResponse](getresponse--metadata-exchange--message.md) создаются в ответ на проверку, разрешение и получение сообщений.</span><span class="sxs-lookup"><span data-stu-id="91592-108">[ProbeMatches](probematches-message.md), [ResolveMatches](resolvematches-message.md), and [GetResponse](getresponse--metadata-exchange--message.md) messages are generated in response to Probe, Resolve and Get messages.</span></span>

<span data-ttu-id="91592-109">Сообщения [Hello](hello-message.md), [Bye](bye-message.md), [Resolve](resolve-message.md)и [ресолвематчес](resolvematches-message.md) всегда будут выполняться по протоколу UDP.</span><span class="sxs-lookup"><span data-stu-id="91592-109">[Hello](hello-message.md), [Bye](bye-message.md), [Resolve](resolve-message.md), and [ResolveMatches](resolvematches-message.md) messages will always occur over UDP.</span></span> <span data-ttu-id="91592-110">Аналогичным образом, сообщения метаданных [Get](get--metadata-exchange--http-request-and-message.md) и [GetResponse](getresponse--metadata-exchange--message.md) всегда будут выполняться по протоколам HTTP или HTTPS.</span><span class="sxs-lookup"><span data-stu-id="91592-110">Similarly, [Get](get--metadata-exchange--http-request-and-message.md) and [GetResponse](getresponse--metadata-exchange--message.md) metadata messages will always occur over HTTP or HTTPS.</span></span> <span data-ttu-id="91592-111">Сообщения [проверки](probe-message.md) и [ProbeMatch](probematches-message.md) обычно передаются по протоколу UDP, но выполняются по протоколу HTTP или HTTPS в сценарии направленного обнаружения.</span><span class="sxs-lookup"><span data-stu-id="91592-111">[Probe](probe-message.md) and [ProbeMatches](probematches-message.md) messages are normally transmitted over UDP, but take place over an HTTP or HTTPS connection in a directed discovery scenario.</span></span> <span data-ttu-id="91592-112">Дополнительные сведения о направленных шаблонах сообщений обнаружения см. в разделе [Устранение неполадок приложений с помощью](troubleshooting-applications-using-directed-discovery.md)управляемого обнаружения.</span><span class="sxs-lookup"><span data-stu-id="91592-112">For more information about directed discovery message patterns, see [Troubleshooting Applications Using Directed Discovery](troubleshooting-applications-using-directed-discovery.md).</span></span>

<span data-ttu-id="91592-113">В следующем списке показана типичная последовательность сообщений, отправляемых по сети.</span><span class="sxs-lookup"><span data-stu-id="91592-113">The following list shows the typical sequence of messages on the wire.</span></span> <span data-ttu-id="91592-114">Не все сообщения являются обязательными.</span><span class="sxs-lookup"><span data-stu-id="91592-114">Not all messages are mandatory.</span></span>

1.  [<span data-ttu-id="91592-115">Привет</span><span class="sxs-lookup"><span data-stu-id="91592-115">Hello</span></span>](hello-message.md)
2.  [<span data-ttu-id="91592-116">Проба</span><span class="sxs-lookup"><span data-stu-id="91592-116">Probe</span></span>](probe-message.md)
3.  [<span data-ttu-id="91592-117">ProbeMatch</span><span class="sxs-lookup"><span data-stu-id="91592-117">ProbeMatches</span></span>](probematches-message.md)
4.  [<span data-ttu-id="91592-118">Разрешить</span><span class="sxs-lookup"><span data-stu-id="91592-118">Resolve</span></span>](resolve-message.md)
5.  [<span data-ttu-id="91592-119">ресолвематчес</span><span class="sxs-lookup"><span data-stu-id="91592-119">ResolveMatches</span></span>](resolvematches-message.md)
6.  <span data-ttu-id="91592-120">[Get](get--metadata-exchange--http-request-and-message.md) (запрос на обмен метаданными)</span><span class="sxs-lookup"><span data-stu-id="91592-120">[Get](get--metadata-exchange--http-request-and-message.md) (metadata exchange request)</span></span>
7.  [<span data-ttu-id="91592-121">GetResponse</span><span class="sxs-lookup"><span data-stu-id="91592-121">GetResponse</span></span>](getresponse--metadata-exchange--message.md)
8.  [<span data-ttu-id="91592-122">Пока</span><span class="sxs-lookup"><span data-stu-id="91592-122">Bye</span></span>](bye-message.md)

## <a name="related-topics"></a><span data-ttu-id="91592-123">См. также</span><span class="sxs-lookup"><span data-stu-id="91592-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="91592-124">О веб-службах на устройствах</span><span class="sxs-lookup"><span data-stu-id="91592-124">About Web Services on Devices</span></span>](about-web-services-for-devices.md)
</dt> </dl>

 

 



