---
title: Использование непрозрачных указателей
description: Клиенты часто должны хранить дополнительные сведения о назначениях, относящиеся к клиенту.
ms.assetid: e96805b0-680f-411c-a02c-2c3fda7276ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9893b3a8b8e8a69ab78f33156efbe872b86d83ca
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888768"
---
# <a name="using-opaque-pointers"></a><span data-ttu-id="bb769-103">Использование непрозрачных указателей</span><span class="sxs-lookup"><span data-stu-id="bb769-103">Using Opaque Pointers</span></span>

<span data-ttu-id="bb769-104">Клиенты часто должны хранить дополнительные сведения о назначениях, относящиеся к клиенту.</span><span class="sxs-lookup"><span data-stu-id="bb769-104">Clients often must store additional, client-specific information about destinations.</span></span> <span data-ttu-id="bb769-105">Диспетчер таблиц маршрутизации позволяет клиентам хранить эти сведения в целевых структурах в таблице маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="bb769-105">The routing table manager enables clients to store this information in destination structures in the routing table.</span></span> <span data-ttu-id="bb769-106">Информация хранится и извлекается с помощью *непрозрачных указателей*.</span><span class="sxs-lookup"><span data-stu-id="bb769-106">The information is stored and retrieved by using *opaque pointers*.</span></span> <span data-ttu-id="bb769-107">Хранимая информация является закрытой и доступна только клиенту, владеющему непрозрачным указателем.</span><span class="sxs-lookup"><span data-stu-id="bb769-107">The information stored is private, and accessible only to the client that owns the opaque pointer.</span></span>

<span data-ttu-id="bb769-108">Например, Диспетчер групп многоадресной рассылки хранит список записей многоадресной пересылки, зависящих от конкретного назначения.</span><span class="sxs-lookup"><span data-stu-id="bb769-108">For example, the multicast group manager keeps a list of multicast forwarding entries that are dependent on a particular destination.</span></span> <span data-ttu-id="bb769-109">Диспетчер групп многоадресной рассылки использует непрозрачный указатель в этом месте назначения.</span><span class="sxs-lookup"><span data-stu-id="bb769-109">The multicast group manager uses an opaque pointer in that destination.</span></span> <span data-ttu-id="bb769-110">В другом примере протокол маршрутизации, объявляющий определенное назначение, может обеспечить сведения, связанные с его собственным объявлением маршрута назначения, с помощью непрозрачного указателя, даже если он не владеет лучшим маршрутом.</span><span class="sxs-lookup"><span data-stu-id="bb769-110">In another example, a routing protocol that advertises a particular destination can keep information related to its own route advertisement of the destination using an opaque pointer, even though it does not own the best route.</span></span>

<span data-ttu-id="bb769-111">Число непрозрачных указателей ограничено; Эти указатели выделяются клиентам на основе первого поступления.</span><span class="sxs-lookup"><span data-stu-id="bb769-111">The number of opaque pointers is limited; these pointers are allocated to clients on a first-come, first-served basis.</span></span> <span data-ttu-id="bb769-112">Администратор маршрутизатора должен выделить правильное число указателей во время настройки маршрутизатора. Поэтому протоколы маршрутизации и другие клиенты должны документировать использование непрозрачных указателей.</span><span class="sxs-lookup"><span data-stu-id="bb769-112">The router administrator must allocate the correct number of pointers during the router configuration; therefore, routing protocols and other clients must document their use of opaque pointers.</span></span>

 

 




