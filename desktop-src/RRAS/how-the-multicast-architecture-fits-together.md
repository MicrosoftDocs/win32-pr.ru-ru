---
title: Совместное использование многоадресной архитектуры
description: В этом разделе описывается пример конфигурации и объясняется, как основные компоненты соединяются друг с другом.
ms.assetid: 1fa0b343-0276-402b-8c3d-5ca114ad43cf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dc82178568bac01e89eb0a4d6ea9222d45e7f5a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104258659"
---
# <a name="how-the-multicast-architecture-fits-together"></a><span data-ttu-id="edf60-103">Совместное использование многоадресной архитектуры</span><span class="sxs-lookup"><span data-stu-id="edf60-103">How the Multicast Architecture Fits Together</span></span>

<span data-ttu-id="edf60-104">В этом разделе описывается пример конфигурации и объясняется, как основные компоненты соединяются друг с другом.</span><span class="sxs-lookup"><span data-stu-id="edf60-104">This section describes a sample configuration and how the major components fit together.</span></span>

<span data-ttu-id="edf60-105">На следующем рисунке показана связь между различными компонентами маршрутизатора.</span><span class="sxs-lookup"><span data-stu-id="edf60-105">The following illustration shows the relationship between the various components of a router.</span></span>

![отношение между компонентами маршрутизатора Windows 2000](images/mrarch1.png)

<span data-ttu-id="edf60-107">Диспетчер групп многоадресной рассылки является частью службы RRAS, которая работает на сервере, работающем в качестве маршрутизатора.</span><span class="sxs-lookup"><span data-stu-id="edf60-107">The multicast group manager is a part of the RRAS service that runs on a server that is operating as a router.</span></span>

<span data-ttu-id="edf60-108">На указанном маршрутизаторе есть три протокола многоадресной маршрутизации (протокол 1, протокол 2, протокол 3), который работает на нем.</span><span class="sxs-lookup"><span data-stu-id="edf60-108">The router shown has three multicast routing protocols (Protocol 1, Protocol 2, Protocol 3) running on it.</span></span> <span data-ttu-id="edf60-109">Каждый протокол может владеть одним или несколькими интерфейсами (на этом рисунке протокол 1 владеет интерфейсом 1, протокол 2 владеет интерфейсом 2, а протокол 3 владеет интерфейсом 3).</span><span class="sxs-lookup"><span data-stu-id="edf60-109">Each protocol can own one or more interfaces (in this illustration, Protocol 1 owns Interface 1, Protocol 2 owns Interface 2, and Protocol 3 owns Interface 3).</span></span> <span data-ttu-id="edf60-110">Каждый интерфейс может принадлежать только одному протоколу маршрутизации (в дополнение к IGMP, что является особым случаем).</span><span class="sxs-lookup"><span data-stu-id="edf60-110">Each interface can be owned by only one routing protocol (in addition to IGMP, which is a special case).</span></span>

<span data-ttu-id="edf60-111">Диспетчер групп многоадресной рассылки выполняется на маршрутизаторе и координирует распределение сведений о группах между протоколами маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="edf60-111">The multicast group manager runs on the router and coordinates the distribution of group information between the routing protocols.</span></span>

<span data-ttu-id="edf60-112">На следующем рисунке показана связь между двумя маршрутизаторами в архитектуре многоадресной рассылки.</span><span class="sxs-lookup"><span data-stu-id="edf60-112">The following illustration shows the relationship between two routers in a multicast architecture.</span></span>

![отношение между двумя маршрутизаторами в архитектуре многоадресной рассылки](images/mrarch2.png)

<span data-ttu-id="edf60-114">На предыдущем рисунке маршрутизатор 2 отправляет многоадресное сообщение в сеть 2 в интерфейсе 3.</span><span class="sxs-lookup"><span data-stu-id="edf60-114">In the previous illustration, Router 2 sends a multicast message to Network 2 on Interface 3.</span></span> <span data-ttu-id="edf60-115">Маршрутизатор 1 получает многоадресное сообщение из сети 2 в интерфейсе 3.</span><span class="sxs-lookup"><span data-stu-id="edf60-115">Router 1 receives the multicast message from Network 2 on Interface 3.</span></span> <span data-ttu-id="edf60-116">На обоих маршрутизаторах протокол 3 владеет соответствующим интерфейсом 3.</span><span class="sxs-lookup"><span data-stu-id="edf60-116">On both routers, Protocol 3 owns the respective Interface 3.</span></span>

<span data-ttu-id="edf60-117">На следующем рисунке показан путь к сообщению, полученному от источника многоадресной рассылки (в группу многоадресной рассылки), для достижения узла, который присоединился к группе многоадресной рассылки.</span><span class="sxs-lookup"><span data-stu-id="edf60-117">The following illustration shows the path a message from a multicast source (to a multicast group) takes to reach the host that has joined the multicast group.</span></span> <span data-ttu-id="edf60-118">Маршрутизаторы на рисунке используют ту же конфигурацию, что и предыдущие иллюстрации; Однако сведения об интерфейсе и Протоколе не отображаются, чтобы не усложнять рисунок.</span><span class="sxs-lookup"><span data-stu-id="edf60-118">The routers in the illustration use the same configuration as previous illustrations; however, the interface and protocol details are not shown in order to keep the figure simple.</span></span>

