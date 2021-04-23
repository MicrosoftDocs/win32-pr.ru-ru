---
description: Формат текстуры DXT1 предназначен для текстур, которые являются непрозрачными или имеют один прозрачный цвет.
ms.assetid: a890ed0a-1f68-45b8-93cb-b621d1908d9f
title: Непрозрачные и 1-разрядные текстуры Alpha (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f629eff594d28d9a807021c0b9df0bd05ea66c3
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/04/2021
ms.locfileid: "104555804"
---
# <a name="opaque-and-1-bit-alpha-textures-direct3d-9"></a><span data-ttu-id="17b16-103">Непрозрачные и 1-разрядные текстуры Alpha (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="17b16-103">Opaque and 1-Bit Alpha Textures (Direct3D 9)</span></span>

<span data-ttu-id="17b16-104">Формат текстуры DXT1 предназначен для текстур, которые являются непрозрачными или имеют один прозрачный цвет.</span><span class="sxs-lookup"><span data-stu-id="17b16-104">Texture format DXT1 is for textures that are opaque or have a single transparent color.</span></span>

<span data-ttu-id="17b16-105">Для каждого непрозрачного или 1-разрядного альфа-блока сохраняются два 16-разрядных значения (формат RGB 5:6:5) и битовая карта 4 x 4 с 2 битами на пиксель.</span><span class="sxs-lookup"><span data-stu-id="17b16-105">For each opaque or 1-bit alpha block, two 16-bit values (RGB 5:6:5 format) and a 4x4 bitmap with 2 bits per pixel are stored.</span></span> <span data-ttu-id="17b16-106">Это в сумме составляет 64 бита для 16 текселей или четыре бита на тексель.</span><span class="sxs-lookup"><span data-stu-id="17b16-106">This totals 64 bits for 16 texels, or four bits per texel.</span></span> <span data-ttu-id="17b16-107">В битовой карте блока предусматриваются 2 бита на тексель для выбора из четырех цветов, два из которых хранятся в закодированных данных.</span><span class="sxs-lookup"><span data-stu-id="17b16-107">In the block bitmap, there are 2 bits per texel to select between the four colors, two of which are stored in the encoded data.</span></span> <span data-ttu-id="17b16-108">Другие два цвета являются производными от эти сохраненных цветов путем линейной интерполяции.</span><span class="sxs-lookup"><span data-stu-id="17b16-108">The other two colors are derived from these stored colors by linear interpolation.</span></span> <span data-ttu-id="17b16-109">Этом макет показан на следующей схеме.</span><span class="sxs-lookup"><span data-stu-id="17b16-109">This layout is shown in the following diagram.</span></span>

![схема битовой карты](images/colors1.png)

<span data-ttu-id="17b16-111">Формат 1-разрядного альфа-значения может быть отличен от формата непрозрачного цвета путем сравнения двух 16-разрядных значений цвета, сохраненных в блоке.</span><span class="sxs-lookup"><span data-stu-id="17b16-111">The 1-bit alpha format is distinguished from the opaque format by comparing the two 16-bit color values stored in the block.</span></span> <span data-ttu-id="17b16-112">Они обрабатываются как целые числа без знака.</span><span class="sxs-lookup"><span data-stu-id="17b16-112">They are treated as unsigned integers.</span></span> <span data-ttu-id="17b16-113">Если первый цвет больше, чем второй, подразумевается, что определены только непрозрачные тексели.</span><span class="sxs-lookup"><span data-stu-id="17b16-113">If the first color is greater than the second, it implies that only opaque texels are defined.</span></span> <span data-ttu-id="17b16-114">Это означает, что для представления текселей используются четыре цвета.</span><span class="sxs-lookup"><span data-stu-id="17b16-114">This means four colors are used to represent the texels.</span></span> <span data-ttu-id="17b16-115">В четырехцветном кодировании существует два производных цвета, а все четыре цвета распределяются равномерно в цветовом пространстве RGB.</span><span class="sxs-lookup"><span data-stu-id="17b16-115">In four-color encoding, there are two derived colors and all four colors are equally distributed in RGB color space.</span></span> <span data-ttu-id="17b16-116">Этот формат аналогичен формату RGB 5:6:5.</span><span class="sxs-lookup"><span data-stu-id="17b16-116">This format is analogous to RGB 5:6:5 format.</span></span> <span data-ttu-id="17b16-117">В противном случае для 1-разрядной альфа-прозрачности используются три цвета, а четвертый резервируется для представления прозрачных текселей.</span><span class="sxs-lookup"><span data-stu-id="17b16-117">Otherwise, for 1-bit alpha transparency, three colors are used and the fourth is reserved to represent transparent texels.</span></span>

<span data-ttu-id="17b16-118">В кодировке тремя цветами существует один производный цвет, а четвертый 2-разрядный код резервируется для указания прозрачного текселя (данные альфа-канала).</span><span class="sxs-lookup"><span data-stu-id="17b16-118">In three-color encoding, there is one derived color and the fourth 2-bit code is reserved to indicate a transparent texel (alpha information).</span></span> <span data-ttu-id="17b16-119">Этот формат аналогичен RGBA 5:5:5:1, где заключительный разряд используется для кодирования альфа-маски.</span><span class="sxs-lookup"><span data-stu-id="17b16-119">This format is analogous to RGBA 5:5:5:1, where the final bit is used for encoding the alpha mask.</span></span>

<span data-ttu-id="17b16-120">В следующем примере кода показан алгоритм определения того, выбрано ли трех- или четырехцветовое кодирование.</span><span class="sxs-lookup"><span data-stu-id="17b16-120">The following code example illustrates the algorithm for deciding whether three- or four-color encoding is selected:</span></span>


```
if (color_0 > color_1) 
{
    // Four-color block: derive the other two colors.    
    // 00 = color_0, 01 = color_1, 10 = color_2, 11 = color_3
    // These 2-bit codes correspond to the 2-bit fields 
    // stored in the 64-bit block.
    color_2 = (2 * color_0 + color_1 + 1) / 3;
    color_3 = (color_0 + 2 * color_1 + 1) / 3;
}    
else
{ 
    // Three-color block: derive the other color.
    // 00 = color_0,  01 = color_1,  10 = color_2,  
    // 11 = transparent.
    // These 2-bit codes correspond to the 2-bit fields 
    // stored in the 64-bit block. 
    color_2 = (color_0 + color_1) / 2;    
    color_3 = transparent;    

}
```



<span data-ttu-id="17b16-121">Перед наложением рекомендуется установить компоненты RGBA для пикселя прозрачности равными нулю.</span><span class="sxs-lookup"><span data-stu-id="17b16-121">It is recommended that you set the RGBA components of the transparency pixel to zero before blending.</span></span>

<span data-ttu-id="17b16-122">В следующих таблицах показана схема памяти для 8-байтового блока.</span><span class="sxs-lookup"><span data-stu-id="17b16-122">The following tables show the memory layout for the 8-byte block.</span></span> <span data-ttu-id="17b16-123">Предполагается, что первый индекс соответствует координате по оси Y, а второй соответствует координате по оси X.</span><span class="sxs-lookup"><span data-stu-id="17b16-123">It is assumed that the first index corresponds to the y-coordinate and the second corresponds to the x-coordinate.</span></span> <span data-ttu-id="17b16-124">Например, шаг текселя \[ 1 \] \[ 2 \] ссылается на пиксель текстуры на карте (x, y) = (2, 1).</span><span class="sxs-lookup"><span data-stu-id="17b16-124">For example, Texel\[1\]\[2\] refers to the texture map pixel at (x,y) = (2,1).</span></span>

<span data-ttu-id="17b16-125">Эта таблица содержит макет памяти для 8-байтового (64-разрядного) блока.</span><span class="sxs-lookup"><span data-stu-id="17b16-125">This table contains the memory layout for the 8-byte (64-bit) block.</span></span>



| <span data-ttu-id="17b16-126">Адрес слова</span><span class="sxs-lookup"><span data-stu-id="17b16-126">Word address</span></span> | <span data-ttu-id="17b16-127">16-разрядное слово</span><span class="sxs-lookup"><span data-stu-id="17b16-127">16-bit word</span></span>    |
|--------------|----------------|
| <span data-ttu-id="17b16-128">0</span><span class="sxs-lookup"><span data-stu-id="17b16-128">0</span></span>            | <span data-ttu-id="17b16-129">Цвет \_ 0</span><span class="sxs-lookup"><span data-stu-id="17b16-129">Color\_0</span></span>       |
| <span data-ttu-id="17b16-130">1</span><span class="sxs-lookup"><span data-stu-id="17b16-130">1</span></span>            | <span data-ttu-id="17b16-131">Цвет \_ 1</span><span class="sxs-lookup"><span data-stu-id="17b16-131">Color\_1</span></span>       |
| <span data-ttu-id="17b16-132">2</span><span class="sxs-lookup"><span data-stu-id="17b16-132">2</span></span>            | <span data-ttu-id="17b16-133">Битовое слово \_ 0</span><span class="sxs-lookup"><span data-stu-id="17b16-133">Bitmap Word\_0</span></span> |
| <span data-ttu-id="17b16-134">3</span><span class="sxs-lookup"><span data-stu-id="17b16-134">3</span></span>            | <span data-ttu-id="17b16-135">Битовое слово \_ 1</span><span class="sxs-lookup"><span data-stu-id="17b16-135">Bitmap Word\_1</span></span> |



 

<span data-ttu-id="17b16-136">Цвет \_ 0 и цвет \_ 1, цвета с двумя крайними, размещаются следующим образом:</span><span class="sxs-lookup"><span data-stu-id="17b16-136">Color\_0 and Color\_1, the colors at the two extremes, are laid out as follows:</span></span>



| <span data-ttu-id="17b16-137">Bits</span><span class="sxs-lookup"><span data-stu-id="17b16-137">Bits</span></span>        | <span data-ttu-id="17b16-138">Цвет</span><span class="sxs-lookup"><span data-stu-id="17b16-138">Color</span></span>                 |
|-------------|-----------------------|
| <span data-ttu-id="17b16-139">4:0 (ЛСБ \* )</span><span class="sxs-lookup"><span data-stu-id="17b16-139">4:0 (LSB\*)</span></span> | <span data-ttu-id="17b16-140">Компонент синего цвета</span><span class="sxs-lookup"><span data-stu-id="17b16-140">Blue color component</span></span>  |
| <span data-ttu-id="17b16-141">10:5</span><span class="sxs-lookup"><span data-stu-id="17b16-141">10:5</span></span>        | <span data-ttu-id="17b16-142">Компонент зеленого цвета</span><span class="sxs-lookup"><span data-stu-id="17b16-142">Green color component</span></span> |
| <span data-ttu-id="17b16-143">15:11</span><span class="sxs-lookup"><span data-stu-id="17b16-143">15:11</span></span>       | <span data-ttu-id="17b16-144">Компонент красного цвета</span><span class="sxs-lookup"><span data-stu-id="17b16-144">Red color component</span></span>   |



 

<span data-ttu-id="17b16-145">\*Наименьший значащий бит</span><span class="sxs-lookup"><span data-stu-id="17b16-145">\*least-significant bit</span></span>

<span data-ttu-id="17b16-146">Битовое слово \_ 0 располагается следующим образом:</span><span class="sxs-lookup"><span data-stu-id="17b16-146">Bitmap Word\_0 is laid out as follows:</span></span>



| <span data-ttu-id="17b16-147">Bits</span><span class="sxs-lookup"><span data-stu-id="17b16-147">Bits</span></span>          | <span data-ttu-id="17b16-148">Тексель</span><span class="sxs-lookup"><span data-stu-id="17b16-148">Texel</span></span>           |
|---------------|-----------------|
| <span data-ttu-id="17b16-149">1:0 (LSB)</span><span class="sxs-lookup"><span data-stu-id="17b16-149">1:0 (LSB)</span></span>     | <span data-ttu-id="17b16-150">Шаг текселя \[ 0 \] \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="17b16-150">Texel\[0\]\[0\]</span></span> |
| <span data-ttu-id="17b16-151">3:2</span><span class="sxs-lookup"><span data-stu-id="17b16-151">3:2</span></span>           | <span data-ttu-id="17b16-152">Шаг текселя \[ 0 \] \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="17b16-152">Texel\[0\]\[1\]</span></span> |
| <span data-ttu-id="17b16-153">5:4</span><span class="sxs-lookup"><span data-stu-id="17b16-153">5:4</span></span>           | <span data-ttu-id="17b16-154">Шаг текселя \[ 0 \] \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="17b16-154">Texel\[0\]\[2\]</span></span> |
| <span data-ttu-id="17b16-155">7:6</span><span class="sxs-lookup"><span data-stu-id="17b16-155">7:6</span></span>           | <span data-ttu-id="17b16-156">Шаг текселя \[ 0 \] \[ 3\]</span><span class="sxs-lookup"><span data-stu-id="17b16-156">Texel\[0\]\[3\]</span></span> |
| <span data-ttu-id="17b16-157">9:8</span><span class="sxs-lookup"><span data-stu-id="17b16-157">9:8</span></span>           | <span data-ttu-id="17b16-158">Шаг текселя \[ 1 \] \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="17b16-158">Texel\[1\]\[0\]</span></span> |
| <span data-ttu-id="17b16-159">11:10</span><span class="sxs-lookup"><span data-stu-id="17b16-159">11:10</span></span>         | <span data-ttu-id="17b16-160">Шаг текселя \[ 1 \] \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="17b16-160">Texel\[1\]\[1\]</span></span> |
| <span data-ttu-id="17b16-161">13:12</span><span class="sxs-lookup"><span data-stu-id="17b16-161">13:12</span></span>         | <span data-ttu-id="17b16-162">Шаг текселя \[ 1 \] \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="17b16-162">Texel\[1\]\[2\]</span></span> |
| <span data-ttu-id="17b16-163">15:14 (от старшего \* )</span><span class="sxs-lookup"><span data-stu-id="17b16-163">15:14 (MSB\*)</span></span> | <span data-ttu-id="17b16-164">Шаг текселя \[ 1 \] \[ 3\]</span><span class="sxs-lookup"><span data-stu-id="17b16-164">Texel\[1\]\[3\]</span></span> |



 

<span data-ttu-id="17b16-165">\*наиболее значащий бит (старший)</span><span class="sxs-lookup"><span data-stu-id="17b16-165">\*most significant bit (MSB)</span></span>

<span data-ttu-id="17b16-166">Битовое слово \_ 1 размещается следующим образом:</span><span class="sxs-lookup"><span data-stu-id="17b16-166">Bitmap Word\_1 is laid out as follows:</span></span>



| <span data-ttu-id="17b16-167">Bits</span><span class="sxs-lookup"><span data-stu-id="17b16-167">Bits</span></span>        | <span data-ttu-id="17b16-168">Тексель</span><span class="sxs-lookup"><span data-stu-id="17b16-168">Texel</span></span>           |
|-------------|-----------------|
| <span data-ttu-id="17b16-169">1:0 (LSB)</span><span class="sxs-lookup"><span data-stu-id="17b16-169">1:0 (LSB)</span></span>   | <span data-ttu-id="17b16-170">Шаг текселя \[ 2 \] \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="17b16-170">Texel\[2\]\[0\]</span></span> |
| <span data-ttu-id="17b16-171">3:2</span><span class="sxs-lookup"><span data-stu-id="17b16-171">3:2</span></span>         | <span data-ttu-id="17b16-172">Шаг текселя \[ 2 \] \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="17b16-172">Texel\[2\]\[1\]</span></span> |
| <span data-ttu-id="17b16-173">5:4</span><span class="sxs-lookup"><span data-stu-id="17b16-173">5:4</span></span>         | <span data-ttu-id="17b16-174">Шаг текселя \[ 2 \] \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="17b16-174">Texel\[2\]\[2\]</span></span> |
| <span data-ttu-id="17b16-175">7:6</span><span class="sxs-lookup"><span data-stu-id="17b16-175">7:6</span></span>         | <span data-ttu-id="17b16-176">Шаг текселя \[ 2 \] \[ 3\]</span><span class="sxs-lookup"><span data-stu-id="17b16-176">Texel\[2\]\[3\]</span></span> |
| <span data-ttu-id="17b16-177">9:8</span><span class="sxs-lookup"><span data-stu-id="17b16-177">9:8</span></span>         | <span data-ttu-id="17b16-178">Шаг текселя \[ 3 \] \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="17b16-178">Texel\[3\]\[0\]</span></span> |
| <span data-ttu-id="17b16-179">11:10</span><span class="sxs-lookup"><span data-stu-id="17b16-179">11:10</span></span>       | <span data-ttu-id="17b16-180">Шаг текселя \[ 3 \] \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="17b16-180">Texel\[3\]\[1\]</span></span> |
| <span data-ttu-id="17b16-181">13:12</span><span class="sxs-lookup"><span data-stu-id="17b16-181">13:12</span></span>       | <span data-ttu-id="17b16-182">Шаг текселя \[ 3 \] \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="17b16-182">Texel\[3\]\[2\]</span></span> |
| <span data-ttu-id="17b16-183">15:14 (MSB)</span><span class="sxs-lookup"><span data-stu-id="17b16-183">15:14 (MSB)</span></span> | <span data-ttu-id="17b16-184">Шаг текселя \[ 3 \] \[ 3\]</span><span class="sxs-lookup"><span data-stu-id="17b16-184">Texel\[3\]\[3\]</span></span> |



 

## <a name="example-of-opaque-color-encoding"></a><span data-ttu-id="17b16-185">Пример непрозрачной кодировки цвета</span><span class="sxs-lookup"><span data-stu-id="17b16-185">Example of Opaque Color Encoding</span></span>

<span data-ttu-id="17b16-186">В примере кодирования непрозрачного цвета предположим, что красный и черный цвета находятся на разных краях диапазона.</span><span class="sxs-lookup"><span data-stu-id="17b16-186">As an example of opaque encoding, assume that the colors red and black are at the extremes.</span></span> <span data-ttu-id="17b16-187">Красный цвет — \_ 0, а черный — цвет \_ 1.</span><span class="sxs-lookup"><span data-stu-id="17b16-187">Red is color\_0, and black is color\_1.</span></span> <span data-ttu-id="17b16-188">Существует четыре интерполированных цвета, которые образуют равномерно распределенный между ними градиент.</span><span class="sxs-lookup"><span data-stu-id="17b16-188">There are four interpolated colors that form the uniformly distributed gradient between them.</span></span> <span data-ttu-id="17b16-189">Чтобы определить значения для битовой карты 4 x 4, используются следующие расчеты.</span><span class="sxs-lookup"><span data-stu-id="17b16-189">To determine the values for the 4x4 bitmap, the following calculations are used:</span></span>


```
00 ? color_0
01 ? color_1
10 ? 2/3 color_0 + 1/3 color_1
11 ? 1/3 color_0 + 2/3 color_1
```



<span data-ttu-id="17b16-190">Битовая карта выглядит согласно следующей схеме.</span><span class="sxs-lookup"><span data-stu-id="17b16-190">The bitmap then looks like the following diagram.</span></span>

![Схема, показывающая развернутую разметку точечного рисунка.](images/colors2.png)

<span data-ttu-id="17b16-192">Это выглядит как следующий набор цветов на иллюстрации.</span><span class="sxs-lookup"><span data-stu-id="17b16-192">This looks like the following illustrated series of colors.</span></span>

> [!Note]  
> <span data-ttu-id="17b16-193">В изображении в верхнем левом углу отображается пиксель (0, 0).</span><span class="sxs-lookup"><span data-stu-id="17b16-193">In an image, pixel (0,0) appears on the top left.</span></span>

 

![иллюстрация непрозрачного закодированного градиента](images/redsquares.png)

## <a name="example-of-1-bit-alpha-encoding"></a><span data-ttu-id="17b16-195">Пример 1-битовой кодировки Alpha</span><span class="sxs-lookup"><span data-stu-id="17b16-195">Example of 1-Bit Alpha Encoding</span></span>

<span data-ttu-id="17b16-196">Этот формат выбирается, когда 16-разрядное целое число без знака, цвет \_ 0, меньше, чем 16-разрядное целое число без знака, цвет \_ 1.</span><span class="sxs-lookup"><span data-stu-id="17b16-196">This format is selected when the unsigned 16-bit integer, color\_0, is less than the unsigned 16-bit integer, color\_1.</span></span> <span data-ttu-id="17b16-197">Пример использования этого формата — листья на дереве на фоне голубого неба.</span><span class="sxs-lookup"><span data-stu-id="17b16-197">An example of where this format can be used is leaves on a tree, shown against a blue sky.</span></span> <span data-ttu-id="17b16-198">Некоторые тексели могут быть отмечены как прозрачные, и в то же время три оттенка зеленого по-прежнему доступны для листьев.</span><span class="sxs-lookup"><span data-stu-id="17b16-198">Some texels can be marked as transparent while three shades of green are still available for the leaves.</span></span> <span data-ttu-id="17b16-199">Два цвета располагаются по краям, а третий является интерполированным цветом.</span><span class="sxs-lookup"><span data-stu-id="17b16-199">Two colors fix the extremes, and the third is an interpolated color.</span></span>

<span data-ttu-id="17b16-200">Ниже приведена иллюстрация с примером такого рисунка.</span><span class="sxs-lookup"><span data-stu-id="17b16-200">The following illustration is an example of such a picture.</span></span>

![иллюстрация кодирования 1-разрядного альфа-значения](images/greenthing.png)

<span data-ttu-id="17b16-202">Обратите внимание, что если изображение отображается белым, шаг текселя будет кодироваться как прозрачный.</span><span class="sxs-lookup"><span data-stu-id="17b16-202">Note that where the image is shown as white, the texel would be encoded as transparent.</span></span> <span data-ttu-id="17b16-203">Также обратите внимание, что для компонентов RGBA прозрачного пикселей текстуры должно быть установлено значение 0 перед наложением.</span><span class="sxs-lookup"><span data-stu-id="17b16-203">Also note that the RGBA components of the transparent texels should be set to zero before blending.</span></span>

<span data-ttu-id="17b16-204">Кодировка битовой карты для цветов и прозрачности определяется с помощью следующих вычислений.</span><span class="sxs-lookup"><span data-stu-id="17b16-204">The bitmap encoding for the colors and the transparency is determined using the following calculations.</span></span>


```
00 ? color_0
01 ? color_1
10 ? 1/2 color_0 + 1/2 color_1
11   ?   Transparent
```



<span data-ttu-id="17b16-205">Битовая карта выглядит согласно следующей схеме.</span><span class="sxs-lookup"><span data-stu-id="17b16-205">The bitmap then looks like the following diagram.</span></span>

![схема развернутой битовой карты](images/colors3.png)

## <a name="related-topics"></a><span data-ttu-id="17b16-207">См. также</span><span class="sxs-lookup"><span data-stu-id="17b16-207">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="17b16-208">Сжатые ресурсы текстуры</span><span class="sxs-lookup"><span data-stu-id="17b16-208">Compressed Texture Resources</span></span>](compressed-texture-resources.md)
</dt> </dl>

 

 



