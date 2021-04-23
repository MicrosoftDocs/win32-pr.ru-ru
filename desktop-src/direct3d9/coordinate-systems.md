---
description: 'Обычно приложения трехмерной графики используют два типа декартовой системы координат: левый и правый.'
ms.assetid: 268c3024-85a5-4fd5-b575-e126dd4be97c
title: Системы координат (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcb9fa389b2bf11bec9ee4f8053bbeb4c822f422
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692004"
---
# <a name="coordinate-systems-direct3d-9"></a><span data-ttu-id="ade70-103">Системы координат (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="ade70-103">Coordinate Systems (Direct3D 9)</span></span>

<span data-ttu-id="ade70-104">Обычно приложения трехмерной графики используют два типа декартовой системы координат: левый и правый.</span><span class="sxs-lookup"><span data-stu-id="ade70-104">Typically 3D graphics applications use two types of Cartesian coordinate systems: left-handed and right-handed.</span></span> <span data-ttu-id="ade70-105">В обеих системах координат положительная ось x указывает вправо, а положительная ось y — вверх.</span><span class="sxs-lookup"><span data-stu-id="ade70-105">In both coordinate systems, the positive x-axis points to the right, and the positive y-axis points up.</span></span> <span data-ttu-id="ade70-106">Можно запомнить, в каком направлении указывает положительная ось z, указав пальцами левой или правой руки в направлении положительной оси x и скруглив их в направлении положительной оси y.</span><span class="sxs-lookup"><span data-stu-id="ade70-106">You can remember which direction the positive z-axis points by pointing the fingers of either your left or right hand in the positive x-direction and curling them into the positive y-direction.</span></span> <span data-ttu-id="ade70-107">Направление, в котором указывают ваши пальцы (к вам или от вас), — это направление, в котором указывает положительная ось z в этой системе координат.</span><span class="sxs-lookup"><span data-stu-id="ade70-107">The direction your thumb points, either toward or away from you, is the direction that the positive z-axis points for that coordinate system.</span></span> <span data-ttu-id="ade70-108">На следующем рисунке показаны эти две системы координат.</span><span class="sxs-lookup"><span data-stu-id="ade70-108">The following illustration shows these two coordinate systems.</span></span>

![изображение левосторонней и правосторонней Декартовых систем координат](images/leftrght.png)

<span data-ttu-id="ade70-110">В Direct3D используется левосторонняя система координат.</span><span class="sxs-lookup"><span data-stu-id="ade70-110">Direct3D uses a left-handed coordinate system.</span></span> <span data-ttu-id="ade70-111">При переносе приложения, основанного на правой системе координат, необходимо внести два изменения в данные, передаваемые в Direct3D.</span><span class="sxs-lookup"><span data-stu-id="ade70-111">If you are porting an application that is based on a right-handed coordinate system, you must make two changes to the data passed to Direct3D.</span></span>

-   <span data-ttu-id="ade70-112">Измените порядок вершин треугольников так, чтобы система обходила их по часовой стрелке от передней.</span><span class="sxs-lookup"><span data-stu-id="ade70-112">Flip the order of triangle vertices so that the system traverses them clockwise from the front.</span></span> <span data-ttu-id="ade70-113">Другими словами, если имеются вершины v0, v1, v2, передайте их в Direct3D как v0, v2, v1.</span><span class="sxs-lookup"><span data-stu-id="ade70-113">In other words, if the vertices are v0, v1, v2, pass them to Direct3D as v0, v2, v1.</span></span>
-   <span data-ttu-id="ade70-114">Используйте матрицу представления для масштабирования пространства на -1 по оси z.</span><span class="sxs-lookup"><span data-stu-id="ade70-114">Use the view matrix to scale world space by -1 in the z-direction.</span></span> <span data-ttu-id="ade70-115">Для этого следует отразить знак \_ 31, \_ 32, \_ 33 и \_ 34 в структуре [**D3DMATRIX**](d3dmatrix.md) , используемой для матрицы представления.</span><span class="sxs-lookup"><span data-stu-id="ade70-115">To do this, flip the sign of the \_31, \_32, \_33, and \_34 member of the [**D3DMATRIX**](d3dmatrix.md) structure that you use for your view matrix.</span></span>

<span data-ttu-id="ade70-116">Чтобы получить объемы в правой части мира, используйте функции [**D3DXMatrixPerspectiveRH**](d3dxmatrixperspectiverh.md) и [**D3DXMatrixOrthoRH**](d3dxmatrixorthorh.md) , чтобы определить преобразование проекции.</span><span class="sxs-lookup"><span data-stu-id="ade70-116">To obtain what amounts to a right-handed world, use the [**D3DXMatrixPerspectiveRH**](d3dxmatrixperspectiverh.md) and [**D3DXMatrixOrthoRH**](d3dxmatrixorthorh.md) functions to define the projection transform.</span></span> <span data-ttu-id="ade70-117">Однако будьте внимательны при использовании соответствующей функции [**D3DXMatrixLookAtRH**](d3dxmatrixlookatrh.md) , отмените порядок отбора обратных сторон и разметьте соответствующие карты Куба.</span><span class="sxs-lookup"><span data-stu-id="ade70-117">However, be careful to use the corresponding [**D3DXMatrixLookAtRH**](d3dxmatrixlookatrh.md) function, reverse the backface-culling order, and lay out the cube maps accordingly.</span></span>

<span data-ttu-id="ade70-118">Несмотря на то что левосторонние и правосторонние системы координат относятся к наиболее распространенным, в программном обеспечении для работы с трехмерными объектами существует множество других систем координат.</span><span class="sxs-lookup"><span data-stu-id="ade70-118">Although left-handed and right-handed coordinates are the most common systems, there is a variety of other coordinate systems used in 3D software.</span></span> <span data-ttu-id="ade70-119">Например, приложения для трехмерного моделирования часто используют систему координат, в которой ось y указывает в направлении смотрящего или от него, а ось z — вверх.</span><span class="sxs-lookup"><span data-stu-id="ade70-119">For example, it is not unusual for 3D modeling applications to use a coordinate system in which the y-axis points toward or away from the viewer, and the z-axis points up.</span></span>

<span data-ttu-id="ade70-120">Формально, ориентация набора базисных векторов (т. е. системы координат) может быть найдена путем вычисления определителя матрицы, определенной определенным набором базисных векторов.</span><span class="sxs-lookup"><span data-stu-id="ade70-120">Formally, the orientation of a set of basis vectors (i.e. a coordinate system) can be found by the computing the determinant of the matrix defined by the particular set of basis vectors.</span></span> <span data-ttu-id="ade70-121">Если определитель положительный, то говорят, что он является «положительным» ориентированным (или правым).</span><span class="sxs-lookup"><span data-stu-id="ade70-121">If the determinant is positive, the basis is said to be "positively" oriented (or right-handed).</span></span> <span data-ttu-id="ade70-122">Если определитель отрицательный, то говорят, что это "отрицательно" ориентированный (или левый).</span><span class="sxs-lookup"><span data-stu-id="ade70-122">If the determinant is negative, the basis is said to be "negatively" oriented (or left-handed).</span></span> <span data-ttu-id="ade70-123">Описание того, что такое определитель, см. в статье ресурс линейной перезаписи.</span><span class="sxs-lookup"><span data-stu-id="ade70-123">For an explanation of what a determinant is, see any linear algebra resource.</span></span>

<span data-ttu-id="ade70-124">Неформально можно использовать "правое или левое правило", чтобы определить, является ли заданный набор базисных векторов формой правой или левой точки координат.</span><span class="sxs-lookup"><span data-stu-id="ade70-124">Informally, you can use the "right/left hand rule" to determine if a given set of basis vectors form either a right or left handed coordinate system.</span></span>

<span data-ttu-id="ade70-125">Основными операциями, выполняемыми над объектами, определенными в трехмерной системе координат, являются преобразование, вращение и масштабирование.</span><span class="sxs-lookup"><span data-stu-id="ade70-125">The essential operations performed on objects defined in a 3D coordinate system are translation, rotation, and scaling.</span></span> <span data-ttu-id="ade70-126">Можно комбинировать эти базовые трансформации и создавать матрицу трансформаций.</span><span class="sxs-lookup"><span data-stu-id="ade70-126">You can combine these basic transformations to create a transform matrix.</span></span> <span data-ttu-id="ade70-127">Дополнительные сведения см. в разделе [преобразования (Direct3D 9)](transforms.md).</span><span class="sxs-lookup"><span data-stu-id="ade70-127">For details, see [Transforms (Direct3D 9)](transforms.md).</span></span>

<span data-ttu-id="ade70-128">При объединении этих операций результаты не будут коммутативными; важен порядок умножения матриц.</span><span class="sxs-lookup"><span data-stu-id="ade70-128">When you combine these operations, the results are not commutative; the order in which you multiply matrices is important.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ade70-129">См. также</span><span class="sxs-lookup"><span data-stu-id="ade70-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ade70-130">Системы координат и геометрия</span><span class="sxs-lookup"><span data-stu-id="ade70-130">Coordinate Systems and Geometry</span></span>](coordinate-systems-and-geometry.md)
</dt> </dl>

 

 



