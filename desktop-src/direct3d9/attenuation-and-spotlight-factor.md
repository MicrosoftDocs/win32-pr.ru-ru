---
description: Компоненты рассеянного и зеркального света глобального уравнения света содержат термины, описывающие затухание света и конус вспышки. Эти термины описаны ниже.
ms.assetid: 960b5fc2-3074-4e51-b3de-5ed370379b01
title: Ослабление и отличительные коэффициенты (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 623bb3cb2b1c2a3ee9e0e5d9419ff71dd9a303b6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104551590"
---
# <a name="attenuation-and-spotlight-factor-direct3d-9"></a><span data-ttu-id="ab6be-104">Ослабление и отличительные коэффициенты (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="ab6be-104">Attenuation and Spotlight Factor (Direct3D 9)</span></span>

<span data-ttu-id="ab6be-105">Компоненты рассеянного и зеркального света глобального уравнения света содержат термины, описывающие затухание света и конус вспышки.</span><span class="sxs-lookup"><span data-stu-id="ab6be-105">The diffuse and specular lighting components of the global illumination equation contain terms that describe light attenuation and the spotlight cone.</span></span> <span data-ttu-id="ab6be-106">Эти термины описаны ниже.</span><span class="sxs-lookup"><span data-stu-id="ab6be-106">These terms are described below.</span></span>

## <a name="attenuation"></a><span data-ttu-id="ab6be-107">Затухание</span><span class="sxs-lookup"><span data-stu-id="ab6be-107">Attenuation</span></span>

<span data-ttu-id="ab6be-108">Затухание света зависит от типа света и расстояния между светом и положением вершины.</span><span class="sxs-lookup"><span data-stu-id="ab6be-108">The attenuation of a light depends on the type of light and the distance between the light and the vertex position.</span></span> <span data-ttu-id="ab6be-109">Чтобы вычислить затухание, используйте одну из следующих формул.</span><span class="sxs-lookup"><span data-stu-id="ab6be-109">To calculate attenuation, use one of the following equations.</span></span>

<span data-ttu-id="ab6be-110">Аттен = 1/(att0<sub>i</sub> + Att1<sub>i</sub> + \* att2<sub>я</sub> \* d ²)</span><span class="sxs-lookup"><span data-stu-id="ab6be-110">Atten = 1/( att0<sub>i</sub> + att1<sub>i</sub> \* d + att2<sub>i</sub> \* d²)</span></span>

<span data-ttu-id="ab6be-111">Где:</span><span class="sxs-lookup"><span data-stu-id="ab6be-111">Where:</span></span>



| <span data-ttu-id="ab6be-112">Параметр</span><span class="sxs-lookup"><span data-stu-id="ab6be-112">Parameter</span></span>        | <span data-ttu-id="ab6be-113">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="ab6be-113">Default value</span></span> | <span data-ttu-id="ab6be-114">Тип</span><span class="sxs-lookup"><span data-stu-id="ab6be-114">Type</span></span>  | <span data-ttu-id="ab6be-115">Description</span><span class="sxs-lookup"><span data-stu-id="ab6be-115">Description</span></span>                                     | <span data-ttu-id="ab6be-116">Диапазон</span><span class="sxs-lookup"><span data-stu-id="ab6be-116">Range</span></span>          |
|------------------|---------------|-------|-------------------------------------------------|----------------|
| <span data-ttu-id="ab6be-117">att0<sub>i</sub></span><span class="sxs-lookup"><span data-stu-id="ab6be-117">att0<sub>i</sub></span></span> | <span data-ttu-id="ab6be-118">0,0</span><span class="sxs-lookup"><span data-stu-id="ab6be-118">0.0</span></span>           | <span data-ttu-id="ab6be-119">FLOAT</span><span class="sxs-lookup"><span data-stu-id="ab6be-119">FLOAT</span></span> | <span data-ttu-id="ab6be-120">Константный коэффициент затухания</span><span class="sxs-lookup"><span data-stu-id="ab6be-120">Constant attenuation factor</span></span>                     | <span data-ttu-id="ab6be-121">от 0 до +∞</span><span class="sxs-lookup"><span data-stu-id="ab6be-121">0 to +infinity</span></span> |
| <span data-ttu-id="ab6be-122">att1<sub>i</sub></span><span class="sxs-lookup"><span data-stu-id="ab6be-122">att1<sub>i</sub></span></span> | <span data-ttu-id="ab6be-123">0,0</span><span class="sxs-lookup"><span data-stu-id="ab6be-123">0.0</span></span>           | <span data-ttu-id="ab6be-124">FLOAT</span><span class="sxs-lookup"><span data-stu-id="ab6be-124">FLOAT</span></span> | <span data-ttu-id="ab6be-125">Линейный коэффициент затухания</span><span class="sxs-lookup"><span data-stu-id="ab6be-125">Linear attenuation factor</span></span>                       | <span data-ttu-id="ab6be-126">от 0 до +∞</span><span class="sxs-lookup"><span data-stu-id="ab6be-126">0 to +infinity</span></span> |
| <span data-ttu-id="ab6be-127">att2<sub>i</sub></span><span class="sxs-lookup"><span data-stu-id="ab6be-127">att2<sub>i</sub></span></span> | <span data-ttu-id="ab6be-128">0,0</span><span class="sxs-lookup"><span data-stu-id="ab6be-128">0.0</span></span>           | <span data-ttu-id="ab6be-129">FLOAT</span><span class="sxs-lookup"><span data-stu-id="ab6be-129">FLOAT</span></span> | <span data-ttu-id="ab6be-130">Квадратический коэффициент затухания</span><span class="sxs-lookup"><span data-stu-id="ab6be-130">Quadratic attenuation factor</span></span>                    | <span data-ttu-id="ab6be-131">от 0 до +∞</span><span class="sxs-lookup"><span data-stu-id="ab6be-131">0 to +infinity</span></span> |
| <span data-ttu-id="ab6be-132">d</span><span class="sxs-lookup"><span data-stu-id="ab6be-132">d</span></span>                | <span data-ttu-id="ab6be-133">Н/Д</span><span class="sxs-lookup"><span data-stu-id="ab6be-133">N/A</span></span>           | <span data-ttu-id="ab6be-134">FLOAT</span><span class="sxs-lookup"><span data-stu-id="ab6be-134">FLOAT</span></span> | <span data-ttu-id="ab6be-135">Расстояние от положения вершины до положения света</span><span class="sxs-lookup"><span data-stu-id="ab6be-135">Distance from vertex position to light position</span></span> | <span data-ttu-id="ab6be-136">Н/Д</span><span class="sxs-lookup"><span data-stu-id="ab6be-136">N/A</span></span>            |



 

-   <span data-ttu-id="ab6be-137">Atten = 1, если свет является направленным светом.</span><span class="sxs-lookup"><span data-stu-id="ab6be-137">Atten = 1, if the light is a directional light.</span></span>
-   <span data-ttu-id="ab6be-138">Atten = 0, если расстояние между светом и вершиной превышает диапазон света.</span><span class="sxs-lookup"><span data-stu-id="ab6be-138">Atten = 0, if the distance between the light and the vertex exceeds the light's range.</span></span>

<span data-ttu-id="ab6be-139">Значения att0, Att1 и att2 задаются членами Attenuation0, Attenuation1 и Attenuation2 в [**D3DLIGHT9**](d3dlight9.md).</span><span class="sxs-lookup"><span data-stu-id="ab6be-139">The att0, att1, att2 values are specified by the Attenuation0, Attenuation1, and Attenuation2 members of [**D3DLIGHT9**](d3dlight9.md).</span></span>

<span data-ttu-id="ab6be-140">Расстояние между светом и положением вершины всегда положительное.</span><span class="sxs-lookup"><span data-stu-id="ab6be-140">The distance between the light and the vertex position is always positive.</span></span>

<span data-ttu-id="ab6be-141">d = \| L<sub>dir</sub>\|</span><span class="sxs-lookup"><span data-stu-id="ab6be-141">d = \| L<sub>dir</sub> \|</span></span>

<span data-ttu-id="ab6be-142">Где:</span><span class="sxs-lookup"><span data-stu-id="ab6be-142">Where:</span></span>



| <span data-ttu-id="ab6be-143">Параметр</span><span class="sxs-lookup"><span data-stu-id="ab6be-143">Parameter</span></span>       | <span data-ttu-id="ab6be-144">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="ab6be-144">Default value</span></span> | <span data-ttu-id="ab6be-145">Тип</span><span class="sxs-lookup"><span data-stu-id="ab6be-145">Type</span></span>      | <span data-ttu-id="ab6be-146">Описание</span><span class="sxs-lookup"><span data-stu-id="ab6be-146">Description</span></span>                                                 |
|-----------------|---------------|-----------|-------------------------------------------------------------|
| <span data-ttu-id="ab6be-147">L<sub>dir</sub></span><span class="sxs-lookup"><span data-stu-id="ab6be-147">L<sub>dir</sub></span></span> | <span data-ttu-id="ab6be-148">Н/Д</span><span class="sxs-lookup"><span data-stu-id="ab6be-148">N/A</span></span>           | <span data-ttu-id="ab6be-149">D3DVECTOR</span><span class="sxs-lookup"><span data-stu-id="ab6be-149">D3DVECTOR</span></span> | <span data-ttu-id="ab6be-150">Вектор направления от положения вершины до положения света</span><span class="sxs-lookup"><span data-stu-id="ab6be-150">Direction vector from vertex position to the light position</span></span> |



 

<span data-ttu-id="ab6be-151">Если значение d больше, чем диапазон освещения, то есть элемент Range структуры [**D3DLIGHT9**](d3dlight9.md) , то Direct3D не делает никаких дополнительных вычислений ослабления и не применяет эффекты с самого светлого к вершине.</span><span class="sxs-lookup"><span data-stu-id="ab6be-151">If d is greater than the light's range, that is, the Range member of a [**D3DLIGHT9**](d3dlight9.md) structure, Direct3D makes no further attenuation calculations and applies no effects from the light to the vertex.</span></span>

<span data-ttu-id="ab6be-152">Константы затухания функционируют в качестве коэффициентов в формуле: можно создать несколько кривых затухания, внеся в них простые коррективы.</span><span class="sxs-lookup"><span data-stu-id="ab6be-152">The attenuation constants act as coefficients in the formula - you can produce a variety of attenuation curves by making simple adjustments to them.</span></span> <span data-ttu-id="ab6be-153">Можно настроить значение Attenuation1 равным 1,0, чтобы создать свет, который не затухает, но все равно ограничен диапазоном. Либо можно экспериментировать с разными значениями для достижения разных эффектов затухания.</span><span class="sxs-lookup"><span data-stu-id="ab6be-153">You can set Attenuation1 to 1.0 to create a light that doesn't attenuate but is still limited by range, or you can experiment with different values to achieve various attenuation effects.</span></span>

<span data-ttu-id="ab6be-154">Затухание в максимальном диапазоне света не равно 0,0.</span><span class="sxs-lookup"><span data-stu-id="ab6be-154">The attenuation at the maximum range of the light is not 0.0.</span></span> <span data-ttu-id="ab6be-155">Чтобы не допустить случайного отображения света при нахождении в диапазоне света, приложение может увеличить диапазон света.</span><span class="sxs-lookup"><span data-stu-id="ab6be-155">To prevent lights from suddenly appearing when they are at the light range, an application can increase the light range.</span></span> <span data-ttu-id="ab6be-156">Либо приложение может настроить константы затухания так, чтобы коэффициент затухания был близок к 0,0 в диапазоне света.</span><span class="sxs-lookup"><span data-stu-id="ab6be-156">Or, the application can set up attenuation constants so that the attenuation factor is close to 0.0 at the light range.</span></span> <span data-ttu-id="ab6be-157">Значение затухания умножается на компоненты красного, зеленого и синего цветов света, чтобы регулировать интенсивность света как коэффициент расстояния, которое свет проходит до вершины.</span><span class="sxs-lookup"><span data-stu-id="ab6be-157">The attenuation value is multiplied by the red, green, and blue components of the light's color to scale the light's intensity as a factor of the distance light travels to a vertex.</span></span>

## <a name="spotlight-factor"></a><span data-ttu-id="ab6be-158">Коэффициент вспышки</span><span class="sxs-lookup"><span data-stu-id="ab6be-158">Spotlight Factor</span></span>

<span data-ttu-id="ab6be-159">Следующее уравнение задает коэффициент вспышки.</span><span class="sxs-lookup"><span data-stu-id="ab6be-159">The following equation specifies the spotlight factor.</span></span>

![Уравнение с коэффициентом вспышки](images/dx8light9.png)



| <span data-ttu-id="ab6be-161">Параметр</span><span class="sxs-lookup"><span data-stu-id="ab6be-161">Parameter</span></span>         | <span data-ttu-id="ab6be-162">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="ab6be-162">Default value</span></span> | <span data-ttu-id="ab6be-163">Тип</span><span class="sxs-lookup"><span data-stu-id="ab6be-163">Type</span></span>  | <span data-ttu-id="ab6be-164">Description</span><span class="sxs-lookup"><span data-stu-id="ab6be-164">Description</span></span>                              | <span data-ttu-id="ab6be-165">Диапазон</span><span class="sxs-lookup"><span data-stu-id="ab6be-165">Range</span></span>                    |
|-------------------|---------------|-------|------------------------------------------|--------------------------|
| <span data-ttu-id="ab6be-166">Ро<sub>i</sub></span><span class="sxs-lookup"><span data-stu-id="ab6be-166">rho<sub>i</sub></span></span>   | <span data-ttu-id="ab6be-167">Н/Д</span><span class="sxs-lookup"><span data-stu-id="ab6be-167">N/A</span></span>           | <span data-ttu-id="ab6be-168">FLOAT</span><span class="sxs-lookup"><span data-stu-id="ab6be-168">FLOAT</span></span> | <span data-ttu-id="ab6be-169">cosine(угол) для i света</span><span class="sxs-lookup"><span data-stu-id="ab6be-169">cosine(angle) for spotlight i</span></span>            | <span data-ttu-id="ab6be-170">Н/Д</span><span class="sxs-lookup"><span data-stu-id="ab6be-170">N/A</span></span>                      |
| <span data-ttu-id="ab6be-171">phi<sub>i</sub></span><span class="sxs-lookup"><span data-stu-id="ab6be-171">phi<sub>i</sub></span></span>   | <span data-ttu-id="ab6be-172">0,0</span><span class="sxs-lookup"><span data-stu-id="ab6be-172">0.0</span></span>           | <span data-ttu-id="ab6be-173">FLOAT</span><span class="sxs-lookup"><span data-stu-id="ab6be-173">FLOAT</span></span> | <span data-ttu-id="ab6be-174">Угол мягкого затенения вспышки i в радиусе</span><span class="sxs-lookup"><span data-stu-id="ab6be-174">Penumbra angle of spotlight i in radians</span></span> | <span data-ttu-id="ab6be-175">\[тета<sub>i</sub>, PI)</span><span class="sxs-lookup"><span data-stu-id="ab6be-175">\[theta<sub>i</sub>, pi)</span></span> |
| <span data-ttu-id="ab6be-176">theta<sub>i</sub></span><span class="sxs-lookup"><span data-stu-id="ab6be-176">theta<sub>i</sub></span></span> | <span data-ttu-id="ab6be-177">0,0</span><span class="sxs-lookup"><span data-stu-id="ab6be-177">0.0</span></span>           | <span data-ttu-id="ab6be-178">FLOAT</span><span class="sxs-lookup"><span data-stu-id="ab6be-178">FLOAT</span></span> | <span data-ttu-id="ab6be-179">Угол полной тени вспышки i в радиусе</span><span class="sxs-lookup"><span data-stu-id="ab6be-179">Umbra angle of spotlight i in radians</span></span>    | <span data-ttu-id="ab6be-180">\[0, PI)</span><span class="sxs-lookup"><span data-stu-id="ab6be-180">\[0, pi)</span></span>                 |
| <span data-ttu-id="ab6be-181">снижение</span><span class="sxs-lookup"><span data-stu-id="ab6be-181">falloff</span></span>           | <span data-ttu-id="ab6be-182">0,0</span><span class="sxs-lookup"><span data-stu-id="ab6be-182">0.0</span></span>           | <span data-ttu-id="ab6be-183">FLOAT</span><span class="sxs-lookup"><span data-stu-id="ab6be-183">FLOAT</span></span> | <span data-ttu-id="ab6be-184">Коэффициент снижения</span><span class="sxs-lookup"><span data-stu-id="ab6be-184">Falloff factor</span></span>                           | <span data-ttu-id="ab6be-185">(-∞ + ∞)</span><span class="sxs-lookup"><span data-stu-id="ab6be-185">(-infinity, +infinity)</span></span>   |



 

<span data-ttu-id="ab6be-186">Где:</span><span class="sxs-lookup"><span data-stu-id="ab6be-186">Where:</span></span>

<span data-ttu-id="ab6be-187">rho = norm(L<sub>dcs</sub>)<sup>.</sup>norm(L<sub>dir</sub>)</span><span class="sxs-lookup"><span data-stu-id="ab6be-187">rho = norm(L<sub>dcs</sub>)<sup>.</sup>norm(L<sub>dir</sub>)</span></span>

<span data-ttu-id="ab6be-188">and:</span><span class="sxs-lookup"><span data-stu-id="ab6be-188">and:</span></span>



| <span data-ttu-id="ab6be-189">Параметр</span><span class="sxs-lookup"><span data-stu-id="ab6be-189">Parameter</span></span>       | <span data-ttu-id="ab6be-190">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="ab6be-190">Default value</span></span> | <span data-ttu-id="ab6be-191">Тип</span><span class="sxs-lookup"><span data-stu-id="ab6be-191">Type</span></span>      | <span data-ttu-id="ab6be-192">Описание</span><span class="sxs-lookup"><span data-stu-id="ab6be-192">Description</span></span>                                                 |
|-----------------|---------------|-----------|-------------------------------------------------------------|
| <span data-ttu-id="ab6be-193">L<sub>dcs</sub></span><span class="sxs-lookup"><span data-stu-id="ab6be-193">L<sub>dcs</sub></span></span> | <span data-ttu-id="ab6be-194">Н/Д</span><span class="sxs-lookup"><span data-stu-id="ab6be-194">N/A</span></span>           | <span data-ttu-id="ab6be-195">D3DVECTOR</span><span class="sxs-lookup"><span data-stu-id="ab6be-195">D3DVECTOR</span></span> | <span data-ttu-id="ab6be-196">Отрицательное значение направления света в пространстве камеры</span><span class="sxs-lookup"><span data-stu-id="ab6be-196">The negative of the light direction in camera space</span></span>         |
| <span data-ttu-id="ab6be-197">L<sub>dir</sub></span><span class="sxs-lookup"><span data-stu-id="ab6be-197">L<sub>dir</sub></span></span> | <span data-ttu-id="ab6be-198">Н/Д</span><span class="sxs-lookup"><span data-stu-id="ab6be-198">N/A</span></span>           | <span data-ttu-id="ab6be-199">D3DVECTOR</span><span class="sxs-lookup"><span data-stu-id="ab6be-199">D3DVECTOR</span></span> | <span data-ttu-id="ab6be-200">Вектор направления от положения вершины до положения света</span><span class="sxs-lookup"><span data-stu-id="ab6be-200">Direction vector from vertex position to the light position</span></span> |



 

<span data-ttu-id="ab6be-201">После вычисления ослабления яркости Direct3D также рассматривает эффекты Spotlight, если применимо, угол, который отразится на поверхности, и отражение текущего материала для вычисления рассеянных и отражающих компонентов для этой вершины.</span><span class="sxs-lookup"><span data-stu-id="ab6be-201">After computing the light attenuation, Direct3D also considers spotlight effects if applicable, the angle that the light reflects from a surface, and the reflectance of the current material to calculate the diffuse and specular components for that vertex.</span></span> <span data-ttu-id="ab6be-202">Дополнительные сведения см. в разделе [Spotlight](light-types.md).</span><span class="sxs-lookup"><span data-stu-id="ab6be-202">For more information, see [SpotLight](light-types.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="ab6be-203">См. также</span><span class="sxs-lookup"><span data-stu-id="ab6be-203">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ab6be-204">Математика освещения</span><span class="sxs-lookup"><span data-stu-id="ab6be-204">Mathematics of Lighting</span></span>](mathematics-of-lighting.md)
</dt> </dl>

 

 



