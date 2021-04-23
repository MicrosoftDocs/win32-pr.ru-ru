---
description: Подсистема освещения Direct3D может использовать данные цвета каждого вершины при выполнении освещения, если вы сообщаете среде выполнения о наличии данных.
ms.assetid: acb43921-f0d4-4151-9371-1b99e5d30c0e
title: Состояние цвета Per-Vertex (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e0104b427753fa3d7b7cf5a0a5a10cfeb5d10f2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104416404"
---
# <a name="per-vertex-color-state-direct3d-9"></a><span data-ttu-id="ba964-103">Состояние цвета Per-Vertex (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="ba964-103">Per-Vertex Color State (Direct3D 9)</span></span>

<span data-ttu-id="ba964-104">Подсистема освещения Direct3D может использовать данные цвета каждого вершины при выполнении освещения, если вы сообщаете среде выполнения о наличии данных.</span><span class="sxs-lookup"><span data-stu-id="ba964-104">The Direct3D lighting engine can use per-vertex color data when performing lighting if you tell the runtime the data is present.</span></span> <span data-ttu-id="ba964-105">Для этого необходимо включить следующее состояние визуализации:</span><span class="sxs-lookup"><span data-stu-id="ba964-105">This is done by turning on the following render state:</span></span>


```
// disable per-vertex color
SetRenderState(D3DRS_COLORVERTEX, FALSE);

// enable per-vertex color
SetRenderState(D3DRS_COLORVERTEX, TRUE);
```



<span data-ttu-id="ba964-106">Если включен цвет на уровне вершины, то приложения могут настраивать источник, из которого система получает сведения о цвете для вершины.</span><span class="sxs-lookup"><span data-stu-id="ba964-106">If per-vertex color is enabled, applications can configure the source from which the system retrieves color information for a vertex.</span></span> <span data-ttu-id="ba964-107">D3DRS \_ амбиентматериалсаурце, D3DRS \_ ДИФФУСЕМАТЕРИАЛСАУРЦЕ, D3DRS \_ емиссивематериалсаурце и D3DRS \_ спекуларматериалсаурце отображают источники для управления внешними, рассеянными, эмиссионный и отражающими цветовыми компонентами соответственно.</span><span class="sxs-lookup"><span data-stu-id="ba964-107">The D3DRS\_AMBIENTMATERIALSOURCE, D3DRS\_DIFFUSEMATERIALSOURCE, D3DRS\_EMISSIVEMATERIALSOURCE, and D3DRS\_SPECULARMATERIALSOURCE render states control the ambient, diffuse, emissive, and specular color component sources, respectively.</span></span> <span data-ttu-id="ba964-108">Каждое состояние может быть задано для членов перечисляемого типа [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) , который определяет константы, которые указывают системе на использование текущего материала, рассеянного цвета или отраженного цвета в качестве источника для указанного компонента цвета.</span><span class="sxs-lookup"><span data-stu-id="ba964-108">Each state can be set to members of the [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) enumerated type, which defines constants that instruct the system to use the current material, diffuse color, or specular color as the source for the specified color component.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ba964-109">См. также</span><span class="sxs-lookup"><span data-stu-id="ba964-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ba964-110">Состояния отрисовки</span><span class="sxs-lookup"><span data-stu-id="ba964-110">Render States</span></span>](render-states.md)
</dt> </dl>

 

 
