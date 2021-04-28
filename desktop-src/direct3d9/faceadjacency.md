---
description: Фацеаджаценци — этот шаблон создается на основе отдельной сетки, и в нем хранятся сведения о том, какие вершины в этой сетке дублируются друг от друга.
ms.assetid: dd30b3d6-767a-4d87-9b5c-1324738bcbb2
title: фацеаджаценци
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0508b822f45c6796a793dc4b17caeaa1e30b4c3d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090512"
---
# <a name="faceadjacency"></a><span data-ttu-id="1b728-103">фацеаджаценци</span><span class="sxs-lookup"><span data-stu-id="1b728-103">FaceAdjacency</span></span>

<span data-ttu-id="1b728-104">Этот шаблон создается отдельно для каждой сетки и содержит сведения о том, какие вершины в этой сетке дублируются друг от друга.</span><span class="sxs-lookup"><span data-stu-id="1b728-104">This template is instantiated on a per-mesh basis, holding information about which vertices in the mesh are duplicates of each other.</span></span> <span data-ttu-id="1b728-105">Дублирует результат, если вершина находится в группе сглаживания или на границе материала.</span><span class="sxs-lookup"><span data-stu-id="1b728-105">Duplicates result when a vertex sits on a smoothing group or material boundary.</span></span> <span data-ttu-id="1b728-106">Этот шаблон предназначен для того, чтобы загрузчик определил, какие вершины, появляющиеся различными параметрами периферийных устройств, на самом деле являются вершинами в модели.</span><span class="sxs-lookup"><span data-stu-id="1b728-106">The purpose of this template is to allow the loader to determine which vertices exhibiting different peripheral parameters are actually the same vertexes in the model.</span></span> <span data-ttu-id="1b728-107">Некоторые приложения (например, упрощение сетки) могут использовать эти сведения.</span><span class="sxs-lookup"><span data-stu-id="1b728-107">Certain applications (mesh simplification, for example) can make use of this information.</span></span>

``` syntax
template FaceAdjacency
{
    < A64C844A-E282-4756-8B80-250CDE04398C >
    DWORD nIndices;
    array DWORD indices[nIndices];
} 
```

<span data-ttu-id="1b728-108">Где:</span><span class="sxs-lookup"><span data-stu-id="1b728-108">Where:</span></span>

-   <span data-ttu-id="1b728-109">Ниндицес — количество индексов в сетке.</span><span class="sxs-lookup"><span data-stu-id="1b728-109">nIndices - Number of indices in the mesh.</span></span>
-   <span data-ttu-id="1b728-110">индексы \[ ниндицес \] — массив индексов.</span><span class="sxs-lookup"><span data-stu-id="1b728-110">indices\[nIndices\] - Array of indices.</span></span>

## <a name="see-also"></a><span data-ttu-id="1b728-111">См. также</span><span class="sxs-lookup"><span data-stu-id="1b728-111">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b728-112">Шаблоны</span><span class="sxs-lookup"><span data-stu-id="1b728-112">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



