---
title: Диспетчер таблиц маршрутизации
description: Диспетчер таблиц маршрутизации является центральным репозиторием сведений о маршрутизации для всех протоколов маршрутизации, которые работают в службе маршрутизации и удаленного доступа (RRAS).
ms.assetid: 7b01704e-c1fb-40e3-89cf-1206fdf9fd75
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98094eb34c8575e0c24854813fc7458c98749568
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105672021"
---
# <a name="routing-table-manager"></a><span data-ttu-id="9adc5-103">Диспетчер таблиц маршрутизации</span><span class="sxs-lookup"><span data-stu-id="9adc5-103">Routing Table Manager</span></span>

<span data-ttu-id="9adc5-104">Диспетчер таблиц маршрутизации является центральным репозиторием сведений о маршрутизации для всех протоколов маршрутизации, которые работают в службе маршрутизации и удаленного доступа (RRAS).</span><span class="sxs-lookup"><span data-stu-id="9adc5-104">The routing table manager is the central repository of routing information for all routing protocols that operate under the Routing and Remote Access Service (RRAS).</span></span> <span data-ttu-id="9adc5-105">Он уведомляет клиентов, когда произошли изменения, и позволяет клиентам обмениваться конфиденциальной информацией.</span><span class="sxs-lookup"><span data-stu-id="9adc5-105">It notifies clients when changes have occurred, and allows clients to exchange private information.</span></span>

<span data-ttu-id="9adc5-106">Диспетчер таблиц маршрутизации предоставляет сведения о маршрутизации всем заинтересованным клиентам, таким как протоколы маршрутизации, программы управления и программы наблюдения.</span><span class="sxs-lookup"><span data-stu-id="9adc5-106">The routing table manager provides routing information to all interested clients, such as routing protocols, management programs, and monitoring programs.</span></span> <span data-ttu-id="9adc5-107">Диспетчер таблиц маршрутизации также определяет оптимальный маршрут к каждой целевой сети, известной протоколам маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="9adc5-107">The routing table manager also determines the best route to each destination network that is known to the routing protocols.</span></span> <span data-ttu-id="9adc5-108">Диспетчер таблиц маршрутизации определяет этот маршрут на основе приоритетов протоколов маршрутизации и метрик, связанных с маршрутами.</span><span class="sxs-lookup"><span data-stu-id="9adc5-108">The routing table manager determines this route based on routing protocol priorities and on the metrics associated with the routes.</span></span> <span data-ttu-id="9adc5-109">Пользователь, который управляет маршрутизатором, может настроить приоритеты протоколов маршрутизации с помощью консоли управления RRAS.</span><span class="sxs-lookup"><span data-stu-id="9adc5-109">The person administering the router can configure routing protocol priorities using the RRAS management console.</span></span>

<span data-ttu-id="9adc5-110">Диспетчер таблиц маршрутизации передает сведения о наилучшем маршруте серверам пересылки (по одному на каждое семейство адресов или по одному на интерфейс) и всем заинтересованным клиентам.</span><span class="sxs-lookup"><span data-stu-id="9adc5-110">The routing table manager passes the best-route information to the forwarders (one per address family, or one per interface) and to all interested clients.</span></span>

<span data-ttu-id="9adc5-111">Каждый клиент регистрируется в диспетчере таблиц маршрутизации, а в Return получает маркер, используемый клиентом для добавления или удаления маршрутов.</span><span class="sxs-lookup"><span data-stu-id="9adc5-111">Each client registers with the routing table manager, and in return receives a handle that the client uses to add or delete routes.</span></span> <span data-ttu-id="9adc5-112">Клиенты могут получать сведения, хранящиеся в таблице маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="9adc5-112">Clients can retrieve information stored in the routing table.</span></span> <span data-ttu-id="9adc5-113">Кроме того, клиенты могут зарегистрироваться в диспетчере таблиц маршрутизации, чтобы получить уведомления об изменениях лучшего маршрута к назначению.</span><span class="sxs-lookup"><span data-stu-id="9adc5-113">Additionally, clients can register with the routing table manager to receive notification of changes to the best route to a destination.</span></span>

 

 




