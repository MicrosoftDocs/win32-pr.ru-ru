---
title: Флаги перечисления
description: Флаги перечисления
ms.assetid: d5677e3a-c0c1-4768-aae4-f6564a40ee99
keywords:
- Перечисление
- Флаги перечисления
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a1cbec08496ccd6338de77ebdddf76547a48258
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986485"
---
# <a name="enumeration-flags"></a><span data-ttu-id="8a9db-105">Флаги перечисления</span><span class="sxs-lookup"><span data-stu-id="8a9db-105">Enumeration Flags</span></span>



| <span data-ttu-id="8a9db-106">Константа</span><span class="sxs-lookup"><span data-stu-id="8a9db-106">Constant</span></span>               | <span data-ttu-id="8a9db-107">Значение</span><span class="sxs-lookup"><span data-stu-id="8a9db-107">Value</span></span>      | <span data-ttu-id="8a9db-108">Описание</span><span class="sxs-lookup"><span data-stu-id="8a9db-108">Description</span></span>                                                                                                                                               |
|------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a9db-109">\_Начало ПЕРЕЧИСЛЕНИЯ \_ RTM</span><span class="sxs-lookup"><span data-stu-id="8a9db-109">RTM\_ENUM\_START</span></span>       | <span data-ttu-id="8a9db-110">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8a9db-110">0x00000000</span></span> | <span data-ttu-id="8a9db-111">Перечисление маршрутов или назначений, начиная с 0/0.</span><span class="sxs-lookup"><span data-stu-id="8a9db-111">Enumerate routes or destinations starting at 0/0.</span></span>                                                                                                         |
| <span data-ttu-id="8a9db-112">\_Далее перечисление RTM \_</span><span class="sxs-lookup"><span data-stu-id="8a9db-112">RTM\_ENUM\_NEXT</span></span>        | <span data-ttu-id="8a9db-113">0x00000001</span><span class="sxs-lookup"><span data-stu-id="8a9db-113">0x00000001</span></span> | <span data-ttu-id="8a9db-114">Перечисление маршрутов или назначений, начиная с указанного адреса или длины маски (например, 10/8).</span><span class="sxs-lookup"><span data-stu-id="8a9db-114">Enumerate routes or destinations starting at the specified address/mask length (such as 10/8).</span></span> <span data-ttu-id="8a9db-115">Перечисление переходит к концу таблицы маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="8a9db-115">The enumeration continues to the end of the routing table.</span></span> |
| <span data-ttu-id="8a9db-116">\_диапазон ПЕРЕЧИСЛЕНИЯ \_ RTM</span><span class="sxs-lookup"><span data-stu-id="8a9db-116">RTM\_ENUM\_RANGE</span></span>       | <span data-ttu-id="8a9db-117">0x00000002</span><span class="sxs-lookup"><span data-stu-id="8a9db-117">0x00000002</span></span> | <span data-ttu-id="8a9db-118">Перечисляет маршруты или назначения в указанном поддереве, заданном параметром длина адреса или маски (например, 10/8).</span><span class="sxs-lookup"><span data-stu-id="8a9db-118">Enumerate routes or destinations in the specified subtree specified by the address/mask length (such as 10/8).</span></span>                                            |
| <span data-ttu-id="8a9db-119">RTM, \_ Перечисление \_ всех \_ DESTS</span><span class="sxs-lookup"><span data-stu-id="8a9db-119">RTM\_ENUM\_ALL\_DESTS</span></span>  | <span data-ttu-id="8a9db-120">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8a9db-120">0x00000000</span></span> | <span data-ttu-id="8a9db-121">Возвращает все назначения.</span><span class="sxs-lookup"><span data-stu-id="8a9db-121">Return all destinations.</span></span>                                                                                                                                  |
| <span data-ttu-id="8a9db-122">RTM — \_ собственное перечисление \_ \_ DESTS</span><span class="sxs-lookup"><span data-stu-id="8a9db-122">RTM\_ENUM\_OWN\_DESTS</span></span>  | <span data-ttu-id="8a9db-123">0x01000000</span><span class="sxs-lookup"><span data-stu-id="8a9db-123">0x01000000</span></span> | <span data-ttu-id="8a9db-124">Возвращать только те назначения, которыми владеет клиент.</span><span class="sxs-lookup"><span data-stu-id="8a9db-124">Return only those destinations that the client owns.</span></span>                                                                                                      |
| <span data-ttu-id="8a9db-125">RTM, \_ Перечисление \_ всех \_ маршрутов</span><span class="sxs-lookup"><span data-stu-id="8a9db-125">RTM\_ENUM\_ALL\_ROUTES</span></span> | <span data-ttu-id="8a9db-126">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8a9db-126">0x00000000</span></span> | <span data-ttu-id="8a9db-127">Возвращает все маршруты.</span><span class="sxs-lookup"><span data-stu-id="8a9db-127">Return all routes.</span></span>                                                                                                                                        |
| <span data-ttu-id="8a9db-128">Окончательная версия \_ Перечисление \_ собственных \_ маршрутов</span><span class="sxs-lookup"><span data-stu-id="8a9db-128">RTM\_ENUM\_OWN\_ROUTES</span></span> | <span data-ttu-id="8a9db-129">0x00010000</span><span class="sxs-lookup"><span data-stu-id="8a9db-129">0x00010000</span></span> | <span data-ttu-id="8a9db-130">Возвращать только те маршруты, которыми владеет клиент.</span><span class="sxs-lookup"><span data-stu-id="8a9db-130">Return only those routes that the client owns.</span></span>                                                                                                            |



 

 

 




