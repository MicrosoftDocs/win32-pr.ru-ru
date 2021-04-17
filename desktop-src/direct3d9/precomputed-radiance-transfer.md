---
description: Предварительно вычисленный перенос Радианце (Direct3D 9)
ms.assetid: 2a233d23-9a9e-4774-9be0-f3bfe0369b21
title: Предварительно вычисленный перенос Радианце (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94829a2559888c61ae795309bac5d1ab699d7f27
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104566860"
---
# <a name="precomputed-radiance-transfer-direct3d-9"></a><span data-ttu-id="f7ea6-103">Предварительно вычисленный перенос Радианце (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="f7ea6-103">Precomputed Radiance Transfer (Direct3D 9)</span></span>

## <a name="using-precomputed-radiance-transfer"></a><span data-ttu-id="f7ea6-104">Использование предварительно вычисленного Радианценого перемещения</span><span class="sxs-lookup"><span data-stu-id="f7ea6-104">Using Precomputed Radiance Transfer</span></span>

<span data-ttu-id="f7ea6-105">В интересных сценах есть несколько форм сложности, в том числе способ моделирования среды освещения (т. е. модели освещения с областями по отношению к точкам и направлениям) и модели глобальных эффектов (например, тени, взаимозависимости, точечные подповерхности). Традиционные методы интерактивной отрисовки моделируют ограниченную степень сложности.</span><span class="sxs-lookup"><span data-stu-id="f7ea6-105">There are several forms of complexity present in interesting scenes, including how the lighting environment is modeled (that is, area lighting models versus point/directional ones) and what kind of global effects are modeled (for example, shadows, interreflections, subsurface scattering.) Traditional interactive rendering techniques model a limited amount of this complexity.</span></span> <span data-ttu-id="f7ea6-106">PRT обеспечивает эти эффекты с некоторыми существенными ограничениями.</span><span class="sxs-lookup"><span data-stu-id="f7ea6-106">PRT enables these effects with some significant restrictions:</span></span>

-   <span data-ttu-id="f7ea6-107">Предполагается, что объекты являются жесткими (то есть без преобразований).</span><span class="sxs-lookup"><span data-stu-id="f7ea6-107">Objects are assumed to be rigid (that is, no deformations).</span></span>
-   <span data-ttu-id="f7ea6-108">Это объектно-ориентированный подход (если объекты не перемещаются вместе, эти глобальные эффекты не поддерживаются).</span><span class="sxs-lookup"><span data-stu-id="f7ea6-108">It is an object-centric approach (unless objects are moved together, these global effects are not maintained between them).</span></span>
-   <span data-ttu-id="f7ea6-109">Моделируются только освещение с низкой частотой (что приводит к мягким теням). Для индикаторов высокой частоты (острых теней) следует применять традиционные методы.</span><span class="sxs-lookup"><span data-stu-id="f7ea6-109">Only low-frequency lighting is modeled (resulting in soft shadows.) For high-frequency lights (sharp shadows), traditional techniques would have to be employed.</span></span>

<span data-ttu-id="f7ea6-110">PRT требуется один из следующих типов, но не оба.</span><span class="sxs-lookup"><span data-stu-id="f7ea6-110">PRT requires either of the following, but not both:</span></span>

-   <span data-ttu-id="f7ea6-111">модели с высоким уровнем мозаики и VS \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="f7ea6-111">highly-tessellated models and vs\_1\_1</span></span>
-   <span data-ttu-id="f7ea6-112">PS \_ 2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="f7ea6-112">ps\_2\_0</span></span>

### <a name="standard-diffuse-lighting-versus-prt"></a><span data-ttu-id="f7ea6-113">Стандартное рассеянное освещение и PRT</span><span class="sxs-lookup"><span data-stu-id="f7ea6-113">Standard Diffuse Lighting versus PRT</span></span>

<span data-ttu-id="f7ea6-114">Следующая иллюстрация отображается с использованием традиционной модели освещения (n · l).</span><span class="sxs-lookup"><span data-stu-id="f7ea6-114">The following illustration is rendered using the traditional (n · l) lighting model.</span></span> <span data-ttu-id="f7ea6-115">Четкие тени можно включить с помощью другого прохода и какой-то другой способ создания тени (карты глубины тени или теневые тома).</span><span class="sxs-lookup"><span data-stu-id="f7ea6-115">Sharp shadows could be enabled using another pass and some form of shadowing technique (shadow depth maps or shadow volumes).</span></span> <span data-ttu-id="f7ea6-116">Добавление нескольких источников света потребует нескольких проходов (при использовании теней) или более сложных шейдеров с традиционными методами.</span><span class="sxs-lookup"><span data-stu-id="f7ea6-116">Adding multiple lights would require either multiple passes (if shadows are to be used) or more complex shaders with traditional techniques.</span></span>

![снимок экрана с изображением, отображаемым с помощью традиционной модели освещения](images/prt-diffuse-cropped.png)

<span data-ttu-id="f7ea6-118">Следующая иллюстрация отображается с PRT с использованием наилучшей аппроксимации одного направленного освещения, который он может разрешить.</span><span class="sxs-lookup"><span data-stu-id="f7ea6-118">The next illustration is rendered with PRT using the best approximation of a single directional light that it can resolve.</span></span> <span data-ttu-id="f7ea6-119">Это приводит к созданию мягких теней, которые трудно создать с помощью традиционных методов.</span><span class="sxs-lookup"><span data-stu-id="f7ea6-119">This results in soft shadows that would be difficult to produce with traditional techniques.</span></span> <span data-ttu-id="f7ea6-120">Поскольку PRT всегда моделирует завершение сред освещения, добавляя несколько источников света или карту среды, вы только изменяете значения (но не число) констант, используемых шейдером.</span><span class="sxs-lookup"><span data-stu-id="f7ea6-120">Because PRT always models complete lighting environments adding multiple lights or using an environment map, you would only change the values (but not the number) of constants used by the shader.</span></span>

![снимок экрана с изображением, отображаемым с помощью PRT](images/prt-diffuseshadows-cropped.png)

### <a name="prt-with-interreflections"></a><span data-ttu-id="f7ea6-122">PRT с использованием взаимоотражений</span><span class="sxs-lookup"><span data-stu-id="f7ea6-122">PRT with Interreflections</span></span>

<span data-ttu-id="f7ea6-123">Прямое освещение достигает поверхности непосредственно от света.</span><span class="sxs-lookup"><span data-stu-id="f7ea6-123">Direct lighting reaches the surface directly from the light.</span></span> <span data-ttu-id="f7ea6-124">При переходе на другую поверхность некоторые моменты между переделами становятся небольшими.</span><span class="sxs-lookup"><span data-stu-id="f7ea6-124">Interreflections are light reaching the surface after bouncing off some other surface some number of times.</span></span> <span data-ttu-id="f7ea6-125">PRT может моделировать это поведение без изменения производительности во время выполнения, просто запустив симулятор с различными параметрами.</span><span class="sxs-lookup"><span data-stu-id="f7ea6-125">PRT can model this behavior without changing the performance at run time by simply running the simulator with different parameters.</span></span>

<span data-ttu-id="f7ea6-126">Следующая иллюстрация создается только с прямым PRT (0 возвращается без прямых отражений).</span><span class="sxs-lookup"><span data-stu-id="f7ea6-126">The following illustration is created using direct PRT only (0 bounces with no interreflections).</span></span>

![снимок экрана с изображением, отображаемым только с прямым PRT](images/prt-nointerreflections.png)

<span data-ttu-id="f7ea6-128">На следующем рисунке создается с помощью PRT с пересчетами (2 отскоками с взаимоотражениями).</span><span class="sxs-lookup"><span data-stu-id="f7ea6-128">The following illustration is created using PRT with interreflections (2 bounces with interreflections).</span></span>

![снимок экрана с изображением, отображаемым с помощью PRT с использованием взаимоотражений](images/prt-interreflections.png)

### <a name="prt-with-subsurface-scattering"></a><span data-ttu-id="f7ea6-130">PRT с разбросами подповерхности</span><span class="sxs-lookup"><span data-stu-id="f7ea6-130">PRT with Subsurface Scattering</span></span>

<span data-ttu-id="f7ea6-131">Рассеивание подповерхности — это метод, который моделирует, как освещение проходит через определенные материалы.</span><span class="sxs-lookup"><span data-stu-id="f7ea6-131">Subsurface scattering is a technique that models how light passes through certain materials.</span></span> <span data-ttu-id="f7ea6-132">Например, нажмите кнопку с изображением фонарика для ладони своей руки.</span><span class="sxs-lookup"><span data-stu-id="f7ea6-132">As an example, press a lit flashlight against the palm of your hand.</span></span> <span data-ttu-id="f7ea6-133">Освещение от фонарик проходит через руки, перемещается вокруг (изменение цвета в процессе) и выходит с другой стороны руки.</span><span class="sxs-lookup"><span data-stu-id="f7ea6-133">The light from the flashlight passes through your hand, bounces around (changing color in the process), and exits from the other side of your hand.</span></span> <span data-ttu-id="f7ea6-134">Это также можно моделировать с помощью простых изменений в симуляторе и без изменений в среде выполнения.</span><span class="sxs-lookup"><span data-stu-id="f7ea6-134">This can also be modeled with simple changes to the simulator and no changes to the runtime.</span></span>

<span data-ttu-id="f7ea6-135">На следующем рисунке показано PRT с разбросами подповерхности.</span><span class="sxs-lookup"><span data-stu-id="f7ea6-135">The following illustration demonstrates PRT with subsurface scattering.</span></span>

![снимок экрана с изображением, отображаемым с помощью PRT с разбросами подповерхности](images/prt-subsurface.png)

## <a name="how-prt-works"></a><span data-ttu-id="f7ea6-137">Как работает PRT</span><span class="sxs-lookup"><span data-stu-id="f7ea6-137">How PRT Works</span></span>

<span data-ttu-id="f7ea6-138">Следующие термины полезны для понимания того, как работает PRT, как показано на следующей схеме.</span><span class="sxs-lookup"><span data-stu-id="f7ea6-138">The following terms are useful for understanding how PRT works, as illustrated in the following diagram.</span></span>

<span data-ttu-id="f7ea6-139">Source Радианце: источник радианце представляет среду освещения в целом.</span><span class="sxs-lookup"><span data-stu-id="f7ea6-139">Source Radiance: The source radiance represents the lighting environment as a whole.</span></span> <span data-ttu-id="f7ea6-140">В PRT произвольная среда приблизительна с учетом сферического гармонического. это освещение предполагается удаленно относительно объекта (то же самое предположение, которое было сделано с картами среды).</span><span class="sxs-lookup"><span data-stu-id="f7ea6-140">In PRT an arbitrary environment is approximated using the spherical harmonic basis - this lighting is assumed to be distant relative to the object (the same assumption that is made with environment maps.)</span></span>

<span data-ttu-id="f7ea6-141">Выход из Радианце: Exit радианце — это источник, который выходит с точки на поверхности с любого возможного источника (отражен радианце, рассеивание подповерхности, эмиссия).</span><span class="sxs-lookup"><span data-stu-id="f7ea6-141">Exit Radiance: Exit radiance is the light leaving from a point on the surface from any possible source (reflected radiance, subsurface scattering, emission).</span></span>

<span data-ttu-id="f7ea6-142">Векторы передачи: векторы передачи сопоставляют источник Радианце с выходом радианце и предварительно вычисляются в автономном режиме с помощью сложной модели освещения.</span><span class="sxs-lookup"><span data-stu-id="f7ea6-142">Transfer Vectors: Transfer vectors map Source Radiance into exit radiance and are precomputed offline using a complex light transport simulation.</span></span>

![Схема работы PRT](images/prt-lightingpicture.png)

<span data-ttu-id="f7ea6-144">PRT факторы процесса отрисовки в два этапа, как показано на следующей схеме:</span><span class="sxs-lookup"><span data-stu-id="f7ea6-144">PRT factors the rendering process into two stages, as shown in the following diagram:</span></span>

1.  <span data-ttu-id="f7ea6-145">Дорогостоящая модель освещения с низкой интенсивностью позволяет использовать коэффициенты передачи, которые могут использоваться во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="f7ea6-145">An expensive light transport simulation precomputes transfer coefficients that can be used at run time.</span></span>
2.  <span data-ttu-id="f7ea6-146">Относительно упрощенный этап времени выполнения сначала приблизительно отражает среду освещения с учетом сферического гармонического, а затем использует эти коэффициенты освещения и коэффициенты предварительно вычисленных передаваемых данных (из этапа 1) с простым шейдером, что приводит к выходу радианце (источнику, оставляемому объектом).</span><span class="sxs-lookup"><span data-stu-id="f7ea6-146">A relatively lightweight run-time stage first approximates the lighting environment using the spherical harmonic basis, then uses these lighting coefficients and the precomputed transfer coefficients (from stage 1) with a simple shader, resulting in exit radiance (the light leaving the object).</span></span>

![Схема потока данных PRT](images/prt-dataflow.png)

### <a name="how-to-use-the-prt-api"></a><span data-ttu-id="f7ea6-148">Как использовать API PRT</span><span class="sxs-lookup"><span data-stu-id="f7ea6-148">How to Use the PRT API</span></span>

1.  <span data-ttu-id="f7ea6-149">Вычисление векторов перемещения с помощью одного из вычислений... методы [**ID3DXPRTEngine**](id3dxprtengine.md).</span><span class="sxs-lookup"><span data-stu-id="f7ea6-149">Compute the transfer vectors with one of the Compute... methods of [**ID3DXPRTEngine**](id3dxprtengine.md).</span></span>

    <span data-ttu-id="f7ea6-150">Для непосредственного реагирования на эти векторы передач требуется значительный объем памяти и вычислений шейдеров.</span><span class="sxs-lookup"><span data-stu-id="f7ea6-150">Directly dealing with these transfer vectors requires a significant amount of memory and shader computation.</span></span> <span data-ttu-id="f7ea6-151">Сжатие значительно сокращает объем памяти и вычисление шейдера.</span><span class="sxs-lookup"><span data-stu-id="f7ea6-151">Compression significantly reduces the amount of memory and shader computation required.</span></span>

    <span data-ttu-id="f7ea6-152">Окончательные значения освещения вычисляются в шейдере вершин, который реализует следующее сжатое уравнение отрисовки.</span><span class="sxs-lookup"><span data-stu-id="f7ea6-152">The final lighting values are calculated in a vertex shader that implements the following compressed rendering equation.</span></span>

    ![уравнение отрисовки PRT](images/prt-shaderequation.png)

    <span data-ttu-id="f7ea6-154">Где:</span><span class="sxs-lookup"><span data-stu-id="f7ea6-154">Where:</span></span>

    

    | <span data-ttu-id="f7ea6-155">Параметр</span><span class="sxs-lookup"><span data-stu-id="f7ea6-155">Parameter</span></span>      | <span data-ttu-id="f7ea6-156">Описание</span><span class="sxs-lookup"><span data-stu-id="f7ea6-156">Description</span></span>                                                                                                     |
    |----------------|-----------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="f7ea6-157">RP</span><span class="sxs-lookup"><span data-stu-id="f7ea6-157">Rₚ</span></span>             | <span data-ttu-id="f7ea6-158">Один канал выхода радианце в вершине p и вычисляется на каждой вершине сетки.</span><span class="sxs-lookup"><span data-stu-id="f7ea6-158">A single channel of exit radiance at vertex p and is evaluated at every vertex on the mesh.</span></span>                     |
    | <span data-ttu-id="f7ea6-159">MK</span><span class="sxs-lookup"><span data-stu-id="f7ea6-159">Mₖ</span></span>             | <span data-ttu-id="f7ea6-160">Среднее для Cluster k.</span><span class="sxs-lookup"><span data-stu-id="f7ea6-160">The mean for cluster k.</span></span> <span data-ttu-id="f7ea6-161">Это порядковый вектор коэффициента ².</span><span class="sxs-lookup"><span data-stu-id="f7ea6-161">This is an Order² vector of coefficients.</span></span>                                               |
    | <span data-ttu-id="f7ea6-162">k</span><span class="sxs-lookup"><span data-stu-id="f7ea6-162">k</span></span>              | <span data-ttu-id="f7ea6-163">ИДЕНТИФИКАТОР кластера для вершины p.</span><span class="sxs-lookup"><span data-stu-id="f7ea6-163">The cluster ID for vertex p.</span></span>                                                                                    |
    | <span data-ttu-id="f7ea6-164">L<sup>'</sup></span><span class="sxs-lookup"><span data-stu-id="f7ea6-164">L<sup>'</sup></span></span>  | <span data-ttu-id="f7ea6-165">Приближение радианце источника к функциям SH.</span><span class="sxs-lookup"><span data-stu-id="f7ea6-165">The approximation of the source radiance into the SH basis functions.</span></span> <span data-ttu-id="f7ea6-166">Это порядковый вектор коэффициента ².</span><span class="sxs-lookup"><span data-stu-id="f7ea6-166">This is an Order² vector of coefficients.</span></span> |
    | <span data-ttu-id="f7ea6-167">j</span><span class="sxs-lookup"><span data-stu-id="f7ea6-167">j</span></span>              | <span data-ttu-id="f7ea6-168">Целое число, которое суммирует по количеству векторов PCA.</span><span class="sxs-lookup"><span data-stu-id="f7ea6-168">An integer that sums over the number of PCA vectors.</span></span>                                                            |
    | <span data-ttu-id="f7ea6-169">w<sub>PJ</sub></span><span class="sxs-lookup"><span data-stu-id="f7ea6-169">w<sub>pj</sub></span></span> | <span data-ttu-id="f7ea6-170">Вес ЖС PCA для точки p.</span><span class="sxs-lookup"><span data-stu-id="f7ea6-170">The jth PCA weight for point p.</span></span> <span data-ttu-id="f7ea6-171">Это один коэффициент.</span><span class="sxs-lookup"><span data-stu-id="f7ea6-171">This is a single coefficient.</span></span>                                                   |
    | <span data-ttu-id="f7ea6-172">Б<sub>KJ</sub></span><span class="sxs-lookup"><span data-stu-id="f7ea6-172">B<sub>kj</sub></span></span> | <span data-ttu-id="f7ea6-173">Вектор ЖС PCA для кластера k.</span><span class="sxs-lookup"><span data-stu-id="f7ea6-173">The jth PCA basis vector for cluster k.</span></span> <span data-ttu-id="f7ea6-174">Это порядковый вектор коэффициента ².</span><span class="sxs-lookup"><span data-stu-id="f7ea6-174">This is an Order² vector of coefficients.</span></span>                               |

    

     

    <span data-ttu-id="f7ea6-175">Извлечение... методы [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) обеспечивают доступ к сжатым данным из имитации.</span><span class="sxs-lookup"><span data-stu-id="f7ea6-175">The Extract... methods of [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) provide access to compressed data from the simulation.</span></span>

2.  <span data-ttu-id="f7ea6-176">Вычислите исходный радианце.</span><span class="sxs-lookup"><span data-stu-id="f7ea6-176">Compute the source radiance.</span></span>

    <span data-ttu-id="f7ea6-177">В API есть несколько вспомогательных функций для решения различных распространенных сценариев освещения.</span><span class="sxs-lookup"><span data-stu-id="f7ea6-177">There are several helper functions in the API to handle a variety of common lighting scenarios.</span></span>

    

    | <span data-ttu-id="f7ea6-178">Функция</span><span class="sxs-lookup"><span data-stu-id="f7ea6-178">Function</span></span>                                                         | <span data-ttu-id="f7ea6-179">Назначение</span><span class="sxs-lookup"><span data-stu-id="f7ea6-179">Purpose</span></span>                                                                                                     |
    |------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
    | [<span data-ttu-id="f7ea6-180">**D3DXSHEvalDirectionalLight**</span><span class="sxs-lookup"><span data-stu-id="f7ea6-180">**D3DXSHEvalDirectionalLight**</span></span>](d3dxshevaldirectionallight.md) | <span data-ttu-id="f7ea6-181">Приблизительный обычный направленный источник.</span><span class="sxs-lookup"><span data-stu-id="f7ea6-181">Approximates a conventional directional light.</span></span>                                                              |
    | [<span data-ttu-id="f7ea6-182">**D3DXSHEvalSphericalLight**</span><span class="sxs-lookup"><span data-stu-id="f7ea6-182">**D3DXSHEvalSphericalLight**</span></span>](d3dxshevalsphericallight.md)     | <span data-ttu-id="f7ea6-183">Приблизительные локальные источники освещения.</span><span class="sxs-lookup"><span data-stu-id="f7ea6-183">Approximates local spherical light sources.</span></span> <span data-ttu-id="f7ea6-184">(Обратите внимание, что PRT работает только с средами освещения расстояний.)</span><span class="sxs-lookup"><span data-stu-id="f7ea6-184">(Note that PRT only works with distance lighting environments.)</span></span> |
    | [<span data-ttu-id="f7ea6-185">**D3DXSHEvalConeLight**</span><span class="sxs-lookup"><span data-stu-id="f7ea6-185">**D3DXSHEvalConeLight**</span></span>](d3dxshevalconelight.md)               | <span data-ttu-id="f7ea6-186">Приближение к удаленному источнику освещения области.</span><span class="sxs-lookup"><span data-stu-id="f7ea6-186">Approximates a distant area light source.</span></span> <span data-ttu-id="f7ea6-187">В качестве примера можно привести солнце (очень маленький угол конуса).</span><span class="sxs-lookup"><span data-stu-id="f7ea6-187">An example would be the sun (very small cone angle).</span></span>              |
    | [<span data-ttu-id="f7ea6-188">**D3DXSHEvalHemisphereLight**</span><span class="sxs-lookup"><span data-stu-id="f7ea6-188">**D3DXSHEvalHemisphereLight**</span></span>](d3dxshevalhemispherelight.md)   | <span data-ttu-id="f7ea6-189">Вычисляет освещение, которое является линейной интерполяцией между двумя цветами (по одному на каждом полюсе сферы).</span><span class="sxs-lookup"><span data-stu-id="f7ea6-189">Evaluates a light that is a linear interpolation between two colors (one on each pole of a sphere).</span></span>         |

    

     

3.  <span data-ttu-id="f7ea6-190">Вычислите радианце выхода.</span><span class="sxs-lookup"><span data-stu-id="f7ea6-190">Compute the exit radiance.</span></span>

    <span data-ttu-id="f7ea6-191">Уравнение 1 теперь должно вычисляться в каждой точке с помощью шейдера вершин или пиксельных построителей текстуры.</span><span class="sxs-lookup"><span data-stu-id="f7ea6-191">Equation 1 now has to be evaluated at every point using either a vertex or pixel shader.</span></span> <span data-ttu-id="f7ea6-192">Перед вычислением шейдера необходимо предварительно вычислить константы и загрузить их в таблицу констант (Дополнительные сведения см. в [примере демонстрационного примера PRT](https://msdn.microsoft.com/library/Ee418763(v=VS.85).aspx) ).</span><span class="sxs-lookup"><span data-stu-id="f7ea6-192">Before the shader can be evaluated, constants have to be precomputed and loaded into the constant table (see the [PRT Demo Sample](https://msdn.microsoft.com/library/Ee418763(v=VS.85).aspx) for details).</span></span> <span data-ttu-id="f7ea6-193">Сам шейдер является простой реализацией этого уравнения.</span><span class="sxs-lookup"><span data-stu-id="f7ea6-193">The shader itself is a straightforward implementation of this equation.</span></span>

    ```
    struct VS_OUTPUT
    {
        float4 Position   : POSITION;   // vertex position 
        float2 TextureUV  : TEXCOORD0;  // vertex texture coordinates 
        float4 Diffuse    : COLOR0;     // vertex diffuse color
    };

    VS_OUTPUT Output;   
    Output.Position = mul(vPos, mWorldViewProjection);

    float4 vExitR = float4(0,0,0,0);
    float4 vExitG = float4(0,0,0,0);
    float4 vExitB = float4(0,0,0,0);
        
    for (int i=0; i < (NUM_PCA_VECTORS/4); i++) 
    {
       vExitR += vPCAWeights[i] * 
           vClusteredPCA[iClusterOffset+i+1+(NUM_PCA_VECTORS/4)*0];
       vExitG += vPCAWeights[i] * 
           vClusteredPCA[iClusterOffset+i+1+(NUM_PCA_VECTORS/4)*1];
       vExitB += vPCAWeights[i] * 
           vClusteredPCA[iClusterOffset+i+1+(NUM_PCA_VECTORS/4)*2];
    }
       
    float4 vExitRadiance = vClusteredPCA[iClusterOffset];
    vExitRadiance.r += dot(vExitR,1);
    vExitRadiance.g += dot(vExitG,1);
    vExitRadiance.b += dot(vExitB,1);

    Output.Diffuse = vExitRadiance;
    ```

    

## <a name="references"></a><span data-ttu-id="f7ea6-194">Ссылки</span><span class="sxs-lookup"><span data-stu-id="f7ea6-194">References</span></span>

<span data-ttu-id="f7ea6-195">Дополнительные сведения о PRT и сферных гармониях см. в следующих документах:</span><span class="sxs-lookup"><span data-stu-id="f7ea6-195">For more information about PRT and spherical harmonics, see the following papers:</span></span>


```
Precomputed Radiance Transfer for Real-Time Rendering in Dynamic, 
Low-Frequency Lighting Environments 
P.-P. Sloan, J. Kautz, J. Snyder
SIGGRAPH 2002 

Clustered Principal Components for Precomputed Radiance Transfer 
P.-P. Sloan, J. Hall, J. Hart, J. Snyder 
SIGGRAPH 2003 

Efficient Evaluation of Irradiance Environment Maps 
P.-P. Sloan 
ShaderX 2,  W. Engel 

Spherical Harmonic Lighting: The Gritty Details 
R. Green 
GDC 2003 

An Efficient Representation for Irradiance Environment Maps 
R. Ramamoorthi, P. Hanrahan 

A Practical Model for Subsurface Light Transport 
H. W. Jensen, S. R. Marschner, M. Levoy, and P. Hanrahan 
SIGGRAPH 2001 

Bi-Scale Radiance Transfer 
P.-P. Sloan, X. Liu, H.-Y. Shum, J. Snyder
SIGGRAPH 2003 

Fast, Arbitrary BRDF Shading for Low-Frequency Lighting Using Spherical 
Harmonics 
J. Kautz, P.-P. Sloan, J. Snyder
12th Eurographics Workshop on Rendering 

Precomputing Interactive Dynamic Deformable Scenes 
D. James, K. Fatahalian 
SIGGRAPH 2003 

All-Frequency Shadows Using Non-linear Wavelet Lighting Approximation 
R. Ng, R. Ramamoorth, P. Hanrahan 
SIGGRAPH 2003 

Matrix Radiance Transfer 
J. Lehtinen, J. Kautz
SIGGRAPH 2003 

Math World 
E. W. Weisstein, Wolfram Research, Inc. 

Quantum Theory of Angular Momentum 
D. A. Varshalovich, A.N. Moskalev, V.K. Khersonskii 
```



## <a name="related-topics"></a><span data-ttu-id="f7ea6-196">См. также</span><span class="sxs-lookup"><span data-stu-id="f7ea6-196">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f7ea6-197">Дополнительные разделы</span><span class="sxs-lookup"><span data-stu-id="f7ea6-197">Advanced Topics</span></span>](advanced-topics.md)
</dt> <dt>

[<span data-ttu-id="f7ea6-198">Уравнения PRT (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="f7ea6-198">PRT Equations (Direct3D 9)</span></span>](prt-equations.md)
</dt> <dt>

[<span data-ttu-id="f7ea6-199">Представление PRT с текстурами (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="f7ea6-199">Representing PRT With Textures (Direct3D 9)</span></span>](representing-prt-with-textures.md)
</dt> <dt>

[<span data-ttu-id="f7ea6-200">**ID3DXPRTBuffer**</span><span class="sxs-lookup"><span data-stu-id="f7ea6-200">**ID3DXPRTBuffer**</span></span>](id3dxprtbuffer.md)
</dt> <dt>

[<span data-ttu-id="f7ea6-201">**ID3DXPRTCompBuffer**</span><span class="sxs-lookup"><span data-stu-id="f7ea6-201">**ID3DXPRTCompBuffer**</span></span>](id3dxprtcompbuffer.md)
</dt> <dt>

[<span data-ttu-id="f7ea6-202">**ID3DXPRTEngine**</span><span class="sxs-lookup"><span data-stu-id="f7ea6-202">**ID3DXPRTEngine**</span></span>](id3dxprtengine.md)
</dt> <dt>

[<span data-ttu-id="f7ea6-203">**ID3DXTextureGutterHelper**</span><span class="sxs-lookup"><span data-stu-id="f7ea6-203">**ID3DXTextureGutterHelper**</span></span>](id3dxtexturegutterhelper.md)
</dt> <dt>

[<span data-ttu-id="f7ea6-204">Предварительно вычисленные функции пересылки Радианце</span><span class="sxs-lookup"><span data-stu-id="f7ea6-204">Precomputed Radiance Transfer Functions</span></span>](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> <dt>

[<span data-ttu-id="f7ea6-205">Математические функции</span><span class="sxs-lookup"><span data-stu-id="f7ea6-205">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 



