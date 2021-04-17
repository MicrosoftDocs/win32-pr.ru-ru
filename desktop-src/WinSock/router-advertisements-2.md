---
description: Содержимое объявлений маршрутизаторов IPv6 автоматически извлекается из опубликованных маршрутов в таблице маршрутизации. Неопубликованные маршруты используются для маршрутизации, но игнорируются при создании объявлений маршрутизатора.
ms.assetid: 27b735db-4e87-497b-b39c-e464cf44f09e
title: Объявления маршрутизаторов IPv6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77a75b31a988595cba85d23dbafc1bd93ffff4ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105702092"
---
# <a name="ipv6-router-advertisements"></a><span data-ttu-id="b01aa-104">Объявления маршрутизаторов IPv6</span><span class="sxs-lookup"><span data-stu-id="b01aa-104">IPv6 Router Advertisements</span></span>

<span data-ttu-id="b01aa-105">Содержимое объявлений маршрутизаторов IPv6 автоматически извлекается из опубликованных маршрутов в таблице маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="b01aa-105">The content of IPv6 router advertisements is automatically derived from the published routes in the routing table.</span></span> <span data-ttu-id="b01aa-106">Неопубликованные маршруты используются для маршрутизации, но игнорируются при создании объявлений маршрутизатора.</span><span class="sxs-lookup"><span data-stu-id="b01aa-106">Nonpublished routes are used for routing but are ignored when constructing router advertisements.</span></span>

<span data-ttu-id="b01aa-107">Объявления маршрутизатора для IPv6 всегда содержат исходный параметр адреса канального уровня и параметр MTU.</span><span class="sxs-lookup"><span data-stu-id="b01aa-107">Router advertisements for IPv6 always contain a source link-layer address option and an MTU option.</span></span> <span data-ttu-id="b01aa-108">Значение параметра MTU берется из MTU текущей ссылки на интерфейс отправки.</span><span class="sxs-lookup"><span data-stu-id="b01aa-108">The value for the MTU option is taken from the sending interface's current link MTU.</span></span> <span data-ttu-id="b01aa-109">Это значение можно изменить с помощью команды IPv6 ИФК MTU.</span><span class="sxs-lookup"><span data-stu-id="b01aa-109">This value can be changed with the ipv6 ifc mtu command.</span></span>

<span data-ttu-id="b01aa-110">При наличии опубликованного маршрута по умолчанию объявление маршрутизатора имеет ненулевое время существования маршрутизатора.</span><span class="sxs-lookup"><span data-stu-id="b01aa-110">The router advertisement only has a nonzero router lifetime if there is a published default route.</span></span> <span data-ttu-id="b01aa-111">Маршрут по умолчанию — это маршрут для префикса нулевой длины.</span><span class="sxs-lookup"><span data-stu-id="b01aa-111">A default route is a route for the zero-length prefix.</span></span>

<span data-ttu-id="b01aa-112">Опубликованные маршруты по каналу приводят к параметрам сведений о префиксах в объявлениях маршрутизатора.</span><span class="sxs-lookup"><span data-stu-id="b01aa-112">Published on-link routes result in prefix information options in router advertisements.</span></span> <span data-ttu-id="b01aa-113">Если префикс ссылки содержит 64 бит, параметр сведений о префиксе включает и набор битов, и, и узлы, получающие его, будут настраивать адреса.</span><span class="sxs-lookup"><span data-stu-id="b01aa-113">If the on-link prefix has 64 bits, the prefix information option has both the L and A bits set and hosts receiving it will autoconfigure addresses.</span></span>

<span data-ttu-id="b01aa-114">Интерфейс, отправляющий объявления маршрутизатора, также автоматически настраивает адреса для себя на основе передаваемых параметров сведений о префиксе.</span><span class="sxs-lookup"><span data-stu-id="b01aa-114">An interface that sends router advertisements will also autoconfigure addresses for itself based on the prefix information options that it sends.</span></span>

<span data-ttu-id="b01aa-115">Рекомендуется использовать конечное время существования на всех опубликованных маршрутах (например, 30 минут).</span><span class="sxs-lookup"><span data-stu-id="b01aa-115">A finite nonaging lifetime on all published routes (for example, 30 minutes) is recommended.</span></span> <span data-ttu-id="b01aa-116">Если вы решили отозвать маршрут, его можно изменить на время существования устаревания.</span><span class="sxs-lookup"><span data-stu-id="b01aa-116">If you decide to retract a route, you can change the route to have an aging lifetime.</span></span> <span data-ttu-id="b01aa-117">Маршрут будет вести себя за несколько объявлений маршрутизатора, а затем исчезнет из маршрутизатора и узлов, получающих объявления маршрутизатора.</span><span class="sxs-lookup"><span data-stu-id="b01aa-117">The route will age over the course of several router advertisements and then disappear from both the router and any hosts receiving the router advertisements.</span></span>

<span data-ttu-id="b01aa-118">Маршруты, на которых размещается Поиск через объявления маршрутизатора, не публикуются.</span><span class="sxs-lookup"><span data-stu-id="b01aa-118">Routes that hosts find through router advertisements age and are not published.</span></span> <span data-ttu-id="b01aa-119">Адреса, настроенные на основе возрастных объявлений маршрутизатора, также исстраиваются.</span><span class="sxs-lookup"><span data-stu-id="b01aa-119">Addresses autoconfigured from router advertisements age as well.</span></span>

 

 



