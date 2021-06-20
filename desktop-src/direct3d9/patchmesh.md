---
description: Патчмеш определяет сетку, определенную с помощью исправлений Безье, включая список вершин и исправлений для сетки путем индексирования в массив вершин.
ms.assetid: vs|directx_sdk|~\patchmesh.htm
title: патчмеш
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fabb3846246c7fb76a7146baf0b30bd9730fe24b
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404717"
---
# <a name="patchmesh"></a><span data-ttu-id="fa3ea-103">патчмеш</span><span class="sxs-lookup"><span data-stu-id="fa3ea-103">PatchMesh</span></span>

<span data-ttu-id="fa3ea-104">Определяет сетку, определенную с помощью исправлений Безье.</span><span class="sxs-lookup"><span data-stu-id="fa3ea-104">Defines a mesh defined by Bézier patches.</span></span> <span data-ttu-id="fa3ea-105">Первый массив представляет собой список вершин, а второй массив определяет исправления для сетки путем индексирования в массиве вершин.</span><span class="sxs-lookup"><span data-stu-id="fa3ea-105">The first array is a list of vertices, and the second array defines the patches for the mesh by indexing into the vertex array.</span></span>

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

<span data-ttu-id="fa3ea-106">Где:</span><span class="sxs-lookup"><span data-stu-id="fa3ea-106">Where:</span></span>

-   <span data-ttu-id="fa3ea-107">Нвертицес — число вершин.</span><span class="sxs-lookup"><span data-stu-id="fa3ea-107">nVertices - Number of vertices.</span></span>
-   <span data-ttu-id="fa3ea-108">вершины \[ нвертицес \] — массив вершин.</span><span class="sxs-lookup"><span data-stu-id="fa3ea-108">vertices\[nVertices\] - Array of vertices.</span></span> <span data-ttu-id="fa3ea-109">См. раздел [**vector**](vector.md).</span><span class="sxs-lookup"><span data-stu-id="fa3ea-109">See [**Vector**](vector.md).</span></span>
-   <span data-ttu-id="fa3ea-110">Нпатчес — число исправлений.</span><span class="sxs-lookup"><span data-stu-id="fa3ea-110">nPatches - Number of patches.</span></span>
-   <span data-ttu-id="fa3ea-111">исправления \[ нпатчес \] — массив исправлений.</span><span class="sxs-lookup"><span data-stu-id="fa3ea-111">patches\[nPatches\] - Array of patches.</span></span> <span data-ttu-id="fa3ea-112">См. [**исправление**](patch.md).</span><span class="sxs-lookup"><span data-stu-id="fa3ea-112">See [**Patch**](patch.md).</span></span>
-   <span data-ttu-id="fa3ea-113">\[ ... \] -Здесь можно использовать любой шаблон файла. x.</span><span class="sxs-lookup"><span data-stu-id="fa3ea-113">\[ ... \] - Any .x file template can be used here.</span></span> <span data-ttu-id="fa3ea-114">Это делает архитектуру расширяемой.</span><span class="sxs-lookup"><span data-stu-id="fa3ea-114">This makes the architecture extensible.</span></span>

<span data-ttu-id="fa3ea-115">Исправления используют вершины в массиве вершин в качестве контрольных точек для каждого исправления.</span><span class="sxs-lookup"><span data-stu-id="fa3ea-115">The patches use the vertices in the array of vertices as the control points for each patch.</span></span> <span data-ttu-id="fa3ea-116">Это устаревший шаблон.</span><span class="sxs-lookup"><span data-stu-id="fa3ea-116">This is a legacy template.</span></span> <span data-ttu-id="fa3ea-117">Последний шаблон сетки исправлений — [**PatchMesh9**](patchmesh9.md).</span><span class="sxs-lookup"><span data-stu-id="fa3ea-117">The latest patch mesh template is [**PatchMesh9**](patchmesh9.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="fa3ea-118">См. также</span><span class="sxs-lookup"><span data-stu-id="fa3ea-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa3ea-119">Шаблоны</span><span class="sxs-lookup"><span data-stu-id="fa3ea-119">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



