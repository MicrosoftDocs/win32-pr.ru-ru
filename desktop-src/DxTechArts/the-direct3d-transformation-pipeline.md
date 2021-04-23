---
title: Конвейер преобразования Direct3D
description: В этой статье содержится техническое описание разработчиков приложений Direct3D по настройке параметров конвейера преобразования Direct3D путем непосредственной манипуляции с матрицами Direct3D.
ms.assetid: 48ae49f0-1162-c292-4bd4-34da5aadd2df
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2b97a87293a840ccd9641b1418c2005cf73a855
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/04/2021
ms.locfileid: "103913943"
---
# <a name="the-direct3d-transformation-pipeline"></a><span data-ttu-id="bd6ff-103">Конвейер преобразования Direct3D</span><span class="sxs-lookup"><span data-stu-id="bd6ff-103">The Direct3D Transformation Pipeline</span></span>

<span data-ttu-id="bd6ff-104">В этой статье содержится техническое описание разработчиков приложений Direct3D по настройке параметров конвейера преобразования Direct3D путем непосредственной манипуляции с матрицами Direct3D.</span><span class="sxs-lookup"><span data-stu-id="bd6ff-104">This article provides a technical explanation for Direct3D application developers on how to set the parameters of the Direct3D Transformation Pipeline by the direct manipulation of Direct3D matrices.</span></span>

