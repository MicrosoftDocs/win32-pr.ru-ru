---
title: Эффект масштабирования
description: 'Используйте этот результат для увеличения или уменьшения масштаба изображения. Этот результат включает шесть режимов масштабирования: ближайший соседний, линейный, кубический, многопримерный линейный, анизотропный и высококачественный кубический.'
ms.assetid: 99DFA8DB-384B-4F64-90A2-0D3D7E1ACF27
keywords:
- масштабный результат
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad3af77bc24db387fff0854e0432c270fa2ce6d5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415369"
---
# <a name="scale-effect"></a><span data-ttu-id="b4ece-105">Эффект масштабирования</span><span class="sxs-lookup"><span data-stu-id="b4ece-105">Scale effect</span></span>

<span data-ttu-id="b4ece-106">Используйте этот результат для увеличения или уменьшения масштаба изображения.</span><span class="sxs-lookup"><span data-stu-id="b4ece-106">Use this effect to scale an image up or down.</span></span> <span data-ttu-id="b4ece-107">Этот результат включает шесть режимов масштабирования: ближайший соседний, линейный, кубический, многопримерный линейный, анизотропный и высококачественный кубический уровень.</span><span class="sxs-lookup"><span data-stu-id="b4ece-107">The effect has six scaling modes: nearest neighbor, linear, cubic, multi-sample linear, anisotropic, and high quality cubic.</span></span>

<span data-ttu-id="b4ece-108">Идентификатором CLSID для этого действия является CLSID \_ D2D1Scale.</span><span class="sxs-lookup"><span data-stu-id="b4ece-108">The CLSID for this effect is CLSID\_D2D1Scale.</span></span>

