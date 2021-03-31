---
title: Публикация службы
description: Службы объявляются с помощью объектов, хранящихся в службах домен Active Directory.
ms.assetid: 69e9256f-40ee-4aed-8213-1bbda0e508af
ms.tgt_platform: multiple
keywords:
- Публикация службы AD
- Active Directory, использование, публикация службы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9437d9f4aa5184c53f2962d7b2640e933107501f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067352"
---
# <a name="service-publication"></a><span data-ttu-id="55b16-105">Публикация службы</span><span class="sxs-lookup"><span data-stu-id="55b16-105">Service Publication</span></span>

<span data-ttu-id="55b16-106">Службы объявляются с помощью объектов, хранящихся в службах домен Active Directory.</span><span class="sxs-lookup"><span data-stu-id="55b16-106">Services advertise themselves using objects stored in Active Directory Domain Services.</span></span> <span data-ttu-id="55b16-107">Это называется *публикацией службы*.</span><span class="sxs-lookup"><span data-stu-id="55b16-107">This is known as *service publication*.</span></span> <span data-ttu-id="55b16-108">Клиенты запрашивают каталог для поиска служб.</span><span class="sxs-lookup"><span data-stu-id="55b16-108">Clients query the directory to locate services.</span></span> <span data-ttu-id="55b16-109">Это называется *встречей Client-Service*.</span><span class="sxs-lookup"><span data-stu-id="55b16-109">This is called *client-service rendezvous*.</span></span> <span data-ttu-id="55b16-110">В этом разделе обсуждаются типы объектов каталога, используемые для публикации службы, и объясняется, как они используются для встреч с клиентскими службами.</span><span class="sxs-lookup"><span data-stu-id="55b16-110">This section discusses the types of directory objects used for service publication and explains how they are used for client-service rendezvous.</span></span>

<span data-ttu-id="55b16-111">В этом разделе рассматриваются следующие темы:</span><span class="sxs-lookup"><span data-stu-id="55b16-111">This section discusses the following topics:</span></span>

-   [<span data-ttu-id="55b16-112">Общие сведения о публикации службы</span><span class="sxs-lookup"><span data-stu-id="55b16-112">An overview of service publication</span></span>](about-service-publication.md)
-   [<span data-ttu-id="55b16-113">Проблемы безопасности для публикации службы</span><span class="sxs-lookup"><span data-stu-id="55b16-113">Security issues for service publication</span></span>](security-issues-for-service-publication.md)
-   [<span data-ttu-id="55b16-114">Объекты точек подключения</span><span class="sxs-lookup"><span data-stu-id="55b16-114">Connection point objects</span></span>](connection-points.md)
-   [<span data-ttu-id="55b16-115">Публикация с точками подключения службы (запрашивая)</span><span class="sxs-lookup"><span data-stu-id="55b16-115">Publishing with service connection points (SCPs)</span></span>](publishing-with-service-connection-points.md)
-   [<span data-ttu-id="55b16-116">Сведения для хранения в точке подключения службы</span><span class="sxs-lookup"><span data-stu-id="55b16-116">What information to store in a service connection point</span></span>](service-connection-point-properties.md)
-   [<span data-ttu-id="55b16-117">Где можно создать точку подключения службы</span><span class="sxs-lookup"><span data-stu-id="55b16-117">Where to create a service connection point</span></span>](where-to-create-a-service-connection-point.md)
-   [<span data-ttu-id="55b16-118">Публикация реплицируемых, основанных на узлах и служб баз данных с помощью точек подключения службы</span><span class="sxs-lookup"><span data-stu-id="55b16-118">How to publish replicable, host-based, and database services using service connection points</span></span>](service-connection-points-for-replicated-host-based-and-database-services.md)
-   [<span data-ttu-id="55b16-119">Создание и обслуживание точки подключения службы</span><span class="sxs-lookup"><span data-stu-id="55b16-119">Creating and maintaining a service connection point</span></span>](creating-and-maintaining-a-service-connection-point.md)
-   [<span data-ttu-id="55b16-120">Как клиент запрашивает точку подключения службы и использует ее для привязки к экземпляру службы</span><span class="sxs-lookup"><span data-stu-id="55b16-120">How a client queries for an SCP and uses it to bind to a service instance</span></span>](how-clients-find-and-use-a-service-connection-point.md)
-   [<span data-ttu-id="55b16-121">Использование API службы имен RPC (Рпкнс) для публикации службы RPC</span><span class="sxs-lookup"><span data-stu-id="55b16-121">Using the RPC name service (RpcNs) APIs to publish an RPC service</span></span>](publishing-with-the-rpc-name-service-rpcns.md)
-   [<span data-ttu-id="55b16-122">Регистрация и разрешение Windows Sockets (РНР) для публикации службы сокетов Windows</span><span class="sxs-lookup"><span data-stu-id="55b16-122">Windows Sockets registration and resolution (RnR) to publish a Windows Sockets service</span></span>](publishing-with-windows-sockets-registration-and-resolution.md)
-   [<span data-ttu-id="55b16-123">Публикация служб на основе COM в хранилище классов COM+</span><span class="sxs-lookup"><span data-stu-id="55b16-123">Publication of COM-based services in the COM+ class store</span></span>](publishing-com-services.md)

<span data-ttu-id="55b16-124">Дополнительные сведения о проверке подлинности между службами и клиентами см. в статье [взаимная проверка подлинности с помощью протокола Kerberos](mutual-authentication-using-kerberos.md).</span><span class="sxs-lookup"><span data-stu-id="55b16-124">For more information about how services and clients authenticate each other, see [Mutual Authentication Using Kerberos](mutual-authentication-using-kerberos.md).</span></span> <span data-ttu-id="55b16-125">Дополнительные сведения о контекстах безопасности службы и учетных записях входа см. в статье [учетные записи входа в службу](service-logon-accounts.md).</span><span class="sxs-lookup"><span data-stu-id="55b16-125">For more information about service security contexts and logon accounts, see [Service Logon Accounts](service-logon-accounts.md).</span></span>

 

 




