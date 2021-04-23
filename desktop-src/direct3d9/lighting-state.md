---
description: Если вы не лампочки с шейдером вершин или шейдером пикселей, вы можете использовать механизм освещения в среде выполнения.
ms.assetid: vs|directx_sdk|~\lighting_state.htm
title: Состояние освещения (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74f0e7b7ec4a8bcf0ee27c9bc1e643536819d8fc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105701099"
---
# <a name="lighting-state-direct3d-9"></a><span data-ttu-id="4ac20-103">Состояние освещения (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="4ac20-103">Lighting State (Direct3D 9)</span></span>

<span data-ttu-id="4ac20-104">Если вы не лампочки с шейдером вершин или шейдером пикселей, вы можете использовать механизм освещения в среде выполнения.</span><span class="sxs-lookup"><span data-stu-id="4ac20-104">If you do not light with a vertex shader or a pixel shader, you may choose to use the lighting engine in the runtime.</span></span> <span data-ttu-id="4ac20-105">Подсистема освещения требует, чтобы данные вершин содержали нормали для вершины, вершины без обычных данных будут формировать точку с нулевым значением во всех вычислениях освещения.</span><span class="sxs-lookup"><span data-stu-id="4ac20-105">The lighting engine requires that the vertex data contains per-vertex normals; vertices without normal data will generate a dot product of zero in all lighting computations.</span></span> <span data-ttu-id="4ac20-106">Вычисления освещения рассматриваются более подробно в [математике освещения (Direct3D 9)](mathematics-of-lighting.md).</span><span class="sxs-lookup"><span data-stu-id="4ac20-106">The lighting calculations are covered in more detail in [Mathematics of Lighting (Direct3D 9)](mathematics-of-lighting.md).</span></span>

<span data-ttu-id="4ac20-107">Чтобы включить механизм освещения, используйте:</span><span class="sxs-lookup"><span data-stu-id="4ac20-107">To enable the lighting engine, use:</span></span>


```
SetRenderState(D3DRS_LIGHTING, TRUE); 
```



## <a name="related-topics"></a><span data-ttu-id="4ac20-108">См. также</span><span class="sxs-lookup"><span data-stu-id="4ac20-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4ac20-109">Состояния отрисовки</span><span class="sxs-lookup"><span data-stu-id="4ac20-109">Render States</span></span>](render-states.md)
</dt> </dl>

 

 



