---
title: События элемента управления агента
description: События элемента управления агента
ms.assetid: 86543cc0-ed1c-41d8-9fc9-cc163e308947
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04d57a0f21734d4b53987be6935d179a6b9b59eb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105654237"
---
# <a name="agent-control-events"></a><span data-ttu-id="487c0-103">События элемента управления агента</span><span class="sxs-lookup"><span data-stu-id="487c0-103">Agent Control Events</span></span>

<span data-ttu-id="487c0-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="487c0-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="487c0-105">Элемент управления Microsoft Agent предоставляет несколько событий, которые позволяют клиентскому приложению отслеживанию состояния сервера:</span><span class="sxs-lookup"><span data-stu-id="487c0-105">The Microsoft Agent control provides several events that enable your client application to track the state of the server:</span></span>

-   [<span data-ttu-id="487c0-106">**активатеинпут**</span><span class="sxs-lookup"><span data-stu-id="487c0-106">**ActivateInput**</span></span>](activateinput-event.md)
-   [<span data-ttu-id="487c0-107">**активеклиентчанже**</span><span class="sxs-lookup"><span data-stu-id="487c0-107">**ActiveClientChange**</span></span>](activeclientchange-event.md)
-   [<span data-ttu-id="487c0-108">**ажентпропертичанже**</span><span class="sxs-lookup"><span data-stu-id="487c0-108">**AgentPropertyChange**</span></span>](agentpropertychange-event.md)
-   [<span data-ttu-id="487c0-109">**баллунхиде**</span><span class="sxs-lookup"><span data-stu-id="487c0-109">**BalloonHide**</span></span>](balloonhide-event.md)
-   [<span data-ttu-id="487c0-110">**баллуншов**</span><span class="sxs-lookup"><span data-stu-id="487c0-110">**BalloonShow**</span></span>](balloonshow-event.md)
-   [<span data-ttu-id="487c0-111">**Закладка**</span><span class="sxs-lookup"><span data-stu-id="487c0-111">**Bookmark**</span></span>](bookmark-event.md)
-   [<span data-ttu-id="487c0-112">**Щелкните**</span><span class="sxs-lookup"><span data-stu-id="487c0-112">**Click**</span></span>](click-event.md)
-   [<span data-ttu-id="487c0-113">**Get-Help**</span><span class="sxs-lookup"><span data-stu-id="487c0-113">**Command**</span></span>](command-event.md)
-   [<span data-ttu-id="487c0-114">**Кнопки**</span><span class="sxs-lookup"><span data-stu-id="487c0-114">**DblClick**</span></span>](dblclick-event.md)
-   [<span data-ttu-id="487c0-115">**деактиватеинпут**</span><span class="sxs-lookup"><span data-stu-id="487c0-115">**DeactivateInput**</span></span>](deactivateinput-event.md)
-   [<span data-ttu-id="487c0-116">**дефаултчарактерчанже**</span><span class="sxs-lookup"><span data-stu-id="487c0-116">**DefaultCharacterChange**</span></span>](defaultcharacterchange-event.md)
-   [<span data-ttu-id="487c0-117">**драгкомплете**</span><span class="sxs-lookup"><span data-stu-id="487c0-117">**DragComplete**</span></span>](dragcomplete-event.md)
-   [<span data-ttu-id="487c0-118">**драгстарт**</span><span class="sxs-lookup"><span data-stu-id="487c0-118">**DragStart**</span></span>](dragstart-event.md)
-   [<span data-ttu-id="487c0-119">**хелпкомплете**</span><span class="sxs-lookup"><span data-stu-id="487c0-119">**HelpComplete**</span></span>](helpcomplete-event.md)
-   [<span data-ttu-id="487c0-120">**Скрыть**</span><span class="sxs-lookup"><span data-stu-id="487c0-120">**Hide**</span></span>](hide-event.md)
-   [<span data-ttu-id="487c0-121">**идлекомплете**</span><span class="sxs-lookup"><span data-stu-id="487c0-121">**IdleComplete**</span></span>](idlecomplete-event.md)
-   [<span data-ttu-id="487c0-122">**идлестарт**</span><span class="sxs-lookup"><span data-stu-id="487c0-122">**IdleStart**</span></span>](idlestart-event.md)
-   [<span data-ttu-id="487c0-123">**листенкомплете**</span><span class="sxs-lookup"><span data-stu-id="487c0-123">**ListenComplete**</span></span>](listencomplete-event.md)
-   [<span data-ttu-id="487c0-124">**листенстарт**</span><span class="sxs-lookup"><span data-stu-id="487c0-124">**ListenStart**</span></span>](listenstart-event.md)
-   [<span data-ttu-id="487c0-125">**Переместить**</span><span class="sxs-lookup"><span data-stu-id="487c0-125">**Move**</span></span>](move-event.md)
-   [<span data-ttu-id="487c0-126">**рекуесткомплете**</span><span class="sxs-lookup"><span data-stu-id="487c0-126">**RequestComplete**</span></span>](requestcomplete-event.md)
-   [<span data-ttu-id="487c0-127">**RequestStart**</span><span class="sxs-lookup"><span data-stu-id="487c0-127">**RequestStart**</span></span>](requeststart-event.md)
-   [<span data-ttu-id="487c0-128">**Казывающи**</span><span class="sxs-lookup"><span data-stu-id="487c0-128">**Show**</span></span>](show-event.md)
-   [<span data-ttu-id="487c0-129">**Размер**</span><span class="sxs-lookup"><span data-stu-id="487c0-129">**Size**</span></span>](size-event.md)

<span data-ttu-id="487c0-130">Сервер больше не отправляет эти события перезагрузки и завершения работы.</span><span class="sxs-lookup"><span data-stu-id="487c0-130">The server no longer sends these Restart and Shutdown events.</span></span>

 

 




