---
description: Зеркальное отражение моделирования требует, чтобы система не только знала, в каком направлении находится в дороге, а также направлена на глаз средства просмотра.
ms.assetid: 35da0ac3-4e68-4d37-a987-405fc15d0cbf
title: Отраженное освещение (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ab378d4ca3f00ef81c5048e6ad6cc85eaeb18ad
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104567988"
---
# <a name="specular-lighting-direct3d-9"></a><span data-ttu-id="4c7b1-103">Отраженное освещение (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="4c7b1-103">Specular Lighting (Direct3D 9)</span></span>

<span data-ttu-id="4c7b1-104">Зеркальное отражение моделирования требует, чтобы система не только знала, в каком направлении находится в дороге, а также направлена на глаз средства просмотра.</span><span class="sxs-lookup"><span data-stu-id="4c7b1-104">Modeling specular reflection requires that the system not only know in what direction light is traveling, but also the direction to the viewer's eye.</span></span> <span data-ttu-id="4c7b1-105">Система использует упрощенную версию модели отражения света Фонга, в которой применяется вектор полупути для аппроксимации интенсивности отраженного света.</span><span class="sxs-lookup"><span data-stu-id="4c7b1-105">The system uses a simplified version of the Phong specular-reflection model, which employs a halfway vector to approximate the intensity of specular reflection.</span></span>

<span data-ttu-id="4c7b1-106">В состоянии освещения по умолчанию блики отражения не рассчитываются.</span><span class="sxs-lookup"><span data-stu-id="4c7b1-106">The default lighting state does not calculate specular highlights.</span></span> <span data-ttu-id="4c7b1-107">Чтобы включить зеркальное освещение, обязательно установите для параметра D3DRS \_ спекуларенабле значение **true**.</span><span class="sxs-lookup"><span data-stu-id="4c7b1-107">To enable specular lighting, be sure to set D3DRS\_SPECULARENABLE to **TRUE**.</span></span>

## <a name="specular-lighting-equation"></a><span data-ttu-id="4c7b1-108">Уравнение отраженного света</span><span class="sxs-lookup"><span data-stu-id="4c7b1-108">Specular Lighting Equation</span></span>

<span data-ttu-id="4c7b1-109">Отраженный свет описывается следующим уравнением.</span><span class="sxs-lookup"><span data-stu-id="4c7b1-109">Specular Lighting is described by the following equation.</span></span>



|                                                                             |
|-----------------------------------------------------------------------------|
| <span data-ttu-id="4c7b1-110">Зеркальное освещение = CS \* Sum \[ Ls \* (N · З)<sup></sup> \* Аттен в \* точке P\]</span><span class="sxs-lookup"><span data-stu-id="4c7b1-110">Specular Lighting = Cₛ \* sum\[Lₛ \* (N · H)<sup>P</sup> \* Atten \* Spot\]</span></span> |



 

<span data-ttu-id="4c7b1-111">В следующей таблице указаны переменные, их типы и диапазоны.</span><span class="sxs-lookup"><span data-stu-id="4c7b1-111">The following table identifies the variables, their types, and their ranges.</span></span>



| <span data-ttu-id="4c7b1-112">Параметр</span><span class="sxs-lookup"><span data-stu-id="4c7b1-112">Parameter</span></span>    | <span data-ttu-id="4c7b1-113">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="4c7b1-113">Default value</span></span> | <span data-ttu-id="4c7b1-114">Тип</span><span class="sxs-lookup"><span data-stu-id="4c7b1-114">Type</span></span>          | <span data-ttu-id="4c7b1-115">Описание</span><span class="sxs-lookup"><span data-stu-id="4c7b1-115">Description</span></span>                                                                                                         |
|--------------|---------------|---------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c7b1-116">Cₛ</span><span class="sxs-lookup"><span data-stu-id="4c7b1-116">Cₛ</span></span>           | <span data-ttu-id="4c7b1-117">(0,0,0,0)</span><span class="sxs-lookup"><span data-stu-id="4c7b1-117">(0,0,0,0)</span></span>     | <span data-ttu-id="4c7b1-118">D3DCOLORVALUE</span><span class="sxs-lookup"><span data-stu-id="4c7b1-118">D3DCOLORVALUE</span></span> | <span data-ttu-id="4c7b1-119">Отраженный цвет.</span><span class="sxs-lookup"><span data-stu-id="4c7b1-119">Specular color.</span></span>                                                                                                     |
| <span data-ttu-id="4c7b1-120">Sum</span><span class="sxs-lookup"><span data-stu-id="4c7b1-120">sum</span></span>          | <span data-ttu-id="4c7b1-121">Н/Д</span><span class="sxs-lookup"><span data-stu-id="4c7b1-121">N/A</span></span>           | <span data-ttu-id="4c7b1-122">Н/Д</span><span class="sxs-lookup"><span data-stu-id="4c7b1-122">N/A</span></span>           | <span data-ttu-id="4c7b1-123">Суммирование каждого компонента отраженного света.</span><span class="sxs-lookup"><span data-stu-id="4c7b1-123">Summation of each light's specular component.</span></span>                                                                       |
| <span data-ttu-id="4c7b1-124">Нет</span><span class="sxs-lookup"><span data-stu-id="4c7b1-124">N</span></span>            | <span data-ttu-id="4c7b1-125">Н/Д</span><span class="sxs-lookup"><span data-stu-id="4c7b1-125">N/A</span></span>           | <span data-ttu-id="4c7b1-126">D3DVECTOR</span><span class="sxs-lookup"><span data-stu-id="4c7b1-126">D3DVECTOR</span></span>     | <span data-ttu-id="4c7b1-127">Нормальная вершина.</span><span class="sxs-lookup"><span data-stu-id="4c7b1-127">Vertex normal.</span></span>                                                                                                      |
| <span data-ttu-id="4c7b1-128">H</span><span class="sxs-lookup"><span data-stu-id="4c7b1-128">H</span></span>            | <span data-ttu-id="4c7b1-129">Н/Д</span><span class="sxs-lookup"><span data-stu-id="4c7b1-129">N/A</span></span>           | <span data-ttu-id="4c7b1-130">D3DVECTOR</span><span class="sxs-lookup"><span data-stu-id="4c7b1-130">D3DVECTOR</span></span>     | <span data-ttu-id="4c7b1-131">Вектор полупути.</span><span class="sxs-lookup"><span data-stu-id="4c7b1-131">Half way vector.</span></span> <span data-ttu-id="4c7b1-132">См. раздел по вектору полупути.</span><span class="sxs-lookup"><span data-stu-id="4c7b1-132">See the section on the halfway vector.</span></span>                                                             |
| <span data-ttu-id="4c7b1-133"><sup>P</sup></span><span class="sxs-lookup"><span data-stu-id="4c7b1-133"><sup>P</sup></span></span> | <span data-ttu-id="4c7b1-134">0,0</span><span class="sxs-lookup"><span data-stu-id="4c7b1-134">0.0</span></span>           | <span data-ttu-id="4c7b1-135">FLOAT</span><span class="sxs-lookup"><span data-stu-id="4c7b1-135">FLOAT</span></span>         | <span data-ttu-id="4c7b1-136">Сила отраженного света</span><span class="sxs-lookup"><span data-stu-id="4c7b1-136">Specular reflection power.</span></span> <span data-ttu-id="4c7b1-137">Диапазон от 0 до +бесконечность</span><span class="sxs-lookup"><span data-stu-id="4c7b1-137">Range is 0 to +infinity</span></span>                                                                  |
| <span data-ttu-id="4c7b1-138">Lₛ</span><span class="sxs-lookup"><span data-stu-id="4c7b1-138">Lₛ</span></span>           | <span data-ttu-id="4c7b1-139">(0,0,0,0)</span><span class="sxs-lookup"><span data-stu-id="4c7b1-139">(0,0,0,0)</span></span>     | <span data-ttu-id="4c7b1-140">D3DCOLORVALUE</span><span class="sxs-lookup"><span data-stu-id="4c7b1-140">D3DCOLORVALUE</span></span> | <span data-ttu-id="4c7b1-141">Цвет отраженного света.</span><span class="sxs-lookup"><span data-stu-id="4c7b1-141">Light specular color.</span></span>                                                                                               |
| <span data-ttu-id="4c7b1-142">Atten</span><span class="sxs-lookup"><span data-stu-id="4c7b1-142">Atten</span></span>        | <span data-ttu-id="4c7b1-143">Н/Д</span><span class="sxs-lookup"><span data-stu-id="4c7b1-143">N/A</span></span>           | <span data-ttu-id="4c7b1-144">FLOAT</span><span class="sxs-lookup"><span data-stu-id="4c7b1-144">FLOAT</span></span>         | <span data-ttu-id="4c7b1-145">Значение ослабления света.</span><span class="sxs-lookup"><span data-stu-id="4c7b1-145">Light attenuation value.</span></span> <span data-ttu-id="4c7b1-146">См. раздел " [ослабление и прожектор" (Direct3D 9)](attenuation-and-spotlight-factor.md).</span><span class="sxs-lookup"><span data-stu-id="4c7b1-146">See [Attenuation and Spotlight Factor (Direct3D 9)](attenuation-and-spotlight-factor.md).</span></span> |
| <span data-ttu-id="4c7b1-147">Немедленная оплата.</span><span class="sxs-lookup"><span data-stu-id="4c7b1-147">Spot</span></span>         | <span data-ttu-id="4c7b1-148">Н/Д</span><span class="sxs-lookup"><span data-stu-id="4c7b1-148">N/A</span></span>           | <span data-ttu-id="4c7b1-149">FLOAT</span><span class="sxs-lookup"><span data-stu-id="4c7b1-149">FLOAT</span></span>         | <span data-ttu-id="4c7b1-150">Коэффициент узкой направленности света.</span><span class="sxs-lookup"><span data-stu-id="4c7b1-150">Spotlight factor.</span></span> <span data-ttu-id="4c7b1-151">См. раздел " [ослабление и прожектор" (Direct3D 9)](attenuation-and-spotlight-factor.md).</span><span class="sxs-lookup"><span data-stu-id="4c7b1-151">See [Attenuation and Spotlight Factor (Direct3D 9)](attenuation-and-spotlight-factor.md).</span></span>        |



 

