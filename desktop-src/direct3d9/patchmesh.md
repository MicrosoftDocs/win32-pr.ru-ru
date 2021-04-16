---
description: Определяет сетку, определенную с помощью исправлений Безье. Первый массив представляет собой список вершин, а второй массив определяет исправления для сетки путем индексирования в массиве вершин.
ms.assetid: vs|directx_sdk|~\patchmesh.htm
title: патчмеш
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fcdefac9799736c796aef7cbb7222ab1942540d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104536821"
---
# <a name="patchmesh"></a><span data-ttu-id="6ffd5-104">патчмеш</span><span class="sxs-lookup"><span data-stu-id="6ffd5-104">PatchMesh</span></span>

<span data-ttu-id="6ffd5-105">Определяет сетку, определенную с помощью исправлений Безье.</span><span class="sxs-lookup"><span data-stu-id="6ffd5-105">Defines a mesh defined by Bézier patches.</span></span> <span data-ttu-id="6ffd5-106">Первый массив представляет собой список вершин, а второй массив определяет исправления для сетки путем индексирования в массиве вершин.</span><span class="sxs-lookup"><span data-stu-id="6ffd5-106">The first array is a list of vertices, and the second array defines the patches for the mesh by indexing into the vertex array.</span></span>

``` syntax
template PatchMesh
{
    < D02C95CC-EDBA-4305-9B5D-1820D7704BBF >
    DWORD nVertices;
    array Vector vertices[nVertices];
    DWORD nPatches;
    array Patch patches[nPatches];
    [ ... ]
}
```

<span data-ttu-id="6ffd5-107">Где:</span><span class="sxs-lookup"><span data-stu-id="6ffd5-107">Where:</span></span>

-   <span data-ttu-id="6ffd5-108">Нвертицес — число вершин.</span><span class="sxs-lookup"><span data-stu-id="6ffd5-108">nVertices - Number of vertices.</span></span>
-   <span data-ttu-id="6ffd5-109">вершины \[ нвертицес \] — массив вершин.</span><span class="sxs-lookup"><span data-stu-id="6ffd5-109">vertices\[nVertices\] - Array of vertices.</span></span> <span data-ttu-id="6ffd5-110">См. раздел [**vector**](vector.md).</span><span class="sxs-lookup"><span data-stu-id="6ffd5-110">See [**Vector**](vector.md).</span></span>
-   <span data-ttu-id="6ffd5-111">Нпатчес — число исправлений.</span><span class="sxs-lookup"><span data-stu-id="6ffd5-111">nPatches - Number of patches.</span></span>
-   <span data-ttu-id="6ffd5-112">исправления \[ нпатчес \] — массив исправлений.</span><span class="sxs-lookup"><span data-stu-id="6ffd5-112">patches\[nPatches\] - Array of patches.</span></span> <span data-ttu-id="6ffd5-113">См. [**исправление**](patch.md).</span><span class="sxs-lookup"><span data-stu-id="6ffd5-113">See [**Patch**](patch.md).</span></span>
-   <span data-ttu-id="6ffd5-114">\[ ... \] -Здесь можно использовать любой шаблон файла. x.</span><span class="sxs-lookup"><span data-stu-id="6ffd5-114">\[ ... \] - Any .x file template can be used here.</span></span> <span data-ttu-id="6ffd5-115">Это делает архитектуру расширяемой.</span><span class="sxs-lookup"><span data-stu-id="6ffd5-115">This makes the architecture extensible.</span></span>

<span data-ttu-id="6ffd5-116">Исправления используют вершины в массиве вершин в качестве контрольных точек для каждого исправления.</span><span class="sxs-lookup"><span data-stu-id="6ffd5-116">The patches use the vertices in the array of vertices as the control points for each patch.</span></span> <span data-ttu-id="6ffd5-117">Это устаревший шаблон.</span><span class="sxs-lookup"><span data-stu-id="6ffd5-117">This is a legacy template.</span></span> <span data-ttu-id="6ffd5-118">Последний шаблон сетки исправлений — [**PatchMesh9**](patchmesh9.md).</span><span class="sxs-lookup"><span data-stu-id="6ffd5-118">The latest patch mesh template is [**PatchMesh9**](patchmesh9.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="6ffd5-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6ffd5-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ffd5-120">Шаблоны</span><span class="sxs-lookup"><span data-stu-id="6ffd5-120">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



