---
title: Перенос матриц и функций преобразования
description: Аналогичным образом обрабатывались матрицы и преобразования IRI GL и OpenGL.
ms.assetid: 732ba65a-d776-43ea-a605-0f59209c9a46
keywords:
- Перенос GL по IRI, матрицы
- Перенос из ДИАФРАГМы в ГК, матрицы
- Перенос на OpenGL из IRI GL, матрицы
- Перенос по стандарту OpenGL из IRI GL, матрицы
- матрицы
- Перенос GL в ГК, преобразования
- Перенос из IRI GL, преобразования
- перенос в OpenGL из IRI GL, преобразования
- Перенос по стандарту OpenGL из IRI GL, преобразования
- преобразования
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1c6219640085370202b8dbebad9a2e9d4992b4f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331016"
---
# <a name="porting-matrix-and-transformation-functions"></a><span data-ttu-id="b6281-113">Перенос матриц и функций преобразования</span><span class="sxs-lookup"><span data-stu-id="b6281-113">Porting Matrix and Transformation Functions</span></span>

<span data-ttu-id="b6281-114">Аналогичным образом обрабатывались матрицы и преобразования IRI GL и OpenGL.</span><span class="sxs-lookup"><span data-stu-id="b6281-114">IRIS GL and OpenGL handle matrices and transformations in a similar manner.</span></span> <span data-ttu-id="b6281-115">Но при переносе кода из IRI GL следует учитывать несколько различий.</span><span class="sxs-lookup"><span data-stu-id="b6281-115">But there are several differences to keep in mind when porting code from IRIS GL:</span></span>

-   <span data-ttu-id="b6281-116">В OpenGL всегда используется режим двойной матрицы. режим одиночной матрицы отсутствует.</span><span class="sxs-lookup"><span data-stu-id="b6281-116">In OpenGL you are always in double-matrix mode; there is no single-matrix mode.</span></span>
-   <span data-ttu-id="b6281-117">Углы измеряются в градусах, а не десятых градусов.</span><span class="sxs-lookup"><span data-stu-id="b6281-117">Angles are measured in degrees, instead of tenths of degrees.</span></span>
-   <span data-ttu-id="b6281-118">Вызовы матриц проекции, такие как [**глфрустум**](glfrustum.md) и [**глорсо**](glortho.md), теперь умножаются на текущую матрицу, а не загружаются в текущую матрицу.</span><span class="sxs-lookup"><span data-stu-id="b6281-118">Projection matrix calls, like [**glFrustum**](glfrustum.md) and [**glOrtho**](glortho.md), now multiply onto the current matrix, instead of being loaded onto the current matrix.</span></span>
-   <span data-ttu-id="b6281-119">Функция OpenGL, [**глротате**](glrotate.md), сильно отличается от **вращения**.</span><span class="sxs-lookup"><span data-stu-id="b6281-119">The OpenGL function, [**glRotate**](glrotate.md), is very different from **rotate**.</span></span> <span data-ttu-id="b6281-120">Можно поворачивать любую произвольную ось, а не ограниченную осями x, y и z.</span><span class="sxs-lookup"><span data-stu-id="b6281-120">You can rotate around any arbitrary axis, instead of being confined to the x-, y-, and z- axes.</span></span> <span data-ttu-id="b6281-121">Например, можно перевести:</span><span class="sxs-lookup"><span data-stu-id="b6281-121">For example, you can translate:</span></span>

    ```C++
    rotate(200*(i+1), 'z');
    ```

    

    <span data-ttu-id="b6281-122">на:</span><span class="sxs-lookup"><span data-stu-id="b6281-122">to:</span></span>

    ```C++
    glRotate(.1*(200*(i+1), 0.0, 0.0, 1.0);
    ```

    

    <span data-ttu-id="b6281-123">При преобразовании из **перехода** в **глротате** вы перейдете в градусы с десятых градусов и замените "z" вектором для оси z.</span><span class="sxs-lookup"><span data-stu-id="b6281-123">When translating from **rotate** to **glRotate** you switch to degrees from tenths of degrees and replace 'z' with a vector for the z-axis.</span></span>