<span data-ttu-id="4c7b1-152">Значение для Cₛ — либо:</span><span class="sxs-lookup"><span data-stu-id="4c7b1-152">The value for Cₛ is either:</span></span>


```
if(SPECULARMATERIALSOURCE == D3DMCS_COLOR1)
  C = color1;
```



-   <span data-ttu-id="4c7b1-153">Вершинный color1, если источником отраженных материалов является D3DMCS \_ color1, а первый цвет вершин указан в объявлении вершины.</span><span class="sxs-lookup"><span data-stu-id="4c7b1-153">vertex color1, if the specular material source is D3DMCS\_COLOR1, and the first vertex color is supplied in the vertex declaration.</span></span>
-   <span data-ttu-id="4c7b1-154">Вершинный color2, если источником отраженных материалов является D3DMCS \_ color2, а второй цвет вершин указан в объявлении вершины.</span><span class="sxs-lookup"><span data-stu-id="4c7b1-154">vertex color2, if specular material source is D3DMCS\_COLOR2, and the second vertex color is supplied in the vertex declaration.</span></span>
-   <span data-ttu-id="4c7b1-155">цвет отражения материала</span><span class="sxs-lookup"><span data-stu-id="4c7b1-155">material specular color</span></span>

> [!Note]  
> <span data-ttu-id="4c7b1-156">Если используется параметр источника отраженных материалов и не указан цвет вершины, используется отражающий цвет материала.</span><span class="sxs-lookup"><span data-stu-id="4c7b1-156">If either specular material source option is used and the vertex color is not provided, then the material specular color is used.</span></span>

 

