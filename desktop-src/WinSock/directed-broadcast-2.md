---
description: Как правило, это больше, чем широковещательная рассылка ALL-Routes, а направленная широковещательная рассылка ограничивается указанной вами локальной сетью.
ms.assetid: e2358580-5a65-434d-ba4c-a6b0615bccc3
title: Направленное вещание
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f3a47bd47e9800e1f9c93cffa555b76feb77373
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701539"
---
# <a name="directed-broadcast"></a><span data-ttu-id="8e305-103">Направленное вещание</span><span class="sxs-lookup"><span data-stu-id="8e305-103">Directed Broadcast</span></span>

<span data-ttu-id="8e305-104">Как правило, это больше, чем широковещательная рассылка ALL-Routes, а направленная широковещательная рассылка ограничивается указанной вами локальной сетью.</span><span class="sxs-lookup"><span data-stu-id="8e305-104">Generally considered more network friendly than an all-routes broadcast, a directed broadcast limits itself to the local network that you specify.</span></span> <span data-ttu-id="8e305-105">Введите **SA \_ нетнум** с номером целевой сети и **SA \_ ноденум** с двоичными данными.</span><span class="sxs-lookup"><span data-stu-id="8e305-105">Fill **sa\_netnum** with the target network number and **sa\_nodenum** with binary ones.</span></span> <span data-ttu-id="8e305-106">Маршрутизаторы перенаправляют этот запрос в целевую сеть, где он преобразуется в локальную трансляцию.</span><span class="sxs-lookup"><span data-stu-id="8e305-106">Routers forward this request to the destination network where it becomes a local broadcast.</span></span> <span data-ttu-id="8e305-107">Промежуточные сети не видят этот пакет в качестве вещания.</span><span class="sxs-lookup"><span data-stu-id="8e305-107">Intermediate networks do not see this packet as a broadcast.</span></span>

 

 



