---
description: Этот шаблон создается отдельно для каждой сетки.
ms.assetid: ac5289c6-989c-43b4-9190-ac8f831a05f0
title: скинвеигхтс
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 759239a3a7ec8ebb608cf9ede6624105cee321b4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104536815"
---
# <a name="skinweights"></a><span data-ttu-id="ad385-103">скинвеигхтс</span><span class="sxs-lookup"><span data-stu-id="ad385-103">SkinWeights</span></span>

<span data-ttu-id="ad385-104">Этот шаблон создается отдельно для каждой сетки.</span><span class="sxs-lookup"><span data-stu-id="ad385-104">This template is instantiated on a per-mesh basis.</span></span> <span data-ttu-id="ad385-105">В пределах сетки будет отображаться последовательность из n экземпляров этого шаблона, где n — число костей (кадров файла X), влияющих на вершины в сетке.</span><span class="sxs-lookup"><span data-stu-id="ad385-105">Within a mesh, a sequence of n instances of this template will appear, where n is the number of bones (X file frames) that influence the vertices in the mesh.</span></span> <span data-ttu-id="ad385-106">Каждый экземпляр шаблона по сути определяет влияние определенной кости на сетку.</span><span class="sxs-lookup"><span data-stu-id="ad385-106">Each instance of the template basically defines the influence of a particular bone on the mesh.</span></span> <span data-ttu-id="ad385-107">Имеется список индексов вершин и соответствующий список весов.</span><span class="sxs-lookup"><span data-stu-id="ad385-107">There is a list of vertex indices, and a corresponding list of weights.</span></span>

``` syntax
template SkinWeights 
{ 
    < 6F0D123B-BAD2-4167-A0D0-80224F25FABB > 
    STRING transformNodeName; 
    DWORD nWeights; 
    array DWORD vertexIndices[nWeights]; 
    array float weights[nWeights]; 
    Matrix4x4 matrixOffset; 
} 
```

<span data-ttu-id="ad385-108">Где:</span><span class="sxs-lookup"><span data-stu-id="ad385-108">Where:</span></span>

-   <span data-ttu-id="ad385-109">Имя кости, для которой определяется воздействие, — Трансформноденаме, а Нвеигхтс — число вершин, затронутых этой костью.</span><span class="sxs-lookup"><span data-stu-id="ad385-109">The name of the bone whose influence is being defined is transformNodeName, and nWeights is the number of vertices affected by this bone.</span></span>
-   <span data-ttu-id="ad385-110">Вершины, на которые влияет эта кость, содержатся в Вертексиндицес, а весовые коэффициенты для каждого из вершин, влияющих на эту кость, содержатся в весовых коэффициентах.</span><span class="sxs-lookup"><span data-stu-id="ad385-110">The vertices influenced by this bone are contained in vertexIndices, and the weights for each of the vertices influenced by this bone are contained in weights.</span></span>
-   <span data-ttu-id="ad385-111">Матрица Матриксоффсет преобразует вершины сетки в пространство кости.</span><span class="sxs-lookup"><span data-stu-id="ad385-111">The matrix matrixOffset transforms the mesh vertices to the space of the bone.</span></span> <span data-ttu-id="ad385-112">При объединении с преобразованием кости это обеспечивает координаты сетки в мировом пространстве, как это влияет на кость.</span><span class="sxs-lookup"><span data-stu-id="ad385-112">When concatenated to the bone's transform, this provides the world space coordinates of the mesh as affected by the bone.</span></span> <span data-ttu-id="ad385-113">См. [**Matrix4x4**](matrix4x4.md).</span><span class="sxs-lookup"><span data-stu-id="ad385-113">See [**Matrix4x4**](matrix4x4.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="ad385-114">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ad385-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad385-115">Шаблоны</span><span class="sxs-lookup"><span data-stu-id="ad385-115">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



