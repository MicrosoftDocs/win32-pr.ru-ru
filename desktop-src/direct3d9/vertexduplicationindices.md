---
description: Этот шаблон создается отдельно для каждой сетки и содержит сведения о том, какие вершины в этой сетке дублируются друг от друга.
ms.assetid: 43417389-69c1-4af6-92c2-75b621f9c165
title: вертексдупликатиониндицес
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42d62278c206032c9a2dfed6ce9b2cd36c5e7456
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105691970"
---
# <a name="vertexduplicationindices"></a><span data-ttu-id="22419-103">вертексдупликатиониндицес</span><span class="sxs-lookup"><span data-stu-id="22419-103">VertexDuplicationIndices</span></span>

<span data-ttu-id="22419-104">Этот шаблон создается отдельно для каждой сетки и содержит сведения о том, какие вершины в этой сетке дублируются друг от друга.</span><span class="sxs-lookup"><span data-stu-id="22419-104">This template is instantiated on a per-mesh basis, holding information about which vertices in the mesh are duplicates of each other.</span></span> <span data-ttu-id="22419-105">Дублирует результат, если вершина находится в группе сглаживания или на границе материала.</span><span class="sxs-lookup"><span data-stu-id="22419-105">Duplicates result when a vertex sits on a smoothing group or material boundary.</span></span> <span data-ttu-id="22419-106">Этот шаблон предназначен для того, чтобы загрузчик определил, какие вершины, появляющиеся различными параметрами периферийных устройств, на самом деле являются вершинами в модели.</span><span class="sxs-lookup"><span data-stu-id="22419-106">The purpose of this template is to allow the loader to determine which vertices exhibiting different peripheral parameters are actually the same vertexes in the model.</span></span> <span data-ttu-id="22419-107">Некоторые приложения (например, упрощение сетки) могут использовать эти сведения.</span><span class="sxs-lookup"><span data-stu-id="22419-107">Certain applications (mesh simplification, for example) can make use of this information.</span></span>

``` syntax
template VertexDuplicationIndices 
{ 
    < B8D65549-D7C9-4995-89CF-53A9A8B031E3 > 
    DWORD nIndices; 
    DWORD nOriginalVertices; 
    array DWORD indices[nIndices]; 
}
```

<span data-ttu-id="22419-108">Где:</span><span class="sxs-lookup"><span data-stu-id="22419-108">Where:</span></span>

-   <span data-ttu-id="22419-109">Ниндицес — число индексов вершин.</span><span class="sxs-lookup"><span data-stu-id="22419-109">nIndices - Number of vertex indices.</span></span> <span data-ttu-id="22419-110">Это число вершин в сетке.</span><span class="sxs-lookup"><span data-stu-id="22419-110">This is the number of vertices in the mesh.</span></span>
-   <span data-ttu-id="22419-111">Норигиналвертицес — число вершин в сети, прежде чем произойдет дублирование.</span><span class="sxs-lookup"><span data-stu-id="22419-111">nOriginalVertices - Number of vertices in the mesh before any duplication occurs.</span></span>
-   <span data-ttu-id="22419-112">Значения Indices \[ n \] содержат индекс вершин, в котором вершина \[ n \] в массиве вершин для сетки была бы имела место при отсутствии дублирования.</span><span class="sxs-lookup"><span data-stu-id="22419-112">The value indices\[n\] holds the vertex index that vertex\[n\] in the vertex array for the mesh would have had if no duplication had occurred.</span></span> <span data-ttu-id="22419-113">В этом массиве индексы совпадают, поэтому указываются дубликаты вершин.</span><span class="sxs-lookup"><span data-stu-id="22419-113">Indices in this array that are the same, therefore, indicate duplicate vertices.</span></span>

## <a name="see-also"></a><span data-ttu-id="22419-114">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="22419-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22419-115">Шаблоны</span><span class="sxs-lookup"><span data-stu-id="22419-115">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



