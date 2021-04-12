---
description: Анимированная анимация вершин объединяет две предоставляемые пользователем положения (или нормали).
ms.assetid: vs|directx_sdk|~\vertex_tweening.htm
title: Анимированная анимация вершин (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7a5458e384fa69b91b1eab1623fb526d514591f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104262404"
---
# <a name="vertex-tweening-direct3d-9"></a><span data-ttu-id="0153a-103">Анимированная анимация вершин (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="0153a-103">Vertex Tweening (Direct3D 9)</span></span>

<span data-ttu-id="0153a-104">Анимированная анимация вершин объединяет две предоставляемые пользователем положения (или нормали).</span><span class="sxs-lookup"><span data-stu-id="0153a-104">Vertex tweening blends two user-provided positions (or normals).</span></span> <span data-ttu-id="0153a-105">Tween-анимация является взаимоисключающей из смешения вершин с весовыми коэффициентами.</span><span class="sxs-lookup"><span data-stu-id="0153a-105">Tweening is mutually exclusive from vertex blending with weights.</span></span> <span data-ttu-id="0153a-106">Tween-анимация выполняется до освещения и обрезки и включается путем установки D3DRS \_ вертексбленд в D3DVBF \_ tween-анимации.</span><span class="sxs-lookup"><span data-stu-id="0153a-106">Tweening is performed before lighting and clipping, and is enabled by setting D3DRS\_VERTEXBLEND to D3DVBF\_TWEENING.</span></span> <span data-ttu-id="0153a-107">Результирующая вершина вершины вычислена следующим образом:</span><span class="sxs-lookup"><span data-stu-id="0153a-107">The resulting vertex position is computed by:</span></span>


```
POSITION = POSITION1 * (1.0 - TWEENFACTOR) + POSITION2 * TWEENFACTOR
```



<span data-ttu-id="0153a-108">Для вычисления нормалей используется тот же подход.</span><span class="sxs-lookup"><span data-stu-id="0153a-108">The same approach is used for calculating normals.</span></span> <span data-ttu-id="0153a-109">Дополнительные сведения см. [в разделе Использование анимации по вершинам (Direct3D 9)](using-vertex-tweening.md).</span><span class="sxs-lookup"><span data-stu-id="0153a-109">For more information, see [Using Vertex Tweening (Direct3D 9)](using-vertex-tweening.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="0153a-110">См. также</span><span class="sxs-lookup"><span data-stu-id="0153a-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0153a-111">Смешение геометрических объектов</span><span class="sxs-lookup"><span data-stu-id="0153a-111">Geometry Blending</span></span>](geometry-blending.md)
</dt> </dl>

 

 