<span data-ttu-id="4c7b1-157">Компоненты отражения ужимаются до диапазона 0-255, после отдельной обработки и интерполяции всех источников света.</span><span class="sxs-lookup"><span data-stu-id="4c7b1-157">Specular components are clamped to be from 0 to 255, after all lights are processed and interpolated separately.</span></span>

## <a name="the-halfway-vector"></a><span data-ttu-id="4c7b1-158">Вектор полупути</span><span class="sxs-lookup"><span data-stu-id="4c7b1-158">The Halfway Vector</span></span>

<span data-ttu-id="4c7b1-159">Вектор полупути (H) существует посередине между двумя векторами: вектором из вершины объекта к источнику света и вектором из вершины объекта к положению камеры.</span><span class="sxs-lookup"><span data-stu-id="4c7b1-159">The halfway vector (H) exists midway between two vectors: the vector from an object vertex to the light source, and the vector from an object vertex to the camera position.</span></span> <span data-ttu-id="4c7b1-160">Direct3D предоставляет два способа расчета вектора полупути.</span><span class="sxs-lookup"><span data-stu-id="4c7b1-160">Direct3D provides two ways to compute the halfway vector.</span></span> <span data-ttu-id="4c7b1-161">Если \_ для параметра D3DRS локалвиевер задано **значение true**, система вычисляет посередине вектора с использованием расположения камеры и расположения вершины вместе с вектором направления освещения.</span><span class="sxs-lookup"><span data-stu-id="4c7b1-161">When D3DRS\_LOCALVIEWER is set to **TRUE**, the system calculates the halfway vector using the position of the camera and the position of the vertex, along with the light's direction vector.</span></span> <span data-ttu-id="4c7b1-162">Это демонстрируется в следующей формуле:</span><span class="sxs-lookup"><span data-stu-id="4c7b1-162">The following formula illustrates this.</span></span>



