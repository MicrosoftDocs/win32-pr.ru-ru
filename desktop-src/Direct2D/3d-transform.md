---
title: Эффект трехмерного преобразования
description: Используйте эффект трехмерного преобразования, чтобы применить произвольную матрицу преобразования 4x4 к изображению.
ms.assetid: BC2F2837-40F0-4293-A190-8B5F81BB01B6
keywords:
- трехмерное преобразование, эффект
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fabe0c2c220038802b5218b54187a1ff89268bfa
ms.sourcegitcommit: ee06501cc29132927ade9813e0888aaa4decc487
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/28/2021
ms.locfileid: "104559171"
---
# <a name="3d-transform-effect"></a><span data-ttu-id="bbdd7-104">Эффект трехмерного преобразования</span><span class="sxs-lookup"><span data-stu-id="bbdd7-104">3D transform effect</span></span>

<span data-ttu-id="bbdd7-105">Используйте эффект трехмерного преобразования, чтобы применить произвольную матрицу преобразования 4x4 к изображению.</span><span class="sxs-lookup"><span data-stu-id="bbdd7-105">Use the 3D transform effect to apply an arbitrary 4x4 transform matrix to an image.</span></span>

<span data-ttu-id="bbdd7-106">Этот результат применяет матрицу (M?), которую вы предоставляете для угловых вершин исходного изображения ( \[ x y z 1 \] ), используя это вычисление:</span><span class="sxs-lookup"><span data-stu-id="bbdd7-106">This effect applies the matrix (M?) you provide to the corner vertices of the source image (\[ x y z 1 \]) using this calculation:</span></span>

<span data-ttu-id="bbdd7-107">\[x<sub>r</sub> y<sub>r</sub> z<sub>r</sub> 1 \] = \[ x y z 1 \] \* M?</span><span class="sxs-lookup"><span data-stu-id="bbdd7-107">\[ x<sub>r</sub> y<sub>r</sub> z<sub>r</sub> 1 \]=\[ x y z 1 \]\*M?</span></span>

<span data-ttu-id="bbdd7-108">Идентификатором CLSID для этого действия является CLSID \_ D2D13DTransform.</span><span class="sxs-lookup"><span data-stu-id="bbdd7-108">The CLSID for this effect is CLSID\_D2D13DTransform.</span></span>

