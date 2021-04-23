---
title: Флаги следующего прыжка
description: Флаги следующего прыжка
ms.assetid: e4c7e9ea-21f5-491a-b005-1ef1a457cb80
keywords:
- Следующая
- Флаги следующего прыжка
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5bd672c9b083e47c3d0a7419d03ab890c1037ce5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068460"
---
# <a name="next-hop-flags"></a><span data-ttu-id="ecdef-105">Флаги следующего прыжка</span><span class="sxs-lookup"><span data-stu-id="ecdef-105">Next Hop Flags</span></span>

## <a name="next-hop-state-flags"></a><span data-ttu-id="ecdef-106">Флаги состояния следующего прыжка</span><span class="sxs-lookup"><span data-stu-id="ecdef-106">Next Hop State Flags</span></span>



| <span data-ttu-id="ecdef-107">Константа</span><span class="sxs-lookup"><span data-stu-id="ecdef-107">Constant</span></span>                     | <span data-ttu-id="ecdef-108">Значение</span><span class="sxs-lookup"><span data-stu-id="ecdef-108">Value</span></span> | <span data-ttu-id="ecdef-109">Описание</span><span class="sxs-lookup"><span data-stu-id="ecdef-109">Description</span></span>                              |
|------------------------------|-------|------------------------------------------|
| <span data-ttu-id="ecdef-110">RTM \_ — \_ состояние " \_ создано"</span><span class="sxs-lookup"><span data-stu-id="ecdef-110">RTM\_NEXTHOP\_STATE\_CREATED</span></span> | <span data-ttu-id="ecdef-111">0</span><span class="sxs-lookup"><span data-stu-id="ecdef-111">0</span></span>     | <span data-ttu-id="ecdef-112">Указывает, что был создан следующий прыжок.</span><span class="sxs-lookup"><span data-stu-id="ecdef-112">Indicates that the next hop was created.</span></span> |
| <span data-ttu-id="ecdef-113">\_состояние RTM \_ \_ удалено</span><span class="sxs-lookup"><span data-stu-id="ecdef-113">RTM\_NEXTHOP\_STATE\_DELETED</span></span> | <span data-ttu-id="ecdef-114">1</span><span class="sxs-lookup"><span data-stu-id="ecdef-114">1</span></span>     | <span data-ttu-id="ecdef-115">Указывает, что следующий прыжок был удален.</span><span class="sxs-lookup"><span data-stu-id="ecdef-115">Indicates that the next hop was deleted.</span></span> |



 

## <a name="next-hop-flags"></a><span data-ttu-id="ecdef-116">Флаги следующего прыжка</span><span class="sxs-lookup"><span data-stu-id="ecdef-116">Next Hop Flags</span></span>



| <span data-ttu-id="ecdef-117">Константа</span><span class="sxs-lookup"><span data-stu-id="ecdef-117">Constant</span></span>                    | <span data-ttu-id="ecdef-118">Значение</span><span class="sxs-lookup"><span data-stu-id="ecdef-118">Value</span></span>  | <span data-ttu-id="ecdef-119">Описание</span><span class="sxs-lookup"><span data-stu-id="ecdef-119">Description</span></span>                                                                                                                                           |
|-----------------------------|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ecdef-120">RTM \_ — \_ Флаги \_ удаленных</span><span class="sxs-lookup"><span data-stu-id="ecdef-120">RTM\_NEXTHOP\_FLAGS\_REMOTE</span></span> | <span data-ttu-id="ecdef-121">0x0001</span><span class="sxs-lookup"><span data-stu-id="ecdef-121">0x0001</span></span> | <span data-ttu-id="ecdef-122">Следующий прыжок указывает на удаленное назначение, которое недоступно напрямую.</span><span class="sxs-lookup"><span data-stu-id="ecdef-122">This next hop points to a remote destination that is not directly reachable.</span></span> <span data-ttu-id="ecdef-123">Чтобы получить полный путь, клиент должен выполнить рекурсивный Уточняющий запрос.</span><span class="sxs-lookup"><span data-stu-id="ecdef-123">To obtain the complete path, the client must perform a recursive lookup.</span></span> |
| <span data-ttu-id="ecdef-124">RTM \_ , \_ Флаги NEXTHOP \_</span><span class="sxs-lookup"><span data-stu-id="ecdef-124">RTM\_NEXTHOP\_FLAGS\_DOWN</span></span>   | <span data-ttu-id="ecdef-125">0x0002</span><span class="sxs-lookup"><span data-stu-id="ecdef-125">0x0002</span></span> | <span data-ttu-id="ecdef-126">Этот флаг зарезервирован для использования в будущем.</span><span class="sxs-lookup"><span data-stu-id="ecdef-126">This flag is reserved for future use.</span></span>                                                                                                                 |



 

## <a name="next-hop-added"></a><span data-ttu-id="ecdef-127">Добавлен следующий прыжок</span><span class="sxs-lookup"><span data-stu-id="ecdef-127">Next Hop Added</span></span>



| <span data-ttu-id="ecdef-128">Константа</span><span class="sxs-lookup"><span data-stu-id="ecdef-128">Constant</span></span>                  | <span data-ttu-id="ecdef-129">Значение</span><span class="sxs-lookup"><span data-stu-id="ecdef-129">Value</span></span> | <span data-ttu-id="ecdef-130">Описание</span><span class="sxs-lookup"><span data-stu-id="ecdef-130">Description</span></span>                 |
|---------------------------|-------|-----------------------------|
| <span data-ttu-id="ecdef-131">RTM \_ , \_ изменение \_ новой версии</span><span class="sxs-lookup"><span data-stu-id="ecdef-131">RTM\_NEXTHOP\_CHANGE\_NEW</span></span> | <span data-ttu-id="ecdef-132">0x01</span><span class="sxs-lookup"><span data-stu-id="ecdef-132">0x01</span></span>  | <span data-ttu-id="ecdef-133">Создан новый следующий прыжок.</span><span class="sxs-lookup"><span data-stu-id="ecdef-133">A new next hop was created.</span></span> |



 

 

 




