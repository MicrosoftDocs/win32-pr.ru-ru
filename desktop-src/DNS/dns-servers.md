---
title: DNS-серверы
description: Сведения о DNS-серверах. DNS-сервер — это компьютер, который завершает процесс разрешения имен в DNS.
ms.assetid: c7ce6e46-491c-482e-8d72-a79b911c3f68
keywords:
- DNS-серверы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fe2415c50cdd2472b20e8f14123afa2aa919d26
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2021
ms.locfileid: "112011257"
---
# <a name="dns-servers"></a><span data-ttu-id="72cf9-105">DNS-серверы</span><span class="sxs-lookup"><span data-stu-id="72cf9-105">DNS Servers</span></span>

<span data-ttu-id="72cf9-106">*DNS-сервер* — это компьютер, который завершает процесс разрешения имен в DNS.</span><span class="sxs-lookup"><span data-stu-id="72cf9-106">A *DNS Server* is a computer that completes the process of name resolution in DNS.</span></span> <span data-ttu-id="72cf9-107">DNS-серверы содержат [*файлы зон*](z-gly.md) , которые позволяют им разрешать имена в IP-адреса и IP-адреса в имена.</span><span class="sxs-lookup"><span data-stu-id="72cf9-107">DNS Servers contain [*zone files*](z-gly.md) that enable them to resolve names to IP addresses and IP addresses to names.</span></span> <span data-ttu-id="72cf9-108">При запросе DNS-сервер будет отвечать одним из трех способов:</span><span class="sxs-lookup"><span data-stu-id="72cf9-108">When queried, a DNS Server will respond in one of three ways:</span></span>

-   <span data-ttu-id="72cf9-109">Сервер возвращает запрошенные данные разрешения имен или разрешения IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="72cf9-109">The server returns the requested name-resolution or IP-resolution data.</span></span>
-   <span data-ttu-id="72cf9-110">Сервер возвращает указатель на другой DNS-сервер, который может обслуживать запрос.</span><span class="sxs-lookup"><span data-stu-id="72cf9-110">The server returns a pointer to another DNS Server that can service the request.</span></span>
-   <span data-ttu-id="72cf9-111">Сервер указывает, что у него нет запрошенных данных.</span><span class="sxs-lookup"><span data-stu-id="72cf9-111">The server indicates that it does not have the requested data.</span></span>

<span data-ttu-id="72cf9-112">DNS-серверы могут, во время подготовки к возврату запрошенных данных разрешения, выполнять запросы к другим DNS-серверам, но после этого DNS-серверы не выполняют никаких других операций.</span><span class="sxs-lookup"><span data-stu-id="72cf9-112">DNS Servers might, during the course of preparing to return the requested resolution data, query other DNS Servers, but beyond that, DNS Servers do not perform any other operations.</span></span>

<span data-ttu-id="72cf9-113">Существует три основных типа DNS-серверов: основные серверы, серверы-получатели и серверы кэширования.</span><span class="sxs-lookup"><span data-stu-id="72cf9-113">There are three main kinds of DNS Servers — primary servers, secondary servers, and caching servers.</span></span>

## <a name="primary-server"></a><span data-ttu-id="72cf9-114">Основной сервер</span><span class="sxs-lookup"><span data-stu-id="72cf9-114">Primary Server</span></span>

<span data-ttu-id="72cf9-115">*Сервер-источник* является полномочным сервером для зоны.</span><span class="sxs-lookup"><span data-stu-id="72cf9-115">The *primary server* is the authoritative server for the zone.</span></span> <span data-ttu-id="72cf9-116">Все задачи администрирования, связанные с зоной (например, создание поддоменов в зоне или другие аналогичные задачи администрирования), должны выполняться на сервере-источнике.</span><span class="sxs-lookup"><span data-stu-id="72cf9-116">All administrative tasks associated with the zone (such as creating subdomains within the zone, or other similar administrative tasks) must be performed on the primary server.</span></span> <span data-ttu-id="72cf9-117">Кроме того, любые изменения, связанные с зоной или любые изменения или дополнения к записям RR в файлах зоны, должны выполняться на сервере источника.</span><span class="sxs-lookup"><span data-stu-id="72cf9-117">In addition, any changes associated with the zone or any modifications or additions to RRs in the zone files must be made on the primary server.</span></span> <span data-ttu-id="72cf9-118">Для любой конкретной зоны существует один сервер-источник, за исключением интеграции Active Directory служб и DNS-сервера Microsoft.</span><span class="sxs-lookup"><span data-stu-id="72cf9-118">For any given zone, there is one primary server, except when you integrate Active Directory services and Microsoft DNS Server.</span></span>