-   <span data-ttu-id="b6281-124">OpenGL не имеет эквивалента функции **поларвиев** .</span><span class="sxs-lookup"><span data-stu-id="b6281-124">OpenGL has no equivalent to the **polarview** function.</span></span> <span data-ttu-id="b6281-125">Его можно легко заменить с помощью перевода и трех поворотов.</span><span class="sxs-lookup"><span data-stu-id="b6281-125">You can replace it easily with a translation and three rotations.</span></span> <span data-ttu-id="b6281-126">Например, можно перевести:</span><span class="sxs-lookup"><span data-stu-id="b6281-126">For example, you can translate:</span></span>

    ```C++
    polarview(distance, azimuth, incidence, twist);
     
    ```

    

    <span data-ttu-id="b6281-127">на:</span><span class="sxs-lookup"><span data-stu-id="b6281-127">to:</span></span>

    ```C++
    glTranslatef( 0.0, 0.0, -distance); 
    glRotatef( -twist * 10.0, 0.0, 0.0, 1.0); 
    glRotatef( -incidence * 10.0, 1.0, 0.0, 0.0); 
    glRotatef( -azimuth * 10.0, 0.0, 0.0, 1.0);
    ```

    

<span data-ttu-id="b6281-128">В следующей таблице перечислены функции матрицы OpenGL и их эквивалентные функции IRI GL.</span><span class="sxs-lookup"><span data-stu-id="b6281-128">The following table lists the OpenGL matrix functions and their equivalent IRIS GL functions.</span></span>



