---
title: Не использовать безопасность конечных точек
description: Безопасность конечных точек — это модель безопасности, в которой дескриптор безопасности предоставляется при создании конечной точки с помощью Рпксерверусепротсек \ Group функций RPC.
ms.assetid: 5b8841c4-5b65-417f-b790-e8c2dabb44a1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 289513810ba7e67e0da625151c3c2975e0eaaf99
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103775497"
---
# <a name="do-not-use-endpoint-security"></a><span data-ttu-id="eb351-103">Не использовать безопасность конечных точек</span><span class="sxs-lookup"><span data-stu-id="eb351-103">Do Not Use Endpoint Security</span></span>

<span data-ttu-id="eb351-104">Безопасность конечных точек — это модель безопасности, в которой дескриптор безопасности предоставляется при создании конечной точки с помощью [**рпксерверусепротсек**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq) \* группы функций RPC.</span><span class="sxs-lookup"><span data-stu-id="eb351-104">Endpoint security is a security model in which a security descriptor is given when an endpoint is created with the [**RpcServerUseProtseq**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq)\* group of RPC functions.</span></span> <span data-ttu-id="eb351-105">Не используйте эту модель безопасности.</span><span class="sxs-lookup"><span data-stu-id="eb351-105">Do not use this security model.</span></span> <span data-ttu-id="eb351-106">Не присваивайте этим функциям дескрипторы безопасности.</span><span class="sxs-lookup"><span data-stu-id="eb351-106">Do not give security descriptors to those functions.</span></span> <span data-ttu-id="eb351-107">В лучшем случае этот метод не тратит ресурсы ЦП.</span><span class="sxs-lookup"><span data-stu-id="eb351-107">At best, this method is a waste of CPU resources.</span></span> <span data-ttu-id="eb351-108">В худшем случае, во многих средах можно обойти дескриптор безопасности, так как с [осторожностью других конечных точек RPC, выполняемых в том же](be-wary-of-other-rpc-endpoints-running-in-the-same-process.md) обладает разделе процесса.</span><span class="sxs-lookup"><span data-stu-id="eb351-108">At worst, in many environments it is possible to circumvent the security descriptor, as the [Be Wary of Other RPC Endpoints Running In the Same Process](be-wary-of-other-rpc-endpoints-running-in-the-same-process.md) section exemplifies.</span></span>

<span data-ttu-id="eb351-109">Безопасность конечных точек существует только для обеспечения обратной совместимости.</span><span class="sxs-lookup"><span data-stu-id="eb351-109">Endpoint security exists only for backward compatibility.</span></span>

 

 




