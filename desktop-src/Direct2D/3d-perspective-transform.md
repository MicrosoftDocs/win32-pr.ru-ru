---
title: Эффект трехмерного преобразования перспективы
description: Используйте эффект преобразование Трехмерная перспектива для поворота изображения в 3 измерения, как при просмотре с расстояния.
ms.assetid: 0E1A940E-2DCA-4772-BB68-7E5EF5CEF833
keywords:
- трехмерный эффект преобразования перспективы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ed2b1c5131319dd711d2c7802a0bfabceaaa32e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892778"
---
# <a name="3d-perspective-transform-effect"></a><span data-ttu-id="9f468-104">Эффект трехмерного преобразования перспективы</span><span class="sxs-lookup"><span data-stu-id="9f468-104">3D perspective transform effect</span></span>

<span data-ttu-id="9f468-105">Используйте эффект преобразование Трехмерная перспектива для поворота изображения в 3 измерения, как при просмотре с расстояния.</span><span class="sxs-lookup"><span data-stu-id="9f468-105">Use the 3D perspective transform effect to rotate the image in 3 dimensions as if viewed from a distance.</span></span>

<span data-ttu-id="9f468-106">Преобразование «Трехмерная перспектива» является более удобным, чем эффект трехмерного преобразования, но предоставляет только подмножество функциональных возможностей.</span><span class="sxs-lookup"><span data-stu-id="9f468-106">The 3D perspective transform is more convenient than the 3D transform effect, but only exposes a subset of the functionality.</span></span> <span data-ttu-id="9f468-107">Можно вычислить полную матрицу трехмерного преобразования и применить к изображению более произвольную матрицу преобразования, используя эффект [трехмерного преобразования](3d-transform.md) .</span><span class="sxs-lookup"><span data-stu-id="9f468-107">You can compute a full 3D transformation matrix and apply a more arbitrary transform matrix to an image using the [3D transform](3d-transform.md) effect.</span></span>

<span data-ttu-id="9f468-108">Идентификатором CLSID для этого действия является CLSID \_ D2D13DPerspectiveTransform.</span><span class="sxs-lookup"><span data-stu-id="9f468-108">The CLSID for this effect is CLSID\_D2D13DPerspectiveTransform.</span></span>