|                                           |
|-------------------------------------------|
| <span data-ttu-id="4c7b1-163">H = norm(norm(Cₚ - Vₚ) + L<sub>dir</sub>)</span><span class="sxs-lookup"><span data-stu-id="4c7b1-163">H = norm(norm(Cₚ - Vₚ) + L<sub>dir</sub>)</span></span> |



 



| <span data-ttu-id="4c7b1-164">Параметр</span><span class="sxs-lookup"><span data-stu-id="4c7b1-164">Parameter</span></span>       | <span data-ttu-id="4c7b1-165">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="4c7b1-165">Default value</span></span> | <span data-ttu-id="4c7b1-166">Тип</span><span class="sxs-lookup"><span data-stu-id="4c7b1-166">Type</span></span>      | <span data-ttu-id="4c7b1-167">Описание</span><span class="sxs-lookup"><span data-stu-id="4c7b1-167">Description</span></span>                                                  |
|-----------------|---------------|-----------|--------------------------------------------------------------|
| <span data-ttu-id="4c7b1-168">Cₚ</span><span class="sxs-lookup"><span data-stu-id="4c7b1-168">Cₚ</span></span>              | <span data-ttu-id="4c7b1-169">Н/Д</span><span class="sxs-lookup"><span data-stu-id="4c7b1-169">N/A</span></span>           | <span data-ttu-id="4c7b1-170">D3DVECTOR</span><span class="sxs-lookup"><span data-stu-id="4c7b1-170">D3DVECTOR</span></span> | <span data-ttu-id="4c7b1-171">Позиция камеры.</span><span class="sxs-lookup"><span data-stu-id="4c7b1-171">Camera position.</span></span>                                             |
| <span data-ttu-id="4c7b1-172">Vₚ</span><span class="sxs-lookup"><span data-stu-id="4c7b1-172">Vₚ</span></span>              | <span data-ttu-id="4c7b1-173">Н/Д</span><span class="sxs-lookup"><span data-stu-id="4c7b1-173">N/A</span></span>           | <span data-ttu-id="4c7b1-174">D3DVECTOR</span><span class="sxs-lookup"><span data-stu-id="4c7b1-174">D3DVECTOR</span></span> | <span data-ttu-id="4c7b1-175">Положение вершины.</span><span class="sxs-lookup"><span data-stu-id="4c7b1-175">Vertex position.</span></span>                                             |
| <span data-ttu-id="4c7b1-176">L<sub>dir</sub></span><span class="sxs-lookup"><span data-stu-id="4c7b1-176">L<sub>dir</sub></span></span> | <span data-ttu-id="4c7b1-177">Н/Д</span><span class="sxs-lookup"><span data-stu-id="4c7b1-177">N/A</span></span>           | <span data-ttu-id="4c7b1-178">D3DVECTOR</span><span class="sxs-lookup"><span data-stu-id="4c7b1-178">D3DVECTOR</span></span> | <span data-ttu-id="4c7b1-179">Вектор направления из положения вершины к позиции источника освещения.</span><span class="sxs-lookup"><span data-stu-id="4c7b1-179">Direction vector from vertex position to the light position.</span></span> |



 

