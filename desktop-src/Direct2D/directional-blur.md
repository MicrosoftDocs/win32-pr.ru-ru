---
title: Эффект размытия по направлению
description: Эффект размытия по направлению похож на Размытие по Гауссу, за исключением того, что вы можете наклонять размытие в определенном направлении.
ms.assetid: 59328FA4-5C27-4A81-AAB2-C5B25B3615C6
keywords:
- Размытие по направлению
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0e1c098d17929563cf69f4e61416fa0d93a88dd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801042"
---
# <a name="directional-blur-effect"></a><span data-ttu-id="b6d28-104">Эффект размытия по направлению</span><span class="sxs-lookup"><span data-stu-id="b6d28-104">Directional blur effect</span></span>

<span data-ttu-id="b6d28-105">Эффект размытия по направлению похож на [Размытие по Гауссу](gaussian-blur.md), за исключением того, что вы можете наклонять размытие в определенном направлении.</span><span class="sxs-lookup"><span data-stu-id="b6d28-105">The directional blur effect is similar to [Gaussian blur](gaussian-blur.md), except you can skew the blur in a particular direction.</span></span> <span data-ttu-id="b6d28-106">Этот результат можно использовать для того, чтобы изображение было выглядеть так, как если бы оно было в движении, или чтобы подчеркнуть анимированное изображение.</span><span class="sxs-lookup"><span data-stu-id="b6d28-106">You can use this effect to make an image look as if it is in motion or to emphasize an animated image.</span></span>

<span data-ttu-id="b6d28-107">Идентификатором CLSID для этого действия является CLSID \_ D2D1DirectionalBlur.</span><span class="sxs-lookup"><span data-stu-id="b6d28-107">The CLSID for this effect is CLSID\_D2D1DirectionalBlur.</span></span>