| <span data-ttu-id="b6281-129">Функция IRI GL</span><span class="sxs-lookup"><span data-stu-id="b6281-129">IRIS GL function</span></span>              | <span data-ttu-id="b6281-130">Функция OpenGL</span><span class="sxs-lookup"><span data-stu-id="b6281-130">OpenGL function</span></span>                                                                        | <span data-ttu-id="b6281-131">Значение</span><span class="sxs-lookup"><span data-stu-id="b6281-131">Meaning</span></span>                                                                                                                                                                        |
|-------------------------------|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6281-132">**ммоде**</span><span class="sxs-lookup"><span data-stu-id="b6281-132">**mmode**</span></span>                     | [<span data-ttu-id="b6281-133">**глматриксмоде**</span><span class="sxs-lookup"><span data-stu-id="b6281-133">**glMatrixMode**</span></span>](glmatrixmode.md)                                                   | <span data-ttu-id="b6281-134">Задает текущий режим матрицы.</span><span class="sxs-lookup"><span data-stu-id="b6281-134">Sets current matrix mode.</span></span>                                                                                                                                                      |
|                               | [<span data-ttu-id="b6281-135">**гллоадидентити**</span><span class="sxs-lookup"><span data-stu-id="b6281-135">**glLoadIdentity**</span></span>](glloadidentity.md)                                               | <span data-ttu-id="b6281-136">Заменяет текущую матрицу матрицей идентификаторов.</span><span class="sxs-lookup"><span data-stu-id="b6281-136">Replaces current matrix with the identity matrix.</span></span>                                                                                                                              |
| <span data-ttu-id="b6281-137">**лоадматрикс**</span><span class="sxs-lookup"><span data-stu-id="b6281-137">**loadmatrix**</span></span>                | <span data-ttu-id="b6281-138">[**гллоадматриксф**](glloadmatrix.md),[**гллоадматриксд**](glloadmatrix.md)</span><span class="sxs-lookup"><span data-stu-id="b6281-138">[**glLoadMatrixf**](glloadmatrix.md),[**glLoadMatrixd**](glloadmatrix.md)</span></span><br/> | <span data-ttu-id="b6281-139">Заменяет текущую матрицу указанной матрицей.</span><span class="sxs-lookup"><span data-stu-id="b6281-139">Replaces current matrix with the specified matrix.</span></span>                                                                                                                             |
| <span data-ttu-id="b6281-140">**мултматрикс**</span><span class="sxs-lookup"><span data-stu-id="b6281-140">**multmatrix**</span></span>                | <span data-ttu-id="b6281-141">[**глмултматриксф**](glmultmatrix.md),[**глмултматриксд**](glmultmatrix.md)</span><span class="sxs-lookup"><span data-stu-id="b6281-141">[**glMultMatrixf**](glmultmatrix.md),[**glMultMatrixd**](glmultmatrix.md)</span></span><br/> | <span data-ttu-id="b6281-142">После этого производится умножение текущей матрицы на указанную матрицу (Обратите внимание, что **мултматрикс** предварительно умножается).</span><span class="sxs-lookup"><span data-stu-id="b6281-142">Post-multiplies current matrix with the specified matrix (note that **multmatrix** pre-multiplied).</span></span>                                                                            |
| <span data-ttu-id="b6281-143">**МАПВ**, **mapw2**</span><span class="sxs-lookup"><span data-stu-id="b6281-143">**mapw**, **mapw2**</span></span>           | [<span data-ttu-id="b6281-144">**глуунпрожект**</span><span class="sxs-lookup"><span data-stu-id="b6281-144">**gluUnProject**</span></span>](gluunproject.md)                                                   | <span data-ttu-id="b6281-145">Проецирует координаты мирового пространства в объектное пространство (см. также [**глупрожект**](gluproject.md)).</span><span class="sxs-lookup"><span data-stu-id="b6281-145">Projects world-space coordinates to object space (see also [**gluProject**](gluproject.md)).</span></span>                                                                                  |
| <span data-ttu-id="b6281-146">**орсо**</span><span class="sxs-lookup"><span data-stu-id="b6281-146">**ortho**</span></span>                     | [<span data-ttu-id="b6281-147">**глорсо**</span><span class="sxs-lookup"><span data-stu-id="b6281-147">**glOrtho**</span></span>](glortho.md)                                                             | <span data-ttu-id="b6281-148">Умножает текущую матрицу на ортогональную матрицу проекции.</span><span class="sxs-lookup"><span data-stu-id="b6281-148">Multiplies current matrix by an orthographic projection matrix.</span></span>                                                                                                                |
| <span data-ttu-id="b6281-149">**ortho2**</span><span class="sxs-lookup"><span data-stu-id="b6281-149">**ortho2**</span></span>                    | [<span data-ttu-id="b6281-150">**gluOrtho2D**</span><span class="sxs-lookup"><span data-stu-id="b6281-150">**gluOrtho2D**</span></span>](gluortho2d.md)                                                       | <span data-ttu-id="b6281-151">Определяет матрицу двухмерной ортогональной проекции.</span><span class="sxs-lookup"><span data-stu-id="b6281-151">Defines a two-dimensional orthographic projection matrix.</span></span>                                                                                                                      |
| <span data-ttu-id="b6281-152">**перспектив**</span><span class="sxs-lookup"><span data-stu-id="b6281-152">**perspective**</span></span>               | [<span data-ttu-id="b6281-153">**глуперспективе**</span><span class="sxs-lookup"><span data-stu-id="b6281-153">**gluPerspective**</span></span>](gluperspective.md)                                               | <span data-ttu-id="b6281-154">Определяет матрицу проекции перспективы.</span><span class="sxs-lookup"><span data-stu-id="b6281-154">Defines a perspective projection matrix.</span></span>                                                                                                                                       |
| <span data-ttu-id="b6281-155">**пикксизе**</span><span class="sxs-lookup"><span data-stu-id="b6281-155">**picksize**</span></span>                  | [<span data-ttu-id="b6281-156">**глупиккматрикс**</span><span class="sxs-lookup"><span data-stu-id="b6281-156">**gluPickMatrix**</span></span>](glupickmatrix.md)                                                 | <span data-ttu-id="b6281-157">Определяет регион комплектации.</span><span class="sxs-lookup"><span data-stu-id="b6281-157">Defines a picking region.</span></span>                                                                                                                                                      |
| <span data-ttu-id="b6281-158">**попматрикс**</span><span class="sxs-lookup"><span data-stu-id="b6281-158">**popmatrix**</span></span>                 | [<span data-ttu-id="b6281-159">**глпопматрикс**</span><span class="sxs-lookup"><span data-stu-id="b6281-159">**glPopMatrix**</span></span>](glpopmatrix.md)                                                     | <span data-ttu-id="b6281-160">Выводит текущий стек матриц, заменяя текущую матрицу на ту, которая находится под ней.</span><span class="sxs-lookup"><span data-stu-id="b6281-160">Pops current matrix stack, replacing the current matrix with the one below it.</span></span>                                                                                                 |
| <span data-ttu-id="b6281-161">**пушматрикс**</span><span class="sxs-lookup"><span data-stu-id="b6281-161">**pushmatrix**</span></span>                | [<span data-ttu-id="b6281-162">**глпушматрикс**</span><span class="sxs-lookup"><span data-stu-id="b6281-162">**glPushMatrix**</span></span>](glpushmatrix.md)                                                   | <span data-ttu-id="b6281-163">Помещает текущую матрицу в стек по одному, дублируют текущую матрицу.</span><span class="sxs-lookup"><span data-stu-id="b6281-163">Pushes current matrix stack down by one, duplicating the current matrix.</span></span>                                                                                                       |
| <span data-ttu-id="b6281-164">**вращение**,**ROT**</span><span class="sxs-lookup"><span data-stu-id="b6281-164">**rotate**,**rot**</span></span><br/> | <span data-ttu-id="b6281-165">[**глротатед**](glrotate.md),[**глротатеф**](glrotate.md)</span><span class="sxs-lookup"><span data-stu-id="b6281-165">[**glRotated**](glrotate.md),[**glRotatef**](glrotate.md)</span></span><br/>                 | <span data-ttu-id="b6281-166">Поворачивает текущую систему координат на заданный угол относительно вектора от начала до заданной точки.</span><span class="sxs-lookup"><span data-stu-id="b6281-166">Rotates current coordinate system by the given angle about the vector from the origin through the given point.</span></span> <span data-ttu-id="b6281-167">Обратите **внимание, что поворот** поворачивается только относительно осей x, y и z.</span><span class="sxs-lookup"><span data-stu-id="b6281-167">Note that **rotate** rotated only about the x-, y-, and z-axes.</span></span> |
| <span data-ttu-id="b6281-168">**масштаб**</span><span class="sxs-lookup"><span data-stu-id="b6281-168">**scale**</span></span>                     | <span data-ttu-id="b6281-169">[**глскалед**](glscale.md),[**глскалеф**](glscale.md)</span><span class="sxs-lookup"><span data-stu-id="b6281-169">[**glScaled**](glscale.md),[**glScalef**](glscale.md)</span></span><br/>                     | <span data-ttu-id="b6281-170">Умножает текущую матрицу на матрицу масштабирования.</span><span class="sxs-lookup"><span data-stu-id="b6281-170">Multiplies current matrix by a scaling matrix.</span></span>                                                                                                                                 |
| <span data-ttu-id="b6281-171">**Перевести**</span><span class="sxs-lookup"><span data-stu-id="b6281-171">**translate**</span></span>                 | <span data-ttu-id="b6281-172">[**глтранслатеф**](gltranslate.md),[**глтранслатед**](gltranslate.md)</span><span class="sxs-lookup"><span data-stu-id="b6281-172">[**glTranslatef**](gltranslate.md),[**glTranslated**](gltranslate.md)</span></span><br/>     | <span data-ttu-id="b6281-173">Перемещает источник системы координат на указанную точку путем умножения текущей матрицы на матрицу перевода.</span><span class="sxs-lookup"><span data-stu-id="b6281-173">Moves coordinate-system origin to the point specified, by multiplying the current matrix by a translation matrix.</span></span>                                                              |
| <span data-ttu-id="b6281-174">**окно**</span><span class="sxs-lookup"><span data-stu-id="b6281-174">**window**</span></span>                    | [<span data-ttu-id="b6281-175">**глфрустум**</span><span class="sxs-lookup"><span data-stu-id="b6281-175">**glFrustum**</span></span>](glfrustum.md)                                                         | <span data-ttu-id="b6281-176">При заданных координатах для обтравочных плоскостей текущая матрица умножается на матрицу перспективы.</span><span class="sxs-lookup"><span data-stu-id="b6281-176">Given coordinates for clipping planes, multiplies the current matrix by a perspective matrix.</span></span>                                                                                  |



 