-   [<span data-ttu-id="9f468-109">Пример изображения</span><span class="sxs-lookup"><span data-stu-id="9f468-109">Example image</span></span>](#example-image)
-   [<span data-ttu-id="9f468-110">Свойства эффектов</span><span class="sxs-lookup"><span data-stu-id="9f468-110">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="9f468-111">Режимы интерполяции</span><span class="sxs-lookup"><span data-stu-id="9f468-111">Interpolation modes</span></span>](#interpolation-modes)
-   [<span data-ttu-id="9f468-112">Режимы границ</span><span class="sxs-lookup"><span data-stu-id="9f468-112">Border modes</span></span>](#border-modes)
-   [<span data-ttu-id="9f468-113">Битовая карта вывода</span><span class="sxs-lookup"><span data-stu-id="9f468-113">Output bitmap</span></span>](#output-bitmap)
-   [<span data-ttu-id="9f468-114">Требования</span><span class="sxs-lookup"><span data-stu-id="9f468-114">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="9f468-115">См. также</span><span class="sxs-lookup"><span data-stu-id="9f468-115">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="9f468-116">Пример изображения</span><span class="sxs-lookup"><span data-stu-id="9f468-116">Example image</span></span>



| <span data-ttu-id="9f468-117">До</span><span class="sxs-lookup"><span data-stu-id="9f468-117">Before</span></span>                                                               |
|----------------------------------------------------------------------|
| ![изображение перед результатом.](images/default-before.jpg)           |
| <span data-ttu-id="9f468-119">После</span><span class="sxs-lookup"><span data-stu-id="9f468-119">After</span></span>                                                                |
| ![изображение после этого действия.](images/23-3dperspectivetransform.png) |



 


```C++
ComPtr<ID2D1Effect> perspectiveTransformEffect;
m_d2dContext->CreateEffect(CLSID_D2D13DPerspectiveTransform, &perspectiveTransformEffect);

perspectiveTransformEffect->SetInput(0, bitmap);

perspectiveTransformEffect->SetValue(D2D1_3DPERSPECTIVETRANSFORM_PROP_PERSPECTIVE_ORIGIN, D2D1::Vector3F(0.0f, 192.0f, 0.0f));
perspectiveTransformEffect->SetValue(D2D1_3DPERSPECTIVETRANSFORM_PROP_ROTATION, D2D1::Vector3F(0.0f, 30.0f, 0.0f));

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(perspectiveTransformEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a><span data-ttu-id="9f468-121">Свойства эффектов</span><span class="sxs-lookup"><span data-stu-id="9f468-121">Effect properties</span></span>



| <span data-ttu-id="9f468-122">Отображаемое имя и перечисление индекса</span><span class="sxs-lookup"><span data-stu-id="9f468-122">Display name and index enumeration</span></span>                                                              | <span data-ttu-id="9f468-123">Описание</span><span class="sxs-lookup"><span data-stu-id="9f468-123">Description</span></span>                                                                                                                                                                                                                                                                                        |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f468-124">интерполатионмоде</span><span class="sxs-lookup"><span data-stu-id="9f468-124">InterpolationMode</span></span><br/> <span data-ttu-id="9f468-125">\_ \_ \_ Режим интерполяции D2D1 3DPERSPECTIVETRANSFORM Prop \_</span><span class="sxs-lookup"><span data-stu-id="9f468-125">D2D1\_3DPERSPECTIVETRANSFORM\_PROP\_INTERPOLATION\_MODE</span></span><br/> | <span data-ttu-id="9f468-126">Режим интерполяции, используемый в изображении в результате применения.</span><span class="sxs-lookup"><span data-stu-id="9f468-126">The interpolation mode the effect uses on the image.</span></span> <span data-ttu-id="9f468-127">Существует 5 режимов масштабирования, имеющих высокое качество и скорость.</span><span class="sxs-lookup"><span data-stu-id="9f468-127">There are 5 scale modes that range in quality and speed.</span></span><br/> <span data-ttu-id="9f468-128">Тип — D2D1 \_ 3DPERSPECTIVETRANSFORM \_ Режим интерполяции \_ .</span><span class="sxs-lookup"><span data-stu-id="9f468-128">Type is D2D1\_3DPERSPECTIVETRANSFORM\_INTERPOLATION\_MODE.</span></span><br/> <span data-ttu-id="9f468-129">Значение по умолчанию — D2D1 \_ 3DPERSPECTIVETRANSFORM \_ Режим интерполяции — \_ \_ линейный.</span><span class="sxs-lookup"><span data-stu-id="9f468-129">Default value is D2D1\_3DPERSPECTIVETRANSFORM\_INTERPOLATION\_MODE\_LINEAR.</span></span><br/>              |
| <span data-ttu-id="9f468-130">бордермоде</span><span class="sxs-lookup"><span data-stu-id="9f468-130">BorderMode</span></span><br/> <span data-ttu-id="9f468-131">\_Режим границы D2D1 3DPERSPECTIVETRANSFORM " \_ prop" \_ \_</span><span class="sxs-lookup"><span data-stu-id="9f468-131">D2D1\_3DPERSPECTIVETRANSFORM\_PROP\_BORDER\_MODE</span></span><br/>               | <span data-ttu-id="9f468-132">Режим, используемый для вычисления границы изображения: Soft или Hard.</span><span class="sxs-lookup"><span data-stu-id="9f468-132">The mode used to calculate the border of the image, soft or hard.</span></span> <span data-ttu-id="9f468-133">Дополнительные сведения см. в разделе [режимы границ](https://www.bing.com/search?q=Border+modes) .</span><span class="sxs-lookup"><span data-stu-id="9f468-133">See [Border modes](https://www.bing.com/search?q=Border+modes) for more info.</span></span><br/> <span data-ttu-id="9f468-134">Тип — D2D1 \_ границы \_ .</span><span class="sxs-lookup"><span data-stu-id="9f468-134">Type is D2D1\_BORDER\_MODE.</span></span><br/> <span data-ttu-id="9f468-135">Значение по умолчанию — D2D1 в \_ \_ режиме границы \_ .</span><span class="sxs-lookup"><span data-stu-id="9f468-135">Default value is D2D1\_BORDER\_MODE\_SOFT.</span></span><br/>                                                              |
| <span data-ttu-id="9f468-136">Глубина</span><span class="sxs-lookup"><span data-stu-id="9f468-136">Depth</span></span><br/> <span data-ttu-id="9f468-137">\_Глубина D2D1 \_ 3DPERSPECTIVETRANSFORM \_</span><span class="sxs-lookup"><span data-stu-id="9f468-137">D2D1\_3DPERSPECTIVETRANSFORM\_PROP\_DEPTH</span></span><br/>                           | <span data-ttu-id="9f468-138">Расстояние от *перспективеоригин* до плоскости проекции.</span><span class="sxs-lookup"><span data-stu-id="9f468-138">The distance from the *PerspectiveOrigin* to the projection plane.</span></span> <span data-ttu-id="9f468-139">Значение, указанное в параметре DIP и, должно быть больше 0.</span><span class="sxs-lookup"><span data-stu-id="9f468-139">The value specified in DIPs and must be greater than 0.</span></span><br/> <span data-ttu-id="9f468-140">Тип — FLOAT.</span><span class="sxs-lookup"><span data-stu-id="9f468-140">Type is FLOAT.</span></span><br/> <span data-ttu-id="9f468-141">Значение по умолчанию — 1000.0 f.</span><span class="sxs-lookup"><span data-stu-id="9f468-141">Default value is 1000.0f.</span></span><br/>                                                                                               |
| <span data-ttu-id="9f468-142">перспективеоригин</span><span class="sxs-lookup"><span data-stu-id="9f468-142">PerspectiveOrigin</span></span><br/> <span data-ttu-id="9f468-143">\_ \_ \_ Источник перспективы D2D1 3DPERSPECTIVETRANSFORM \_ prop</span><span class="sxs-lookup"><span data-stu-id="9f468-143">D2D1\_3DPERSPECTIVETRANSFORM\_PROP\_PERSPECTIVE\_ORIGIN</span></span><br/> | <span data-ttu-id="9f468-144">Позиция X и Y средства просмотра в трехмерной сцене.</span><span class="sxs-lookup"><span data-stu-id="9f468-144">The X and Y location of the viewer in the 3D scene.</span></span> <span data-ttu-id="9f468-145">Это свойство является D2D1 \_ вектором \_ 2F, определенным как: (точка X, точка Y).</span><span class="sxs-lookup"><span data-stu-id="9f468-145">This property is a D2D1\_VECTOR\_2F defined as: (point X, point Y).</span></span> <span data-ttu-id="9f468-146">Единицы измерения — DIP.</span><span class="sxs-lookup"><span data-stu-id="9f468-146">The units are in DIPs.</span></span><br/> <span data-ttu-id="9f468-147">Значение Z задается с помощью свойства *Depth* .</span><span class="sxs-lookup"><span data-stu-id="9f468-147">You set the Z value with the *Depth* property.</span></span><br/> <span data-ttu-id="9f468-148">Тип — D2D1 \_ vector \_ 2F.</span><span class="sxs-lookup"><span data-stu-id="9f468-148">Type is D2D1\_VECTOR\_2F.</span></span><br/> <span data-ttu-id="9f468-149">Значение по умолчанию — {0.0 f, 0,0 f}.</span><span class="sxs-lookup"><span data-stu-id="9f468-149">Default value is {0.0f, 0.0f}.</span></span><br/> |
| <span data-ttu-id="9f468-150">локалоффсет</span><span class="sxs-lookup"><span data-stu-id="9f468-150">LocalOffset</span></span><br/> <span data-ttu-id="9f468-151">\_ \_ \_ Локальное смещение D2D1 3DPERSPECTIVETRANSFORM Prop \_</span><span class="sxs-lookup"><span data-stu-id="9f468-151">D2D1\_3DPERSPECTIVETRANSFORM\_PROP\_LOCAL\_OFFSET</span></span><br/>             | <span data-ttu-id="9f468-152">Преобразование, выполняемое этим действием перед поворотом плоскости проекции.</span><span class="sxs-lookup"><span data-stu-id="9f468-152">A translation the effect performs before it rotates the projection plane.</span></span> <span data-ttu-id="9f468-153">Это свойство является D2D1 \_ вектором \_ 3F, определенным как: (X, Y, Z).</span><span class="sxs-lookup"><span data-stu-id="9f468-153">This property is a D2D1\_VECTOR\_3F defined as: (X, Y, Z).</span></span> <span data-ttu-id="9f468-154">Единицы измерения — DIP.</span><span class="sxs-lookup"><span data-stu-id="9f468-154">The units are in DIPs.</span></span><br/> <span data-ttu-id="9f468-155">Тип — D2D1 \_ vector \_ 3F.</span><span class="sxs-lookup"><span data-stu-id="9f468-155">Type is D2D1\_VECTOR\_3F.</span></span><br/> <span data-ttu-id="9f468-156">Значение по умолчанию — {0.0 f, 0,0 f, 0,0 f}.</span><span class="sxs-lookup"><span data-stu-id="9f468-156">Default value is {0.0f, 0.0f, 0.0f}.</span></span><br/>                                        |
| <span data-ttu-id="9f468-157">глобалоффсет</span><span class="sxs-lookup"><span data-stu-id="9f468-157">GlobalOffset</span></span><br/> <span data-ttu-id="9f468-158">\_ \_ \_ Глобальное смещение D2D1 3DPERSPECTIVETRANSFORM \_</span><span class="sxs-lookup"><span data-stu-id="9f468-158">D2D1\_3DPERSPECTIVETRANSFORM\_PROP\_GLOBAL\_OFFSET</span></span><br/>           | <span data-ttu-id="9f468-159">Перевод, который выполняет действие после поворота плоскости проекции.</span><span class="sxs-lookup"><span data-stu-id="9f468-159">A translation the effect performs after it rotates the projection plane.</span></span> <span data-ttu-id="9f468-160">Это свойство является D2D1 \_ вектором \_ 3F, определенным как: (X, Y, Z).</span><span class="sxs-lookup"><span data-stu-id="9f468-160">This property is a D2D1\_VECTOR\_3F defined as: (X, Y, Z).</span></span> <span data-ttu-id="9f468-161">Единицы измерения — DIP.</span><span class="sxs-lookup"><span data-stu-id="9f468-161">The units are in DIPs.</span></span><br/> <span data-ttu-id="9f468-162">Тип — D2D1 \_ vector \_ 3F.</span><span class="sxs-lookup"><span data-stu-id="9f468-162">Type is D2D1\_VECTOR\_3F.</span></span><br/> <span data-ttu-id="9f468-163">Значение по умолчанию — {0.0 f, 0,0 f, 0,0 f}.</span><span class="sxs-lookup"><span data-stu-id="9f468-163">Default value is {0.0f, 0.0f, 0.0f}.</span></span><br/>                                         |
| <span data-ttu-id="9f468-164">ротатионоригин</span><span class="sxs-lookup"><span data-stu-id="9f468-164">RotationOrigin</span></span><br/> <span data-ttu-id="9f468-165">\_ \_ \_ Начало вращения D2D1 3DPERSPECTIVETRANSFORM \_ prop</span><span class="sxs-lookup"><span data-stu-id="9f468-165">D2D1\_3DPERSPECTIVETRANSFORM\_PROP\_ROTATION\_ORIGIN</span></span><br/>       | <span data-ttu-id="9f468-166">Центральная точка вращения, выполняемой действием.</span><span class="sxs-lookup"><span data-stu-id="9f468-166">The center point of the rotation the effect performs.</span></span> <span data-ttu-id="9f468-167">Это свойство является D2D1 \_ вектором \_ 3F, определенным как: (X, Y, Z).</span><span class="sxs-lookup"><span data-stu-id="9f468-167">This property is a D2D1\_VECTOR\_3F defined as: (X, Y, Z).</span></span> <span data-ttu-id="9f468-168">Единицы измерения — DIP.</span><span class="sxs-lookup"><span data-stu-id="9f468-168">The units are in DIPs.</span></span><br/> <span data-ttu-id="9f468-169">Тип — D2D1 \_ vector \_ 3F.</span><span class="sxs-lookup"><span data-stu-id="9f468-169">Type is D2D1\_VECTOR\_3F.</span></span><br/> <span data-ttu-id="9f468-170">Значение по умолчанию — {0.0 f, 0,0 f, 0,0 f}.</span><span class="sxs-lookup"><span data-stu-id="9f468-170">Default value is {0.0f, 0.0f, 0.0f}.</span></span><br/>                                                            |
| <span data-ttu-id="9f468-171">Поворот</span><span class="sxs-lookup"><span data-stu-id="9f468-171">Rotation</span></span><br/> <span data-ttu-id="9f468-172">D2D1 \_ 3DPERSPECTIVETRANSFORM \_ prop \_</span><span class="sxs-lookup"><span data-stu-id="9f468-172">D2D1\_3DPERSPECTIVETRANSFORM\_PROP\_ROTATION</span></span><br/>                     | <span data-ttu-id="9f468-173">Угол поворота для каждой оси.</span><span class="sxs-lookup"><span data-stu-id="9f468-173">The angles of rotation for each axis.</span></span> <span data-ttu-id="9f468-174">Это свойство является D2D1 \_ вектором \_ 3F, определенным как: (X, Y, Z).</span><span class="sxs-lookup"><span data-stu-id="9f468-174">This property is a D2D1\_VECTOR\_3F defined as: (X, Y, Z).</span></span> <span data-ttu-id="9f468-175">Единицы измерения — в градусах.</span><span class="sxs-lookup"><span data-stu-id="9f468-175">The units are in degrees.</span></span><br/> <span data-ttu-id="9f468-176">Тип — D2D1 \_ vector \_ 3F.</span><span class="sxs-lookup"><span data-stu-id="9f468-176">Type is D2D1\_VECTOR\_3F.</span></span><br/> <span data-ttu-id="9f468-177">Значение по умолчанию — {0.0 f, 0,0 f, 0,0 f}.</span><span class="sxs-lookup"><span data-stu-id="9f468-177">Default value is {0.0f, 0.0f, 0.0f}.</span></span><br/>                                                                         |



 

## <a name="interpolation-modes"></a><span data-ttu-id="9f468-178">Режимы интерполяции</span><span class="sxs-lookup"><span data-stu-id="9f468-178">Interpolation modes</span></span>



| <span data-ttu-id="9f468-179">Перечисление</span><span class="sxs-lookup"><span data-stu-id="9f468-179">Enumeration</span></span>                                                              | <span data-ttu-id="9f468-180">Описание</span><span class="sxs-lookup"><span data-stu-id="9f468-180">Description</span></span>                                                                                                                                                |
|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f468-181">\_ \_ \_ \_ Ближайший сосед в режиме интерполяции D2D1 3DPERSPECTIVETRANSFORM \_</span><span class="sxs-lookup"><span data-stu-id="9f468-181">D2D1\_3DPERSPECTIVETRANSFORM\_INTERPOLATION\_MODE\_NEAREST\_NEIGHBOR</span></span>     | <span data-ttu-id="9f468-182">Выбирает ближайшую одиночную точку и использует ее.</span><span class="sxs-lookup"><span data-stu-id="9f468-182">Samples the nearest single point and uses that.</span></span> <span data-ttu-id="9f468-183">В этом режиме используется меньше времени на обработку, но выводится изображение самого низкого качества.</span><span class="sxs-lookup"><span data-stu-id="9f468-183">This mode uses less processing time, but outputs the lowest quality image.</span></span>                                 |
| <span data-ttu-id="9f468-184">\_ \_ Линейный режим интерполяции D2D1 3DPERSPECTIVETRANSFORM \_ \_</span><span class="sxs-lookup"><span data-stu-id="9f468-184">D2D1\_3DPERSPECTIVETRANSFORM\_INTERPOLATION\_MODE\_LINEAR</span></span>                | <span data-ttu-id="9f468-185">Использует выборку с четырьмя точками и линейную интерполяцию.</span><span class="sxs-lookup"><span data-stu-id="9f468-185">Uses a four point sample and linear interpolation.</span></span> <span data-ttu-id="9f468-186">Этот режим использует больше времени на обработку, чем ближайший соседний режим, но выводит изображение более высокого качества.</span><span class="sxs-lookup"><span data-stu-id="9f468-186">This mode uses more processing time than the nearest neighbor mode, but outputs a higher quality image.</span></span> |
| <span data-ttu-id="9f468-187">D2D1 \_ 3DPERSPECTIVETRANSFORM \_ Режим интерполяции ( \_ \_ кубический)</span><span class="sxs-lookup"><span data-stu-id="9f468-187">D2D1\_3DPERSPECTIVETRANSFORM\_INTERPOLATION\_MODE\_CUBIC</span></span>                 | <span data-ttu-id="9f468-188">Использует 16-примерный ядро кубических для интерполяции.</span><span class="sxs-lookup"><span data-stu-id="9f468-188">Uses a 16 sample cubic kernel for interpolation.</span></span> <span data-ttu-id="9f468-189">Этот режим использует наибольшее время обработки, но выводит изображение с более высоким качеством.</span><span class="sxs-lookup"><span data-stu-id="9f468-189">This mode uses the most processing time, but outputs a higher quality image.</span></span>                              |
| <span data-ttu-id="9f468-190">D2D1 \_ 3DPERSPECTIVETRANSFORM \_ Режим интерполяции — \_ \_ \_ многопримерная \_ линейная</span><span class="sxs-lookup"><span data-stu-id="9f468-190">D2D1\_3DPERSPECTIVETRANSFORM\_INTERPOLATION\_MODE\_MULTI\_SAMPLE\_LINEAR</span></span> | <span data-ttu-id="9f468-191">Использует 4 линейных образца в пределах одного пикселя для удобного сглаживания.</span><span class="sxs-lookup"><span data-stu-id="9f468-191">Uses 4 linear samples within a single pixel for good edge anti-aliasing.</span></span> <span data-ttu-id="9f468-192">Этот режим хорошо подходит для уменьшения масштаба по небольшим объемам на изображениях с небольшими пикселями.</span><span class="sxs-lookup"><span data-stu-id="9f468-192">This mode is good for scaling down by small amounts on images with few pixels.</span></span>    |
| <span data-ttu-id="9f468-193">D2D1 \_ 3DPERSPECTIVETRANSFORM \_ Режим интерполяции — \_ \_ анизотропная</span><span class="sxs-lookup"><span data-stu-id="9f468-193">D2D1\_3DPERSPECTIVETRANSFORM\_INTERPOLATION\_MODE\_ANISOTROPIC</span></span>           | <span data-ttu-id="9f468-194">Использует анизотропную фильтрацию для выборки шаблона в соответствии с преобразованной формой точечного рисунка.</span><span class="sxs-lookup"><span data-stu-id="9f468-194">Uses anisotropic filtering to sample a pattern according to the transformed shape of the bitmap.</span></span>                                                           |



 

> [!Note]  
> <span data-ttu-id="9f468-195">Если не выбрать режим, то по умолчанию будет применяться \_ \_ линейный режим интерполяции D2D1 3DPERSPECTIVETRANSFORM \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="9f468-195">If you don't select a mode, the effect defaults to D2D1\_3DPERSPECTIVETRANSFORM\_INTERPOLATION\_MODE\_LINEAR.</span></span>

 

> [!Note]  
> <span data-ttu-id="9f468-196">В режиме анизотропного масштабирования создается MIP-карты при масштабировании, однако если для свойства **кэширования** задано значение true для эффектов, вводимых в результате этого эффекта, MIP-карты не будет создаваться каждый раз для достаточного размера изображений.</span><span class="sxs-lookup"><span data-stu-id="9f468-196">Anisotropic mode generates mipmaps when scaling, however, if you set the **Cached** property to true on the effects that are input to this effect, the mipmaps won't be generated every time for sufficiently small images.</span></span>

 

## <a name="border-modes"></a><span data-ttu-id="9f468-197">Режимы границ</span><span class="sxs-lookup"><span data-stu-id="9f468-197">Border modes</span></span>



| <span data-ttu-id="9f468-198">Имя</span><span class="sxs-lookup"><span data-stu-id="9f468-198">Name</span></span>                     | <span data-ttu-id="9f468-199">Описание</span><span class="sxs-lookup"><span data-stu-id="9f468-199">Description</span></span>                                                                                                      |
|--------------------------|------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f468-200">\_ \_ Мягкий режим границы \_ D2D1</span><span class="sxs-lookup"><span data-stu-id="9f468-200">D2D1\_BORDER\_MODE\_SOFT</span></span> | <span data-ttu-id="9f468-201">При интерполяции изображение получает прозрачные черные пиксели, что приводит к мягкому пограничным границе.</span><span class="sxs-lookup"><span data-stu-id="9f468-201">The effect pads the image with transparent black pixels as it interpolates, resulting in a soft edge.</span></span><br/> |
| <span data-ttu-id="9f468-202">Жесткое D2D1 в \_ \_ режиме границы \_</span><span class="sxs-lookup"><span data-stu-id="9f468-202">D2D1\_BORDER\_MODE\_HARD</span></span> | <span data-ttu-id="9f468-203">В результате выходные данные заменяются на размер входного изображения.</span><span class="sxs-lookup"><span data-stu-id="9f468-203">The effect clamps the output to the size of the input image.</span></span> <br/>                                         |



 

## <a name="output-bitmap"></a><span data-ttu-id="9f468-204">Битовая карта вывода</span><span class="sxs-lookup"><span data-stu-id="9f468-204">Output bitmap</span></span>

<span data-ttu-id="9f468-205">Размер выходного растрового изображения зависит от матрицы преобразования, применяемой к изображению.</span><span class="sxs-lookup"><span data-stu-id="9f468-205">The size of the output bitmap depends on the transform matrix that is applied to the image.</span></span>

<span data-ttu-id="9f468-206">Этот результат выполняет операцию преобразования, а затем применяет ограничивающий прямоугольник вокруг результата.</span><span class="sxs-lookup"><span data-stu-id="9f468-206">The effect performs the transform operation and then applies a bounding box around the result.</span></span> <span data-ttu-id="9f468-207">Битовая карта выходных данных — это размер ограничивающего прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="9f468-207">The output bitmap is the size of the bounding box.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f468-208">Требования</span><span class="sxs-lookup"><span data-stu-id="9f468-208">Requirements</span></span>



| <span data-ttu-id="9f468-209">Требование</span><span class="sxs-lookup"><span data-stu-id="9f468-209">Requirement</span></span> | <span data-ttu-id="9f468-210">Значение</span><span class="sxs-lookup"><span data-stu-id="9f468-210">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9f468-211">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9f468-211">Minimum supported client</span></span> | <span data-ttu-id="9f468-212">Windows 8 и обновление платформы для \[ классических приложений Windows 7 \| приложения для Магазина Windows\]</span><span class="sxs-lookup"><span data-stu-id="9f468-212">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="9f468-213">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9f468-213">Minimum supported server</span></span> | <span data-ttu-id="9f468-214">Windows 8 и обновление платформы для \[ классических приложений Windows 7 \| приложения для Магазина Windows\]</span><span class="sxs-lookup"><span data-stu-id="9f468-214">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="9f468-215">Header</span><span class="sxs-lookup"><span data-stu-id="9f468-215">Header</span></span>                   | <span data-ttu-id="9f468-216">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="9f468-216">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="9f468-217">Библиотека</span><span class="sxs-lookup"><span data-stu-id="9f468-217">Library</span></span>                  | <span data-ttu-id="9f468-218">D2D1. lib, дксгуид. lib</span><span class="sxs-lookup"><span data-stu-id="9f468-218">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="9f468-219">См. также</span><span class="sxs-lookup"><span data-stu-id="9f468-219">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9f468-220">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="9f468-220">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

