---
description: После настройки интенсивности света для всех эффектов затухания модуль освещения вычисляет количество оставшегося света, отражаемое от вершины, с учетом угла нормали вершины и направления падающего света.
ms.assetid: 29280a02-1c26-4b54-8468-707dd96dea1d
title: Рассеянное освещение (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f51e45093786348aaa115ec38c420acec471f718
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104139235"
---
# <a name="diffuse-lighting-direct3d-9"></a><span data-ttu-id="d912c-103">Рассеянное освещение (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="d912c-103">Diffuse Lighting (Direct3D 9)</span></span>

<span data-ttu-id="d912c-104">После настройки интенсивности света для всех эффектов затухания модуль освещения вычисляет количество оставшегося света, отражаемое от вершины, с учетом угла нормали вершины и направления падающего света.</span><span class="sxs-lookup"><span data-stu-id="d912c-104">After adjusting the light intensity for any attenuation effects, the lighting engine computes how much of the remaining light reflects from a vertex, given the angle of the vertex normal and the direction of the incident light.</span></span> <span data-ttu-id="d912c-105">Модуль освещения переходит к этому этапу в случае с направленными источниками света, так как они не ослабевают с расстоянием.</span><span class="sxs-lookup"><span data-stu-id="d912c-105">The lighting engine skips to this step for directional lights because they do not attenuate over distance.</span></span> <span data-ttu-id="d912c-106">Система учитывает два типа отражения — рассеянное и зеркальное — и использует другую формулу для определения количества отраженного света в каждом случае.</span><span class="sxs-lookup"><span data-stu-id="d912c-106">The system considers two reflection types, diffuse and specular, and uses a different formula to determine how much light is reflected for each.</span></span> <span data-ttu-id="d912c-107">После вычисления количества отраженного света Direct3D применяет новые полученные значения к свойствам рассеянного и зеркального отражения текущего материала.</span><span class="sxs-lookup"><span data-stu-id="d912c-107">After calculating the amounts of light reflected, Direct3D applies these new values to the diffuse and specular reflectance properties of the current material.</span></span> <span data-ttu-id="d912c-108">Полученные значения цвета являются компонентами рассеянного и зеркального отражения, которые средство отрисовки использует для создания затенения по методу Гуро и световых бликов.</span><span class="sxs-lookup"><span data-stu-id="d912c-108">The resulting color values are the diffuse and specular components that the rasterizer uses to produce Gouraud shading and specular highlighting.</span></span>

<span data-ttu-id="d912c-109">Рассеянное освещение описывается следующим уравнением.</span><span class="sxs-lookup"><span data-stu-id="d912c-109">Diffuse lighting is described by the following equation.</span></span>

<span data-ttu-id="d912c-110">Рассеянное освещение = сумма \[ C<sub>d</sub> \* L<sub>d</sub> \* (N<sup>.</sup> L<sub>dir</sub>) \* аттен \*\]</span><span class="sxs-lookup"><span data-stu-id="d912c-110">Diffuse Lighting = sum\[C<sub>d</sub>\*L<sub>d</sub>\*(N<sup>.</sup>L<sub>dir</sub>)\*Atten\*Spot\]</span></span>



| <span data-ttu-id="d912c-111">Параметр</span><span class="sxs-lookup"><span data-stu-id="d912c-111">Parameter</span></span>       | <span data-ttu-id="d912c-112">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="d912c-112">Default value</span></span> | <span data-ttu-id="d912c-113">Тип</span><span class="sxs-lookup"><span data-stu-id="d912c-113">Type</span></span>          | <span data-ttu-id="d912c-114">Описание</span><span class="sxs-lookup"><span data-stu-id="d912c-114">Description</span></span>                                                                                                   |
|-----------------|---------------|---------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d912c-115">Sum</span><span class="sxs-lookup"><span data-stu-id="d912c-115">sum</span></span>             | <span data-ttu-id="d912c-116">Н/Д</span><span class="sxs-lookup"><span data-stu-id="d912c-116">N/A</span></span>           | <span data-ttu-id="d912c-117">Н/Д</span><span class="sxs-lookup"><span data-stu-id="d912c-117">N/A</span></span>           | <span data-ttu-id="d912c-118">Совокупность рассеянных компонентов каждого источника света.</span><span class="sxs-lookup"><span data-stu-id="d912c-118">Summation of each light's diffuse component.</span></span>                                                                  |
| <span data-ttu-id="d912c-119">C<sub>d</sub></span><span class="sxs-lookup"><span data-stu-id="d912c-119">C<sub>d</sub></span></span>   | <span data-ttu-id="d912c-120">(0,0,0,0)</span><span class="sxs-lookup"><span data-stu-id="d912c-120">(0,0,0,0)</span></span>     | <span data-ttu-id="d912c-121">D3DCOLORVALUE</span><span class="sxs-lookup"><span data-stu-id="d912c-121">D3DCOLORVALUE</span></span> | <span data-ttu-id="d912c-122">Рассеянный цвет.</span><span class="sxs-lookup"><span data-stu-id="d912c-122">Diffuse color.</span></span>                                                                                                |
| <span data-ttu-id="d912c-123">L<sub>d</sub></span><span class="sxs-lookup"><span data-stu-id="d912c-123">L<sub>d</sub></span></span>   | <span data-ttu-id="d912c-124">(0,0,0,0)</span><span class="sxs-lookup"><span data-stu-id="d912c-124">(0,0,0,0)</span></span>     | <span data-ttu-id="d912c-125">D3DCOLORVALUE</span><span class="sxs-lookup"><span data-stu-id="d912c-125">D3DCOLORVALUE</span></span> | <span data-ttu-id="d912c-126">Рассеянный цвет источника света.</span><span class="sxs-lookup"><span data-stu-id="d912c-126">Light diffuse color.</span></span>                                                                                          |
| <span data-ttu-id="d912c-127">Нет</span><span class="sxs-lookup"><span data-stu-id="d912c-127">N</span></span>               | <span data-ttu-id="d912c-128">Н/Д</span><span class="sxs-lookup"><span data-stu-id="d912c-128">N/A</span></span>           | <span data-ttu-id="d912c-129">D3DVECTOR</span><span class="sxs-lookup"><span data-stu-id="d912c-129">D3DVECTOR</span></span>     | <span data-ttu-id="d912c-130">Нормаль вершины</span><span class="sxs-lookup"><span data-stu-id="d912c-130">Vertex normal</span></span>                                                                                                 |
| <span data-ttu-id="d912c-131">L<sub>dir</sub></span><span class="sxs-lookup"><span data-stu-id="d912c-131">L<sub>dir</sub></span></span> | <span data-ttu-id="d912c-132">Н/Д</span><span class="sxs-lookup"><span data-stu-id="d912c-132">N/A</span></span>           | <span data-ttu-id="d912c-133">D3DVECTOR</span><span class="sxs-lookup"><span data-stu-id="d912c-133">D3DVECTOR</span></span>     | <span data-ttu-id="d912c-134">Вектор направления от вершины объекта к источнику света.</span><span class="sxs-lookup"><span data-stu-id="d912c-134">Direction vector from object vertex to the light.</span></span>                                                             |
| <span data-ttu-id="d912c-135">Atten</span><span class="sxs-lookup"><span data-stu-id="d912c-135">Atten</span></span>           | <span data-ttu-id="d912c-136">Н/Д</span><span class="sxs-lookup"><span data-stu-id="d912c-136">N/A</span></span>           | <span data-ttu-id="d912c-137">FLOAT</span><span class="sxs-lookup"><span data-stu-id="d912c-137">FLOAT</span></span>         | <span data-ttu-id="d912c-138">Затухание света.</span><span class="sxs-lookup"><span data-stu-id="d912c-138">Light attenuation.</span></span> <span data-ttu-id="d912c-139">См. раздел " [ослабление и прожектор" (Direct3D 9)](attenuation-and-spotlight-factor.md).</span><span class="sxs-lookup"><span data-stu-id="d912c-139">See [Attenuation and Spotlight Factor (Direct3D 9)](attenuation-and-spotlight-factor.md).</span></span> |
| <span data-ttu-id="d912c-140">Немедленная оплата.</span><span class="sxs-lookup"><span data-stu-id="d912c-140">Spot</span></span>            | <span data-ttu-id="d912c-141">Н/Д</span><span class="sxs-lookup"><span data-stu-id="d912c-141">N/A</span></span>           | <span data-ttu-id="d912c-142">FLOAT</span><span class="sxs-lookup"><span data-stu-id="d912c-142">FLOAT</span></span>         | <span data-ttu-id="d912c-143">Коэффициент узкой направленности света.</span><span class="sxs-lookup"><span data-stu-id="d912c-143">Spotlight factor.</span></span> <span data-ttu-id="d912c-144">См. раздел " [ослабление и прожектор" (Direct3D 9)](attenuation-and-spotlight-factor.md).</span><span class="sxs-lookup"><span data-stu-id="d912c-144">See [Attenuation and Spotlight Factor (Direct3D 9)](attenuation-and-spotlight-factor.md).</span></span>  |



 

