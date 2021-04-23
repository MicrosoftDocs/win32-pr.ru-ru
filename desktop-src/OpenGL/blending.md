---
title: Смешения
description: Смешивание сочетает в себе R, G, B и значения, которые хранятся в буфера кадров в соответствующем расположении.
ms.assetid: 02a78ce3-bb0a-4e9c-a2b1-6da8e95bcee5
keywords:
- Конвейер обработки OpenGL, смешивание
- смешение OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0fe7cd2893700d8015148fcc5c25707d19676c7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329939"
---
# <a name="blending"></a><span data-ttu-id="5664b-105">Смешения</span><span class="sxs-lookup"><span data-stu-id="5664b-105">Blending</span></span>

<span data-ttu-id="5664b-106">Смешивание сочетает в себе R, G, B и значения, которые хранятся в буфера кадров в соответствующем расположении.</span><span class="sxs-lookup"><span data-stu-id="5664b-106">Blending combines a fragment's R, G, B, and A values with those stored in the framebuffer at the corresponding location.</span></span> <span data-ttu-id="5664b-107">Смешивание, которое выполняется только в режиме RGBA, зависит от альфа-значения фрагмента и соответствующего текущего сохраненного пикселя. Он также может зависеть от значений RGB.</span><span class="sxs-lookup"><span data-stu-id="5664b-107">The blending, which is performed only in RGBA mode, depends on the alpha value of the fragment and that of the corresponding currently stored pixel; it may also depend on the RGB values.</span></span> <span data-ttu-id="5664b-108">Вы управляете наложением с помощью [**глблендфунк**](glblendfunc.md), в котором указываются исходные и целевые Коэффициенты смешения.</span><span class="sxs-lookup"><span data-stu-id="5664b-108">You control blending with [**glBlendFunc**](glblendfunc.md), with which you indicate the source and destination blending factors.</span></span>

 

 




