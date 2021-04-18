---
description: Список треугольников — это список изолированных треугольников. Они могут находиться рядом друг с другом. Список треугольников должен быт иметь как минимум три вершины, а общее количество вершин должно делиться на три.
ms.assetid: e5c3470f-361c-458a-a42a-3549c51d8794
title: Списки треугольников
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 230cac9b4120d31821d70db022ab50d311d7b73e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105701158"
---
# <a name="triangle-lists"></a><span data-ttu-id="cfaf9-105">Списки треугольников</span><span class="sxs-lookup"><span data-stu-id="cfaf9-105">Triangle Lists</span></span>

<span data-ttu-id="cfaf9-106">Список треугольников — это список изолированных треугольников.</span><span class="sxs-lookup"><span data-stu-id="cfaf9-106">A triangle list is a list of isolated triangles.</span></span> <span data-ttu-id="cfaf9-107">Они могут находиться рядом друг с другом.</span><span class="sxs-lookup"><span data-stu-id="cfaf9-107">They might or might not be near each other.</span></span> <span data-ttu-id="cfaf9-108">Список треугольников должен быт иметь как минимум три вершины, а общее количество вершин должно делиться на три.</span><span class="sxs-lookup"><span data-stu-id="cfaf9-108">A triangle list must have at least three vertices and the total number of vertices must be divisible by three.</span></span>

<span data-ttu-id="cfaf9-109">Используем списки треугольников для создания объекта, состоящего из несмежных элементов.</span><span class="sxs-lookup"><span data-stu-id="cfaf9-109">Use triangle lists to create an object that is composed of disjoint pieces.</span></span> <span data-ttu-id="cfaf9-110">Например, один из способов создать силовую стену в 3D-игре — это задать большой список маленьких, несвязных треугольников.</span><span class="sxs-lookup"><span data-stu-id="cfaf9-110">For instance, one way to create a force-field wall in a 3D game is to specify a large list of small, unconnected triangles.</span></span> <span data-ttu-id="cfaf9-111">Затем необходимо применить к списку треугольников материал и текстуру, которые создают впечатление излучаемого света.</span><span class="sxs-lookup"><span data-stu-id="cfaf9-111">Then apply a material and texture that appears to emit light to the triangle list.</span></span> <span data-ttu-id="cfaf9-112">Кажется, что каждый треугольник в стене светится.</span><span class="sxs-lookup"><span data-stu-id="cfaf9-112">Each triangle in the wall appears to glow.</span></span> <span data-ttu-id="cfaf9-113">Сцена за стеной становится частично видимой через пробелы в треугольниках; именно таким образом игроки привыкли видеть силовое поле.</span><span class="sxs-lookup"><span data-stu-id="cfaf9-113">The scene behind the wall becomes partially visible through the gaps between the triangles, as a player might expect when looking at a force field.</span></span>

<span data-ttu-id="cfaf9-114">Списками треугольников также удобно пользоваться для создания примитивов, имеющих острые ребра и затененных по методу Гуро.</span><span class="sxs-lookup"><span data-stu-id="cfaf9-114">Triangle lists are also useful for creating primitives that have sharp edges and are shaded with Gouraud shading.</span></span> <span data-ttu-id="cfaf9-115">См. Дополнительные [векторы граней и вершин (Direct3D 9)](face-and-vertex-normal-vectors.md).</span><span class="sxs-lookup"><span data-stu-id="cfaf9-115">See [Face and Vertex Normal Vectors (Direct3D 9)](face-and-vertex-normal-vectors.md).</span></span>

<span data-ttu-id="cfaf9-116">На следующем рисунке показан отрисованный список треугольников.</span><span class="sxs-lookup"><span data-stu-id="cfaf9-116">The following illustration depicts a rendered triangle list.</span></span>

![иллюстрация отрисованного списка треугольников](images/trilist.png)

<span data-ttu-id="cfaf9-118">В следующем коде показано, как создать вершины для такого списка треугольников.</span><span class="sxs-lookup"><span data-stu-id="cfaf9-118">The following code shows how to create vertices for this triangle list.</span></span>


```
struct CUSTOMVERTEX
{
    float x,y,z;
};

CUSTOMVERTEX Vertices[] = 
{
    {-5.0, -5.0, 0.0},
    { 0.0,  5.0, 0.0},
    { 5.0, -5.0, 0.0},
    {10.0,  5.0, 0.0},
    {15.0, -5.0, 0.0},
    {20.0,  5.0, 0.0}

};
```



<span data-ttu-id="cfaf9-119">В приведенном ниже примере кода показано, как визуализировать этот список треугольников в Direct3D 9 с помощью [**IDirect3DDevice9::D равпримитиве**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive).</span><span class="sxs-lookup"><span data-stu-id="cfaf9-119">The code example below shows how to render this triangle list in Direct3D 9 using [**IDirect3DDevice9::DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive).</span></span>


```
//
// It is assumed that d3dDevice is a valid
// pointer to a IDirect3DDevice9 interface.
//
d3dDevice->DrawPrimitive( D3DPT_TRIANGLELIST, 0, 2 );
```



<span data-ttu-id="cfaf9-120">Можно также использовать ленты треугольников для отрисовки треугольников, которые не соединены друг с другом.</span><span class="sxs-lookup"><span data-stu-id="cfaf9-120">You can also use triangle strips to render triangles that are not connected to one another.</span></span> <span data-ttu-id="cfaf9-121">Для этого укажите вырожденный треугольник (то есть треугольник с нулевым размером) в списке; в результате будет создана линия между двумя треугольниками, которые не будут отображаться при отрисовке.</span><span class="sxs-lookup"><span data-stu-id="cfaf9-121">To do this, specify a degenerate triangle (that is, a triangle with zero size) in the list; this will create a line between the two triangles which will not appear during rendering.</span></span> <span data-ttu-id="cfaf9-122">Например, чтобы отобразить только первый и последний треугольник из предыдущего примера, инициализируйте буфер вершин со следующими вершинами:</span><span class="sxs-lookup"><span data-stu-id="cfaf9-122">For example, to render only the first and last triangle from the previous example, initialize the vertex buffer with the following vertices:</span></span>


```
CUSTOMVERTEX Vertices[] =
{
    {-5.0, -5.0, 0.0},
    { 0.0,  5.0, 0.0},
    { 5.0, -5.0, 0.0},
    { 5.0, -5.0, 0.0}, // degenerate triangle
    {10.0,  5.0, 0.0}, // degenerate triangle
    {10.0,  5.0, 0.0},
    {15.0, -5.0, 0.0},
    {20.0,  5.0, 0.0}
};
```



## <a name="related-topics"></a><span data-ttu-id="cfaf9-123">См. также</span><span class="sxs-lookup"><span data-stu-id="cfaf9-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cfaf9-124">Примитивы</span><span class="sxs-lookup"><span data-stu-id="cfaf9-124">Primitives</span></span>](primitives.md)
</dt> </dl>

 

 
