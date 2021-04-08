---
title: Составной результат
description: Используйте составной результат для объединения двух или более изображений. Этот результат имеет 13 различных составных режима.
ms.assetid: 60b878e9-1bc6-40d4-ade3-4bbd5c822c55
keywords:
- составной результат
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9872a66d031e8307f911ec7270af81397a80276
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988803"
---
# <a name="composite-effect"></a><span data-ttu-id="22259-105">Составной результат</span><span class="sxs-lookup"><span data-stu-id="22259-105">Composite effect</span></span>

<span data-ttu-id="22259-106">Используйте составной результат для объединения двух или более изображений.</span><span class="sxs-lookup"><span data-stu-id="22259-106">Use the composite effect to combine 2 or more images.</span></span> <span data-ttu-id="22259-107">Этот результат имеет 13 различных составных режима.</span><span class="sxs-lookup"><span data-stu-id="22259-107">This effect has 13 different composite modes.</span></span> <span data-ttu-id="22259-108">T</span><span class="sxs-lookup"><span data-stu-id="22259-108">T</span></span>

<span data-ttu-id="22259-109">Составной результат принимает 2 или более входных данных.</span><span class="sxs-lookup"><span data-stu-id="22259-109">The composite effect accepts 2 or more inputs.</span></span> <span data-ttu-id="22259-110">При указании двух изображений назначение является первым входом (индексом 0), а источником является второй вход (индекс 1).</span><span class="sxs-lookup"><span data-stu-id="22259-110">When you specify 2 images, destination is the first input (index 0) and the source is the second input (index 1).</span></span> <span data-ttu-id="22259-111">Если указать более двух входных данных, образы будут составными, начиная с первого входного, второго и т. д.</span><span class="sxs-lookup"><span data-stu-id="22259-111">If you specify more than 2 inputs the images are composited starting with the first input and the second and so on.</span></span>

<span data-ttu-id="22259-112">Этот результат реализует все режимы с использованием блока наложения графического процессора (GPU).</span><span class="sxs-lookup"><span data-stu-id="22259-112">This effect implements all of the modes using the blending unit of the graphics processing unit (GPU).</span></span>

<span data-ttu-id="22259-113">Идентификатором CLSID для этого действия является CLSID \_ D2D1Composite.</span><span class="sxs-lookup"><span data-stu-id="22259-113">The CLSID for this effect is CLSID\_D2D1Composite.</span></span>

