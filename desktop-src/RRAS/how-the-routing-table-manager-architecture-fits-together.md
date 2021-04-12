---
title: Совместное использование архитектуры диспетчера таблиц маршрутизации
description: На следующем рисунке показана связь между различными компонентами маршрутизатора.
ms.assetid: 862566ce-47c4-424a-84c2-99f4c92efcc0
keywords:
- RTM, архитектура
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc36c339ac89f01d5ba14c00857b3ced9c29414c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332752"
---
# <a name="how-the-routing-table-manager-architecture-fits-together"></a><span data-ttu-id="ef274-104">Совместное использование архитектуры диспетчера таблиц маршрутизации</span><span class="sxs-lookup"><span data-stu-id="ef274-104">How the Routing Table Manager Architecture Fits Together</span></span>

<span data-ttu-id="ef274-105">На следующем рисунке показана связь между различными компонентами маршрутизатора.</span><span class="sxs-lookup"><span data-stu-id="ef274-105">The following illustration shows the relationship between the different components of a router.</span></span>

![отношение между компонентами маршрутизатора](images/rtsrvarch.png)

<span data-ttu-id="ef274-107">При начальной загрузке маршрутизатора запускается служба диспетчера маршрутизаторов, а также один или несколько протоколов маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="ef274-107">When the router is bootstrapped, the router manager service is started, as well as one or more routing protocols.</span></span> <span data-ttu-id="ef274-108">Протоколы маршрутизации связаны с различными интерфейсами маршрутизатора.</span><span class="sxs-lookup"><span data-stu-id="ef274-108">Routing protocols are associated with the various interfaces on the router.</span></span> <span data-ttu-id="ef274-109">Диспетчер маршрутизаторов также запускает диспетчер таблиц маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="ef274-109">The router manager also starts the routing table manager.</span></span>

<span data-ttu-id="ef274-110">На следующем рисунке показана связь между клиентами и различными компонентами диспетчера таблиц маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="ef274-110">The following illustration shows the relationship between clients and the different components of the routing table manager.</span></span>

![отношение между клиентами и компонентами диспетчера таблиц маршрутизации](images/rtmentrel.png)

<span data-ttu-id="ef274-112">Диспетчер маршрутизаторов запускает один или несколько экземпляров диспетчера таблиц маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="ef274-112">The router manager starts one or more instances of the routing table manager.</span></span> <span data-ttu-id="ef274-113">При запуске нескольких экземпляров диспетчера таблиц маршрутизации маршрутизатор настроен на работу в качестве одного или нескольких виртуальных маршрутизаторов.</span><span class="sxs-lookup"><span data-stu-id="ef274-113">When multiple instances of the routing table manager are started, the router has been configured to act as one or more virtual routers.</span></span> <span data-ttu-id="ef274-114">Каждый экземпляр диспетчера таблиц маршрутизации владеет одним или несколькими интерфейсами. Каждый интерфейс может принадлежать только одному экземпляру диспетчера таблиц маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="ef274-114">Each instance of the routing table manager owns one or more interfaces; each interface can only be owned by one instance of the routing table manager.</span></span>

<span data-ttu-id="ef274-115">Каждый экземпляр диспетчера таблиц маршрутизации не зависит от других. Обмен данными между экземплярами не осуществляется.</span><span class="sxs-lookup"><span data-stu-id="ef274-115">Each instance of the routing table manager is independent from the others; no information is exchanged between the instances.</span></span>

<span data-ttu-id="ef274-116">Каждый экземпляр диспетчера таблиц маршрутизации содержит одну или несколько таблиц маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="ef274-116">Each instance of the routing table manager contains one or more routing tables.</span></span> <span data-ttu-id="ef274-117">Каждая таблица маршрутизации связана с семейством адресов.</span><span class="sxs-lookup"><span data-stu-id="ef274-117">Each routing table is associated with an address family.</span></span>

