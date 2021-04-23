---
title: Балансировка нагрузки RPC
description: Балансировка нагрузки RPC
ms.assetid: c646f748-d5f2-422d-8305-1f86c0dc61b4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4039742fcfcc67280c610270908bed51034f691a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067417"
---
# <a name="rpc-load-balancing"></a><span data-ttu-id="03a9e-103">Балансировка нагрузки RPC</span><span class="sxs-lookup"><span data-stu-id="03a9e-103">RPC Load Balancing</span></span>

<span data-ttu-id="03a9e-104">Балансировка нагрузки Microsoft RPC предназначена для обеспечения масштабируемого решения для сценариев, требующих высокой нагрузки трафика [RPC через HTTP](remote-procedure-calls-using-rpc-over-http.md) .</span><span class="sxs-lookup"><span data-stu-id="03a9e-104">Microsoft RPC Load Balancing is intended to provide a scalable solution for scenarios which demand a high load of [RPC over HTTP](remote-procedure-calls-using-rpc-over-http.md) traffic.</span></span> <span data-ttu-id="03a9e-105">Основной целью RPC-Load Balancer является обеспечение возможности обслуживания трафика RPC/HTTP в ферме серверов для повышения масштабируемости.</span><span class="sxs-lookup"><span data-stu-id="03a9e-105">The RPC Load Balancer’s primary purpose is to ensure RPC/HTTP traffic can be serviced by a server farm to improve scalability.</span></span> <span data-ttu-id="03a9e-106">Для этого RPC должен убедиться, что все соединения от клиентского процесса обслуживаются одной и той же конечной точкой сервера в ферме серверов.</span><span class="sxs-lookup"><span data-stu-id="03a9e-106">To achieve this, RPC must ensure that all connections from a client process are serviced by the same server endpoint in the server farm.</span></span> <span data-ttu-id="03a9e-107">Load Balancer RPC реализуется как служба, которая выполняется в сочетании с прокси-службой RPC через HTTP.</span><span class="sxs-lookup"><span data-stu-id="03a9e-107">The RPC Load Balancer is implemented as a service which runs in conjunction with the RPC over HTTP Proxy service.</span></span>

<span data-ttu-id="03a9e-108">Чтобы включить балансировку нагрузки, служба балансировки нагрузки RPC, запущенная на каждом из серверов, взаимодействует друг с другом, чтобы определить предпочитаемый сервер для первоначального подключения клиента.</span><span class="sxs-lookup"><span data-stu-id="03a9e-108">To enable load balancing, the RPC Load Balancing service running on each of the servers communicates with each other to determine the preferred server for the initial client connection.</span></span> <span data-ttu-id="03a9e-109">Этот процесс называется арбитражом и возникает во время первоначального подключения клиента.</span><span class="sxs-lookup"><span data-stu-id="03a9e-109">This process is called arbitration and it occurs at the time of the initial client connection.</span></span> <span data-ttu-id="03a9e-110">Для уменьшения межсерверного трафика служба балансировки нагрузки RPC выбирает локальную конечную точку для обслуживания соединения, если клиент еще не связан с сервером.</span><span class="sxs-lookup"><span data-stu-id="03a9e-110">To reduce cross server traffic, the RPC Load Balancing service chooses the local endpoint to service the connection if the client is not already associated with a server.</span></span> <span data-ttu-id="03a9e-111">Для данного клиентского соединения результат арбитража — одна из двух возможностей:</span><span class="sxs-lookup"><span data-stu-id="03a9e-111">For a given client connection, the outcome of arbitration is one of two possibilities:</span></span>

-   <span data-ttu-id="03a9e-112">Если клиент уже установил подключение, сервер, который сначала получает подключение, будет выполнять все последующие соединения.</span><span class="sxs-lookup"><span data-stu-id="03a9e-112">If the client has already made a connection, the server to first receive the connection will handle the subsequent connections.</span></span>
-   <span data-ttu-id="03a9e-113">Если это первое соединение с клиентом, то при арбитраже будет применен локальный сервер, обрабатывающий подключение, и, следовательно, все соединения от клиента.</span><span class="sxs-lookup"><span data-stu-id="03a9e-113">If this is the first connection from the client, arbitration will result in the local server handling the connection, and thus all connections from the client.</span></span> <span data-ttu-id="03a9e-114">Эти сведения, будучи определенными, будут зафиксированы в других службах Load Balancer RPC в ферме серверов, тем самым уведомляя их о том, что сервер обрабатывает все клиентские запросы.</span><span class="sxs-lookup"><span data-stu-id="03a9e-114">This information, once determined, will be committed to the other RPC Load Balancer services in the server farm, thus informing them of the server handling all of the client’s requests.</span></span>