-   [<span data-ttu-id="22259-114">Пример изображения</span><span class="sxs-lookup"><span data-stu-id="22259-114">Example image</span></span>](#example-image)
-   [<span data-ttu-id="22259-115">Свойства эффектов</span><span class="sxs-lookup"><span data-stu-id="22259-115">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="22259-116">Типы режимов</span><span class="sxs-lookup"><span data-stu-id="22259-116">Mode types</span></span>](#mode-types)
-   [<span data-ttu-id="22259-117">Образец кода</span><span class="sxs-lookup"><span data-stu-id="22259-117">Sample code</span></span>](#sample-code)
-   [<span data-ttu-id="22259-118">Требования</span><span class="sxs-lookup"><span data-stu-id="22259-118">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="22259-119">См. также</span><span class="sxs-lookup"><span data-stu-id="22259-119">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="22259-120">Пример изображения</span><span class="sxs-lookup"><span data-stu-id="22259-120">Example image</span></span>

<span data-ttu-id="22259-121">На рисунке изображены два скругленных прямоугольника того же размера, которые перекрываются.</span><span class="sxs-lookup"><span data-stu-id="22259-121">The image here shows 2 rounded rectangles of the same size that overlap.</span></span> <span data-ttu-id="22259-122">Синим прямоугольником является источник, а красный прямоугольник — место назначения.</span><span class="sxs-lookup"><span data-stu-id="22259-122">The blue rectangle is the source and the red rectangle is the destination.</span></span> <span data-ttu-id="22259-123">Изображения были совмещены с источником в режиме.</span><span class="sxs-lookup"><span data-stu-id="22259-123">The images were composited with the Source Over mode.</span></span>

![Пример изображения с двумя скругленными прямоугольниками того же размера, который пересекается с использованием источника в режиме.](images/composite-over.png)

<span data-ttu-id="22259-125">Ниже приведен другой пример использования режима по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="22259-125">Here's another example using the default mode.</span></span>



| <span data-ttu-id="22259-126">До образа 1</span><span class="sxs-lookup"><span data-stu-id="22259-126">Before image 1</span></span>                                                          |
|-------------------------------------------------------------------------|
| ![Первое исходное изображение перед результатом.](images/default-before.jpg) |
| <span data-ttu-id="22259-128">До изображения 2</span><span class="sxs-lookup"><span data-stu-id="22259-128">Before image 2</span></span>                                                          |
| ![Второе изображение перед результатом.](images/3-composite(2of2).png)    |
| <span data-ttu-id="22259-130">После</span><span class="sxs-lookup"><span data-stu-id="22259-130">After</span></span>                                                                   |
| ![изображение после преобразования.](images/3-composite.png)               |



 


```C++
ComPtr<ID2D1Effect> compositeEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Composite, &compositeEffect);

compositeEffect->SetInput(0, bitmap);
compositeEffect->SetInput(1, bitmapTwo);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(compositeEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a><span data-ttu-id="22259-132">Свойства эффектов</span><span class="sxs-lookup"><span data-stu-id="22259-132">Effect properties</span></span>



| <span data-ttu-id="22259-133">Отображаемое имя и перечисление индекса</span><span class="sxs-lookup"><span data-stu-id="22259-133">Display name and index enumeration</span></span>                     | <span data-ttu-id="22259-134">Тип и значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="22259-134">Type and default value</span></span>                                                          | <span data-ttu-id="22259-135">Описание</span><span class="sxs-lookup"><span data-stu-id="22259-135">Description</span></span>                   |
|--------------------------------------------------------|---------------------------------------------------------------------------------|-------------------------------|
| <span data-ttu-id="22259-136">Режим</span><span class="sxs-lookup"><span data-stu-id="22259-136">Mode</span></span><br/> <span data-ttu-id="22259-137">D2D1 \_ составной \_ \_ режим Prop</span><span class="sxs-lookup"><span data-stu-id="22259-137">D2D1\_COMPOSITE\_PROP\_MODE</span></span><br/> | <span data-ttu-id="22259-138">\_Составной \_ режим D2D1</span><span class="sxs-lookup"><span data-stu-id="22259-138">D2D1\_COMPOSITE\_MODE</span></span><br/> <span data-ttu-id="22259-139">\_Источник D2D1 составного \_ режима \_ \_</span><span class="sxs-lookup"><span data-stu-id="22259-139">D2D1\_COMPOSITE\_MODE\_SOURCE\_OVER</span></span><br/> | <span data-ttu-id="22259-140">Режим, используемый для этого результата.</span><span class="sxs-lookup"><span data-stu-id="22259-140">The mode used for the effect.</span></span> |



 

## <a name="mode-types"></a><span data-ttu-id="22259-141">Типы режимов</span><span class="sxs-lookup"><span data-stu-id="22259-141">Mode types</span></span>

<span data-ttu-id="22259-142">В таблице здесь показаны режимы этого результата.</span><span class="sxs-lookup"><span data-stu-id="22259-142">The table here shows the modes of this effect.</span></span> <span data-ttu-id="22259-143">В формулах, перечисленных в таблице, используются следующие элементы:</span><span class="sxs-lookup"><span data-stu-id="22259-143">The equations listed in the table use these elements:</span></span>

-   <span data-ttu-id="22259-144">O = выходные данные</span><span class="sxs-lookup"><span data-stu-id="22259-144">O = Output</span></span>
-   <span data-ttu-id="22259-145">S = источник</span><span class="sxs-lookup"><span data-stu-id="22259-145">S = Source</span></span>
-   <span data-ttu-id="22259-146">SA = источник альфа</span><span class="sxs-lookup"><span data-stu-id="22259-146">SA = Source Alpha</span></span>
-   <span data-ttu-id="22259-147">D = назначение</span><span class="sxs-lookup"><span data-stu-id="22259-147">D = Destination</span></span>
-   <span data-ttu-id="22259-148">DA = альфа-канал назначения</span><span class="sxs-lookup"><span data-stu-id="22259-148">DA = Destination Alpha</span></span>



| <span data-ttu-id="22259-149">Перечисление</span><span class="sxs-lookup"><span data-stu-id="22259-149">Enumeration</span></span>                                  | <span data-ttu-id="22259-150">Дробь</span><span class="sxs-lookup"><span data-stu-id="22259-150">Equation</span></span>                          | <span data-ttu-id="22259-151">Размер выходного растрового изображения</span><span class="sxs-lookup"><span data-stu-id="22259-151">Output Bitmap Size</span></span>                                                                                      |
|----------------------------------------------|-----------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="22259-152">\_Источник D2D1 составного \_ режима \_ \_</span><span class="sxs-lookup"><span data-stu-id="22259-152">D2D1\_COMPOSITE\_MODE\_SOURCE\_OVER</span></span>          | <span data-ttu-id="22259-153">O = S + (1 SA) \* D</span><span class="sxs-lookup"><span data-stu-id="22259-153">O = S + (1   SA) \* D</span></span>             | <span data-ttu-id="22259-154">Объединение исходного и конечного точечных рисунков</span><span class="sxs-lookup"><span data-stu-id="22259-154">Union of source and destination bitmaps</span></span>                                                                 |
| <span data-ttu-id="22259-155">\_ \_ \_ Назначение для СОСТАВного режима D2D1 \_</span><span class="sxs-lookup"><span data-stu-id="22259-155">D2D1\_COMPOSITE\_MODE\_DESTINATION\_OVER</span></span>     | <span data-ttu-id="22259-156">O = (1 DA) \* S + D</span><span class="sxs-lookup"><span data-stu-id="22259-156">O = (1   DA) \* S + D</span></span>             | <span data-ttu-id="22259-157">Объединение исходного и конечного точечных рисунков</span><span class="sxs-lookup"><span data-stu-id="22259-157">Union of source and destination bitmaps</span></span>                                                                 |
| <span data-ttu-id="22259-158">\_Источник составного \_ режима D2D1 \_ \_ в</span><span class="sxs-lookup"><span data-stu-id="22259-158">D2D1\_COMPOSITE\_MODE\_SOURCE\_IN</span></span>            | <span data-ttu-id="22259-159">O = DA \* S</span><span class="sxs-lookup"><span data-stu-id="22259-159">O = DA \* S</span></span>                       | <span data-ttu-id="22259-160">Пересечение исходного и конечного точечных рисунков</span><span class="sxs-lookup"><span data-stu-id="22259-160">Intersection of source and destination bitmaps</span></span>                                                          |
| <span data-ttu-id="22259-161">\_Назначение составного \_ режима D2D1 \_ \_ в</span><span class="sxs-lookup"><span data-stu-id="22259-161">D2D1\_COMPOSITE\_MODE\_DESTINATION\_IN</span></span>       | <span data-ttu-id="22259-162">O = SA \* D</span><span class="sxs-lookup"><span data-stu-id="22259-162">O = SA \* D</span></span>                       | <span data-ttu-id="22259-163">Пересечение исходного и конечного точечных рисунков</span><span class="sxs-lookup"><span data-stu-id="22259-163">Intersection of source and destination bitmaps</span></span>                                                          |
| <span data-ttu-id="22259-164">\_Источник составного \_ режима D2D1 \_ \_</span><span class="sxs-lookup"><span data-stu-id="22259-164">D2D1\_COMPOSITE\_MODE\_SOURCE\_OUT</span></span>           | <span data-ttu-id="22259-165">O = (1-DA) \* S</span><span class="sxs-lookup"><span data-stu-id="22259-165">O = (1 - DA) \* S</span></span>                 | <span data-ttu-id="22259-166">Регион исходного точечного рисунка</span><span class="sxs-lookup"><span data-stu-id="22259-166">Region of the source bitmap</span></span>                                                                             |
| <span data-ttu-id="22259-167">\_Назначение для составного \_ режима \_ \_ D2D1</span><span class="sxs-lookup"><span data-stu-id="22259-167">D2D1\_COMPOSITE\_MODE\_DESTINATION\_OUT</span></span>      | <span data-ttu-id="22259-168">O = (1-SA) \* D</span><span class="sxs-lookup"><span data-stu-id="22259-168">O = (1 - SA) \* D</span></span>                 | <span data-ttu-id="22259-169">Регион точечного рисунка назначения</span><span class="sxs-lookup"><span data-stu-id="22259-169">Region of the destination bitmap</span></span>                                                                        |
| <span data-ttu-id="22259-170">\_Источник D2D1 составного \_ режима \_ \_</span><span class="sxs-lookup"><span data-stu-id="22259-170">D2D1\_COMPOSITE\_MODE\_SOURCE\_ATOP</span></span>          | <span data-ttu-id="22259-171">O = DA \* S + (1-SA) \* D</span><span class="sxs-lookup"><span data-stu-id="22259-171">O = DA \* S + (1 - SA) \* D</span></span>       | <span data-ttu-id="22259-172">Регион точечного рисунка назначения</span><span class="sxs-lookup"><span data-stu-id="22259-172">Region of the destination bitmap</span></span>                                                                        |
| <span data-ttu-id="22259-173">D2D1 \_ для \_ назначения составного режима \_ \_</span><span class="sxs-lookup"><span data-stu-id="22259-173">D2D1\_COMPOSITE\_MODE\_DESTINATION\_ATOP</span></span>     | <span data-ttu-id="22259-174">O = (1-DA) \* S + SA \* D</span><span class="sxs-lookup"><span data-stu-id="22259-174">O = (1 - DA) \* S + SA \* D</span></span>       | <span data-ttu-id="22259-175">Регион исходного точечного рисунка</span><span class="sxs-lookup"><span data-stu-id="22259-175">Region of the source bitmap</span></span>                                                                             |
| <span data-ttu-id="22259-176">D2D1 \_ составной \_ режим \_ XOR</span><span class="sxs-lookup"><span data-stu-id="22259-176">D2D1\_COMPOSITE\_MODE\_XOR</span></span>                   | <span data-ttu-id="22259-177">O = (1-DA) \* S + (1-SA) \* D</span><span class="sxs-lookup"><span data-stu-id="22259-177">O = (1 - DA) \* S + (1 - SA) \* D</span></span> | <span data-ttu-id="22259-178">Объединение исходного и конечного точечных рисунков</span><span class="sxs-lookup"><span data-stu-id="22259-178">Union of source and destination bitmaps</span></span>                                                                 |
| <span data-ttu-id="22259-179">D2D1 \_ составной \_ режим \_ и</span><span class="sxs-lookup"><span data-stu-id="22259-179">D2D1\_COMPOSITE\_MODE\_PLUS</span></span>                  | <span data-ttu-id="22259-180">O = S + D</span><span class="sxs-lookup"><span data-stu-id="22259-180">O = S + D</span></span>                         | <span data-ttu-id="22259-181">Объединение исходного и конечного точечных рисунков</span><span class="sxs-lookup"><span data-stu-id="22259-181">Union of source and destination bitmaps</span></span>                                                                 |
| <span data-ttu-id="22259-182">\_ \_ \_ Копия источника СОСТАВного режима D2D1 \_</span><span class="sxs-lookup"><span data-stu-id="22259-182">D2D1\_COMPOSITE\_MODE\_SOURCE\_COPY</span></span>          | <span data-ttu-id="22259-183">O = S</span><span class="sxs-lookup"><span data-stu-id="22259-183">O = S</span></span>                             | <span data-ttu-id="22259-184">Регион исходного точечного рисунка</span><span class="sxs-lookup"><span data-stu-id="22259-184">Region of the source bitmap</span></span>                                                                             |
| <span data-ttu-id="22259-185">\_ \_ \_ Копия с ОГРАНИЧЕНным \_ источником \_ D2D1 в составном режиме</span><span class="sxs-lookup"><span data-stu-id="22259-185">D2D1\_COMPOSITE\_MODE\_BOUNDED\_SOURCE\_COPY</span></span> | <span data-ttu-id="22259-186">O = S (только в том месте, где существует источник)</span><span class="sxs-lookup"><span data-stu-id="22259-186">O = S (only where source exists)</span></span>  | <span data-ttu-id="22259-187">Объединение исходного и целевого точечных рисунков.</span><span class="sxs-lookup"><span data-stu-id="22259-187">Union of source and destination bitmaps.</span></span> <span data-ttu-id="22259-188">Назначение не перезаписывается, если источник не существует.</span><span class="sxs-lookup"><span data-stu-id="22259-188">Destination is not overwritten where the source doesn't exist.</span></span> |
| <span data-ttu-id="22259-189">\_Инверсия D2D1 в составном \_ режиме \_ \_</span><span class="sxs-lookup"><span data-stu-id="22259-189">D2D1\_COMPOSITE\_MODE\_MASK\_INVERT</span></span>          | <span data-ttu-id="22259-190">O = (1 D) \* S + (1 SA) \* D</span><span class="sxs-lookup"><span data-stu-id="22259-190">O = (1   D) \* S + (1   SA) \* D</span></span>  | <span data-ttu-id="22259-191">Объединение исходного и целевого точечных рисунков. Альфа-значения не меняются.</span><span class="sxs-lookup"><span data-stu-id="22259-191">Union of source and destination bitmaps.The alpha values are unchanged.</span></span>                                 |



 

<span data-ttu-id="22259-192">На рисунке ниже показан пример каждого режима с изображениями со степенью непрозрачности 1,0 или 0,5.</span><span class="sxs-lookup"><span data-stu-id="22259-192">The figure here shows an example of each of the modes with images that have an opacity of 1.0 or 0.5.</span></span>

![Пример изображения для каждого из режимов с непрозрачностью, равным 1,0 или 0,5.](images/composite-types.png)

## <a name="sample-code"></a><span data-ttu-id="22259-194">Пример кода</span><span class="sxs-lookup"><span data-stu-id="22259-194">Sample code</span></span>

<span data-ttu-id="22259-195">Чтобы получить пример этого результата, скачайте [образец Direct2D составных эффектов](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct2D%20composite%20effect%20modes%20sample).</span><span class="sxs-lookup"><span data-stu-id="22259-195">For an example of this effect, download the [Direct2D composite effect modes sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct2D%20composite%20effect%20modes%20sample).</span></span>

## <a name="requirements"></a><span data-ttu-id="22259-196">Требования</span><span class="sxs-lookup"><span data-stu-id="22259-196">Requirements</span></span>



| <span data-ttu-id="22259-197">Требование</span><span class="sxs-lookup"><span data-stu-id="22259-197">Requirement</span></span> | <span data-ttu-id="22259-198">Значение</span><span class="sxs-lookup"><span data-stu-id="22259-198">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="22259-199">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="22259-199">Minimum supported client</span></span> | <span data-ttu-id="22259-200">Windows 8 и обновление платформы для \[ классических приложений Windows 7 \| приложения для Магазина Windows\]</span><span class="sxs-lookup"><span data-stu-id="22259-200">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="22259-201">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="22259-201">Minimum supported server</span></span> | <span data-ttu-id="22259-202">Windows 8 и обновление платформы для \[ классических приложений Windows 7 \| приложения для Магазина Windows\]</span><span class="sxs-lookup"><span data-stu-id="22259-202">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="22259-203">Header</span><span class="sxs-lookup"><span data-stu-id="22259-203">Header</span></span>                   | <span data-ttu-id="22259-204">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="22259-204">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="22259-205">Библиотека</span><span class="sxs-lookup"><span data-stu-id="22259-205">Library</span></span>                  | <span data-ttu-id="22259-206">D2D1. lib, дксгуид. lib</span><span class="sxs-lookup"><span data-stu-id="22259-206">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="22259-207">См. также</span><span class="sxs-lookup"><span data-stu-id="22259-207">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="22259-208">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="22259-208">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

