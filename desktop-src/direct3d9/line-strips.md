---
description: Ломаная — это примитив, состоящий из соединенных отрезков.
ms.assetid: 73905718-a4c6-4f73-beef-4cccac7eea8c
title: Полосы строк
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3dee7eb79b583ad04dc0ed576a7d9426e8dda9fa
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537616"
---
# <a name="line-strips"></a><span data-ttu-id="272a2-103">Полосы строк</span><span class="sxs-lookup"><span data-stu-id="272a2-103">Line Strips</span></span>

<span data-ttu-id="272a2-104">Ломаная — это примитив, состоящий из соединенных отрезков.</span><span class="sxs-lookup"><span data-stu-id="272a2-104">A line strip is a primitive that is composed of connected line segments.</span></span> <span data-ttu-id="272a2-105">Приложение может использовать ломаные линии для создания незамкнутых многоугольников.</span><span class="sxs-lookup"><span data-stu-id="272a2-105">Your application can use line strips for creating polygons that are not closed.</span></span> <span data-ttu-id="272a2-106">Замкнутый многоугольник — это многоугольник, последняя вершина которого соединяется отрезком с его первой вершиной.</span><span class="sxs-lookup"><span data-stu-id="272a2-106">A closed polygon is a polygon whose last vertex is connected to its first vertex by a line segment.</span></span> <span data-ttu-id="272a2-107">Если приложение создает многоугольники на основе ломаных, вершины могут находиться в разных плоскостях.</span><span class="sxs-lookup"><span data-stu-id="272a2-107">If your application makes polygons based on line strips, the vertices are not guaranteed to be coplanar.</span></span>

<span data-ttu-id="272a2-108">На следующем рисунке показана отрисованная ломаная линия.</span><span class="sxs-lookup"><span data-stu-id="272a2-108">The following illustration shows a rendered line strip.</span></span>

![иллюстрация ломаной линии](images/linstrip.gif)

<span data-ttu-id="272a2-110">Следующий код показывает, как создать вершины для такой ломаной линии.</span><span class="sxs-lookup"><span data-stu-id="272a2-110">The following code shows how to create vertices for this line strip.</span></span>


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



<span data-ttu-id="272a2-111">В приведенном ниже примере кода показано, как отобразить полосу строк в Direct3D 9 с помощью [**IDirect3DDevice9::D равпримитиве**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) .</span><span class="sxs-lookup"><span data-stu-id="272a2-111">The code example below shows how to render a line strip in Direct3D 9 using [**IDirect3DDevice9::DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) .</span></span>


```
//
// It is assumed that d3dDevice is a valid
// pointer to a IDirect3DDevice9 interface.
//
d3dDevice->DrawPrimitive( D3DPT_LINESTRIP, 0, 5 );
```



## <a name="related-topics"></a><span data-ttu-id="272a2-112">См. также</span><span class="sxs-lookup"><span data-stu-id="272a2-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="272a2-113">Примитивы</span><span class="sxs-lookup"><span data-stu-id="272a2-113">Primitives</span></span>](primitives.md)
</dt> </dl>

 

 
