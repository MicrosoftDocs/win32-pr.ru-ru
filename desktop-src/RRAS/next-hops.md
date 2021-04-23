---
title: Следующие прыжки
description: С маршрутами связано по одному или нескольким прыжкам.
ms.assetid: 90e5a79b-4fee-479c-9888-fcb3b6d38c1f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d26fcbc13ea7ad7c886ebd9f6f945f7cf6d6efe6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067453"
---
# <a name="next-hops"></a><span data-ttu-id="88407-103">Следующие прыжки</span><span class="sxs-lookup"><span data-stu-id="88407-103">Next Hops</span></span>

<span data-ttu-id="88407-104">С маршрутами связано по одному или нескольким прыжкам.</span><span class="sxs-lookup"><span data-stu-id="88407-104">Routes have one or more next hops associated with them.</span></span> <span data-ttu-id="88407-105">Если назначение находится не в подключенной напрямую сети, следующий прыжок — это адрес следующего маршрутизатора (или сети) в исходящей сети, который наилучшим образом направляет данные в место назначения.</span><span class="sxs-lookup"><span data-stu-id="88407-105">If the destination is not on a directly connected network, the next hop is the address of the next router (or network) on the outgoing network that can best route data to the destination.</span></span> <span data-ttu-id="88407-106">Лучшим маршрутом является маршрут с минимальными затратами в зависимости от используемой политики маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="88407-106">The best route is the route that has the least cost, based on the routing policy in use.</span></span> <span data-ttu-id="88407-107">Каждый следующий прыжок можно использовать для пересылки данных по пути к назначению.</span><span class="sxs-lookup"><span data-stu-id="88407-107">Each next hop can be used to forward data on the path to the destination.</span></span> <span data-ttu-id="88407-108">Все маршруты, принадлежащие клиенту, совместно используют общий набор записей следующего прыжка, добавленных клиентом.</span><span class="sxs-lookup"><span data-stu-id="88407-108">All routes owned by a client share a common set of next-hop entries that were added by the client.</span></span>

<span data-ttu-id="88407-109">Каждый следующий прыжок однозначно идентифицируется по адресу следующего прыжка и индексу интерфейса, используемому для достижения следующего прыжка.</span><span class="sxs-lookup"><span data-stu-id="88407-109">Each next hop is uniquely identified by the address of the next hop and the interface index used to reach the next hop.</span></span>

<span data-ttu-id="88407-110">Если следующий прыжок не подключен напрямую, он помечается как удаленный следующий прыжок.</span><span class="sxs-lookup"><span data-stu-id="88407-110">If the next hop itself is not directly connected, it is marked as a "remote" next hop.</span></span> <span data-ttu-id="88407-111">В этом случае сервер пересылки должен выполнить другой поиск, используя сетевой адрес следующего прыжка.</span><span class="sxs-lookup"><span data-stu-id="88407-111">In this case, the forwarder must perform another lookup using the next hop's network address.</span></span> <span data-ttu-id="88407-112">Этот поиск необходим для поиска "локального" следующего прыжка, используемого для достижения удаленного следующего прыжка и назначения.</span><span class="sxs-lookup"><span data-stu-id="88407-112">This lookup is necessary to find the "local" next hop used to reach the remote next hop and the destination.</span></span>

<span data-ttu-id="88407-113">Запись следующего прыжка в таблице маршрутизации включает:</span><span class="sxs-lookup"><span data-stu-id="88407-113">A next-hop entry in the routing table includes:</span></span>

-   <span data-ttu-id="88407-114">Сетевой адрес следующего прыжка</span><span class="sxs-lookup"><span data-stu-id="88407-114">The network address of the next hop</span></span>
-   <span data-ttu-id="88407-115">Владелец следующего прыжка</span><span class="sxs-lookup"><span data-stu-id="88407-115">The owner of the next hop</span></span>
-   <span data-ttu-id="88407-116">Идентификатор исходящего интерфейса</span><span class="sxs-lookup"><span data-stu-id="88407-116">The identifier of the outgoing interface</span></span>
-   <span data-ttu-id="88407-117">Состояние следующего прыжка</span><span class="sxs-lookup"><span data-stu-id="88407-117">The state of the next hop</span></span>
-   <span data-ttu-id="88407-118">Флаги, связанные со следующим прыжком</span><span class="sxs-lookup"><span data-stu-id="88407-118">Flags associated with the next hop</span></span>
-   <span data-ttu-id="88407-119">Сведения, являющиеся частными для владельца следующего прыжка</span><span class="sxs-lookup"><span data-stu-id="88407-119">Information that is private to the owner of the next hop</span></span>
-   <span data-ttu-id="88407-120">Маркер назначения, соответствующий удаленному следующему прыжку</span><span class="sxs-lookup"><span data-stu-id="88407-120">A handle to the destination corresponding to the remote next hop</span></span>

 

 




