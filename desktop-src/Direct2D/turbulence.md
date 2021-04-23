---
title: Турбуленце, результат
description: Используйте турбуленценый результат для создания точечного рисунка на основе функции шума Perl.
ms.assetid: 86C1990E-958C-46D7-840A-E4A17F1D1740
keywords:
- турбуленце, результат
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61f67f615ec5b68ca285a048b68bc7bc8eab6e24
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/04/2021
ms.locfileid: "104571546"
---
# <a name="turbulence-effect"></a><span data-ttu-id="71052-104">Турбуленце, результат</span><span class="sxs-lookup"><span data-stu-id="71052-104">Turbulence effect</span></span>

<span data-ttu-id="71052-105">Используйте турбуленценый результат для создания точечного рисунка на основе функции шума Perl.</span><span class="sxs-lookup"><span data-stu-id="71052-105">Use the turbulence effect to generate a bitmap based on the Perlin noise function.</span></span>

<span data-ttu-id="71052-106">У влияния турбуленце нет входного изображения.</span><span class="sxs-lookup"><span data-stu-id="71052-106">The turbulence effect has no input image.</span></span>

<span data-ttu-id="71052-107">Идентификатором CLSID для этого действия является CLSID \_ D2D1Turbulence.</span><span class="sxs-lookup"><span data-stu-id="71052-107">The CLSID for this effect is CLSID\_D2D1Turbulence.</span></span>

