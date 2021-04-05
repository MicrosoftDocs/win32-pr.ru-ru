---
title: Насколько защищен мой RPC-сервер?
description: При обеспечении безопасности, описанной в этом разделе, в других пакетах SDK для RPC и, как правило, в качестве правильных методов обеспечения безопасности, будет обеспечен очень безопасный сервер. Такие серверы защищены от атак на проникновение в уязвимости или нарушений конфиденциальности.
ms.assetid: 528ff35c-f37c-43d8-8cc1-dbc36a9a826c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34279e4fb8899db6b7e980a0e868e91c6edb8166
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986527"
---
# <a name="how-secure-is-my-rpc-server-now"></a><span data-ttu-id="6268f-104">Насколько защищен мой RPC-сервер?</span><span class="sxs-lookup"><span data-stu-id="6268f-104">How Secure is My RPC Server Now?</span></span>

<span data-ttu-id="6268f-105">При обеспечении безопасности, описанной в этом разделе, в других пакетах SDK для RPC и, как правило, в качестве правильных методов обеспечения безопасности, будет обеспечен очень безопасный сервер.</span><span class="sxs-lookup"><span data-stu-id="6268f-105">Following the security outlined in this section, provided elsewhere in the RPC SDK, and generally accepted as proper security practices, will result in a server that is very secure.</span></span> <span data-ttu-id="6268f-106">Такие серверы защищены от атак на проникновение в уязвимости или нарушений конфиденциальности.</span><span class="sxs-lookup"><span data-stu-id="6268f-106">Such servers are protected from penetration attacks or privacy breaches.</span></span>

<span data-ttu-id="6268f-107">Если между вызовами RPC хранится состояние, убедитесь, что один клиент не приводит к выделению чрезмерных ресурсов, что может привести к отказу в обслуживании других клиентов.</span><span class="sxs-lookup"><span data-stu-id="6268f-107">If state is kept between RPC calls, make sure a single client does not cause the allocation of excessive resources, which could potentially deny service to other clients.</span></span>

 

 




