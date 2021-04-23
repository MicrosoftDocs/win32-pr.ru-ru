---
title: Извлечение сведений
description: RTMv2 позволяет клиенту получать информацию, на которую ссылается данный обработчик, с помощью функций Ртмжетентитинфо, Ртмжетдестинфо, Ртмжетраутеинфо и Ртмжетнекссопинфо.
ms.assetid: a3fc2020-eac4-40a1-9a6e-6eaa2bcc582c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 058a87c9463011aec55b0c6c8c0574ff1e013f23
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104252869"
---
# <a name="retrieving-information"></a><span data-ttu-id="c1b76-103">Извлечение сведений</span><span class="sxs-lookup"><span data-stu-id="c1b76-103">Retrieving Information</span></span>

<span data-ttu-id="c1b76-104">RTMv2 позволяет клиенту получать информацию, на которую ссылается данный обработчик, с помощью функций [**ртмжетентитинфо**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetentityinfo), [**ртмжетдестинфо**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetdestinfo), [**ртмжетраутеинфо**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetrouteinfo)и [**ртмжетнекссопинфо**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetnexthopinfo) .</span><span class="sxs-lookup"><span data-stu-id="c1b76-104">RTMv2 allows a client to retrieve the information referred to by a given handle using the [**RtmGetEntityInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetentityinfo), [**RtmGetDestInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetdestinfo), [**RtmGetRouteInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetrouteinfo), and [**RtmGetNextHopInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetnexthopinfo) functions.</span></span>

<span data-ttu-id="c1b76-105">Эти вызовы функций имеют соответствующие функции ([**ртмрелеасинтитинфо**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaseentityinfo), [**ртмрелеаседестинфо**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasedestinfo), [**ртмрелеасераутеинфо**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaserouteinfo), [**ртмрелеасенекссопинфо**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasenexthopinfo)) для освобождения дескрипторов, связанных со структурой данных, возвращаемой диспетчером таблиц маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="c1b76-105">These function calls have corresponding functions ([**RtmReleaseEntityInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaseentityinfo), [**RtmReleaseDestInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasedestinfo), [**RtmReleaseRouteInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaserouteinfo), [**RtmReleaseNextHopInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasenexthopinfo)) to release the handles associated with the information structure returned by the routing table manager.</span></span>

> [!Note]  
> <span data-ttu-id="c1b76-106">Сведения для клиентов доступны только в текущем экземпляре и семействе адресов.</span><span class="sxs-lookup"><span data-stu-id="c1b76-106">Information for clients is available only in the current instance and address family.</span></span>

 

<span data-ttu-id="c1b76-107">Пример кода, демонстрирующий использование этих функций, см. [в разделе Поиск лучшего маршрута](search-for-the-best-route.md).</span><span class="sxs-lookup"><span data-stu-id="c1b76-107">For sample code that shows how to use these functions, see [Search For the Best Route](search-for-the-best-route.md).</span></span>

## <a name="using-rtmgetexactmatchroute-and-rtmgetexactmatchdestination"></a><span data-ttu-id="c1b76-108">Использование Ртмжетексактматчрауте и Ртмжетексактматчдестинатион</span><span class="sxs-lookup"><span data-stu-id="c1b76-108">Using RtmGetExactMatchRoute and RtmGetExactMatchDestination</span></span>

<span data-ttu-id="c1b76-109">Функции [**ртмжетексактматчрауте**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetexactmatchroute) и [**ртмжетексактматчдестинатион**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetexactmatchdestination) используются клиентами для поиска конкретного маршрута или назначения.</span><span class="sxs-lookup"><span data-stu-id="c1b76-109">The [**RtmGetExactMatchRoute**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetexactmatchroute) and [**RtmGetExactMatchDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetexactmatchdestination) functions are used by clients to find a specific route or destination.</span></span> <span data-ttu-id="c1b76-110">Эти функции экономируют время, выполняя операции сравнения для клиента.</span><span class="sxs-lookup"><span data-stu-id="c1b76-110">These functions save time by doing the comparison work for the client.</span></span>

<span data-ttu-id="c1b76-111">Например, когда RIP обновляет маршрут, RIP должен хранить старые сведения о метриках.</span><span class="sxs-lookup"><span data-stu-id="c1b76-111">For example, when RIP updates a route, RIP must retain the old metric information.</span></span> <span data-ttu-id="c1b76-112">RIP ищет маршрут и сведения о нем.</span><span class="sxs-lookup"><span data-stu-id="c1b76-112">RIP searches for the route and its information.</span></span> <span data-ttu-id="c1b76-113">Затем RIP может скопировать информацию и обновить маршрут.</span><span class="sxs-lookup"><span data-stu-id="c1b76-113">Then RIP can copy the information and update the route.</span></span>

## <a name="using-rtmgetmostspecificdestination"></a><span data-ttu-id="c1b76-114">Использование РтмжетмостспеЦификдестинатион</span><span class="sxs-lookup"><span data-stu-id="c1b76-114">Using RtmGetMostSpecificDestination</span></span>

