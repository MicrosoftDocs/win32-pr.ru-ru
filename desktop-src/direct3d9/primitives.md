---
description: Трехмерный примитив — это коллекция вершин, которые формируют одну трехмерную фигуру. Простейший примитив — это коллекция точек в трехмерной системе координат, которая называется списком точек.
ms.assetid: vs|directx_sdk|~\primitives.htm
title: Примитивы (графика Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38916e85add69574a2437b0e48c209b14a341e44
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104139274"
---
# <a name="primitives-direct3d-9-graphics"></a><span data-ttu-id="c92fd-104">Примитивы (графика Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="c92fd-104">Primitives (Direct3D 9 Graphics)</span></span>

<span data-ttu-id="c92fd-105">Трехмерный примитив — это коллекция вершин, которые формируют одну трехмерную фигуру.</span><span class="sxs-lookup"><span data-stu-id="c92fd-105">A 3D primitive is a collection of vertices that form a single 3D entity.</span></span> <span data-ttu-id="c92fd-106">Простейший примитив — это коллекция точек в трехмерной системе координат, которая называется списком точек.</span><span class="sxs-lookup"><span data-stu-id="c92fd-106">The simplest primitive is a collection of points in a 3D coordinate system, which is called a point list.</span></span>

<span data-ttu-id="c92fd-107">Часто трехмерные примитивы являются многоугольниками.</span><span class="sxs-lookup"><span data-stu-id="c92fd-107">Often, 3D primitives are polygons.</span></span> <span data-ttu-id="c92fd-108">Многоугольник — это замкнутая 3D-фигура, обозначенная как минимум тремя вершинами.</span><span class="sxs-lookup"><span data-stu-id="c92fd-108">A polygon is a closed 3D figure delineated by at least three vertices.</span></span> <span data-ttu-id="c92fd-109">Самый простой многоугольник — это треугольник.</span><span class="sxs-lookup"><span data-stu-id="c92fd-109">The simplest polygon is a triangle.</span></span> <span data-ttu-id="c92fd-110">В Microsoft Direct3D треугольники используются для составления большинства многоугольников, потому что все три вершины в треугольнике гарантированно копланарны.</span><span class="sxs-lookup"><span data-stu-id="c92fd-110">Microsoft Direct3D uses triangles to compose most of its polygons because all three vertices in a triangle are guaranteed to be coplanar.</span></span> <span data-ttu-id="c92fd-111">Отрисовка непланарных вершин неэффективна.</span><span class="sxs-lookup"><span data-stu-id="c92fd-111">Rendering nonplanar vertices is inefficient.</span></span> <span data-ttu-id="c92fd-112">Вы можете объединять треугольники для получения больших, сложных многоугольников и сеток.</span><span class="sxs-lookup"><span data-stu-id="c92fd-112">You can combine triangles to form large, complex polygons and meshes.</span></span>

<span data-ttu-id="c92fd-113">На следующем рисунке показан куб.</span><span class="sxs-lookup"><span data-stu-id="c92fd-113">The following illustration shows a cube.</span></span> <span data-ttu-id="c92fd-114">Каждая грань куба образована двумя треугольниками.</span><span class="sxs-lookup"><span data-stu-id="c92fd-114">Two triangles form each face of the cube.</span></span> <span data-ttu-id="c92fd-115">Весь набор треугольников образует один кубический примитив.</span><span class="sxs-lookup"><span data-stu-id="c92fd-115">The entire set of triangles forms one cubic primitive.</span></span> <span data-ttu-id="c92fd-116">Можно применить текстуры и материалы к поверхности примитивов, чтобы они отображались в виде одной сплошной формы.</span><span class="sxs-lookup"><span data-stu-id="c92fd-116">You can apply textures and materials to the surfaces of primitives to make them appear to be a single solid form.</span></span> <span data-ttu-id="c92fd-117">Дополнительные сведения см. в разделе [материалы (Direct3D 9)](materials.md) и [Direct3D текстуры (Direct3D 9)](direct3d-textures.md).</span><span class="sxs-lookup"><span data-stu-id="c92fd-117">For details, see [Materials (Direct3D 9)](materials.md) and [Direct3D Textures (Direct3D 9)](direct3d-textures.md).</span></span>

![иллюстрация куба с двумя треугольниками на каждой грани](images/cube3d.png)

<span data-ttu-id="c92fd-119">Можно также использовать треугольники для создания примитивов, поверхности которых кажутся плавными кривыми.</span><span class="sxs-lookup"><span data-stu-id="c92fd-119">You can also use triangles to create primitives whose surfaces appear to be smooth curves.</span></span> <span data-ttu-id="c92fd-120">На следующем рисунке показано, как с помощью треугольников можно смоделировать сферу.</span><span class="sxs-lookup"><span data-stu-id="c92fd-120">The following illustration shows how a sphere can be simulated with triangles.</span></span> <span data-ttu-id="c92fd-121">После применения материала сфера будет изогнута при подготовке к просмотру.</span><span class="sxs-lookup"><span data-stu-id="c92fd-121">After a material is applied, the sphere looks curved when it is rendered.</span></span> <span data-ttu-id="c92fd-122">Это особенно верно, если используется заливка по методу Гуро.</span><span class="sxs-lookup"><span data-stu-id="c92fd-122">This is especially true if you use Gouraud shading.</span></span> <span data-ttu-id="c92fd-123">Дополнительные сведения см. в разделе [Заливка](shading-modes.md)по методу Гуро.</span><span class="sxs-lookup"><span data-stu-id="c92fd-123">For details, see [Gouraud Shading](shading-modes.md).</span></span>

![иллюстрация сферы, смоделированной с использованием треугольников](images/sphere3d.png)

<span data-ttu-id="c92fd-125">Устройства Direct3D могут создавать примитивы следующих типов и управлять ими.</span><span class="sxs-lookup"><span data-stu-id="c92fd-125">Direct3D devices can create and manipulate the following types of primitives.</span></span>

-   [<span data-ttu-id="c92fd-126">Списки точек</span><span class="sxs-lookup"><span data-stu-id="c92fd-126">Point Lists</span></span>](point-lists.md)
-   [<span data-ttu-id="c92fd-127">Списки строк</span><span class="sxs-lookup"><span data-stu-id="c92fd-127">Line Lists</span></span>](line-lists.md)
-   [<span data-ttu-id="c92fd-128">Полосы строк</span><span class="sxs-lookup"><span data-stu-id="c92fd-128">Line Strips</span></span>](line-strips.md)
-   [<span data-ttu-id="c92fd-129">Списки треугольников</span><span class="sxs-lookup"><span data-stu-id="c92fd-129">Triangle Lists</span></span>](triangle-lists.md)
-   [<span data-ttu-id="c92fd-130">Ленты треугольников</span><span class="sxs-lookup"><span data-stu-id="c92fd-130">Triangle Strips</span></span>](triangle-strips.md)
-   [<span data-ttu-id="c92fd-131">Треугольные вентиляторы (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="c92fd-131">Triangle Fans (Direct3D 9)</span></span>](triangle-fans.md)

<span data-ttu-id="c92fd-132">Типы-примитивы можно визуализировать из приложения C++ с помощью любого из методов подготовки к просмотру интерфейса [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) .</span><span class="sxs-lookup"><span data-stu-id="c92fd-132">You can render primitive types from a C++ application with any of the rendering methods of the [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c92fd-133">См. также</span><span class="sxs-lookup"><span data-stu-id="c92fd-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c92fd-134">Устройства Direct3D</span><span class="sxs-lookup"><span data-stu-id="c92fd-134">Direct3D Devices</span></span>](direct3d-devices.md)
</dt> </dl>

 

 
