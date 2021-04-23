---
description: Внешнее освещение предоставляет постоянное освещение для сцены.
ms.assetid: 327095a7-f4e0-48c2-9e4d-bec8493fe37e
title: Окружающее освещение (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e991981a9c1d7d24714e7014d08cefeaa94fe20f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539032"
---
# <a name="ambient-lighting-direct3d-9"></a><span data-ttu-id="5c1f5-103">Окружающее освещение (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="5c1f5-103">Ambient Lighting (Direct3D 9)</span></span>

<span data-ttu-id="5c1f5-104">Внешнее освещение предоставляет постоянное освещение для сцены.</span><span class="sxs-lookup"><span data-stu-id="5c1f5-104">Ambient lighting provides constant lighting for a scene.</span></span> <span data-ttu-id="5c1f5-105">Оно освещает все вершины объекта одинаково, потому что не зависит ни от каких других факторов освещения, таких как нормали вершины, направление света, положение света, диапазон или затухание.</span><span class="sxs-lookup"><span data-stu-id="5c1f5-105">It lights all object vertices the same because it is not dependent on any other lighting factors such as vertex normals, light direction, light position, range, or attenuation.</span></span> <span data-ttu-id="5c1f5-106">Это самый быстрый тип освещения, но он выдает наиболее реалистичные результаты.</span><span class="sxs-lookup"><span data-stu-id="5c1f5-106">It is the fastest type of lighting but it produces the least realistic results.</span></span> <span data-ttu-id="5c1f5-107">Direct3D содержит одно глобальное свойство внешнего освещения, которое можно использовать, не создавая никакого света.</span><span class="sxs-lookup"><span data-stu-id="5c1f5-107">Direct3D contains a single global ambient light property that you can use without creating any light.</span></span> <span data-ttu-id="5c1f5-108">Кроме того, можно настроить любой объект освещения так, чтобы он обеспечивал внешнее освещение.</span><span class="sxs-lookup"><span data-stu-id="5c1f5-108">Alternatively, you can set any light object to provide ambient lighting.</span></span> <span data-ttu-id="5c1f5-109">Внешнее освещение для сцены описывается в следующем уравнении.</span><span class="sxs-lookup"><span data-stu-id="5c1f5-109">The ambient lighting for a scene is described by the following equation.</span></span>

<span data-ttu-id="5c1f5-110">Окружающее освещение = C ₐ \* \[ g ₐ + Sum (аттен<sub>я разберу</sub> \* <sub>i</sub> \* L<sub>AI</sub>)\]</span><span class="sxs-lookup"><span data-stu-id="5c1f5-110">Ambient Lighting = Cₐ\*\[Gₐ + sum(Atten<sub>i</sub>\*Spot<sub>i</sub>\*L<sub>ai</sub>)\]</span></span>

<span data-ttu-id="5c1f5-111">Где:</span><span class="sxs-lookup"><span data-stu-id="5c1f5-111">Where:</span></span>



| <span data-ttu-id="5c1f5-112">Параметр</span><span class="sxs-lookup"><span data-stu-id="5c1f5-112">Parameter</span></span>         | <span data-ttu-id="5c1f5-113">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="5c1f5-113">Default value</span></span> | <span data-ttu-id="5c1f5-114">Тип</span><span class="sxs-lookup"><span data-stu-id="5c1f5-114">Type</span></span>          | <span data-ttu-id="5c1f5-115">Описание</span><span class="sxs-lookup"><span data-stu-id="5c1f5-115">Description</span></span>                                                                                                                    |
|-------------------|---------------|---------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c1f5-116">Cₐ</span><span class="sxs-lookup"><span data-stu-id="5c1f5-116">Cₐ</span></span>                | <span data-ttu-id="5c1f5-117">(0,0,0,0)</span><span class="sxs-lookup"><span data-stu-id="5c1f5-117">(0,0,0,0)</span></span>     | <span data-ttu-id="5c1f5-118">D3DCOLORVALUE</span><span class="sxs-lookup"><span data-stu-id="5c1f5-118">D3DCOLORVALUE</span></span> | <span data-ttu-id="5c1f5-119">Внешний цвет материала</span><span class="sxs-lookup"><span data-stu-id="5c1f5-119">Material ambient color</span></span>                                                                                                         |
| <span data-ttu-id="5c1f5-120">Gₐ</span><span class="sxs-lookup"><span data-stu-id="5c1f5-120">Gₐ</span></span>                | <span data-ttu-id="5c1f5-121">(0,0,0,0)</span><span class="sxs-lookup"><span data-stu-id="5c1f5-121">(0,0,0,0)</span></span>     | <span data-ttu-id="5c1f5-122">D3DCOLORVALUE</span><span class="sxs-lookup"><span data-stu-id="5c1f5-122">D3DCOLORVALUE</span></span> | <span data-ttu-id="5c1f5-123">Глобальный внешний цвет</span><span class="sxs-lookup"><span data-stu-id="5c1f5-123">Global ambient color</span></span>                                                                                                           |
| <span data-ttu-id="5c1f5-124">Аттен<sub>i</sub></span><span class="sxs-lookup"><span data-stu-id="5c1f5-124">Atten<sub>i</sub></span></span> | <span data-ttu-id="5c1f5-125">(0,0,0,0)</span><span class="sxs-lookup"><span data-stu-id="5c1f5-125">(0,0,0,0)</span></span>     | <span data-ttu-id="5c1f5-126">D3DCOLORVALUE</span><span class="sxs-lookup"><span data-stu-id="5c1f5-126">D3DCOLORVALUE</span></span> | <span data-ttu-id="5c1f5-127">Затухание света i.</span><span class="sxs-lookup"><span data-stu-id="5c1f5-127">Light attenuation of the ith light.</span></span> <span data-ttu-id="5c1f5-128">См. раздел " [ослабление и прожектор" (Direct3D 9)](attenuation-and-spotlight-factor.md).</span><span class="sxs-lookup"><span data-stu-id="5c1f5-128">See [Attenuation and Spotlight Factor (Direct3D 9)](attenuation-and-spotlight-factor.md).</span></span> |
| <span data-ttu-id="5c1f5-129">Точечная<sub>i</sub></span><span class="sxs-lookup"><span data-stu-id="5c1f5-129">Spot<sub>i</sub></span></span>  | <span data-ttu-id="5c1f5-130">(0,0,0,0)</span><span class="sxs-lookup"><span data-stu-id="5c1f5-130">(0,0,0,0)</span></span>     | <span data-ttu-id="5c1f5-131">D3DVECTOR</span><span class="sxs-lookup"><span data-stu-id="5c1f5-131">D3DVECTOR</span></span>     | <span data-ttu-id="5c1f5-132">Коэффициент вспышки света i.</span><span class="sxs-lookup"><span data-stu-id="5c1f5-132">Spotlight factor of the ith light.</span></span> <span data-ttu-id="5c1f5-133">См. раздел " [ослабление и прожектор" (Direct3D 9)](attenuation-and-spotlight-factor.md).</span><span class="sxs-lookup"><span data-stu-id="5c1f5-133">See [Attenuation and Spotlight Factor (Direct3D 9)](attenuation-and-spotlight-factor.md).</span></span>  |
| <span data-ttu-id="5c1f5-134">Sum</span><span class="sxs-lookup"><span data-stu-id="5c1f5-134">sum</span></span>               | <span data-ttu-id="5c1f5-135">Н/Д</span><span class="sxs-lookup"><span data-stu-id="5c1f5-135">N/A</span></span>           | <span data-ttu-id="5c1f5-136">Н/Д</span><span class="sxs-lookup"><span data-stu-id="5c1f5-136">N/A</span></span>           | <span data-ttu-id="5c1f5-137">Сумма внешнего освещения</span><span class="sxs-lookup"><span data-stu-id="5c1f5-137">Sum of the ambient light</span></span>                                                                                                       |
| <span data-ttu-id="5c1f5-138">L<sub>AI</sub></span><span class="sxs-lookup"><span data-stu-id="5c1f5-138">L<sub>ai</sub></span></span>    | <span data-ttu-id="5c1f5-139">(0,0,0,0)</span><span class="sxs-lookup"><span data-stu-id="5c1f5-139">(0,0,0,0)</span></span>     | <span data-ttu-id="5c1f5-140">D3DVECTOR</span><span class="sxs-lookup"><span data-stu-id="5c1f5-140">D3DVECTOR</span></span>     | <span data-ttu-id="5c1f5-141">Внешний цвет света i</span><span class="sxs-lookup"><span data-stu-id="5c1f5-141">Light ambient color of the ith light</span></span>                                                                                           |



 

