---
title: Привязка к начальной точке поиска
description: Начальная точка поиска — это контейнер, который напрямую или косвенно содержит искомые объекты.
ms.assetid: f93c1310-7c8b-4d28-bd4d-6fab969d3353
ms.tgt_platform: multiple
keywords:
- Active Directory примеры Active Directory, привязка к начальной точке поиска
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 741986e651848c1d2a88ab016b63365db91b26b1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486545"
---
# <a name="binding-to-the-search-start-point"></a><span data-ttu-id="69f88-104">Привязка к начальной точке поиска</span><span class="sxs-lookup"><span data-stu-id="69f88-104">Binding to the Search Start Point</span></span>

<span data-ttu-id="69f88-105">Начальная точка поиска — это контейнер, который напрямую или косвенно содержит искомые объекты.</span><span class="sxs-lookup"><span data-stu-id="69f88-105">The start point for a search is a container that directly or indirectly contains the objects searched for.</span></span> <span data-ttu-id="69f88-106">Поиск не будет выполняться в контейнерах выше начальной точки поиска.</span><span class="sxs-lookup"><span data-stu-id="69f88-106">The search will not be performed in containers above the search start point.</span></span> <span data-ttu-id="69f88-107">Например, возьмем следующую гипотетическую структуру каталогов:</span><span class="sxs-lookup"><span data-stu-id="69f88-107">For example, take the following hypothetical directory structure:</span></span>

``` syntax
Domain A
    Container 1
        Object 1
        Object 2
    Container 2
        Object 3
        Object 4
```

<span data-ttu-id="69f88-108">Если поиск выполняется для всех объектов, а начальная точка поиска — "контейнер 2", то будут получены только объекты "объект 3" и "объект 4".</span><span class="sxs-lookup"><span data-stu-id="69f88-108">If a search is performed for all objects and the search start point is "Container 2", only "Object 3" and "Object 4" would be retrieved.</span></span> <span data-ttu-id="69f88-109">Если поиск выполняется с точкой начала поиска в "контейнер 1", то будет получен объект "Object 1" и "Object 2".</span><span class="sxs-lookup"><span data-stu-id="69f88-109">If the same search was performed with the search start point at "Container 1", "Object 1" and "Object 2" would be retrieved.</span></span>

<span data-ttu-id="69f88-110">Чтобы выполнить привязку к начальной точке поиска, выполните привязку к ADsPath контейнера, который будет начальной точкой поиска.</span><span class="sxs-lookup"><span data-stu-id="69f88-110">To bind to the search start point, bind to the ADsPath of the container that will be the search start point.</span></span>

 

 




