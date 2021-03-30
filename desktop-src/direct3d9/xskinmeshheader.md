---
description: Этот шаблон создается на основе отдельной сетки только в тех сетках, которые содержат экспортированные сведения о обложках. Этот шаблон предназначен для предоставления сведений о характере экспортированной информации о обложках.
ms.assetid: 95a4fa45-63d1-4931-9c91-b26807d2b043
title: ксскинмешхеадер
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 306f8c183086846fca020040af00b9ccef2665cc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104423053"
---
# <a name="xskinmeshheader"></a><span data-ttu-id="4bfc9-104">ксскинмешхеадер</span><span class="sxs-lookup"><span data-stu-id="4bfc9-104">XSkinMeshHeader</span></span>

<span data-ttu-id="4bfc9-105">Этот шаблон создается на основе отдельной сетки только в тех сетках, которые содержат экспортированные сведения о обложках.</span><span class="sxs-lookup"><span data-stu-id="4bfc9-105">This template is instantiated on a per-mesh basis only in meshes that contain exported skinning information.</span></span> <span data-ttu-id="4bfc9-106">Этот шаблон предназначен для предоставления сведений о характере экспортированной информации о обложках.</span><span class="sxs-lookup"><span data-stu-id="4bfc9-106">The purpose of this template is to provide information about the nature of the skinning information that was exported.</span></span>

``` syntax
template XSkinMeshHeader 
{ 
    < 3CF169CE-FF7C-44ab-93C0-F78F62D172E2 >  
    WORD nMaxSkinWeightsPerVertex; 
    WORD nMaxSkinWeightsPerFace; 
    WORD nBones; 
}
```

<span data-ttu-id="4bfc9-107">Где:</span><span class="sxs-lookup"><span data-stu-id="4bfc9-107">Where:</span></span>

-   <span data-ttu-id="4bfc9-108">Нмаксскинвеигхтспервертекс — максимальное число преобразований, влияющих на вершину сетки.</span><span class="sxs-lookup"><span data-stu-id="4bfc9-108">nMaxSkinWeightsPerVertex - Maximum number of transforms that affect a vertex in the mesh.</span></span>
-   <span data-ttu-id="4bfc9-109">Нмаксскинвеигхтсперфаце — максимальное число уникальных преобразований, влияющих на три вершины любой грани.</span><span class="sxs-lookup"><span data-stu-id="4bfc9-109">nMaxSkinWeightsPerFace - Maximum number of unique transforms that affect the three vertices of any face.</span></span>
-   <span data-ttu-id="4bfc9-110">Нбонес — число костей, влияющих на вершины в этой сетке.</span><span class="sxs-lookup"><span data-stu-id="4bfc9-110">nBones - Number of bones that affect vertices in this mesh.</span></span>

## <a name="see-also"></a><span data-ttu-id="4bfc9-111">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4bfc9-111">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4bfc9-112">Шаблоны</span><span class="sxs-lookup"><span data-stu-id="4bfc9-112">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