<span data-ttu-id="03a9e-115">В этом разделе приводятся общие сведения о балансировке нагрузки RPC в следующих разделах.</span><span class="sxs-lookup"><span data-stu-id="03a9e-115">This section provides an overview of RPC Load Balancing in the following topics:</span></span>

-   [<span data-ttu-id="03a9e-116">Развертывание балансировки нагрузки</span><span class="sxs-lookup"><span data-stu-id="03a9e-116">Deploying Load Balancing</span></span>](deploying-load-balancing.md)
-   [<span data-ttu-id="03a9e-117">Настройка балансировки нагрузки</span><span class="sxs-lookup"><span data-stu-id="03a9e-117">Configuring Load Balancing</span></span>](configuring-load-balancing.md)
-   [<span data-ttu-id="03a9e-118">Рекомендации по балансировке нагрузки</span><span class="sxs-lookup"><span data-stu-id="03a9e-118">Load Balancing Best Practices</span></span>](load-balancing-best-practices.md)

## <a name="requirements"></a><span data-ttu-id="03a9e-119">Требования</span><span class="sxs-lookup"><span data-stu-id="03a9e-119">Requirements</span></span>

<span data-ttu-id="03a9e-120">Служба балансировки нагрузки RPC поддерживается на серверах под управлением Windows Server 2008 R2 или более поздней версии, а также на клиентах под управлением Windows 7 или более поздних версий Windows.</span><span class="sxs-lookup"><span data-stu-id="03a9e-120">The RPC Load Balancing service is supported on servers running Windows Server 2008 R2 or later and clients running Windows 7 or later versions of Windows.</span></span>

<span data-ttu-id="03a9e-121">Служба RPC-прокси, служба балансировки нагрузки RPC и конечные точки сервера должны работать на одном компьютере.</span><span class="sxs-lookup"><span data-stu-id="03a9e-121">The RPC Proxy service, the RPC Load Balancing service and the server endpoints must all be running on the same machine.</span></span> <span data-ttu-id="03a9e-122">Кроме того, все серверы фермы серверов должны поддерживать обслуживание запрошенной конечной точки.</span><span class="sxs-lookup"><span data-stu-id="03a9e-122">Additionally, all servers in the server farm must be capable of servicing the requested endpoint.</span></span> <span data-ttu-id="03a9e-123">Сведения о настройке прокси-службы RPC и службы балансировки нагрузки RPC см. в разделе [Настройка компьютеров для RPC через HTTP](configuring-computers-for-rpc-over-http.md) и [Настройка балансировки нагрузки](configuring-load-balancing.md)соответственно.</span><span class="sxs-lookup"><span data-stu-id="03a9e-123">For information on configuring the RPC Proxy service and the RPC Load Balancing service, see [Configuring Computers for RPC over HTTP](configuring-computers-for-rpc-over-http.md) and [Configuring Load Balancing](configuring-load-balancing.md), respectively.</span></span>

## <a name="limitations"></a><span data-ttu-id="03a9e-124">Ограничения</span><span class="sxs-lookup"><span data-stu-id="03a9e-124">Limitations</span></span>

<span data-ttu-id="03a9e-125">В настоящее время балансировка нагрузки RPC поддерживает только одну ферму серверов для каждого ресурса.</span><span class="sxs-lookup"><span data-stu-id="03a9e-125">At this time, RPC Load Balancing supports only one server farm per resource.</span></span> <span data-ttu-id="03a9e-126">Все серверы во всех фермах серверов должны поддерживать обслуживание всех ресурсов.</span><span class="sxs-lookup"><span data-stu-id="03a9e-126">All servers in all server farms must be capable of servicing all resources as well.</span></span>

 

 