-   [<span data-ttu-id="b6d28-108">Пример изображения</span><span class="sxs-lookup"><span data-stu-id="b6d28-108">Example image</span></span>](#example-image)
-   [<span data-ttu-id="b6d28-109">Свойства эффектов</span><span class="sxs-lookup"><span data-stu-id="b6d28-109">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="b6d28-110">Режимы оптимизации</span><span class="sxs-lookup"><span data-stu-id="b6d28-110">Optimization modes</span></span>](#optimization-modes)
-   [<span data-ttu-id="b6d28-111">Режимы границ</span><span class="sxs-lookup"><span data-stu-id="b6d28-111">Border modes</span></span>](#border-modes)
-   [<span data-ttu-id="b6d28-112">Битовая карта вывода</span><span class="sxs-lookup"><span data-stu-id="b6d28-112">Output bitmap</span></span>](#output-bitmap)
-   [<span data-ttu-id="b6d28-113">Требования</span><span class="sxs-lookup"><span data-stu-id="b6d28-113">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="b6d28-114">См. также</span><span class="sxs-lookup"><span data-stu-id="b6d28-114">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="b6d28-115">Пример изображения</span><span class="sxs-lookup"><span data-stu-id="b6d28-115">Example image</span></span>



| <span data-ttu-id="b6d28-116">До</span><span class="sxs-lookup"><span data-stu-id="b6d28-116">Before</span></span>                                                          |
|-----------------------------------------------------------------|
| ![изображение перед результатом.](images/default-before.jpg)      |
| <span data-ttu-id="b6d28-118">После</span><span class="sxs-lookup"><span data-stu-id="b6d28-118">After</span></span>                                                           |
| ![изображение после преобразования.](images/2-directionalblur.png) |



 


```C++
ComPtr<ID2D1Effect> directionalBlurEffect;
m_d2dContext->CreateEffect(CLSID_D2D1DirectionalBlur, &directionalBlurEffect);

directionalBlurEffect->SetInput(0, bitmap);
directionalBlurEffect->SetValue(D2D1_DIRECTIONALBLUR_PROP_STANDARD_DEVIATION, 7.0f);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(directionalBlurEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a><span data-ttu-id="b6d28-120">Свойства эффектов</span><span class="sxs-lookup"><span data-stu-id="b6d28-120">Effect properties</span></span>



| <span data-ttu-id="b6d28-121">Отображаемое имя и перечисление индекса</span><span class="sxs-lookup"><span data-stu-id="b6d28-121">Display name and index enumeration</span></span>                                                       | <span data-ttu-id="b6d28-122">Описание</span><span class="sxs-lookup"><span data-stu-id="b6d28-122">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6d28-123">StandardDeviation</span><span class="sxs-lookup"><span data-stu-id="b6d28-123">StandardDeviation</span></span><br/> <span data-ttu-id="b6d28-124">\_ \_ \_ Стандартное отклонение D2D1 директионалблур Prop \_</span><span class="sxs-lookup"><span data-stu-id="b6d28-124">D2D1\_DIRECTIONALBLUR\_PROP\_STANDARD\_DEVIATION</span></span><br/> | <span data-ttu-id="b6d28-125">Объем размытия, применяемый к изображению.</span><span class="sxs-lookup"><span data-stu-id="b6d28-125">The amount of blur to be applied to the image.</span></span> <span data-ttu-id="b6d28-126">Можно вычислить Радиус размытия ядра, умножив стандартное отклонение на 3.</span><span class="sxs-lookup"><span data-stu-id="b6d28-126">You can compute the blur radius of the kernel by multiplying the standard deviation by 3.</span></span> <span data-ttu-id="b6d28-127">Единицы как стандартного отклонения, так и размытого радиуса являются DIP.</span><span class="sxs-lookup"><span data-stu-id="b6d28-127">The units of both the standard deviation and blur radius are DIPs.</span></span> <span data-ttu-id="b6d28-128">Значение 0 DIP отключает этот результат.</span><span class="sxs-lookup"><span data-stu-id="b6d28-128">A value of 0 DIPs disables this effect.</span></span> <span data-ttu-id="b6d28-129">Тип — FLOAT.</span><span class="sxs-lookup"><span data-stu-id="b6d28-129">The type is FLOAT.</span></span><br/> <span data-ttu-id="b6d28-130">Значение по умолчанию — 3.0 f.</span><span class="sxs-lookup"><span data-stu-id="b6d28-130">The default value is 3.0f.</span></span><br/>                                                                            |
| <span data-ttu-id="b6d28-131">Angle</span><span class="sxs-lookup"><span data-stu-id="b6d28-131">Angle</span></span><br/> <span data-ttu-id="b6d28-132">D2D1 \_ директионалблур \_ , \_ угол</span><span class="sxs-lookup"><span data-stu-id="b6d28-132">D2D1\_DIRECTIONALBLUR\_PROP\_ANGLE</span></span><br/>                           | <span data-ttu-id="b6d28-133">Угол размытия относительно оси x в направлении против часовой стрелки.</span><span class="sxs-lookup"><span data-stu-id="b6d28-133">The angle of the blur relative to the x-axis, in the counterclockwise direction.</span></span> <span data-ttu-id="b6d28-134">Единицы указываются в градусах.</span><span class="sxs-lookup"><span data-stu-id="b6d28-134">The units are specified in degrees.</span></span><br/> <span data-ttu-id="b6d28-135">Ядро размытия сначала создается с использованием того же процесса, что и эффект [размытия по Гауссу](gaussian-blur.md) .</span><span class="sxs-lookup"><span data-stu-id="b6d28-135">The blur kernel is first generated using the same process as for the [Gaussian blur](gaussian-blur.md) effect.</span></span> <span data-ttu-id="b6d28-136">Затем значения ядра преобразуются в соответствии со значением угла размытия.</span><span class="sxs-lookup"><span data-stu-id="b6d28-136">The kernel values are then transformed according to the blur angle.</span></span><br/> <span data-ttu-id="b6d28-137">Тип — FLOAT.</span><span class="sxs-lookup"><span data-stu-id="b6d28-137">The type is FLOAT.</span></span><br/> <span data-ttu-id="b6d28-138">Значение по умолчанию — 0,0 f.</span><span class="sxs-lookup"><span data-stu-id="b6d28-138">The default value is 0.0f.</span></span><br/> |
| <span data-ttu-id="b6d28-139">Optimization</span><span class="sxs-lookup"><span data-stu-id="b6d28-139">Optimization</span></span><br/> <span data-ttu-id="b6d28-140">\_Оптимизация D2D1 \_ директионалблур \_</span><span class="sxs-lookup"><span data-stu-id="b6d28-140">D2D1\_DIRECTIONALBLUR\_PROP\_OPTIMIZATION</span></span><br/>             | <span data-ttu-id="b6d28-141">Режим оптимизации.</span><span class="sxs-lookup"><span data-stu-id="b6d28-141">The optimization mode.</span></span> <span data-ttu-id="b6d28-142">Дополнительные сведения см. в разделе [режимы оптимизации](#optimization-modes) .</span><span class="sxs-lookup"><span data-stu-id="b6d28-142">See [Optimization modes](#optimization-modes) for more info.</span></span><br/> <span data-ttu-id="b6d28-143">Тип — D2D1 \_ директионалблур \_ OPTIMIZATION.</span><span class="sxs-lookup"><span data-stu-id="b6d28-143">The type is D2D1\_DIRECTIONALBLUR\_OPTIMIZATION.</span></span><br/> <span data-ttu-id="b6d28-144">Значение по умолчанию — D2D1 \_ директионалблур \_ OPTIMIZATION \_ Balance.</span><span class="sxs-lookup"><span data-stu-id="b6d28-144">The default value is D2D1\_DIRECTIONALBLUR\_OPTIMIZATION\_BALANCED.</span></span> <br/>                                                                                                                                                         |
| <span data-ttu-id="b6d28-145">бордермоде</span><span class="sxs-lookup"><span data-stu-id="b6d28-145">BorderMode</span></span><br/> <span data-ttu-id="b6d28-146">\_Режим границы D2D1 директионалблур " \_ prop" \_ \_</span><span class="sxs-lookup"><span data-stu-id="b6d28-146">D2D1\_DIRECTIONALBLUR\_PROP\_BORDER\_MODE</span></span><br/>               | <span data-ttu-id="b6d28-147">Режим, используемый для вычисления границы изображения: Soft или Hard.</span><span class="sxs-lookup"><span data-stu-id="b6d28-147">The mode used to calculate the border of the image, soft or hard.</span></span> <span data-ttu-id="b6d28-148">Дополнительные сведения см. в разделе [режимы границ](#border-modes) .</span><span class="sxs-lookup"><span data-stu-id="b6d28-148">See [Border modes](#border-modes) for more info.</span></span><br/> <span data-ttu-id="b6d28-149">Тип — D2D1 \_ границы \_ .</span><span class="sxs-lookup"><span data-stu-id="b6d28-149">The type is D2D1\_BORDER\_MODE.</span></span><br/> <span data-ttu-id="b6d28-150">Значение по умолчанию — D2D1 \_ границы \_ режима \_ Soft.</span><span class="sxs-lookup"><span data-stu-id="b6d28-150">The default value is D2D1\_BORDER\_MODE\_SOFT.</span></span><br/>                                                                                                                                                                 |



 

## <a name="optimization-modes"></a><span data-ttu-id="b6d28-151">Режимы оптимизации</span><span class="sxs-lookup"><span data-stu-id="b6d28-151">Optimization modes</span></span>



| <span data-ttu-id="b6d28-152">Имя</span><span class="sxs-lookup"><span data-stu-id="b6d28-152">Name</span></span>                                          | <span data-ttu-id="b6d28-153">Описание</span><span class="sxs-lookup"><span data-stu-id="b6d28-153">Description</span></span>                                                                                                                           |
|-----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6d28-154">\_ \_ Скорость оптимизации D2D1 \_ директионалблур</span><span class="sxs-lookup"><span data-stu-id="b6d28-154">D2D1\_DIRECTIONALBLUR\_OPTIMIZATION\_SPEED</span></span>    | <span data-ttu-id="b6d28-155">Применяет внутренние оптимизации, такие как предварительное масштабирование относительно небольших радиусов.</span><span class="sxs-lookup"><span data-stu-id="b6d28-155">Applies internal optimizations such as pre-scaling at relatively small radii.</span></span> <span data-ttu-id="b6d28-156">Использует линейную фильтрацию.</span><span class="sxs-lookup"><span data-stu-id="b6d28-156">Uses linear filtering.</span></span>                                  |
| <span data-ttu-id="b6d28-157">\_ \_ Сбалансированная оптимизация D2D1 директионалблур \_</span><span class="sxs-lookup"><span data-stu-id="b6d28-157">D2D1\_DIRECTIONALBLUR\_OPTIMIZATION\_BALANCED</span></span> | <span data-ttu-id="b6d28-158">Использует те же пороговые значения оптимизации, что и режим скорости, но использует фильтрацию трилинейной.</span><span class="sxs-lookup"><span data-stu-id="b6d28-158">Uses the same optimization thresholds as Speed mode, but uses trilinear filtering.</span></span>                                                    |
| <span data-ttu-id="b6d28-159">\_ \_ Качество оптимизации D2D1 \_ директионалблур</span><span class="sxs-lookup"><span data-stu-id="b6d28-159">D2D1\_DIRECTIONALBLUR\_OPTIMIZATION\_QUALITY</span></span>  | <span data-ttu-id="b6d28-160">В используются только внутренние оптимизации с большими радиусами, где приближение меньше вероятно должно быть видимым.</span><span class="sxs-lookup"><span data-stu-id="b6d28-160">Only uses internal optimizations with large blur radii, where approximations are less likely to be visible.</span></span> <span data-ttu-id="b6d28-161">Использует фильтрацию трилинейной.</span><span class="sxs-lookup"><span data-stu-id="b6d28-161">Uses trilinear filtering.</span></span> |



 

## <a name="border-modes"></a><span data-ttu-id="b6d28-162">Режимы границ</span><span class="sxs-lookup"><span data-stu-id="b6d28-162">Border modes</span></span>



| <span data-ttu-id="b6d28-163">Имя</span><span class="sxs-lookup"><span data-stu-id="b6d28-163">Name</span></span>                     | <span data-ttu-id="b6d28-164">Описание</span><span class="sxs-lookup"><span data-stu-id="b6d28-164">Description</span></span>                                                                                                                                                                                                              |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6d28-165">\_ \_ Мягкий режим границы \_ D2D1</span><span class="sxs-lookup"><span data-stu-id="b6d28-165">D2D1\_BORDER\_MODE\_SOFT</span></span> | <span data-ttu-id="b6d28-166">Эффект записывает изображение прозрачными черными пикселями, так как оно применяет ядро размытия, что приводит к мягкому пограничным границе.</span><span class="sxs-lookup"><span data-stu-id="b6d28-166">The effect pads the image with transparent black pixels as it applies the blur kernel, resulting in a soft edge.</span></span> <br/>                                                                                             |
| <span data-ttu-id="b6d28-167">Жесткое D2D1 в \_ \_ режиме границы \_</span><span class="sxs-lookup"><span data-stu-id="b6d28-167">D2D1\_BORDER\_MODE\_HARD</span></span> | <span data-ttu-id="b6d28-168">В результате выходные данные заменяются на размер входного изображения.</span><span class="sxs-lookup"><span data-stu-id="b6d28-168">The effect clamps the output to the size of the input image.</span></span> <span data-ttu-id="b6d28-169">Когда эффект применяет ядро размытия, он расширяет входной образ с помощью преобразования границы зеркального типа для выборок за пределами входных данных.</span><span class="sxs-lookup"><span data-stu-id="b6d28-169">When the effect applies the blur kernel, it extends the input image with a mirror-type border transform for samples outside of the input bounds.</span></span><br/> |



 

## <a name="output-bitmap"></a><span data-ttu-id="b6d28-170">Битовая карта вывода</span><span class="sxs-lookup"><span data-stu-id="b6d28-170">Output bitmap</span></span>

<span data-ttu-id="b6d28-171">Размер выходного растрового изображения увеличивается в зависимости от стандартного отклонения, угла результата и режима границы.</span><span class="sxs-lookup"><span data-stu-id="b6d28-171">The size of the output bitmap increases based on the standard deviation, the angle of the effect, and the border mode.</span></span> <span data-ttu-id="b6d28-172">Если для параметра режим границы задано значение \_ D2D1 \_ границы \_ , размер выходного растрового изображения увеличивается на размер ядра размытия, представленного в пикселях.</span><span class="sxs-lookup"><span data-stu-id="b6d28-172">If the border mode is set to D2D1\_BORDER\_MODE\_SOFT the size of the output bitmap increases by the size of the blur kernel, represented in pixels.</span></span> <span data-ttu-id="b6d28-173">Эти уравнения можно использовать для вычисления размера выходного растрового изображения.</span><span class="sxs-lookup"><span data-stu-id="b6d28-173">These equations can be used to calculate the size of the output bitmap.</span></span>



| <span data-ttu-id="b6d28-174">Требование</span><span class="sxs-lookup"><span data-stu-id="b6d28-174">Requirement</span></span> | <span data-ttu-id="b6d28-175">Значение</span><span class="sxs-lookup"><span data-stu-id="b6d28-175">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="b6d28-176">Увеличение выходного растрового изображения X</span><span class="sxs-lookup"><span data-stu-id="b6d28-176">Output Bitmap Growth X</span></span> | <span data-ttu-id="b6d28-177">Стандартное отклонение (DIP) \* 6 \* ((dpi для пользователей)/96) \* cos (угол))</span><span class="sxs-lookup"><span data-stu-id="b6d28-177">StandardDeviation (DIPs) \* 6 \* ((User DPI) / 96) \* cos(Angle))</span></span> |
| <span data-ttu-id="b6d28-178">Увеличение выходного растрового изображения Y</span><span class="sxs-lookup"><span data-stu-id="b6d28-178">Output Bitmap Growth Y</span></span> | <span data-ttu-id="b6d28-179">Стандартное отклонение (DIP) \* 6 \* ((dpi для пользователей)/96) \* sin (угол))</span><span class="sxs-lookup"><span data-stu-id="b6d28-179">StandardDeviation (DIPs) \* 6 \* ((User DPI) / 96) \* sin(Angle))</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="b6d28-180">Требования</span><span class="sxs-lookup"><span data-stu-id="b6d28-180">Requirements</span></span>



| <span data-ttu-id="b6d28-181">Требование</span><span class="sxs-lookup"><span data-stu-id="b6d28-181">Requirement</span></span> | <span data-ttu-id="b6d28-182">Значение</span><span class="sxs-lookup"><span data-stu-id="b6d28-182">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b6d28-183">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b6d28-183">Minimum supported client</span></span> | <span data-ttu-id="b6d28-184">Windows 8 и обновление платформы для \[ классических приложений Windows 7 \| приложения для Магазина Windows\]</span><span class="sxs-lookup"><span data-stu-id="b6d28-184">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="b6d28-185">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b6d28-185">Minimum supported server</span></span> | <span data-ttu-id="b6d28-186">Windows 8 и обновление платформы для \[ классических приложений Windows 7 \| приложения для Магазина Windows\]</span><span class="sxs-lookup"><span data-stu-id="b6d28-186">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="b6d28-187">Header</span><span class="sxs-lookup"><span data-stu-id="b6d28-187">Header</span></span>                   | <span data-ttu-id="b6d28-188">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="b6d28-188">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="b6d28-189">Библиотека</span><span class="sxs-lookup"><span data-stu-id="b6d28-189">Library</span></span>                  | <span data-ttu-id="b6d28-190">D2D1. lib, дксгуид. lib</span><span class="sxs-lookup"><span data-stu-id="b6d28-190">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="b6d28-191">См. также</span><span class="sxs-lookup"><span data-stu-id="b6d28-191">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b6d28-192">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="b6d28-192">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

