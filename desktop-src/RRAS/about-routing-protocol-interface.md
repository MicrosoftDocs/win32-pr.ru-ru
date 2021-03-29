---
title: О интерфейсе протокола маршрутизации
description: В следующей документации описывается интеграция протоколов маршрутизации сторонних производителей в службу маршрутизации и удаленного доступа (RRAS).
ms.assetid: 593e3b8a-6f26-47c6-aa93-520d36db7a6f
keywords:
- RRAS службы маршрутизации и удаленного доступа, интерфейс протокола маршрутизации
- RRAS службы маршрутизации и удаленного доступа, интерфейс протокола маршрутизации, описание
- Интерфейс протокола маршрутизации RRAS
- Интерфейс протокола маршрутизации RRAS, описание
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5bc663f249ca42ebbae509c164a828d603a9b968
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103777375"
---
# <a name="about-routing-protocol-interface"></a><span data-ttu-id="e9976-107">О интерфейсе протокола маршрутизации</span><span class="sxs-lookup"><span data-stu-id="e9976-107">About Routing Protocol Interface</span></span>

<span data-ttu-id="e9976-108">В следующей документации описывается интеграция протоколов маршрутизации сторонних производителей в службу маршрутизации и удаленного доступа (RRAS).</span><span class="sxs-lookup"><span data-stu-id="e9976-108">The following documentation describes the integration of third-party routing protocols into the Routing and Remote Access Service (RRAS).</span></span> <span data-ttu-id="e9976-109">RRAS — это функция Windows, которая выступает в качестве маршрутизатора с несколькими протоколами.</span><span class="sxs-lookup"><span data-stu-id="e9976-109">RRAS is a feature of Windows that acts as a multi-protocol router.</span></span> <span data-ttu-id="e9976-110">RRAS определяет интерфейс между диспетчером маршрутизаторов и протоколом маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="e9976-110">RRAS defines the interface between the router manager and the routing protocol.</span></span> <span data-ttu-id="e9976-111">Протокол маршрутизации реализуется в библиотеке динамической компоновки (DLL).</span><span class="sxs-lookup"><span data-stu-id="e9976-111">The routing protocol is implemented in a dynamic link library (DLL).</span></span>

<span data-ttu-id="e9976-112">Используйте этот интерфейс для реализации протоколов маршрутизации, таких как ИГРП, НЛСП и BGP, в качестве библиотек DLL пользовательского режима, работающих с RRAS.</span><span class="sxs-lookup"><span data-stu-id="e9976-112">Use this interface to implement routing protocols, such as IGRP, NLSP, and BGP, as user-mode DLLs that work with RRAS.</span></span>

<span data-ttu-id="e9976-113">В этой документации описаны следующие темы:</span><span class="sxs-lookup"><span data-stu-id="e9976-113">This documentation describes the following topics:</span></span>

-   [<span data-ttu-id="e9976-114">Адаптеры</span><span class="sxs-lookup"><span data-stu-id="e9976-114">Adapters</span></span>](adapters.md)
-   [<span data-ttu-id="e9976-115">Интерфейсы</span><span class="sxs-lookup"><span data-stu-id="e9976-115">Interfaces</span></span>](interfaces.md)
-   [<span data-ttu-id="e9976-116">Статические и автостатические маршруты</span><span class="sxs-lookup"><span data-stu-id="e9976-116">Static and Autostatic Routes</span></span>](static-and-autostatic-routes.md)

 

 




