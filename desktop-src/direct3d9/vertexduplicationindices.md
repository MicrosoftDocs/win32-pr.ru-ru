---
description: Вертексдупликатиониндицес — этот шаблон создается на основе отдельной сетки, и в нем хранятся сведения о том, какие вершины в этой сетке дублируются друг от друга.
ms.assetid: 43417389-69c1-4af6-92c2-75b621f9c165
title: вертексдупликатиониндицес
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b33a8c5fca4f479eec6e9864d4528d4e3e4a1e32
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090182"
---
# <a name="vertexduplicationindices"></a><span data-ttu-id="bdea0-103">вертексдупликатиониндицес</span><span class="sxs-lookup"><span data-stu-id="bdea0-103">VertexDuplicationIndices</span></span>

<span data-ttu-id="bdea0-104">Этот шаблон создается отдельно для каждой сетки и содержит сведения о том, какие вершины в этой сетке дублируются друг от друга.</span><span class="sxs-lookup"><span data-stu-id="bdea0-104">This template is instantiated on a per-mesh basis, holding information about which vertices in the mesh are duplicates of each other.</span></span> <span data-ttu-id="bdea0-105">Дублирует результат, если вершина находится в группе сглаживания или на границе материала.</span><span class="sxs-lookup"><span data-stu-id="bdea0-105">Duplicates result when a vertex sits on a smoothing group or material boundary.</span></span> <span data-ttu-id="bdea0-106">Этот шаблон предназначен для того, чтобы загрузчик определил, какие вершины, появляющиеся различными параметрами периферийных устройств, на самом деле являются вершинами в модели.</span><span class="sxs-lookup"><span data-stu-id="bdea0-106">The purpose of this template is to allow the loader to determine which vertices exhibiting different peripheral parameters are actually the same vertexes in the model.</span></span> <span data-ttu-id="bdea0-107">Некоторые приложения (например, упрощение сетки) могут использовать эти сведения.</span><span class="sxs-lookup"><span data-stu-id="bdea0-107">Certain applications (mesh simplification, for example) can make use of this information.</span></span>

``` syntax
template VertexDuplicationIndices 
{ 
    < B8D65549-D7C9-4995-89CF-53A9A8B031E3 > 
    DWORD nIndices; 
    DWORD nOriginalVertices; 
    array DWORD indices[nIndices]; 
}
```

<span data-ttu-id="bdea0-108">Где:</span><span class="sxs-lookup"><span data-stu-id="bdea0-108">Where:</span></span>

-   <span data-ttu-id="bdea0-109">Ниндицес — число индексов вершин.</span><span class="sxs-lookup"><span data-stu-id="bdea0-109">nIndices - Number of vertex indices.</span></span> <span data-ttu-id="bdea0-110">Это число вершин в сетке.</span><span class="sxs-lookup"><span data-stu-id="bdea0-110">This is the number of vertices in the mesh.</span></span>
-   <span data-ttu-id="bdea0-111">Норигиналвертицес — число вершин в сети, прежде чем произойдет дублирование.</span><span class="sxs-lookup"><span data-stu-id="bdea0-111">nOriginalVertices - Number of vertices in the mesh before any duplication occurs.</span></span>
-   <span data-ttu-id="bdea0-112">Значения Indices \[ n \] содержат индекс вершин, в котором вершина \[ n \] в массиве вершин для сетки была бы имела место при отсутствии дублирования.</span><span class="sxs-lookup"><span data-stu-id="bdea0-112">The value indices\[n\] holds the vertex index that vertex\[n\] in the vertex array for the mesh would have had if no duplication had occurred.</span></span> <span data-ttu-id="bdea0-113">В этом массиве индексы совпадают, поэтому указываются дубликаты вершин.</span><span class="sxs-lookup"><span data-stu-id="bdea0-113">Indices in this array that are the same, therefore, indicate duplicate vertices.</span></span>

## <a name="see-also"></a><span data-ttu-id="bdea0-114">См. также</span><span class="sxs-lookup"><span data-stu-id="bdea0-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bdea0-115">Шаблоны</span><span class="sxs-lookup"><span data-stu-id="bdea0-115">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



