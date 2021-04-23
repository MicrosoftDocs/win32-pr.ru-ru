---
title: Эффект двумерного аффинного преобразования
description: В результате 2D-преобразования применяется Пространственное преобразование к изображению на основе матрицы 3X2 с помощью преобразования матрицы Direct2D и любого из шести режимов интерполяции.
ms.assetid: E8973EBE-764C-4220-BB1E-3BFD4853582D
keywords:
- Эффект двумерного аффинного преобразования
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3017992d34cd98095f01192ea948684a6b52e53
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137822"
---
# <a name="2d-affine-transform-effect"></a><span data-ttu-id="ae0c7-104">Эффект двумерного аффинного преобразования</span><span class="sxs-lookup"><span data-stu-id="ae0c7-104">2D affine transform effect</span></span>

<span data-ttu-id="ae0c7-105">В результате 2D-преобразования применяется Пространственное преобразование к изображению на основе матрицы 3X2 с помощью [преобразования](direct2d-transforms-overview.md) матрицы Direct2D и любого из шести режимов интерполяции.</span><span class="sxs-lookup"><span data-stu-id="ae0c7-105">The 2D affine transform effect applies a spatial transform to a image based on a 3X2 matrix using the Direct2D matrix [transform](direct2d-transforms-overview.md) and any of six interpolation modes.</span></span> <span data-ttu-id="ae0c7-106">Этот результат можно использовать для вращения, масштабирования, наклона или преобразования изображения.</span><span class="sxs-lookup"><span data-stu-id="ae0c7-106">You can use this effect to rotate, scale, skew, or translate an image.</span></span> <span data-ttu-id="ae0c7-107">Можно также объединить эти операции.</span><span class="sxs-lookup"><span data-stu-id="ae0c7-107">Or, you can combine these operations.</span></span> <span data-ttu-id="ae0c7-108">Аффинных передачи сохраняют параллельные линии и отношение расстояний между любыми тремя точками в изображении.</span><span class="sxs-lookup"><span data-stu-id="ae0c7-108">Affine transfers preserve parallel lines and the ratio of distances between any three points in an image.</span></span>

<span data-ttu-id="ae0c7-109">Идентификатором CLSID для этого действия является CLSID \_ D2D12DAffineTransform.</span><span class="sxs-lookup"><span data-stu-id="ae0c7-109">The CLSID for this effect is CLSID\_D2D12DAffineTransform.</span></span>