<span data-ttu-id="4c7b1-180">Нахождение вектора полупути таким образом может быть затратно в плане вычислений.</span><span class="sxs-lookup"><span data-stu-id="4c7b1-180">Determining the halfway vector in this manner can be computationally intensive.</span></span> <span data-ttu-id="4c7b1-181">В качестве альтернативы параметр D3DRS \_ локалвиевер = **false** предписывает системе действовать так, будто точка зрения не бесконечно удалена по оси z.</span><span class="sxs-lookup"><span data-stu-id="4c7b1-181">As an alternative, setting D3DRS\_LOCALVIEWER = **FALSE** instructs the system to act as though the viewpoint is infinitely distant on the z-axis.</span></span> <span data-ttu-id="4c7b1-182">Это отражено в следующей формуле.</span><span class="sxs-lookup"><span data-stu-id="4c7b1-182">This is reflected in the following formula.</span></span>



|                                     |
|-------------------------------------|
| <span data-ttu-id="4c7b1-183">H = norm((0,0,1) + L<sub>dir</sub>)</span><span class="sxs-lookup"><span data-stu-id="4c7b1-183">H = norm((0,0,1) + L<sub>dir</sub>)</span></span> |



 

<span data-ttu-id="4c7b1-184">Этот вариант требует меньше вычислений, но он гораздо менее точен, поэтому лучше всего применять его в приложениях с ортогональной проекцией.</span><span class="sxs-lookup"><span data-stu-id="4c7b1-184">This setting is less computationally intensive, but much less accurate, so it is best used by applications that use orthogonal projection.</span></span>

## <a name="example"></a><span data-ttu-id="4c7b1-185">Пример</span><span class="sxs-lookup"><span data-stu-id="4c7b1-185">Example</span></span>

<span data-ttu-id="4c7b1-186">В этом примере объект расцвечивается с помощью цвет отраженного света сцены и цвета отражения материала.</span><span class="sxs-lookup"><span data-stu-id="4c7b1-186">In this example, the object is colored using the scene specular light color and a material specular color.</span></span> <span data-ttu-id="4c7b1-187">Код показан ниже.</span><span class="sxs-lookup"><span data-stu-id="4c7b1-187">The code is shown below.</span></span>