-   [<span data-ttu-id="bbdd7-109">Пример изображения</span><span class="sxs-lookup"><span data-stu-id="bbdd7-109">Example image</span></span>](#example-image)
-   [<span data-ttu-id="bbdd7-110">Свойства эффектов</span><span class="sxs-lookup"><span data-stu-id="bbdd7-110">Effect properties</span></span>](#effect-properties)
    -   [<span data-ttu-id="bbdd7-111">Режимы интерполяции</span><span class="sxs-lookup"><span data-stu-id="bbdd7-111">Interpolation modes</span></span>](#interpolation-modes)
    -   [<span data-ttu-id="bbdd7-112">Режимы границ</span><span class="sxs-lookup"><span data-stu-id="bbdd7-112">Border modes</span></span>](#border-modes)
-   [<span data-ttu-id="bbdd7-113">Класс Matrix преобразования 4x4</span><span class="sxs-lookup"><span data-stu-id="bbdd7-113">4x4 Transform Matrix Class</span></span>](#4x4-transform-matrix-class)
-   [<span data-ttu-id="bbdd7-114">Требования</span><span class="sxs-lookup"><span data-stu-id="bbdd7-114">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="bbdd7-115">См. также</span><span class="sxs-lookup"><span data-stu-id="bbdd7-115">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="bbdd7-116">Пример изображения</span><span class="sxs-lookup"><span data-stu-id="bbdd7-116">Example image</span></span>



| <span data-ttu-id="bbdd7-117">До</span><span class="sxs-lookup"><span data-stu-id="bbdd7-117">Before</span></span>                                                        |
|---------------------------------------------------------------|
| ![изображение перед преобразованием.](images/default-before.jpg) |
| <span data-ttu-id="bbdd7-119">После</span><span class="sxs-lookup"><span data-stu-id="bbdd7-119">After</span></span>                                                         |
| ![изображение после преобразования.](images/24-3dtransform.png)  |



 


```C++
ComPtr<ID2D1Effect> D2D13DTransformEffect;
m_d2dContext->CreateEffect(CLSID_D2D13DTransform, &D2D13DTransformEffect);

D2D13DTransformEffect->SetInput(0, bitmap);

// You can use the helper methods in D2D1::Matrix4x4F to create common matrix transformations.
D2D1_MATRIX_4X4_F matrix = 
    D2D1::Matrix4x4F::Translation(0.0f, -192.0f, 0.0f) *
    D2D1::Matrix4x4F::RotationY(30.0f) *
    D2D1::Matrix4x4F::Translation(0.0f, 192.0f, 0.0f);

D2D13DTransformEffect->SetValue(D2D1_3DTRANSFORM_PROP_TRANSFORM_MATRIX, matrix);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(D2D13DTransformEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a><span data-ttu-id="bbdd7-121">Свойства эффектов</span><span class="sxs-lookup"><span data-stu-id="bbdd7-121">Effect properties</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="bbdd7-122">Отображаемое имя и перечисление индекса</span><span class="sxs-lookup"><span data-stu-id="bbdd7-122">Display name and index enumeration</span></span></th>
<th><span data-ttu-id="bbdd7-123">Описание</span><span class="sxs-lookup"><span data-stu-id="bbdd7-123">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="bbdd7-124">интерполатионмоде</span><span class="sxs-lookup"><span data-stu-id="bbdd7-124">InterpolationMode</span></span><br/> <span data-ttu-id="bbdd7-125">D2D1_3DTRANSFORM_PROP_INTERPOLATION_MODE</span><span class="sxs-lookup"><span data-stu-id="bbdd7-125">D2D1_3DTRANSFORM_PROP_INTERPOLATION_MODE</span></span><br/></td>
<td><span data-ttu-id="bbdd7-126">Режим интерполяции, используемый в изображении в результате применения.</span><span class="sxs-lookup"><span data-stu-id="bbdd7-126">The interpolation mode the effect uses on the image.</span></span> <span data-ttu-id="bbdd7-127">Существует 5 режимов масштабирования, имеющих высокое качество и скорость.</span><span class="sxs-lookup"><span data-stu-id="bbdd7-127">There are 5 scale modes that range in quality and speed.</span></span><br/> <span data-ttu-id="bbdd7-128">Тип — D2D1_3DTRANSFORM_INTERPOLATION_MODE.</span><span class="sxs-lookup"><span data-stu-id="bbdd7-128">Type is D2D1_3DTRANSFORM_INTERPOLATION_MODE.</span></span><br/> <span data-ttu-id="bbdd7-129">Значение по умолчанию — D2D1_3DTRANSFORM_INTERPOLATION_MODE_LINEAR.</span><span class="sxs-lookup"><span data-stu-id="bbdd7-129">Default value is D2D1_3DTRANSFORM_INTERPOLATION_MODE_LINEAR.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bbdd7-130">бордермоде</span><span class="sxs-lookup"><span data-stu-id="bbdd7-130">BorderMode</span></span><br/> <span data-ttu-id="bbdd7-131">D2D1_3DTRANSFORM_PROP_BORDER_MODE</span><span class="sxs-lookup"><span data-stu-id="bbdd7-131">D2D1_3DTRANSFORM_PROP_BORDER_MODE</span></span><br/></td>
<td><span data-ttu-id="bbdd7-132">Режим, используемый для вычисления границы изображения: Soft или Hard.</span><span class="sxs-lookup"><span data-stu-id="bbdd7-132">The mode used to calculate the border of the image, soft or hard.</span></span> <span data-ttu-id="bbdd7-133">Дополнительные сведения см. в разделе <a href="https://www.bing.com/search?q=Border+modes">режимы границ</a> .</span><span class="sxs-lookup"><span data-stu-id="bbdd7-133">See <a href="https://www.bing.com/search?q=Border+modes">Border modes</a> for more info.</span></span><br/> <span data-ttu-id="bbdd7-134">Тип — D2D1_BORDER_MODE.</span><span class="sxs-lookup"><span data-stu-id="bbdd7-134">Type is D2D1_BORDER_MODE.</span></span><br/> <span data-ttu-id="bbdd7-135">Значение по умолчанию — D2D1_BORDER_MODE_SOFT.</span><span class="sxs-lookup"><span data-stu-id="bbdd7-135">Default value is D2D1_BORDER_MODE_SOFT.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bbdd7-136">трансформматрикс</span><span class="sxs-lookup"><span data-stu-id="bbdd7-136">TransformMatrix</span></span><br/> <span data-ttu-id="bbdd7-137">D2D1_3DTRANSFORM_PROP_TRANSFORM_MATRIX</span><span class="sxs-lookup"><span data-stu-id="bbdd7-137">D2D1_3DTRANSFORM_PROP_TRANSFORM_MATRIX</span></span><br/></td>
<td><span data-ttu-id="bbdd7-138">Матрица преобразования 4x4, применяемая к плоскости проекции.</span><span class="sxs-lookup"><span data-stu-id="bbdd7-138">A 4x4 transform matrix applied to the projection plane.</span></span> <span data-ttu-id="bbdd7-139">Приведенное ниже вычисление матрицы используется для отображения точек из одной трехмерной системы координат в преобразованную двухмерную систему координат.</span><span class="sxs-lookup"><span data-stu-id="bbdd7-139">The following matrix calculation is used to map points from one 3D coordinate system to the transformed 2D coordinate system.</span></span> <br/><img src="images/3d-transform-matrix1.png" alt="3D Depth Matrix" /><span data-ttu-id="bbdd7-140">Где:</span><span class="sxs-lookup"><span data-stu-id="bbdd7-140">Where:</span></span><dl> <span data-ttu-id="bbdd7-141">Координаты X, Y, Z = входная плоскость проекции</span><span class="sxs-lookup"><span data-stu-id="bbdd7-141">X, Y, Z = Input projection plane coordinates</span></span><br />
<span data-ttu-id="bbdd7-142">Элементы матрицы M<sub>x, y</sub> = Transform</span><span class="sxs-lookup"><span data-stu-id="bbdd7-142">M<sub>x,y</sub> = Transform Matrix elements</span></span><br />
<span data-ttu-id="bbdd7-143">X, Y, Z = выходные координаты плоскости проекции</span><span class="sxs-lookup"><span data-stu-id="bbdd7-143">X , Y , Z  =Output projection plane coordinates</span></span><br />
</dl> <br/> <span data-ttu-id="bbdd7-144">Отдельные элементы матрицы не привязаны и не имеют модулей.</span><span class="sxs-lookup"><span data-stu-id="bbdd7-144">The individual matrix elements are not bounded and are unitless.</span></span> <br/> <span data-ttu-id="bbdd7-145">Тип — D2D1_MATRIX_4X4_F.</span><span class="sxs-lookup"><span data-stu-id="bbdd7-145">Type is D2D1_MATRIX_4X4_F.</span></span><br/> <span data-ttu-id="bbdd7-146">Значение по умолчанию — Matrix4x4F (1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 0, 0, 0, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="bbdd7-146">Default value is Matrix4x4F(1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1).</span></span><br/></td>
</tr>
</tbody>
</table>



 

### <a name="interpolation-modes"></a><span data-ttu-id="bbdd7-147">Режимы интерполяции</span><span class="sxs-lookup"><span data-stu-id="bbdd7-147">Interpolation modes</span></span>



| <span data-ttu-id="bbdd7-148">Перечисление</span><span class="sxs-lookup"><span data-stu-id="bbdd7-148">Enumeration</span></span>                                                   | <span data-ttu-id="bbdd7-149">Описание</span><span class="sxs-lookup"><span data-stu-id="bbdd7-149">Description</span></span>                                                                                                                                                |
|---------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bbdd7-150">\_ \_ \_ \_ Ближайший сосед в режиме интерполяции D2D1 3DTRANSFORM \_</span><span class="sxs-lookup"><span data-stu-id="bbdd7-150">D2D1\_3DTRANSFORM\_INTERPOLATION\_MODE\_NEAREST\_NEIGHBOR</span></span>     | <span data-ttu-id="bbdd7-151">Выбирает ближайшую одиночную точку и использует ее.</span><span class="sxs-lookup"><span data-stu-id="bbdd7-151">Samples the nearest single point and uses that.</span></span> <span data-ttu-id="bbdd7-152">В этом режиме используется меньше времени на обработку, но выводится изображение самого низкого качества.</span><span class="sxs-lookup"><span data-stu-id="bbdd7-152">This mode uses less processing time, but outputs the lowest quality image.</span></span>                                 |
| <span data-ttu-id="bbdd7-153">\_ \_ Линейный режим интерполяции D2D1 3DTRANSFORM \_ \_</span><span class="sxs-lookup"><span data-stu-id="bbdd7-153">D2D1\_3DTRANSFORM\_INTERPOLATION\_MODE\_LINEAR</span></span>                | <span data-ttu-id="bbdd7-154">Использует выборку с четырьмя точками и линейную интерполяцию.</span><span class="sxs-lookup"><span data-stu-id="bbdd7-154">Uses a four point sample and linear interpolation.</span></span> <span data-ttu-id="bbdd7-155">Этот режим использует больше времени на обработку, чем ближайший соседний режим, но выводит изображение более высокого качества.</span><span class="sxs-lookup"><span data-stu-id="bbdd7-155">This mode uses more processing time than the nearest neighbor mode, but outputs a higher quality image.</span></span> |
| <span data-ttu-id="bbdd7-156">D2D1 \_ 3DTRANSFORM \_ Режим интерполяции ( \_ \_ кубический)</span><span class="sxs-lookup"><span data-stu-id="bbdd7-156">D2D1\_3DTRANSFORM\_INTERPOLATION\_MODE\_CUBIC</span></span>                 | <span data-ttu-id="bbdd7-157">Использует 16-примерный ядро кубических для интерполяции.</span><span class="sxs-lookup"><span data-stu-id="bbdd7-157">Uses a 16 sample cubic kernel for interpolation.</span></span> <span data-ttu-id="bbdd7-158">Этот режим использует наибольшее время обработки, но выводит изображение с более высоким качеством.</span><span class="sxs-lookup"><span data-stu-id="bbdd7-158">This mode uses the most processing time, but outputs a higher quality image.</span></span>                              |
| <span data-ttu-id="bbdd7-159">D2D1 \_ 3DTRANSFORM \_ Режим интерполяции — \_ \_ \_ многопримерная \_ линейная</span><span class="sxs-lookup"><span data-stu-id="bbdd7-159">D2D1\_3DTRANSFORM\_INTERPOLATION\_MODE\_MULTI\_SAMPLE\_LINEAR</span></span> | <span data-ttu-id="bbdd7-160">Использует 4 линейных образца в пределах одного пикселя для удобного сглаживания.</span><span class="sxs-lookup"><span data-stu-id="bbdd7-160">Uses 4 linear samples within a single pixel for good edge anti-aliasing.</span></span> <span data-ttu-id="bbdd7-161">Этот режим хорошо подходит для уменьшения масштаба по небольшим объемам на изображениях с небольшими пикселями.</span><span class="sxs-lookup"><span data-stu-id="bbdd7-161">This mode is good for scaling down by small amounts on images with few pixels.</span></span>    |
| <span data-ttu-id="bbdd7-162">D2D1 \_ 3DTRANSFORM \_ Режим интерполяции — \_ \_ анизотропная</span><span class="sxs-lookup"><span data-stu-id="bbdd7-162">D2D1\_3DTRANSFORM\_INTERPOLATION\_MODE\_ANISOTROPIC</span></span>           | <span data-ttu-id="bbdd7-163">Использует анизотропную фильтрацию для выборки шаблона в соответствии с преобразованной формой точечного рисунка.</span><span class="sxs-lookup"><span data-stu-id="bbdd7-163">Uses anisotropic filtering to sample a pattern according to the transformed shape of the bitmap.</span></span>                                                           |



 

> [!Note]  
> <span data-ttu-id="bbdd7-164">Если не выбрать режим, то по умолчанию будет применяться \_ \_ линейный режим интерполяции D2D1 3DTRANSFORM \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="bbdd7-164">If you don't select a mode, the effect defaults to D2D1\_3DTRANSFORM\_INTERPOLATION\_MODE\_LINEAR.</span></span>

 

> [!Note]  
> <span data-ttu-id="bbdd7-165">В режиме анизотропного масштабирования создается MIP-карты при масштабировании, однако если для свойства **кэширования** задано значение true для эффектов, вводимых в результате этого эффекта, MIP-карты не будет создаваться каждый раз для достаточного размера изображений.</span><span class="sxs-lookup"><span data-stu-id="bbdd7-165">Anisotropic mode generates mipmaps when scaling, however, if you set the **Cached** property to true on the effects that are input to this effect, the mipmaps won't be generated every time for sufficiently small images.</span></span>

 

### <a name="border-modes"></a><span data-ttu-id="bbdd7-166">Режимы границ</span><span class="sxs-lookup"><span data-stu-id="bbdd7-166">Border modes</span></span>



| <span data-ttu-id="bbdd7-167">Имя</span><span class="sxs-lookup"><span data-stu-id="bbdd7-167">Name</span></span>                     | <span data-ttu-id="bbdd7-168">Описание</span><span class="sxs-lookup"><span data-stu-id="bbdd7-168">Description</span></span>                                                                                                      |
|--------------------------|------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bbdd7-169">\_ \_ Мягкий режим границы \_ D2D1</span><span class="sxs-lookup"><span data-stu-id="bbdd7-169">D2D1\_BORDER\_MODE\_SOFT</span></span> | <span data-ttu-id="bbdd7-170">При интерполяции изображение получает прозрачные черные пиксели, что приводит к мягкому пограничным границе.</span><span class="sxs-lookup"><span data-stu-id="bbdd7-170">The effect pads the image with transparent black pixels as it interpolates, resulting in a soft edge.</span></span><br/> |
| <span data-ttu-id="bbdd7-171">Жесткое D2D1 в \_ \_ режиме границы \_</span><span class="sxs-lookup"><span data-stu-id="bbdd7-171">D2D1\_BORDER\_MODE\_HARD</span></span> | <span data-ttu-id="bbdd7-172">В результате выходные данные заменяются на размер входного изображения.</span><span class="sxs-lookup"><span data-stu-id="bbdd7-172">The effect clamps the output to the size of the input image.</span></span> <br/>                                         |



 

## <a name="4x4-transform-matrix-class"></a><span data-ttu-id="bbdd7-173">Класс Matrix преобразования 4x4</span><span class="sxs-lookup"><span data-stu-id="bbdd7-173">4x4 Transform Matrix Class</span></span>

<span data-ttu-id="bbdd7-174">Direct2D предоставляет класс матрицы 4x4 для предоставления вспомогательных функций для преобразования изображения в 3 измерения.</span><span class="sxs-lookup"><span data-stu-id="bbdd7-174">Direct2D provides a 4x4 matrix class to provide helper functions for transforming the image in 3 dimensions.</span></span> <span data-ttu-id="bbdd7-175">Дополнительные сведения и описание всех членов класса см. в разделе [**Matrix4x4F**](/windows/desktop/api/d2d1_1helper/nl-d2d1_1helper-matrix4x4f) .</span><span class="sxs-lookup"><span data-stu-id="bbdd7-175">See the [**Matrix4x4F**](/windows/desktop/api/d2d1_1helper/nl-d2d1_1helper-matrix4x4f) topic for more info and a description of all the class members.</span></span>



| <span data-ttu-id="bbdd7-176">Функция</span><span class="sxs-lookup"><span data-stu-id="bbdd7-176">Function</span></span>                                | <span data-ttu-id="bbdd7-177">Описание</span><span class="sxs-lookup"><span data-stu-id="bbdd7-177">Description</span></span>                                                                                    | <span data-ttu-id="bbdd7-178">Матрица</span><span class="sxs-lookup"><span data-stu-id="bbdd7-178">Matrix</span></span>                                                 |
|-----------------------------------------|------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span data-ttu-id="bbdd7-179">Matrix4x4F:: Scale (X, Y, Z)</span><span class="sxs-lookup"><span data-stu-id="bbdd7-179">Matrix4x4F::Scale(X, Y, Z)</span></span>              | <span data-ttu-id="bbdd7-180">Формирует матрицу преобразования, которая масштабирует плоскость проекции в направлении X, Y и (или) Z.</span><span class="sxs-lookup"><span data-stu-id="bbdd7-180">Generates a transform matrix that scales the projection plane in the X, Y, and/or Z direction.</span></span> | ![Матрица scale3d](images/3d-transform-matrix2.png)     |
| <span data-ttu-id="bbdd7-182">Скевкс (X)</span><span class="sxs-lookup"><span data-stu-id="bbdd7-182">SkewX(X)</span></span>                                | <span data-ttu-id="bbdd7-183">Формирует матрицу преобразования, которая наклоняет плоскость проекции по оси X.</span><span class="sxs-lookup"><span data-stu-id="bbdd7-183">Generates a transform matrix that skews the projection plane in the X direction.</span></span>               | ![Показывает матрицу смещения в направлении по оси X.](images/matrix4x4-skewx.png)             |
| <span data-ttu-id="bbdd7-185">Отклонение (Y)</span><span class="sxs-lookup"><span data-stu-id="bbdd7-185">SkewY(Y)</span></span>                                | <span data-ttu-id="bbdd7-186">Формирует матрицу преобразования, которая наклоняет плоскость проекции в направлении Y.</span><span class="sxs-lookup"><span data-stu-id="bbdd7-186">Generates a transform matrix that skews the projection plane in the Y direction.</span></span>               | ![Матрица отклонений](images/matrix4x4-skewy.png)             |
| <span data-ttu-id="bbdd7-188">Преобразование (X, Y, Z)</span><span class="sxs-lookup"><span data-stu-id="bbdd7-188">Translation(X, Y, Z)</span></span>                    | <span data-ttu-id="bbdd7-189">Формирует матрицу преобразования, преобразующую плоскость проекции в направлении X, Y или Z.</span><span class="sxs-lookup"><span data-stu-id="bbdd7-189">Generates a transform matrix that translates the projection plane in the X, Y, or Z direction.</span></span> | ![Преобразование матрицы](images/3d-transform-matrix4.png)   |
| <span data-ttu-id="bbdd7-191">Ротатионкс (X)</span><span class="sxs-lookup"><span data-stu-id="bbdd7-191">RotationX(X)</span></span>                            | <span data-ttu-id="bbdd7-192">Формирует матрицу преобразования, которая поворачивает плоскость проекции по оси X.</span><span class="sxs-lookup"><span data-stu-id="bbdd7-192">Generates a transform matrix that rotates the projection plane about the X axis.</span></span>               | ![повернуть x матрицу](images/3d-transform-matrix5.png)    |
| <span data-ttu-id="bbdd7-194">Вращение (Y)</span><span class="sxs-lookup"><span data-stu-id="bbdd7-194">RotationY(Y)</span></span>                            | <span data-ttu-id="bbdd7-195">Формирует матрицу преобразования, которая поворачивает плоскость проекции по оси Y.</span><span class="sxs-lookup"><span data-stu-id="bbdd7-195">Generates a transform matrix that rotates the projection plane about the Y axis.</span></span>               | ![повернуть матрицу y](images/3d-transform-matrix6.png)    |
| <span data-ttu-id="bbdd7-197">Ротатионз (Z)</span><span class="sxs-lookup"><span data-stu-id="bbdd7-197">RotationZ(Z)</span></span>                            | <span data-ttu-id="bbdd7-198">Формирует матрицу преобразования, которая поворачивает плоскость проекции по оси Z.</span><span class="sxs-lookup"><span data-stu-id="bbdd7-198">Generates a transform matrix that rotates the projection plane about the Z axis.</span></span>               | ![повернуть матрицу z](images/3d-transform-matrix7.png)    |
| <span data-ttu-id="bbdd7-200">Перспективепрожектион (г)</span><span class="sxs-lookup"><span data-stu-id="bbdd7-200">PerspectiveProjection(D)</span></span>                | <span data-ttu-id="bbdd7-201">Преобразование «перспектива» со значением глубины «D».</span><span class="sxs-lookup"><span data-stu-id="bbdd7-201">A perspective transformation with a depth value of D.</span></span>                                          | ![Матрица перспективы](images/3d-transform-matrix8.png) |
| <span data-ttu-id="bbdd7-203">Ротатионарбитраряксис (X, Y, Z, градусы)</span><span class="sxs-lookup"><span data-stu-id="bbdd7-203">RotationArbitraryAxis(X, Y, Z, degrees)</span></span> | <span data-ttu-id="bbdd7-204">Поворачивает плоскость проекции относительно указанной оси.</span><span class="sxs-lookup"><span data-stu-id="bbdd7-204">Rotates the projection plane about the axis you specify.</span></span>                                       |                                                        |



 

## <a name="requirements"></a><span data-ttu-id="bbdd7-205">Требования</span><span class="sxs-lookup"><span data-stu-id="bbdd7-205">Requirements</span></span>



| <span data-ttu-id="bbdd7-206">Требование</span><span class="sxs-lookup"><span data-stu-id="bbdd7-206">Requirement</span></span> | <span data-ttu-id="bbdd7-207">Значение</span><span class="sxs-lookup"><span data-stu-id="bbdd7-207">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="bbdd7-208">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bbdd7-208">Minimum supported client</span></span> | <span data-ttu-id="bbdd7-209">Windows 8 и обновление платформы для \[ классических приложений Windows 7 \| приложения для Магазина Windows\]</span><span class="sxs-lookup"><span data-stu-id="bbdd7-209">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="bbdd7-210">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bbdd7-210">Minimum supported server</span></span> | <span data-ttu-id="bbdd7-211">Windows 8 и обновление платформы для \[ классических приложений Windows 7 \| приложения для Магазина Windows\]</span><span class="sxs-lookup"><span data-stu-id="bbdd7-211">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="bbdd7-212">Header</span><span class="sxs-lookup"><span data-stu-id="bbdd7-212">Header</span></span>                   | <span data-ttu-id="bbdd7-213">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="bbdd7-213">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="bbdd7-214">Библиотека</span><span class="sxs-lookup"><span data-stu-id="bbdd7-214">Library</span></span>                  | <span data-ttu-id="bbdd7-215">D2D1. lib, дксгуид. lib</span><span class="sxs-lookup"><span data-stu-id="bbdd7-215">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="bbdd7-216">См. также</span><span class="sxs-lookup"><span data-stu-id="bbdd7-216">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bbdd7-217">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="bbdd7-217">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

