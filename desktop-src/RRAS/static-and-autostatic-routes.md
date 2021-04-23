---
title: Статические и автостатические маршруты
description: Как правило, маршруты к удаленным сетям получаются динамически через протоколы маршрутизации.
ms.assetid: af2f2039-8131-4ca9-98bf-6aeb7a511034
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3faa8931e0fee5c75f598b920b7b97a1e0e829d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986757"
---
# <a name="static-and-autostatic-routes"></a><span data-ttu-id="4590c-103">Статические и автостатические маршруты</span><span class="sxs-lookup"><span data-stu-id="4590c-103">Static and Autostatic Routes</span></span>

<span data-ttu-id="4590c-104">Как правило, маршруты к удаленным сетям получаются динамически через протоколы маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="4590c-104">Typically, routes to remote networks are obtained dynamically through routing protocols.</span></span> <span data-ttu-id="4590c-105">Однако администратор может также *заполнить* таблицу маршрутизации, предоставив маршруты вручную.</span><span class="sxs-lookup"><span data-stu-id="4590c-105">However, the administrator can also *seed* the routing table by providing routes manually.</span></span> <span data-ttu-id="4590c-106">Эти маршруты называются *статическими*.</span><span class="sxs-lookup"><span data-stu-id="4590c-106">These routes are referred to as *static*.</span></span> <span data-ttu-id="4590c-107">Статический маршрут связан с интерфейсом, представляющим удаленную сеть.</span><span class="sxs-lookup"><span data-stu-id="4590c-107">A static route is associated with an interface that represents the remote network.</span></span> <span data-ttu-id="4590c-108">В отличие от динамических маршрутов, статические маршруты сохраняются даже при перезапуске маршрутизатора или отключенном интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="4590c-108">Unlike dynamic routes, static routes are retained even if the router is restarted or the interface is disabled.</span></span>

<span data-ttu-id="4590c-109">*Статический* маршрут получается через протокол маршрутизации, но после его получения ведет себя как статический маршрут.</span><span class="sxs-lookup"><span data-stu-id="4590c-109">An *autostatic* route is obtained through a routing protocol, but once obtained behaves like a static route.</span></span> <span data-ttu-id="4590c-110">Для получения маршрутов с автостатическим интерфейсом используется следующий процесс: Диспетчер маршрутизаторов IP или IPX выдает запрос о том, что протокол маршрутизации обновляет сведения о маршрутизации для определенного интерфейса.</span><span class="sxs-lookup"><span data-stu-id="4590c-110">The process for obtaining autostatic routes is as follows: The IP or IPX router manager issues a request that a routing protocol update the routing information for a specific interface.</span></span> <span data-ttu-id="4590c-111">Затем результаты обновления преобразуются в статические маршруты.</span><span class="sxs-lookup"><span data-stu-id="4590c-111">The results of the update are then converted into static routes.</span></span> <span data-ttu-id="4590c-112">Обратите внимание, что только некоторые протоколы маршрутизации поддерживают запросы на обновления маршрутов для автостатического маршрута.</span><span class="sxs-lookup"><span data-stu-id="4590c-112">Note that only certain routing protocols support requests for autostatic route updates.</span></span>

 

 




