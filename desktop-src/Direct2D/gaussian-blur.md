---
title: Эффект размытия по Гауссу
description: Используйте эффект размытия по Гауссу, чтобы создать размытие на основе функции по Гауссу для всего входного изображения.
ms.assetid: 6B8C9A0A-81D6-4CC2-B30B-995D4C2E59FC
keywords:
- Размытие по Гауссу
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfbe8b309a498315e389be45d382eca3ee1b98ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104558209"
---
# <a name="gaussian-blur-effect"></a><span data-ttu-id="038ea-104">Эффект размытия по Гауссу</span><span class="sxs-lookup"><span data-stu-id="038ea-104">Gaussian blur effect</span></span>

<span data-ttu-id="038ea-105">Используйте эффект размытия по Гауссу, чтобы создать размытие на основе функции по Гауссу для всего входного изображения.</span><span class="sxs-lookup"><span data-stu-id="038ea-105">Use the Gaussian blur effect to create a blur based on the Gaussian function over the entire input image.</span></span>

<span data-ttu-id="038ea-106">С помощью этого действия можно создавать свечения и тени и использовать [составной](composite.md) эффект для применения результата к исходному изображению.</span><span class="sxs-lookup"><span data-stu-id="038ea-106">You can use this effect to create glows and drop shadows and use the [composite](composite.md) effect to apply the result to the original image.</span></span> <span data-ttu-id="038ea-107">Это полезно при обработке фотографий для таких фильтров, как выделение и тени.</span><span class="sxs-lookup"><span data-stu-id="038ea-107">It is useful in photo processing for filters like highlights and shadows.</span></span> <span data-ttu-id="038ea-108">Выходные данные этого эффекта можно использовать для ввода в эффекты освещения, например при [отраженном освещении](specular-lighting.md) или эффектах [рассеянного освещения](diffuse-lighting.md) , так как альфа-канал размыт, а эффекты освещения используют альфа-канал, чтобы определить геометрию поверхности как карту высоты.</span><span class="sxs-lookup"><span data-stu-id="038ea-108">You can use the output of this effect for input into lighting effects, like the [Specular Lighting](specular-lighting.md) or [Diffuse Lighting](diffuse-lighting.md) effects, because the alpha channel is blurred, too and lighting effects use the alpha channel to determine surface geometry as a height map.</span></span>

<span data-ttu-id="038ea-109">Этот эффект используется встроенным эффектом [тени](drop-shadow.md) .</span><span class="sxs-lookup"><span data-stu-id="038ea-109">This effect is used by the built-in [Shadow](drop-shadow.md) effect.</span></span>

<span data-ttu-id="038ea-110">Идентификатором CLSID для этого действия является CLSID \_ D2D1GaussianBlur.</span><span class="sxs-lookup"><span data-stu-id="038ea-110">The CLSID for this effect is CLSID\_D2D1GaussianBlur.</span></span>