-   [<span data-ttu-id="71052-108">Пример изображения</span><span class="sxs-lookup"><span data-stu-id="71052-108">Example image</span></span>](#example-image)
-   [<span data-ttu-id="71052-109">Свойства эффектов</span><span class="sxs-lookup"><span data-stu-id="71052-109">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="71052-110">Режимы шума</span><span class="sxs-lookup"><span data-stu-id="71052-110">Noise modes</span></span>](#noise-modes)
-   [<span data-ttu-id="71052-111">Битовая карта вывода</span><span class="sxs-lookup"><span data-stu-id="71052-111">Output bitmap</span></span>](#output-bitmap)
-   [<span data-ttu-id="71052-112">Требования</span><span class="sxs-lookup"><span data-stu-id="71052-112">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="71052-113">См. также</span><span class="sxs-lookup"><span data-stu-id="71052-113">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="71052-114">Пример изображения</span><span class="sxs-lookup"><span data-stu-id="71052-114">Example image</span></span>

![снимок экрана примера эффектов, показывающий выходные данные турбуленценого действия.](images/32-turbulence.png)

<span data-ttu-id="71052-116">Турбуленценый результат вычисляет сумму одного или нескольких октав функции шума Perl.</span><span class="sxs-lookup"><span data-stu-id="71052-116">The Turbulence effect computes the sum of one or more octaves of the Perlin noise function.</span></span> <span data-ttu-id="71052-117">Шум Perl — это функция псевдо-Random, значение которой зависит от частоты, расположения и начального значения.</span><span class="sxs-lookup"><span data-stu-id="71052-117">Perlin noise is a pseudo-random function whose value depends on the frequency, position, and seed value.</span></span> <span data-ttu-id="71052-118">Этот результат создает значения RGBA с помощью одного из этих уравнений.</span><span class="sxs-lookup"><span data-stu-id="71052-118">The effect generates the RGBA values using one of these equations.</span></span>

<span data-ttu-id="71052-119">При выборе \_ режима шума D2D1 турбуленце "сумма помех" \_ \_ \_ в результате используется это уравнение.</span><span class="sxs-lookup"><span data-stu-id="71052-119">If you select the D2D1\_TURBULENCE\_NOISE\_FRACTAL\_SUM noise mode the effect uses this equation.</span></span>

![Снимок экрана, на котором показана функция турбуленце, используемая для создания точечного рисунка.](images/turbulence-equation1.png)

<span data-ttu-id="71052-121">Если выбрать \_ режим шума ТУРБУЛЕНЦЕ D2D1 \_ турбуленце \_ , то в результате будет использоваться это уравнение.</span><span class="sxs-lookup"><span data-stu-id="71052-121">If you select the D2D1\_TURBULENCE\_NOISE\_TURBULENCE noise mode the effect uses this equation.</span></span>

![Функция турбуленце, используемая для создания точечного рисунка.](images/turbulence-equation2.png)

> [!Note]  
> <span data-ttu-id="71052-123">`PerlinNoise`Функция имеет диапазон \[ -1, 1 \] .</span><span class="sxs-lookup"><span data-stu-id="71052-123">The `PerlinNoise` function has a range of \[-1, 1\].</span></span>

 

<span data-ttu-id="71052-124">Этот результат выводит значения пикселей в предварительно умноженном альфа-канале.</span><span class="sxs-lookup"><span data-stu-id="71052-124">This effect outputs pixel values in premultiplied alpha.</span></span>

## <a name="effect-properties"></a><span data-ttu-id="71052-125">Свойства эффектов</span><span class="sxs-lookup"><span data-stu-id="71052-125">Effect properties</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="71052-126">Отображаемое имя и перечисление индекса</span><span class="sxs-lookup"><span data-stu-id="71052-126">Display name and index enumeration</span></span></th>
<th><span data-ttu-id="71052-127">Описание</span><span class="sxs-lookup"><span data-stu-id="71052-127">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="71052-128">Offset</span><span class="sxs-lookup"><span data-stu-id="71052-128">Offset</span></span><br/> <span data-ttu-id="71052-129">D2D1_TURBULENCE_PROP_OFFSET</span><span class="sxs-lookup"><span data-stu-id="71052-129">D2D1_TURBULENCE_PROP_OFFSET</span></span><br/></td>
<td><span data-ttu-id="71052-130">Координаты, в которых создаются выходные данные турбуленце.</span><span class="sxs-lookup"><span data-stu-id="71052-130">The coordinates where the turbulence output is generated.</span></span><br/> <span data-ttu-id="71052-131">Алгоритм, используемый для создания шума в Perl, зависит от позиции, поэтому другое смещение приводит к различным выходным данным.</span><span class="sxs-lookup"><span data-stu-id="71052-131">The algorithm used to generate the Perlin noise is position dependent, so a different offset results in a different output.</span></span> <span data-ttu-id="71052-132">Это свойство не привязано, а единицы измерения указаны в параметрах DIP</span><span class="sxs-lookup"><span data-stu-id="71052-132">This property is not bounded and the units are specified in DIPs</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="71052-133">Смещение не имеет того же результата, что и преобразование, так как выходные данные функции шума имеют бесконечное значение, а функция обходит плитку.</span><span class="sxs-lookup"><span data-stu-id="71052-133">The offset does not have the same effect as a translation because the noise function output is infinite and the function will wrap around the tile.</span></span>
</blockquote>
<br/> <span data-ttu-id="71052-134">Тип — D2D1_VECTOR_2F.</span><span class="sxs-lookup"><span data-stu-id="71052-134">The type is D2D1_VECTOR_2F.</span></span><br/> <span data-ttu-id="71052-135">Значение по умолчанию — {0.0 f, 0,0 f}.</span><span class="sxs-lookup"><span data-stu-id="71052-135">The default value is {0.0f, 0.0f}.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71052-136">Размер</span><span class="sxs-lookup"><span data-stu-id="71052-136">Size</span></span><br/> <span data-ttu-id="71052-137">D2D1_TURBULENCE_PROP_SIZE</span><span class="sxs-lookup"><span data-stu-id="71052-137">D2D1_TURBULENCE_PROP_SIZE</span></span><br/></td>
<td><span data-ttu-id="71052-138">Размер выходных данных турбуленце.</span><span class="sxs-lookup"><span data-stu-id="71052-138">The size of the turbulence output.</span></span><br/> <span data-ttu-id="71052-139">Это свойство не привязано, а единицы измерения указаны в параметрах DIP</span><span class="sxs-lookup"><span data-stu-id="71052-139">This property is not bounded and the units are specified in DIPs</span></span> <br/>
<br/> <span data-ttu-id="71052-140">Тип — D2D1_VECTOR_2F.</span><span class="sxs-lookup"><span data-stu-id="71052-140">The type is D2D1_VECTOR_2F.</span></span><br/> <span data-ttu-id="71052-141">Значение по умолчанию — {0.0 f, 0,0 f}.</span><span class="sxs-lookup"><span data-stu-id="71052-141">The default value is {0.0f, 0.0f}.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71052-142">басефрекуенци</span><span class="sxs-lookup"><span data-stu-id="71052-142">BaseFrequency</span></span><br/> <span data-ttu-id="71052-143">D2D1_TURBULENCE_PROP_BASE_FREQUENCY</span><span class="sxs-lookup"><span data-stu-id="71052-143">D2D1_TURBULENCE_PROP_BASE_FREQUENCY</span></span><br/></td>
<td><span data-ttu-id="71052-144">Базовые частоты в направлении X и Y.</span><span class="sxs-lookup"><span data-stu-id="71052-144">The base frequencies in the X and Y direction.</span></span> <span data-ttu-id="71052-145">Это свойство имеет тип float и должно быть больше 0.</span><span class="sxs-lookup"><span data-stu-id="71052-145">This property is a float and must be greater than 0.</span></span> <span data-ttu-id="71052-146">Единицы указываются в 1/DIP.</span><span class="sxs-lookup"><span data-stu-id="71052-146">The units are specified in 1/DIPs.</span></span> <br/> <span data-ttu-id="71052-147">Значение 1 (1/DIP) для базовой частоты приводит к получению помех в Perl для завершения всего цикла между двумя пикселями.</span><span class="sxs-lookup"><span data-stu-id="71052-147">A value of 1 (1/DIPs) for the base frequency results in the Perlin noise completing an entire cycle between two pixels.</span></span> <span data-ttu-id="71052-148">Простота интерполяции этих точек приводит к совершенно случайным пикселям, так как между пикселями нет никакой корреляции.</span><span class="sxs-lookup"><span data-stu-id="71052-148">The ease interpolation for these pixels results in completely random pixels, since there is no correlation between the pixels.</span></span><br/> <span data-ttu-id="71052-149">При значении 0,1 (1/DIP) для базовой частоты функция шума Perl повторяется каждые 10 DIP.</span><span class="sxs-lookup"><span data-stu-id="71052-149">A value of 0.1(1/DIPs) for the base frequency, the Perlin noise function repeats every 10 DIPs.</span></span> <span data-ttu-id="71052-150">Это приводит к получению корреляции между пикселями, а типичный турбуленце-результат является видимым.</span><span class="sxs-lookup"><span data-stu-id="71052-150">This results in correlation between pixels and the typical turbulence effect is visible.</span></span><br/> <span data-ttu-id="71052-151">Тип — D2D1_VECTOR_2F.</span><span class="sxs-lookup"><span data-stu-id="71052-151">The type is D2D1_VECTOR_2F.</span></span><br/> <span data-ttu-id="71052-152">Значение по умолчанию — {0,01 f, 0,01 f}.</span><span class="sxs-lookup"><span data-stu-id="71052-152">The default value is {0.01f, 0.01f}.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71052-153">нумоктавес</span><span class="sxs-lookup"><span data-stu-id="71052-153">NumOctaves</span></span><br/> <span data-ttu-id="71052-154">D2D1_TURBULENCE_PROP_NUM_OCTAVES</span><span class="sxs-lookup"><span data-stu-id="71052-154">D2D1_TURBULENCE_PROP_NUM_OCTAVES</span></span><br/></td>
<td><span data-ttu-id="71052-155">Число октав для функции noise.</span><span class="sxs-lookup"><span data-stu-id="71052-155">The number of octaves for the noise function.</span></span> <span data-ttu-id="71052-156">Это свойство является UINT32 и должно быть больше 0.</span><span class="sxs-lookup"><span data-stu-id="71052-156">This property is a UINT32 and must be greater than 0.</span></span><br/> <span data-ttu-id="71052-157">Тип — UINT32.</span><span class="sxs-lookup"><span data-stu-id="71052-157">The type is UINT32.</span></span><br/> <span data-ttu-id="71052-158">Значение по умолчанию — 1.</span><span class="sxs-lookup"><span data-stu-id="71052-158">The default value is 1.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71052-159">Seed</span><span class="sxs-lookup"><span data-stu-id="71052-159">Seed</span></span><br/> <span data-ttu-id="71052-160">D2D1_TURBULENCE_PROP_SEED</span><span class="sxs-lookup"><span data-stu-id="71052-160">D2D1_TURBULENCE_PROP_SEED</span></span><br/></td>
<td><span data-ttu-id="71052-161">Начальное значение генератора псевдослучайных чисел.</span><span class="sxs-lookup"><span data-stu-id="71052-161">The seed for the pseudo random generator.</span></span> <span data-ttu-id="71052-162">Это свойство не ограничено.</span><span class="sxs-lookup"><span data-stu-id="71052-162">This property is unbounded.</span></span><br/> <span data-ttu-id="71052-163">Тип — UINT32.</span><span class="sxs-lookup"><span data-stu-id="71052-163">The type is UINT32.</span></span><br/> <span data-ttu-id="71052-164">Значение по умолчанию — 0.</span><span class="sxs-lookup"><span data-stu-id="71052-164">The default value is 0.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71052-165">Помехи</span><span class="sxs-lookup"><span data-stu-id="71052-165">Noise</span></span><br/> <span data-ttu-id="71052-166">D2D1_TURBULENCE_PROP_NOISE</span><span class="sxs-lookup"><span data-stu-id="71052-166">D2D1_TURBULENCE_PROP_NOISE</span></span><br/></td>
<td><span data-ttu-id="71052-167">Режим шума турбуленце.</span><span class="sxs-lookup"><span data-stu-id="71052-167">The turbulence noise mode.</span></span> <span data-ttu-id="71052-168">Это свойство может быть либо <em>фракталом Sum</em> , либо <em>турбуленце</em>.</span><span class="sxs-lookup"><span data-stu-id="71052-168">This property can be either <em>fractal sum</em> or <em>turbulence</em>.</span></span> <span data-ttu-id="71052-169">Указывает, создавать ли точечный рисунок на основе шума фрактала или функции Турбуленце.</span><span class="sxs-lookup"><span data-stu-id="71052-169">Indicates whether to generate a bitmap based on Fractal Noise or the Turbulence function.</span></span> <span data-ttu-id="71052-170">Дополнительные сведения см. в разделе <a href="#noise-modes">режимы шума</a> .</span><span class="sxs-lookup"><span data-stu-id="71052-170">See <a href="#noise-modes">Noise modes</a> for more info.</span></span> <br/> <span data-ttu-id="71052-171">Тип — D2D1_TURBULENCE_NOISE.</span><span class="sxs-lookup"><span data-stu-id="71052-171">The type is D2D1_TURBULENCE_NOISE.</span></span><br/> <span data-ttu-id="71052-172">Значение по умолчанию — D2D1_TURBULENCE_NOISE_FRACTAL_SUM.</span><span class="sxs-lookup"><span data-stu-id="71052-172">The default value is D2D1_TURBULENCE_NOISE_FRACTAL_SUM.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71052-173">Сшивка</span><span class="sxs-lookup"><span data-stu-id="71052-173">Stitchable</span></span><br/> <span data-ttu-id="71052-174">D2D1_TURBULENCE_PROP_STITCHABLE</span><span class="sxs-lookup"><span data-stu-id="71052-174">D2D1_TURBULENCE_PROP_STITCHABLE</span></span><br/></td>
<td><span data-ttu-id="71052-175">Включает или выключает сшивания.</span><span class="sxs-lookup"><span data-stu-id="71052-175">Turns stitching on or off.</span></span> <span data-ttu-id="71052-176">Базовая частота корректируется таким образом, чтобы выходное растровое изображение можно было скомпоновать.</span><span class="sxs-lookup"><span data-stu-id="71052-176">The base frequency is adjusted so that output bitmap can be stitched.</span></span> <span data-ttu-id="71052-177">Это полезно, если требуется мозаичное заполнение нескольких копий выходных данных эффектов турбуленце.</span><span class="sxs-lookup"><span data-stu-id="71052-177">This is useful if you want to tile multiple copies of the turbulence effect output.</span></span>
<ul>
<li><span data-ttu-id="71052-178">True. Выходное растровое изображение может быть мозаичным (с помощью эффектов плитки) без внешнего вида пристыков.</span><span class="sxs-lookup"><span data-stu-id="71052-178">True   The output bitmap can be tiled (using the tile effect) without the appearance of seams.</span></span> <span data-ttu-id="71052-179">Базовая частота корректируется таким образом, чтобы выходное растровое изображение можно было скомпоновать.</span><span class="sxs-lookup"><span data-stu-id="71052-179">The base frequency is adjusted so that output bitmap can be stitched.</span></span></li>
<li><span data-ttu-id="71052-180">False. Базовая частота не корректируется, поэтому при мозаичном отображении точечного рисунка могут отображаться стыки.</span><span class="sxs-lookup"><span data-stu-id="71052-180">False   The base frequency is not adjusted, so seams may appear between tiles if the bitmap is tiled.</span></span></li>
</ul>
<br/> <span data-ttu-id="71052-181">Тип — BOOL.</span><span class="sxs-lookup"><span data-stu-id="71052-181">The type is BOOL.</span></span><br/> <span data-ttu-id="71052-182">Значение по умолчанию — FALSE.</span><span class="sxs-lookup"><span data-stu-id="71052-182">The default value is FALSE.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="noise-modes"></a><span data-ttu-id="71052-183">Режимы шума</span><span class="sxs-lookup"><span data-stu-id="71052-183">Noise modes</span></span>



| <span data-ttu-id="71052-184">Перечисление</span><span class="sxs-lookup"><span data-stu-id="71052-184">Enumeration</span></span>                           | <span data-ttu-id="71052-185">Описание</span><span class="sxs-lookup"><span data-stu-id="71052-185">Description</span></span>                                                                           |
|---------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="71052-186">\_ \_ \_ Сумма фрактала шума D2D1 турбуленце \_</span><span class="sxs-lookup"><span data-stu-id="71052-186">D2D1\_TURBULENCE\_NOISE\_FRACTAL\_SUM</span></span> | <span data-ttu-id="71052-187">Вычисляет сумму октав, сдвигя выходного диапазона от \[ -1, 1 \] до \[ 0, 1 \] .</span><span class="sxs-lookup"><span data-stu-id="71052-187">Computes a sum of the octaves, shifting the output range from \[-1, 1\], to \[0, 1\].</span></span> |
| <span data-ttu-id="71052-188">D2D1 \_ турбуленце \_ шум \_ турбуленце</span><span class="sxs-lookup"><span data-stu-id="71052-188">D2D1\_TURBULENCE\_NOISE\_TURBULENCE</span></span>   | <span data-ttu-id="71052-189">Вычисляет сумму абсолютного значения каждого Октава.</span><span class="sxs-lookup"><span data-stu-id="71052-189">Computes a sum of the absolute value of each octave.</span></span>                                  |



 

> [!Note]  
> <span data-ttu-id="71052-190">Ни один из режимов не содержит явный срез выходных значений.</span><span class="sxs-lookup"><span data-stu-id="71052-190">Neither mode contains an explicit clamp of the output values.</span></span>

 

## <a name="output-bitmap"></a><span data-ttu-id="71052-191">Битовая карта вывода</span><span class="sxs-lookup"><span data-stu-id="71052-191">Output bitmap</span></span>

<span data-ttu-id="71052-192">Этот результат приводит к созданию точечного рисунка с логически бесконечным размером.</span><span class="sxs-lookup"><span data-stu-id="71052-192">This effect generates a logically infinite sized bitmap.</span></span>

## <a name="requirements"></a><span data-ttu-id="71052-193">Требования</span><span class="sxs-lookup"><span data-stu-id="71052-193">Requirements</span></span>



| <span data-ttu-id="71052-194">Требование</span><span class="sxs-lookup"><span data-stu-id="71052-194">Requirement</span></span> | <span data-ttu-id="71052-195">Значение</span><span class="sxs-lookup"><span data-stu-id="71052-195">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="71052-196">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="71052-196">Minimum supported client</span></span> | <span data-ttu-id="71052-197">Windows 8 и обновление платформы для \[ классических приложений Windows 7 \| приложения для Магазина Windows\]</span><span class="sxs-lookup"><span data-stu-id="71052-197">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="71052-198">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="71052-198">Minimum supported server</span></span> | <span data-ttu-id="71052-199">Windows 8 и обновление платформы для \[ классических приложений Windows 7 \| приложения для Магазина Windows\]</span><span class="sxs-lookup"><span data-stu-id="71052-199">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="71052-200">Header</span><span class="sxs-lookup"><span data-stu-id="71052-200">Header</span></span>                   | <span data-ttu-id="71052-201">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="71052-201">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="71052-202">Библиотека</span><span class="sxs-lookup"><span data-stu-id="71052-202">Library</span></span>                  | <span data-ttu-id="71052-203">D2D1. lib, дксгуид. lib</span><span class="sxs-lookup"><span data-stu-id="71052-203">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="71052-204">См. также</span><span class="sxs-lookup"><span data-stu-id="71052-204">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="71052-205">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="71052-205">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

