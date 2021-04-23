---
title: Смещение глубины
description: Многоугольники, копланар в трехмерном пространстве, могут выглядеть так, как если бы они не копланар, добавляя z-смещение (или смещение глубины) к каждому из них.
ms.assetid: ee904316-dc6d-48a4-bdb7-0f7dcdb9d9d6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d6f9a3850b03e033a90b358d0c6ffd1ceef830f
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "103797352"
---
# <a name="depth-bias"></a><span data-ttu-id="61039-103">Смещение глубины</span><span class="sxs-lookup"><span data-stu-id="61039-103">Depth Bias</span></span>

<span data-ttu-id="61039-104">Многоугольники, копланар в трехмерном пространстве, могут выглядеть так, как если бы они не копланар, добавляя z-смещение (или смещение глубины) к каждому из них.</span><span class="sxs-lookup"><span data-stu-id="61039-104">Polygons that are coplanar in 3D space can be made to appear as if they are not coplanar by adding a z-bias (or depth bias) to each one.</span></span>

<span data-ttu-id="61039-105">Это метод, который обычно используется для обеспечения правильного отображения теней в сцене.</span><span class="sxs-lookup"><span data-stu-id="61039-105">This is a technique commonly used to ensure that shadows in a scene are displayed properly.</span></span> <span data-ttu-id="61039-106">Например, тень на стене, скорее всего, будет иметь то же значение глубины, что и стенка.</span><span class="sxs-lookup"><span data-stu-id="61039-106">For instance, a shadow on a wall will likely have the same depth value as the wall.</span></span> <span data-ttu-id="61039-107">Если приложение сначала отображает стену, а затем тень, то тень может быть невидимой, а артефакты глубины могут быть видимыми.</span><span class="sxs-lookup"><span data-stu-id="61039-107">If an application renders a wall first and then a shadow, the shadow might not be visible, or depth artifacts might be visible.</span></span>


<span data-ttu-id="61039-108">Приложение может обеспечить правильное отображение многоугольников копланар, добавив сдвиг (от элемента **депсбиас** средства [**\_ прорисовки D3D11 \_ DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_rasterizer_desc1)) к значениям z, используемым системой при отрисовке наборов копланар многоугольников.</span><span class="sxs-lookup"><span data-stu-id="61039-108">An application can help ensure that coplanar polygons are rendered properly by adding the bias (from the **DepthBias** member of [**D3D11\_RASTERIZER\_DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_rasterizer_desc1)) to the z-values that the system uses when rendering the sets of coplanar polygons.</span></span> <span data-ttu-id="61039-109">Многоугольники с большим значением z будут отображаться перед многоугольниками с меньшим значением z.</span><span class="sxs-lookup"><span data-stu-id="61039-109">Polygons with a larger z value will be drawn in front of polygons with a smaller z value.</span></span>

<span data-ttu-id="61039-110">Существует два варианта вычисления смещения глубины.</span><span class="sxs-lookup"><span data-stu-id="61039-110">There are two options for calculating depth bias.</span></span>

1.  <span data-ttu-id="61039-111">Если буфер глубины, привязанный в настоящее время к этапу слияния вывода, имеет формат **UNORM** или не привязан буфер глубины, значение смещения вычисляется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="61039-111">If the depth buffer currently bound to the output-merger stage has a **UNORM** format or no depth buffer is bound, the bias value is calculated like this:</span></span>
    ```
    Bias = (float)DepthBias * r + SlopeScaledDepthBias * MaxDepthSlope;
    ```

    

    <span data-ttu-id="61039-112">где *r* — минимальное представимое значение > 0 в формате буфера глубины, преобразованном в **float32**.</span><span class="sxs-lookup"><span data-stu-id="61039-112">where *r* is the minimum representable value > 0 in the depth-buffer format converted to **float32**.</span></span> <span data-ttu-id="61039-113">Значения **депсбиас** и **слопескаледдепсбиас** — [**D3D11 средство \_ прорисовки \_ DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_rasterizer_desc1) члены структуры.</span><span class="sxs-lookup"><span data-stu-id="61039-113">The **DepthBias** and **SlopeScaledDepthBias** values are [**D3D11\_RASTERIZER\_DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_rasterizer_desc1) structure members.</span></span> <span data-ttu-id="61039-114">Значение **максдепсслопе** является максимальным значением горизонтального и вертикального наклоненной значения глубины в пикселе.</span><span class="sxs-lookup"><span data-stu-id="61039-114">The **MaxDepthSlope** value is the maximum of the horizontal and vertical slopes of the depth value at the pixel.</span></span>
2.  <span data-ttu-id="61039-115">Если буфер глубины с плавающей точкой привязан к этапу слияния вывода, значение смещения вычисляется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="61039-115">If a floating-point depth buffer is bound to the output-merger stage the bias value is calculated like this:</span></span>
    ```
    Bias = (float)DepthBias * 2**(exponent(max z in primitive) - r) +
                SlopeScaledDepthBias * MaxDepthSlope;
    ```

    

    <span data-ttu-id="61039-116">где *r* — число битов мантисса в представлении с плавающей запятой (за исключением скрытого бита); Например, 23 для **float32**.</span><span class="sxs-lookup"><span data-stu-id="61039-116">where *r* is the number of mantissa bits in the floating point representation (excluding the hidden bit); for example, 23 for **float32**.</span></span>

