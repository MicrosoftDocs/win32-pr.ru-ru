---
title: Структуры DirectDraw
description: В этом разделе содержатся сведения о следующих структурах, используемых с DirectDraw.
ms.assetid: 36424B41-B179-414A-ACFF-E63DA7B27043
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52cf24c71da3f022833c6ecf9843e996df2c514b
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/20/2020
ms.locfileid: "105691710"
---
# <a name="directdraw-structures"></a><span data-ttu-id="d38a5-103">Структуры DirectDraw</span><span class="sxs-lookup"><span data-stu-id="d38a5-103">DirectDraw Structures</span></span>

<span data-ttu-id="d38a5-104">В этом разделе содержатся сведения о следующих структурах, используемых в DirectDraw:</span><span class="sxs-lookup"><span data-stu-id="d38a5-104">This section contains information about the following structures used with DirectDraw:</span></span>

-   [<span data-ttu-id="d38a5-105">**ддблтбатч**</span><span class="sxs-lookup"><span data-stu-id="d38a5-105">**DDBLTBATCH**</span></span>](/windows/desktop/api/Ddraw/ns-ddraw-ddbltbatch)
-   [<span data-ttu-id="d38a5-106">**ддблтфкс**</span><span class="sxs-lookup"><span data-stu-id="d38a5-106">**DDBLTFX**</span></span>](/windows/desktop/api/Ddraw/ns-ddraw-ddbltfx)
-   [<span data-ttu-id="d38a5-107">**ддкапс**</span><span class="sxs-lookup"><span data-stu-id="d38a5-107">**DDCAPS**</span></span>](/windows/desktop/api/Ddraw/ns-ddraw-ddcaps_dx3)
-   [<span data-ttu-id="d38a5-108">**ддколорконтрол**</span><span class="sxs-lookup"><span data-stu-id="d38a5-108">**DDCOLORCONTROL**</span></span>](/windows/win32/api/ddraw/nn-ddraw-idirectdrawcolorcontrol)
-   [<span data-ttu-id="d38a5-109">**ддколоркэй**</span><span class="sxs-lookup"><span data-stu-id="d38a5-109">**DDCOLORKEY**</span></span>](/windows/desktop/api/Ddraw/ns-ddraw-ddcolorkey)
-   [<span data-ttu-id="d38a5-110">**DDDEVICEIDENTIFIER2**</span><span class="sxs-lookup"><span data-stu-id="d38a5-110">**DDDEVICEIDENTIFIER2**</span></span>](/windows/win32/api/ddraw/ns-ddraw-dddeviceidentifier2)
-   [<span data-ttu-id="d38a5-111">**ддгаммарамп**</span><span class="sxs-lookup"><span data-stu-id="d38a5-111">**DDGAMMARAMP**</span></span>](/windows/desktop/api/Ddraw/ns-ddraw-ddgammaramp)
-   [<span data-ttu-id="d38a5-112">**ддоверлайфкс**</span><span class="sxs-lookup"><span data-stu-id="d38a5-112">**DDOVERLAYFX**</span></span>](/windows/desktop/api/Ddraw/ns-ddraw-ddoverlayfx)
-   [<span data-ttu-id="d38a5-113">**ддпикселформат**</span><span class="sxs-lookup"><span data-stu-id="d38a5-113">**DDPIXELFORMAT**</span></span>](/windows/desktop/api/Ddraw/ns-ddraw-ddpixelformat)
-   <span data-ttu-id="d38a5-114">[**ддскапс**](/previous-versions/ms783271(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d38a5-114">[**DDSCAPS**](/previous-versions/ms783271(v=vs.85))</span></span>
-   <span data-ttu-id="d38a5-115">[**DDSCAPS2**](/previous-versions/bb943980(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d38a5-115">[**DDSCAPS2**](/previous-versions/bb943980(v=vs.85))</span></span>
-   <span data-ttu-id="d38a5-116">[**ддсурфацедеск**](/previous-versions/ms783272(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d38a5-116">[**DDSURFACEDESC**](/previous-versions/ms783272(v=vs.85))</span></span>
-   <span data-ttu-id="d38a5-117">[**DDSURFACEDESC2**](/previous-versions/bb943981(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d38a5-117">[**DDSURFACEDESC2**](/previous-versions/bb943981(v=vs.85))</span></span>

> [!Note]  
> <span data-ttu-id="d38a5-118">Перед использованием структуры необходимо инициализировать память для каждой структуры DirectX до 0.</span><span class="sxs-lookup"><span data-stu-id="d38a5-118">You should initialize the memory for each DirectX structure to 0 before you use the structure.</span></span> <span data-ttu-id="d38a5-119">Кроме того, для всех структур, содержащих элемент **двсизе** , необходимо задать для элемента размер структуры (в байтах) перед использованием структуры.</span><span class="sxs-lookup"><span data-stu-id="d38a5-119">In addition, for all structures that contain a **dwSize** member, you should set the member to the size of the structure, in bytes, before the structure is used.</span></span> <span data-ttu-id="d38a5-120">В следующем примере выполняются эти задачи в общей структуре, [**ддкапс**](/windows/desktop/api/Ddraw/ns-ddraw-ddcaps_dx3):</span><span class="sxs-lookup"><span data-stu-id="d38a5-120">The following example performs these tasks on a common structure, [**DDCAPS**](/windows/desktop/api/Ddraw/ns-ddraw-ddcaps_dx3):</span></span>

 


```
DDCAPS ddcaps; // You cannot use this yet.
 
ZeroMemory(&ddcaps, sizeof(DDCAPS));
ddcaps.dwSize = sizeof(DDCAPS);
 
// Now you can use the structure.
.
.
```



 

 




