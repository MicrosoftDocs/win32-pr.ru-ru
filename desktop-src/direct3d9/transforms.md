---
description: Компонент Direct3D, перемещающий геометрию через фиксированный конвейер функциональной геометрии, называется модулем преобразования.
ms.assetid: ed52e32f-8fae-4e6f-b908-26e05ce940cc
title: Преобразования (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f482ef12c88140c2eff4c61e634fd3297aeaf295
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104423149"
---
# <a name="transforms-direct3d-9"></a><span data-ttu-id="06416-103">Преобразования (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="06416-103">Transforms (Direct3D 9)</span></span>

<span data-ttu-id="06416-104">Компонент Direct3D, перемещающий геометрию через фиксированный конвейер функциональной геометрии, называется модулем преобразования.</span><span class="sxs-lookup"><span data-stu-id="06416-104">The part of Direct3D that pushes geometry through the fixed function geometry pipeline is the transform engine.</span></span> <span data-ttu-id="06416-105">Он находит модель и смотрящего в реальном мире, проецирует вершины для отображения на экране и обрезает вершины в окне просмотра.</span><span class="sxs-lookup"><span data-stu-id="06416-105">It locates the model and viewer in the world, projects vertices for display on the screen, and clips vertices to the viewport.</span></span> <span data-ttu-id="06416-106">Модуль преобразования также выполняет вычисления освещения, чтобы определить рассеянные и зеркальные компоненты в каждой вершине.</span><span class="sxs-lookup"><span data-stu-id="06416-106">The transform engine also performs lighting computations to determine diffuse and specular components at each vertex.</span></span>

<span data-ttu-id="06416-107">Геометрический конвейер принимает вершины в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="06416-107">The geometry pipeline takes vertices as input.</span></span> <span data-ttu-id="06416-108">Модуль преобразований применяет к вершинам мировое, видовое и проекционное преобразования, кадрирует результат и передает все в средство программной прорисовки.</span><span class="sxs-lookup"><span data-stu-id="06416-108">The transform engine applies the world, view, and projection transforms to the vertices, clips the result, and passes everything to the rasterizer.</span></span>

<span data-ttu-id="06416-109">В начале конвейера вершины модели объявлены относительно локальной системы координат.</span><span class="sxs-lookup"><span data-stu-id="06416-109">At the head of the pipeline, a model's vertices are declared relative to a local coordinate system.</span></span> <span data-ttu-id="06416-110">Локальная система координат — это локальное начало координат и ориентация.</span><span class="sxs-lookup"><span data-stu-id="06416-110">This is a local origin and an orientation.</span></span> <span data-ttu-id="06416-111">Такая ориентация координат часто называется пространством модели, а отдельные координаты называются координатами модели.</span><span class="sxs-lookup"><span data-stu-id="06416-111">This orientation of coordinates is often referred to as model space, and individual coordinates are called model coordinates.</span></span>

<span data-ttu-id="06416-112">Первый этап геометрического конвейера преобразует вершины модели из их локальной системы координат в систему координат, используемую всеми объектами в сцене.</span><span class="sxs-lookup"><span data-stu-id="06416-112">The first stage of the geometry pipeline transforms a model's vertices from their local coordinate system to a coordinate system that is used by all the objects in a scene.</span></span> <span data-ttu-id="06416-113">Процесс переориентации вершин называется универсальным преобразованием.</span><span class="sxs-lookup"><span data-stu-id="06416-113">The process of reorienting the vertices is called the world transform.</span></span> <span data-ttu-id="06416-114">Эта новая ориентация обычно называется мировым пространством, а каждая вершина в мировом пространстве объявляется с помощью координат мира.</span><span class="sxs-lookup"><span data-stu-id="06416-114">This new orientation is commonly referred to as world space, and each vertex in world space is declared using world coordinates.</span></span>

<span data-ttu-id="06416-115">На следующем этапе вершины, которые описывают ваш трехмерный мир, ориентируются по отношению к камере.</span><span class="sxs-lookup"><span data-stu-id="06416-115">In the next stage, the vertices that describe your 3D world are oriented with respect to a camera.</span></span> <span data-ttu-id="06416-116">Это значит, что приложение выбирает точку зрения для сцены, а координаты мирового пространства перемещаются и поворачиваются вокруг представления камеры, преобразуя мировое пространство в область камеры.</span><span class="sxs-lookup"><span data-stu-id="06416-116">That is, your application chooses a point-of-view for the scene, and world space coordinates are relocated and rotated around the camera's view, turning world space into camera space.</span></span> <span data-ttu-id="06416-117">Это преобразование представления.</span><span class="sxs-lookup"><span data-stu-id="06416-117">This is the view transform.</span></span>

<span data-ttu-id="06416-118">Следующим этапом является преобразование проекции.</span><span class="sxs-lookup"><span data-stu-id="06416-118">The next stage is the projection transform.</span></span> <span data-ttu-id="06416-119">В этой части конвейера объекты, как правило, масштабируются по отношению к их расстоянию от средства просмотра, чтобы дать иллюзию глубины сцены. Закрытые объекты будут выглядеть больше, чем удаленные объекты, и т. д.</span><span class="sxs-lookup"><span data-stu-id="06416-119">In this part of the pipeline, objects are usually scaled with relation to their distance from the viewer in order to give the illusion of depth to a scene; close objects are made to appear larger than distant objects, and so on.</span></span> <span data-ttu-id="06416-120">С целью упрощения в этой документации пространство, в котором существуют вершины после проекционного преобразования, называется проекционным пространством.</span><span class="sxs-lookup"><span data-stu-id="06416-120">For simplicity, this documentation refers to the space in which vertices exist after the projection transform as projection space.</span></span> <span data-ttu-id="06416-121">В некоторых книгах по графике проекционное пространство может называться постперспективным однородным пространством.</span><span class="sxs-lookup"><span data-stu-id="06416-121">Some graphics books might refer to projection space as post-perspective homogeneous space.</span></span> <span data-ttu-id="06416-122">Не все проекционные преобразования обеспечивают масштабирование размера объектов в сцене.</span><span class="sxs-lookup"><span data-stu-id="06416-122">Not all projection transforms scale the size of objects in a scene.</span></span> <span data-ttu-id="06416-123">Такая проекция иногда называется аффинной или ортогональной проекцией.</span><span class="sxs-lookup"><span data-stu-id="06416-123">A projection such as this is sometimes called an affine or orthogonal projection.</span></span>

<span data-ttu-id="06416-124">На последнем этапе конвейера все вершины, которые не будут видны на экране, удаляются, чтобы средство программной прорисовки не тратило время на вычисление цветов и затенения для того, что никто не увидит.</span><span class="sxs-lookup"><span data-stu-id="06416-124">In the final part of the pipeline, any vertices that will not be visible on the screen are removed, so that the rasterizer doesn't take the time to calculate the colors and shading for something that will never be seen.</span></span> <span data-ttu-id="06416-125">Этот процесс называется кадрированием.</span><span class="sxs-lookup"><span data-stu-id="06416-125">This process is called clipping.</span></span> <span data-ttu-id="06416-126">После кадрирования оставшиеся вершины масштабируются в соответствии с параметрами окна просмотра и преобразуются в экранные координаты.</span><span class="sxs-lookup"><span data-stu-id="06416-126">After clipping, the remaining vertices are scaled according to the viewport parameters and converted into screen coordinates.</span></span> <span data-ttu-id="06416-127">Итоговые вершины, отображаемые на экране после растеризации стены, существуют в экранном пространстве.</span><span class="sxs-lookup"><span data-stu-id="06416-127">The resulting vertices, seen on the screen when the scene is rasterized, exist in screen space.</span></span>

<span data-ttu-id="06416-128">Преобразования используются для преобразования геометрии объектов из одного пространства координат в другое.</span><span class="sxs-lookup"><span data-stu-id="06416-128">Transforms are used to convert object geometry from one coordinate space to another.</span></span> <span data-ttu-id="06416-129">В Direct3D для 3D-преобразований используются матрицы.</span><span class="sxs-lookup"><span data-stu-id="06416-129">Direct3D uses matrices to perform 3D transforms.</span></span> <span data-ttu-id="06416-130">В этом разделе объясняется, как матрицы создают трехмерные преобразования, описаны некоторые распространенные способы использования преобразований и сведения о том, как можно объединить матрицы для создания одной матрицы, охватывающей несколько преобразований.</span><span class="sxs-lookup"><span data-stu-id="06416-130">This section explains how matrices create 3D transforms, describes some common uses for transforms, and details how you can combine matrices to produce a single matrix that encompasses multiple transforms.</span></span>

-   <span data-ttu-id="06416-131">[Преобразование мира (Direct3D 9)](world-transform.md) — преобразование из пространства модели в мировое пространство</span><span class="sxs-lookup"><span data-stu-id="06416-131">[World Transform (Direct3D 9)](world-transform.md) - convert from model space to world space</span></span>
-   <span data-ttu-id="06416-132">[Преобразование представления (Direct3D 9)](view-transform.md) — преобразование из универсального пространства в область просмотра</span><span class="sxs-lookup"><span data-stu-id="06416-132">[View Transform (Direct3D 9)](view-transform.md) - convert from world space to view space</span></span>
-   <span data-ttu-id="06416-133">[Преобразование проекции (Direct3D 9)](projection-transform.md) — преобразование из пространства представления в пространство проекции</span><span class="sxs-lookup"><span data-stu-id="06416-133">[Projection Transform (Direct3D 9)](projection-transform.md) - convert from view space to projection space</span></span>

## <a name="matrix-transforms"></a><span data-ttu-id="06416-134">Преобразования матрицы</span><span class="sxs-lookup"><span data-stu-id="06416-134">Matrix Transforms</span></span>

<span data-ttu-id="06416-135">В приложениях, работающих с 3D-графикой, с помощью геометрических преобразований можно:</span><span class="sxs-lookup"><span data-stu-id="06416-135">In applications that work with 3D graphics, you can use geometrical transforms to do the following:</span></span>

-   <span data-ttu-id="06416-136">выражать местоположение одного объекта относительного другого объекта;</span><span class="sxs-lookup"><span data-stu-id="06416-136">Express the location of an object relative to another object.</span></span>
-   <span data-ttu-id="06416-137">поворачивать объекты и задавать их размер;</span><span class="sxs-lookup"><span data-stu-id="06416-137">Rotate and size objects.</span></span>
-   <span data-ttu-id="06416-138">менять позиции наблюдателя, направления и перспективы.</span><span class="sxs-lookup"><span data-stu-id="06416-138">Change viewing positions, directions, and perspectives.</span></span>

<span data-ttu-id="06416-139">Любую точку (X,Y,Z) можно преобразовать в другую точку (X', Y', Z') с помощью матрицы 4x4, как показано в следующем уравнении.</span><span class="sxs-lookup"><span data-stu-id="06416-139">You can transform any point (x,y,z) into another point (x', y', z') by using a 4x4 matrix, as shown in the following equation.</span></span>

![уравнение для преобразования любой точки в другую точку](images/matmult.png)

<span data-ttu-id="06416-141">Примените следующие уравнения к (X, Y, Z) и матрице для получения точки (X', Y', Z').</span><span class="sxs-lookup"><span data-stu-id="06416-141">Perform the following equations on (x, y, z) and the matrix to produce the point (x', y', z').</span></span>

![уравнения для новой точки](images/matexpnd.png)

<span data-ttu-id="06416-143">Наиболее распространенные преобразования — это параллельный перенос, поворот и масштабирование.</span><span class="sxs-lookup"><span data-stu-id="06416-143">The most common transforms are translation, rotation, and scaling.</span></span> <span data-ttu-id="06416-144">Можно объединить матрицы, которые обеспечивают эти эффекты, в одну матрицу и вычислять сразу несколько преобразований.</span><span class="sxs-lookup"><span data-stu-id="06416-144">You can combine the matrices that produce these effects into a single matrix to calculate several transforms at once.</span></span> <span data-ttu-id="06416-145">Например, можно построить единую матрицу для параллельного переноса и поворота серии точек.</span><span class="sxs-lookup"><span data-stu-id="06416-145">For example, you can build a single matrix to translate and rotate a series of points.</span></span>

<span data-ttu-id="06416-146">Матрицы записываются в порядке строка-столбец.</span><span class="sxs-lookup"><span data-stu-id="06416-146">Matrices are written in row-column order.</span></span> <span data-ttu-id="06416-147">Матрица, которая равномерно масштабирует вершины вдоль каждой оси — так называемое пропорциональное масштабирование — в математической записи будет представлена следующей матрицей.</span><span class="sxs-lookup"><span data-stu-id="06416-147">A matrix that evenly scales vertices along each axis, known as uniform scaling, is represented by the following matrix using mathematical notation.</span></span>

![уравнение матрицы для пропорционального масштабирования](images/matrix.png)

<span data-ttu-id="06416-149">В C++ Direct3D объявляет матрицы как двухмерный массив, используя структуру [**D3DMATRIX**](d3dmatrix.md) .</span><span class="sxs-lookup"><span data-stu-id="06416-149">In C++, Direct3D declares matrices as a two-dimensional array, using the [**D3DMATRIX**](d3dmatrix.md) structure.</span></span> <span data-ttu-id="06416-150">В следующем примере показано, как инициализировать структуру **D3DMATRIX** , чтобы она действовала как матрица равномерного масштабирования.</span><span class="sxs-lookup"><span data-stu-id="06416-150">The following example shows how to initialize a **D3DMATRIX** structure to act as a uniform scaling matrix.</span></span>


```
// In this example, s is a variable of type float.

D3DMATRIX scale = {
    s,               0.0f,            0.0f,            0.0f,
    0.0f,            s,               0.0f,            0.0f,
    0.0f,            0.0f,            s,               0.0f,
    0.0f,            0.0f,            0.0f,            1.0f
};
```



## <a name="translate"></a><span data-ttu-id="06416-151">Перевод</span><span class="sxs-lookup"><span data-stu-id="06416-151">Translate</span></span>

<span data-ttu-id="06416-152">Следующее уравнение параллельно переносит точку (X, Y, Z) в новую точку (X', Y', Z').</span><span class="sxs-lookup"><span data-stu-id="06416-152">The following equation translates the point (x, y, z) to a new point (x', y', z').</span></span>

![уравнение матрицы параллельного переноса для получения новой точки](images/transl8.png)

<span data-ttu-id="06416-154">Матрицу параллельного переноса можно вручную создать в C++.</span><span class="sxs-lookup"><span data-stu-id="06416-154">You can manually create a translation matrix in C++.</span></span> <span data-ttu-id="06416-155">В следующем примере показан исходный код для функции, которая создает матрицу для параллельного переноса вершин.</span><span class="sxs-lookup"><span data-stu-id="06416-155">The following example shows the source code for a function that creates a matrix to translate vertices.</span></span>


```
D3DXMATRIX Translate(const float dx, const float dy, const float dz) {
    D3DXMATRIX ret;

    D3DXMatrixIdentity(&ret);
    ret(3, 0) = dx;
    ret(3, 1) = dy;
    ret(3, 2) = dz;
    return ret;
}    // End of Translate
```



<span data-ttu-id="06416-156">Для удобства библиотека служебной программы D3DX предоставляет функцию [**D3DXMatrixTranslation**](d3dxmatrixtranslation.md) .</span><span class="sxs-lookup"><span data-stu-id="06416-156">For convenience, the D3DX utility library supplies the [**D3DXMatrixTranslation**](d3dxmatrixtranslation.md) function.</span></span>

## <a name="scale"></a><span data-ttu-id="06416-157">Масштабирование</span><span class="sxs-lookup"><span data-stu-id="06416-157">Scale</span></span>

<span data-ttu-id="06416-158">Следующее уравнение масштабирует точку (X, Y, Z) на произвольные значения в направлениях (X, Y, Z) для получения новой точки (X', Y', Z').</span><span class="sxs-lookup"><span data-stu-id="06416-158">The following equation scales the point (x, y, z) by arbitrary values in the x-, y-, and z-directions to a new point (x', y', z').</span></span>

![уравнение матрицы масштабирования для получения новой точки](images/matscale.png)

## <a name="rotate"></a><span data-ttu-id="06416-160">Rotate</span><span class="sxs-lookup"><span data-stu-id="06416-160">Rotate</span></span>

<span data-ttu-id="06416-161">Описанные здесь преобразования предназначены для левовинтовых систем координат и, следовательно, могут отличаться от матриц преобразования, которые встречались вам где-либо еще.</span><span class="sxs-lookup"><span data-stu-id="06416-161">The transforms described here are for left-handed coordinate systems, and so may be different from transform matrices that you have seen elsewhere.</span></span>

<span data-ttu-id="06416-162">Следующее уравнение поворачивает точку (X, Y, Z) вокруг оси X для получения новой точки (X', Y', Z').</span><span class="sxs-lookup"><span data-stu-id="06416-162">The following equation rotates the point (x, y, z) around the x-axis, producing a new point (x', y', z').</span></span>

![уравнение матрицы поворота вокруг оси X для получения новой точки](images/matxrot.png)

<span data-ttu-id="06416-164">Следующее уравнение поворачивает точку вокруг оси Y.</span><span class="sxs-lookup"><span data-stu-id="06416-164">The following equation rotates the point around the y-axis.</span></span>

![уравнение матрицы поворота вокруг оси Y для получения новой точки](images/matyrot.png)

<span data-ttu-id="06416-166">Следующее уравнение поворачивает точку вокруг оси Z.</span><span class="sxs-lookup"><span data-stu-id="06416-166">The following equation rotates the point around the z-axis.</span></span>

![уравнение матрицы поворота вокруг оси Z для получения новой точки](images/matzrot.png)

<span data-ttu-id="06416-168">В этих примерах матриц греческой буквой тета обозначен угол поворота в радианах.</span><span class="sxs-lookup"><span data-stu-id="06416-168">In these example matrices, the Greek letter theta stands for the angle of rotation, in radians.</span></span> <span data-ttu-id="06416-169">Углы измеряются по часовой стрелке, если смотреть вдоль оси поворота в направлении начала координат.</span><span class="sxs-lookup"><span data-stu-id="06416-169">Angles are measured clockwise when looking along the rotation axis toward the origin.</span></span>

<span data-ttu-id="06416-170">В приложении C++ используйте функции [**D3DXMatrixRotationX**](d3dxmatrixrotationx.md), [**D3DXMatrixRotationY**](d3dxmatrixrotationy.md)и [**D3DXMatrixRotationZ**](d3dxmatrixrotationz.md) , предоставляемые библиотекой служебной программы D3DX, для создания матриц вращения.</span><span class="sxs-lookup"><span data-stu-id="06416-170">In a C++ application, use the [**D3DXMatrixRotationX**](d3dxmatrixrotationx.md), [**D3DXMatrixRotationY**](d3dxmatrixrotationy.md), and [**D3DXMatrixRotationZ**](d3dxmatrixrotationz.md) functions supplied by the D3DX utility library to create rotation matrices.</span></span> <span data-ttu-id="06416-171">Ниже приведен код для функции **D3DXMatrixRotationX** .</span><span class="sxs-lookup"><span data-stu-id="06416-171">The following is the code for the **D3DXMatrixRotationX** function.</span></span>


```
D3DXMATRIX* WINAPI D3DXMatrixRotationX
    ( D3DXMATRIX *pOut, float angle )
{
#if DBG
    if(!pOut)
        return NULL;
#endif

    float sin, cos;
    sincosf(angle, &sin, &cos);  // Determine sin and cos of angle

    pOut->_11 = 1.0f; pOut->_12 =  0.0f;   pOut->_13 = 0.0f; pOut->_14 = 0.0f;
    pOut->_21 = 0.0f; pOut->_22 =  cos;    pOut->_23 = sin;  pOut->_24 = 0.0f;
    pOut->_31 = 0.0f; pOut->_32 = -sin;    pOut->_33 = cos;  pOut->_34 = 0.0f;
    pOut->_41 = 0.0f; pOut->_42 =  0.0f;   pOut->_43 = 0.0f; pOut->_44 = 1.0f;

    return pOut;
}
```



## <a name="concatenating-matrices"></a><span data-ttu-id="06416-172">Конкатенация матриц</span><span class="sxs-lookup"><span data-stu-id="06416-172">Concatenating Matrices</span></span>

<span data-ttu-id="06416-173">Одним из преимуществ использования матриц является то, что эффекты двух или нескольких матриц можно объединить путем перемножения этих матриц.</span><span class="sxs-lookup"><span data-stu-id="06416-173">One advantage of using matrices is that you can combine the effects of two or more matrices by multiplying them.</span></span> <span data-ttu-id="06416-174">Это означает, что для поворота модели и последующего ее параллельного переноса в какое-либо место не нужно применять две матрицы.</span><span class="sxs-lookup"><span data-stu-id="06416-174">This means that, to rotate a model and then translate it to some location, you don't need to apply two matrices.</span></span> <span data-ttu-id="06416-175">Вместо этого необходимо перемножить матрицы поворота и параллельного переноса для получения составной матрицы, содержащей все их эффекты.</span><span class="sxs-lookup"><span data-stu-id="06416-175">Instead, you multiply the rotation and translation matrices to produce a composite matrix that contains all their effects.</span></span> <span data-ttu-id="06416-176">Этот процесс называется конкатенацией матриц и может описываться следующим уравнением.</span><span class="sxs-lookup"><span data-stu-id="06416-176">This process, called matrix concatenation, can be written with the following equation.</span></span>

![уравнение конкатенации матриц](images/matrxcat.png)

<span data-ttu-id="06416-178">В этом уравнении C — создаваемая составная матрица, а M₁ – Mₙ — отдельные матрицы.</span><span class="sxs-lookup"><span data-stu-id="06416-178">In this equation, C is the composite matrix being created, and M₁ through Mₙ are the individual matrices.</span></span> <span data-ttu-id="06416-179">В большинстве случаев объединяют только две или три матрицы, однако на самом деле их количество не ограничено.</span><span class="sxs-lookup"><span data-stu-id="06416-179">In most cases, only two or three matrices are concatenated, but there is no limit.</span></span>

<span data-ttu-id="06416-180">Чтобы выполнить умножение матрицы, используйте функцию [**D3DXMatrixMultiply**](d3dxmatrixmultiply.md) .</span><span class="sxs-lookup"><span data-stu-id="06416-180">Use the [**D3DXMatrixMultiply**](d3dxmatrixmultiply.md) function to perform matrix multiplication.</span></span>

<span data-ttu-id="06416-181">Порядок, в котором выполняется перемножение матриц, имеет решающее значение.</span><span class="sxs-lookup"><span data-stu-id="06416-181">The order in which the matrix multiplication is performed is crucial.</span></span> <span data-ttu-id="06416-182">Приведенная выше формула отражает правило конкатенации матриц "слева направо".</span><span class="sxs-lookup"><span data-stu-id="06416-182">The preceding formula reflects the left-to-right rule of matrix concatenation.</span></span> <span data-ttu-id="06416-183">Это значит, что визуальные эффекты матриц, используемых для создания составной матрицы, имеют место в порядке слева направо.</span><span class="sxs-lookup"><span data-stu-id="06416-183">That is, the visible effects of the matrices that you use to create a composite matrix occur in left-to-right order.</span></span> <span data-ttu-id="06416-184">В следующем примере показана типичная мировая матрица.</span><span class="sxs-lookup"><span data-stu-id="06416-184">A typical world matrix is shown in the following example.</span></span> <span data-ttu-id="06416-185">Предположим, вы создаете мировую матрицу для классической летающей тарелки.</span><span class="sxs-lookup"><span data-stu-id="06416-185">Imagine that you are creating the world matrix for a stereotypical flying saucer.</span></span> <span data-ttu-id="06416-186">Наверное, имеет смысл вращать летающую тарелку вокруг ее центра — оси Y модельного пространства — и параллельно переносить ее в какое-либо другое место в сцене.</span><span class="sxs-lookup"><span data-stu-id="06416-186">You would probably want to spin the flying saucer around its center - the y-axis of model space - and translate it to some other location in your scene.</span></span> <span data-ttu-id="06416-187">Для достижения этого эффекта необходимо сначала создать матрицу поворота, а затем умножить ее на матрицу параллельного переноса, как показано в следующем уравнении.</span><span class="sxs-lookup"><span data-stu-id="06416-187">To accomplish this effect, you first create a rotation matrix, and then multiply it by a translation matrix, as shown in the following equation.</span></span>

![уравнения вращения, основанное на матрице поворота и матрице параллельного переноса](images/wrldexpl.png)

<span data-ttu-id="06416-189">В этой формуле R<sub>y</sub> — это матрица для поворота вокруг оси Y, а T<sub>w</sub> — это параллельный перенос в некоторую точку в мировых координатах.</span><span class="sxs-lookup"><span data-stu-id="06416-189">In this formula, R<sub>y</sub> is a matrix for rotation about the y-axis, and T<sub>w</sub> is a translation to some position in world coordinates.</span></span>

<span data-ttu-id="06416-190">Порядок, в котором перемножаются матрицы, имеет значение, потому что, в отличие от умножения двух скалярных значений, умножение матриц не является коммутативным.</span><span class="sxs-lookup"><span data-stu-id="06416-190">The order in which you multiply the matrices is important because, unlike multiplying two scalar values, matrix multiplication is not commutative.</span></span> <span data-ttu-id="06416-191">Перемножение матриц в обратном порядке будет производить визуальный эффект параллельного переноса летающей тарелки в ее положение в мировом пространстве, а затем ее поворота вокруг мирового начала координат.</span><span class="sxs-lookup"><span data-stu-id="06416-191">Multiplying the matrices in the opposite order has the visual effect of translating the flying saucer to its world space position, and then rotating it around the world origin.</span></span>

<span data-ttu-id="06416-192">Вне зависимости от того, матрицу какого типа вы создаете, помните о правиле "слева направо", чтобы результаты всегда соответствовали ожидаемым.</span><span class="sxs-lookup"><span data-stu-id="06416-192">No matter what type of matrix you are creating, remember the left-to-right rule to ensure that you achieve the expected effects.</span></span>

## <a name="related-topics"></a><span data-ttu-id="06416-193">См. также</span><span class="sxs-lookup"><span data-stu-id="06416-193">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="06416-194">Начало работы</span><span class="sxs-lookup"><span data-stu-id="06416-194">Getting Started</span></span>](getting-started.md)
</dt> </dl>

 

 



