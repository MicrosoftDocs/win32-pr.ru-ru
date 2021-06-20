---
description: PatchMesh9 определяет сетку, определенную с помощью исправлений Безье, включая список вершин и исправлений для сетки путем индексирования в массив вершин.
ms.assetid: 642ca513-c83e-4c6d-845c-0eaecc232728
title: PatchMesh9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 811e593117f2ec57a4718ea8078d96bcea87e71f
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404707"
---
# <a name="patchmesh9"></a><span data-ttu-id="ac5cc-103">PatchMesh9</span><span class="sxs-lookup"><span data-stu-id="ac5cc-103">PatchMesh9</span></span>

<span data-ttu-id="ac5cc-104">Определяет сетку, определенную с помощью исправлений Безье.</span><span class="sxs-lookup"><span data-stu-id="ac5cc-104">Defines a mesh defined by Bézier patches.</span></span> <span data-ttu-id="ac5cc-105">Первый массив представляет собой список вершин, а второй массив определяет исправления для сетки путем индексирования в массиве вершин.</span><span class="sxs-lookup"><span data-stu-id="ac5cc-105">The first array is a list of vertices, and the second array defines the patches for the mesh by indexing into the vertex array.</span></span>

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

<span data-ttu-id="ac5cc-106">Где:</span><span class="sxs-lookup"><span data-stu-id="ac5cc-106">Where:</span></span>

-   <span data-ttu-id="ac5cc-107">Тип сетки типа исправления: прямоугольник, треугольник или N-patch.</span><span class="sxs-lookup"><span data-stu-id="ac5cc-107">Type - Patch mesh type: rectangle, triangle, or N-patch.</span></span>
-   <span data-ttu-id="ac5cc-108">Градусы переменных в уравнении кривой.</span><span class="sxs-lookup"><span data-stu-id="ac5cc-108">Degree - Degree of the variables in the curve equation.</span></span>
-   <span data-ttu-id="ac5cc-109">Базовый тип поверхности исправления высокого порядка.</span><span class="sxs-lookup"><span data-stu-id="ac5cc-109">Basis - Basis type of a high-order patch surface.</span></span>
-   <span data-ttu-id="ac5cc-110">Нвертицес — число вершин.</span><span class="sxs-lookup"><span data-stu-id="ac5cc-110">nVertices - Number of vertices.</span></span>
-   <span data-ttu-id="ac5cc-111">вершины \[ нвертицес \] — массив вершин.</span><span class="sxs-lookup"><span data-stu-id="ac5cc-111">vertices\[nVertices\] - Array of vertices.</span></span> <span data-ttu-id="ac5cc-112">См. раздел [**vector**](vector.md).</span><span class="sxs-lookup"><span data-stu-id="ac5cc-112">See [**Vector**](vector.md).</span></span>
-   <span data-ttu-id="ac5cc-113">Нпатчес — число исправлений.</span><span class="sxs-lookup"><span data-stu-id="ac5cc-113">nPatches - Number of patches.</span></span>
-   <span data-ttu-id="ac5cc-114">исправления \[ нпатчес \] — массив исправлений.</span><span class="sxs-lookup"><span data-stu-id="ac5cc-114">patches\[nPatches\] - Array of patches.</span></span> <span data-ttu-id="ac5cc-115">См. [**исправление**](patch.md).</span><span class="sxs-lookup"><span data-stu-id="ac5cc-115">See [**Patch**](patch.md).</span></span>
-   <span data-ttu-id="ac5cc-116">\[ ... \] -Здесь можно использовать любой шаблон файла. x.</span><span class="sxs-lookup"><span data-stu-id="ac5cc-116">\[ ... \] - Any .x file template can be used here.</span></span> <span data-ttu-id="ac5cc-117">Это делает архитектуру расширяемой.</span><span class="sxs-lookup"><span data-stu-id="ac5cc-117">This makes the architecture extensible.</span></span>

<span data-ttu-id="ac5cc-118">Исправления используют вершины в массиве вершин в качестве контрольных точек для каждого исправления.</span><span class="sxs-lookup"><span data-stu-id="ac5cc-118">The patches use the vertices in the array of vertices as the control points for each patch.</span></span>

## <a name="see-also"></a><span data-ttu-id="ac5cc-119">См. также</span><span class="sxs-lookup"><span data-stu-id="ac5cc-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac5cc-120">Шаблоны</span><span class="sxs-lookup"><span data-stu-id="ac5cc-120">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