<span data-ttu-id="b6281-177">OpenGL имеет три режима матрицы, которые задаются с помощью [**глматриксмоде**](glmatrixmode.md).</span><span class="sxs-lookup"><span data-stu-id="b6281-177">OpenGL has three matrix modes, which are set with [**glMatrixMode**](glmatrixmode.md).</span></span> <span data-ttu-id="b6281-178">В следующей таблице перечислены режимы, доступные в качестве параметров для **глматриксмоде**.</span><span class="sxs-lookup"><span data-stu-id="b6281-178">The following table lists the modes available as parameters for **glMatrixMode**.</span></span>



| <span data-ttu-id="b6281-179">Режим матрицы IRI GL</span><span class="sxs-lookup"><span data-stu-id="b6281-179">IRIS GL matrix mode</span></span> | <span data-ttu-id="b6281-180">Режим OpenGL</span><span class="sxs-lookup"><span data-stu-id="b6281-180">OpenGL mode</span></span>    | <span data-ttu-id="b6281-181">Значение</span><span class="sxs-lookup"><span data-stu-id="b6281-181">Meaning</span></span>                                  | <span data-ttu-id="b6281-182">Минимальная глубина стека</span><span class="sxs-lookup"><span data-stu-id="b6281-182">Min stack depth</span></span> |
|---------------------|----------------|------------------------------------------|-----------------|
| <span data-ttu-id="b6281-183">**мтекстуре**</span><span class="sxs-lookup"><span data-stu-id="b6281-183">**MTEXTURE**</span></span>        | <span data-ttu-id="b6281-184">\_текстура GL</span><span class="sxs-lookup"><span data-stu-id="b6281-184">GL\_TEXTURE</span></span>    | <span data-ttu-id="b6281-185">Работает с стеком матрицы текстур.</span><span class="sxs-lookup"><span data-stu-id="b6281-185">Operates on the texture matrix stack.</span></span>    | <span data-ttu-id="b6281-186">2</span><span class="sxs-lookup"><span data-stu-id="b6281-186">2</span></span>               |
| <span data-ttu-id="b6281-187">**мвиевинг**</span><span class="sxs-lookup"><span data-stu-id="b6281-187">**MVIEWING**</span></span>        | <span data-ttu-id="b6281-188">\_МОДЕЛВИЕВ GL</span><span class="sxs-lookup"><span data-stu-id="b6281-188">GL\_MODELVIEW</span></span>  | <span data-ttu-id="b6281-189">Работает с стеком матриц представления модели.</span><span class="sxs-lookup"><span data-stu-id="b6281-189">Operates on the model view matrix stack.</span></span> | <span data-ttu-id="b6281-190">32</span><span class="sxs-lookup"><span data-stu-id="b6281-190">32</span></span>              |
| <span data-ttu-id="b6281-191">**мпрожектион**</span><span class="sxs-lookup"><span data-stu-id="b6281-191">**MPROJECTION**</span></span>     | <span data-ttu-id="b6281-192">\_ПРОЕКЦИЯ GL</span><span class="sxs-lookup"><span data-stu-id="b6281-192">GL\_PROJECTION</span></span> | <span data-ttu-id="b6281-193">Работает в стеке матрицы проекции.</span><span class="sxs-lookup"><span data-stu-id="b6281-193">Operates on the projection matrix stack.</span></span> | <span data-ttu-id="b6281-194">2</span><span class="sxs-lookup"><span data-stu-id="b6281-194">2</span></span>               |



 

 

 





