---
title: DNS-серверы
description: DNS-сервер — это компьютер, который завершает процесс разрешения имен в DNS.
ms.assetid: c7ce6e46-491c-482e-8d72-a79b911c3f68
keywords:
- DNS-серверы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 509ceeb811f221560540ae60f269c6ee1b05444f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103777777"
---
# <a name="dns-servers"></a><span data-ttu-id="ce439-104">DNS-серверы</span><span class="sxs-lookup"><span data-stu-id="ce439-104">DNS Servers</span></span>

<span data-ttu-id="ce439-105">*DNS-сервер* — это компьютер, который завершает процесс разрешения имен в DNS.</span><span class="sxs-lookup"><span data-stu-id="ce439-105">A *DNS Server* is a computer that completes the process of name resolution in DNS.</span></span> <span data-ttu-id="ce439-106">DNS-серверы содержат [*файлы зон*](z-gly.md) , которые позволяют им разрешать имена в IP-адреса и IP-адреса в имена.</span><span class="sxs-lookup"><span data-stu-id="ce439-106">DNS Servers contain [*zone files*](z-gly.md) that enable them to resolve names to IP addresses and IP addresses to names.</span></span> <span data-ttu-id="ce439-107">При запросе DNS-сервер будет отвечать одним из трех способов:</span><span class="sxs-lookup"><span data-stu-id="ce439-107">When queried, a DNS Server will respond in one of three ways:</span></span>

-   <span data-ttu-id="ce439-108">Сервер возвращает запрошенные данные разрешения имен или разрешения IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="ce439-108">The server returns the requested name-resolution or IP-resolution data.</span></span>
-   <span data-ttu-id="ce439-109">Сервер возвращает указатель на другой DNS-сервер, который может обслуживать запрос.</span><span class="sxs-lookup"><span data-stu-id="ce439-109">The server returns a pointer to another DNS Server that can service the request.</span></span>
-   <span data-ttu-id="ce439-110">Сервер указывает, что у него нет запрошенных данных.</span><span class="sxs-lookup"><span data-stu-id="ce439-110">The server indicates that it does not have the requested data.</span></span>

<span data-ttu-id="ce439-111">DNS-серверы могут, во время подготовки к возврату запрошенных данных разрешения, выполнять запросы к другим DNS-серверам, но после этого DNS-серверы не выполняют никаких других операций.</span><span class="sxs-lookup"><span data-stu-id="ce439-111">DNS Servers might, during the course of preparing to return the requested resolution data, query other DNS Servers, but beyond that, DNS Servers do not perform any other operations.</span></span>

<span data-ttu-id="ce439-112">Существует три основных типа DNS-серверов: основные серверы, серверы-получатели и серверы кэширования.</span><span class="sxs-lookup"><span data-stu-id="ce439-112">There are three main kinds of DNS Servers — primary servers, secondary servers, and caching servers.</span></span>

## <a name="primary-server"></a><span data-ttu-id="ce439-113">Основной сервер</span><span class="sxs-lookup"><span data-stu-id="ce439-113">Primary Server</span></span>

<span data-ttu-id="ce439-114">*Сервер-источник* является полномочным сервером для зоны.</span><span class="sxs-lookup"><span data-stu-id="ce439-114">The *primary server* is the authoritative server for the zone.</span></span> <span data-ttu-id="ce439-115">Все задачи администрирования, связанные с зоной (например, создание поддоменов в зоне или другие аналогичные задачи администрирования), должны выполняться на сервере-источнике.</span><span class="sxs-lookup"><span data-stu-id="ce439-115">All administrative tasks associated with the zone (such as creating subdomains within the zone, or other similar administrative tasks) must be performed on the primary server.</span></span> <span data-ttu-id="ce439-116">Кроме того, любые изменения, связанные с зоной или любые изменения или дополнения к записям RR в файлах зоны, должны выполняться на сервере источника.</span><span class="sxs-lookup"><span data-stu-id="ce439-116">In addition, any changes associated with the zone or any modifications or additions to RRs in the zone files must be made on the primary server.</span></span> <span data-ttu-id="ce439-117">Для любой конкретной зоны существует один сервер-источник, за исключением интеграции Active Directory служб и DNS-сервера Microsoft.</span><span class="sxs-lookup"><span data-stu-id="ce439-117">For any given zone, there is one primary server, except when you integrate Active Directory services and Microsoft DNS Server.</span></span>

