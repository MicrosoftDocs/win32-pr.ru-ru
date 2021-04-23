---
title: Многоадресный клиент диспетчера групп
description: Клиент — это сущность, которая вызывает функцию МГМ, например протокол маршрутизации или административное приложение.
ms.assetid: 98d13b48-9f1d-4649-a5a3-03926c7facee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4a5f2a8ba63903c084547e3d04ea04474171651
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103779601"
---
# <a name="multicast-group-manager-client"></a><span data-ttu-id="baa06-103">Многоадресный клиент диспетчера групп</span><span class="sxs-lookup"><span data-stu-id="baa06-103">Multicast Group Manager Client</span></span>

<span data-ttu-id="baa06-104">Клиент — это сущность, которая вызывает функцию МГМ, например протокол маршрутизации или административное приложение.</span><span class="sxs-lookup"><span data-stu-id="baa06-104">A client is an entity that calls an MGM function, such as a routing protocol or an administrative application.</span></span>

<span data-ttu-id="baa06-105">API МГМ используется преимущественно протоколами многоадресной маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="baa06-105">The MGM API is used primarily by multicast routing protocols.</span></span> <span data-ttu-id="baa06-106">Разработчики протоколов многоадресной маршрутизации используют API МГМ для:</span><span class="sxs-lookup"><span data-stu-id="baa06-106">Developers of multicast routing protocols use the MGM API to:</span></span>

-   <span data-ttu-id="baa06-107">Ведение членства в группах</span><span class="sxs-lookup"><span data-stu-id="baa06-107">Maintain group membership</span></span>
-   <span data-ttu-id="baa06-108">Управление владением интерфейсом</span><span class="sxs-lookup"><span data-stu-id="baa06-108">Control interface ownership</span></span>
-   <span data-ttu-id="baa06-109">Получение уведомлений от диспетчера групп многоадресной рассылки относительно других протоколов многоадресной маршрутизации — запросов для многоадресных данных</span><span class="sxs-lookup"><span data-stu-id="baa06-109">Receive notifications from the multicast group manager regarding other multicast routing protocols' requests for multicast data</span></span>

<span data-ttu-id="baa06-110">Определенные административные приложения, которые должны отслеживать записи многоадресной пересылки (мфес), могут сделать это без добавления или удаления членства в группе.</span><span class="sxs-lookup"><span data-stu-id="baa06-110">Specific administrative applications that must monitor multicast forwarding entries (MFEs) can do so without adding or removing group membership.</span></span> <span data-ttu-id="baa06-111">Разработчики приложений с правами администратора используют определенные функции МГМ для просмотра информации в мфес.</span><span class="sxs-lookup"><span data-stu-id="baa06-111">Administrative application developers use specific MGM functions to review information in MFEs.</span></span>

> [!Note]  
> <span data-ttu-id="baa06-112">Протоколы многоадресной маршрутизации также имеют доступ к мфес.</span><span class="sxs-lookup"><span data-stu-id="baa06-112">Multicast routing protocols also access MFEs.</span></span>

 

<span data-ttu-id="baa06-113">МФЕ пересылает сведения, создаваемые диспетчером групп многоадресной рассылки на основе членства в группе.</span><span class="sxs-lookup"><span data-stu-id="baa06-113">An MFE is forwarding information that the multicast group manager creates based on group membership.</span></span> <span data-ttu-id="baa06-114">Мфес, получаемые из диспетчера групп многоадресной рассылки, могут предоставлять статистические данные.</span><span class="sxs-lookup"><span data-stu-id="baa06-114">The MFEs that are retrieved from the multicast group manager can provide statistical information.</span></span> <span data-ttu-id="baa06-115">После этого административное приложение может использовать эти сведения для определения соответствующих действий.</span><span class="sxs-lookup"><span data-stu-id="baa06-115">An administrative application can then use this information to determine the appropriate actions.</span></span> <span data-ttu-id="baa06-116">Например, административное приложение может выполнять действия, основанные на объеме пакетов в определенном интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="baa06-116">For example, an administrative application could perform actions that are based on the volume of packets on a specific interface.</span></span>

 

 




