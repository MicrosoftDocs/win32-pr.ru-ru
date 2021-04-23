---
title: Эффект тени
description: Используйте эффект тени, чтобы создать тень из альфа-канала изображения.
ms.assetid: 53525584-10CF-46C2-9400-C4FB225D4693
keywords:
- эффект тени
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c42fd8755078dd79f2b01b623b1839785beb3c3e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340410"
---
# <a name="shadow-effect"></a><span data-ttu-id="07162-104">Эффект тени</span><span class="sxs-lookup"><span data-stu-id="07162-104">Shadow effect</span></span>

<span data-ttu-id="07162-105">Используйте эффект тени, чтобы создать тень из альфа-канала изображения.</span><span class="sxs-lookup"><span data-stu-id="07162-105">Use the shadow effect to generate a shadow from the alpha channel of an image.</span></span> <span data-ttu-id="07162-106">Тень является более непрозрачной для больших альфа-значений и более прозрачной для меньших значений альфа.</span><span class="sxs-lookup"><span data-stu-id="07162-106">The shadow is more opaque for higher alpha values and more transparent for lower alpha values.</span></span> <span data-ttu-id="07162-107">Можно задать степень размытия и цвет тени.</span><span class="sxs-lookup"><span data-stu-id="07162-107">You can set the amount of blur and the color of the shadow.</span></span>

