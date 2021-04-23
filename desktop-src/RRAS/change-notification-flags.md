---
title: Изменение флагов уведомления
description: Изменение флагов уведомления
ms.assetid: 1f1aef71-a2b7-49ad-a0bc-f61f10b701c9
keywords:
- Change
- Изменение флагов уведомления
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3e6d3015be29c84b6b93b47b373d05f96f4388b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330291"
---
# <a name="change-notification-flags"></a><span data-ttu-id="f82ce-105">Изменение флагов уведомления</span><span class="sxs-lookup"><span data-stu-id="f82ce-105">Change Notification Flags</span></span>



| <span data-ttu-id="f82ce-106">Константа</span><span class="sxs-lookup"><span data-stu-id="f82ce-106">Constant</span></span>                         | <span data-ttu-id="f82ce-107">Значение</span><span class="sxs-lookup"><span data-stu-id="f82ce-107">Value</span></span>      | <span data-ttu-id="f82ce-108">Описание</span><span class="sxs-lookup"><span data-stu-id="f82ce-108">Description</span></span>                                                                                                                                                           |
|----------------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f82ce-109">\_ \_ типы изменения номера \_ RTM</span><span class="sxs-lookup"><span data-stu-id="f82ce-109">RTM\_NUM\_CHANGE\_TYPES</span></span>          | <span data-ttu-id="f82ce-110">3</span><span class="sxs-lookup"><span data-stu-id="f82ce-110">3</span></span>          | <span data-ttu-id="f82ce-111">Указывает число типов изменений, которые в настоящее время используются диспетчером таблиц маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="f82ce-111">Specifies the number of change types that are currently used by the routing table manager.</span></span>                                                                            |
| <span data-ttu-id="f82ce-112">\_тип изменения \_ RTM \_</span><span class="sxs-lookup"><span data-stu-id="f82ce-112">RTM\_CHANGE\_TYPE\_ALL</span></span>           | <span data-ttu-id="f82ce-113">0x0001</span><span class="sxs-lookup"><span data-stu-id="f82ce-113">0x0001</span></span>     | <span data-ttu-id="f82ce-114">Уведомляет клиента о любом изменении назначения.</span><span class="sxs-lookup"><span data-stu-id="f82ce-114">Notifies the client of any change to a destination.</span></span>                                                                                                                   |
| <span data-ttu-id="f82ce-115">\_ \_ оптимальный тип изменения RTM \_</span><span class="sxs-lookup"><span data-stu-id="f82ce-115">RTM\_CHANGE\_TYPE\_BEST</span></span>          | <span data-ttu-id="f82ce-116">0x0002</span><span class="sxs-lookup"><span data-stu-id="f82ce-116">0x0002</span></span>     | <span data-ttu-id="f82ce-117">Уведомляет клиента об изменениях в оптимальном маршруте или при изменении наилучшего маршрута.</span><span class="sxs-lookup"><span data-stu-id="f82ce-117">Notifies the client of changes to the best route, or when the best route changes.</span></span>                                                                                     |
| <span data-ttu-id="f82ce-118">\_Пересылка \_ типов изменений в RTM \_</span><span class="sxs-lookup"><span data-stu-id="f82ce-118">RTM\_CHANGE\_TYPE\_FORWARDING</span></span>    | <span data-ttu-id="f82ce-119">0x0004</span><span class="sxs-lookup"><span data-stu-id="f82ce-119">0x0004</span></span>     | <span data-ttu-id="f82ce-120">Уведомляет клиента о любых наиболее оптимальных изменениях маршрута, влияющих на перенаправление (например, изменения следующего прыжка).</span><span class="sxs-lookup"><span data-stu-id="f82ce-120">Notifies the client of any best route changes that affect forwarding (such as next hop changes).</span></span>                                                                      |
| <span data-ttu-id="f82ce-121">RTM \_ уведомлять \_ только \_ отмеченные \_ DESTS</span><span class="sxs-lookup"><span data-stu-id="f82ce-121">RTM\_NOTIFY\_ONLY\_MARKED\_DESTS</span></span> | <span data-ttu-id="f82ce-122">0x00010000</span><span class="sxs-lookup"><span data-stu-id="f82ce-122">0x00010000</span></span> | <span data-ttu-id="f82ce-123">Уведомляет клиента об изменениях назначений, помеченных клиентом.</span><span class="sxs-lookup"><span data-stu-id="f82ce-123">Notifies the client of changes to destinations that the client has marked.</span></span> <span data-ttu-id="f82ce-124">Если этот флаг не указан, отправляются сообщения уведомления об изменении для всех назначений.</span><span class="sxs-lookup"><span data-stu-id="f82ce-124">If this flag is not specified, change notification messages for all destinations are sent.</span></span> |



 

 

 




