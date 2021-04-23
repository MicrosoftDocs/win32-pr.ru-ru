---
description: Приложения C++ могут управлять влиянием тумана на цвет объектов в сцене, изменяя способ, которым Microsoft Direct3D будет рассчитывать эффекты тумана по расстоянию.
ms.assetid: b7148ae8-45c7-4dbe-8295-0335c7fdeff0
title: Формулы тумана (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75150a00d491f1e3fc1ea1444209449c1c2a825d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103894526"
---
# <a name="fog-formulas-direct3d-9"></a><span data-ttu-id="7b9e5-103">Формулы тумана (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="7b9e5-103">Fog Formulas (Direct3D 9)</span></span>

<span data-ttu-id="7b9e5-104">Приложения C++ могут управлять влиянием тумана на цвет объектов в сцене, изменяя способ, которым Microsoft Direct3D будет рассчитывать эффекты тумана по расстоянию.</span><span class="sxs-lookup"><span data-stu-id="7b9e5-104">C++ applications can control how fog affects the color of objects in a scene by changing how Microsoft Direct3D computes fog effects over distance.</span></span> <span data-ttu-id="7b9e5-105">Перечисляемый тип [**D3DFOGMODE**](./d3dfogmode.md) содержит члены, которые обозначают три формулы тумана.</span><span class="sxs-lookup"><span data-stu-id="7b9e5-105">The [**D3DFOGMODE**](./d3dfogmode.md) enumerated type contains members that identify the three fog formulas.</span></span> <span data-ttu-id="7b9e5-106">Во всех формулах коэффициент тумана вычисляется как функция расстояния, учитывая параметры, заданные приложением.</span><span class="sxs-lookup"><span data-stu-id="7b9e5-106">All formulas calculate a fog factor as a function of distance, given parameters that your application sets.</span></span>

## <a name="linear-fog"></a><span data-ttu-id="7b9e5-107">Линейный туман</span><span class="sxs-lookup"><span data-stu-id="7b9e5-107">Linear Fog</span></span>

<span data-ttu-id="7b9e5-108">Это задается со следующим \_ линейным уравнением D3DFOG.</span><span class="sxs-lookup"><span data-stu-id="7b9e5-108">This is set with the following D3DFOG\_LINEAR equation.</span></span>

![уравнение линейного тумана Direct3D](images/fogliner.png)

<span data-ttu-id="7b9e5-110">where</span><span class="sxs-lookup"><span data-stu-id="7b9e5-110">where</span></span>

-   <span data-ttu-id="7b9e5-111">Начало — это расстояние, с которого начинается эффект тумана.</span><span class="sxs-lookup"><span data-stu-id="7b9e5-111">start is the distance at which fog effects begin.</span></span>
-   <span data-ttu-id="7b9e5-112">конец — это расстояние, с которым эффекты тумана больше не увеличиваются.</span><span class="sxs-lookup"><span data-stu-id="7b9e5-112">end is the distance at which fog effects no longer increase.</span></span>
-   <span data-ttu-id="7b9e5-113">d представляет глубину или расстояние от точки зрения.</span><span class="sxs-lookup"><span data-stu-id="7b9e5-113">d represents depth, or the distance from the viewpoint.</span></span> <span data-ttu-id="7b9e5-114">Для тумана на основе диапазона значение d является расстоянием между положением камеры и вершиной.</span><span class="sxs-lookup"><span data-stu-id="7b9e5-114">For range based fog, the value for d is the distance between the camera position and a vertex.</span></span> <span data-ttu-id="7b9e5-115">Для тумана, не основанного на диапазоне, значение d является абсолютным значением координаты Z в пространстве камеры.</span><span class="sxs-lookup"><span data-stu-id="7b9e5-115">For non-range based fog, the value for d is the absolute value of the Z-coordinate in camera space.</span></span>

## <a name="exponential-fog"></a><span data-ttu-id="7b9e5-116">Экспоненциальный туман</span><span class="sxs-lookup"><span data-stu-id="7b9e5-116">Exponential Fog</span></span>

<span data-ttu-id="7b9e5-117">Линейные и экспоненциальные формулы поддерживаются как для пиксельных, так и для вершинных туманов.</span><span class="sxs-lookup"><span data-stu-id="7b9e5-117">Linear and exponential formulas are supported for both pixel fog and vertex fog.</span></span>

<span data-ttu-id="7b9e5-118">Это задается следующим \_ уравнением D3DFOG Exp.</span><span class="sxs-lookup"><span data-stu-id="7b9e5-118">This is set with the following D3DFOG\_EXP equation.</span></span>

![уравнение экспоненциального тумана Direct3D](images/fogexp.png)

<span data-ttu-id="7b9e5-120">where</span><span class="sxs-lookup"><span data-stu-id="7b9e5-120">where</span></span>

-   <span data-ttu-id="7b9e5-121">e — основание натуральных логарифмов (приблизительно 2,71828).</span><span class="sxs-lookup"><span data-stu-id="7b9e5-121">e is the base of natural logarithms (approximately 2.71828).</span></span>
-   <span data-ttu-id="7b9e5-122">плотность — это произвольная плотность тумана, которая может варьироваться от 0,0 до 1,0.</span><span class="sxs-lookup"><span data-stu-id="7b9e5-122">density is an arbitrary fog density that can range from 0.0 to 1.0.</span></span>
-   <span data-ttu-id="7b9e5-123">d представляет глубину или расстояние от точки зрения, как было сказано ранее.</span><span class="sxs-lookup"><span data-stu-id="7b9e5-123">d represents depth, or the distance from the viewpoint, as stated earlier.</span></span>

<span data-ttu-id="7b9e5-124">Это задается следующим \_ уравнением D3DFOG EXP2.</span><span class="sxs-lookup"><span data-stu-id="7b9e5-124">This is set with the following D3DFOG\_EXP2 equation.</span></span>

![уравнение экспоненциального тумана Direct3D 2](images/fogexp2.png)

<span data-ttu-id="7b9e5-126">where</span><span class="sxs-lookup"><span data-stu-id="7b9e5-126">where</span></span>

-   <span data-ttu-id="7b9e5-127">e — основание натуральных логарифмов, как указано выше.</span><span class="sxs-lookup"><span data-stu-id="7b9e5-127">e is the base of natural logarithms as stated above.</span></span>
-   <span data-ttu-id="7b9e5-128">плотность — это произвольная плотность тумана, которая может варьироваться от 0,0 до 1,0, как указано выше.</span><span class="sxs-lookup"><span data-stu-id="7b9e5-128">density is an arbitrary fog density that can range from 0.0 to 1.0 as stated above.</span></span>
-   <span data-ttu-id="7b9e5-129">d представляет глубину или расстояние от точки зрения, как указано выше.</span><span class="sxs-lookup"><span data-stu-id="7b9e5-129">d represents depth, or the distance from the viewpoint, as stated above.</span></span>

> [!Note]  
> <span data-ttu-id="7b9e5-130">Система сохраняет коэффициент тумана в альфа-компоненте отраженного цвета для вершины.</span><span class="sxs-lookup"><span data-stu-id="7b9e5-130">The system stores the fog factor in the alpha component of the specular color for a vertex.</span></span> <span data-ttu-id="7b9e5-131">Если приложение выполняет собственное преобразование и освещение, можно вставлять значения коэффициента тумана вручную, чтобы они были применены системой во время подготовки к просмотру.</span><span class="sxs-lookup"><span data-stu-id="7b9e5-131">If your application performs its own transformation and lighting, you can insert fog factor values manually, to be applied by the system during rendering.</span></span>

 

<span data-ttu-id="7b9e5-132">На следующей диаграмме показаны эти формулы с использованием общих значений, как в параметрах формулы.</span><span class="sxs-lookup"><span data-stu-id="7b9e5-132">The following graph shows these formulas, using common values as in the formula parameters.</span></span>

![Диаграмма для формул тумана по расстоянию и количеству цветов](images/foggraph.png)

<span data-ttu-id="7b9e5-134">\_Линейный D3DFOG — 1,0 в начале и 0,0 в конце.</span><span class="sxs-lookup"><span data-stu-id="7b9e5-134">D3DFOG\_LINEAR is 1.0 at start and 0.0 at end.</span></span> <span data-ttu-id="7b9e5-135">Он не измеряется относительно ближайших или дальнего плоскости.</span><span class="sxs-lookup"><span data-stu-id="7b9e5-135">It is not measured relative to the near or far planes.</span></span>

<span data-ttu-id="7b9e5-136">Когда Direct3D вычисляет эффекты тумана, он использует коэффициент тумана из одного из предыдущих уравнений в следующем уравнении смешения.</span><span class="sxs-lookup"><span data-stu-id="7b9e5-136">When Direct3D calculates fog effects, it uses the fog factor from one of the preceding equations in the following blending equation.</span></span>

![уравнение эффектов тумана для Direct3D](images/fogcalc.png)

<span data-ttu-id="7b9e5-138">Эта формула эффективно масштабирует цвет текущего многоугольника C на коэффициент тумана f и добавляет продукт к цвету тумана C, который масштабируется по побитовому инвертированию от фактора тумана.</span><span class="sxs-lookup"><span data-stu-id="7b9e5-138">This formula effectively scales the color of the current polygon C by the fog factor f, and adds the product to the fog color C, scaled by the bitwise inverse of the fog factor.</span></span> <span data-ttu-id="7b9e5-139">Полученное значение цвета — это смешение цвета тумана и исходного цвета в качестве коэффициента расстояния.</span><span class="sxs-lookup"><span data-stu-id="7b9e5-139">The resulting color value is a blend of the fog color and the original color, as a factor of distance.</span></span> <span data-ttu-id="7b9e5-140">Формула применяется ко всем устройствам, поддерживаемым в Microsoft DirectX 7,0 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="7b9e5-140">The formula applies to all devices supported in Microsoft DirectX 7.0 and later.</span></span> <span data-ttu-id="7b9e5-141">Для устройства с устаревшим пандусом фактор тумана масштабирует компоненты рассеянного и зеркального цвета с фиксацией в диапазоне от 0,0 до 1,0 включительно.</span><span class="sxs-lookup"><span data-stu-id="7b9e5-141">For the legacy ramp device, the fog factor scales the diffuse and specular color components, clamped to the range of 0.0 and 1.0, inclusive.</span></span> <span data-ttu-id="7b9e5-142">Коэффициент тумана обычно начинается с 1,0 для ближней плоскости и уменьшается до 0,0 на дальней плоскости.</span><span class="sxs-lookup"><span data-stu-id="7b9e5-142">The fog factor typically starts at 1.0 for the near plane and decreases to 0.0 at the far plane.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7b9e5-143">См. также</span><span class="sxs-lookup"><span data-stu-id="7b9e5-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7b9e5-144">Типы туманов</span><span class="sxs-lookup"><span data-stu-id="7b9e5-144">Fog Types</span></span>](fog-types.md)
</dt> </dl>

 

 