<span data-ttu-id="5c1f5-142">Значение Cₐ равно одному из следующих:</span><span class="sxs-lookup"><span data-stu-id="5c1f5-142">The value for Cₐ is either:</span></span>

-   <span data-ttu-id="5c1f5-143">Вершинный color1, если АМБИЕНТМАТЕРИАЛСАУРЦЕ = D3DMCS \_ color1, а первый цвет вершин указан в объявлении вершины.</span><span class="sxs-lookup"><span data-stu-id="5c1f5-143">vertex color1, if AMBIENTMATERIALSOURCE = D3DMCS\_COLOR1, and the first vertex color is supplied in the vertex declaration.</span></span>
-   <span data-ttu-id="5c1f5-144">Вершинный color2, если АМБИЕНТМАТЕРИАЛСАУРЦЕ = D3DMCS \_ color2, а второй цвет вершин указан в объявлении вершины.</span><span class="sxs-lookup"><span data-stu-id="5c1f5-144">vertex color2, if AMBIENTMATERIALSOURCE = D3DMCS\_COLOR2, and the second vertex color is supplied in vertex declaration.</span></span>
-   <span data-ttu-id="5c1f5-145">внешний цвет материала.</span><span class="sxs-lookup"><span data-stu-id="5c1f5-145">material ambient color.</span></span>