<span data-ttu-id="61039-117">Затем значение смещения будет заменяться следующим образом:</span><span class="sxs-lookup"><span data-stu-id="61039-117">The bias value is then clamped like this:</span></span>


```
if(DepthBiasClamp > 0)
    Bias = min(DepthBiasClamp, Bias)
else if(DepthBiasClamp < 0)
    Bias = max(DepthBiasClamp, Bias)
```



<span data-ttu-id="61039-118">Затем значение смещения используется для вычисления глубины пикселя.</span><span class="sxs-lookup"><span data-stu-id="61039-118">The bias value is then used to calculate the pixel depth.</span></span>


```
if ( (DepthBias != 0) || (SlopeScaledDepthBias != 0) )
    z = z + Bias
```



<span data-ttu-id="61039-119">Операции смещения глубины выполняются на вершинах после обрезки, поэтому смещение глубины не влияет на геометрическую отсечение.</span><span class="sxs-lookup"><span data-stu-id="61039-119">Depth-bias operations occur on vertices after clipping, therefore, depth-bias has no effect on geometric clipping.</span></span> <span data-ttu-id="61039-120">Значение смещения является константой для данного примитива и добавляется к значению z для каждой вершины перед настройкой интерполяции.</span><span class="sxs-lookup"><span data-stu-id="61039-120">The bias value is constant for a given primitive and is added to the z value for each vertex before interpolator setup.</span></span> <span data-ttu-id="61039-121">При использовании [уровней компонентов](overviews-direct3d-11-devices-downlevel-intro.md) 10,0 и выше все вычисления смещения выполняются с использованием 32-разрядных арифметических вычислений с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="61039-121">When you use [feature levels](overviews-direct3d-11-devices-downlevel-intro.md) 10.0 and higher, all bias calculations are performed using 32-bit floating-point arithmetic.</span></span> <span data-ttu-id="61039-122">Смещение не применяется к примитивным или строкам, за исключением линий, нарисованных в режиме каркаса.</span><span class="sxs-lookup"><span data-stu-id="61039-122">Bias is not applied to any point or line primitives, except for lines drawn in wireframe mode.</span></span>

<span data-ttu-id="61039-123">Одним из артефактов с тенями на основе теневого буфера является теневая акнека или затенение поверхности из-за незначительного различия между вычислениями глубины в шейдере и глубиной той же поверхности в теневом буфере.</span><span class="sxs-lookup"><span data-stu-id="61039-123">One of the artifacts with shadow buffer based shadows is shadow acne, or a surface shadowing itself due to minor differences between the depth computation in a shader, and the depth of the same surface in the shadow buffer.</span></span> <span data-ttu-id="61039-124">Одним из способов решения этой этой проблему является использование **депсбиас** и **слопескаледдепсбиас** при подготовке буфера теневого отображения.</span><span class="sxs-lookup"><span data-stu-id="61039-124">One way to alleviate this is to use **DepthBias** and **SlopeScaledDepthBias** when rendering a shadow buffer.</span></span> <span data-ttu-id="61039-125">Идея заключается в том, чтобы отправить поверхности достаточно при отрисовке теневого буфера, чтобы результат сравнения (между теневым буфером z и шейдером z) был согласованным по поверхности, и не использовать локальную самотень.</span><span class="sxs-lookup"><span data-stu-id="61039-125">The idea is to push surfaces out enough while rendering a shadow buffer so that the comparison result (between the shadow buffer z and the shader z) is consistent across the surface, and avoid local self-shadowing.</span></span>

<span data-ttu-id="61039-126">Однако использование **депсбиас** и **слопескаледдепсбиас** может привести к новым проблемам отрисовки, если многоугольник, просматривает очень острый угол, приводит к тому, что уравнение смещения создает очень большое значение z.</span><span class="sxs-lookup"><span data-stu-id="61039-126">However, using **DepthBias** and **SlopeScaledDepthBias** can introduce new rendering problems when a polygon viewed at an extremely sharp angle causes the bias equation to generate a very large z value.</span></span> <span data-ttu-id="61039-127">Это, в свою сторону, помещает многоугольник крайне далеко из исходной области на теневой карте.</span><span class="sxs-lookup"><span data-stu-id="61039-127">This in effect pushes the polygon extremely far away from the original surface in the shadow map.</span></span> <span data-ttu-id="61039-128">Одним из способов помочь обойти эту проблему является использование **депсбиаскламп**, который предоставляет верхнюю границу (положительное или отрицательное) на величину вычисляемого смещения z.</span><span class="sxs-lookup"><span data-stu-id="61039-128">One way to help alleviate this particular problem is to use **DepthBiasClamp**, which provides an upper bound (positive or negative) on the magnitude of the z bias calculated.</span></span>

> [!Note]  
> <span data-ttu-id="61039-129">Для [уровней компонентов](overviews-direct3d-11-devices-downlevel-intro.md) 9,1, 9,2, 9,3, **депсбиаскламп** не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="61039-129">For [feature levels](overviews-direct3d-11-devices-downlevel-intro.md) 9.1, 9.2, 9.3, **DepthBiasClamp** is not supported.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="61039-130">См. также</span><span class="sxs-lookup"><span data-stu-id="61039-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="61039-131">Стадия средства слияния вывода</span><span class="sxs-lookup"><span data-stu-id="61039-131">Output-Merger Stage</span></span>](d3d10-graphics-programming-guide-output-merger-stage.md)
</dt> </dl>

 

 