<span data-ttu-id="ef274-118">Каждая таблица маршрутизации содержит одно или несколько представлений.</span><span class="sxs-lookup"><span data-stu-id="ef274-118">Each routing table contains one or more views.</span></span> <span data-ttu-id="ef274-119">В этом примере таблица маршрутизации отображается с одноадресным и многоадресным представлением.</span><span class="sxs-lookup"><span data-stu-id="ef274-119">In this example, the routing table is shown with a unicast and multicast view.</span></span> <span data-ttu-id="ef274-120">Каждое представление является подмножеством таблицы маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="ef274-120">Each view is a subset of the routing table.</span></span>

<span data-ttu-id="ef274-121">На следующем рисунке показана связь между клиентами и несколькими экземплярами диспетчера таблиц маршрутизации, таблиц маршрутизации и представлений.</span><span class="sxs-lookup"><span data-stu-id="ef274-121">The following illustration shows the relationship between clients and multiple instances of the routing table manager, routing tables, and views.</span></span>

![Клиенты отношений, диспетчер таблиц маршрутизации, таблицы маршрутизации, представления](images/multrtabrel.png)

<span data-ttu-id="ef274-123">Экземпляр клиента может быть зарегистрирован несколько раз с экземпляром диспетчера таблиц маршрутизации — один раз для каждого семейства адресов.</span><span class="sxs-lookup"><span data-stu-id="ef274-123">An instance of the client can register multiple times with an instance of the routing table manager — once per address family.</span></span> <span data-ttu-id="ef274-124">Клиент может зарегистрироваться в каждом экземпляре диспетчера таблиц маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="ef274-124">A client can register with each instance of the routing table manager.</span></span>

<span data-ttu-id="ef274-125">На следующем рисунке показано, как связаны записи таблицы маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="ef274-125">The following illustration shows how the routing table entries are related.</span></span> <span data-ttu-id="ef274-126">Дополнительные сведения о записях таблицы маршрутизации см. в разделе [Маршрутизация записей таблицы маршрутизации](routing-table-entries.md).</span><span class="sxs-lookup"><span data-stu-id="ef274-126">For more information on routing table entries, see [Routing Table Entries](routing-table-entries.md).</span></span>

![связь между записями таблицы маршрутизации](images/nexthop.png)

<span data-ttu-id="ef274-128">Таблица маршрутизации содержит назначения.</span><span class="sxs-lookup"><span data-stu-id="ef274-128">The routing table contains destinations.</span></span> <span data-ttu-id="ef274-129">Каждое назначение связано с одним или несколькими маршрутами.</span><span class="sxs-lookup"><span data-stu-id="ef274-129">Each destination is related to one or more routes.</span></span> <span data-ttu-id="ef274-130">Каждый маршрут имеет ноль, один или несколько указателей на следующие прыжки, связанные с маршрутом.</span><span class="sxs-lookup"><span data-stu-id="ef274-130">Each route has zero, one, or more pointers to next hops that are associated with the route.</span></span> <span data-ttu-id="ef274-131">Каждый указатель ссылается на фактический следующий прыжок в списке следующих прыжков.</span><span class="sxs-lookup"><span data-stu-id="ef274-131">Each pointer refers to the actual next hop in the list of next hops.</span></span> <span data-ttu-id="ef274-132">Каждый клиент, который регистрируется в диспетчере таблиц маршрутизации, создает список следующих прыжков, которыми владеет клиент.</span><span class="sxs-lookup"><span data-stu-id="ef274-132">Each client that registers with the routing table manager creates a list of next hops that the client owns.</span></span>

<span data-ttu-id="ef274-133">Маршруты могут содержать только указатели на список следующего прыжка, связанный с клиентом, которому принадлежит маршрут.</span><span class="sxs-lookup"><span data-stu-id="ef274-133">Routes can only contain pointers to the next-hop list associated with the client that owns the route.</span></span>

 

 