-   [<span data-ttu-id="038ea-111">Пример изображения</span><span class="sxs-lookup"><span data-stu-id="038ea-111">Example image</span></span>](#example-image)
-   [<span data-ttu-id="038ea-112">Свойства эффектов</span><span class="sxs-lookup"><span data-stu-id="038ea-112">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="038ea-113">Режимы оптимизации</span><span class="sxs-lookup"><span data-stu-id="038ea-113">Optimization modes</span></span>](#optimization-modes)
-   [<span data-ttu-id="038ea-114">Режимы границ</span><span class="sxs-lookup"><span data-stu-id="038ea-114">Border modes</span></span>](#border-modes)
-   [<span data-ttu-id="038ea-115">Битовая карта вывода</span><span class="sxs-lookup"><span data-stu-id="038ea-115">Output bitmap</span></span>](#output-bitmap)
-   [<span data-ttu-id="038ea-116">Требования</span><span class="sxs-lookup"><span data-stu-id="038ea-116">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="038ea-117">См. также</span><span class="sxs-lookup"><span data-stu-id="038ea-117">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="038ea-118">Пример изображения</span><span class="sxs-lookup"><span data-stu-id="038ea-118">Example image</span></span>



| <span data-ttu-id="038ea-119">До</span><span class="sxs-lookup"><span data-stu-id="038ea-119">Before</span></span>                                                       |
|--------------------------------------------------------------|
| ![изображение перед результатом.](images/default-before.jpg)   |
| <span data-ttu-id="038ea-121">После</span><span class="sxs-lookup"><span data-stu-id="038ea-121">After</span></span>                                                        |
| ![изображение после преобразования.](images/1-gaussianblur.png) |



 


```C++
ComPtr<ID2D1Effect> gaussianBlurEffect;
m_d2dContext->CreateEffect(CLSID_D2D1GaussianBlur, &gaussianBlurEffect);

gaussianBlurEffect->SetInput(0, bitmap);
gaussianBlurEffect->SetValue(D2D1_GAUSSIANBLUR_PROP_STANDARD_DEVIATION, 3.0f);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(gaussianBlurEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a><span data-ttu-id="038ea-123">Свойства эффектов</span><span class="sxs-lookup"><span data-stu-id="038ea-123">Effect properties</span></span>



| <span data-ttu-id="038ea-124">Отображаемое имя и перечисление индекса</span><span class="sxs-lookup"><span data-stu-id="038ea-124">Display name and index enumeration</span></span>                                                    | <span data-ttu-id="038ea-125">Описание</span><span class="sxs-lookup"><span data-stu-id="038ea-125">Description</span></span>                                                                                                                                                                                                                                                                                                                         |
|---------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="038ea-126">StandardDeviation</span><span class="sxs-lookup"><span data-stu-id="038ea-126">StandardDeviation</span></span><br/> <span data-ttu-id="038ea-127">\_ \_ \_ Стандартное отклонение D2D1 гауссианблур Prop \_</span><span class="sxs-lookup"><span data-stu-id="038ea-127">D2D1\_GAUSSIANBLUR\_PROP\_STANDARD\_DEVIATION</span></span><br/> | <span data-ttu-id="038ea-128">Объем размытия, применяемый к изображению.</span><span class="sxs-lookup"><span data-stu-id="038ea-128">The amount of blur to be applied to the image.</span></span> <span data-ttu-id="038ea-129">Можно вычислить Радиус размытия ядра, умножив стандартное отклонение на 3.</span><span class="sxs-lookup"><span data-stu-id="038ea-129">You can compute the blur radius of the kernel by multiplying the standard deviation by 3.</span></span> <span data-ttu-id="038ea-130">Единицы как стандартного отклонения, так и размытого радиуса являются DIP.</span><span class="sxs-lookup"><span data-stu-id="038ea-130">The units of both the standard deviation and blur radius are DIPs.</span></span> <span data-ttu-id="038ea-131">Нулевое значение DIP отключает этот результат целиком.</span><span class="sxs-lookup"><span data-stu-id="038ea-131">A value of zero DIPs disables this effect entirely.</span></span> <span data-ttu-id="038ea-132">Тип — FLOAT.</span><span class="sxs-lookup"><span data-stu-id="038ea-132">The type is FLOAT.</span></span><br/> <span data-ttu-id="038ea-133">Значение по умолчанию — 3.0 f.</span><span class="sxs-lookup"><span data-stu-id="038ea-133">The default value is 3.0f.</span></span><br/> |
| <span data-ttu-id="038ea-134">Optimization</span><span class="sxs-lookup"><span data-stu-id="038ea-134">Optimization</span></span><br/> <span data-ttu-id="038ea-135">\_Оптимизация D2D1 \_ гауссианблур \_</span><span class="sxs-lookup"><span data-stu-id="038ea-135">D2D1\_GAUSSIANBLUR\_PROP\_OPTIMIZATION</span></span><br/>             | <span data-ttu-id="038ea-136">Режим оптимизации.</span><span class="sxs-lookup"><span data-stu-id="038ea-136">The optimization mode.</span></span> <span data-ttu-id="038ea-137">Дополнительные сведения см. в разделе [режимы оптимизации](#optimization-modes) .</span><span class="sxs-lookup"><span data-stu-id="038ea-137">See [Optimization modes](#optimization-modes) for more info.</span></span> <span data-ttu-id="038ea-138">Тип — D2D1 \_ гауссианблур \_ OPTIMIZATION.</span><span class="sxs-lookup"><span data-stu-id="038ea-138">The type is D2D1\_GAUSSIANBLUR\_OPTIMIZATION.</span></span><br/> <span data-ttu-id="038ea-139">Значение по умолчанию — D2D1 \_ гауссианблур \_ OPTIMIZATION \_ Balance.</span><span class="sxs-lookup"><span data-stu-id="038ea-139">The default value is D2D1\_GAUSSIANBLUR\_OPTIMIZATION\_BALANCED.</span></span><br/>                                                                                                            |
| <span data-ttu-id="038ea-140">бордермоде</span><span class="sxs-lookup"><span data-stu-id="038ea-140">BorderMode</span></span><br/> <span data-ttu-id="038ea-141">\_Режим границы D2D1 гауссианблур " \_ prop" \_ \_</span><span class="sxs-lookup"><span data-stu-id="038ea-141">D2D1\_GAUSSIANBLUR\_PROP\_BORDER\_MODE</span></span><br/>               | <span data-ttu-id="038ea-142">Режим, используемый для вычисления границы изображения: Soft или Hard.</span><span class="sxs-lookup"><span data-stu-id="038ea-142">The mode used to calculate the border of the image, soft or hard.</span></span> <span data-ttu-id="038ea-143">Дополнительные сведения см. в разделе [режимы границ](#border-modes) .</span><span class="sxs-lookup"><span data-stu-id="038ea-143">See [Border modes](#border-modes) for more info.</span></span> <br/> <span data-ttu-id="038ea-144">Тип — D2D1 \_ гауссианблур \_ Border ( \_ режим границы).</span><span class="sxs-lookup"><span data-stu-id="038ea-144">The type is D2D1\_GAUSSIANBLUR\_BORDER\_MODE.</span></span><br/> <span data-ttu-id="038ea-145">Значение по умолчанию — D2D1 \_ границы \_ режима \_ Soft.</span><span class="sxs-lookup"><span data-stu-id="038ea-145">The default value is D2D1\_BORDER\_MODE\_SOFT.</span></span><br/>                                                                                   |



 

## <a name="optimization-modes"></a><span data-ttu-id="038ea-146">Режимы оптимизации</span><span class="sxs-lookup"><span data-stu-id="038ea-146">Optimization modes</span></span>



| <span data-ttu-id="038ea-147">Имя</span><span class="sxs-lookup"><span data-stu-id="038ea-147">Name</span></span>                                          | <span data-ttu-id="038ea-148">Описание</span><span class="sxs-lookup"><span data-stu-id="038ea-148">Description</span></span>                                                                                                                           |
|-----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="038ea-149">\_ \_ Скорость оптимизации D2D1 \_ директионалблур</span><span class="sxs-lookup"><span data-stu-id="038ea-149">D2D1\_DIRECTIONALBLUR\_OPTIMIZATION\_SPEED</span></span>    | <span data-ttu-id="038ea-150">Применяет внутренние оптимизации, такие как предварительное масштабирование относительно небольших радиусов.</span><span class="sxs-lookup"><span data-stu-id="038ea-150">Applies internal optimizations such as pre-scaling at relatively small radii.</span></span> <span data-ttu-id="038ea-151">Использует линейную фильтрацию.</span><span class="sxs-lookup"><span data-stu-id="038ea-151">Uses linear filtering.</span></span>                                  |
| <span data-ttu-id="038ea-152">\_ \_ Сбалансированная оптимизация D2D1 директионалблур \_</span><span class="sxs-lookup"><span data-stu-id="038ea-152">D2D1\_DIRECTIONALBLUR\_OPTIMIZATION\_BALANCED</span></span> | <span data-ttu-id="038ea-153">Использует те же пороговые значения оптимизации, что и режим скорости, но использует фильтрацию трилинейной.</span><span class="sxs-lookup"><span data-stu-id="038ea-153">Uses the same optimization thresholds as Speed mode, but uses trilinear filtering.</span></span>                                                    |
| <span data-ttu-id="038ea-154">\_ \_ Качество оптимизации D2D1 \_ директионалблур</span><span class="sxs-lookup"><span data-stu-id="038ea-154">D2D1\_DIRECTIONALBLUR\_OPTIMIZATION\_QUALITY</span></span>  | <span data-ttu-id="038ea-155">В используются только внутренние оптимизации с большими радиусами, где приближение меньше вероятно должно быть видимым.</span><span class="sxs-lookup"><span data-stu-id="038ea-155">Only uses internal optimizations with large blur radii, where approximations are less likely to be visible.</span></span> <span data-ttu-id="038ea-156">Использует фильтрацию трилинейной.</span><span class="sxs-lookup"><span data-stu-id="038ea-156">Uses trilinear filtering.</span></span> |



 

## <a name="border-modes"></a><span data-ttu-id="038ea-157">Режимы границ</span><span class="sxs-lookup"><span data-stu-id="038ea-157">Border modes</span></span>



| <span data-ttu-id="038ea-158">Имя</span><span class="sxs-lookup"><span data-stu-id="038ea-158">Name</span></span>                     | <span data-ttu-id="038ea-159">Описание</span><span class="sxs-lookup"><span data-stu-id="038ea-159">Description</span></span>                                                                                                                                                                                                              |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="038ea-160">\_ \_ Мягкий режим границы \_ D2D1</span><span class="sxs-lookup"><span data-stu-id="038ea-160">D2D1\_BORDER\_MODE\_SOFT</span></span> | <span data-ttu-id="038ea-161">Эффект записывает изображение прозрачными черными пикселями, так как оно применяет ядро размытия, что приводит к мягкому пограничным границе.</span><span class="sxs-lookup"><span data-stu-id="038ea-161">The effect pads the image with transparent black pixels as it applies the blur kernel, resulting in a soft edge.</span></span> <br/>                                                                                             |
| <span data-ttu-id="038ea-162">Жесткое D2D1 в \_ \_ режиме границы \_</span><span class="sxs-lookup"><span data-stu-id="038ea-162">D2D1\_BORDER\_MODE\_HARD</span></span> | <span data-ttu-id="038ea-163">В результате выходные данные заменяются на размер входного изображения.</span><span class="sxs-lookup"><span data-stu-id="038ea-163">The effect clamps the output to the size of the input image.</span></span> <span data-ttu-id="038ea-164">Когда эффект применяет ядро размытия, он расширяет входной образ с помощью преобразования границы зеркального типа для выборок за пределами входных данных.</span><span class="sxs-lookup"><span data-stu-id="038ea-164">When the effect applies the blur kernel, it extends the input image with a mirror-type border transform for samples outside of the input bounds.</span></span><br/> |



 

## <a name="output-bitmap"></a><span data-ttu-id="038ea-165">Битовая карта вывода</span><span class="sxs-lookup"><span data-stu-id="038ea-165">Output bitmap</span></span>

<span data-ttu-id="038ea-166">Результат этого действия может быть больше, чем входной точечный рисунок, основанный на радиусе размытия и режиме границы.</span><span class="sxs-lookup"><span data-stu-id="038ea-166">The output of this effect can be larger than the input bitmap based on the blur radius and the border mode.</span></span> <span data-ttu-id="038ea-167">Если для параметра режим границы задано значение \_ D2D1 \_ в режиме границы, \_ гории для выходного точечного рисунка увеличивается на размер ядра размытия, представленного в пикселях.</span><span class="sxs-lookup"><span data-stu-id="038ea-167">If the border mode is set to D2D1\_BORDER\_MODE\_SOFT the s ize of the output bitmap increases by the size of the blur kernel, represented in pixels.</span></span> <span data-ttu-id="038ea-168">В этой таблице представлена формула, с помощью которой можно вычислить выходное растровое изображение.</span><span class="sxs-lookup"><span data-stu-id="038ea-168">This table provides an equation that you can use to compute the output bitmap.</span></span>

`Output bitmap growth (X and Y) = StandardDeviation  (DIPs)*6*((User DPI)/96)`

<span data-ttu-id="038ea-169">Таким образом, если размер изображения увеличивается на 10 пикселей в каждом направлении, верхний левый угол изображения будет находиться в (-5,-5), а нижний правый — в (105, 105).</span><span class="sxs-lookup"><span data-stu-id="038ea-169">So, if the image size increases by 10 pixels in each direction the upper left corner of the image will be located at (-5, -5) while the lower right will be at (105, 105).</span></span>

## <a name="requirements"></a><span data-ttu-id="038ea-170">Требования</span><span class="sxs-lookup"><span data-stu-id="038ea-170">Requirements</span></span>



| <span data-ttu-id="038ea-171">Требование</span><span class="sxs-lookup"><span data-stu-id="038ea-171">Requirement</span></span> | <span data-ttu-id="038ea-172">Значение</span><span class="sxs-lookup"><span data-stu-id="038ea-172">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="038ea-173">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="038ea-173">Minimum supported client</span></span> | <span data-ttu-id="038ea-174">Windows 8 и обновление платформы для \[ классических приложений Windows 7 \| приложения для Магазина Windows\]</span><span class="sxs-lookup"><span data-stu-id="038ea-174">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="038ea-175">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="038ea-175">Minimum supported server</span></span> | <span data-ttu-id="038ea-176">Windows 8 и обновление платформы для \[ классических приложений Windows 7 \| приложения для Магазина Windows\]</span><span class="sxs-lookup"><span data-stu-id="038ea-176">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="038ea-177">Header</span><span class="sxs-lookup"><span data-stu-id="038ea-177">Header</span></span>                   | <span data-ttu-id="038ea-178">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="038ea-178">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="038ea-179">Библиотека</span><span class="sxs-lookup"><span data-stu-id="038ea-179">Library</span></span>                  | <span data-ttu-id="038ea-180">D2D1. lib, дксгуид. lib</span><span class="sxs-lookup"><span data-stu-id="038ea-180">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="038ea-181">См. также</span><span class="sxs-lookup"><span data-stu-id="038ea-181">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="038ea-182">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="038ea-182">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