<span data-ttu-id="d912c-145">Значение для C<sub>d</sub> может быть следующим:</span><span class="sxs-lookup"><span data-stu-id="d912c-145">The value for C<sub>d</sub> is either:</span></span>

-   <span data-ttu-id="d912c-146">Вершинный color1, если ДИФФУСЕМАТЕРИАЛСАУРЦЕ = D3DMCS \_ color1, а первый цвет вершин указан в объявлении вершины.</span><span class="sxs-lookup"><span data-stu-id="d912c-146">vertex color1, if DIFFUSEMATERIALSOURCE = D3DMCS\_COLOR1, and the first vertex color is supplied in the vertex declaration.</span></span>
-   <span data-ttu-id="d912c-147">Вершинный color2, если ДИФФУСЕМАТЕРИАЛСАУРЦЕ = D3DMCS \_ color2, а второй цвет вершин указан в объявлении вершины.</span><span class="sxs-lookup"><span data-stu-id="d912c-147">vertex color2, if DIFFUSEMATERIALSOURCE = D3DMCS\_COLOR2, and the second vertex color is supplied in the vertex declaration.</span></span>
-   <span data-ttu-id="d912c-148">цвет рассеянного материала</span><span class="sxs-lookup"><span data-stu-id="d912c-148">material diffuse color</span></span>