-   [<span data-ttu-id="bd6ff-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="bd6ff-105">Overview</span></span>](#overview)
-   [<span data-ttu-id="bd6ff-106">Конвейер преобразования</span><span class="sxs-lookup"><span data-stu-id="bd6ff-106">The Transformation Pipeline</span></span>](#the-transformation-pipeline)
-   [<span data-ttu-id="bd6ff-107">Советы по использованию</span><span class="sxs-lookup"><span data-stu-id="bd6ff-107">Usage Tips</span></span>](#usage-tips)

## <a name="overview"></a><span data-ttu-id="bd6ff-108">Обзор</span><span class="sxs-lookup"><span data-stu-id="bd6ff-108">Overview</span></span>

<span data-ttu-id="bd6ff-109">В Direct3D используется три преобразования для перевода координат трехмерной модели в координаты пикселей (пространство экрана).</span><span class="sxs-lookup"><span data-stu-id="bd6ff-109">Direct3D uses three transformations to change your 3D model coordinates into pixel coordinates (screen space).</span></span> <span data-ttu-id="bd6ff-110">Эти преобразования — мировое преобразование, видовое преобразование и проекционное преобразование.</span><span class="sxs-lookup"><span data-stu-id="bd6ff-110">These transformations are world transform, view transform, and projection transform.</span></span>

<span data-ttu-id="bd6ff-111">Преобразование «мир» управляет тем, как координаты модели преобразуются в мировые координаты.</span><span class="sxs-lookup"><span data-stu-id="bd6ff-111">World transform controls how model coordinates are transformed into world coordinates.</span></span> <span data-ttu-id="bd6ff-112">Преобразование «мир» может включать переводы, вращения и масштабирование, но не применяется к индикаторам.</span><span class="sxs-lookup"><span data-stu-id="bd6ff-112">World transform can include translations, rotations, and scalings, but it does not apply to lights.</span></span> <span data-ttu-id="bd6ff-113">Дополнительные сведения о работе с преобразованиями мирового уровня см. в разделе [универсальное преобразование](/windows/desktop/direct3d9/world-transform).</span><span class="sxs-lookup"><span data-stu-id="bd6ff-113">For more information on working with world transforms, see [World Transform](/windows/desktop/direct3d9/world-transform).</span></span>

<span data-ttu-id="bd6ff-114">Представление "преобразование" управляет переходом от мировых координат в "область камеры", определяя расположение камеры в мире.</span><span class="sxs-lookup"><span data-stu-id="bd6ff-114">View transform controls the transition from world coordinates into "camera space," determining camera position in the world.</span></span> <span data-ttu-id="bd6ff-115">Пример работы с преобразованиями представлений см. в разделе [представление преобразования](/windows/desktop/direct3d9/view-transform).</span><span class="sxs-lookup"><span data-stu-id="bd6ff-115">For an example of working with view transforms, see [View Transform](/windows/desktop/direct3d9/view-transform).</span></span>

<span data-ttu-id="bd6ff-116">Преобразование «проекция» изменяет геометрию из области камеры на «место обрезки» и применяет искажение перспективы.</span><span class="sxs-lookup"><span data-stu-id="bd6ff-116">Projection transform changes the geometry from camera space into "clip space" and applies perspective distortion.</span></span> <span data-ttu-id="bd6ff-117">Термин «пространство обрезки» означает, как геометрия обрезается в том представления во время этого преобразования.</span><span class="sxs-lookup"><span data-stu-id="bd6ff-117">The term "clip space" refers to how the geometry is clipped to the view volume during this transform.</span></span> <span data-ttu-id="bd6ff-118">Пример работы с преобразованиями проекции см. в разделе [преобразование проекции](/windows/desktop/direct3d9/projection-transform).</span><span class="sxs-lookup"><span data-stu-id="bd6ff-118">For an example of working with projection transforms, see [Projection Transform](/windows/desktop/direct3d9/projection-transform).</span></span>

<span data-ttu-id="bd6ff-119">Наконец, геометрия в пространстве обрезки преобразуется в координаты пикселей (пространство экрана).</span><span class="sxs-lookup"><span data-stu-id="bd6ff-119">Finally, the geometry in clip space is transformed into pixel coordinates (screen space).</span></span> <span data-ttu-id="bd6ff-120">Это преобразование управляется параметрами окна просмотра.</span><span class="sxs-lookup"><span data-stu-id="bd6ff-120">This transformation is controlled by the viewport settings.</span></span>

<span data-ttu-id="bd6ff-121">Отсечение и преобразование вершин должно выполняться в однородном пространстве (просто размещение, в котором система координат включает четвертый элемент), но окончательный результат для большинства приложений должен быть не однородными трехмерными (трехмерными) координатами, определенными в "пространстве экрана".</span><span class="sxs-lookup"><span data-stu-id="bd6ff-121">Clipping and transforming vertices must take place in homogenous space (simply put, space in which the coordinate system includes a fourth element), but the final result for most applications needs to be non-homogenous three-dimensional (3D) coordinates defined in "screen space."</span></span> <span data-ttu-id="bd6ff-122">Это означает, что входные вершины и том обрезки должны быть преобразованы в однородное пространство для выполнения обрезки, а затем преобразованы обратно в неоднородное пространство для отображения.</span><span class="sxs-lookup"><span data-stu-id="bd6ff-122">This means that both the input vertices and the clipping volume must be translated into homogenous space to perform the clipping and then translated back into non-homogenous space to be displayed.</span></span>

<span data-ttu-id="bd6ff-123">Три преобразования Direct3D — преобразование «мир», «представление» и «проекция» — определяются матрицами Direct3D.</span><span class="sxs-lookup"><span data-stu-id="bd6ff-123">The three Direct3D transformations-world, view, and projection transform-are defined by Direct3D matrices.</span></span> <span data-ttu-id="bd6ff-124">Матрица Direct3D — это однородная матрица 4x4, определенная структурой [**D3DMATRIX**](/windows/desktop/direct3d9/d3dmatrix) .</span><span class="sxs-lookup"><span data-stu-id="bd6ff-124">A Direct3D matrix is a 4x4 homogenous matrix defined by a [**D3DMATRIX**](/windows/desktop/direct3d9/d3dmatrix) structure.</span></span> <span data-ttu-id="bd6ff-125">Несмотря на то, что матрицы Direct3D не являются стандартными объектами, они не представлены COM-интерфейсом. их можно создавать и задавать так же, как любой другой объект Direct3D.</span><span class="sxs-lookup"><span data-stu-id="bd6ff-125">Although Direct3D matrices are not standard objects-they are not represented by a COM interface-you can create and set them just as you would any other Direct3D object.</span></span> <span data-ttu-id="bd6ff-126">Дополнительные сведения о матрицах Direct3D см. в разделе [преобразования](/windows/desktop/direct3d9/transforms).</span><span class="sxs-lookup"><span data-stu-id="bd6ff-126">For more information on Direct3D matrices, see [Transforms](/windows/desktop/direct3d9/transforms).</span></span>

## <a name="the-transformation-pipeline"></a><span data-ttu-id="bd6ff-127">Конвейер преобразования</span><span class="sxs-lookup"><span data-stu-id="bd6ff-127">The Transformation Pipeline</span></span>

<span data-ttu-id="bd6ff-128">Если вершина в координатах модели имеет значение PM = (XM, им, ZM, 1), то преобразования, показанные на следующем рисунке, применяются к экранным координатам вычислений PS = (XS, ИС, ZS, WS).</span><span class="sxs-lookup"><span data-stu-id="bd6ff-128">If a vertex in the model coordinate is given by Pm = (Xm, Ym, Zm, 1), then the transformations shown in the following figure are applied to compute screen coordinates Ps = (Xs, Ys, Zs, Ws).</span></span>

![Преобразование пространства модели в область экрана](images/d3dxfrm61.gif)

<span data-ttu-id="bd6ff-130">Ниже приведены описания этапов, показанных на предыдущем рисунке.</span><span class="sxs-lookup"><span data-stu-id="bd6ff-130">Here are descriptions of the stages that are shown in the preceding figure:</span></span>

1.  <span data-ttu-id="bd6ff-131">Матрица World Мворлд преобразует вершины из области модели в мировое пространство.</span><span class="sxs-lookup"><span data-stu-id="bd6ff-131">World matrix Mworld transforms vertices from the model space to the world space.</span></span> <span data-ttu-id="bd6ff-132">Эта матрица задается следующим образом:</span><span class="sxs-lookup"><span data-stu-id="bd6ff-132">This matrix is set by:</span></span>

    ``` syntax
        d3dDevice->SetTransform (D3DTRANSFORMSTATE_WORLD, matrix address) 
    ```

    <span data-ttu-id="bd6ff-133">В реализации Direct3D предполагается, что последний столбец этой матрицы имеет значение (0, 0, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="bd6ff-133">Direct3D implementation assumes that the last column of this matrix is (0, 0, 0, 1).</span></span> <span data-ttu-id="bd6ff-134">Если пользователь указывает матрицу с другим последним столбцом, то ошибка не возвращается, но освещение и туман будут неправильными.</span><span class="sxs-lookup"><span data-stu-id="bd6ff-134">No error is returned if the user specifies a matrix with a different last column, but the lighting and fog will be incorrect.</span></span>

2.  <span data-ttu-id="bd6ff-135">Просмотр матрицы Мвиев преобразует вершины из мирового пространства в пространство камеры.</span><span class="sxs-lookup"><span data-stu-id="bd6ff-135">View matrix Mview transforms vertices from the world space to the camera space.</span></span> <span data-ttu-id="bd6ff-136">Эта матрица задается следующим образом:</span><span class="sxs-lookup"><span data-stu-id="bd6ff-136">This matrix is set by:</span></span>

    ``` syntax
        d3dDevice->SetTransform (D3DTRANSFORMSTATE_VIEW, matrix address) 
    ```

    <span data-ttu-id="bd6ff-137">В реализации Direct3D предполагается, что последний столбец этой матрицы имеет значение (0, 0, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="bd6ff-137">Direct3D implementation assumes that the last column of this matrix is (0, 0, 0, 1).</span></span> <span data-ttu-id="bd6ff-138">Если пользователь указывает матрицу с другим последним столбцом, то ошибка не возвращается, но освещение и туман будут неправильными.</span><span class="sxs-lookup"><span data-stu-id="bd6ff-138">No error is returned if the user specifies a matrix with different last column, but the lighting and fog will be incorrect.</span></span>

3.  <span data-ttu-id="bd6ff-139">Матрица проекции Мпрож преобразует вершины из пространства камеры в пространство проекции.</span><span class="sxs-lookup"><span data-stu-id="bd6ff-139">Projection matrix Mproj transforms vertices from the camera space to the projection space.</span></span> <span data-ttu-id="bd6ff-140">Эта матрица задается следующим образом:</span><span class="sxs-lookup"><span data-stu-id="bd6ff-140">This matrix is set by:</span></span>

    ``` syntax
        d3dDevice->SetTransform (D3DTRANSFORMSTATE_PROJECTION, matrix address) 
    ```

    <span data-ttu-id="bd6ff-141">Последний столбец матрицы проекции должен иметь значение (0, 0, 1, 0) или (0, 0, a, 0) для правильного эффекта тумана и освещения. предпочтительно использовать форму (0, 0, 1, 0).</span><span class="sxs-lookup"><span data-stu-id="bd6ff-141">The last column of the projection matrix should be (0, 0, 1, 0), or (0, 0, a, 0) for correct fog and lighting effects; (0, 0, 1, 0) form is preferred.</span></span>

    <span data-ttu-id="bd6ff-142">Отсеченный том для всех точек XP = (XP, ИП, ZP, WP) в пространстве проекции определяется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="bd6ff-142">Clipping volume for all points Xp = (Xp, Yp, Zp, Wp) in the projection space is defined as:</span></span>

    ``` syntax
        -Wp < Xp <= Wp 
        -Wp < Yp <= Wp 
        0 < Zp <= Wp 
    ```

    <span data-ttu-id="bd6ff-143">Все точки, которые не соответствуют этим формулам, будут обрезаны.</span><span class="sxs-lookup"><span data-stu-id="bd6ff-143">All points that do not satisfy these equations will be clipped.</span></span>

    <span data-ttu-id="bd6ff-144">Если том представления определен как:</span><span class="sxs-lookup"><span data-stu-id="bd6ff-144">If a view volume is defined as:</span></span>

    -   <span data-ttu-id="bd6ff-145">Программная ширина экранного окна в пространстве камеры в ближней вырезанной плоскости</span><span class="sxs-lookup"><span data-stu-id="bd6ff-145">Sw-screen window width in camera space in near clipping plane</span></span>
    -   <span data-ttu-id="bd6ff-146">SH-высота окна экрана в пространстве камеры в ближайшем вырезанной плоскости</span><span class="sxs-lookup"><span data-stu-id="bd6ff-146">Sh-screen window height in camera space in near clipping plane</span></span>
    -   <span data-ttu-id="bd6ff-147">Зн. Расстояние до ближайшей плоскости обрезки вдоль Z-осей в пространстве камеры</span><span class="sxs-lookup"><span data-stu-id="bd6ff-147">Zn-distance to the near clipping plane along Z axes in camera space</span></span>
    -   <span data-ttu-id="bd6ff-148">ЗФ, расстояние до дальней плоскости и оси Z в пространстве камеры</span><span class="sxs-lookup"><span data-stu-id="bd6ff-148">Zf-distance to the far clipping plane along Z axes in camera space</span></span>

    <span data-ttu-id="bd6ff-149">затем матрица проекции перспективы может быть написана следующим образом:</span><span class="sxs-lookup"><span data-stu-id="bd6ff-149">then a perspective projection matrix could be written as follows:</span></span>

    ![Показывает матрицу проекции перспективы.](images/d3dxfrm62.gif)

    <span data-ttu-id="bd6ff-151">где миж являются членами Мпрож.</span><span class="sxs-lookup"><span data-stu-id="bd6ff-151">where Mij are members of Mproj.</span></span>

    <span data-ttu-id="bd6ff-152">Для ортогональной проекции:</span><span class="sxs-lookup"><span data-stu-id="bd6ff-152">For the orthogonal projection we have:</span></span>

    ![Ортогональная проекция](images/d3dxfrm63.gif)

    <span data-ttu-id="bd6ff-154">В Direct3D предполагается, что матрица проекции перспективы имеет вид:</span><span class="sxs-lookup"><span data-stu-id="bd6ff-154">Direct3D assumes that the perspective projection matrix has the form:</span></span>

    ![матрица проекции перспективы](images/d3dxfrm64.gif)

    <span data-ttu-id="bd6ff-156">Если матрица проекции перспективы не имеет такой формы, то будут присутствовать некоторые артефакты.</span><span class="sxs-lookup"><span data-stu-id="bd6ff-156">If the perspective projection matrix does not have this form, there will be some artifacts.</span></span> <span data-ttu-id="bd6ff-157">Например, таблица тумана не будет работать.</span><span class="sxs-lookup"><span data-stu-id="bd6ff-157">For example, table fog will not work.</span></span>

4.  <span data-ttu-id="bd6ff-158">Direct3D позволяет пользователю изменить громкость клипа следующим образом:</span><span class="sxs-lookup"><span data-stu-id="bd6ff-158">Direct3D allows the user to change the clip volume as follows:</span></span>

    ![изменение громкости клипа](images/d3dxfrm65.gif)

    <span data-ttu-id="bd6ff-160">Его можно переписывать следующим образом:</span><span class="sxs-lookup"><span data-stu-id="bd6ff-160">This can be rewritten as:</span></span>

    ![изменение перезаписи клипа](images/d3dxfrm66.gif)

    <span data-ttu-id="bd6ff-162">где:</span><span class="sxs-lookup"><span data-stu-id="bd6ff-162">where:</span></span>

    ``` syntax
        Cx, Cy - dvClipX, dvClipY from D3DVIEWPORT9  
        Cw, Ch - dvClipWidth, dvClipHeight from D3DVIEWPORT9  
        Zmin, Zmax - dvMinZ, dvMaxZ from D3DVIEWPORT9  
    ```

    <span data-ttu-id="bd6ff-163">Это преобразование может обеспечить повышенную точность и эквивалентно масштабированию и сдвигу тома обрезки.</span><span class="sxs-lookup"><span data-stu-id="bd6ff-163">This transformation can provide increased precision and is equivalent to scaling and shifting the clipping volume.</span></span>

    <span data-ttu-id="bd6ff-164">Соответствующая матрица Мклип:</span><span class="sxs-lookup"><span data-stu-id="bd6ff-164">The corresponding Mclip matrix is:</span></span>

    ![Матрица мклип](images/d3dxfrm67.gif)

    <span data-ttu-id="bd6ff-166">Вершина преобразуется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="bd6ff-166">A vertex is transformed by:</span></span>

    ``` syntax
        dvClipWidth = 2   
        dvClipHeight = 2   
        dvClipX = -1   
        dvClipY = 1   
        dvMinZ = 0   
        dvMaxZ = 1   
    ```

    <span data-ttu-id="bd6ff-167">Если вы не хотите масштабировать громкость клипа, можно задать для параметров окна просмотра значения по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="bd6ff-167">If you do not want to scale the clip volume, you can set viewport parameters to default values:</span></span>

    ``` syntax
        (Xc, Yc, Zc, Wc) = (Xp, Yp, Zp, Wp) * Mclip   
    ```

5.  <span data-ttu-id="bd6ff-168">Этап обрезки необязателен, если пользователь указывает \_ флаг D3DDP донотклип в вызове дравпримитиве.</span><span class="sxs-lookup"><span data-stu-id="bd6ff-168">The clipping stage is optional if the user specifies the D3DDP\_DONOTCLIP flag in a DrawPrimitive call.</span></span> <span data-ttu-id="bd6ff-169">В этом случае все матрицы (включая MVS) могут быть объединены.</span><span class="sxs-lookup"><span data-stu-id="bd6ff-169">In this case, all matrices (including Mvs) can be combined.</span></span>
6.  <span data-ttu-id="bd6ff-170">Матрица масштаба окна просмотра MVS масштабирует координаты в окне окна просмотра и переворачивает ось Y в сторону:</span><span class="sxs-lookup"><span data-stu-id="bd6ff-170">The viewport scale matrix Mvs scales coordinates to be within the viewport window and flips the Y axis from up to down:</span></span>

    ![Матрица масштаба окна просмотра MVS](images/d3dxfrm68.gif)

    <span data-ttu-id="bd6ff-172">где:</span><span class="sxs-lookup"><span data-stu-id="bd6ff-172">where:</span></span>

    ``` syntax
        dwX, dwY - viewport offsets in pixels from D3DVIEWPORT9 
        dwWidth, dwHeight - viewport width and height in pixels from D3DVIEWPORT9    
    ```

7.  <span data-ttu-id="bd6ff-173">Наконец, экранные координаты вычисляются и передаются в средство программной прорисовки:</span><span class="sxs-lookup"><span data-stu-id="bd6ff-173">Finally, screen coordinates are computed and passed to the rasterizer:</span></span>

    ![экранные координаты, вычисленные и передаваемые в средство программной прорисовки](images/d3dxfrm69.gif)

## <a name="usage-tips"></a><span data-ttu-id="bd6ff-175">Советы по использованию</span><span class="sxs-lookup"><span data-stu-id="bd6ff-175">Usage Tips</span></span>

<span data-ttu-id="bd6ff-176">Ниже приведены некоторые советы по использованию конвейера преобразования Direct3D.</span><span class="sxs-lookup"><span data-stu-id="bd6ff-176">Here are some tips for how to use the Direct3D Transformation Pipeline:</span></span>

-   <span data-ttu-id="bd6ff-177">Последний столбец мира и матрицы просмотра должны иметь значение (0, 0, 0, 1) или освещение будет неправильным.</span><span class="sxs-lookup"><span data-stu-id="bd6ff-177">The last column of the world and view matrices should be (0, 0, 0, 1), or the lighting will be incorrect.</span></span>
-   <span data-ttu-id="bd6ff-178">Задайте параметры окна просмотра для создания матрицы Мклип Identity, если только вы не понимаете, для чего она нужна.</span><span class="sxs-lookup"><span data-stu-id="bd6ff-178">Set the viewport parameters to build an identity Mclip matrix, unless you understand exactly what it is needed for.</span></span>

    ``` syntax
        dvClipWidth = 2 
        dvClipHeight = 2
        dvClipX = -1
        dvClipY = 1
        dvMinZ = 0 
        dvMaxZ = 1
    ```

 

 