> [!Note]  
> <span data-ttu-id="5c1f5-146">Если используется параметр АМБИЕНТМАТЕРИАЛСАУРЦЕ и не указан цвет вершины, используется окружающий цвет материала.</span><span class="sxs-lookup"><span data-stu-id="5c1f5-146">If either AMBIENTMATERIALSOURCE option is used, and the vertex color is not provided, then the material ambient color is used.</span></span>

 

<span data-ttu-id="5c1f5-147">Чтобы использовать внешний цвет материала, используйте свойство SetMaterial, как показано в примере кода ниже.</span><span class="sxs-lookup"><span data-stu-id="5c1f5-147">To use the material ambient color, use SetMaterial as shown in the example code below.</span></span>

<span data-ttu-id="5c1f5-148">Gₐ — это глобальный внешний цвет.</span><span class="sxs-lookup"><span data-stu-id="5c1f5-148">Gₐ is the global ambient color.</span></span> <span data-ttu-id="5c1f5-149">Он задается с помощью Сетрендерстате ( \_ внешнего D3DRS).</span><span class="sxs-lookup"><span data-stu-id="5c1f5-149">It is set using SetRenderState(D3DRS\_AMBIENT).</span></span> <span data-ttu-id="5c1f5-150">В сцене Direct3D существует один глобальный внешний цвет.</span><span class="sxs-lookup"><span data-stu-id="5c1f5-150">There is one global ambient color in a Direct3D scene.</span></span> <span data-ttu-id="5c1f5-151">Этот параметр не связан с объектом света Direct3D.</span><span class="sxs-lookup"><span data-stu-id="5c1f5-151">This parameter is not associated with a Direct3D light object.</span></span>

