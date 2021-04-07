---
title: Публикация в контейнере системы домена
description: Системный контейнер раздела домена содержит операционные сведения для каждого домена.
ms.assetid: 18bb3409-774e-42d9-8f27-6c582d74ca86
ms.tgt_platform: multiple
keywords:
- Публикация в контейнере Active Directory системы домена
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdf7d1febd91e3540c7bc2002a36d33346820344
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103887627"
---
# <a name="publishing-in-a-domain-system-container"></a><span data-ttu-id="cb96f-104">Публикация в контейнере системы домена</span><span class="sxs-lookup"><span data-stu-id="cb96f-104">Publishing in a Domain System Container</span></span>

<span data-ttu-id="cb96f-105">Системный контейнер раздела домена содержит операционные сведения для каждого домена.</span><span class="sxs-lookup"><span data-stu-id="cb96f-105">The System container of a domain partition holds per-domain operational information.</span></span> <span data-ttu-id="cb96f-106">К ним относятся локальная политика безопасности по умолчанию, отслеживание ссылок на файлы, сетевые собрания и контейнеры для точек подключения Windows Sockets Registration and Resolution (РНР) и службы имен RPC (Рпкнс).</span><span class="sxs-lookup"><span data-stu-id="cb96f-106">This includes the default local security policy, file link tracking, network meetings, and containers for Windows Sockets registration and resolution (RnR) and RPC name service (RpcNs) connection points.</span></span> <span data-ttu-id="cb96f-107">Контейнер системы по умолчанию скрыт и предоставляет удобное место для хранения объектов, представляющих интерес для администраторов, но не для конечных пользователей.</span><span class="sxs-lookup"><span data-stu-id="cb96f-107">The system container is hidden, by default, and provides a convenient place for storing objects that are of interest to administrators, but not to end users.</span></span>

<span data-ttu-id="cb96f-108">Службы, которые не привязаны к одному узлу, могут создавать свои запрашивая в системном контейнере раздела домена.</span><span class="sxs-lookup"><span data-stu-id="cb96f-108">Services that are not tied to a single host may want to create their SCPs under the System container of a domain partition.</span></span> <span data-ttu-id="cb96f-109">Эта альтернатива может быть полезна для служб с репликами, установленными на нескольких узлах, Каждая реплика предоставляет клиентам одинаковые службы на всем домене.</span><span class="sxs-lookup"><span data-stu-id="cb96f-109">This alternative can be useful for services with replicas installed on multiple hosts, each replica providing identical services to clients throughout the domain.</span></span> <span data-ttu-id="cb96f-110">Она позволяет сгруппировать все объекты для реплицированной службы в одном контейнере.</span><span class="sxs-lookup"><span data-stu-id="cb96f-110">It enables you to group all the objects for the replicated service under a single container.</span></span>

<span data-ttu-id="cb96f-111">Службы, создающие зависящие от службы объекты в контейнере System, должны выполнять следующие действия:</span><span class="sxs-lookup"><span data-stu-id="cb96f-111">Services that create service-specific objects in the System container must do the following:</span></span>

1.  <span data-ttu-id="cb96f-112">Создайте вложенный контейнер **контейнера** класса объекта как непосредственный дочерний элемент контейнера System.</span><span class="sxs-lookup"><span data-stu-id="cb96f-112">Create a sub-container of object class **container** as an immediate child of the System container.</span></span> <span data-ttu-id="cb96f-113">Присвойте этому подконтейнеру имя, которое четко идентифицирует его как отношение к службе.</span><span class="sxs-lookup"><span data-stu-id="cb96f-113">Give this sub-container a name that clearly identifies it as pertaining to the service.</span></span>
2.  <span data-ttu-id="cb96f-114">Создайте объекты, связанные со службой, в этом подконтейнере.</span><span class="sxs-lookup"><span data-stu-id="cb96f-114">Create the service-related objects in this sub-container.</span></span> <span data-ttu-id="cb96f-115">Например, NetMeeting использует контейнер meetings для публикации объектов сетевого собрания.</span><span class="sxs-lookup"><span data-stu-id="cb96f-115">For example, NetMeeting uses the Meetings container to publish network meeting objects.</span></span>

<span data-ttu-id="cb96f-116">Поставщик с несколькими продуктами может использовать аналогичную стратегию группирования объектов, связанных со службами, для всех своих продуктов.</span><span class="sxs-lookup"><span data-stu-id="cb96f-116">A vendor with multiple products can use a similar strategy to group service-related objects for all of its products.</span></span> <span data-ttu-id="cb96f-117">В этом случае можно создать объект- **контейнер** с именем, которое ясно идентифицирует поставщика. Затем создайте объекты **контейнера** для каждой службы в качестве дочерних элементов контейнера поставщика.</span><span class="sxs-lookup"><span data-stu-id="cb96f-117">In this case, you could create a **container** object with a name that clearly identifies the vendor; then create **container** objects for each service as children of the vendor container.</span></span> <span data-ttu-id="cb96f-118">Создайте контейнер для конкретного поставщика в качестве дочернего для системного контейнера.</span><span class="sxs-lookup"><span data-stu-id="cb96f-118">Create the vendor-specific container as a child of the System container.</span></span>

 

 




