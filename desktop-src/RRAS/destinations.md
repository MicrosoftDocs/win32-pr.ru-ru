---
title: Места назначения
description: Назначение в таблице маршрутизации — это сетевая запись, представленная сетевым адресом и маской сети.
ms.assetid: 115d86e3-f933-4601-af10-abaab287b509
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49c0c758720824284147c2f35be004622157edb3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888515"
---
# <a name="destinations"></a><span data-ttu-id="3a626-103">Места назначения</span><span class="sxs-lookup"><span data-stu-id="3a626-103">Destinations</span></span>

<span data-ttu-id="3a626-104">Назначение в таблице маршрутизации — это сетевая запись, представленная сетевым адресом и маской сети.</span><span class="sxs-lookup"><span data-stu-id="3a626-104">A destination in the routing table is a network entry represented by a network address and a network mask.</span></span>

<span data-ttu-id="3a626-105">Конечная запись в таблице маршрутизации включает:</span><span class="sxs-lookup"><span data-stu-id="3a626-105">A destination entry in the routing table includes:</span></span>

-   <span data-ttu-id="3a626-106">Адрес, выраженный в виде сетевого адреса и маски сети.</span><span class="sxs-lookup"><span data-stu-id="3a626-106">The address, expressed as a network address and network mask.</span></span>
-   <span data-ttu-id="3a626-107">Список маршрутов к назначению.</span><span class="sxs-lookup"><span data-stu-id="3a626-107">A list of routes to the destination.</span></span>
-   <span data-ttu-id="3a626-108">Список областей непрозрачных указателей.</span><span class="sxs-lookup"><span data-stu-id="3a626-108">A list of opaque pointer slots.</span></span>
-   <span data-ttu-id="3a626-109">Представления, в которых это назначение является допустимым.</span><span class="sxs-lookup"><span data-stu-id="3a626-109">The views in which this destination is valid.</span></span> <span data-ttu-id="3a626-110">Назначение содержит структуру для каждого представления, которое содержит следующие сведения:</span><span class="sxs-lookup"><span data-stu-id="3a626-110">The destination contains a structure for each view that contains the following information:</span></span>
    -   <span data-ttu-id="3a626-111">Идентификатор представления.</span><span class="sxs-lookup"><span data-stu-id="3a626-111">An identifier for the view.</span></span>
    -   <span data-ttu-id="3a626-112">Указатель на оптимальный маршрут к назначению в этом представлении.</span><span class="sxs-lookup"><span data-stu-id="3a626-112">A pointer to the best route to the destination in this view.</span></span>
    -   <span data-ttu-id="3a626-113">Владелец лучшего маршрута в этом представлении.</span><span class="sxs-lookup"><span data-stu-id="3a626-113">The owner of the best route in this view.</span></span>
    -   <span data-ttu-id="3a626-114">Флаги, связанные с лучшим маршрутом в этом представлении.</span><span class="sxs-lookup"><span data-stu-id="3a626-114">Flags associated with the best route in this view.</span></span>
    -   <span data-ttu-id="3a626-115">Обработчик для всех маршрутов, которые находятся в состоянии удержания в этом представлении.</span><span class="sxs-lookup"><span data-stu-id="3a626-115">Handle to any routes that are in a hold-down state in this view.</span></span>

 

 