<span data-ttu-id="c1b76-115">Функция [**ртмжетмостспеЦификдестинатион**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetmostspecificdestination) используется для поиска места назначения, которое лучше соответствует указанному сетевому префиксу.</span><span class="sxs-lookup"><span data-stu-id="c1b76-115">The [**RtmGetMostSpecificDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetmostspecificdestination) function is used to locate the destination that best matches the specified network prefix.</span></span>

<span data-ttu-id="c1b76-116">Например, Диспетчер групп многоадресной рассылки использует эту функцию для выполнения проверки с обратным путем перенаправления (РПФ) на одном адресе.</span><span class="sxs-lookup"><span data-stu-id="c1b76-116">For example, the multicast group manager uses this function to perform a reverse-path-forwarding (RPF) check on a single address.</span></span> <span data-ttu-id="c1b76-117">Функцию также можно использовать для поиска локального следующего прыжка для данного удаленного следующего прыжка.</span><span class="sxs-lookup"><span data-stu-id="c1b76-117">The function can also be used to find the local next hop for a given remote next hop.</span></span>

<span data-ttu-id="c1b76-118">Пример кода, демонстрирующий использование этих функций, см. в разделе [Поиск маршрутов с помощью дерева префиксов](search-for-routes-using-rtmgetmostspecificdestination-and-rtmgetlessspecificdestination.md) и [Поиск лучшего маршрута](search-for-the-best-route.md).</span><span class="sxs-lookup"><span data-stu-id="c1b76-118">For sample code that shows how to use these functions, see [Search for Routes Using a Prefix Tree](search-for-routes-using-rtmgetmostspecificdestination-and-rtmgetlessspecificdestination.md) and [Search For the Best Route](search-for-the-best-route.md).</span></span>

## <a name="using-rtmgetlessspecificdestination"></a><span data-ttu-id="c1b76-119">Использование РтмжетлессспеЦификдестинатион</span><span class="sxs-lookup"><span data-stu-id="c1b76-119">Using RtmGetLessSpecificDestination</span></span>

<span data-ttu-id="c1b76-120">Функция [**ртмжетлессспеЦификдестинатион**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetlessspecificdestination) используется для поиска назначения, которое является наиболее подходящей для указанного префикса сети.</span><span class="sxs-lookup"><span data-stu-id="c1b76-120">The [**RtmGetLessSpecificDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetlessspecificdestination) function is used to locate the destination that is the next-best match for the specified network prefix.</span></span> <span data-ttu-id="c1b76-121">Эту функцию можно вызвать многократно, чтобы вернуть следующее повторяющееся совпадение с меньшим соответствием, пока не будут найдены другие назначения.</span><span class="sxs-lookup"><span data-stu-id="c1b76-121">This function can be called repeatedly to return the next successive less-specific match, until no more destinations match.</span></span>

<span data-ttu-id="c1b76-122">Эта функция вызывается после вызова [**ртмжетмостспеЦификдестинатион**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetmostspecificdestination).</span><span class="sxs-lookup"><span data-stu-id="c1b76-122">This function is called after a call to [**RtmGetMostSpecificDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetmostspecificdestination).</span></span>

<span data-ttu-id="c1b76-123">Пример кода, демонстрирующий использование этих функций, см. в разделе [Поиск маршрутов с помощью дерева префиксов](search-for-routes-using-rtmgetmostspecificdestination-and-rtmgetlessspecificdestination.md).</span><span class="sxs-lookup"><span data-stu-id="c1b76-123">For sample code that illustrates how to use these functions, see [Search for Routes Using a Prefix Tree](search-for-routes-using-rtmgetmostspecificdestination-and-rtmgetlessspecificdestination.md).</span></span>

## <a name="using-rtmisbestroute"></a><span data-ttu-id="c1b76-124">Использование Ртмисбестрауте</span><span class="sxs-lookup"><span data-stu-id="c1b76-124">Using RtmIsBestRoute</span></span>

<span data-ttu-id="c1b76-125">Функция [**ртмисбестрауте**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmisbestroute) позволяет клиенту быстро определить, является ли конкретный маршрут лучшим маршрутом к назначению.</span><span class="sxs-lookup"><span data-stu-id="c1b76-125">The [**RtmIsBestRoute**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmisbestroute) function enables a client to quickly find out whether or not a particular route is the best route to a destination.</span></span> <span data-ttu-id="c1b76-126">Например, клиенту может потребоваться хранить определенный маршрут только в том случае, если это лучший маршрут.</span><span class="sxs-lookup"><span data-stu-id="c1b76-126">For example, a client may need to store a particular route only if it is the best route.</span></span> <span data-ttu-id="c1b76-127">Таким образом, клиент может вызвать эту функцию вместо перечисления всех маршрутов и выполнения сравнения.</span><span class="sxs-lookup"><span data-stu-id="c1b76-127">Therefore, the client can call this function, instead of enumerating all routes and making the comparison itself.</span></span>

 

 




