---
title: Просмотреть флаги
description: Используйте флаги представления для управления представлениями таблицы маршрутизации.
ms.assetid: 836e3400-0dca-4a21-9a5c-7da357ed72ea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5192bf3e1acaa91412d8ae7e06d035e54af1ece6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105672149"
---
# <a name="view-flags"></a><span data-ttu-id="7aecb-103">Просмотреть флаги</span><span class="sxs-lookup"><span data-stu-id="7aecb-103">View Flags</span></span>

<span data-ttu-id="7aecb-104">Используйте флаги представления для управления представлениями таблицы маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="7aecb-104">Use the View Flags to control routing table views.</span></span>



| <span data-ttu-id="7aecb-105">Константа</span><span class="sxs-lookup"><span data-stu-id="7aecb-105">Constant</span></span>                 | <span data-ttu-id="7aecb-106">Значение</span><span class="sxs-lookup"><span data-stu-id="7aecb-106">Value</span></span>      | <span data-ttu-id="7aecb-107">Описание</span><span class="sxs-lookup"><span data-stu-id="7aecb-107">Description</span></span>                                                      |
|--------------------------|------------|------------------------------------------------------------------|
| <span data-ttu-id="7aecb-108">\_Максимальная \_ длина адреса \_ RTM</span><span class="sxs-lookup"><span data-stu-id="7aecb-108">RTM\_MAX \_ADDRESS\_SIZE</span></span> | <span data-ttu-id="7aecb-109">16</span><span class="sxs-lookup"><span data-stu-id="7aecb-109">16</span></span>         | <span data-ttu-id="7aecb-110">Максимальный размер адреса для семейства адресов.</span><span class="sxs-lookup"><span data-stu-id="7aecb-110">Max address size for an address family.</span></span>                          |
| <span data-ttu-id="7aecb-111">\_Максимальное число \_ просмотров RTM</span><span class="sxs-lookup"><span data-stu-id="7aecb-111">RTM\_MAX\_VIEWS</span></span>          | <span data-ttu-id="7aecb-112">32</span><span class="sxs-lookup"><span data-stu-id="7aecb-112">32</span></span>         | <span data-ttu-id="7aecb-113">Максимальное число представлений, которые могут быть активными в таблице маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="7aecb-113">Maximum number of views that can be active in the routing table.</span></span> |
| <span data-ttu-id="7aecb-114">\_идентификатор представления \_ RTM \_ укаст</span><span class="sxs-lookup"><span data-stu-id="7aecb-114">RTM\_VIEW\_ID\_UCAST</span></span>     | <span data-ttu-id="7aecb-115">0</span><span class="sxs-lookup"><span data-stu-id="7aecb-115">0</span></span>          | <span data-ttu-id="7aecb-116">Указывает представление одноадресной рассылки.</span><span class="sxs-lookup"><span data-stu-id="7aecb-116">Specifies a unicast view.</span></span>                                        |
| <span data-ttu-id="7aecb-117">\_идентификатор представления \_ RTM \_ мкаст</span><span class="sxs-lookup"><span data-stu-id="7aecb-117">RTM\_VIEW\_ID\_MCAST</span></span>     | <span data-ttu-id="7aecb-118">1</span><span class="sxs-lookup"><span data-stu-id="7aecb-118">1</span></span>          | <span data-ttu-id="7aecb-119">Указывает представление многоадресной рассылки.</span><span class="sxs-lookup"><span data-stu-id="7aecb-119">Specifies a multicast view.</span></span>                                      |
| <span data-ttu-id="7aecb-120">\_ \_ размер маски представления \_ RTM</span><span class="sxs-lookup"><span data-stu-id="7aecb-120">RTM\_VIEW\_MASK\_SIZE</span></span>    | <span data-ttu-id="7aecb-121">0x20</span><span class="sxs-lookup"><span data-stu-id="7aecb-121">0x20</span></span>       | <span data-ttu-id="7aecb-122">Указывает максимальное число представлений, которые можно настроить.</span><span class="sxs-lookup"><span data-stu-id="7aecb-122">Specifies the maximum number of views that can be configured.</span></span>    |
| <span data-ttu-id="7aecb-123">\_Маска представления RTM — \_ \_ нет</span><span class="sxs-lookup"><span data-stu-id="7aecb-123">RTM\_VIEW\_MASK\_NONE</span></span>    | <span data-ttu-id="7aecb-124">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7aecb-124">0x00000000</span></span> | <span data-ttu-id="7aecb-125">Возвращает сведения независимо от представления.</span><span class="sxs-lookup"><span data-stu-id="7aecb-125">Returns information regardless of the view.</span></span>                      |
| <span data-ttu-id="7aecb-126">\_Маска представления \_ RTM \_ любая</span><span class="sxs-lookup"><span data-stu-id="7aecb-126">RTM\_VIEW\_MASK\_ANY</span></span>     | <span data-ttu-id="7aecb-127">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7aecb-127">0x00000000</span></span> | <span data-ttu-id="7aecb-128">Возвращает назначения из всех представлений.</span><span class="sxs-lookup"><span data-stu-id="7aecb-128">Returns destinations from all views.</span></span> <span data-ttu-id="7aecb-129">Это значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="7aecb-129">This is the default value.</span></span>  |
| <span data-ttu-id="7aecb-130">\_ \_ укаст маски представления \_ RTM</span><span class="sxs-lookup"><span data-stu-id="7aecb-130">RTM\_VIEW\_MASK\_UCAST</span></span>   | <span data-ttu-id="7aecb-131">0x00000001</span><span class="sxs-lookup"><span data-stu-id="7aecb-131">0x00000001</span></span> | <span data-ttu-id="7aecb-132">Возвращает назначения из представления одноадресной рассылки.</span><span class="sxs-lookup"><span data-stu-id="7aecb-132">Returns destinations from the unicast view.</span></span>                      |
| <span data-ttu-id="7aecb-133">\_ \_ мкаст маски представления \_ RTM</span><span class="sxs-lookup"><span data-stu-id="7aecb-133">RTM\_VIEW\_MASK\_MCAST</span></span>   | <span data-ttu-id="7aecb-134">0x00000002</span><span class="sxs-lookup"><span data-stu-id="7aecb-134">0x00000002</span></span> | <span data-ttu-id="7aecb-135">Возвращает назначения из представления многоадресной рассылки.</span><span class="sxs-lookup"><span data-stu-id="7aecb-135">Returns destinations from the multicast view.</span></span>                    |
| <span data-ttu-id="7aecb-136">ОКОНЧАТЕЛЬНая \_ \_ Маска \_ представления</span><span class="sxs-lookup"><span data-stu-id="7aecb-136">RTM\_VIEW\_MASK\_ALL</span></span>     | <span data-ttu-id="7aecb-137">0xFFFFFFFF</span><span class="sxs-lookup"><span data-stu-id="7aecb-137">0xFFFFFFFF</span></span> | <span data-ttu-id="7aecb-138">Возвращает сведения из всех представлений.</span><span class="sxs-lookup"><span data-stu-id="7aecb-138">Returns information from all views.</span></span>                              |



 

 

 