<span data-ttu-id="5c1f5-152">L<sub>ai</sub> — это внешний цвет света i в сцене.</span><span class="sxs-lookup"><span data-stu-id="5c1f5-152">L<sub>ai</sub> is the ambient color of the ith light in the scene.</span></span> <span data-ttu-id="5c1f5-153">Каждый свет Direct3D имеет набор свойств, одно из которых — внешний цвет.</span><span class="sxs-lookup"><span data-stu-id="5c1f5-153">Each Direct3D light has a set of properties, one of which is the ambient color.</span></span> <span data-ttu-id="5c1f5-154">Термин sum(L<sub>ai</sub>) представляет собой сумму всех внешних цветов в сцене.</span><span class="sxs-lookup"><span data-stu-id="5c1f5-154">The term, sum(L<sub>ai</sub>) is a sum of all the ambient colors in the scene.</span></span>

## <a name="example"></a><span data-ttu-id="5c1f5-155">Пример</span><span class="sxs-lookup"><span data-stu-id="5c1f5-155">Example</span></span>

<span data-ttu-id="5c1f5-156">В этом примере объект окрашен с помощью внешнего света сцены и внешнего цвета материала.</span><span class="sxs-lookup"><span data-stu-id="5c1f5-156">In this example, the object is colored using the scene ambient light and a material ambient color.</span></span>


```
#define GRAY_COLOR  0x00bfbfbf

// create material
D3DMATERIAL9 mtrl;
ZeroMemory(&mtrl, sizeof(mtrl));
mtrl.Ambient.r = 0.75f;
mtrl.Ambient.g = 0.0f;
mtrl.Ambient.b = 0.0f;
mtrl.Ambient.a = 0.0f;
m_pd3dDevice->SetMaterial(&mtrl);
m_pd3dDevice->SetRenderState(D3DRS_AMBIENT, GRAY_COLOR);
```



<span data-ttu-id="5c1f5-157">Согласно уравнению, получившийся цвет для вершин объекта — это сочетание цвета материала и цвета света.</span><span class="sxs-lookup"><span data-stu-id="5c1f5-157">According to the equation, the resulting color for the object vertices is a combination of the material color and the light color.</span></span>

<span data-ttu-id="5c1f5-158">На двух следующих рисунках показан цвет материала (серый) и цвет света (ярко-красный).</span><span class="sxs-lookup"><span data-stu-id="5c1f5-158">The following two illustrations show the material color, which is gray, and the light color, which is bright red.</span></span>

![иллюстрация серой сферы](images/amb1.jpg)![иллюстрация красной сферы](images/lightred.jpg)

<span data-ttu-id="5c1f5-161">Получившаяся сцена показана на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="5c1f5-161">The resulting scene is shown in the following illustration.</span></span> <span data-ttu-id="5c1f5-162">Единственный объект в сцене — сфера.</span><span class="sxs-lookup"><span data-stu-id="5c1f5-162">The only object in the scene is a sphere.</span></span> <span data-ttu-id="5c1f5-163">Внешний свет освещает все вершины объекта одинаковым цветом.</span><span class="sxs-lookup"><span data-stu-id="5c1f5-163">Ambient light lights all object vertices with the same color.</span></span> <span data-ttu-id="5c1f5-164">Это не зависит от нормали вершины или направления света.</span><span class="sxs-lookup"><span data-stu-id="5c1f5-164">It is not dependent on the vertex normal or the light direction.</span></span> <span data-ttu-id="5c1f5-165">В результате сфера выглядит как двухмерный круг, поскольку затенение вокруг поверхности объекта одинаковое.</span><span class="sxs-lookup"><span data-stu-id="5c1f5-165">As a result, the sphere looks like a 2D circle because there is no difference in shading around the surface of the object.</span></span>

![иллюстрация сферы с внешним светом](images/lighta.jpg)

<span data-ttu-id="5c1f5-167">Чтобы объекты выглядели более реалистично, используйте помимо внешнего света еще рассеянный и зеркальный свет.</span><span class="sxs-lookup"><span data-stu-id="5c1f5-167">To give objects a more realistic look, apply diffuse or specular lighting in addition to ambient lighting.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5c1f5-168">См. также</span><span class="sxs-lookup"><span data-stu-id="5c1f5-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5c1f5-169">Математика освещения</span><span class="sxs-lookup"><span data-stu-id="5c1f5-169">Mathematics of Lighting</span></span>](mathematics-of-lighting.md)
</dt> </dl>

 

 



