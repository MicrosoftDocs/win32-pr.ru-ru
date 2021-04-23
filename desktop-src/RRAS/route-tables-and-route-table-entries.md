---
title: Таблицы маршрутов и записи таблицы маршрутов
description: Диспетчер таблиц маршрутизации обслуживает отдельные таблицы маршрутов для каждого семейства протоколов.
ms.assetid: 3848d93d-cc54-4a08-bd36-a9700cde6ce0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f118ec1d0a6f8fe4ef301654e139f217257c3a0b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105672005"
---
# <a name="route-tables-and-route-table-entries"></a><span data-ttu-id="230ae-103">Таблицы маршрутов и записи таблицы маршрутов</span><span class="sxs-lookup"><span data-stu-id="230ae-103">Route Tables and Route Table Entries</span></span>

<span data-ttu-id="230ae-104">**Windows Server 2003:** Этот API был заменен API [диспетчера таблиц маршрутизации версии 2](about-routing-table-manager-version-2.md) и не будет доступен за пределами Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="230ae-104">**Windows Server 2003:** This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="230ae-105">Новые приложения должны использовать API диспетчера таблиц маршрутизации версии 2.</span><span class="sxs-lookup"><span data-stu-id="230ae-105">New applications should use the Routing Table Manager Version 2 API.</span></span>

<span data-ttu-id="230ae-106">Диспетчер таблиц маршрутизации обслуживает отдельные таблицы маршрутов для каждого семейства протоколов.</span><span class="sxs-lookup"><span data-stu-id="230ae-106">The routing table manager maintains distinct route tables for each protocol family.</span></span> <span data-ttu-id="230ae-107">В настоящее время для семейств протоколов IP-маршрутизации и протокола IPX (Internet Packet Exchange) предусмотрена явная поддержка.</span><span class="sxs-lookup"><span data-stu-id="230ae-107">Currently, explicit support is provided for the Internet Protocol (IP) and Internet Packet Exchange (IPX) routing protocol families.</span></span> <span data-ttu-id="230ae-108">Независимо от семейства протоколов, каждая запись маршрута содержит следующие сведения.</span><span class="sxs-lookup"><span data-stu-id="230ae-108">Regardless of the protocol family, each route entry contains the following information:</span></span>

