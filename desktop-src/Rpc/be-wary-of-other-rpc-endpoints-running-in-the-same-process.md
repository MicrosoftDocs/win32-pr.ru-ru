---
title: Будьте осторожны с другими конечными точками RPC, работающими в том же процессе
description: Если приложение находится в процессе с другими серверами RPC, все приложения прослушивают все протоколы.
ms.assetid: edb20108-e0c3-4b9b-b57d-45a96d9472ba
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00828ddf95fd024069a8a535c95673eb014d84b9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103777108"
---
# <a name="be-wary-of-other-rpc-endpoints-running-in-the-same-process"></a><span data-ttu-id="4f98e-103">Будьте осторожны с другими конечными точками RPC, работающими в том же процессе</span><span class="sxs-lookup"><span data-stu-id="4f98e-103">Be Wary of Other RPC Endpoints Running in the Same Process</span></span>

<span data-ttu-id="4f98e-104">Если приложение находится в процессе с другими серверами RPC, все приложения прослушивают все протоколы.</span><span class="sxs-lookup"><span data-stu-id="4f98e-104">When an application resides in a process with other RPC servers, all applications listen on all protocols.</span></span> <span data-ttu-id="4f98e-105">Таким образом, если компонент вызывает [**рпксерверусепротсек**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq) \* только для лрпк, он не обязательно должен быть доступен только для лрпк.</span><span class="sxs-lookup"><span data-stu-id="4f98e-105">As such, if a component calls [**RpcServerUseProtseq**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq)\* for LRPC only, it is not necessarily accessible over LRPC only.</span></span> <span data-ttu-id="4f98e-106">Он может быть доступен по другим протоколам, так как другие серверы RPC в процессе могут прослушивать каналы или сокеты (например,).</span><span class="sxs-lookup"><span data-stu-id="4f98e-106">It may be accessible over other protocols, since other RPC servers in the process may be listening on pipes or sockets (for example).</span></span>

<span data-ttu-id="4f98e-107">Как и в случае с ограниченными дескрипторами контекста, размещение другой конечной точки в процессе не означает, что другая конечная точка не существует.</span><span class="sxs-lookup"><span data-stu-id="4f98e-107">Similar to strict context handles, not putting another endpoint in the process does not mean another endpoint does not exist.</span></span> <span data-ttu-id="4f98e-108">Независимо от способа регистрации сервера, между интерфейсом и конечной точкой не существует специальной связи. все интерфейсы вызываемы для всех конечных точек в этом процессе.</span><span class="sxs-lookup"><span data-stu-id="4f98e-108">Regardless of how you register your server, there is no special association between your interface and your endpoint; all interfaces are callable on all endpoints in that process.</span></span> <span data-ttu-id="4f98e-109">Это еще одна причина, по которой модель безопасности конечной точки неэффективна; Если дескриптор безопасности размещается на конечной точке, злоумышленники могут вызвать интерфейс в другой конечной точке.</span><span class="sxs-lookup"><span data-stu-id="4f98e-109">This is another reason why the endpoint security model is ineffective; if a security descriptor is placed on an endpoint, attackers can call the interface on another endpoint.</span></span>

<span data-ttu-id="4f98e-110">Чтобы процесс вызывался только в определенной последовательности протокола, зарегистрируйте функцию обратного вызова безопасности и в этой функции проверьте, какая последовательность протоколов вызывается.</span><span class="sxs-lookup"><span data-stu-id="4f98e-110">To ensure a process be called only on a specific protocol sequence, register a security callback function, and in that function, check on which protocol sequence the call is made.</span></span>

 

 




