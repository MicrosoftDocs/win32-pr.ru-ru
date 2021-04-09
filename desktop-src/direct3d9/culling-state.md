---
description: Чтобы повысить производительность отрисовки, можно исключать (или удалять) примитив, который отрывается от камеры.
ms.assetid: b4b8ff3f-aa20-4422-8f6f-34cae25de0e6
title: Состояние отбора (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad86e71fd7c6543f0d232e32a630d73e0ebbadae
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141965"
---
# <a name="culling-state-direct3d-9"></a><span data-ttu-id="afe76-103">Состояние отбора (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="afe76-103">Culling State (Direct3D 9)</span></span>

<span data-ttu-id="afe76-104">Чтобы повысить производительность отрисовки, можно исключать (или удалять) примитив, который отрывается от камеры.</span><span class="sxs-lookup"><span data-stu-id="afe76-104">To improve rendering performance, you can cull out (or remove) a primitive that faces away from the camera.</span></span> <span data-ttu-id="afe76-105">Для односторонних примитивов это экономит время отрисовки, так как задняя сторона не видна.</span><span class="sxs-lookup"><span data-stu-id="afe76-105">For single-sided primitives, this saves rendering time because a back-face is not visible.</span></span> <span data-ttu-id="afe76-106">Чтобы включить отбор, необходимо знать порядок поворота вершин (обычно в противном случае — по часовой стрелке).</span><span class="sxs-lookup"><span data-stu-id="afe76-106">To enable culling, you need to know the winding order of the vertices (typically counter-clockwise).</span></span> <span data-ttu-id="afe76-107">В этом примере удаляется все примитивы, для которых обратная поверхность направлена вперед (по часовой стрелке):</span><span class="sxs-lookup"><span data-stu-id="afe76-107">This example will remove any primitive whose back face is facing forward (given a counter-clockwise winding order):</span></span>


```
SetRenderState(D3DRS_CULLMODE, D3DCULL_CCW);
```



## <a name="related-topics"></a><span data-ttu-id="afe76-108">См. также</span><span class="sxs-lookup"><span data-stu-id="afe76-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="afe76-109">Состояния отрисовки</span><span class="sxs-lookup"><span data-stu-id="afe76-109">Render States</span></span>](render-states.md)
</dt> </dl>

 

 



