---
title: Арифметический составной эффекты
description: Используйте арифметический составной результат для объединения двух изображений с взвешенной суммой пикселей из входных изображений.
ms.assetid: 6EC8CD61-5B51-4A8E-8A61-B291ABB5C5E0
keywords:
- Арифметический составной эффекты
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04c235ecb024c6b9e7adbce31c9f0cd65bc36cdf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989125"
---
# <a name="arithmetic-composite-effect"></a><span data-ttu-id="42703-104">Арифметический составной эффекты</span><span class="sxs-lookup"><span data-stu-id="42703-104">Arithmetic composite effect</span></span>

<span data-ttu-id="42703-105">Используйте арифметический составной результат для объединения двух изображений с взвешенной суммой пикселей из входных изображений.</span><span class="sxs-lookup"><span data-stu-id="42703-105">Use the arithmetic composite effect to combine 2 images using a weighted sum of pixels from the input images.</span></span>

<span data-ttu-id="42703-106">Идентификатором CLSID для этого действия является CLSID \_ D2D1ArithmeticComposite.</span><span class="sxs-lookup"><span data-stu-id="42703-106">The CLSID for this effect is CLSID\_D2D1ArithmeticComposite.</span></span>

-   [<span data-ttu-id="42703-107">Формула</span><span class="sxs-lookup"><span data-stu-id="42703-107">Formula</span></span>](#formula)
-   [<span data-ttu-id="42703-108">Пример изображения</span><span class="sxs-lookup"><span data-stu-id="42703-108">Example image</span></span>](#example-image)
-   [<span data-ttu-id="42703-109">Свойства эффектов</span><span class="sxs-lookup"><span data-stu-id="42703-109">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="42703-110">Битовая карта вывода</span><span class="sxs-lookup"><span data-stu-id="42703-110">Output bitmap</span></span>](#output-bitmap)
-   [<span data-ttu-id="42703-111">Требования</span><span class="sxs-lookup"><span data-stu-id="42703-111">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="42703-112">См. также</span><span class="sxs-lookup"><span data-stu-id="42703-112">Related topics</span></span>](#related-topics)

## <a name="formula"></a><span data-ttu-id="42703-113">Формула</span><span class="sxs-lookup"><span data-stu-id="42703-113">Formula</span></span>

<span data-ttu-id="42703-114">Формула здесь используется для вычисления этого результата.</span><span class="sxs-lookup"><span data-stu-id="42703-114">The formula here is used to compute this effect.</span></span>

<span data-ttu-id="42703-115">Выходное<sub>RGBA</sub> = \* исходное<sub></sub> \* место назначения<sub></sub> RGBA, целевые RGBA + C2 \* исходное<sub>RGBA</sub> + \* C4<sub></sub></span><span class="sxs-lookup"><span data-stu-id="42703-115">Output<sub>rgba</sub> = C1 \* Source<sub>rgba</sub> \* Destination<sub>rgba</sub> + C2 \* Source<sub>rgba</sub> + C3 \* Destination<sub>rgba</sub> + C4</span></span>

<span data-ttu-id="42703-116">Где C1, C2, C3 и C4 — это коэффициенты, которые вы задаете.</span><span class="sxs-lookup"><span data-stu-id="42703-116">Where C1, C2, C3, C4 are coefficients that you set.</span></span>

<span data-ttu-id="42703-117">Коэффициенты сопоставляются со значениями в D2D1 \_ векторной \_ 4F (x, y, z, w):</span><span class="sxs-lookup"><span data-stu-id="42703-117">The coefficients map to the values in a D2D1\_VECTOR\_4F (x, y, z, w):</span></span>

-   <span data-ttu-id="42703-118">x = C1</span><span class="sxs-lookup"><span data-stu-id="42703-118">x = C1</span></span>
-   <span data-ttu-id="42703-119">y = C2</span><span class="sxs-lookup"><span data-stu-id="42703-119">y = C2</span></span>
-   <span data-ttu-id="42703-120">z = C3</span><span class="sxs-lookup"><span data-stu-id="42703-120">z = C3</span></span>
-   <span data-ttu-id="42703-121">w = C4</span><span class="sxs-lookup"><span data-stu-id="42703-121">w = C4</span></span>

## <a name="example-image"></a><span data-ttu-id="42703-122">Пример изображения</span><span class="sxs-lookup"><span data-stu-id="42703-122">Example image</span></span>

<span data-ttu-id="42703-123">Простой пример — добавить исходный и целевой Пиксели.</span><span class="sxs-lookup"><span data-stu-id="42703-123">A simple example is to add the source and destination pixels.</span></span> <span data-ttu-id="42703-124">В этом примере два прямоугольника с закругленными углами совмещены вместе.</span><span class="sxs-lookup"><span data-stu-id="42703-124">In the example, 2 rounded rectangles are composited together.</span></span> <span data-ttu-id="42703-125">Исходный прямоугольник является синим, а назначение — красным.</span><span class="sxs-lookup"><span data-stu-id="42703-125">The source rectangle is blue and the destination is red.</span></span>

<span data-ttu-id="42703-126">Изображение здесь является выходным результатом арифметического составного воздействия с коэффициентами уравнения, установленными в значения.</span><span class="sxs-lookup"><span data-stu-id="42703-126">The image here is the output of the Arithmetic Composite effect with the coefficients of the equation set to the values here.</span></span>

-   <span data-ttu-id="42703-127">C1 = 0</span><span class="sxs-lookup"><span data-stu-id="42703-127">C1 = 0</span></span>
-   <span data-ttu-id="42703-128">C2 = 1</span><span class="sxs-lookup"><span data-stu-id="42703-128">C2 = 1</span></span>
-   <span data-ttu-id="42703-129">C3 = 1</span><span class="sxs-lookup"><span data-stu-id="42703-129">C3 = 1</span></span>
-   <span data-ttu-id="42703-130">C4 = 0</span><span class="sxs-lookup"><span data-stu-id="42703-130">C4 = 0</span></span>

![Пример изображения с двумя скругленными прямоугольниками такого же размера, которые перекрываются с помощью арифметического составного действия.](images/arithmetic-50-percent.png)

<span data-ttu-id="42703-132">В результате добавляются значения пикселей для источника и назначения.</span><span class="sxs-lookup"><span data-stu-id="42703-132">The result is that the pixel values for the source and destination are added.</span></span> <span data-ttu-id="42703-133">Регионы, в которых прямоугольники не пересекаются со значениями RGBA, равны 0.</span><span class="sxs-lookup"><span data-stu-id="42703-133">The regions where the rectangles don't overlap the RGBA values are all 0.</span></span> <span data-ttu-id="42703-134">Когда прямоугольники перекрываются, цвет является пурпурным, так как значения R и B равны максимуму.</span><span class="sxs-lookup"><span data-stu-id="42703-134">Where the rectangles overlap the color is magenta because the R and B values are both at maximum.</span></span>

<span data-ttu-id="42703-135">Вот еще один пример изображения с кодом.</span><span class="sxs-lookup"><span data-stu-id="42703-135">Here's another example image with code.</span></span>



| <span data-ttu-id="42703-136">До образа 1</span><span class="sxs-lookup"><span data-stu-id="42703-136">Before image 1</span></span>                                                             |
|----------------------------------------------------------------------------|
| ![Первое исходное изображение перед результатом.](images/default-before.jpg)    |
| <span data-ttu-id="42703-138">До изображения 2</span><span class="sxs-lookup"><span data-stu-id="42703-138">Before image 2</span></span>                                                             |
| ![Второе изображение перед результатом.](images/4-arthimetic-composite2.jpg) |
| <span data-ttu-id="42703-140">После</span><span class="sxs-lookup"><span data-stu-id="42703-140">After</span></span>                                                                      |
| ![изображение после преобразования.](images/4-arithmeticcomposite.png)        |



 


```C++
ComPtr<ID2D1Effect> arithmeticCompositeEffect;
m_d2dContext->CreateEffect(CLSID_D2D1ArithmeticComposite, &arithmeticCompositeEffect);

arithmeticCompositeEffect->SetInput(0, bitmap);
arithmeticCompositeEffect->SetInput(1, bitmapTwo);
arithmeticCompositeEffect->SetValue(D2D1_ARITHMETICCOMPOSITE_PROP_COEFFICIENTS, D2D1::Vector4F(0.0f, 0.5f, 0.5f, 0.0f));

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(arithmeticCompositeEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a><span data-ttu-id="42703-142">Свойства эффектов</span><span class="sxs-lookup"><span data-stu-id="42703-142">Effect properties</span></span>



| <span data-ttu-id="42703-143">Отображаемое имя и перечисление индекса</span><span class="sxs-lookup"><span data-stu-id="42703-143">Display name and index enumeration</span></span>                                               | <span data-ttu-id="42703-144">Описание</span><span class="sxs-lookup"><span data-stu-id="42703-144">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42703-145">Коэффициенты</span><span class="sxs-lookup"><span data-stu-id="42703-145">Coefficients</span></span><br/> <span data-ttu-id="42703-146">\_ \_ Коэффициенты Prop арисметиккомпосите D2D1 \_</span><span class="sxs-lookup"><span data-stu-id="42703-146">D2D1\_ARITHMETICCOMPOSITE\_PROP\_COEFFICIENTS</span></span><br/> | <span data-ttu-id="42703-147">Коэффициенты для формулы, используемой для совмещения двух входных изображений.</span><span class="sxs-lookup"><span data-stu-id="42703-147">The coefficients for the equation used to composite the two input images.</span></span> <span data-ttu-id="42703-148">Коэффициенты — бесмодульный и неограниченный.</span><span class="sxs-lookup"><span data-stu-id="42703-148">The coefficients are unitless and unbounded.</span></span> <span data-ttu-id="42703-149">Тип — D2D1 \_ vector \_ 4F.</span><span class="sxs-lookup"><span data-stu-id="42703-149">Type is D2D1\_VECTOR\_4F.</span></span><br/> <span data-ttu-id="42703-150">Значение по умолчанию — {1.0 f, 0,0 f, 0,0 f, 0,0 f}.</span><span class="sxs-lookup"><span data-stu-id="42703-150">Default value is {1.0f, 0.0f, 0.0f, 0.0f}.</span></span><br/>                                                                                                                                                                                                                                 |
| <span data-ttu-id="42703-151">клампаутпут</span><span class="sxs-lookup"><span data-stu-id="42703-151">ClampOutput</span></span><br/> <span data-ttu-id="42703-152">\_ \_ \_ Выходные данные среза D2D1 арисметиккомпосите \_</span><span class="sxs-lookup"><span data-stu-id="42703-152">D2D1\_ARITHMETICCOMPOSITE\_PROP\_CLAMP\_OUTPUT</span></span><br/> | <span data-ttu-id="42703-153">В результате значения цвета заменяются значениями от 0 до 1, прежде чем результат передаст значения следующему результату в графе.</span><span class="sxs-lookup"><span data-stu-id="42703-153">The effect clamps color values to between 0 and 1 before the effect passes the values to the next effect in the graph.</span></span> <br/> <span data-ttu-id="42703-154">Если присвоить этому параметру значение TRUE, то действие будет выполнять фиксацию значений.</span><span class="sxs-lookup"><span data-stu-id="42703-154">If you set this to TRUE the effect will clamp the values.</span></span> <span data-ttu-id="42703-155">Если присвоить этому параметру значение FALSE, то эффект не будет выполнять фиксацию цветовых значений, но другие эффекты и поверхность вывода могут попытаться отразить значения, если они не имеют достаточно высокой точности.</span><span class="sxs-lookup"><span data-stu-id="42703-155">If you set this to FALSE, the effect will not clamp the color values, but other effects and the output surface may clamp the values if they are not of high enough precision.</span></span><br/> <span data-ttu-id="42703-156">Тип — BOOL.</span><span class="sxs-lookup"><span data-stu-id="42703-156">Type is BOOL.</span></span><br/> <span data-ttu-id="42703-157">Значение по умолчанию — FALSE.</span><span class="sxs-lookup"><span data-stu-id="42703-157">Default value is FALSE.</span></span><br/> |



 

## <a name="output-bitmap"></a><span data-ttu-id="42703-158">Битовая карта вывода</span><span class="sxs-lookup"><span data-stu-id="42703-158">Output bitmap</span></span>

<span data-ttu-id="42703-159">Выходное растровое изображение зависит от значений коэффициента.</span><span class="sxs-lookup"><span data-stu-id="42703-159">The output bitmap depends on the coefficient values.</span></span> <span data-ttu-id="42703-160">Это возможные размеры выходного растрового изображения.</span><span class="sxs-lookup"><span data-stu-id="42703-160">These are the possible output bitmap sizes.</span></span>

-   <span data-ttu-id="42703-161">Если C1 является единственным ненулевым коэффициентом, то размер выходных данных является пересечением прямоугольников ввода.</span><span class="sxs-lookup"><span data-stu-id="42703-161">If C1 is the only non-zero coefficient, the output size is the intersection of the input rectangles.</span></span>
-   <span data-ttu-id="42703-162">Если значение C2 является единственным ненулевым коэффициентом, то размер выходных данных равен размеру исходного прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="42703-162">If C2 is the only non-zero coefficient, the output size is the size of the Source rectangle.</span></span>
-   <span data-ttu-id="42703-163">Если значение C3 является единственным ненулевым коэффициентом, то размер выходных данных равен размеру прямоугольника назначения.</span><span class="sxs-lookup"><span data-stu-id="42703-163">If C3 is the only non-zero coefficient, the output size is the size of the Destination rectangle..</span></span>
-   <span data-ttu-id="42703-164">Если все коэффициенты равны нулю, то размер выходных данных будет пустым прямоугольником.</span><span class="sxs-lookup"><span data-stu-id="42703-164">If all coefficients are zero, the output size is an empty rectangle.</span></span>
-   <span data-ttu-id="42703-165">Для всех остальных значений коэффициента выходным размером является объединение прямоугольников ввода.</span><span class="sxs-lookup"><span data-stu-id="42703-165">For all other coefficient values, the output size is the union of the input rectangles.</span></span>

## <a name="requirements"></a><span data-ttu-id="42703-166">Требования</span><span class="sxs-lookup"><span data-stu-id="42703-166">Requirements</span></span>



| <span data-ttu-id="42703-167">Требование</span><span class="sxs-lookup"><span data-stu-id="42703-167">Requirement</span></span> | <span data-ttu-id="42703-168">Значение</span><span class="sxs-lookup"><span data-stu-id="42703-168">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="42703-169">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="42703-169">Minimum supported client</span></span> | <span data-ttu-id="42703-170">Windows 8 и обновление платформы для \[ классических приложений Windows 7 \| приложения для Магазина Windows\]</span><span class="sxs-lookup"><span data-stu-id="42703-170">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="42703-171">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="42703-171">Minimum supported server</span></span> | <span data-ttu-id="42703-172">Windows 8 и обновление платформы для \[ классических приложений Windows 7 \| приложения для Магазина Windows\]</span><span class="sxs-lookup"><span data-stu-id="42703-172">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="42703-173">Header</span><span class="sxs-lookup"><span data-stu-id="42703-173">Header</span></span>                   | <span data-ttu-id="42703-174">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="42703-174">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="42703-175">Библиотека</span><span class="sxs-lookup"><span data-stu-id="42703-175">Library</span></span>                  | <span data-ttu-id="42703-176">D2D1. lib, дксгуид. lib</span><span class="sxs-lookup"><span data-stu-id="42703-176">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="42703-177">См. также</span><span class="sxs-lookup"><span data-stu-id="42703-177">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="42703-178">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="42703-178">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