![путь к сообщению от источника многоадресной рассылки на узел назначения](images/mrarch3.png)

<span data-ttu-id="edf60-120">В следующем сценарии описываются события, происходящие при присоединении узла к группе многоадресной рассылки.</span><span class="sxs-lookup"><span data-stu-id="edf60-120">The following scenario describes the events that take place when a host joins a multicast group.</span></span> <span data-ttu-id="edf60-121">Связи между различными сущностями см. на предыдущем рисунке.</span><span class="sxs-lookup"><span data-stu-id="edf60-121">Refer to the previous illustration for relationships between the various entities.</span></span>

1.  <span data-ttu-id="edf60-122">Узел 1 присоединяется к группе многоадресной рассылки G в сети 3.</span><span class="sxs-lookup"><span data-stu-id="edf60-122">Host 1 joins the multicast group G on Network 3.</span></span>
2.  <span data-ttu-id="edf60-123">Маршрутизатор 3 рассказывает об G через IGMP.</span><span class="sxs-lookup"><span data-stu-id="edf60-123">Router 3 learns about G via IGMP.</span></span>
3.  <span data-ttu-id="edf60-124">Диспетчер групп многоадресной рассылки на маршрутизаторе 3 уведомляет протокол 3 на маршрутизаторе 3 о новых получателях для G.</span><span class="sxs-lookup"><span data-stu-id="edf60-124">The multicast group manager on Router 3 notifies Protocol 3 on Router 3 that there are new receivers for G.</span></span>
4.  <span data-ttu-id="edf60-125">Протокол 3 на маршрутизаторе 3 затем уведомляет протокол 3 на маршрутизаторе 1 о G.</span><span class="sxs-lookup"><span data-stu-id="edf60-125">Protocol 3 on Router 3 then notifies Protocol 3 on Router 1 about G.</span></span>
5.  <span data-ttu-id="edf60-126">В свою очередь, протокол 3 на маршрутизаторе 1 уведомляет Диспетчер групп многоадресной рассылки на маршрутизаторе 1 о G.</span><span class="sxs-lookup"><span data-stu-id="edf60-126">In turn, Protocol 3 on Router 1 notifies the multicast group manager on Router 1 about G.</span></span>
6.  <span data-ttu-id="edf60-127">Диспетчер групп многоадресной рассылки на маршрутизаторе 1 затем уведомляет протокол 1 и протокол 2 о G.</span><span class="sxs-lookup"><span data-stu-id="edf60-127">The multicast group manager on Router 1 then notifies Protocol 1 and Protocol 2 about G.</span></span>
7.  <span data-ttu-id="edf60-128">Протокол 2 может сообщить маршрутизатору 2 о G, если этот протокол предназначен для этого.</span><span class="sxs-lookup"><span data-stu-id="edf60-128">Protocol 2 may inform Router 2 about G, if the protocol is designed to do so.</span></span>

<span data-ttu-id="edf60-129">В следующем сценарии описываются события, происходящие при отправке сообщения группе многоадресной рассылки.</span><span class="sxs-lookup"><span data-stu-id="edf60-129">The following scenario describes the events that take place when a message is sent to a multicast group.</span></span> <span data-ttu-id="edf60-130">Сведения о связях между различными сущностями см. на предыдущем рисунке.</span><span class="sxs-lookup"><span data-stu-id="edf60-130">Refer to the previous illustration for the relationships between the various entities.</span></span>

1.  <span data-ttu-id="edf60-131">Источник в сети 1 отправляет сообщение группе G.</span><span class="sxs-lookup"><span data-stu-id="edf60-131">A source on Network 1 sends a message to Group G.</span></span>
2.  <span data-ttu-id="edf60-132">Сообщение, отправленное из источника S, сначала поступает маршрутизатору 2, который затем пересылает его маршрутизатору 1 через интерфейс 2 (так как маршрутизатор 2 был уведомлен по протоколу 2 о том, что приемники находятся в подчиненном виде).</span><span class="sxs-lookup"><span data-stu-id="edf60-132">The message sent from Source S goes first to Router 2, which then forwards it to Router 1 using Interface 2 (since Router 2 has been informed by Protocol 2 that receivers are present downstream).</span></span>
3.  <span data-ttu-id="edf60-133">Маршрутизатор 1 перенаправляет сообщение маршрутизатору 3 (поскольку маршрутизатор 1 был уведомлен по протоколу 2 о том, что приемники находятся в подчиненном виде).</span><span class="sxs-lookup"><span data-stu-id="edf60-133">Router 1 forwards the message to Router 3 (since Router 1 has been informed by Protocol 2 that receivers are present downstream).</span></span>
4.  <span data-ttu-id="edf60-134">Маршрутизатор 3 перенаправляет сообщение в сеть 3 и, следовательно, поступает на узел 1.</span><span class="sxs-lookup"><span data-stu-id="edf60-134">Router 3 forwards the message to Network 3, and therefore it arrives at Host 1.</span></span>

<span data-ttu-id="edf60-135">Дополнительные сведения о взаимодействии протокола многоадресной маршрутизации см. в статье [RFC 2715](routing-protocols-request-for-comments.md), правила взаимодействия для протоколов многоадресной маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="edf60-135">For further information on multicast routing protocol interaction, see [RFC 2715](routing-protocols-request-for-comments.md), Interoperability Rules for Multicast Routing Protocols.</span></span>

 

 




