---
description: Определяет сетку, определенную с помощью исправлений Безье. Первый массив представляет собой список вершин, а второй массив определяет исправления для сетки путем индексирования в массиве вершин.
ms.assetid: 642ca513-c83e-4c6d-845c-0eaecc232728
title: PatchMesh9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b3d8232fe8c83358feb216acfb45a7877d7acb9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105692002"
---
# <a name="patchmesh9"></a><span data-ttu-id="5a7a0-104">PatchMesh9</span><span class="sxs-lookup"><span data-stu-id="5a7a0-104">PatchMesh9</span></span>

<span data-ttu-id="5a7a0-105">Определяет сетку, определенную с помощью исправлений Безье.</span><span class="sxs-lookup"><span data-stu-id="5a7a0-105">Defines a mesh defined by Bézier patches.</span></span> <span data-ttu-id="5a7a0-106">Первый массив представляет собой список вершин, а второй массив определяет исправления для сетки путем индексирования в массиве вершин.</span><span class="sxs-lookup"><span data-stu-id="5a7a0-106">The first array is a list of vertices, and the second array defines the patches for the mesh by indexing into the vertex array.</span></span>

``` syntax
template PatchMesh9
{
    < B9EC94E1-B9A6-4251-BA18-94893F02C0EA >
    DWORD Type;
    DWORD Degree;
    DWORD Basis;
    DWORD nVertices;
    array Vector vertices[nVertices];
    DWORD nPatches;
    array Patch patches[nPatches];
    [ ... ]
} 
```

<span data-ttu-id="5a7a0-107">Где:</span><span class="sxs-lookup"><span data-stu-id="5a7a0-107">Where:</span></span>

-   <span data-ttu-id="5a7a0-108">Тип сетки типа исправления: прямоугольник, треугольник или N-patch.</span><span class="sxs-lookup"><span data-stu-id="5a7a0-108">Type - Patch mesh type: rectangle, triangle, or N-patch.</span></span>
-   <span data-ttu-id="5a7a0-109">Градусы переменных в уравнении кривой.</span><span class="sxs-lookup"><span data-stu-id="5a7a0-109">Degree - Degree of the variables in the curve equation.</span></span>
-   <span data-ttu-id="5a7a0-110">Базовый тип поверхности исправления высокого порядка.</span><span class="sxs-lookup"><span data-stu-id="5a7a0-110">Basis - Basis type of a high-order patch surface.</span></span>
-   <span data-ttu-id="5a7a0-111">Нвертицес — число вершин.</span><span class="sxs-lookup"><span data-stu-id="5a7a0-111">nVertices - Number of vertices.</span></span>
-   <span data-ttu-id="5a7a0-112">вершины \[ нвертицес \] — массив вершин.</span><span class="sxs-lookup"><span data-stu-id="5a7a0-112">vertices\[nVertices\] - Array of vertices.</span></span> <span data-ttu-id="5a7a0-113">См. раздел [**vector**](vector.md).</span><span class="sxs-lookup"><span data-stu-id="5a7a0-113">See [**Vector**](vector.md).</span></span>
-   <span data-ttu-id="5a7a0-114">Нпатчес — число исправлений.</span><span class="sxs-lookup"><span data-stu-id="5a7a0-114">nPatches - Number of patches.</span></span>
-   <span data-ttu-id="5a7a0-115">исправления \[ нпатчес \] — массив исправлений.</span><span class="sxs-lookup"><span data-stu-id="5a7a0-115">patches\[nPatches\] - Array of patches.</span></span> <span data-ttu-id="5a7a0-116">См. [**исправление**](patch.md).</span><span class="sxs-lookup"><span data-stu-id="5a7a0-116">See [**Patch**](patch.md).</span></span>
-   <span data-ttu-id="5a7a0-117">\[ ... \] -Здесь можно использовать любой шаблон файла. x.</span><span class="sxs-lookup"><span data-stu-id="5a7a0-117">\[ ... \] - Any .x file template can be used here.</span></span> <span data-ttu-id="5a7a0-118">Это делает архитектуру расширяемой.</span><span class="sxs-lookup"><span data-stu-id="5a7a0-118">This makes the architecture extensible.</span></span>

<span data-ttu-id="5a7a0-119">Исправления используют вершины в массиве вершин в качестве контрольных точек для каждого исправления.</span><span class="sxs-lookup"><span data-stu-id="5a7a0-119">The patches use the vertices in the array of vertices as the control points for each patch.</span></span>

## <a name="see-also"></a><span data-ttu-id="5a7a0-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5a7a0-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a7a0-121">Шаблоны</span><span class="sxs-lookup"><span data-stu-id="5a7a0-121">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