```
D3DMATERIAL9 mtrl;
ZeroMemory( &mtrl, sizeof(mtrl) );

D3DLIGHT9 light;
ZeroMemory( &light, sizeof(light) );
light.Type = D3DLIGHT_DIRECTIONAL;

D3DXVECTOR3 vecDir;
vecDir = D3DXVECTOR3(0.5f, 0.0f, -0.5f);
D3DXVec3Normalize( (D3DXVECTOR3*)&light.Direction, &vecDir );

light.Specular.r = 1.0f;
light.Specular.g = 1.0f;
light.Specular.b = 1.0f;
light.Specular.a = 1.0f;

light.Range = 1000;
light.Falloff = 0;
light.Attenuation0 = 1;
light.Attenuation1 = 0;
light.Attenuation2 = 0;
m_pd3dDevice->SetLight( 0, &light );
m_pd3dDevice->LightEnable( 0, TRUE );
m_pd3dDevice->SetRenderState( D3DRS_SPECULARENABLE, TRUE );

mtrl.Specular.r = 0.5f;
mtrl.Specular.g = 0.5f;
mtrl.Specular.b = 0.5f;
mtrl.Specular.a = 0.5f;
mtrl.Power = 20;
m_pd3dDevice->SetMaterial( &mtrl );
m_pd3dDevice->SetRenderState(D3DRS_SPECULARMATERIALSOURCE, D3DMCS_MATERIAL);
```



<span data-ttu-id="4c7b1-188">Согласно уравнению, получившийся цвет для вершин объекта — это сочетание цвета материала и цвета света.</span><span class="sxs-lookup"><span data-stu-id="4c7b1-188">According to the equation, the resulting color for the object vertices is a combination of the material color and the light color.</span></span>

<span data-ttu-id="4c7b1-189">На следующих двух иллюстрациях показан цвет отражения материала, серый, и цвет отраженного света, белый.</span><span class="sxs-lookup"><span data-stu-id="4c7b1-189">The following two illustration show the specular material color, which is gray, and the specular light color, which is white.</span></span>

![иллюстрация серой сферы](images/amb1.jpg)![Иллюстрация белой сферы](images/lightwhite.jpg)

<span data-ttu-id="4c7b1-192">Итоговый блик показан на следующей иллюстрации.</span><span class="sxs-lookup"><span data-stu-id="4c7b1-192">The resulting specular highlight is shown in the following illustration.</span></span>

![Иллюстрация блика](images/lights.jpg)

<span data-ttu-id="4c7b1-194">Объединение блика с рассеянным и общим светом дает следующий результат.</span><span class="sxs-lookup"><span data-stu-id="4c7b1-194">Combining the specular highlight with the ambient and diffuse lighting produces the following illustration.</span></span> <span data-ttu-id="4c7b1-195">Применение всех трех типов освещения дает более реалистичное изображение объекта.</span><span class="sxs-lookup"><span data-stu-id="4c7b1-195">With all three types of lighting applied, this more clearly resembles a realistic object.</span></span>

![Иллюстрация сочетания бликов, общего и рассеянного света](images/lightads.jpg)

<span data-ttu-id="4c7b1-197">Отраженный свет требуют больше вычислительных ресурсов, чем рассеянный свет.</span><span class="sxs-lookup"><span data-stu-id="4c7b1-197">Specular lighting is more intensive to calculate than diffuse lighting.</span></span> <span data-ttu-id="4c7b1-198">Обычно он применяется для предоставления визуальных подсказок о материале поверхности.</span><span class="sxs-lookup"><span data-stu-id="4c7b1-198">It is typically used to provide visual clues about the surface material.</span></span> <span data-ttu-id="4c7b1-199">Блики варьируются по размеру и цвету для разных материалов поверхности.</span><span class="sxs-lookup"><span data-stu-id="4c7b1-199">The specular highlight varies in size and color with the material of the surface.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4c7b1-200">См. также</span><span class="sxs-lookup"><span data-stu-id="4c7b1-200">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4c7b1-201">Математика освещения</span><span class="sxs-lookup"><span data-stu-id="4c7b1-201">Mathematics of Lighting</span></span>](mathematics-of-lighting.md)
</dt> </dl>

 

 



