---
title: Определение того, может ли драйвер управлять входным форматом
description: Определение того, может ли драйвер управлять входным форматом
ms.assetid: 456eab43-d830-4a28-b724-3ef35b852372
keywords:
- Диспетчер сжатия видео (ВКМ), формат ввода
- ВКМ (диспетчер сжатия видео), формат ввода
- Макрос Икдравкуери
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07b3e2da69f8c061a7d0aefe847f40113d5104d8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067957"
---
# <a name="determining-if-a-driver-can-handle-the-input-format"></a><span data-ttu-id="a0a9a-106">Определение того, может ли драйвер управлять входным форматом</span><span class="sxs-lookup"><span data-stu-id="a0a9a-106">Determining If a Driver Can Handle the Input Format</span></span>

<span data-ttu-id="a0a9a-107">В следующем примере показано, как проверить формат ввода с помощью макроса [**икдравкуери**](/windows/desktop/api/Vfw/nf-vfw-icdrawquery) .</span><span class="sxs-lookup"><span data-stu-id="a0a9a-107">The following example shows how to check the input format with the [**ICDrawQuery**](/windows/desktop/api/Vfw/nf-vfw-icdrawquery) macro.</span></span>


```C++
// lpbiIn points to BITMAPINFOHEADER structure indicating the input 
// format. 

if (ICDrawQuery(hIC, lpbiIn) == ICERR_OK) 
{ 
    // Driver recognizes the input format. 
} 
else 
{ 
    // Need a different decompressor. 
} 
 
```



 

 




