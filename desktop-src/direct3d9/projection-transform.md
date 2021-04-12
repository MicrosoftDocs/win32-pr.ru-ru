---
description: Преобразование «проекция» можно рассматривать как управление внутренними функциями камеры. аналогично выбору линзы для камеры.
ms.assetid: 09e6e887-7657-4654-be19-2e83dcbc91cf
title: Преобразование проекции (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37b518583dd534bec9784590150233847274ca71
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104262406"
---
# <a name="projection-transform-direct3d-9"></a><span data-ttu-id="141a1-103">Преобразование проекции (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="141a1-103">Projection Transform (Direct3D 9)</span></span>

<span data-ttu-id="141a1-104">Преобразование «проекция» можно рассматривать как управление внутренними функциями камеры. аналогично выбору линзы для камеры.</span><span class="sxs-lookup"><span data-stu-id="141a1-104">You can think of the projection transformation as controlling the camera's internals; it is analogous to choosing a lens for the camera.</span></span> <span data-ttu-id="141a1-105">Это самый сложный из всех трех типов преобразований.</span><span class="sxs-lookup"><span data-stu-id="141a1-105">This is the most complicated of the three transformation types.</span></span> <span data-ttu-id="141a1-106">Это обсуждение преобразования «проекция» организовано в следующие разделы.</span><span class="sxs-lookup"><span data-stu-id="141a1-106">This discussion of the projection transformation is organized into the following topics.</span></span>

<span data-ttu-id="141a1-107">Обычно матрица проекции — это проекция масштаба и перспективы.</span><span class="sxs-lookup"><span data-stu-id="141a1-107">The projection matrix is typically a scale and perspective projection.</span></span> <span data-ttu-id="141a1-108">Проекционное преобразование превращает видимое пространство (усеченную пирамиду) в кубовидную фигуру.</span><span class="sxs-lookup"><span data-stu-id="141a1-108">The projection transformation converts the viewing frustum into a cuboid shape.</span></span> <span data-ttu-id="141a1-109">Так как ближний конец видимого пространства меньше дальнего, это приводит к развертыванию объектов, которые находятся ближе к камере — так перспектива применяется к сцене.</span><span class="sxs-lookup"><span data-stu-id="141a1-109">Because the near end of the viewing frustum is smaller than the far end, this has the effect of expanding objects that are near to the camera; this is how perspective is applied to the scene.</span></span>

<span data-ttu-id="141a1-110">В [видимом пространстве](viewports-and-clipping.md) расстояние между камерой и началом координат видимого пространства преобразования определяется произвольно как D, поэтому матрица проекции выглядит, как показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="141a1-110">In [the viewing frustum](viewports-and-clipping.md), the distance between the camera and the origin of the viewing transform space is defined arbitrarily as D, so the projection matrix looks like the following illustration.</span></span>

![иллюстрация матрицы проекции](images/projmat1.png)

<span data-ttu-id="141a1-112">Матрица просмотра переносит камеру в начало координат, перемещаясь в направлении z на –D. Матрицы преобразования выглядит, как показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="141a1-112">The viewing matrix translates the camera to the origin by translating in the z direction by - D. The translation matrix is like the following illustration.</span></span>

![иллюстрация матрицы преобразования](images/projmat2.png)

<span data-ttu-id="141a1-114">Умножение матрицы преобразования на матрицу проекции (T \* P) дает матрицу составной проекции, как показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="141a1-114">Multiplying the translation matrix by the projection matrix (T\*P) gives the composite projection matrix, as shown in the following illustration.</span></span>

![иллюстрация составной матрицы проекции](images/projmat3.png)

<span data-ttu-id="141a1-116">Преобразование перспективы превращает видимое пространство в новое пространство координат.</span><span class="sxs-lookup"><span data-stu-id="141a1-116">The perspective transform converts a viewing frustum into a new coordinate space.</span></span> <span data-ttu-id="141a1-117">Обратите внимание, что усеченная пирамида становится кубоидом, а начало координат перемещается из правого верхнего угла сцены в центр, как показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="141a1-117">Notice that the frustum becomes cuboid and also that the origin moves from the upper-right corner of the scene to the center, as shown in the following diagram.</span></span>

![схема изменения усеченной пирамиды обзора в новое пространства координат за счет преобразования перспективы](images/cuboid.png)

<span data-ttu-id="141a1-119">При преобразовании перспективы ограничения направлений x и y равны –1 и 1 соответственно.</span><span class="sxs-lookup"><span data-stu-id="141a1-119">In the perspective transform, the limits of the x- and y-directions are -1 and 1.</span></span> <span data-ttu-id="141a1-120">Ограничения по оси z равны 0 для передней плоскости и 1 для задней плоскости.</span><span class="sxs-lookup"><span data-stu-id="141a1-120">The limits of the z-direction are 0 for the front plane and 1 for the back plane.</span></span>

<span data-ttu-id="141a1-121">Эта матрица преобразует и масштабирует объекты на основе определенного расстояния между камерой и ближней плоскостью отсечения, но при этом не учитывается, что поле зрения (fov) и z-значения, создаваемые для объектов, на расстоянии могут быть практически идентичными, что усложняет сравнение глубины.</span><span class="sxs-lookup"><span data-stu-id="141a1-121">This matrix translates and scales objects based on a specified distance from the camera to the near clipping plane, but it doesn't consider the field of view (fov), and the z-values that it produces for objects in the distance can be nearly identical, making depth comparisons difficult.</span></span> <span data-ttu-id="141a1-122">Следующая матрица решает эти проблемы и корректирует вершины для учета пропорций окна просмотра, что хорошо подходит для проекции перспективы.</span><span class="sxs-lookup"><span data-stu-id="141a1-122">The following matrix addresses these issues, and it adjusts vertices to account for the aspect ratio of the viewport, making it a good choice for the perspective projection.</span></span>

![иллюстрация матрицы для проекции перспективы](images/prjmatx1.png)

<span data-ttu-id="141a1-124">В этой матрице Zₙ — это z-значение ближней плоскости отсечения.</span><span class="sxs-lookup"><span data-stu-id="141a1-124">In this matrix, Zₙ is the z-value of the near clipping plane.</span></span> <span data-ttu-id="141a1-125">Переменные w, h и Q имеют следующие значения.</span><span class="sxs-lookup"><span data-stu-id="141a1-125">The variables w, h, and Q have the following meanings.</span></span> <span data-ttu-id="141a1-126">Обратите внимание, что fov<sub>w</sub> и fovₖ представляют горизонтальные и вертикальные поля зрения окна просмотра в радианах.</span><span class="sxs-lookup"><span data-stu-id="141a1-126">Note that fov<sub>w</sub> and fovₖ represent the viewport's horizontal and vertical fields of view, in radians.</span></span>

![формулы значений переменных](images/prjmatx2.png)

<span data-ttu-id="141a1-128">В вашем приложении использование углов полей зрения для определения коэффициентов масштабирования осей x и y может быть не так удобно, как применение горизонтального и вертикального измерения окна просмотра (в пространстве камеры).</span><span class="sxs-lookup"><span data-stu-id="141a1-128">For your application, using field-of-view angles to define the x- and y-scaling coefficients might not be as convenient as using the viewport's horizontal and vertical dimensions (in camera space).</span></span> <span data-ttu-id="141a1-129">В следующих двух уравнениях для w и h используются измерения окна просмотра, при этом они эквивалентны предыдущим формулам.</span><span class="sxs-lookup"><span data-stu-id="141a1-129">As the math works out, the following two equations for w and h use the viewport's dimensions, and are equivalent to the preceding equations.</span></span>

![формулы значений переменных w и h](images/prjmatx3.png)

<span data-ttu-id="141a1-131">В этих формулах Zₙ представляет положение ближней плоскости отсечения, а переменные V<sub>w</sub> и Vₕ представляют ширину и высоту окна просмотра в пространстве камеры.</span><span class="sxs-lookup"><span data-stu-id="141a1-131">In these formulas, Zₙ represents the position of the near clipping plane, and the V<sub>w</sub> and Vₕ variables represent the width and height of the viewport, in camera space.</span></span>

<span data-ttu-id="141a1-132">Для приложения C++ эти два измерения непосредственно соответствуют элементам Width и Height структуры [**D3DVIEWPORT9**](d3dviewport9.md) .</span><span class="sxs-lookup"><span data-stu-id="141a1-132">For a C++ application, these two dimensions correspond directly to the Width and Height members of the [**D3DVIEWPORT9**](d3dviewport9.md) structure.</span></span>

<span data-ttu-id="141a1-133">Какую бы формулу вы ни выбрали, обязательно установите для Zₙ максимально возможное значение, так как z-значения, очень близкие к камере, не сильно отличаются.</span><span class="sxs-lookup"><span data-stu-id="141a1-133">Whatever formula you decide to use, be sure to set Zₙ to as large a value as possible, because z-values extremely close to the camera don't vary by much.</span></span> <span data-ttu-id="141a1-134">Это относительно усложняет сравнение глубины с помощью 16-разрядных z-буферов.</span><span class="sxs-lookup"><span data-stu-id="141a1-134">This makes depth comparisons using 16-bit z-buffers somewhat complicated.</span></span>

<span data-ttu-id="141a1-135">Как и в случае с преобразованиями мира и представлений, вы вызываете метод [**IDirect3DDevice9:: сеттрансформ**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform) , чтобы задать преобразование проекции.</span><span class="sxs-lookup"><span data-stu-id="141a1-135">As with the world and view transformations, you call the [**IDirect3DDevice9::SetTransform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform) method to set the projection transform.</span></span>

## <a name="setting-up-a-projection-matrix"></a><span data-ttu-id="141a1-136">Настройка матрицы проекции</span><span class="sxs-lookup"><span data-stu-id="141a1-136">Setting Up a Projection Matrix</span></span>

<span data-ttu-id="141a1-137">В приведенной ниже образце функции Прожектионматрикс задаются фронтальные и обратные плоскости, а также горизонтальное и вертикальное поле углов представления.</span><span class="sxs-lookup"><span data-stu-id="141a1-137">The following ProjectionMatrix sample function sets the front and back clipping planes, as well as the horizontal and vertical field of view angles.</span></span> <span data-ttu-id="141a1-138">Поля представления должны быть меньше PI радиан.</span><span class="sxs-lookup"><span data-stu-id="141a1-138">The fields of view should be less than pi radians.</span></span>


```
D3DXMATRIX 
ProjectionMatrix(const float near_plane, // Distance to near clipping 
                                         // plane
                 const float far_plane,  // Distance to far clipping 
                                         // plane
                 const float fov_horiz,  // Horizontal field of view 
                                         // angle, in radians
                 const float fov_vert)   // Vertical field of view 
                                         // angle, in radians
{
    float    h, w, Q;

    w = (float)1/tan(fov_horiz*0.5);  // 1/tan(x) == cot(x)
    h = (float)1/tan(fov_vert*0.5);   // 1/tan(x) == cot(x)
    Q = far_plane/(far_plane - near_plane);

    D3DXMATRIX ret;
    ZeroMemory(&ret, sizeof(ret));

    ret(0, 0) = w;
    ret(1, 1) = h;
    ret(2, 2) = Q;
    ret(3, 2) = -Q*near_plane;
    ret(2, 3) = 1;
    return ret;
}   // End of ProjectionMatrix
```



<span data-ttu-id="141a1-139">После создания матрицы задайте [**IDirect3DDevice9:: сеттрансформ**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform) , указав D3DTS \_ проекцию.</span><span class="sxs-lookup"><span data-stu-id="141a1-139">After creating the matrix, set it with [**IDirect3DDevice9::SetTransform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform) specifying D3DTS\_PROJECTION.</span></span>

<span data-ttu-id="141a1-140">Библиотека служебной программы D3DX предоставляет следующие функции, помогающие настроить матрицу проекции.</span><span class="sxs-lookup"><span data-stu-id="141a1-140">The D3DX utility library provides the following functions to help you set up your projection matrix.</span></span>

-   [<span data-ttu-id="141a1-141">**D3DXMatrixPerspectiveLH**</span><span class="sxs-lookup"><span data-stu-id="141a1-141">**D3DXMatrixPerspectiveLH**</span></span>](d3dxmatrixperspectivelh.md)
-   [<span data-ttu-id="141a1-142">**D3DXMatrixPerspectiveRH**</span><span class="sxs-lookup"><span data-stu-id="141a1-142">**D3DXMatrixPerspectiveRH**</span></span>](d3dxmatrixperspectiverh.md)
-   [<span data-ttu-id="141a1-143">**D3DXMatrixPerspectiveFovLH**</span><span class="sxs-lookup"><span data-stu-id="141a1-143">**D3DXMatrixPerspectiveFovLH**</span></span>](d3dxmatrixperspectivefovlh.md)
-   [<span data-ttu-id="141a1-144">**D3DXMatrixPerspectiveFovRH**</span><span class="sxs-lookup"><span data-stu-id="141a1-144">**D3DXMatrixPerspectiveFovRH**</span></span>](d3dxmatrixperspectivefovrh.md)
-   [<span data-ttu-id="141a1-145">**D3DXMatrixPerspectiveOffCenterLH**</span><span class="sxs-lookup"><span data-stu-id="141a1-145">**D3DXMatrixPerspectiveOffCenterLH**</span></span>](d3dxmatrixperspectiveoffcenterlh.md)
-   [<span data-ttu-id="141a1-146">**D3DXMatrixPerspectiveOffCenterRH**</span><span class="sxs-lookup"><span data-stu-id="141a1-146">**D3DXMatrixPerspectiveOffCenterRH**</span></span>](d3dxmatrixperspectiveoffcenterrh.md)

## <a name="a-w-friendly-projection-matrix"></a><span data-ttu-id="141a1-147">Матрица проекций с поддержкой W</span><span class="sxs-lookup"><span data-stu-id="141a1-147">A W-Friendly Projection Matrix</span></span>

<span data-ttu-id="141a1-148">Direct3D может использовать компонент w вершины, которая была преобразована абсолютной матрицей, а также матрицами представления и проекции для вычислений на основе глубины при использовании буфера глубины или эффекта тумана.</span><span class="sxs-lookup"><span data-stu-id="141a1-148">Direct3D can use the w-component of a vertex that has been transformed by the world, view, and projection matrices to perform depth-based calculations in depth-buffer or fog effects.</span></span> <span data-ttu-id="141a1-149">Для таких вычислений требуется, чтобы матрица проекции нормализовала переменную w как эквивалентную координате z в абсолютном пространстве.</span><span class="sxs-lookup"><span data-stu-id="141a1-149">Computations such as these require that your projection matrix normalize w to be equivalent to world-space z.</span></span> <span data-ttu-id="141a1-150">Иными словами, если матрица проекции включает коэффициент (3,4), не равный 1, необходимо масштабировать все коэффициенты, инвертируя коэффициент (3,4) для получения правильной матрицы.</span><span class="sxs-lookup"><span data-stu-id="141a1-150">In short, if your projection matrix includes a (3,4) coefficient that is not 1, you must scale all the coefficients by the inverse of the (3,4) coefficient to make a proper matrix.</span></span> <span data-ttu-id="141a1-151">Если не предоставить совместимую матрицу, эффекты тумана и буферизация глубины не будут правильно применены.</span><span class="sxs-lookup"><span data-stu-id="141a1-151">If you don't provide a compliant matrix, fog effects and depth buffering are not applied correctly.</span></span>

<span data-ttu-id="141a1-152">На следующем рисунке показана несоответствующая требованиям матрица проекции и та же матрица, масштабированная для применения тумана туман относительно зрителя.</span><span class="sxs-lookup"><span data-stu-id="141a1-152">The following illustration shows a noncompliant projection matrix, and the same matrix scaled so that eye-relative fog will be enabled.</span></span>

![иллюстрации несоответствующей матрицы проекции и матрицы с туманом относительно зрителя](images/eyerlmx.png)

<span data-ttu-id="141a1-154">В предыдущих матрицах предполагается, что все переменные не равны нулю.</span><span class="sxs-lookup"><span data-stu-id="141a1-154">In the preceding matrices, all variables are assumed to be nonzero.</span></span> <span data-ttu-id="141a1-155">Дополнительные сведения о относительном тумане с учетом взгляда см. в разделе [глубина, относительная относительно глаз и Z](pixel-fog.md).</span><span class="sxs-lookup"><span data-stu-id="141a1-155">For more information about eye-relative fog, see [Eye-Relative vs. Z-Based Depth](pixel-fog.md).</span></span> <span data-ttu-id="141a1-156">Сведения о буферизации глубины на основе w см. в разделе [буферы глубины (Direct3D 9)](depth-buffers.md).</span><span class="sxs-lookup"><span data-stu-id="141a1-156">For information about w-based depth buffering, see [Depth Buffers (Direct3D 9)](depth-buffers.md).</span></span>

<span data-ttu-id="141a1-157">Direct3D использует текущую матрицу проекции при расчетах глубины вершин на основе переменной w.</span><span class="sxs-lookup"><span data-stu-id="141a1-157">Direct3D uses the currently set projection matrix in its w-based depth calculations.</span></span> <span data-ttu-id="141a1-158">В результате приложения должны установить соответствующую матрицу проекции для получения необходимых функций на основе компонента w, даже если они не используют Direct3D для преобразования.</span><span class="sxs-lookup"><span data-stu-id="141a1-158">As a result, applications must set a compliant projection matrix to receive the desired w-based features, even if they do not use Direct3D for transforms.</span></span>

## <a name="related-topics"></a><span data-ttu-id="141a1-159">См. также</span><span class="sxs-lookup"><span data-stu-id="141a1-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="141a1-160">Преобразования</span><span class="sxs-lookup"><span data-stu-id="141a1-160">Transforms</span></span>](transforms.md)
</dt> </dl>

 

 
