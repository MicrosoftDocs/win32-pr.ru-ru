---
title: Протокол маршрутизации
description: Протокол маршрутизации — это тип клиента, который регистрируется в диспетчере таблиц маршрутизации. Маршрутизаторы используют протоколы маршрутизации для обмена информацией о маршрутах к назначению.
ms.assetid: 957ec896-94e3-4bdb-801a-12b861460fff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e64d12912494d0d6c20f484eba588b47670a808
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067879"
---
# <a name="routing-protocol"></a><span data-ttu-id="2e8f2-104">Протокол маршрутизации</span><span class="sxs-lookup"><span data-stu-id="2e8f2-104">Routing Protocol</span></span>

<span data-ttu-id="2e8f2-105">Протокол маршрутизации — это тип клиента, который регистрируется в диспетчере таблиц маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="2e8f2-105">A routing protocol is a type of client that registers with the routing table manager.</span></span> <span data-ttu-id="2e8f2-106">Маршрутизаторы используют протоколы маршрутизации для обмена информацией о маршрутах к назначению.</span><span class="sxs-lookup"><span data-stu-id="2e8f2-106">Routers use routing protocols to exchange information regarding routes to a destination.</span></span>

<span data-ttu-id="2e8f2-107">Протоколы маршрутизации могут быть одноадресными или многоадресными.</span><span class="sxs-lookup"><span data-stu-id="2e8f2-107">Routing protocols are either unicast or multicast.</span></span> <span data-ttu-id="2e8f2-108">Протоколы маршрутизации объявляют маршруты к назначению.</span><span class="sxs-lookup"><span data-stu-id="2e8f2-108">Routing protocols advertise routes to a destination.</span></span>

<span data-ttu-id="2e8f2-109">Одноадресный маршрут к назначению используется протоколом одноадресной маршрутизации для пересылки одноадресных данных в это место назначения.</span><span class="sxs-lookup"><span data-stu-id="2e8f2-109">A unicast route to a destination is used by a unicast routing protocol to forward unicast data to that destination.</span></span> <span data-ttu-id="2e8f2-110">Примеры протоколов одноадресной маршрутизации: протокол RIP, открытия кратчайшего пути First (OSPF) и протокол BGP (BGP).</span><span class="sxs-lookup"><span data-stu-id="2e8f2-110">Examples of unicast routing protocols include: Routing Information Protocol (RIP), Open Shortest Path First (OSPF), and Border Gateway Protocol (BGP).</span></span>

<span data-ttu-id="2e8f2-111">Многоадресный маршрут к назначению используется некоторыми протоколами многоадресной маршрутизации для создания сведений, которые используются для пересылки многоадресных данных с узлов в конечной сети маршрута (называемой обратной переадресацией пути). Примеры протоколов многоадресной маршрутизации: многоадресная рассылка сначала по кратчайшему пути (МОСПФ), протоколу многоадресной маршрутизации (ДВМРП) расстояния и независимому протоколу многоадресной рассылки (PIM).</span><span class="sxs-lookup"><span data-stu-id="2e8f2-111">A multicast route to a destination is used by some multicast routing protocols to create the information that is used to forward multicast data from hosts on the destination network of the route (known as reverse path forwarding).Examples of multicast routing protocols include: Multicast Open Shortest Path First (MOSPF), Distance Vector Multicast Routing Protocol (DVMRP), and Protocol Independent Multicast (PIM).</span></span>

<span data-ttu-id="2e8f2-112">Диспетчер таблиц маршрутизации поддерживает несколько экземпляров одного протокола (например, реализации OSPF и стороннего стороннего OSPF), выполняющиеся на маршрутизаторе.</span><span class="sxs-lookup"><span data-stu-id="2e8f2-112">The routing table manager supports multiple instances of the same protocol (such as Microsoft's implementation of OSPF and a third-party OSPF) running on the router.</span></span> <span data-ttu-id="2e8f2-113">Это позволяет маршрутизаторам использовать различные возможности каждой версии.</span><span class="sxs-lookup"><span data-stu-id="2e8f2-113">This allows routers to use the different capabilities of each version.</span></span> <span data-ttu-id="2e8f2-114">Эти протоколы имеют разные идентификаторы протоколов.</span><span class="sxs-lookup"><span data-stu-id="2e8f2-114">These protocols have different protocol identifiers.</span></span>

<span data-ttu-id="2e8f2-115">Идентификаторы протоколов состоят из идентификатора поставщика и идентификатора, зависящего от протокола.</span><span class="sxs-lookup"><span data-stu-id="2e8f2-115">Protocol identifiers are comprised of a vendor identifier and a protocol-specific identifier.</span></span> <span data-ttu-id="2e8f2-116">Идентификатор конкретного протокола одинаков для различных реализаций протокола, таких как реализация OSPF в корпорации Майкрософт и реализация OSPF сторонними разработчиками.</span><span class="sxs-lookup"><span data-stu-id="2e8f2-116">The protocol-specific identifier is the same for different implementations of the protocol, such as Microsoft's implementation of OSPF and a third-party implementation of OSPF.</span></span> <span data-ttu-id="2e8f2-117">Только при объединении идентификаторов, зависящих от поставщика и протокола, существует уникальный идентификатор протокола маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="2e8f2-117">Only when the vendor and protocol-specific identifiers are combined is there a unique identifier for a routing protocol.</span></span>

<span data-ttu-id="2e8f2-118">Протокол с тем же идентификатором протокола (то есть один и тот же идентификатор поставщика и идентификатор, зависящий от протокола) может регистрироваться в диспетчере таблиц маршрутизации несколько раз.</span><span class="sxs-lookup"><span data-stu-id="2e8f2-118">A protocol with the same protocol identifier (that is, the same vendor identifier and protocol-specific identifier) can register with the routing table manager multiple times.</span></span> <span data-ttu-id="2e8f2-119">Каждый раз протокол регистрируется с использованием другого идентификатора экземпляра протокола.</span><span class="sxs-lookup"><span data-stu-id="2e8f2-119">Each time, the protocol registers using a different protocol instance identifier.</span></span> <span data-ttu-id="2e8f2-120">Например, реализация OSPF от конкретного поставщика может быть зарегистрирована как Vendor-OSPF-1 и Vendor-OSPF-2.</span><span class="sxs-lookup"><span data-stu-id="2e8f2-120">For example, an implementation of OSPF from a particular vendor can register as Vendor-OSPF-1 and Vendor-OSPF-2.</span></span> <span data-ttu-id="2e8f2-121">Это позволяет конкретной реализации протокола секционировать информацию, которая хранится в таблице маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="2e8f2-121">This enables a specific protocol implementation to partition the information that it keeps in the routing table.</span></span>

 

 