-   [<span data-ttu-id="b4ece-109">Пример изображения</span><span class="sxs-lookup"><span data-stu-id="b4ece-109">Example image</span></span>](#example-image)
-   [<span data-ttu-id="b4ece-110">Свойства эффектов</span><span class="sxs-lookup"><span data-stu-id="b4ece-110">Effect properties</span></span>](#effect-properties)
    -   [<span data-ttu-id="b4ece-111">Режимы границ</span><span class="sxs-lookup"><span data-stu-id="b4ece-111">Border modes</span></span>](#border-modes)
-   [<span data-ttu-id="b4ece-112">Режимы интерполяции</span><span class="sxs-lookup"><span data-stu-id="b4ece-112">Interpolation modes</span></span>](#interpolation-modes)
-   [<span data-ttu-id="b4ece-113">Битовая карта вывода</span><span class="sxs-lookup"><span data-stu-id="b4ece-113">Output bitmap</span></span>](#output-bitmap)
-   [<span data-ttu-id="b4ece-114">Требования</span><span class="sxs-lookup"><span data-stu-id="b4ece-114">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="b4ece-115">См. также</span><span class="sxs-lookup"><span data-stu-id="b4ece-115">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="b4ece-116">Пример изображения</span><span class="sxs-lookup"><span data-stu-id="b4ece-116">Example image</span></span>

<span data-ttu-id="b4ece-117">В этом примере показано масштабирование эффектов масштабирования в два раза больше входных данных и обрезки до исходного размера.</span><span class="sxs-lookup"><span data-stu-id="b4ece-117">This example shows the scale effect zooming in 2 times the input and cropping to the original size.</span></span>



| <span data-ttu-id="b4ece-118">До</span><span class="sxs-lookup"><span data-stu-id="b4ece-118">Before</span></span>                                                     |
|------------------------------------------------------------|
| ![изображение перед результатом.](images/default-before.jpg) |
| <span data-ttu-id="b4ece-120">После</span><span class="sxs-lookup"><span data-stu-id="b4ece-120">After</span></span>                                                      |
| ![изображение после преобразования.](images/22-scale.png)     |



 


```C++
ComPtr<ID2D1Effect> scaleEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Scale, &scaleEffect);

scaleEffect->SetInput(0, bitmap);

scaleEffect->SetValue(D2D1_SCALE_PROP_CENTER_POINT, D2D1::Vector2F(256.0f, 192.0f));
scaleEffect->SetValue(D2D1_SCALE_PROP_SCALE, D2D1::Vector2F(2.0f, 2.0f));

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(scaleEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a><span data-ttu-id="b4ece-122">Свойства эффектов</span><span class="sxs-lookup"><span data-stu-id="b4ece-122">Effect properties</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b4ece-123">Отображаемое имя и перечисление индекса</span><span class="sxs-lookup"><span data-stu-id="b4ece-123">Display name and index enumeration</span></span></th>
<th><span data-ttu-id="b4ece-124">Описание</span><span class="sxs-lookup"><span data-stu-id="b4ece-124">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b4ece-125">Масштабирование</span><span class="sxs-lookup"><span data-stu-id="b4ece-125">Scale</span></span><br/> <span data-ttu-id="b4ece-126">D2D1_SCALE_PROP_SCALE</span><span class="sxs-lookup"><span data-stu-id="b4ece-126">D2D1_SCALE_PROP_SCALE</span></span><br/></td>
<td><span data-ttu-id="b4ece-127">Величина масштаба в направлении X и Y как отношение размера выходных данных к размеру входных данных.</span><span class="sxs-lookup"><span data-stu-id="b4ece-127">The scale amount in the X and Y direction as a ratio of the output size to the input size.</span></span> <span data-ttu-id="b4ece-128">Это свойство имеет D2D1_VECTOR_2Fdefined как: (Scale X, Y).</span><span class="sxs-lookup"><span data-stu-id="b4ece-128">This property a D2D1_VECTOR_2Fdefined as: (X scale, Y scale).</span></span> <span data-ttu-id="b4ece-129">Значения масштаба FLOAT, без единицы и должны быть положительными или равными 0.</span><span class="sxs-lookup"><span data-stu-id="b4ece-129">The scale amounts are FLOAT, unitless, and must be positive or 0.</span></span><br/> <span data-ttu-id="b4ece-130">Тип — D2D1_VECTOR_2F.</span><span class="sxs-lookup"><span data-stu-id="b4ece-130">The type is D2D1_VECTOR_2F.</span></span><br/> <span data-ttu-id="b4ece-131">Значение по умолчанию — {1.0 f, 1.0 f}.</span><span class="sxs-lookup"><span data-stu-id="b4ece-131">The default value is {1.0f, 1.0f}.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b4ece-132">CenterPoint (Центральная точка)</span><span class="sxs-lookup"><span data-stu-id="b4ece-132">CenterPoint</span></span><br/> <span data-ttu-id="b4ece-133">D2D1_SCALE_PROP_CENTER_POINT</span><span class="sxs-lookup"><span data-stu-id="b4ece-133">D2D1_SCALE_PROP_CENTER_POINT</span></span><br/></td>
<td><span data-ttu-id="b4ece-134">Центральная точка масштабирования изображения.</span><span class="sxs-lookup"><span data-stu-id="b4ece-134">The image scaling center point.</span></span> <span data-ttu-id="b4ece-135">Это свойство является D2D1_VECTOR_2F, определенным как: (точка X, точка Y).</span><span class="sxs-lookup"><span data-stu-id="b4ece-135">This property is a D2D1_VECTOR_2F defined as: (point X, point Y).</span></span> <span data-ttu-id="b4ece-136">Единицы измерения — DIP.</span><span class="sxs-lookup"><span data-stu-id="b4ece-136">The units are in DIPs.</span></span><br/> <span data-ttu-id="b4ece-137">Используйте свойство центральной точки для масштабирования вокруг точки, отличной от верхнего левого угла.</span><span class="sxs-lookup"><span data-stu-id="b4ece-137">Use the center point property to scale around a point other than the upper-left corner.</span></span><br/> <span data-ttu-id="b4ece-138">Тип — D2D1_VECTOR_2F.</span><span class="sxs-lookup"><span data-stu-id="b4ece-138">The type is D2D1_VECTOR_2F.</span></span><br/> <span data-ttu-id="b4ece-139">Значение по умолчанию — {0.0 f, 0,0 f}.</span><span class="sxs-lookup"><span data-stu-id="b4ece-139">The default value is {0.0f, 0.0f}.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b4ece-140">бордермоде</span><span class="sxs-lookup"><span data-stu-id="b4ece-140">BorderMode</span></span><br/> <span data-ttu-id="b4ece-141">D2D1_SCALE_PROP_BORDER_MODE</span><span class="sxs-lookup"><span data-stu-id="b4ece-141">D2D1_SCALE_PROP_BORDER_MODE</span></span><br/></td>
<td><span data-ttu-id="b4ece-142">Режим, используемый для вычисления границы изображения: Soft или Hard.</span><span class="sxs-lookup"><span data-stu-id="b4ece-142">The mode used to calculate the border of the image, soft or hard.</span></span> <span data-ttu-id="b4ece-143">Дополнительные сведения см. в разделе <a href="#border-modes">режимы границ</a> .</span><span class="sxs-lookup"><span data-stu-id="b4ece-143">See <a href="#border-modes">Border modes</a> for more info.</span></span> <br/> <span data-ttu-id="b4ece-144">Тип — D2D1_BORDER_MODE.</span><span class="sxs-lookup"><span data-stu-id="b4ece-144">The type is D2D1_BORDER_MODE.</span></span><br/> <span data-ttu-id="b4ece-145">Значение по умолчанию — D2D1_BORDER_MODE_SOFT.</span><span class="sxs-lookup"><span data-stu-id="b4ece-145">The default value is D2D1_BORDER_MODE_SOFT.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b4ece-146">Четкость</span><span class="sxs-lookup"><span data-stu-id="b4ece-146">Sharpness</span></span><br/> <span data-ttu-id="b4ece-147">D2D1_SCALE_PROP_SHARPNESS</span><span class="sxs-lookup"><span data-stu-id="b4ece-147">D2D1_SCALE_PROP_SHARPNESS</span></span><br/></td>
<td><span data-ttu-id="b4ece-148">В режиме интерполяции высокого качества кубический уровень резкости фильтра масштабирования в виде числа с плавающей запятой в диапазоне от 0 до 1.</span><span class="sxs-lookup"><span data-stu-id="b4ece-148">In the high quality cubic interpolation mode, the sharpness level of the scaling filter as a float between 0 and 1.</span></span> <span data-ttu-id="b4ece-149">Значения являются безмодульными.</span><span class="sxs-lookup"><span data-stu-id="b4ece-149">The values are unitless.</span></span> <span data-ttu-id="b4ece-150">Резкость можно использовать для настройки качества изображения при уменьшении масштаба изображения.</span><span class="sxs-lookup"><span data-stu-id="b4ece-150">You can use sharpness to adjust the quality of an image when you scale the image down.</span></span><br/> <span data-ttu-id="b4ece-151">Коэффициент резкости влияет на форму ядра.</span><span class="sxs-lookup"><span data-stu-id="b4ece-151">The sharpness factor affects the shape of the kernel.</span></span> <span data-ttu-id="b4ece-152">Чем выше коэффициент резкости, тем меньше ядро.</span><span class="sxs-lookup"><span data-stu-id="b4ece-152">The higher the sharpness factor, the smaller the kernel.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="b4ece-153">Это свойство влияет только на режим интерполяции высокого качества.</span><span class="sxs-lookup"><span data-stu-id="b4ece-153">This property affects only the high quality cubic interpolation mode.</span></span>
</blockquote>
<br/> <span data-ttu-id="b4ece-154">Тип — FLOAT.</span><span class="sxs-lookup"><span data-stu-id="b4ece-154">The type is FLOAT.</span></span><br/> <span data-ttu-id="b4ece-155">Значение по умолчанию — 0,0 f.</span><span class="sxs-lookup"><span data-stu-id="b4ece-155">The default value is 0.0f.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b4ece-156">интерполатионмоде</span><span class="sxs-lookup"><span data-stu-id="b4ece-156">InterpolationMode</span></span><br/> <span data-ttu-id="b4ece-157">D2D1_SCALE_PROP_INTERPOLATION_MODE</span><span class="sxs-lookup"><span data-stu-id="b4ece-157">D2D1_SCALE_PROP_INTERPOLATION_MODE</span></span><br/></td>
<td><span data-ttu-id="b4ece-158">Режим интерполяции, который применяется для масштабирования изображения.</span><span class="sxs-lookup"><span data-stu-id="b4ece-158">The interpolation mode the effect uses to scale the image.</span></span> <span data-ttu-id="b4ece-159">Существует 6 режимов масштабирования, которые имеют высокое качество и скорость.</span><span class="sxs-lookup"><span data-stu-id="b4ece-159">There are 6 scale modes that range in quality and speed.</span></span> <span data-ttu-id="b4ece-160">Дополнительные сведения см. в разделе <a href="#interpolation-modes">режимы интерполяции</a> .</span><span class="sxs-lookup"><span data-stu-id="b4ece-160">See <a href="#interpolation-modes">Interpolation modes</a> for more info.</span></span> <br/> <span data-ttu-id="b4ece-161">Тип — D2D1_SCALE_INTERPOLATION_MODE.</span><span class="sxs-lookup"><span data-stu-id="b4ece-161">The type is D2D1_SCALE_INTERPOLATION_MODE.</span></span><br/> <span data-ttu-id="b4ece-162">Значение по умолчанию — D2D1_SCALE_INTERPOLATION_MODE_LINEAR.</span><span class="sxs-lookup"><span data-stu-id="b4ece-162">The default value is D2D1_SCALE_INTERPOLATION_MODE_LINEAR.</span></span><br/></td>
</tr>
</tbody>
</table>



 

### <a name="border-modes"></a><span data-ttu-id="b4ece-163">Режимы границ</span><span class="sxs-lookup"><span data-stu-id="b4ece-163">Border modes</span></span>



| <span data-ttu-id="b4ece-164">Имя</span><span class="sxs-lookup"><span data-stu-id="b4ece-164">Name</span></span>                     | <span data-ttu-id="b4ece-165">Описание</span><span class="sxs-lookup"><span data-stu-id="b4ece-165">Description</span></span>                                                                                                                                                                                                                                                              |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4ece-166">\_ \_ Мягкий режим границы \_ D2D1</span><span class="sxs-lookup"><span data-stu-id="b4ece-166">D2D1\_BORDER\_MODE\_SOFT</span></span> | <span data-ttu-id="b4ece-167">При применении ядра свертки к входному изображению применяются прозрачные черные пиксели для выборки за пределами входных данных.</span><span class="sxs-lookup"><span data-stu-id="b4ece-167">The effect pads the input image with transparent black pixels for samples outside of the input bounds when it applies the convolution kernel.</span></span> <span data-ttu-id="b4ece-168">При этом создается мягкая сторона для изображения, а в процессе разворачивается точечный рисунок с размером ядра.</span><span class="sxs-lookup"><span data-stu-id="b4ece-168">This creates a soft edge for the image, and in the process expands the output bitmap by the size of the kernel.</span></span><br/> |
| <span data-ttu-id="b4ece-169">Жесткое D2D1 в \_ \_ режиме границы \_</span><span class="sxs-lookup"><span data-stu-id="b4ece-169">D2D1\_BORDER\_MODE\_HARD</span></span> | <span data-ttu-id="b4ece-170">Этот результат расширяет входной образ с помощью преобразования границы зеркального типа для выборок за пределами входных данных.</span><span class="sxs-lookup"><span data-stu-id="b4ece-170">The effect extends the input image with a mirror-type border transform for samples outside of the input bounds.</span></span> <span data-ttu-id="b4ece-171">Размер выходного растрового изображения равен размеру входного точечного рисунка.</span><span class="sxs-lookup"><span data-stu-id="b4ece-171">The size of the output bitmap is equal to the size of the input bitmap.</span></span><br/>                                                                       |



 

\`

## <a name="interpolation-modes"></a><span data-ttu-id="b4ece-172">Режимы интерполяции</span><span class="sxs-lookup"><span data-stu-id="b4ece-172">Interpolation modes</span></span>



| <span data-ttu-id="b4ece-173">Перечисление</span><span class="sxs-lookup"><span data-stu-id="b4ece-173">Enumeration</span></span>                                             | <span data-ttu-id="b4ece-174">Описание</span><span class="sxs-lookup"><span data-stu-id="b4ece-174">Description</span></span>                                                                                                                                                                                          |
|---------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4ece-175">D2D1 \_ \_ Режим интерполяции масштабирования, \_ \_ ближайший \_ сосед</span><span class="sxs-lookup"><span data-stu-id="b4ece-175">D2D1\_SCALE\_INTERPOLATION\_MODE\_NEAREST\_NEIGHBOR</span></span>     | <span data-ttu-id="b4ece-176">Выбирает ближайшую одиночную точку и использует ее.</span><span class="sxs-lookup"><span data-stu-id="b4ece-176">Samples the nearest single point and uses that.</span></span> <span data-ttu-id="b4ece-177">В этом режиме используется меньше времени на обработку, но выводится изображение самого низкого качества.</span><span class="sxs-lookup"><span data-stu-id="b4ece-177">This mode uses less processing time, but outputs the lowest quality image.</span></span>                                                                           |
| <span data-ttu-id="b4ece-178">\_ \_ Линейный режим интерполяции D2D1 Scale \_ \_</span><span class="sxs-lookup"><span data-stu-id="b4ece-178">D2D1\_SCALE\_INTERPOLATION\_MODE\_LINEAR</span></span>                | <span data-ttu-id="b4ece-179">Использует выборку с четырьмя точками и линейную интерполяцию.</span><span class="sxs-lookup"><span data-stu-id="b4ece-179">Uses a four point sample and linear interpolation.</span></span> <span data-ttu-id="b4ece-180">Этот режим использует больше времени на обработку, чем ближайший соседний режим, но выводит изображение более высокого качества.</span><span class="sxs-lookup"><span data-stu-id="b4ece-180">This mode uses more processing time than the nearest neighbor mode, but outputs a higher quality image.</span></span>                                           |
| <span data-ttu-id="b4ece-181">D2D1 \_ \_ Режим интерполяции масштабирования, \_ \_ кубический</span><span class="sxs-lookup"><span data-stu-id="b4ece-181">D2D1\_SCALE\_INTERPOLATION\_MODE\_CUBIC</span></span>                 | <span data-ttu-id="b4ece-182">Использует 16-примерный ядро кубических для интерполяции.</span><span class="sxs-lookup"><span data-stu-id="b4ece-182">Uses a 16 sample cubic kernel for interpolation.</span></span> <span data-ttu-id="b4ece-183">Этот режим использует наибольшее время обработки, но выводит изображение с более высоким качеством.</span><span class="sxs-lookup"><span data-stu-id="b4ece-183">This mode uses the most processing time, but outputs a higher quality image.</span></span>                                                                        |
| <span data-ttu-id="b4ece-184">D2D1 \_ \_ Режим интерполяции \_ с \_ несколькими \_ образцами \_</span><span class="sxs-lookup"><span data-stu-id="b4ece-184">D2D1\_SCALE\_INTERPOLATION\_MODE\_MULTI\_SAMPLE\_LINEAR</span></span> | <span data-ttu-id="b4ece-185">Использует 4 линейных образца в пределах одного пикселя для удобного сглаживания.</span><span class="sxs-lookup"><span data-stu-id="b4ece-185">Uses 4 linear samples within a single pixel for good edge anti-aliasing.</span></span> <span data-ttu-id="b4ece-186">Этот режим хорошо подходит для уменьшения масштаба по небольшим объемам на изображениях с небольшими пикселями.</span><span class="sxs-lookup"><span data-stu-id="b4ece-186">This mode is good for scaling down by small amounts on images with few pixels.</span></span>                                              |
| <span data-ttu-id="b4ece-187">D2D1 \_ \_ Режим интерполяции масштабирования — \_ \_ анизотропная</span><span class="sxs-lookup"><span data-stu-id="b4ece-187">D2D1\_SCALE\_INTERPOLATION\_MODE\_ANISOTROPIC</span></span>           | <span data-ttu-id="b4ece-188">Использует анизотропную фильтрацию для выборки шаблона в соответствии с преобразованной формой точечного рисунка.</span><span class="sxs-lookup"><span data-stu-id="b4ece-188">Uses anisotropic filtering to sample a pattern according to the transformed shape of the bitmap.</span></span>                                                                                                     |
| <span data-ttu-id="b4ece-189">D2D1 \_ \_ Режим интерполяции \_ с \_ высоким \_ качеством в \_ кубических масштабах</span><span class="sxs-lookup"><span data-stu-id="b4ece-189">D2D1\_SCALE\_INTERPOLATION\_MODE\_HIGH\_QUALITY\_CUBIC</span></span>  | <span data-ttu-id="b4ece-190">Использует высококачественное ядро кубического размера для выполнения предварительно довнскале образа, если довнскалинг участвует в матрице преобразования.</span><span class="sxs-lookup"><span data-stu-id="b4ece-190">Uses a variable size high quality cubic kernel to perform a pre-downscale the image if downscaling is involved in the transform matrix.</span></span> <span data-ttu-id="b4ece-191">Затем использует режим интерполяции кубических для окончательного вывода.</span><span class="sxs-lookup"><span data-stu-id="b4ece-191">Then uses the cubic interpolation mode for the final output.</span></span> |



 

> [!Note]  
> <span data-ttu-id="b4ece-192">Если не выбрать режим, по умолчанию применяется \_ \_ Режим интерполяции D2D1 Scale \_ \_ линейный.</span><span class="sxs-lookup"><span data-stu-id="b4ece-192">If you don't select a mode, the effect defaults to D2D1\_SCALE\_INTERPOLATION\_MODE\_LINEAR.</span></span>

 

> [!Note]  
> <span data-ttu-id="b4ece-193">В режиме анизотропного масштабирования создается MIP-карты при масштабировании, однако если для свойства **кэширования** задано значение true для эффектов, вводимых в результате этого эффекта, MIP-карты не будет создаваться каждый раз для достаточного размера изображений.</span><span class="sxs-lookup"><span data-stu-id="b4ece-193">Anisotropic mode generates mipmaps when scaling, however, if you set the **Cached** property to true on the effects that are input to this effect, the mipmaps won't be generated every time for sufficiently small images.</span></span>

 

## <a name="output-bitmap"></a><span data-ttu-id="b4ece-194">Битовая карта вывода</span><span class="sxs-lookup"><span data-stu-id="b4ece-194">Output bitmap</span></span>

<span data-ttu-id="b4ece-195">Расположение и размер выходного растрового изображения зависит от указанного коэффициента масштабирования и центральной точки.</span><span class="sxs-lookup"><span data-stu-id="b4ece-195">The location and size of the output bitmap depends on the specified scale factor and the center point.</span></span>

<span data-ttu-id="b4ece-196">Вы можете вычислить размер выходного растрового изображения с помощью этого уравнения:</span><span class="sxs-lookup"><span data-stu-id="b4ece-196">You can calculate the size of the output bitmap using this equation:</span></span><dl> <span data-ttu-id="b4ece-197">Битмапсизе? (ПКС) = масштабировать? \* Размер исходного растрового изображения?</span><span class="sxs-lookup"><span data-stu-id="b4ece-197">BitmapSize?(Pixels)=Scale?\*Original Bitmap Size?</span></span> <span data-ttu-id="b4ece-198">(DIP) \* (Усердпи/96)</span><span class="sxs-lookup"><span data-stu-id="b4ece-198">(DIPs)\*(UserDPI/96)</span></span>  
<span data-ttu-id="b4ece-199">Битмапсизе<sub>y</sub>(пиксели) =<sub>масштаб</sub> \* исходного точечного<sub></sub> рисунка y (DIP) \* (усердпи/96)</span><span class="sxs-lookup"><span data-stu-id="b4ece-199">BitmapSize<sub>y</sub>(Pixels)=Scale<sub>y</sub>\*Original Bitmap Size<sub>y</sub> (DIPs)\*(UserDPI/96)</span></span>  
</dl>

<span data-ttu-id="b4ece-200">Результат округляет доли пикселов до ближайшего целого пикселя.</span><span class="sxs-lookup"><span data-stu-id="b4ece-200">The effect rounds fractions of pixels up to the nearest whole pixel.</span></span>

<span data-ttu-id="b4ece-201">Расположение точечного рисунка равно (0, 0) или значению свойства центральной точки.</span><span class="sxs-lookup"><span data-stu-id="b4ece-201">The location of the bitmap is (0, 0) or the value of the center point property.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4ece-202">Требования</span><span class="sxs-lookup"><span data-stu-id="b4ece-202">Requirements</span></span>



| <span data-ttu-id="b4ece-203">Требование</span><span class="sxs-lookup"><span data-stu-id="b4ece-203">Requirement</span></span> | <span data-ttu-id="b4ece-204">Значение</span><span class="sxs-lookup"><span data-stu-id="b4ece-204">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b4ece-205">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b4ece-205">Minimum supported client</span></span> | <span data-ttu-id="b4ece-206">Windows 8 и обновление платформы для \[ классических приложений Windows 7 \| приложения для Магазина Windows\]</span><span class="sxs-lookup"><span data-stu-id="b4ece-206">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="b4ece-207">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b4ece-207">Minimum supported server</span></span> | <span data-ttu-id="b4ece-208">Windows 8 и обновление платформы для \[ классических приложений Windows 7 \| приложения для Магазина Windows\]</span><span class="sxs-lookup"><span data-stu-id="b4ece-208">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="b4ece-209">Header</span><span class="sxs-lookup"><span data-stu-id="b4ece-209">Header</span></span>                   | <span data-ttu-id="b4ece-210">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="b4ece-210">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="b4ece-211">Библиотека</span><span class="sxs-lookup"><span data-stu-id="b4ece-211">Library</span></span>                  | <span data-ttu-id="b4ece-212">D2D1. lib, дксгуид. lib</span><span class="sxs-lookup"><span data-stu-id="b4ece-212">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="b4ece-213">См. также</span><span class="sxs-lookup"><span data-stu-id="b4ece-213">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b4ece-214">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="b4ece-214">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