## <a name="secondary-servers"></a><span data-ttu-id="72cf9-119">Серверы-получатели</span><span class="sxs-lookup"><span data-stu-id="72cf9-119">Secondary Servers</span></span>

<span data-ttu-id="72cf9-120">*Серверы-получатели* являются резервными.</span><span class="sxs-lookup"><span data-stu-id="72cf9-120">*Secondary servers* are backup DNS Servers.</span></span> <span data-ttu-id="72cf9-121">Серверы-получатели получают все свои файлы зон из файлов зоны основного сервера при переносе зоны.</span><span class="sxs-lookup"><span data-stu-id="72cf9-121">Secondary servers receive all of their zone files from the primary server zone files in a zone transfer.</span></span> <span data-ttu-id="72cf9-122">Для каждой определенной зоны может существовать несколько серверов-получателей, сколько необходимо для обеспечения [*балансировки нагрузки*](l-gly.md), [*отказоустойчивости*](f-gly.md)и снижения трафика.</span><span class="sxs-lookup"><span data-stu-id="72cf9-122">Multiple secondary servers can exist for any given zone — as many as necessary to provide [*load balancing*](l-gly.md), [*fault tolerance*](f-gly.md), and traffic reduction.</span></span> <span data-ttu-id="72cf9-123">Кроме того, любой заданный DNS-сервер может быть дополнительным сервером для нескольких зон.</span><span class="sxs-lookup"><span data-stu-id="72cf9-123">Additionally, any given DNS Server can be a secondary server for multiple zones.</span></span>

<span data-ttu-id="72cf9-124">Помимо основного и дополнительного DNS-серверов, можно использовать дополнительные роли DNS-сервера, если такие серверы подходят для инфраструктуры DNS.</span><span class="sxs-lookup"><span data-stu-id="72cf9-124">In addition to primary and secondary DNS Servers, additional DNS Server roles can be used when such servers are appropriate for a DNS infrastructure.</span></span> <span data-ttu-id="72cf9-125">Эти дополнительные серверы являются серверами кэширования и серверов [*пересылки*](f-gly.md).</span><span class="sxs-lookup"><span data-stu-id="72cf9-125">These additional servers are caching servers and [*forwarders*](f-gly.md).</span></span>

## <a name="caching-servers"></a><span data-ttu-id="72cf9-126">Серверы кэширования</span><span class="sxs-lookup"><span data-stu-id="72cf9-126">Caching Servers</span></span>

<span data-ttu-id="72cf9-127">[*Серверы кэширования*](c-gly.md), также известные как серверы кэширования, выполняются в соответствии с их именами. они предоставляют только службу кэшированных запросов для ответов DNS.</span><span class="sxs-lookup"><span data-stu-id="72cf9-127">[*Caching servers*](c-gly.md), also known as caching-only servers, perform as their name suggests; they provide only cached-query service for DNS responses.</span></span> <span data-ttu-id="72cf9-128">Вместо того, чтобы хранить файлы зоны, такие как другие серверы-получатели, кэширование серверов DNS выполняет запросы, кэширует ответы и возвращает результаты клиенту запроса.</span><span class="sxs-lookup"><span data-stu-id="72cf9-128">Rather than maintaining zone files like other secondary servers do, caching DNS Servers perform queries, cache the answers, and return the results to the querying client.</span></span> <span data-ttu-id="72cf9-129">Основное различие между серверами кэширования и другими серверами-получателями заключается в том, что другие вторичные серверы сохраняют файлы зоны (и при необходимости выполняют передачу зоны, тем самым создавая сетевой трафик, связанный с передачей), а серверы кэширования — нет.</span><span class="sxs-lookup"><span data-stu-id="72cf9-129">The primary difference between caching servers and other secondary servers is that other secondary servers maintain zone files (and do zone transfers when appropriate, thereby generating network traffic associated with the transfer), caching servers do not.</span></span>

 

 




