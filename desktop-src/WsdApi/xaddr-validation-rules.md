---
description: Адреса транспорта (Ксаддрс), входящие в сообщения ProbeMatch и Ресолвематчес, подчиняются базовой проверке перед тем, как WSDAPI отправляет HTTP-сообщение, например запрос метаданных.
ms.assetid: 6b5139b5-aa31-42bc-a281-8784006edfbe
title: Правила проверки Ксаддр
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc91ce8a0e1bba267ea92fa79a6680b481297f24
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263782"
---
# <a name="xaddr-validation-rules"></a><span data-ttu-id="34bce-103">Правила проверки Ксаддр</span><span class="sxs-lookup"><span data-stu-id="34bce-103">XAddr Validation Rules</span></span>

<span data-ttu-id="34bce-104">Адреса транспорта (Ксаддрс), входящие в сообщения [ProbeMatch](probematches-message.md) и [ресолвематчес](resolvematches-message.md) , подчиняются базовой проверке перед тем, как WSDAPI отправляет HTTP-сообщение, например запрос метаданных.</span><span class="sxs-lookup"><span data-stu-id="34bce-104">Transport addresses (XAddrs) included in [ProbeMatches](probematches-message.md) and [ResolveMatches](resolvematches-message.md) messages are subject to basic validation before WSDAPI sends an HTTP message, such as a metadata request.</span></span>

<span data-ttu-id="34bce-105">Это позволяет убедиться, что Ксаддрс находятся в той же подсети, что и клиент.</span><span class="sxs-lookup"><span data-stu-id="34bce-105">This is in order to ensure that the XAddrs are on the same subnet as the client.</span></span>

<span data-ttu-id="34bce-106">В следующем коде XML показан пример элемента Ксаддрс.</span><span class="sxs-lookup"><span data-stu-id="34bce-106">The following XML shows a sample XAddrs element.</span></span> <span data-ttu-id="34bce-107">Префикс WSD ссылается на пространство имен `https://schemas.xmlsoap.org/ws/2005/04/discovery` .</span><span class="sxs-lookup"><span data-stu-id="34bce-107">The wsd prefix refers to the namespace `https://schemas.xmlsoap.org/ws/2005/04/discovery`.</span></span>

``` syntax
<wsd:XAddrs>
    https://192.168.0.2:5357/37f86d35-e6ac-4241-964f-1d9ae46fb366
</wsd:XAddrs>
```

<span data-ttu-id="34bce-108">Прежде чем HTTP-сообщение будет отправлено по сети, необходимо выполнить все следующие условия.</span><span class="sxs-lookup"><span data-stu-id="34bce-108">All of the following conditions must be met before the HTTP message will go out over the wire.</span></span>

-   <span data-ttu-id="34bce-109">Ксаддрс должны быть адресами HTTP или HTTPS.</span><span class="sxs-lookup"><span data-stu-id="34bce-109">XAddrs must be HTTP or HTTPS addresses.</span></span> <span data-ttu-id="34bce-110">Ксаддрс других схем игнорируются.</span><span class="sxs-lookup"><span data-stu-id="34bce-110">XAddrs of other schemes are ignored.</span></span>
-   <span data-ttu-id="34bce-111">Если имеются любые Ксаддрс HTTPS, все Ксаддрс должны быть HTTPS.</span><span class="sxs-lookup"><span data-stu-id="34bce-111">If any HTTPS XAddrs are present, all XAddrs must be HTTPS.</span></span> <span data-ttu-id="34bce-112">Разделы Ксаддр, которые содержат адреса HTTP и HTTPS, полностью игнорируются.</span><span class="sxs-lookup"><span data-stu-id="34bce-112">XAddr sections which include both HTTP and HTTPS addresses are completely ignored.</span></span> <span data-ttu-id="34bce-113">Кроме того, адрес конечной точки устройства должен точно соответствовать Ксаддрс HTTPS.</span><span class="sxs-lookup"><span data-stu-id="34bce-113">Additionally, the device's endpoint address must match the HTTPS XAddrs exactly.</span></span>
-   <span data-ttu-id="34bce-114">Ксаддрс должны представлять собой IP-адреса или имена узлов, разрешаемые с помощью DNS.</span><span class="sxs-lookup"><span data-stu-id="34bce-114">XAddrs must be IP addresses or hostnames resolvable through DNS.</span></span> <span data-ttu-id="34bce-115">Обычно используются IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="34bce-115">Usually, IP addresses are used.</span></span>
-   <span data-ttu-id="34bce-116">По крайней мере один IP-адрес, включенный в Ксаддрс (или IP-адрес, разрешенный с имени узла, включенного в Ксаддрс), должен находиться в той же подсети, что и адаптер, по которому было получено сообщение [ProbeMatch](probematches-message.md) или [ресолвематчес](resolvematches-message.md) .</span><span class="sxs-lookup"><span data-stu-id="34bce-116">At least one IP address included in the XAddrs (or IP address resolved from a hostname included in the XAddrs) must be on the same subnet as the adapter over which the [ProbeMatches](probematches-message.md) or [ResolveMatches](resolvematches-message.md) message was received.</span></span>
-   <span data-ttu-id="34bce-117">Адрес и порт, указанные в первом Ксаддр, должны быть доступны.</span><span class="sxs-lookup"><span data-stu-id="34bce-117">The address and port specified in the first XAddr must be accessible.</span></span> <span data-ttu-id="34bce-118">WSDAPI пытается подключиться к этому адресу при установлении HTTP-соединения.</span><span class="sxs-lookup"><span data-stu-id="34bce-118">WSDAPI attempts to connect to this address when establishing an HTTP connection.</span></span>

## <a name="related-topics"></a><span data-ttu-id="34bce-119">См. также</span><span class="sxs-lookup"><span data-stu-id="34bce-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="34bce-120">ProbeMatch</span><span class="sxs-lookup"><span data-stu-id="34bce-120">ProbeMatches</span></span>](probematches-message.md)
</dt> <dt>

[<span data-ttu-id="34bce-121">ресолвематчес</span><span class="sxs-lookup"><span data-stu-id="34bce-121">ResolveMatches</span></span>](resolvematches-message.md)
</dt> <dt>

[<span data-ttu-id="34bce-122">Шаблоны сообщений обнаружения и обмена метаданными</span><span class="sxs-lookup"><span data-stu-id="34bce-122">Discovery and Metadata Exchange Message Patterns</span></span>](discovery-and-metadata-exchange-message-patterns.md)
</dt> </dl>

 

 



