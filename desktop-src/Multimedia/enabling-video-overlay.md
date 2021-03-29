---
title: Включение наложения видео
description: Включение наложения видео
ms.assetid: f0b4f24c-3e35-4a18-ac77-8cae7083b0fe
keywords:
- макрос Капдривержеткапс
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ce51a3b7c77fbb161007ddde7dfe91c36152121
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103779142"
---
# <a name="enabling-video-overlay"></a><span data-ttu-id="76eba-104">Включение наложения видео</span><span class="sxs-lookup"><span data-stu-id="76eba-104">Enabling Video Overlay</span></span>

<span data-ttu-id="76eba-105">В следующем примере с помощью макроса [**капдривержеткапс**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetcaps) определяется, есть ли у драйвера записи возможности наложения. Если это так, макрос включает наложение.</span><span class="sxs-lookup"><span data-stu-id="76eba-105">The following example uses the [**capDriverGetCaps**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetcaps) macro to determine whether a capture driver has overlay capabilities; if it does, the macro enables the overlay.</span></span>


```C++
CAPDRIVERCAPS CapDrvCaps; 

capDriverGetCaps(hWndC, &CapDrvCaps, sizeof (CAPDRIVERCAPS)); 

if (CapDrvCaps.fHasOverlay) 
    capOverlay(hWndC, TRUE);
 
```



## <a name="related-topics"></a><span data-ttu-id="76eba-106">См. также</span><span class="sxs-lookup"><span data-stu-id="76eba-106">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="76eba-107">Использование видеозаписи</span><span class="sxs-lookup"><span data-stu-id="76eba-107">Using Video Capture</span></span>](using-video-capture.md)
</dt> </dl>

 

 




