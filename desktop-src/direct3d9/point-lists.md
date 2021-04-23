---
description: Список точек — это коллекция вершин, которые отображаются в виде изолированных точек. Приложение может использовать их в трехмерных сценах для полей звезд или пунктирных линий на поверхности многоугольника.
ms.assetid: 82866b07-5043-433f-974a-0a301d4b5491
title: Списки точек
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57086a445209d9e60173910e07166a6149e0b8d2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103806233"
---
# <a name="point-lists"></a><span data-ttu-id="bad63-104">Списки точек</span><span class="sxs-lookup"><span data-stu-id="bad63-104">Point Lists</span></span>

<span data-ttu-id="bad63-105">Список точек — это коллекция вершин, которые отображаются в виде изолированных точек.</span><span class="sxs-lookup"><span data-stu-id="bad63-105">A point list is a collection of vertices that are rendered as isolated points.</span></span> <span data-ttu-id="bad63-106">Приложение может использовать их в трехмерных сценах для полей звезд или пунктирных линий на поверхности многоугольника.</span><span class="sxs-lookup"><span data-stu-id="bad63-106">Your application can use them in 3D scenes for star fields, or dotted lines on the surface of a polygon.</span></span>

<span data-ttu-id="bad63-107">На следующем рисунке показан отрисованный список точек.</span><span class="sxs-lookup"><span data-stu-id="bad63-107">The following illustration depicts a rendered point list.</span></span>

![иллюстрация списка точек](images/pointlst.png)

<span data-ttu-id="bad63-109">Приложение может применять к списку точек материалы и текстуры.</span><span class="sxs-lookup"><span data-stu-id="bad63-109">Your application can apply materials and textures to a point list.</span></span> <span data-ttu-id="bad63-110">Цвета материала или текстуры отображаются только в нарисованных точках, но не между ними.</span><span class="sxs-lookup"><span data-stu-id="bad63-110">The colors in the material or texture appear only at the points drawn, and not anywhere between the points.</span></span>

<span data-ttu-id="bad63-111">Следующий код показывает, как создать вершины для такого списка точек.</span><span class="sxs-lookup"><span data-stu-id="bad63-111">The following code shows how to create vertices for this point list.</span></span>


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



<span data-ttu-id="bad63-112">В приведенном ниже примере кода показано, как визуализировать этот список точек в Direct3D 9 с помощью [**IDirect3DDevice9::D равпримитиве**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive).</span><span class="sxs-lookup"><span data-stu-id="bad63-112">The code example below shows how to render this point list in Direct3D 9 using [**IDirect3DDevice9::DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive).</span></span>


```
//
// It is assumed that d3dDevice is a valid
// pointer to a IDirect3DDevice9 interface.
//
d3dDevice->DrawPrimitive( D3DPT_POINTLIST, 0, 6 );
```



## <a name="related-topics"></a><span data-ttu-id="bad63-113">См. также</span><span class="sxs-lookup"><span data-stu-id="bad63-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bad63-114">Примитивы</span><span class="sxs-lookup"><span data-stu-id="bad63-114">Primitives</span></span>](primitives.md)
</dt> </dl>

 

 