> [!Note]  
> <span data-ttu-id="d912c-149">Если используется параметр ДИФФУСЕМАТЕРИАЛСАУРЦЕ и не указан цвет вершины, используется рассеянный цвет материала.</span><span class="sxs-lookup"><span data-stu-id="d912c-149">If either DIFFUSEMATERIALSOURCE option is used, and the vertex color is not provided, the material diffuse color is used.</span></span>

 

<span data-ttu-id="d912c-150">Сведения о вычислении затухания (Аттен) или характеристиках прожектора (точки) см. в разделе " [ослабление" и "прожектор" (Direct3D 9)](attenuation-and-spotlight-factor.md).</span><span class="sxs-lookup"><span data-stu-id="d912c-150">To calculate the attenuation (Atten) or the spotlight characteristics (Spot), see [Attenuation and Spotlight Factor (Direct3D 9)](attenuation-and-spotlight-factor.md).</span></span>

<span data-ttu-id="d912c-151">Рассеянные компоненты прикрепляются к диапазону от 0 до 255, после того как все источники освещения отдельно обработаны и интерполированы.</span><span class="sxs-lookup"><span data-stu-id="d912c-151">Diffuse components are clamped to be from 0 to 255, after all lights are processed and interpolated separately.</span></span> <span data-ttu-id="d912c-152">Полученное значение рассеянного света представляет собой сочетание значений внешнего, рассеянного и излучаемого освещения.</span><span class="sxs-lookup"><span data-stu-id="d912c-152">The resulting diffuse lighting value is a combination of the ambient, diffuse and emissive light values.</span></span>

## <a name="example"></a><span data-ttu-id="d912c-153">Пример</span><span class="sxs-lookup"><span data-stu-id="d912c-153">Example</span></span>

<span data-ttu-id="d912c-154">В этом примере цвет объекта определяется рассеянным цветом источника света и рассеянным цветом материала.</span><span class="sxs-lookup"><span data-stu-id="d912c-154">In this example, the object is colored using the light diffuse color and a material diffuse color.</span></span> <span data-ttu-id="d912c-155">Код показан ниже.</span><span class="sxs-lookup"><span data-stu-id="d912c-155">The code is shown below.</span></span>


```
D3DMATERIAL9 mtrl;
ZeroMemory( &mtrl, sizeof(mtrl) );

D3DLIGHT9 light;
ZeroMemory( &light, sizeof(light) );
light.Type = D3DLIGHT_DIRECTIONAL;

D3DXVECTOR3 vecDir;
vecDir = D3DXVECTOR3(0.5f, 0.0f, -0.5f);
D3DXVec3Normalize( (D3DXVECTOR3*)&light.Direction, &vecDir );

// set directional light diffuse color
light.Diffuse.r = 1.0f;
light.Diffuse.g = 1.0f;
light.Diffuse.b = 1.0f;
light.Diffuse.a = 1.0f;
m_pd3dDevice->SetLight( 0, &light );
m_pd3dDevice->LightEnable( 0, TRUE );

// if a material is used, SetRenderState must be used
// vertex color = light diffuse color * material diffuse color
mtrl.Diffuse.r = 0.75f;
mtrl.Diffuse.g = 0.0f;
mtrl.Diffuse.b = 0.0f;
mtrl.Diffuse.a = 0.0f;
m_pd3dDevice->SetMaterial( &mtrl );
m_pd3dDevice->SetRenderState(D3DRS_DIFFUSEMATERIALSOURCE, D3DMCS_MATERIAL);
```