-   [<span data-ttu-id="ae0c7-110">Пример изображения</span><span class="sxs-lookup"><span data-stu-id="ae0c7-110">Example image</span></span>](#example-image)
-   [<span data-ttu-id="ae0c7-111">Свойства эффектов</span><span class="sxs-lookup"><span data-stu-id="ae0c7-111">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="ae0c7-112">Режимы границ</span><span class="sxs-lookup"><span data-stu-id="ae0c7-112">Border modes</span></span>](#border-modes)
-   [<span data-ttu-id="ae0c7-113">Режимы интерполяции</span><span class="sxs-lookup"><span data-stu-id="ae0c7-113">Interpolation modes</span></span>](#interpolation-modes)
-   [<span data-ttu-id="ae0c7-114">Битовая карта вывода</span><span class="sxs-lookup"><span data-stu-id="ae0c7-114">Output bitmap</span></span>](#output-bitmap)
-   [<span data-ttu-id="ae0c7-115">Требования</span><span class="sxs-lookup"><span data-stu-id="ae0c7-115">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="ae0c7-116">См. также</span><span class="sxs-lookup"><span data-stu-id="ae0c7-116">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="ae0c7-117">Пример изображения</span><span class="sxs-lookup"><span data-stu-id="ae0c7-117">Example image</span></span>



| <span data-ttu-id="ae0c7-118">До</span><span class="sxs-lookup"><span data-stu-id="ae0c7-118">Before</span></span>                                                             |
|--------------------------------------------------------------------|
| ![изображение перед результатом.](images/default-before.jpg)         |
| <span data-ttu-id="ae0c7-120">После</span><span class="sxs-lookup"><span data-stu-id="ae0c7-120">After</span></span>                                                              |
| ![изображение после преобразования.](images/21-2daffinetransform.png) |



 


```C++
ComPtr<ID2D1Effect> affineTransformEffect;
m_d2dContext->CreateEffect(CLSID_D2D12DAffineTransform, &affineTransformEffect);

affineTransformEffect->SetInput(0, bitmap);

D2D1_MATRIX_3X2_F matrix = D2D1::Matrix3x2F(0.9f, -0.1f,   0.1f, 0.9f,   8.0f, 45.0f);

affineTransformEffect->SetValue(D2D1_2DAFFINETRANSFORM_PROP_TRANSFORM_MATRIX, matrix);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(affineTransformEffect.Get());
m_d2dContext->EndDraw();
```



<span data-ttu-id="ae0c7-122">Этот результат выполняет эту операцию матрицы:</span><span class="sxs-lookup"><span data-stu-id="ae0c7-122">This effect performs this matrix operation:</span></span>

![Операция аффинного матрицы](images/affine-matrix-calculation.png)

<span data-ttu-id="ae0c7-124">Хотя входная матрица определена как 3x2 матрица, последний столбец заполняется символами 0, 0 и 1 для создания квадратной матрицы.</span><span class="sxs-lookup"><span data-stu-id="ae0c7-124">Although the input matrix is defined as a 3x2 matrix, the last column is padded with 0, 0 and 1 to produce a square matrix.</span></span> <span data-ttu-id="ae0c7-125">Это позволяет выполнить умножение матрицы, чтобы преобразования можно было объединить в одну матрицу.</span><span class="sxs-lookup"><span data-stu-id="ae0c7-125">This allows for matrix multiplication, so that transforms can be concatenated into a single matrix.</span></span>

## <a name="effect-properties"></a><span data-ttu-id="ae0c7-126">Свойства эффектов</span><span class="sxs-lookup"><span data-stu-id="ae0c7-126">Effect properties</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ae0c7-127">Отображаемое имя и перечисление индекса</span><span class="sxs-lookup"><span data-stu-id="ae0c7-127">Display name and index enumeration</span></span></th>
<th><span data-ttu-id="ae0c7-128">Описание</span><span class="sxs-lookup"><span data-stu-id="ae0c7-128">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ae0c7-129">интерполатионмоде</span><span class="sxs-lookup"><span data-stu-id="ae0c7-129">InterpolationMode</span></span><br/> <span data-ttu-id="ae0c7-130">D2D1_2DAFFINETRANSFORM_PROP_INTERPOLATION_MODE</span><span class="sxs-lookup"><span data-stu-id="ae0c7-130">D2D1_2DAFFINETRANSFORM_PROP_INTERPOLATION_MODE</span></span><br/></td>
<td><span data-ttu-id="ae0c7-131">Режим интерполяции, используемый для масштабирования изображения.</span><span class="sxs-lookup"><span data-stu-id="ae0c7-131">The interpolation mode used to scale the image.</span></span> <span data-ttu-id="ae0c7-132">Существует 6 режимов масштабирования, которые имеют высокое качество и скорость.</span><span class="sxs-lookup"><span data-stu-id="ae0c7-132">There are 6 scale modes that range in quality and speed.</span></span><br/> <span data-ttu-id="ae0c7-133">Тип — D2D1_2DAFFINETRANSFORM_INTERPOLATION_MODE.</span><span class="sxs-lookup"><span data-stu-id="ae0c7-133">Type is D2D1_2DAFFINETRANSFORM_INTERPOLATION_MODE.</span></span><br/> <span data-ttu-id="ae0c7-134">Значение по умолчанию — D2D1_2DAFFINETRANSFORM_INTERPOLATION_MODE_LINEAR.</span><span class="sxs-lookup"><span data-stu-id="ae0c7-134">Default value is D2D1_2DAFFINETRANSFORM_INTERPOLATION_MODE_LINEAR.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ae0c7-135">бордермоде</span><span class="sxs-lookup"><span data-stu-id="ae0c7-135">BorderMode</span></span><br/> <span data-ttu-id="ae0c7-136">D2D1_2DAFFINETRANSFORM_PROP_BORDER_MODE</span><span class="sxs-lookup"><span data-stu-id="ae0c7-136">D2D1_2DAFFINETRANSFORM_PROP_BORDER_MODE</span></span><br/></td>
<td><span data-ttu-id="ae0c7-137">Режим, используемый для вычисления границы изображения: Soft или Hard.</span><span class="sxs-lookup"><span data-stu-id="ae0c7-137">The mode used to calculate the border of the image, soft or hard.</span></span> <span data-ttu-id="ae0c7-138">Дополнительные сведения см. в разделе <a href="https://www.bing.com/search?q=Border+modes">режимы границ</a> .</span><span class="sxs-lookup"><span data-stu-id="ae0c7-138">See <a href="https://www.bing.com/search?q=Border+modes">Border modes</a> for more info.</span></span> <br/> <span data-ttu-id="ae0c7-139">Тип — D2D1_BORDER_MODE.</span><span class="sxs-lookup"><span data-stu-id="ae0c7-139">Type is D2D1_BORDER_MODE.</span></span><br/> <span data-ttu-id="ae0c7-140">Значение по умолчанию — D2D1_BORDER_MODE_SOFT.</span><span class="sxs-lookup"><span data-stu-id="ae0c7-140">Default value is D2D1_BORDER_MODE_SOFT.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ae0c7-141">трансформматрикс</span><span class="sxs-lookup"><span data-stu-id="ae0c7-141">TransformMatrix</span></span><br/> <span data-ttu-id="ae0c7-142">D2D1_2DAFFINETRANSFORM_PROP_TRANSFORM_MATRIX</span><span class="sxs-lookup"><span data-stu-id="ae0c7-142">D2D1_2DAFFINETRANSFORM_PROP_TRANSFORM_MATRIX</span></span><br/></td>
<td><span data-ttu-id="ae0c7-143">Матрица 3x2 для преобразования изображения с помощью <a href="direct2d-transforms-overview.md">преобразования</a>матрицы Direct2D.</span><span class="sxs-lookup"><span data-stu-id="ae0c7-143">The 3x2 matrix to transform the image using the Direct2D matrix <a href="direct2d-transforms-overview.md">transform</a>.</span></span> <br/> <span data-ttu-id="ae0c7-144">Тип — D2D1_MATRIX_3X2_F.</span><span class="sxs-lookup"><span data-stu-id="ae0c7-144">Type is D2D1_MATRIX_3X2_F.</span></span><br/> <span data-ttu-id="ae0c7-145">Значение по умолчанию — Matrix3x2F:: Identity ().</span><span class="sxs-lookup"><span data-stu-id="ae0c7-145">Default value is Matrix3x2F::Identity().</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ae0c7-146">Четкость</span><span class="sxs-lookup"><span data-stu-id="ae0c7-146">Sharpness</span></span><br/> <span data-ttu-id="ae0c7-147">D2D1_2DAFFINETRANSFORM_PROP_SHARPNESS</span><span class="sxs-lookup"><span data-stu-id="ae0c7-147">D2D1_2DAFFINETRANSFORM_PROP_SHARPNESS</span></span><br/></td>
<td><span data-ttu-id="ae0c7-148">В режиме интерполяции высокого качества кубический уровень резкости фильтра масштабирования в виде числа с плавающей запятой в диапазоне от 0 до 1.</span><span class="sxs-lookup"><span data-stu-id="ae0c7-148">In the high quality cubic interpolation mode, the sharpness level of the scaling filter as a float between 0 and 1.</span></span> <span data-ttu-id="ae0c7-149">Значения являются безмодульными.</span><span class="sxs-lookup"><span data-stu-id="ae0c7-149">The values are unitless.</span></span> <span data-ttu-id="ae0c7-150">Резкость можно использовать для настройки качества изображения при масштабировании изображения.</span><span class="sxs-lookup"><span data-stu-id="ae0c7-150">You can use sharpness to adjust the quality of an image when you scale the image.</span></span><br/> <span data-ttu-id="ae0c7-151">Коэффициент резкости влияет на форму ядра.</span><span class="sxs-lookup"><span data-stu-id="ae0c7-151">The sharpness factor affects the shape of the kernel.</span></span> <span data-ttu-id="ae0c7-152">Чем выше коэффициент резкости, тем меньше ядро.</span><span class="sxs-lookup"><span data-stu-id="ae0c7-152">The higher the sharpness factor, the smaller the kernel.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="ae0c7-153">Это свойство влияет только на режим интерполяции высокого качества.</span><span class="sxs-lookup"><span data-stu-id="ae0c7-153">This property affects only the high quality cubic interpolation mode.</span></span>
</blockquote>
<br/> <span data-ttu-id="ae0c7-154">Тип — FLOAT.</span><span class="sxs-lookup"><span data-stu-id="ae0c7-154">Type is FLOAT.</span></span><br/> <span data-ttu-id="ae0c7-155">Значение по умолчанию — 1,0 f.</span><span class="sxs-lookup"><span data-stu-id="ae0c7-155">Default value is 1.0f.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="border-modes"></a><span data-ttu-id="ae0c7-156">Режимы границ</span><span class="sxs-lookup"><span data-stu-id="ae0c7-156">Border modes</span></span>



| <span data-ttu-id="ae0c7-157">Имя</span><span class="sxs-lookup"><span data-stu-id="ae0c7-157">Name</span></span>                     | <span data-ttu-id="ae0c7-158">Описание</span><span class="sxs-lookup"><span data-stu-id="ae0c7-158">Description</span></span>                                                                                                      |
|--------------------------|------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae0c7-159">\_ \_ Мягкий режим границы \_ D2D1</span><span class="sxs-lookup"><span data-stu-id="ae0c7-159">D2D1\_BORDER\_MODE\_SOFT</span></span> | <span data-ttu-id="ae0c7-160">При интерполяции изображение получает прозрачные черные пиксели, что приводит к мягкому пограничным границе.</span><span class="sxs-lookup"><span data-stu-id="ae0c7-160">The effect pads the image with transparent black pixels as it interpolates, resulting in a soft edge.</span></span><br/> |
| <span data-ttu-id="ae0c7-161">Жесткое D2D1 в \_ \_ режиме границы \_</span><span class="sxs-lookup"><span data-stu-id="ae0c7-161">D2D1\_BORDER\_MODE\_HARD</span></span> | <span data-ttu-id="ae0c7-162">В результате выходные данные заменяются на размер входного изображения.</span><span class="sxs-lookup"><span data-stu-id="ae0c7-162">The effect clamps the output to the size of the input image.</span></span> <br/>                                         |



 

## <a name="interpolation-modes"></a><span data-ttu-id="ae0c7-163">Режимы интерполяции</span><span class="sxs-lookup"><span data-stu-id="ae0c7-163">Interpolation modes</span></span>



| <span data-ttu-id="ae0c7-164">Перечисление</span><span class="sxs-lookup"><span data-stu-id="ae0c7-164">Enumeration</span></span>                                                         | <span data-ttu-id="ae0c7-165">Описание</span><span class="sxs-lookup"><span data-stu-id="ae0c7-165">Description</span></span>                                                                                                                                                                                          |
|---------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae0c7-166">\_ \_ \_ \_ Ближайший сосед в режиме интерполяции D2D1 2DAFFINETRANSFORM \_</span><span class="sxs-lookup"><span data-stu-id="ae0c7-166">D2D1\_2DAFFINETRANSFORM\_INTERPOLATION\_MODE\_NEAREST\_NEIGHBOR</span></span>     | <span data-ttu-id="ae0c7-167">Выбирает ближайшую одиночную точку и использует ее.</span><span class="sxs-lookup"><span data-stu-id="ae0c7-167">Samples the nearest single point and uses that.</span></span> <span data-ttu-id="ae0c7-168">В этом режиме используется меньше времени на обработку, но выводится изображение самого низкого качества.</span><span class="sxs-lookup"><span data-stu-id="ae0c7-168">This mode uses less processing time, but outputs the lowest quality image.</span></span>                                                                           |
| <span data-ttu-id="ae0c7-169">\_ \_ Линейный режим интерполяции D2D1 2DAFFINETRANSFORM \_ \_</span><span class="sxs-lookup"><span data-stu-id="ae0c7-169">D2D1\_2DAFFINETRANSFORM\_INTERPOLATION\_MODE\_LINEAR</span></span>                | <span data-ttu-id="ae0c7-170">Использует выборку с четырьмя точками и линейную интерполяцию.</span><span class="sxs-lookup"><span data-stu-id="ae0c7-170">Uses a four point sample and linear interpolation.</span></span> <span data-ttu-id="ae0c7-171">Этот режим использует больше времени на обработку, чем ближайший соседний режим, но выводит изображение более высокого качества.</span><span class="sxs-lookup"><span data-stu-id="ae0c7-171">This mode uses more processing time than the nearest neighbor mode, but outputs a higher quality image.</span></span>                                           |
| <span data-ttu-id="ae0c7-172">D2D1 \_ 2DAFFINETRANSFORM \_ Режим интерполяции ( \_ \_ кубический)</span><span class="sxs-lookup"><span data-stu-id="ae0c7-172">D2D1\_2DAFFINETRANSFORM\_INTERPOLATION\_MODE\_CUBIC</span></span>                 | <span data-ttu-id="ae0c7-173">Использует 16-примерный ядро кубических для интерполяции.</span><span class="sxs-lookup"><span data-stu-id="ae0c7-173">Uses a 16 sample cubic kernel for interpolation.</span></span> <span data-ttu-id="ae0c7-174">Этот режим использует наибольшее время обработки, но выводит изображение с более высоким качеством.</span><span class="sxs-lookup"><span data-stu-id="ae0c7-174">This mode uses the most processing time, but outputs a higher quality image.</span></span>                                                                        |
| <span data-ttu-id="ae0c7-175">D2D1 \_ 2DAFFINETRANSFORM \_ Режим интерполяции — \_ \_ \_ многопримерная \_ линейная</span><span class="sxs-lookup"><span data-stu-id="ae0c7-175">D2D1\_2DAFFINETRANSFORM\_INTERPOLATION\_MODE\_MULTI\_SAMPLE\_LINEAR</span></span> | <span data-ttu-id="ae0c7-176">Использует 4 линейных образца в пределах одного пикселя для удобного сглаживания.</span><span class="sxs-lookup"><span data-stu-id="ae0c7-176">Uses 4 linear samples within a single pixel for good edge anti-aliasing.</span></span> <span data-ttu-id="ae0c7-177">Этот режим хорошо подходит для уменьшения масштаба по небольшим объемам на изображениях с небольшими пикселями.</span><span class="sxs-lookup"><span data-stu-id="ae0c7-177">This mode is good for scaling down by small amounts on images with few pixels.</span></span>                                              |
| <span data-ttu-id="ae0c7-178">D2D1 \_ 2DAFFINETRANSFORM \_ Режим интерполяции — \_ \_ анизотропная</span><span class="sxs-lookup"><span data-stu-id="ae0c7-178">D2D1\_2DAFFINETRANSFORM\_INTERPOLATION\_MODE\_ANISOTROPIC</span></span>           | <span data-ttu-id="ae0c7-179">Использует анизотропную фильтрацию для выборки шаблона в соответствии с преобразованной формой точечного рисунка.</span><span class="sxs-lookup"><span data-stu-id="ae0c7-179">Uses anisotropic filtering to sample a pattern according to the transformed shape of the bitmap.</span></span>                                                                                                     |
| <span data-ttu-id="ae0c7-180">D2D1 \_ 2DAFFINETRANSFORM \_ \_ Режим интерполяции \_ высокого \_ качества, \_ кубический</span><span class="sxs-lookup"><span data-stu-id="ae0c7-180">D2D1\_2DAFFINETRANSFORM\_INTERPOLATION\_MODE\_HIGH\_QUALITY\_CUBIC</span></span>  | <span data-ttu-id="ae0c7-181">Использует высококачественное ядро кубического размера для выполнения предварительно довнскале образа, если довнскалинг участвует в матрице преобразования.</span><span class="sxs-lookup"><span data-stu-id="ae0c7-181">Uses a variable size high quality cubic kernel to perform a pre-downscale the image if downscaling is involved in the transform matrix.</span></span> <span data-ttu-id="ae0c7-182">Затем использует режим интерполяции кубических для окончательного вывода.</span><span class="sxs-lookup"><span data-stu-id="ae0c7-182">Then uses the cubic interpolation mode for the final output.</span></span> |



 

> [!Note]  
> <span data-ttu-id="ae0c7-183">Если не выбрать режим, то по умолчанию будет применяться \_ \_ линейный режим интерполяции D2D1 2DAFFINETRANSFORM \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="ae0c7-183">If you don't select a mode, the effect defaults to D2D1\_2DAFFINETRANSFORM\_INTERPOLATION\_MODE\_LINEAR.</span></span>

 

> [!Note]  
> <span data-ttu-id="ae0c7-184">В режиме анизотропного масштабирования создается MIP-карты при масштабировании, однако если для свойства **кэширования** задано значение true для эффектов, вводимых в результате этого эффекта, MIP-карты не будет создаваться каждый раз для достаточного размера изображений.</span><span class="sxs-lookup"><span data-stu-id="ae0c7-184">Anisotropic mode generates mipmaps when scaling, however, if you set the **Cached** property to true on the effects that are input to this effect, the mipmaps won't be generated every time for sufficiently small images.</span></span>

 

## <a name="output-bitmap"></a><span data-ttu-id="ae0c7-185">Битовая карта вывода</span><span class="sxs-lookup"><span data-stu-id="ae0c7-185">Output bitmap</span></span>

<span data-ttu-id="ae0c7-186">Размер выходного растрового изображения зависит от матрицы преобразования, применяемой к изображению.</span><span class="sxs-lookup"><span data-stu-id="ae0c7-186">The size of the output bitmap depends on the transform matrix that is applied to the image.</span></span>

<span data-ttu-id="ae0c7-187">Этот результат выполняет операцию преобразования, а затем применяет ограничивающий прямоугольник вокруг результата.</span><span class="sxs-lookup"><span data-stu-id="ae0c7-187">The effect performs the transform operation and then applies a bounding box around the result.</span></span> <span data-ttu-id="ae0c7-188">Битовая карта выходных данных — это размер ограничивающего прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="ae0c7-188">The output bitmap is the size of the bounding box.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae0c7-189">Требования</span><span class="sxs-lookup"><span data-stu-id="ae0c7-189">Requirements</span></span>



| <span data-ttu-id="ae0c7-190">Требование</span><span class="sxs-lookup"><span data-stu-id="ae0c7-190">Requirement</span></span> | <span data-ttu-id="ae0c7-191">Значение</span><span class="sxs-lookup"><span data-stu-id="ae0c7-191">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ae0c7-192">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ae0c7-192">Minimum supported client</span></span> | <span data-ttu-id="ae0c7-193">Windows 8 и обновление платформы для \[ классических приложений Windows 7 \| приложения для Магазина Windows\]</span><span class="sxs-lookup"><span data-stu-id="ae0c7-193">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="ae0c7-194">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ae0c7-194">Minimum supported server</span></span> | <span data-ttu-id="ae0c7-195">Windows 8 и обновление платформы для \[ классических приложений Windows 7 \| приложения для Магазина Windows\]</span><span class="sxs-lookup"><span data-stu-id="ae0c7-195">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="ae0c7-196">Header</span><span class="sxs-lookup"><span data-stu-id="ae0c7-196">Header</span></span>                   | <span data-ttu-id="ae0c7-197">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="ae0c7-197">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="ae0c7-198">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ae0c7-198">Library</span></span>                  | <span data-ttu-id="ae0c7-199">D2D1. lib, дксгуид. lib</span><span class="sxs-lookup"><span data-stu-id="ae0c7-199">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="ae0c7-200">См. также</span><span class="sxs-lookup"><span data-stu-id="ae0c7-200">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ae0c7-201">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="ae0c7-201">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

