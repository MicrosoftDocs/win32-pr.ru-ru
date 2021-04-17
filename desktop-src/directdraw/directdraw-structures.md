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
# <a name="directdraw-structures"></a>Структуры DirectDraw

В этом разделе содержатся сведения о следующих структурах, используемых в DirectDraw:

-   [**ддблтбатч**](/windows/desktop/api/Ddraw/ns-ddraw-ddbltbatch)
-   [**ддблтфкс**](/windows/desktop/api/Ddraw/ns-ddraw-ddbltfx)
-   [**ддкапс**](/windows/desktop/api/Ddraw/ns-ddraw-ddcaps_dx3)
-   [**ддколорконтрол**](/windows/win32/api/ddraw/nn-ddraw-idirectdrawcolorcontrol)
-   [**ддколоркэй**](/windows/desktop/api/Ddraw/ns-ddraw-ddcolorkey)
-   [**DDDEVICEIDENTIFIER2**](/windows/win32/api/ddraw/ns-ddraw-dddeviceidentifier2)
-   [**ддгаммарамп**](/windows/desktop/api/Ddraw/ns-ddraw-ddgammaramp)
-   [**ддоверлайфкс**](/windows/desktop/api/Ddraw/ns-ddraw-ddoverlayfx)
-   [**ддпикселформат**](/windows/desktop/api/Ddraw/ns-ddraw-ddpixelformat)
-   [**ддскапс**](/previous-versions/ms783271(v=vs.85))
-   [**DDSCAPS2**](/previous-versions/bb943980(v=vs.85))
-   [**ддсурфацедеск**](/previous-versions/ms783272(v=vs.85))
-   [**DDSURFACEDESC2**](/previous-versions/bb943981(v=vs.85))

> [!Note]  
> Перед использованием структуры необходимо инициализировать память для каждой структуры DirectX до 0. Кроме того, для всех структур, содержащих элемент **двсизе** , необходимо задать для элемента размер структуры (в байтах) перед использованием структуры. В следующем примере выполняются эти задачи в общей структуре, [**ддкапс**](/windows/desktop/api/Ddraw/ns-ddraw-ddcaps_dx3):

 


```
DDCAPS ddcaps; // You cannot use this yet.
 
ZeroMemory(&ddcaps, sizeof(DDCAPS));
ddcaps.dwSize = sizeof(DDCAPS);
 
// Now you can use the structure.
.
.
```



 

 