<span data-ttu-id="d912c-156">Согласно уравнению, получившийся цвет для вершин объекта — это сочетание цвета материала и цвета света.</span><span class="sxs-lookup"><span data-stu-id="d912c-156">According to the equation, the resulting color for the object vertices is a combination of the material color and the light color.</span></span>

<span data-ttu-id="d912c-157">На двух следующих рисунках показан цвет материала (серый) и цвет света (ярко-красный).</span><span class="sxs-lookup"><span data-stu-id="d912c-157">The following two illustrations show the material color, which is gray, and the light color, which is bright red.</span></span>

![иллюстрация серой сферы](images/amb1.jpg)![иллюстрация красной сферы](images/lightred.jpg)

<span data-ttu-id="d912c-160">Получившаяся сцена показана на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="d912c-160">The resulting scene is shown in the following illustration.</span></span> <span data-ttu-id="d912c-161">Единственный объект в сцене — сфера.</span><span class="sxs-lookup"><span data-stu-id="d912c-161">The only object in the scene is a sphere.</span></span> <span data-ttu-id="d912c-162">Для расчета рассеянного света рассеянный цвет материала и источника света изменяется с учетом угла между направлением света и нормалью вершины при помощи скалярного произведения.</span><span class="sxs-lookup"><span data-stu-id="d912c-162">The diffuse lighting calculation takes the material and light diffuse color and modifies it by the angle between the light direction and the vertex normal using the dot product.</span></span> <span data-ttu-id="d912c-163">В результате, тыльная сторона сфера темнеет по мере ухода изгиба сферы от источника света.</span><span class="sxs-lookup"><span data-stu-id="d912c-163">As a result, the backside of the sphere gets darker as the surface of the sphere curves away from the light.</span></span>

![иллюстрация сферы с рассеянным освещением](images/lightd.jpg)

<span data-ttu-id="d912c-165">При совмещении рассеянного и внешнего освещения в предыдущем примере обеспечивает затенение всей поверхности объекта.</span><span class="sxs-lookup"><span data-stu-id="d912c-165">Combining the diffuse lighting with the ambient lighting from the previous example shades the entire surface of the object.</span></span> <span data-ttu-id="d912c-166">Внешнее освещение затеняет всю поверхность, а рассеянное освещение помогает раскрыть трехмерную форму объекта, как показано на следующей иллюстрации.</span><span class="sxs-lookup"><span data-stu-id="d912c-166">The ambient light shades the entire surface and the diffuse light helps reveal the object's 3D shape, as shown in the following illustration.</span></span>

![иллюстрация сферы с рассеянным и внешним освещением](images/lightad.jpg)

<span data-ttu-id="d912c-168">Рассеянное освещение сложнее в расчете, чем внешнее.</span><span class="sxs-lookup"><span data-stu-id="d912c-168">Diffuse lighting is more intensive to calculate than ambient lighting.</span></span> <span data-ttu-id="d912c-169">Поскольку оно зависит от нормалей вершин и направления света, раскрывается геометрия объекта в трехмерном пространстве, поэтому освещение становится более реалистичным, чем при использовании внешнего освещения.</span><span class="sxs-lookup"><span data-stu-id="d912c-169">Because it depends on the vertex normals and light direction, you can see the objects geometry in 3D space, which produces a more realistic lighting than ambient lighting.</span></span> <span data-ttu-id="d912c-170">Вы можете использовать световые блики для получения более реалистичного вида.</span><span class="sxs-lookup"><span data-stu-id="d912c-170">You can use specular highlights to achieve a more realistic look.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d912c-171">См. также</span><span class="sxs-lookup"><span data-stu-id="d912c-171">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d912c-172">Математика освещения</span><span class="sxs-lookup"><span data-stu-id="d912c-172">Mathematics of Lighting</span></span>](mathematics-of-lighting.md)
</dt> </dl>

 

 



