---
title: Разработка высокопроизводительного RPC-сервера
description: Сведения в этом разделе относятся к удаленным последовательностям протоколов нкакн \_ IP \_ TCP, нкакн \_ http, нкакн \_ NP, а также к Windows 2000 и Windows XP.
ms.assetid: 7b4239af-951b-4d1b-8ac3-224279f6929e
keywords:
- Удаленный вызов процедур RPC, рекомендации, Разработка высокопроизводительного сервера
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a18319c1f4ade80ae026b68c8f5540030b992b7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104488157"
---
# <a name="developing-a-high-performance-rpc-server"></a><span data-ttu-id="a8f41-104">Разработка высокопроизводительного RPC-сервера</span><span class="sxs-lookup"><span data-stu-id="a8f41-104">Developing a High Performance RPC Server</span></span>

<span data-ttu-id="a8f41-105">Сведения в этом разделе относятся к удаленным последовательностям протоколов: [**нкакн \_ IP \_ TCP**](/windows/desktop/Midl/ncacn-ip-tcp), [**нкакн \_ http**](/windows/desktop/Midl/ncacn-http), [**нкакн \_ NP**](/windows/desktop/Midl/ncacn-np), а также к Windows 2000 и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="a8f41-105">The information in this section applies to remote protocol sequences: [**ncacn\_ip\_tcp**](/windows/desktop/Midl/ncacn-ip-tcp), [**ncacn\_http**](/windows/desktop/Midl/ncacn-http), [**ncacn\_np**](/windows/desktop/Midl/ncacn-np), and to Windows 2000 and Windows XP.</span></span>

<span data-ttu-id="a8f41-106">В этом разделе рассматриваются три основных аспекта производительности сервера RPC.</span><span class="sxs-lookup"><span data-stu-id="a8f41-106">This section addresses three primary aspects of RPC server performance:</span></span>

-   [<span data-ttu-id="a8f41-107">Задержка и пропускная способность сети</span><span class="sxs-lookup"><span data-stu-id="a8f41-107">Network Latency and Throughput</span></span>](network-latency-and-throughput.md)
-   [<span data-ttu-id="a8f41-108">Масштабируемость</span><span class="sxs-lookup"><span data-stu-id="a8f41-108">Scalability</span></span>](scalability.md)
-   [<span data-ttu-id="a8f41-109">Прочие советы по повышению производительности RPC</span><span class="sxs-lookup"><span data-stu-id="a8f41-109">Miscellaneous RPC Performance Tips</span></span>](miscellaneous-rpc-performance-tips.md)

<span data-ttu-id="a8f41-110">Длина кода пути — это еще один основной фактор производительности для RPC.</span><span class="sxs-lookup"><span data-stu-id="a8f41-110">Code path length is another primary performance consideration for RPC.</span></span> <span data-ttu-id="a8f41-111">Длина пути к коду обычно понятна, а поскольку литература и средства широко доступны в этом разделе, в этой статье не рассматривается.</span><span class="sxs-lookup"><span data-stu-id="a8f41-111">Code path length is generally well understood, and since literature and tools are widely available on that topic, this article does not address it.</span></span>

<span data-ttu-id="a8f41-112">Важное и установленное общее правило производительности, которое следует помнить при рассмотрении производительности RPC, заключается в том, чтобы найти узкие места в системе и решить эту проблему.</span><span class="sxs-lookup"><span data-stu-id="a8f41-112">An important and established general performance rule to remember while considering RPC performance is this: find the bottleneck in the system, and work to resolve that.</span></span> <span data-ttu-id="a8f41-113">Узким местом ограничения может быть не программирование RPC, и в этом случае настройка производительности RPC не приведет к повышению производительности, пока не будет устранено узкое место.</span><span class="sxs-lookup"><span data-stu-id="a8f41-113">The gating bottleneck may not be the RPC programming, and if that is the case, performance tuning in RPC will not result in enhanced performance until that bottleneck is addressed.</span></span> <span data-ttu-id="a8f41-114">Например, система, сталкивались за состязанием за ресурсы, не нуждается в более эффективном использовании сети.</span><span class="sxs-lookup"><span data-stu-id="a8f41-114">For example, a system plagued by resource contention does not need to make more efficient use of the network.</span></span>

<span data-ttu-id="a8f41-115">Если система развернута в различных средах, рекомендуется убедиться, что все его аспекты настроены правильно, так как разные среды могут создавать различные узкие места производительности.</span><span class="sxs-lookup"><span data-stu-id="a8f41-115">If your system is deployed in various environments, it is a good idea to make sure all aspects of it are well tuned, as different environments can produce varied performance bottlenecks.</span></span>

 

 