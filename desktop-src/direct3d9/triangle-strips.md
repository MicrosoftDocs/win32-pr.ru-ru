---
description: Полоса треугольников — это ряд соединенных треугольников.
ms.assetid: 3923c570-47a4-4b53-a097-731981380ae0
title: Ленты треугольников
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2766529a37b994e5fe30815ca6300476f06c7d4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104558818"
---
# <a name="triangle-strips"></a><span data-ttu-id="7a01a-103">Ленты треугольников</span><span class="sxs-lookup"><span data-stu-id="7a01a-103">Triangle Strips</span></span>

<span data-ttu-id="7a01a-104">Полоса треугольников — это ряд соединенных треугольников.</span><span class="sxs-lookup"><span data-stu-id="7a01a-104">A triangle strip is a series of connected triangles.</span></span> <span data-ttu-id="7a01a-105">Поскольку треугольники соединены, приложению не нужно постоянно указывать все три вершины для каждого треугольника.</span><span class="sxs-lookup"><span data-stu-id="7a01a-105">Because the triangles are connected, the application does not need to repeatedly specify all three vertices for each triangle.</span></span> <span data-ttu-id="7a01a-106">Например, для определения следующей полосы треугольников достаточно семи вершин.</span><span class="sxs-lookup"><span data-stu-id="7a01a-106">For example, you need only seven vertices to define the following triangle strip.</span></span>

![иллюстрация полосы треугольников с семью вершинами](images/tristrip.png)

<span data-ttu-id="7a01a-108">Система использует вершины v1, v2 и v3 для рисования первого треугольника; v2, v4 и v3 для рисования второго треугольника; v3, v4 и v5 для рисования третьего треугольника; v4, v6 и v5 для рисования четвертого треугольника и т. д.</span><span class="sxs-lookup"><span data-stu-id="7a01a-108">The system uses vertices v1, v2, and v3 to draw the first triangle; v2, v4, and v3 to draw the second triangle; v3, v4, and v5 to draw the third; v4, v6, and v5 to draw the fourth; and so on.</span></span> <span data-ttu-id="7a01a-109">Обратите внимание, что вершины второго и четвертого треугольников идут не по порядку; это необходимо для того, чтобы все треугольники рисовались в направлении по часовой стрелке.</span><span class="sxs-lookup"><span data-stu-id="7a01a-109">Notice that the vertices of the second and fourth triangles are out of order; this is required to make sure that all the triangles are drawn in a clockwise orientation.</span></span>

<span data-ttu-id="7a01a-110">Большинство объектов в 3D-сценах состоят из полос треугольников.</span><span class="sxs-lookup"><span data-stu-id="7a01a-110">Most objects in 3D scenes are composed of triangle strips.</span></span> <span data-ttu-id="7a01a-111">Это связано с тем, что полосы треугольников можно использовать для задания сложных объектов так, чтобы память и процессорное время использовались эффективно.</span><span class="sxs-lookup"><span data-stu-id="7a01a-111">This is because triangle strips can be used to specify complex objects in a way that makes efficient use of memory and processing time.</span></span>

<span data-ttu-id="7a01a-112">На следующем рисунке показана отрисованная полоса треугольников.</span><span class="sxs-lookup"><span data-stu-id="7a01a-112">The following illustration depicts a rendered triangle strip.</span></span>

![иллюстрация отрисованной полосы треугольников](images/tstrip2.png)

<span data-ttu-id="7a01a-114">В следующем коде показано, как создать вершины для такой полосы треугольников.</span><span class="sxs-lookup"><span data-stu-id="7a01a-114">The following code shows how to create vertices for this triangle strip.</span></span>


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



<span data-ttu-id="7a01a-115">В приведенном ниже примере кода показано, как визуализировать эту полосу треугольника в Direct3D 9 с помощью [**IDirect3DDevice9::D равпримитиве**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive).</span><span class="sxs-lookup"><span data-stu-id="7a01a-115">The code example below shows how to render this triangle strip in Direct3D 9 using [**IDirect3DDevice9::DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive).</span></span>


```
//
// It is assumed that d3dDevice is a valid
// pointer to a IDirect3DDevice9 interface.
//
d3dDevice->DrawPrimitive( D3DPT_TRIANGLESTRIP, 0, 4);
```



<span data-ttu-id="7a01a-116">Используйте полосу треугольника для отрисовки треугольников, которые не соединены друг с другом.</span><span class="sxs-lookup"><span data-stu-id="7a01a-116">Use a triangle strip to render triangles that are not connected to one another.</span></span> <span data-ttu-id="7a01a-117">Для этого укажите вырожденный треугольник (то есть треугольник, область которого равна нулю) в списке треугольников.</span><span class="sxs-lookup"><span data-stu-id="7a01a-117">To do this, specify a degenerate triangle (that is, a triangle whose area is zero) in the triangle list.</span></span> <span data-ttu-id="7a01a-118">При этом создается линия между двумя треугольниками, которые не будут отображены.</span><span class="sxs-lookup"><span data-stu-id="7a01a-118">This creates a line between the two triangles which will not render.</span></span> <span data-ttu-id="7a01a-119">Чтобы отобразить только первый и последний треугольники из предыдущего примера, измените буфер вершин, как показано ниже:</span><span class="sxs-lookup"><span data-stu-id="7a01a-119">To render only the first and last triangles from the previous example, modify the vertex buffer as shown here:</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="7a01a-120">См. также</span><span class="sxs-lookup"><span data-stu-id="7a01a-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7a01a-121">Примитивы</span><span class="sxs-lookup"><span data-stu-id="7a01a-121">Primitives</span></span>](primitives.md)
</dt> </dl>

 

 
