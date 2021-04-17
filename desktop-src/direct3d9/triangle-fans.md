---
description: Треугольный вентилятор подобен полосе треугольника, за исключением того, что все треугольники имеют одну вершину, как показано на следующем рисунке.
ms.assetid: a1fbfd78-121f-4f79-9ba8-44f23356a432
title: Треугольные вентиляторы (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2357af0d999cc759453e34cd278f61064a637cfd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104553828"
---
# <a name="triangle-fans-direct3d-9"></a><span data-ttu-id="82dda-103">Треугольные вентиляторы (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="82dda-103">Triangle Fans (Direct3D 9)</span></span>

<span data-ttu-id="82dda-104">Треугольный вентилятор подобен полосе треугольника, за исключением того, что все треугольники имеют одну вершину, как показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="82dda-104">A triangle fan is similar to a triangle strip, except that all the triangles share one vertex, as shown in the following illustration.</span></span>

![Иллюстрация вентилятора треугольника](images/trifan.gif)

<span data-ttu-id="82dda-106">Для рисования первого треугольника система использует вершины v2, v3 и v1. v3, v4 и v1 для рисования второго треугольника; V4, V5 и v1 для рисования третьего треугольника; и т. д.</span><span class="sxs-lookup"><span data-stu-id="82dda-106">The system uses vertices v2, v3, and v1 to draw the first triangle; v3, v4, and v1 to draw the second triangle; v4, v5, and v1 to draw the third triangle; and so on.</span></span> <span data-ttu-id="82dda-107">Если включено плоское затенение, система перемещает треугольник цветом из первой вершины.</span><span class="sxs-lookup"><span data-stu-id="82dda-107">When flat shading is enabled, the system shades the triangle with the color from its first vertex.</span></span>

<span data-ttu-id="82dda-108">На следующем рисунке показан отрисованный вентилятор треугольника.</span><span class="sxs-lookup"><span data-stu-id="82dda-108">The following illustration depicts a rendered triangle fan.</span></span>

![Иллюстрация отрисованного вентилятора треугольника](images/tfan2.gif)

<span data-ttu-id="82dda-110">В следующем коде показано, как создать вершины для этого вентилятора треугольника.</span><span class="sxs-lookup"><span data-stu-id="82dda-110">The following code shows how to create vertices for this triangle fan.</span></span>


```
struct CUSTOMVERTEX
{
    float x,y,z;
};

CUSTOMVERTEX Vertices[] = 
{
    { 0.0, 0.0, 0.0},
    {-5.0, 5.0, 0.0},
    {-3.0,  7.0, 0.0},
    { 0.0, 10.0, 0.0},
    { 3.0,  7.0, 0.0},
    { 5.0,  5.0, 0.0},
};
```



<span data-ttu-id="82dda-111">В приведенном ниже примере кода показано, как визуализировать этот вентилятор треугольника в Direct3D 9 с помощью [**IDirect3DDevice9::D равпримитиве**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive).</span><span class="sxs-lookup"><span data-stu-id="82dda-111">The code example below shows how to render this triangle fan in Direct3D 9 using [**IDirect3DDevice9::DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive).</span></span>


```
//
// It is assumed that d3dDevice is a valid
// pointer to a IDirect3DDevice9 interface.
//
d3dDevice->DrawPrimitive( D3DPT_TRIANGLEFAN, 0, 4 );
```



<span data-ttu-id="82dda-112">Вентиляторы с треугольниками не поддерживаются в Direct3D 10 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="82dda-112">Triangle fans are not supported in Direct3D 10 or later.</span></span>

## <a name="related-topics"></a><span data-ttu-id="82dda-113">См. также</span><span class="sxs-lookup"><span data-stu-id="82dda-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="82dda-114">Примитивы</span><span class="sxs-lookup"><span data-stu-id="82dda-114">Primitives</span></span>](primitives.md)
</dt> </dl>

 

 
