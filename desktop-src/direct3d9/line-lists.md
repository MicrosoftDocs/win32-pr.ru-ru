---
description: Список линий — это список изолированных прямых отрезков.
ms.assetid: bb02b3d6-f30f-4f2b-8b40-a7e37faf524a
title: Списки строк
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b27bd58ea2de6b5944b8511e99154c50f671439
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105710631"
---
# <a name="line-lists"></a><span data-ttu-id="0adc2-103">Списки строк</span><span class="sxs-lookup"><span data-stu-id="0adc2-103">Line Lists</span></span>

<span data-ttu-id="0adc2-104">Список линий — это список изолированных прямых отрезков.</span><span class="sxs-lookup"><span data-stu-id="0adc2-104">A line list is a list of isolated, straight line segments.</span></span> <span data-ttu-id="0adc2-105">Списки линий полезны для таких задач, как добавление дождя или ливня в трехмерную сцену.</span><span class="sxs-lookup"><span data-stu-id="0adc2-105">Line lists are useful for such tasks as adding sleet or heavy rain to a 3D scene.</span></span> <span data-ttu-id="0adc2-106">Приложения создают списки линий, заполняя массив вершин.</span><span class="sxs-lookup"><span data-stu-id="0adc2-106">Applications create a line list by filling an array of vertices.</span></span> <span data-ttu-id="0adc2-107">Обратите внимание, что число вершин в списке линий должно быть четным числом больше двух или равным двум.</span><span class="sxs-lookup"><span data-stu-id="0adc2-107">Note that the number of vertices in a line list must be an even number greater than or equal to two.</span></span>

<span data-ttu-id="0adc2-108">На следующем рисунке показан список отображаемых линий.</span><span class="sxs-lookup"><span data-stu-id="0adc2-108">The following illustration shows a rendered line list.</span></span>

![иллюстрация списка линий](images/linelst.png)

<span data-ttu-id="0adc2-110">К списку линий можно применять материалы и текстуры.</span><span class="sxs-lookup"><span data-stu-id="0adc2-110">You can apply materials and textures to a line list.</span></span> <span data-ttu-id="0adc2-111">Цвета в материале или текстуре отображаются только на прорисованных линиях и отсутствуют во всех других точках, не относящихся к этим линиям.</span><span class="sxs-lookup"><span data-stu-id="0adc2-111">The colors in the material or texture appear only along the lines drawn, not at any point in between the lines.</span></span>

<span data-ttu-id="0adc2-112">Следующий код показывает, как создать вершины для такого списка линий.</span><span class="sxs-lookup"><span data-stu-id="0adc2-112">The following code shows how to create vertices for this line list.</span></span>


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



<span data-ttu-id="0adc2-113">В приведенном ниже примере кода показано, как отобразить список строк в Direct3D 9 с помощью [**IDirect3DDevice9::D равпримитиве**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive).</span><span class="sxs-lookup"><span data-stu-id="0adc2-113">The code example below shows how to render a line list in Direct3D 9 using [**IDirect3DDevice9::DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive).</span></span>


```
//
// It is assumed that d3dDevice is a valid
// pointer to a IDirect3DDevice9 interface.
//
d3dDevice->DrawPrimitive( D3DPT_LINELIST, 0, 3 );
```



## <a name="related-topics"></a><span data-ttu-id="0adc2-114">См. также</span><span class="sxs-lookup"><span data-stu-id="0adc2-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0adc2-115">Примитивы</span><span class="sxs-lookup"><span data-stu-id="0adc2-115">Primitives</span></span>](primitives.md)
</dt> </dl>

 

 
