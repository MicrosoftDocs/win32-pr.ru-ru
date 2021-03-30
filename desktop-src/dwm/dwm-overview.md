---
title: Диспетчер окон рабочего стола
description: Функция композиции рабочего стола, появившаяся в Windows Vista, существенно изменила способ отображения пикселов в приложениях на экране.
ms.assetid: VS|winui|~\winui\desktopwindowmanager\overviews\dwm_overview.htm
keywords:
- Диспетчер окон рабочего стола (DWM), сведения
- DWM (диспетчер окон рабочего стола), сведения
- Диспетчер окон рабочего стола (DWM), композиция
- DWM (диспетчер окон рабочего стола), композиция
- Композиция рабочего стола
- композиции
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8578001aebf1c73e6d400ffae383674a8432c399
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103776727"
---
# <a name="desktop-window-manager"></a><span data-ttu-id="463ac-109">Диспетчер окон рабочего стола</span><span class="sxs-lookup"><span data-stu-id="463ac-109">Desktop Window Manager</span></span>

<span data-ttu-id="463ac-110">Функция композиции рабочего стола, появившаяся в Windows Vista, существенно изменила способ отображения пикселов в приложениях на экране.</span><span class="sxs-lookup"><span data-stu-id="463ac-110">The desktop composition feature, introduced in Windows Vista, fundamentally changed the way applications display pixels on the screen.</span></span> <span data-ttu-id="463ac-111">Если композиция рабочего стола включена, отдельные окна больше не наводятся непосредственно на экран или на основное устройство отображения, как в предыдущих версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="463ac-111">When desktop composition is enabled, individual windows no longer draw directly to the screen or primary display device as they did in previous versions of Windows.</span></span> <span data-ttu-id="463ac-112">Вместо этого их Рисование перенаправляется на экранные поверхности в видеопамяти, которые затем подготавливаются к просмотру в виде изображения на рабочем столе и отображаются на экране.</span><span class="sxs-lookup"><span data-stu-id="463ac-112">Instead, their drawing is redirected to off-screen surfaces in video memory, which are then rendered into a desktop image and presented on the display.</span></span>

<span data-ttu-id="463ac-113">Композиция рабочего стола выполняется диспетчер окон рабочего стола (DWM).</span><span class="sxs-lookup"><span data-stu-id="463ac-113">Desktop composition is performed by the Desktop Window Manager (DWM).</span></span> <span data-ttu-id="463ac-114">С помощью композиции рабочего стола DWM обеспечивает визуальные эффекты на настольном компьютере, а также различные функции, такие как стеклянные фреймы окна, трехмерные анимации перемещения окон, Windows Flip3D и поддержка высокого разрешения.</span><span class="sxs-lookup"><span data-stu-id="463ac-114">Through desktop composition, DWM enables visual effects on the desktop as well as various features such as glass window frames, 3-D window transition animations, Windows Flip and Windows Flip3D, and high resolution support.</span></span>

<span data-ttu-id="463ac-115">Диспетчер окон рабочего стола выполняется как служба Windows.</span><span class="sxs-lookup"><span data-stu-id="463ac-115">The Desktop Window Manager runs as a Windows service.</span></span> <span data-ttu-id="463ac-116">Его можно включить и отключить с помощью элемента панели управления "Администрирование" в разделе "службы" как диспетчер окон рабочего стола диспетчер сеансов.</span><span class="sxs-lookup"><span data-stu-id="463ac-116">It can be enabled and disabled through the Administrative Tools Control Panel item, under Services, as Desktop Window Manager Session Manager.</span></span>

<span data-ttu-id="463ac-117">Многие функции DWM могут управляться приложением или обращаться к ним через API DWM.</span><span class="sxs-lookup"><span data-stu-id="463ac-117">Many of the DWM features can be controlled or accessed by an application through the DWM APIs.</span></span> <span data-ttu-id="463ac-118">В следующей документации описываются функции и требования интерфейсов API DWM.</span><span class="sxs-lookup"><span data-stu-id="463ac-118">The following documentation describes the features and requirements of the DWM APIs.</span></span>

-   [<span data-ttu-id="463ac-119">Обзоры DWM</span><span class="sxs-lookup"><span data-stu-id="463ac-119">DWM Overviews</span></span>](desktop-window-manager-overviews.md)
-   [<span data-ttu-id="463ac-120">Образец кода DWM</span><span class="sxs-lookup"><span data-stu-id="463ac-120">DWM Sample Code</span></span>](dwm-samples.md)
-   [<span data-ttu-id="463ac-121">Справочник по DWM</span><span class="sxs-lookup"><span data-stu-id="463ac-121">DWM Reference</span></span>](reference.md)

 

 




