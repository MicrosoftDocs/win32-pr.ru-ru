---
title: Эффект смешивания
description: Используйте эффекты смешения для объединения двух изображений. Этот результат имеет 26 режимов смешения.
ms.assetid: 39D8BAA3-8FF3-4F10-99A0-B26FCA3018AE
keywords:
- эффекты смешения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e248d1f7f41721d173510b8d10feac9be2e08f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892594"
---
# <a name="blend-effect"></a><span data-ttu-id="48a4f-105">Эффект смешивания</span><span class="sxs-lookup"><span data-stu-id="48a4f-105">Blend effect</span></span>

<span data-ttu-id="48a4f-106">Используйте эффекты смешения для объединения двух изображений.</span><span class="sxs-lookup"><span data-stu-id="48a4f-106">Use the blend effect to combine 2 images.</span></span> <span data-ttu-id="48a4f-107">Этот результат имеет 26 режимов смешения.</span><span class="sxs-lookup"><span data-stu-id="48a4f-107">This effect has 26 blend modes.</span></span>

<span data-ttu-id="48a4f-108">Идентификатором CLSID для этого действия является CLSID \_ D2D1Blend.</span><span class="sxs-lookup"><span data-stu-id="48a4f-108">The CLSID for this effect is CLSID\_D2D1Blend.</span></span>

