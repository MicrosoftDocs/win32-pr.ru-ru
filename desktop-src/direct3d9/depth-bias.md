---
description: Многоугольники, копланар в трехмерном пространстве, могут выглядеть так, как если бы они не копланар, путем добавления z-смещения к каждому из них.
ms.assetid: 0ab4f63b-49de-4bd0-a10f-6f90b9706c58
title: Смещение глубины (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ce605ea1df161e5ebfed95c214c3dd180ab7ee6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104494925"
---
# <a name="depth-bias-direct3d-9"></a><span data-ttu-id="93b02-103">Смещение глубины (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="93b02-103">Depth Bias (Direct3D 9)</span></span>

<span data-ttu-id="93b02-104">Многоугольники, копланар в трехмерном пространстве, могут выглядеть так, как если бы они не копланар, путем добавления z-смещения к каждому из них.</span><span class="sxs-lookup"><span data-stu-id="93b02-104">Polygons that are coplanar in your 3D space can be made to appear as if they are not coplanar by adding a z-bias to each one.</span></span> <span data-ttu-id="93b02-105">Это метод, который обычно используется для обеспечения правильного отображения теней в сцене.</span><span class="sxs-lookup"><span data-stu-id="93b02-105">This is a technique commonly used to ensure that shadows in a scene are displayed properly.</span></span> <span data-ttu-id="93b02-106">Например, тень на стене, скорее всего, будет иметь то же значение глубины, что и стенка.</span><span class="sxs-lookup"><span data-stu-id="93b02-106">For instance, a shadow on a wall will likely have the same depth value as the wall does.</span></span> <span data-ttu-id="93b02-107">Если сначала отобразить стену, а затем тень, теневая копия может быть невидимой, а также могут быть видны артефакты глубины.</span><span class="sxs-lookup"><span data-stu-id="93b02-107">If you render the wall first and then the shadow, the shadow might not be visible, or depth artifacts might be visible.</span></span> <span data-ttu-id="93b02-108">Можно изменить порядок отрисовки объектов копланар в надеется, чтобы отменить действие, но артефакты глубины все еще вероятны.</span><span class="sxs-lookup"><span data-stu-id="93b02-108">You can reverse the order in which you render the coplanar objects in hopes of reversing the effect, but depth artifacts are still likely.</span></span>

<span data-ttu-id="93b02-109">Приложение может обеспечить правильное отображение многоугольников копланар, добавив сдвиг к значениям z, которые система использует при отрисовке наборов многоугольников копланар.</span><span class="sxs-lookup"><span data-stu-id="93b02-109">An application can help ensure that coplanar polygons are rendered properly by adding a bias to the z-values that the system uses when rendering the sets of coplanar polygons.</span></span> <span data-ttu-id="93b02-110">Чтобы добавить сдвиг z к набору многоугольников, вызовите метод [**IDirect3DDevice9:: сетрендерстате**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) непосредственно перед их отображением, установив для параметра *State* значение D3DRS \_ депсбиас, а параметр *value* — для подходящего значения float (например, подходящее значение может быть от-1,0 до 1,0); чтобы передать это значение в **Сетрендерстате**, необходимо также привести значение к типу **DWORD**.</span><span class="sxs-lookup"><span data-stu-id="93b02-110">To add a z-bias to a set of polygons, call the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method just before rendering them, setting the *State* parameter to D3DRS\_DEPTHBIAS, and the *Value* parameter to a suitable float value (for example, a suitable value might be from -1.0 to 1.0); to pass this value to **SetRenderState**, you must also cast the value to a **DWORD**.</span></span> <span data-ttu-id="93b02-111">Более высокое значение z-смещения увеличивает вероятность того, что отображаемые многоугольники будут видны при отображении с другими копланар многоугольниками.</span><span class="sxs-lookup"><span data-stu-id="93b02-111">A higher z-bias value increases the likelihood that the polygons you render will be visible when displayed with other coplanar polygons.</span></span>


```
Offset = m * D3DRS_SLOPESCALEDEPTHBIAS + D3DRS_DEPTHBIAS
```



<span data-ttu-id="93b02-112">где m — это максимальная глубина глубины отображаемого треугольника.</span><span class="sxs-lookup"><span data-stu-id="93b02-112">where m is the maximum depth slope of the triangle being rendered.</span></span>


```
m = max(abs(delta z / delta x), abs(delta z / delta y)) 
```



<span data-ttu-id="93b02-113">Единицы измерения для D3DRS \_ депсбиас и D3DRS \_ слопескаледепсбиас, зависят от того, включена ли z-буферизация или w-buffer.</span><span class="sxs-lookup"><span data-stu-id="93b02-113">The units for the D3DRS\_DEPTHBIAS and D3DRS\_SLOPESCALEDEPTHBIAS render states depend on whether z-buffering or w-buffering is enabled.</span></span> <span data-ttu-id="93b02-114">Приложение должно предоставить подходящие значения.</span><span class="sxs-lookup"><span data-stu-id="93b02-114">The application must provide suitable values.</span></span>

<span data-ttu-id="93b02-115">Этот сдвиг не применяется к какой-либо линии и примитиву точки.</span><span class="sxs-lookup"><span data-stu-id="93b02-115">The bias is not applied to any line and point primitive.</span></span> <span data-ttu-id="93b02-116">Однако этот сдвиг должен применяться к треугольникам, нарисованным в режиме каркаса.</span><span class="sxs-lookup"><span data-stu-id="93b02-116">However, this bias needs to be applied to triangles drawn in wireframe mode.</span></span>


```
// RenderStates
D3DRS_SLOPESCALEDEPTHBIAS, // Defaults to zero
D3DRS_DEPTHBIAS,           // Defaults to zero
```




```
// Caps
D3DPRASTERCAPS_DEPTHBIAS           
D3DPRASTERCAPS_SLOPESCALEDEPTHBIAS 
```



## <a name="related-topics"></a><span data-ttu-id="93b02-117">См. также</span><span class="sxs-lookup"><span data-stu-id="93b02-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="93b02-118">Конвейер пикселей</span><span class="sxs-lookup"><span data-stu-id="93b02-118">Pixel Pipeline</span></span>](pixel-pipeline.md)
</dt> </dl>

 

 