-   [<span data-ttu-id="07162-108">Пример изображения</span><span class="sxs-lookup"><span data-stu-id="07162-108">Example image</span></span>](#example-image)
-   [<span data-ttu-id="07162-109">Свойства эффектов</span><span class="sxs-lookup"><span data-stu-id="07162-109">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="07162-110">Режимы оптимизации</span><span class="sxs-lookup"><span data-stu-id="07162-110">Optimization modes</span></span>](#optimization-modes)
-   [<span data-ttu-id="07162-111">Битовая карта вывода</span><span class="sxs-lookup"><span data-stu-id="07162-111">Output bitmap</span></span>](#output-bitmap)
-   [<span data-ttu-id="07162-112">Требования</span><span class="sxs-lookup"><span data-stu-id="07162-112">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="07162-113">См. также</span><span class="sxs-lookup"><span data-stu-id="07162-113">Related topics</span></span>](#related-topics)

<span data-ttu-id="07162-114">Идентификатором CLSID для этого действия является CLSID \_ D2D1Shadow.</span><span class="sxs-lookup"><span data-stu-id="07162-114">The CLSID for this effect is CLSID\_D2D1Shadow.</span></span>

## <a name="example-image"></a><span data-ttu-id="07162-115">Пример изображения</span><span class="sxs-lookup"><span data-stu-id="07162-115">Example image</span></span>

<span data-ttu-id="07162-116">В этом примере показаны выходные данные эффект тени, переведенный вниз и вправо, с исходным изображением, совмещенным над ним в исходном расположении.</span><span class="sxs-lookup"><span data-stu-id="07162-116">The example here shows the output of the shadow effect translated down and right with the source image composited over it in the original location.</span></span> <span data-ttu-id="07162-117">Эффект тени выводит только тень.</span><span class="sxs-lookup"><span data-stu-id="07162-117">The shadow effect only outputs the shadow.</span></span>



| <span data-ttu-id="07162-118">До</span><span class="sxs-lookup"><span data-stu-id="07162-118">Before</span></span>                                                  |
|---------------------------------------------------------|
| ![изображение перед результатом.](images/8-crop.png)      |
| <span data-ttu-id="07162-120">После</span><span class="sxs-lookup"><span data-stu-id="07162-120">After</span></span>                                                   |
| ![изображение после преобразования.](images/25-shadow.png) |



 


```C++
ComPtr<ID2D1Effect> shadowEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Shadow, &shadowEffect);

shadowEffect->SetInput(0, bitmap);

// Shadow is composited on top of a white surface to show opacity.
ComPtr<ID2D1Effect> floodEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Flood, &floodEffect);

floodEffect->SetValue(D2D1_FLOOD_PROP_COLOR, D2D1::Vector4F(1.0f, 1.0f, 1.0f, 1.0f));

ComPtr<ID2D1Effect> affineTransformEffect;
m_d2dContext->CreateEffect(CLSID_D2D12DAffineTransform, &affineTransformEffect);

affineTransformEffect->SetInputEffect(0, shadowEffect.Get());

D2D1_MATRIX_3X2_F matrix = D2D1::Matrix3x2F::Translation(20, 20));

affineTransformEffect->SetValue(D2D1_2DAFFINETRANSFORM_PROP_TRANSFORM_MATRIX, matrix);

ComPtr<ID2D1Effect> compositeEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Composite, &compositeEffect);

compositeEffect->SetInputEffect(0, floodEffect.Get());
compositeEffect->SetInputEffect(1, affineTransformEffect.Get());
compositeEffect->SetInput(2, bitmap);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(compositeEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a><span data-ttu-id="07162-122">Свойства эффектов</span><span class="sxs-lookup"><span data-stu-id="07162-122">Effect properties</span></span>



| <span data-ttu-id="07162-123">Отображаемое имя и перечисление индекса</span><span class="sxs-lookup"><span data-stu-id="07162-123">Display name and index enumeration</span></span>                                                        | <span data-ttu-id="07162-124">Описание</span><span class="sxs-lookup"><span data-stu-id="07162-124">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07162-125">блурстандарддевиатион</span><span class="sxs-lookup"><span data-stu-id="07162-125">BlurStandardDeviation</span></span><br/> <span data-ttu-id="07162-126">\_ \_ \_ \_ Стандартное отклонение размытия D2D1 Shadow Prop \_</span><span class="sxs-lookup"><span data-stu-id="07162-126">D2D1\_SHADOW\_PROP\_BLUR\_STANDARD\_DEVIATION</span></span><br/> | <span data-ttu-id="07162-127">Объем размытия, применяемый к альфа-каналу изображения.</span><span class="sxs-lookup"><span data-stu-id="07162-127">The amount of blur to be applied to the alpha channel of the image.</span></span> <span data-ttu-id="07162-128">Можно вычислить Радиус размытия ядра, умножив стандартное отклонение на 3.</span><span class="sxs-lookup"><span data-stu-id="07162-128">You can compute the blur radius of the kernel by multiplying the standard deviation by 3.</span></span> <span data-ttu-id="07162-129">Единицы как стандартного отклонения, так и размытого радиуса являются DIP.</span><span class="sxs-lookup"><span data-stu-id="07162-129">The units of both the standard deviation and blur radius are DIPs.</span></span><br/> <span data-ttu-id="07162-130">Это свойство аналогично свойству отклонение по стандартам [размытия по Гауссу](gaussian-blur.md) .</span><span class="sxs-lookup"><span data-stu-id="07162-130">This property is the same as the [Gaussian Blur](gaussian-blur.md) standard deviation property.</span></span> <br/> <span data-ttu-id="07162-131">Тип — FLOAT.</span><span class="sxs-lookup"><span data-stu-id="07162-131">The type is FLOAT.</span></span><br/> <span data-ttu-id="07162-132">Значение по умолчанию — 3.0 f.</span><span class="sxs-lookup"><span data-stu-id="07162-132">The default value is 3.0f.</span></span><br/> |
| <span data-ttu-id="07162-133">Цвет</span><span class="sxs-lookup"><span data-stu-id="07162-133">Color</span></span><br/> <span data-ttu-id="07162-134">\_Цвет D2D1 \_ shadow \_</span><span class="sxs-lookup"><span data-stu-id="07162-134">D2D1\_SHADOW\_PROP\_COLOR</span></span><br/>                                     | <span data-ttu-id="07162-135">Цвет тени.</span><span class="sxs-lookup"><span data-stu-id="07162-135">The color of the drop shadow.</span></span> <span data-ttu-id="07162-136">Это свойство является D2D1 \_ вектором \_ 4F, определенным как: (R, G, B, a).</span><span class="sxs-lookup"><span data-stu-id="07162-136">This property is a D2D1\_VECTOR\_4F defined as: (R, G, B, A).</span></span> <span data-ttu-id="07162-137">Этот цвет необходимо указать в виде прямой альфа-составляющей.</span><span class="sxs-lookup"><span data-stu-id="07162-137">You must specify this color in straight alpha.</span></span><br/> <span data-ttu-id="07162-138">Тип — D2D1 \_ vector \_ 4F.</span><span class="sxs-lookup"><span data-stu-id="07162-138">The type is D2D1\_VECTOR\_4F.</span></span><br/> <span data-ttu-id="07162-139">Значение по умолчанию — {0.0 f, 0,0 f, 0,0 f, 1,0 f}.</span><span class="sxs-lookup"><span data-stu-id="07162-139">The default value is {0.0f, 0.0f, 0.0f, 1.0f}.</span></span><br/>                                                                                                                                                                     |
| <span data-ttu-id="07162-140">Optimization</span><span class="sxs-lookup"><span data-stu-id="07162-140">Optimization</span></span><br/> <span data-ttu-id="07162-141">\_Оптимизация D2D1 Shadow \_ prop \_</span><span class="sxs-lookup"><span data-stu-id="07162-141">D2D1\_SHADOW\_PROP\_OPTIMIZATION</span></span><br/>                       | <span data-ttu-id="07162-142">Уровень оптимизации производительности.</span><span class="sxs-lookup"><span data-stu-id="07162-142">The level of performance optimization.</span></span><br/> <span data-ttu-id="07162-143">Тип — D2D1 с \_ \_ оптимизацией тени.</span><span class="sxs-lookup"><span data-stu-id="07162-143">The type is D2D1\_SHADOW\_OPTIMIZATION.</span></span><br/> <span data-ttu-id="07162-144">Значение по умолчанию — D2D1 с \_ \_ балансировкой теневой оптимизации \_ .</span><span class="sxs-lookup"><span data-stu-id="07162-144">The default value is D2D1\_SHADOW\_OPTIMIZATION\_BALANCED.</span></span><br/>                                                                                                                                                                                                                                                   |



 

## <a name="optimization-modes"></a><span data-ttu-id="07162-145">Режимы оптимизации</span><span class="sxs-lookup"><span data-stu-id="07162-145">Optimization modes</span></span>



| <span data-ttu-id="07162-146">Имя</span><span class="sxs-lookup"><span data-stu-id="07162-146">Name</span></span>                                          | <span data-ttu-id="07162-147">Описание</span><span class="sxs-lookup"><span data-stu-id="07162-147">Description</span></span>                                                                                                                           |
|-----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07162-148">\_ \_ Скорость оптимизации D2D1 \_ директионалблур</span><span class="sxs-lookup"><span data-stu-id="07162-148">D2D1\_DIRECTIONALBLUR\_OPTIMIZATION\_SPEED</span></span>    | <span data-ttu-id="07162-149">Применяет внутренние оптимизации, такие как предварительное масштабирование относительно небольших радиусов.</span><span class="sxs-lookup"><span data-stu-id="07162-149">Applies internal optimizations such as pre-scaling at relatively small radii.</span></span> <span data-ttu-id="07162-150">Использует линейную фильтрацию.</span><span class="sxs-lookup"><span data-stu-id="07162-150">Uses linear filtering.</span></span>                                  |
| <span data-ttu-id="07162-151">\_ \_ Сбалансированная оптимизация D2D1 директионалблур \_</span><span class="sxs-lookup"><span data-stu-id="07162-151">D2D1\_DIRECTIONALBLUR\_OPTIMIZATION\_BALANCED</span></span> | <span data-ttu-id="07162-152">Использует те же пороговые значения оптимизации, что и режим скорости, но использует фильтрацию трилинейной.</span><span class="sxs-lookup"><span data-stu-id="07162-152">Uses the same optimization thresholds as Speed mode, but uses trilinear filtering.</span></span>                                                    |
| <span data-ttu-id="07162-153">\_ \_ Качество оптимизации D2D1 \_ директионалблур</span><span class="sxs-lookup"><span data-stu-id="07162-153">D2D1\_DIRECTIONALBLUR\_OPTIMIZATION\_QUALITY</span></span>  | <span data-ttu-id="07162-154">В используются только внутренние оптимизации с большими радиусами, где приближение меньше вероятно должно быть видимым.</span><span class="sxs-lookup"><span data-stu-id="07162-154">Only uses internal optimizations with large blur radii, where approximations are less likely to be visible.</span></span> <span data-ttu-id="07162-155">Использует фильтрацию трилинейной.</span><span class="sxs-lookup"><span data-stu-id="07162-155">Uses trilinear filtering.</span></span> |



 

## <a name="output-bitmap"></a><span data-ttu-id="07162-156">Битовая карта вывода</span><span class="sxs-lookup"><span data-stu-id="07162-156">Output bitmap</span></span>

<span data-ttu-id="07162-157">Размер выходного растрового изображения — это размер выходных данных размытия.</span><span class="sxs-lookup"><span data-stu-id="07162-157">The size of the output bitmap is the size of the blur output.</span></span> <span data-ttu-id="07162-158">Сумма увеличения выходного растрового изображения относительно исходного точечного рисунка может быть рассчитана с помощью следующего уравнения:</span><span class="sxs-lookup"><span data-stu-id="07162-158">The amount the output bitmap growth relative to the original bitmap can be calculated using the following equation:</span></span>

<span data-ttu-id="07162-159">Увеличение битовой карты вывода (X и Y) = Блурстандарддевиатион (аппаратно-независимые пиксели (DIP)) \* 6 \* (dpi для пользователей)/96</span><span class="sxs-lookup"><span data-stu-id="07162-159">Output Bitmap Growth (X and Y) = BlurStandardDeviation (device-independent pixels (DIPs))\*6\*(User DPI)/96</span></span>

<span data-ttu-id="07162-160">Выходные данные увеличиваются одинаково во всем направлении. Например, если размер увеличивается на 10 пикселей в каждом направлении, левый верхний угол точечного рисунка расположен в (-5,-5), а нижний правый — в (105, 105), как показано на диаграмме здесь.</span><span class="sxs-lookup"><span data-stu-id="07162-160">The output increases equally in all direction, so for example if the size increases by 10 pixels in each direction, the upper left corner of the bitmap is located at (-5, -5) and the lower right will be at (105, 105) as shown in the diagram here.</span></span>

![Схема роста размера выходных данных эффект тени.](images/drop-shadow-output-growth.png)

## <a name="requirements"></a><span data-ttu-id="07162-162">Требования</span><span class="sxs-lookup"><span data-stu-id="07162-162">Requirements</span></span>



| <span data-ttu-id="07162-163">Требование</span><span class="sxs-lookup"><span data-stu-id="07162-163">Requirement</span></span> | <span data-ttu-id="07162-164">Значение</span><span class="sxs-lookup"><span data-stu-id="07162-164">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="07162-165">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="07162-165">Minimum supported client</span></span> | <span data-ttu-id="07162-166">Windows 8 и обновление платформы для \[ классических приложений Windows 7 \| приложения для Магазина Windows\]</span><span class="sxs-lookup"><span data-stu-id="07162-166">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="07162-167">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="07162-167">Minimum supported server</span></span> | <span data-ttu-id="07162-168">Windows 8 и обновление платформы для \[ классических приложений Windows 7 \| приложения для Магазина Windows\]</span><span class="sxs-lookup"><span data-stu-id="07162-168">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="07162-169">Header</span><span class="sxs-lookup"><span data-stu-id="07162-169">Header</span></span>                   | <span data-ttu-id="07162-170">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="07162-170">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="07162-171">Библиотека</span><span class="sxs-lookup"><span data-stu-id="07162-171">Library</span></span>                  | <span data-ttu-id="07162-172">D2D1. lib, дксгуид. lib</span><span class="sxs-lookup"><span data-stu-id="07162-172">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="07162-173">См. также</span><span class="sxs-lookup"><span data-stu-id="07162-173">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="07162-174">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="07162-174">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