-   [<span data-ttu-id="48a4f-109">Примеры смешения</span><span class="sxs-lookup"><span data-stu-id="48a4f-109">Blending examples</span></span>](#blending-examples)
-   [<span data-ttu-id="48a4f-110">Свойства эффектов</span><span class="sxs-lookup"><span data-stu-id="48a4f-110">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="48a4f-111">Режимы смешения</span><span class="sxs-lookup"><span data-stu-id="48a4f-111">Blend modes</span></span>](#blend-modes)
-   [<span data-ttu-id="48a4f-112">HSL. преобразование цветового пространства</span><span class="sxs-lookup"><span data-stu-id="48a4f-112">HSL color space conversions</span></span>](#hsl-color-space-conversions)
    -   [<span data-ttu-id="48a4f-113">Преобразование RGB в HSL</span><span class="sxs-lookup"><span data-stu-id="48a4f-113">Converting from RGB to HSL</span></span>](#converting-from-rgb-to-hsl)
    -   [<span data-ttu-id="48a4f-114">Преобразование из HSL в RGB</span><span class="sxs-lookup"><span data-stu-id="48a4f-114">Converting from HSL to RGB</span></span>](#converting-from-hsl-to-rgb)
-   [<span data-ttu-id="48a4f-115">Битовая карта вывода</span><span class="sxs-lookup"><span data-stu-id="48a4f-115">Output bitmap</span></span>](#output-bitmap)
-   [<span data-ttu-id="48a4f-116">Образец кода</span><span class="sxs-lookup"><span data-stu-id="48a4f-116">Sample code</span></span>](#sample-code)
-   [<span data-ttu-id="48a4f-117">Требования</span><span class="sxs-lookup"><span data-stu-id="48a4f-117">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="48a4f-118">См. также</span><span class="sxs-lookup"><span data-stu-id="48a4f-118">Related topics</span></span>](#related-topics)

## <a name="blending-examples"></a><span data-ttu-id="48a4f-119">Примеры смешения</span><span class="sxs-lookup"><span data-stu-id="48a4f-119">Blending examples</span></span>

<span data-ttu-id="48a4f-120">Ниже приведен пример изображения для каждого режима наложения в результате смешения.</span><span class="sxs-lookup"><span data-stu-id="48a4f-120">Here is an example image of every blend mode of the blend effect.</span></span> <span data-ttu-id="48a4f-121">Полный список режимов наложения и соответствующих свойств режима см. в следующем разделе.</span><span class="sxs-lookup"><span data-stu-id="48a4f-121">A full list of the blend modes and the corresponding mode properties are in the next section</span></span>

![снимок экрана с примерами эффектов для всех доступных режимов наложения.](images/blend-modes.png)

<span data-ttu-id="48a4f-123">Ниже приведен еще один пример использования режима исключения.</span><span class="sxs-lookup"><span data-stu-id="48a4f-123">Here is another example using the exclusion mode.</span></span>



| <span data-ttu-id="48a4f-124">До образа 1</span><span class="sxs-lookup"><span data-stu-id="48a4f-124">Before image 1</span></span>                                                             |
|----------------------------------------------------------------------------|
| ![Первое исходное изображение перед результатом.](images/default-before.jpg)    |
| <span data-ttu-id="48a4f-126">До изображения 2</span><span class="sxs-lookup"><span data-stu-id="48a4f-126">Before image 2</span></span>                                                             |
| ![Второе изображение перед результатом.](images/4-arthimetic-composite2.jpg) |
| <span data-ttu-id="48a4f-128">После</span><span class="sxs-lookup"><span data-stu-id="48a4f-128">After</span></span>                                                                      |
| ![изображение после преобразования.](images/5-blend.png)                      |



 


```C++
ComPtr<ID2D1Effect> blendEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Blend, &blendEffect);

blendEffect->SetInput(0, bitmap);
blendEffect->SetInput(1, bitmapTwo);
blendEffect->SetValue(D2D1_BLEND_PROP_MODE, D2D1_BLEND_MODE_EXCLUSION);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(blendEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a><span data-ttu-id="48a4f-130">Свойства эффектов</span><span class="sxs-lookup"><span data-stu-id="48a4f-130">Effect properties</span></span>



| <span data-ttu-id="48a4f-131">Отображаемое имя и перечисление индекса</span><span class="sxs-lookup"><span data-stu-id="48a4f-131">Display name and index enumeration</span></span>                 | <span data-ttu-id="48a4f-132">Описание</span><span class="sxs-lookup"><span data-stu-id="48a4f-132">Description</span></span>                                                                                                                                                                               |
|----------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="48a4f-133">Режим</span><span class="sxs-lookup"><span data-stu-id="48a4f-133">Mode</span></span><br/> <span data-ttu-id="48a4f-134">\_Режим D2D1 \_ Blend \_</span><span class="sxs-lookup"><span data-stu-id="48a4f-134">D2D1\_BLEND\_PROP\_MODE</span></span><br/> | <span data-ttu-id="48a4f-135">Режим смешения, используемый для этого результата.</span><span class="sxs-lookup"><span data-stu-id="48a4f-135">The blend mode used for the effect.</span></span> <span data-ttu-id="48a4f-136">Дополнительные сведения см. в разделе [режимы смешения](#blend-modes) .</span><span class="sxs-lookup"><span data-stu-id="48a4f-136">See [Blend modes](#blend-modes) for more info.</span></span> <span data-ttu-id="48a4f-137">Тип — D2D1 \_ Blend \_ .</span><span class="sxs-lookup"><span data-stu-id="48a4f-137">The type is D2D1\_BLEND\_MODE.</span></span><br/> <span data-ttu-id="48a4f-138">Значение по умолчанию — \_ D2D1 \_ Blend \_ .</span><span class="sxs-lookup"><span data-stu-id="48a4f-138">The default value is D2D1\_BLEND\_MODE\_MULTIPLY.</span></span><br/> |



 

## <a name="blend-modes"></a><span data-ttu-id="48a4f-139">Режимы смешения</span><span class="sxs-lookup"><span data-stu-id="48a4f-139">Blend modes</span></span>

<span data-ttu-id="48a4f-140">В таблице здесь показаны все режимы наложения этого результата.</span><span class="sxs-lookup"><span data-stu-id="48a4f-140">The table here shows all the blend modes of this effect.</span></span> <span data-ttu-id="48a4f-141">Вспомогательные функции, необходимые для расчета выходных данных этого результата, приведены в следующем разделе.</span><span class="sxs-lookup"><span data-stu-id="48a4f-141">The helper functions necessary to compute the output of the effect are in the next section.</span></span>

<span data-ttu-id="48a4f-142">Цвет: O <sub>пргб</sub>  =  *f*(f <sub>RGB</sub>, B <sub>RGB</sub>) \* f <sub>a</sub> \* B <sub>а</sub> + f <sub>RGB</sub> \* f <sub>a</sub> \* (1-B <sub>а</sub>) + B <sub>RGB</sub> \* B <sub>A</sub> \* (1 – f <sub>a</sub>)</span><span class="sxs-lookup"><span data-stu-id="48a4f-142">Color: O <sub>PRGB</sub> = *f*(F<sub>RGB</sub>, B<sub>RGB</sub>) \* F<sub>A</sub> \* B<sub>A</sub> + F<sub>RGB</sub> \* F<sub>A</sub> \* (1 - B<sub>A</sub>) + B<sub>RGB</sub> \* B<sub>A</sub> \* (1 - F<sub>A</sub>)</span></span>

<span data-ttu-id="48a4f-143">Альфа: O<sub>a</sub> = F<sub>A</sub> \* (1-B<sub>а</sub>) + B<sub>a</sub></span><span class="sxs-lookup"><span data-stu-id="48a4f-143">Alpha: O<sub>A</sub> = F<sub>A</sub> \* (1 - B<sub>A</sub>) + B<sub>A</sub></span></span>

<span data-ttu-id="48a4f-144">Где:</span><span class="sxs-lookup"><span data-stu-id="48a4f-144">Where:</span></span>

-   <span data-ttu-id="48a4f-145">O<sub>пргб</sub> — это предварительно умноженный выходной цвет</span><span class="sxs-lookup"><span data-stu-id="48a4f-145">O<sub>PRGB</sub> is the pre-multiplied output color</span></span>
-   <span data-ttu-id="48a4f-146">O<sub>A</sub> является выходным альфа-каналом</span><span class="sxs-lookup"><span data-stu-id="48a4f-146">O<sub>A</sub> is Output Alpha</span></span>
-   <span data-ttu-id="48a4f-147">B<sub>RGB</sub> — это непредварительно умноженный цвет назначения</span><span class="sxs-lookup"><span data-stu-id="48a4f-147">B<sub>RGB</sub> is the un-pre-multiplied destination color</span></span>
-   <span data-ttu-id="48a4f-148">Б<sub>— альфа-канал</sub> назначения</span><span class="sxs-lookup"><span data-stu-id="48a4f-148">B<sub>A</sub> is destination alpha</span></span>
-   <span data-ttu-id="48a4f-149">F<sub>RGB</sub> — это непредварительно умноженный исходный цвет</span><span class="sxs-lookup"><span data-stu-id="48a4f-149">F<sub>RGB</sub> is the un-pre-multiplied source color</span></span>
-   <span data-ttu-id="48a4f-150">F<sub>A</sub> — это альфа-версия источника</span><span class="sxs-lookup"><span data-stu-id="48a4f-150">F<sub>A</sub> is source alpha</span></span>
-   <span data-ttu-id="48a4f-151">*f*(<sub>RGB</sub>, D <sub>RGB</sub>) — это функция Blend, которая изменяется в зависимости от режима смешения</span><span class="sxs-lookup"><span data-stu-id="48a4f-151">*f*(S<sub>RGB</sub>, D<sub>RGB</sub>) is a blend function that varies per-blend-mode</span></span>

<span data-ttu-id="48a4f-152">Для некоторых режимов наложения требуется преобразование из цветового пространства оттенки, насыщенности, яркости (HSL) в RGB и обратно.</span><span class="sxs-lookup"><span data-stu-id="48a4f-152">Some of the blend modes require conversion to and from the hue, saturation, luminosity (HSL) color space to RGB.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="48a4f-153">Перечисление</span><span class="sxs-lookup"><span data-stu-id="48a4f-153">Enumeration</span></span></th>
<th><span data-ttu-id="48a4f-154">Дробь</span><span class="sxs-lookup"><span data-stu-id="48a4f-154">Equation</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="48a4f-155">D2D1_BLEND_MODE_DARKEN</span><span class="sxs-lookup"><span data-stu-id="48a4f-155">D2D1_BLEND_MODE_DARKEN</span></span></td>
<td><span data-ttu-id="48a4f-156">Базовая формула Blend только для Alpha.</span><span class="sxs-lookup"><span data-stu-id="48a4f-156">Basic blend formula for alpha only.</span></span> <img src="images/blend-mode-darken-1.png" alt="mathematical formula for a darken effect." /></td>
</tr>
<tr class="even">
<td><span data-ttu-id="48a4f-157">D2D1_BLEND_MODE_MULTIPLY</span><span class="sxs-lookup"><span data-stu-id="48a4f-157">D2D1_BLEND_MODE_MULTIPLY</span></span></td>
<td><span data-ttu-id="48a4f-158">Базовая формула Blend только для Alpha.</span><span class="sxs-lookup"><span data-stu-id="48a4f-158">Basic blend formula for alpha only.</span></span> <img src="images/blend-mode-multiply-1.png" alt="Mathematical formula for a mutiply effect." /></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="48a4f-159">D2D1_BLEND_MODE_COLOR_BURN</span><span class="sxs-lookup"><span data-stu-id="48a4f-159">D2D1_BLEND_MODE_COLOR_BURN</span></span></td>
<td><span data-ttu-id="48a4f-160">Основные формулы смешения с <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) =</span><span class="sxs-lookup"><span data-stu-id="48a4f-160">Basic blend formulas with <em>f</em>(F<sub>RGB</sub>, B<sub>RGB</sub>) =</span></span> <img src="images/blend-mode-colorburn-1.png" alt="Mathematical formula for a coor burn effect." /></td>
</tr>
<tr class="even">
<td><span data-ttu-id="48a4f-161">D2D1_BLEND_MODE_LINEAR_BURN</span><span class="sxs-lookup"><span data-stu-id="48a4f-161">D2D1_BLEND_MODE_LINEAR_BURN</span></span></td>
<td><span data-ttu-id="48a4f-162">Основные формулы смешения с <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) =</span><span class="sxs-lookup"><span data-stu-id="48a4f-162">Basic blend formulas with <em>f</em>(F<sub>RGB</sub>, B<sub>RGB</sub>) =</span></span> <img src="images/blend-mode-linearburn-1.png" alt="Mathematical formula for a linear burn effect." /></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="48a4f-163">D2D1_BLEND_MODE_DARKER_COLOR</span><span class="sxs-lookup"><span data-stu-id="48a4f-163">D2D1_BLEND_MODE_DARKER_COLOR</span></span></td>
<td><span data-ttu-id="48a4f-164">Базовая формула Blend только для Alpha.</span><span class="sxs-lookup"><span data-stu-id="48a4f-164">Basic blend formula for alpha only.</span></span> <img src="images/blend-mode-darkencolor-1.png" alt="Mathematical formla for a darken color effect." /></td>
</tr>
<tr class="even">
<td><span data-ttu-id="48a4f-165">D2D1_BLEND_MODE_LIGHTEN</span><span class="sxs-lookup"><span data-stu-id="48a4f-165">D2D1_BLEND_MODE_LIGHTEN</span></span></td>
<td><span data-ttu-id="48a4f-166">Базовая формула Blend только для Alpha.</span><span class="sxs-lookup"><span data-stu-id="48a4f-166">Basic blend formula for alpha only.</span></span> <img src="images/blend-mode-lighten-1.png" alt="Mathematical formula for a lighten effect." /></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="48a4f-167">D2D1_BLEND_MODE_SCREEN</span><span class="sxs-lookup"><span data-stu-id="48a4f-167">D2D1_BLEND_MODE_SCREEN</span></span></td>
<td><span data-ttu-id="48a4f-168">Базовая формула Blend только для Alpha.</span><span class="sxs-lookup"><span data-stu-id="48a4f-168">Basic blend formula for alpha only.</span></span> <img src="images/blend-mode-screen-1.png" alt="Mathematical formula for a screen effect." /></td>
</tr>
<tr class="even">
<td><span data-ttu-id="48a4f-169">D2D1_BLEND_MODE_COLOR_DODGE</span><span class="sxs-lookup"><span data-stu-id="48a4f-169">D2D1_BLEND_MODE_COLOR_DODGE</span></span></td>
<td><span data-ttu-id="48a4f-170">Основные формулы смешения с <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) =</span><span class="sxs-lookup"><span data-stu-id="48a4f-170">Basic blend formulas with <em>f</em>(F<sub>RGB</sub>, B<sub>RGB</sub>) =</span></span> <img src="images/blend-mode-colordodge-1.png" alt="Mathematical formula for a color dodge effect." /></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="48a4f-171">D2D1_BLEND_MODE_LINEAR_DODGE</span><span class="sxs-lookup"><span data-stu-id="48a4f-171">D2D1_BLEND_MODE_LINEAR_DODGE</span></span></td>
<td><span data-ttu-id="48a4f-172">Основные формулы смешения с <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) =</span><span class="sxs-lookup"><span data-stu-id="48a4f-172">Basic blend formulas with <em>f</em>(F<sub>RGB</sub>, B<sub>RGB</sub>) =</span></span> <img src="images/blend-mode-lineardodge-1.png" alt="Mathematical formula for a linear dodge effect." /></td>
</tr>
<tr class="even">
<td><span data-ttu-id="48a4f-173">D2D1_BLEND_MODE_LIGHTER_COLOR</span><span class="sxs-lookup"><span data-stu-id="48a4f-173">D2D1_BLEND_MODE_LIGHTER_COLOR</span></span></td>
<td><span data-ttu-id="48a4f-174">Базовая формула Blend только для Alpha.</span><span class="sxs-lookup"><span data-stu-id="48a4f-174">Basic blend formula for alpha only.</span></span> <img src="images/blend-mode-lightercolor-1.png" alt="Mathematical formula for a lighter color effect." /></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="48a4f-175">D2D1_BLEND_MODE_OVERLAY</span><span class="sxs-lookup"><span data-stu-id="48a4f-175">D2D1_BLEND_MODE_OVERLAY</span></span></td>
<td><span data-ttu-id="48a4f-176">Основные формулы смешения с <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) =</span><span class="sxs-lookup"><span data-stu-id="48a4f-176">Basic blend formulas with <em>f</em>(F<sub>RGB</sub>, B<sub>RGB</sub>) =</span></span> <img src="images/blend-mode-overlay-1.png" alt="Mathematical formula for an overlay effect." /></td>
</tr>
<tr class="even">
<td><span data-ttu-id="48a4f-177">D2D1_BLEND_MODE_SOFT_LIGHT</span><span class="sxs-lookup"><span data-stu-id="48a4f-177">D2D1_BLEND_MODE_SOFT_LIGHT</span></span></td>
<td><span data-ttu-id="48a4f-178">Основные формулы смешения с <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) =</span><span class="sxs-lookup"><span data-stu-id="48a4f-178">Basic blend formulas with <em>f</em>(F<sub>RGB</sub>, B<sub>RGB</sub>) =</span></span> <img src="images/blend-mode-softlight-1.png" alt="Mathematical formula for a soft light effect." /></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="48a4f-179">D2D1_BLEND_MODE_HARD_LIGHT</span><span class="sxs-lookup"><span data-stu-id="48a4f-179">D2D1_BLEND_MODE_HARD_LIGHT</span></span></td>
<td><span data-ttu-id="48a4f-180">Основные формулы смешения с <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) =</span><span class="sxs-lookup"><span data-stu-id="48a4f-180">Basic blend formulas with <em>f</em>(F<sub>RGB</sub>, B<sub>RGB</sub>) =</span></span> <img src="images/blend-mode-hardlight-1.png" alt="Mathematical formula for a hard light effect." /></td>
</tr>
<tr class="even">
<td><span data-ttu-id="48a4f-181">D2D1_BLEND_MODE_VIVID_LIGHT</span><span class="sxs-lookup"><span data-stu-id="48a4f-181">D2D1_BLEND_MODE_VIVID_LIGHT</span></span></td>
<td><span data-ttu-id="48a4f-182">Основные формулы смешения с <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) =</span><span class="sxs-lookup"><span data-stu-id="48a4f-182">Basic blend formulas with <em>f</em>(F<sub>RGB</sub>, B<sub>RGB</sub>) =</span></span> <img src="images/blend-mode-vividlight-1.png" alt="Mathematical formula for a vivid light effect." /></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="48a4f-183">D2D1_BLEND_MODE_LINEAR_LIGHT</span><span class="sxs-lookup"><span data-stu-id="48a4f-183">D2D1_BLEND_MODE_LINEAR_LIGHT</span></span></td>
<td><span data-ttu-id="48a4f-184">Основные формулы смешения с <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) =</span><span class="sxs-lookup"><span data-stu-id="48a4f-184">Basic blend formulas with <em>f</em>(F<sub>RGB</sub>, B<sub>RGB</sub>) =</span></span> <img src="images/blend-mode-linearlight-1.png" alt="Mathematical formula for a linear light effect." /></td>
</tr>
<tr class="even">
<td><span data-ttu-id="48a4f-185">D2D1_BLEND_MODE_PIN_LIGHT</span><span class="sxs-lookup"><span data-stu-id="48a4f-185">D2D1_BLEND_MODE_PIN_LIGHT</span></span></td>
<td><span data-ttu-id="48a4f-186">Основные формулы смешения с <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) =</span><span class="sxs-lookup"><span data-stu-id="48a4f-186">Basic blend formulas with <em>f</em>(F<sub>RGB</sub>, B<sub>RGB</sub>) =</span></span> <img src="images/blend-mode-pinlight-1.png" alt="Mathematical formula for a pin light effect." /></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="48a4f-187">D2D1_BLEND_MODE_HARD_MIX</span><span class="sxs-lookup"><span data-stu-id="48a4f-187">D2D1_BLEND_MODE_HARD_MIX</span></span></td>
<td><span data-ttu-id="48a4f-188">Основные формулы смешения с <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) =</span><span class="sxs-lookup"><span data-stu-id="48a4f-188">Basic blend formulas with <em>f</em>(F<sub>RGB</sub>, B<sub>RGB</sub>) =</span></span> <img src="images/blend-mode-hardmix-1.png" alt="Mathematical formula for a hard mix effect." /></td>
</tr>
<tr class="even">
<td><span data-ttu-id="48a4f-189">D2D1_BLEND_MODE_DIFFERENCE</span><span class="sxs-lookup"><span data-stu-id="48a4f-189">D2D1_BLEND_MODE_DIFFERENCE</span></span></td>
<td><span data-ttu-id="48a4f-190">Основные формулы смешения с <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) = ABS (f<sub>RGB</sub> - B,<sub>RGB</sub>)</span><span class="sxs-lookup"><span data-stu-id="48a4f-190">Basic blend formulas with <em>f</em>(F<sub>RGB</sub>, B<sub>RGB</sub>) = abs(F<sub>RGB</sub> - B<sub>RGB</sub>)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="48a4f-191">D2D1_BLEND_MODE_EXCLUSION</span><span class="sxs-lookup"><span data-stu-id="48a4f-191">D2D1_BLEND_MODE_EXCLUSION</span></span></td>
<td><span data-ttu-id="48a4f-192">Основные формулы смешения с <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) = f<sub>RGB</sub> + b<sub>RGB</sub>   2 \* \* f<sub>RGB</sub> \* b<sub>RGB</sub></span><span class="sxs-lookup"><span data-stu-id="48a4f-192">Basic blend formulas with <em>f</em>(F<sub>RGB</sub>, B<sub>RGB</sub>) = F<sub>RGB</sub> + B<sub>RGB</sub>   2 \* F<sub>RGB</sub> \* B<sub>RGB</sub></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="48a4f-193">D2D1_BLEND_MODE_HUE</span><span class="sxs-lookup"><span data-stu-id="48a4f-193">D2D1_BLEND_MODE_HUE</span></span></td>
<td><span data-ttu-id="48a4f-194">Базовая формула Blend только для Alpha.</span><span class="sxs-lookup"><span data-stu-id="48a4f-194">Basic blend formula for alpha only.</span></span> <img src="images/blend-mode-hue-1.png" alt="Mathematical formula for a hue blend effect." /></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="48a4f-195">D2D1_BLEND_MODE_SATURATION</span><span class="sxs-lookup"><span data-stu-id="48a4f-195">D2D1_BLEND_MODE_SATURATION</span></span></td>
<td><span data-ttu-id="48a4f-196">Базовая формула Blend только для Alpha.</span><span class="sxs-lookup"><span data-stu-id="48a4f-196">Basic blend formula for alpha only.</span></span> <img src="images/blend-mode-saturation-1.png" alt="Mathematical formula for a sturation blend effect." /></td>
</tr>
<tr class="even">
<td><span data-ttu-id="48a4f-197">D2D1_BLEND_MODE_COLOR</span><span class="sxs-lookup"><span data-stu-id="48a4f-197">D2D1_BLEND_MODE_COLOR</span></span></td>
<td><span data-ttu-id="48a4f-198">Базовая формула Blend только для Alpha.</span><span class="sxs-lookup"><span data-stu-id="48a4f-198">Basic blend formula for alpha only.</span></span> <img src="images/blend-mode-color-1.png" alt="Mathematical formula for a color blend effect." /></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="48a4f-199">D2D1_BLEND_MODE_LUMINOSITY</span><span class="sxs-lookup"><span data-stu-id="48a4f-199">D2D1_BLEND_MODE_LUMINOSITY</span></span></td>
<td><span data-ttu-id="48a4f-200">Базовая формула Blend только для Alpha.</span><span class="sxs-lookup"><span data-stu-id="48a4f-200">Basic blend formula for alpha only.</span></span> <img src="images/blend-mode-luminosity-1.png" alt="Mathematical formula for a luminosity blend effect." /></td>
</tr>
<tr class="even">
<td><span data-ttu-id="48a4f-201">D2D1_BLEND_MODE_DISSOLVE</span><span class="sxs-lookup"><span data-stu-id="48a4f-201">D2D1_BLEND_MODE_DISSOLVE</span></span></td>
<td><span data-ttu-id="48a4f-202">Исходные данные:</span><span class="sxs-lookup"><span data-stu-id="48a4f-202">Given:</span></span>
<ul>
<li><span data-ttu-id="48a4f-203">ТОЧЕЧная координата сцены для текущего пикселя</span><span class="sxs-lookup"><span data-stu-id="48a4f-203">A scene coordinate XY for the current pixel</span></span></li>
<li><span data-ttu-id="48a4f-204">Детерминированный генератор случайных чисел Rand (XY), основанный на координатах начальной координаты, с несмещенным распределением значений из [0, 1]</span><span class="sxs-lookup"><span data-stu-id="48a4f-204">A deterministic pseudo-random number generator rand(XY) based on seed coordinate XY, with unbiased distribution of values from [0, 1]</span></span></li>
</ul>
<br/> <img src="images/blend-mode-dissolve-1.png" alt="Mathematical formula for a dissolve blend effect." /><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="48a4f-205">D2D1_BLEND_MODE_SUBTRACT</span><span class="sxs-lookup"><span data-stu-id="48a4f-205">D2D1_BLEND_MODE_SUBTRACT</span></span></td>
<td><span data-ttu-id="48a4f-206">Базовая формула Blend только для Alpha.</span><span class="sxs-lookup"><span data-stu-id="48a4f-206">Basic blend formula for alpha only.</span></span> <img src="images/blend-mode-subtract-1.png" alt="Mathematical formula for a subtract blend effect." /></td>
</tr>
<tr class="even">
<td><span data-ttu-id="48a4f-207">D2D1_BLEND_MODE_DIVISION</span><span class="sxs-lookup"><span data-stu-id="48a4f-207">D2D1_BLEND_MODE_DIVISION</span></span></td>
<td><span data-ttu-id="48a4f-208">Базовая формула Blend только для Alpha.</span><span class="sxs-lookup"><span data-stu-id="48a4f-208">Basic blend formula for alpha only.</span></span> <img src="images/blend-mode-division-1.png" alt="Mathematical formula for a division blend effect." /></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> <span data-ttu-id="48a4f-209">Для всех режимов наложения выходное значение предварительно умножается и замещается в диапазон \[ 0, 1 \] .</span><span class="sxs-lookup"><span data-stu-id="48a4f-209">For all Blend modes, the output value is premultiplied and clamped to the range \[0, 1\].</span></span>

 

## <a name="hsl-color-space-conversions"></a><span data-ttu-id="48a4f-210">HSL. преобразование цветового пространства</span><span class="sxs-lookup"><span data-stu-id="48a4f-210">HSL color space conversions</span></span>

<span data-ttu-id="48a4f-211">Компонент "яркость" вычисляются с использованием веса RGB здесь:</span><span class="sxs-lookup"><span data-stu-id="48a4f-211">The luminosity component is computed using the RGB weights here:</span></span>

-   <span data-ttu-id="48a4f-212">*k*<sub>R</sub> = 0,30</span><span class="sxs-lookup"><span data-stu-id="48a4f-212">*k*<sub>R</sub> = 0.30</span></span>
-   <span data-ttu-id="48a4f-213">*k*<sub>G</sub> = 0,59</span><span class="sxs-lookup"><span data-stu-id="48a4f-213">*k*<sub>G</sub> = 0.59</span></span>
-   <span data-ttu-id="48a4f-214">*k*<sub>б</sub> = 0,11</span><span class="sxs-lookup"><span data-stu-id="48a4f-214">*k*<sub>B</sub> = 0.11</span></span>

### <a name="converting-from-rgb-to-hsl"></a><span data-ttu-id="48a4f-215">Преобразование RGB в HSL</span><span class="sxs-lookup"><span data-stu-id="48a4f-215">Converting from RGB to HSL</span></span>

![Математическая формула, описывающая преобразование цвета RGB в значение HSL Color.](images/blend-rgb-to-hsl-1.png)

<span data-ttu-id="48a4f-217">Это помещает *S* и *L* в диапазоне \[ 0,0, 1,0 \] и *H* в диапазоне \[ -1,0, 5,0 \] .</span><span class="sxs-lookup"><span data-stu-id="48a4f-217">This places *S* and *L* in the range \[0.0, 1.0\] and *H* in the range \[-1.0, 5.0\].</span></span>

### <a name="converting-from-hsl-to-rgb"></a><span data-ttu-id="48a4f-218">Преобразование из HSL в RGB</span><span class="sxs-lookup"><span data-stu-id="48a4f-218">Converting from HSL to RGB</span></span>

<span data-ttu-id="48a4f-219">Для преобразования другого способа используется обратная часть предыдущих вычислений.</span><span class="sxs-lookup"><span data-stu-id="48a4f-219">To convert the other way we use the inverse of the previous calculations.</span></span>

<span data-ttu-id="48a4f-220">Если *S* = 0, то *R*  =  *G*  =  *B*  =  *L*</span><span class="sxs-lookup"><span data-stu-id="48a4f-220">If *S* = 0 then *R* = *G* = *B* = *L*</span></span>

<span data-ttu-id="48a4f-221">В противном случае есть шесть вариантов, зависимых от оттенок:</span><span class="sxs-lookup"><span data-stu-id="48a4f-221">Otherwise there are six hue-dependant cases:</span></span>

<span data-ttu-id="48a4f-222">Если значение *H* больше 0, значения находятся в красно-пурпурном секторе, где *R*  >  *B*  >  *G*.</span><span class="sxs-lookup"><span data-stu-id="48a4f-222">If *H* is greater than 0, the values are in the red/magenta sector where *R* > *B* > *G*.</span></span>

![математический екуаитон шаг 1 из шести преобразований цвета HSL в RGB.](images/blend-hsl-to-rgb-1rm.png)

<span data-ttu-id="48a4f-224">Если значение *H* больше или равно 0 и меньше 1, значения находятся в красно-желтом секторе, где *R*  >  *G*  >  *B*.</span><span class="sxs-lookup"><span data-stu-id="48a4f-224">If *H* is greater than or equal to 0 and less than 1, the values are in the red/yellow sector where *R* > *G* > *B*.</span></span>

![математический екуаитон шаг 2 из шести преобразований цвета HSL в RGB.](images/blend-hsl-to-rgb-1ry.png)

<span data-ttu-id="48a4f-226">Если *H* больше или равно 1 и меньше 2, значения находятся в желтом/зеленом секторе, где *G*  >  *R*  >  *B*.</span><span class="sxs-lookup"><span data-stu-id="48a4f-226">If *H* is greater than or equal to 1 and less than 2, the values are in the yellow/green sector where *G* > *R* > *B*.</span></span>

![математический екуаитон шаг 3 из шести преобразований цвета HSL в RGB.](images/blend-hsl-to-rgb-1yg.png)

<span data-ttu-id="48a4f-228">Если *H* больше или равно 2 и меньше 3, значения находятся в зеленом/голубом секторе, где *G*  >  *B*  >  *R*.</span><span class="sxs-lookup"><span data-stu-id="48a4f-228">If *H* is greater than or equal to 2 and less than 3, the values are in the green/cyan sector where *G* > *B* > *R*.</span></span>

![математически екуаитон шаг 4 из шести преобразований цвета HSL в RGB.](images/blend-hsl-to-rgb-1gc.png)

<span data-ttu-id="48a4f-230">Если значение *H* больше или равно 3 и меньше 4, значения находятся в голубом/синем секторе, где *B*  >  *G*  >  *R*.</span><span class="sxs-lookup"><span data-stu-id="48a4f-230">If *H* is greater than or equal to 3 and less than 4, the values are in the cyan/blue sector where *B* > *G* > *R*.</span></span>

![математически екуаитон шаг 5 из шести преобразований цвета HSL в RGB.](images/blend-hsl-to-rgb-1cb.png)

<span data-ttu-id="48a4f-232">Если *H* больше или равно 4, значения находятся в синем/пурпурном секторе, где *B*  >  *R*  >  *G*.</span><span class="sxs-lookup"><span data-stu-id="48a4f-232">If *H* is greater than or equal to 4, the values are in the blue/magenta sector where *B* > *R* > *G*.</span></span>

![математически екуаитон шаг шесть из шести преобразований цвета HSL в RGB.](images/blend-hsl-to-rgb-1bm.png)

<span data-ttu-id="48a4f-234">Поскольку режимы наложения выполняют произвольные сочетания компонентов HSL из двух разных цветов, то обычно преобразованное значение RGB становится недопустимым, то есть один или несколько компонентов канала могут находиться за пределами допустимого диапазона \[ 0,0, 1,0 \] .</span><span class="sxs-lookup"><span data-stu-id="48a4f-234">Because the blending modes make arbitrary combinations of HSL components from two different colors, it is common for the converted RGB value to be out-of-gamut, that is, one or more channel components may be outside the legal range of \[0.0, 1.0\].</span></span> <span data-ttu-id="48a4f-235">Эти цвета возвращаются в цветовой охват путем минимального уменьшения насыщенности, сохраняя как оттенок, так и яркость:</span><span class="sxs-lookup"><span data-stu-id="48a4f-235">These colors are brought back into gamut by minimally reducing the saturation, while preserving both hue and luminosity:</span></span>

![Математическая формула, описывающая исправления, необходимые для использования экземпляров цветового охвата.](images/blend-gamut-correction.png)

## <a name="output-bitmap"></a><span data-ttu-id="48a4f-237">Битовая карта вывода</span><span class="sxs-lookup"><span data-stu-id="48a4f-237">Output bitmap</span></span>

<span data-ttu-id="48a4f-238">Выходным точечным рисунком для этого результата всегда является размер объединения двух входных изображений.</span><span class="sxs-lookup"><span data-stu-id="48a4f-238">The output bitmap for this effect is always the size of the union of the two input images.</span></span>

## <a name="sample-code"></a><span data-ttu-id="48a4f-239">Пример кода</span><span class="sxs-lookup"><span data-stu-id="48a4f-239">Sample code</span></span>

<span data-ttu-id="48a4f-240">Чтобы получить пример этого результата, скачайте [образец Direct2D составных эффектов](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct2D%20composite%20effect%20modes%20sample).</span><span class="sxs-lookup"><span data-stu-id="48a4f-240">For an example of this effect, download the [Direct2D composite effect modes sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct2D%20composite%20effect%20modes%20sample).</span></span>

## <a name="requirements"></a><span data-ttu-id="48a4f-241">Требования</span><span class="sxs-lookup"><span data-stu-id="48a4f-241">Requirements</span></span>



| <span data-ttu-id="48a4f-242">Требование</span><span class="sxs-lookup"><span data-stu-id="48a4f-242">Requirement</span></span> | <span data-ttu-id="48a4f-243">Значение</span><span class="sxs-lookup"><span data-stu-id="48a4f-243">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="48a4f-244">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="48a4f-244">Minimum supported client</span></span> | <span data-ttu-id="48a4f-245">Windows 8 и обновление платформы для \[ классических приложений Windows 7 \| приложения для Магазина Windows\]</span><span class="sxs-lookup"><span data-stu-id="48a4f-245">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="48a4f-246">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="48a4f-246">Minimum supported server</span></span> | <span data-ttu-id="48a4f-247">Windows 8 и обновление платформы для \[ классических приложений Windows 7 \| приложения для Магазина Windows\]</span><span class="sxs-lookup"><span data-stu-id="48a4f-247">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="48a4f-248">Header</span><span class="sxs-lookup"><span data-stu-id="48a4f-248">Header</span></span>                   | <span data-ttu-id="48a4f-249">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="48a4f-249">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="48a4f-250">Библиотека</span><span class="sxs-lookup"><span data-stu-id="48a4f-250">Library</span></span>                  | <span data-ttu-id="48a4f-251">D2D1. lib, дксгуид. lib</span><span class="sxs-lookup"><span data-stu-id="48a4f-251">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="48a4f-252">См. также</span><span class="sxs-lookup"><span data-stu-id="48a4f-252">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="48a4f-253">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="48a4f-253">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

