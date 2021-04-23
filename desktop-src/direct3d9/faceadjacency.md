---
description: Этот шаблон создается отдельно для каждой сетки и содержит сведения о том, какие вершины в этой сетке дублируются друг от друга.
ms.assetid: dd30b3d6-767a-4d87-9b5c-1324738bcbb2
title: фацеаджаценци
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a2fd0f0b2bb328aa8b5ec39e7481c0b7fd766fc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103805327"
---
# <a name="faceadjacency"></a><span data-ttu-id="8b1ba-103">фацеаджаценци</span><span class="sxs-lookup"><span data-stu-id="8b1ba-103">FaceAdjacency</span></span>

<span data-ttu-id="8b1ba-104">Этот шаблон создается отдельно для каждой сетки и содержит сведения о том, какие вершины в этой сетке дублируются друг от друга.</span><span class="sxs-lookup"><span data-stu-id="8b1ba-104">This template is instantiated on a per-mesh basis, holding information about which vertices in the mesh are duplicates of each other.</span></span> <span data-ttu-id="8b1ba-105">Дублирует результат, если вершина находится в группе сглаживания или на границе материала.</span><span class="sxs-lookup"><span data-stu-id="8b1ba-105">Duplicates result when a vertex sits on a smoothing group or material boundary.</span></span> <span data-ttu-id="8b1ba-106">Этот шаблон предназначен для того, чтобы загрузчик определил, какие вершины, появляющиеся различными параметрами периферийных устройств, на самом деле являются вершинами в модели.</span><span class="sxs-lookup"><span data-stu-id="8b1ba-106">The purpose of this template is to allow the loader to determine which vertices exhibiting different peripheral parameters are actually the same vertexes in the model.</span></span> <span data-ttu-id="8b1ba-107">Некоторые приложения (например, упрощение сетки) могут использовать эти сведения.</span><span class="sxs-lookup"><span data-stu-id="8b1ba-107">Certain applications (mesh simplification, for example) can make use of this information.</span></span>

``` syntax
template FaceAdjacency
{
    < A64C844A-E282-4756-8B80-250CDE04398C >
    DWORD nIndices;
    array DWORD indices[nIndices];
} 
```

<span data-ttu-id="8b1ba-108">Где:</span><span class="sxs-lookup"><span data-stu-id="8b1ba-108">Where:</span></span>

-   <span data-ttu-id="8b1ba-109">Ниндицес — количество индексов в сетке.</span><span class="sxs-lookup"><span data-stu-id="8b1ba-109">nIndices - Number of indices in the mesh.</span></span>
-   <span data-ttu-id="8b1ba-110">индексы \[ ниндицес \] — массив индексов.</span><span class="sxs-lookup"><span data-stu-id="8b1ba-110">indices\[nIndices\] - Array of indices.</span></span>

## <a name="see-also"></a><span data-ttu-id="8b1ba-111">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8b1ba-111">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b1ba-112">Шаблоны</span><span class="sxs-lookup"><span data-stu-id="8b1ba-112">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



