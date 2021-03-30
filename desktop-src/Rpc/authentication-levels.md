---
title: Уровни проверки подлинности
description: Microsoft RPC обеспечивает несколько уровней проверки подлинности.
ms.assetid: d9ed938e-4cd4-4355-8d08-830f955dd00c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c5fd25efb84b4ee2834e6f79c7fdd21dd903d55
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104253224"
---
# <a name="authentication-levels"></a><span data-ttu-id="42709-103">Уровни проверки подлинности</span><span class="sxs-lookup"><span data-stu-id="42709-103">Authentication Levels</span></span>

<span data-ttu-id="42709-104">Microsoft RPC обеспечивает несколько уровней проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="42709-104">Microsoft RPC provides multiple levels of authentication.</span></span> <span data-ttu-id="42709-105">В зависимости от уровня проверки подлинности источник трафика (участника безопасности, отправившего трафик) может быть проверен при установке соединения, когда клиент запускает новый удаленный вызов процедуры или при обмене пакетами между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="42709-105">Depending on the authentication level, the origin of the traffic (which security principal sent the traffic) can be verified when the connection is established, when the client starts a new remote procedure call, or during each packet exchange between the client and server.</span></span>

<span data-ttu-id="42709-106">Даже при проверке отправителя трафика безопасность остается ненадежной, так как такая проверка не гарантирует, что пакет не был изменен или был поврежден. Он только проверяет, получен ли пакет от данного участника.</span><span class="sxs-lookup"><span data-stu-id="42709-106">Even when the sender of the traffic is verified, security is still weak, since such verification does not ensure the packet was not modified or corrupted en route; it only verifies that the packet came from the given principal.</span></span> <span data-ttu-id="42709-107">Для повышения безопасности распределенные приложения могут задать библиотеку времени выполнения RPC, чтобы убедиться в том, что ни один из данных, которыми обмениваются клиент и сервер, не изменяется.</span><span class="sxs-lookup"><span data-stu-id="42709-107">For greater security, distributed applications can set the RPC run-time library to verify that none of the data exchanged between the client and server is modified.</span></span> <span data-ttu-id="42709-108">Кроме того, с помощью библиотеки RPC можно зашифровать содержимое каждого пакета перед его отправкой.</span><span class="sxs-lookup"><span data-stu-id="42709-108">The RPC library can also encrypt the contents of every packet before sending it.</span></span> <span data-ttu-id="42709-109">Как правило, приложения, которые хотят защитить свой трафик, должны использовать только два последних уровня — целостность и конфиденциальность.</span><span class="sxs-lookup"><span data-stu-id="42709-109">In general, applications that want to secure their traffic should use only the last two levels—integrity and privacy.</span></span>

<span data-ttu-id="42709-110">Имейте в виду, что для более высоких уровней проверки подлинности требуются более высокие вычислительные ресурсы.</span><span class="sxs-lookup"><span data-stu-id="42709-110">Be aware that higher levels of authentication require higher computational overhead.</span></span> <span data-ttu-id="42709-111">Вы, как разработчик, должны решить, какое значение важнее для вашего приложения — скорость или безопасность.</span><span class="sxs-lookup"><span data-stu-id="42709-111">You, as the developer, must decide which is more important for your application—speed or security.</span></span> <span data-ttu-id="42709-112">Большинство разработчиков находят, что при тестировании производительности они могут достичь приемлемых уровней производительности, обеспечивая адекватное обеспечение безопасности.</span><span class="sxs-lookup"><span data-stu-id="42709-112">Most developers find that with some performance testing, they can achieve acceptable performance levels while maintaining adequate security.</span></span>

<span data-ttu-id="42709-113">Клиентская и серверная части распределенного приложения должны использовать одинаковый уровень проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="42709-113">The client and the server portions of the distributed application must use the same authentication level.</span></span> <span data-ttu-id="42709-114">Список уровней проверки подлинности RPC см. в разделе [константы уровня проверки подлинности](authentication-level-constants.md).</span><span class="sxs-lookup"><span data-stu-id="42709-114">For a list of RPC authentication levels, see [Authentication-Level Constants](authentication-level-constants.md).</span></span>

 

 