## <a name="secondary-servers"></a><span data-ttu-id="ce439-118">Серверы-получатели</span><span class="sxs-lookup"><span data-stu-id="ce439-118">Secondary Servers</span></span>

<span data-ttu-id="ce439-119">*Серверы-получатели* являются резервными.</span><span class="sxs-lookup"><span data-stu-id="ce439-119">*Secondary servers* are backup DNS Servers.</span></span> <span data-ttu-id="ce439-120">Серверы-получатели получают все свои файлы зон из файлов зоны основного сервера при переносе зоны.</span><span class="sxs-lookup"><span data-stu-id="ce439-120">Secondary servers receive all of their zone files from the primary server zone files in a zone transfer.</span></span> <span data-ttu-id="ce439-121">Для каждой определенной зоны может существовать несколько серверов-получателей, сколько необходимо для обеспечения [*балансировки нагрузки*](l-gly.md), [*отказоустойчивости*](f-gly.md)и снижения трафика.</span><span class="sxs-lookup"><span data-stu-id="ce439-121">Multiple secondary servers can exist for any given zone — as many as necessary to provide [*load balancing*](l-gly.md), [*fault tolerance*](f-gly.md), and traffic reduction.</span></span> <span data-ttu-id="ce439-122">Кроме того, любой заданный DNS-сервер может быть дополнительным сервером для нескольких зон.</span><span class="sxs-lookup"><span data-stu-id="ce439-122">Additionally, any given DNS Server can be a secondary server for multiple zones.</span></span>

<span data-ttu-id="ce439-123">Помимо основного и дополнительного DNS-серверов, можно использовать дополнительные роли DNS-сервера, если такие серверы подходят для инфраструктуры DNS.</span><span class="sxs-lookup"><span data-stu-id="ce439-123">In addition to primary and secondary DNS Servers, additional DNS Server roles can be used when such servers are appropriate for a DNS infrastructure.</span></span> <span data-ttu-id="ce439-124">Эти дополнительные серверы являются серверами кэширования и серверов [*пересылки*](f-gly.md).</span><span class="sxs-lookup"><span data-stu-id="ce439-124">These additional servers are caching servers and [*forwarders*](f-gly.md).</span></span>

## <a name="caching-servers"></a><span data-ttu-id="ce439-125">Серверы кэширования</span><span class="sxs-lookup"><span data-stu-id="ce439-125">Caching Servers</span></span>

<span data-ttu-id="ce439-126">[*Серверы кэширования*](c-gly.md), также известные как серверы кэширования, выполняются в соответствии с их именами. они предоставляют только службу кэшированных запросов для ответов DNS.</span><span class="sxs-lookup"><span data-stu-id="ce439-126">[*Caching servers*](c-gly.md), also known as caching-only servers, perform as their name suggests; they provide only cached-query service for DNS responses.</span></span> <span data-ttu-id="ce439-127">Вместо того, чтобы хранить файлы зоны, такие как другие серверы-получатели, кэширование серверов DNS выполняет запросы, кэширует ответы и возвращает результаты клиенту запроса.</span><span class="sxs-lookup"><span data-stu-id="ce439-127">Rather than maintaining zone files like other secondary servers do, caching DNS Servers perform queries, cache the answers, and return the results to the querying client.</span></span> <span data-ttu-id="ce439-128">Основное различие между серверами кэширования и другими серверами-получателями заключается в том, что другие вторичные серверы сохраняют файлы зоны (и при необходимости выполняют передачу зоны, тем самым создавая сетевой трафик, связанный с передачей), а серверы кэширования — нет.</span><span class="sxs-lookup"><span data-stu-id="ce439-128">The primary difference between caching servers and other secondary servers is that other secondary servers maintain zone files (and do zone transfers when appropriate, thereby generating network traffic associated with the transfer), caching servers do not.</span></span>

 

 