-   <span data-ttu-id="230ae-109">Целевая сеть.</span><span class="sxs-lookup"><span data-stu-id="230ae-109">Destination network.</span></span>
-   <span data-ttu-id="230ae-110">Идентификатор протокола, который добавил маршрут.</span><span class="sxs-lookup"><span data-stu-id="230ae-110">Identifier of the protocol that added the route.</span></span>
-   <span data-ttu-id="230ae-111">Индекс интерфейса, через который был получен маршрут.</span><span class="sxs-lookup"><span data-stu-id="230ae-111">Index of interface through which the route was obtained.</span></span> <span data-ttu-id="230ae-112">Это значение индекса является числовым значением, назначенным сетевому интерфейсу (аппаратному или виртуальному), который передает данные в сеть.</span><span class="sxs-lookup"><span data-stu-id="230ae-112">This index value is the numeric value assigned to a network interface (hardware-based or virtual) that transmits the data onto the network.</span></span> <span data-ttu-id="230ae-113">(Например, сетевой адаптер Ethernet или беспроводной адаптер 802.1 b.)</span><span class="sxs-lookup"><span data-stu-id="230ae-113">(For example, an Ethernet NIC, or a 802.1b wireless card.)</span></span>
-   <span data-ttu-id="230ae-114">Адрес маршрутизатора следующего прыжка.</span><span class="sxs-lookup"><span data-stu-id="230ae-114">Address of the next hop router.</span></span> <span data-ttu-id="230ae-115">Служба RRAS использует этот маршрутизатор для перенаправления пакетов в целевую сеть, если сеть не подключена напрямую.</span><span class="sxs-lookup"><span data-stu-id="230ae-115">RRAS uses this router to forward packets to the destination network if the network is not directly connected.</span></span>
-   <span data-ttu-id="230ae-116">Время создания или последнего обновления маршрута.</span><span class="sxs-lookup"><span data-stu-id="230ae-116">The time the route was created or last updated.</span></span>
-   <span data-ttu-id="230ae-117">Количество времени, в течение которого этот маршрут хранится в таблице маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="230ae-117">The amount of time this route is kept in the routing table.</span></span> <span data-ttu-id="230ae-118">Если это время истекает, а маршрут не обновлялся, диспетчер таблиц маршрутизации удаляет маршрут из таблицы.</span><span class="sxs-lookup"><span data-stu-id="230ae-118">If this amount of time elapses, and the route has not been updated, the routing table manager removes the route from the table.</span></span> <span data-ttu-id="230ae-119">В этом случае маршрут считается *устаревшим*.</span><span class="sxs-lookup"><span data-stu-id="230ae-119">In this case, the route is said to have *aged out*.</span></span>
-   <span data-ttu-id="230ae-120">Данные, относящиеся к семейству протоколов.</span><span class="sxs-lookup"><span data-stu-id="230ae-120">Data specific to the protocol family.</span></span> <span data-ttu-id="230ae-121">Эти данные прозрачны для RTMv1.</span><span class="sxs-lookup"><span data-stu-id="230ae-121">This data is transparent to RTMv1.</span></span> <span data-ttu-id="230ae-122">Однако если эти данные изменятся для маршрута, обозначенного как лучший маршрут, диспетчер таблиц маршрутизации отправляет уведомление об изменении маршрута.</span><span class="sxs-lookup"><span data-stu-id="230ae-122">However, if this data changes for a route designated as a "best route," the routing table manager sends out route-change notification.</span></span>
-   <span data-ttu-id="230ae-123">Данные, относящиеся к протоколу маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="230ae-123">Data specific to the routing protocol.</span></span> <span data-ttu-id="230ae-124">Эти данные полностью прозрачны для диспетчера таблиц маршрутизации. в этом случае изменения этих данных не приводят к уведомлению об изменении маршрута.</span><span class="sxs-lookup"><span data-stu-id="230ae-124">This data is completely transparent to the routing table manager, in that, changes to this data do not cause route change notification.</span></span>

<span data-ttu-id="230ae-125">Следующие значения совместно однозначно определяют маршрут в таблице маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="230ae-125">The following values taken together uniquely identify a route in the routing table:</span></span>

-   <span data-ttu-id="230ae-126">Целевая сеть</span><span class="sxs-lookup"><span data-stu-id="230ae-126">Destination network</span></span>
-   <span data-ttu-id="230ae-127">Идентификатор протокола</span><span class="sxs-lookup"><span data-stu-id="230ae-127">Protocol identifier</span></span>
-   <span data-ttu-id="230ae-128">Индекс интерфейса</span><span class="sxs-lookup"><span data-stu-id="230ae-128">Interface index</span></span>
-   <span data-ttu-id="230ae-129">Адрес маршрутизатора следующего прыжка</span><span class="sxs-lookup"><span data-stu-id="230ae-129">Address of next-hop router</span></span>

<span data-ttu-id="230ae-130">В общем случае диспетчер таблиц маршрутизации создает отдельные записи для маршрутов, которые различаются в любом из этих значений параметров.</span><span class="sxs-lookup"><span data-stu-id="230ae-130">In general, the routing table manager creates separate entries for routes that differ in any of these parameter values.</span></span> <span data-ttu-id="230ae-131">Однако для протоколов маршрутизации, которые не сохраняют более одной записи для каждой целевой сети, создается исключение.</span><span class="sxs-lookup"><span data-stu-id="230ae-131">However, an exception is made for routing protocols that do not keep more than one entry for each destination network.</span></span> <span data-ttu-id="230ae-132">Для этих протоколов диспетчер таблиц маршрутизации игнорирует различия в индексе интерфейса или адресе следующего прыжка.</span><span class="sxs-lookup"><span data-stu-id="230ae-132">For these protocols, the routing table manager ignores differences in interface index or next-hop address.</span></span> <span data-ttu-id="230ae-133">Примером такого протокола является реализация RRAS в первом кратчайшем пути (OSPF).</span><span class="sxs-lookup"><span data-stu-id="230ae-133">An example of such a protocol is the RRAS implementation of Open Shortest Path First (OSPF).</span></span>

 

 




