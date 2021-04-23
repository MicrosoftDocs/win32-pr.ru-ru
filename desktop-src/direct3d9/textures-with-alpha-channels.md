---
description: Существует два способа кодирования карт текстур с более сложной прозрачностью.
ms.assetid: cae788f6-60f1-4987-8f06-bf4256bccd9b
title: Текстуры с альфа-каналами (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2c361b0335ef4f36b4efc9c90c71270e855f5db
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104567466"
---
# <a name="textures-with-alpha-channels-direct3d-9"></a><span data-ttu-id="c0cca-103">Текстуры с альфа-каналами (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="c0cca-103">Textures with Alpha Channels (Direct3D 9)</span></span>

<span data-ttu-id="c0cca-104">Существует два способа кодирования карт текстур с более сложной прозрачностью.</span><span class="sxs-lookup"><span data-stu-id="c0cca-104">There are two ways to encode texture maps that exhibit more complex transparency.</span></span> <span data-ttu-id="c0cca-105">В каждом случае блок, описывающий прозрачность, предшествует 64-разрядному блоку, который уже был описан.</span><span class="sxs-lookup"><span data-stu-id="c0cca-105">In each case, a block that describes the transparency precedes the 64-bit block already described.</span></span> <span data-ttu-id="c0cca-106">Прозрачность представляется либо в виде точечного рисунка 4x4 с 4 битами на пиксель (явная кодировка) или с меньшим количеством битов и линейной интерполяцией, которая аналогична тому, что используется в кодировании цвета.</span><span class="sxs-lookup"><span data-stu-id="c0cca-106">The transparency is either represented as a 4x4 bitmap with 4 bits per pixel (explicit encoding), or with fewer bits and linear interpolation that is analogous to what is used for color encoding.</span></span>

<span data-ttu-id="c0cca-107">Блок прозрачности и цветовой блок упорядочиваются так, как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="c0cca-107">The transparency block and the color block are arranged as shown in the following table.</span></span>



| <span data-ttu-id="c0cca-108">Адрес слова</span><span class="sxs-lookup"><span data-stu-id="c0cca-108">Word address</span></span> | <span data-ttu-id="c0cca-109">64-разрядный блок</span><span class="sxs-lookup"><span data-stu-id="c0cca-109">64-bit block</span></span>                      |
|--------------|-----------------------------------|
| <span data-ttu-id="c0cca-110">3:0</span><span class="sxs-lookup"><span data-stu-id="c0cca-110">3:0</span></span>          | <span data-ttu-id="c0cca-111">Блок прозрачности</span><span class="sxs-lookup"><span data-stu-id="c0cca-111">Transparency block</span></span>                |
| <span data-ttu-id="c0cca-112">7:4</span><span class="sxs-lookup"><span data-stu-id="c0cca-112">7:4</span></span>          | <span data-ttu-id="c0cca-113">Вышеописанный 64-разрядный блок</span><span class="sxs-lookup"><span data-stu-id="c0cca-113">Previously described 64-bit block</span></span> |



 

## <a name="explicit-texture-encoding"></a><span data-ttu-id="c0cca-114">Явная кодировка текстуры</span><span class="sxs-lookup"><span data-stu-id="c0cca-114">Explicit Texture Encoding</span></span>

<span data-ttu-id="c0cca-115">Для явной кодировки текстуры (форматы DXT2 и DXT3) альфа-компоненты пикселей текстуры, описывающие прозрачность, кодируются в битовой карте 4x4 с 4 битами на шаг текселя.</span><span class="sxs-lookup"><span data-stu-id="c0cca-115">For explicit texture encoding (DXT2 and DXT3 formats), the alpha components of the texels that describe transparency are encoded in a 4x4 bitmap with 4 bits per texel.</span></span> <span data-ttu-id="c0cca-116">Эти четыре бита можно получить различными способами, например с помощью сглаживания или используя четыре наиболее важных бита данных альфа-канала.</span><span class="sxs-lookup"><span data-stu-id="c0cca-116">These four bits can be achieved through a variety of means such as dithering or by using the four most significant bits of the alpha data.</span></span> <span data-ttu-id="c0cca-117">Как бы они ни были получены, они используются в текущем виде, без интерполяции в любой форме.</span><span class="sxs-lookup"><span data-stu-id="c0cca-117">However they are produced, they are used just as they are, without any form of interpolation.</span></span>

<span data-ttu-id="c0cca-118">На следующей схеме показан блок 64-разрядной прозрачности.</span><span class="sxs-lookup"><span data-stu-id="c0cca-118">The following diagram shows a 64-bit transparency block.</span></span>

![Диаграмма 64-разрядного блока прозрачности](images/colors4.png)

> [!Note]  
> <span data-ttu-id="c0cca-120">Метод сжатия Direct3D использует четыре наиболее значимых бита.</span><span class="sxs-lookup"><span data-stu-id="c0cca-120">The compression method of Direct3D uses the four most significant bits.</span></span>

 

<span data-ttu-id="c0cca-121">В следующих таблицах показано, как размещены в памяти данные альфа-канала для каждого 16-разрядного слова.</span><span class="sxs-lookup"><span data-stu-id="c0cca-121">The following tables illustrate how the alpha information is laid out in memory, for each 16-bit word.</span></span>

<span data-ttu-id="c0cca-122">Эта таблица содержит макет для Word 0.</span><span class="sxs-lookup"><span data-stu-id="c0cca-122">This table contains the layout for word 0.</span></span>



| <span data-ttu-id="c0cca-123">Bits</span><span class="sxs-lookup"><span data-stu-id="c0cca-123">Bits</span></span>          | <span data-ttu-id="c0cca-124">Коэффициент альфа</span><span class="sxs-lookup"><span data-stu-id="c0cca-124">Alpha</span></span>      |
|---------------|------------|
| <span data-ttu-id="c0cca-125">3:0 (ЛСБ \* )</span><span class="sxs-lookup"><span data-stu-id="c0cca-125">3:0 (LSB\*)</span></span>   | <span data-ttu-id="c0cca-126">\[0 \] \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="c0cca-126">\[0\]\[0\]</span></span> |
| <span data-ttu-id="c0cca-127">7:4</span><span class="sxs-lookup"><span data-stu-id="c0cca-127">7:4</span></span>           | <span data-ttu-id="c0cca-128">\[0 \] \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="c0cca-128">\[0\]\[1\]</span></span> |
| <span data-ttu-id="c0cca-129">11:8</span><span class="sxs-lookup"><span data-stu-id="c0cca-129">11:8</span></span>          | <span data-ttu-id="c0cca-130">\[0 \] \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="c0cca-130">\[0\]\[2\]</span></span> |
| <span data-ttu-id="c0cca-131">15:12 (от старшего \* )</span><span class="sxs-lookup"><span data-stu-id="c0cca-131">15:12 (MSB\*)</span></span> | <span data-ttu-id="c0cca-132">\[0 \] \[ 3\]</span><span class="sxs-lookup"><span data-stu-id="c0cca-132">\[0\]\[3\]</span></span> |



 

<span data-ttu-id="c0cca-133">\*Наименьший значащий бит, самый значащий бит (старший)</span><span class="sxs-lookup"><span data-stu-id="c0cca-133">\*least-significant bit, most significant bit (MSB)</span></span>

<span data-ttu-id="c0cca-134">Эта таблица содержит макет для Word 1.</span><span class="sxs-lookup"><span data-stu-id="c0cca-134">This table contains the layout for word 1.</span></span>



| <span data-ttu-id="c0cca-135">Bits</span><span class="sxs-lookup"><span data-stu-id="c0cca-135">Bits</span></span>        | <span data-ttu-id="c0cca-136">Коэффициент альфа</span><span class="sxs-lookup"><span data-stu-id="c0cca-136">Alpha</span></span>      |
|-------------|------------|
| <span data-ttu-id="c0cca-137">3:0 (LSB)</span><span class="sxs-lookup"><span data-stu-id="c0cca-137">3:0 (LSB)</span></span>   | <span data-ttu-id="c0cca-138">\[1 \] \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="c0cca-138">\[1\]\[0\]</span></span> |
| <span data-ttu-id="c0cca-139">7:4</span><span class="sxs-lookup"><span data-stu-id="c0cca-139">7:4</span></span>         | <span data-ttu-id="c0cca-140">\[1 \] \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="c0cca-140">\[1\]\[1\]</span></span> |
| <span data-ttu-id="c0cca-141">11:8</span><span class="sxs-lookup"><span data-stu-id="c0cca-141">11:8</span></span>        | <span data-ttu-id="c0cca-142">\[1 \] \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="c0cca-142">\[1\]\[2\]</span></span> |
| <span data-ttu-id="c0cca-143">15:12 (MSB)</span><span class="sxs-lookup"><span data-stu-id="c0cca-143">15:12 (MSB)</span></span> | <span data-ttu-id="c0cca-144">\[1 \] \[ 3\]</span><span class="sxs-lookup"><span data-stu-id="c0cca-144">\[1\]\[3\]</span></span> |



 

<span data-ttu-id="c0cca-145">Эта таблица содержит макет для Word 2.</span><span class="sxs-lookup"><span data-stu-id="c0cca-145">This table contains the layout for word 2.</span></span>



| <span data-ttu-id="c0cca-146">Bits</span><span class="sxs-lookup"><span data-stu-id="c0cca-146">Bits</span></span>        | <span data-ttu-id="c0cca-147">Коэффициент альфа</span><span class="sxs-lookup"><span data-stu-id="c0cca-147">Alpha</span></span>      |
|-------------|------------|
| <span data-ttu-id="c0cca-148">3:0 (LSB)</span><span class="sxs-lookup"><span data-stu-id="c0cca-148">3:0 (LSB)</span></span>   | <span data-ttu-id="c0cca-149">\[2 \] \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="c0cca-149">\[2\]\[0\]</span></span> |
| <span data-ttu-id="c0cca-150">7:4</span><span class="sxs-lookup"><span data-stu-id="c0cca-150">7:4</span></span>         | <span data-ttu-id="c0cca-151">\[2 \] \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="c0cca-151">\[2\]\[1\]</span></span> |
| <span data-ttu-id="c0cca-152">11:8</span><span class="sxs-lookup"><span data-stu-id="c0cca-152">11:8</span></span>        | <span data-ttu-id="c0cca-153">\[2 \] \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="c0cca-153">\[2\]\[2\]</span></span> |
| <span data-ttu-id="c0cca-154">15:12 (MSB)</span><span class="sxs-lookup"><span data-stu-id="c0cca-154">15:12 (MSB)</span></span> | <span data-ttu-id="c0cca-155">\[2 \] \[ 3\]</span><span class="sxs-lookup"><span data-stu-id="c0cca-155">\[2\]\[3\]</span></span> |



 

<span data-ttu-id="c0cca-156">Эта таблица содержит макет для Word 3.</span><span class="sxs-lookup"><span data-stu-id="c0cca-156">This table contains the layout for word 3.</span></span>



| <span data-ttu-id="c0cca-157">Bits</span><span class="sxs-lookup"><span data-stu-id="c0cca-157">Bits</span></span>        | <span data-ttu-id="c0cca-158">Коэффициент альфа</span><span class="sxs-lookup"><span data-stu-id="c0cca-158">Alpha</span></span>      |
|-------------|------------|
| <span data-ttu-id="c0cca-159">3:0 (LSB)</span><span class="sxs-lookup"><span data-stu-id="c0cca-159">3:0 (LSB)</span></span>   | <span data-ttu-id="c0cca-160">\[3 \] \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="c0cca-160">\[3\]\[0\]</span></span> |
| <span data-ttu-id="c0cca-161">7:4</span><span class="sxs-lookup"><span data-stu-id="c0cca-161">7:4</span></span>         | <span data-ttu-id="c0cca-162">\[3 \] \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="c0cca-162">\[3\]\[1\]</span></span> |
| <span data-ttu-id="c0cca-163">11:8</span><span class="sxs-lookup"><span data-stu-id="c0cca-163">11:8</span></span>        | <span data-ttu-id="c0cca-164">\[3 \] \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="c0cca-164">\[3\]\[2\]</span></span> |
| <span data-ttu-id="c0cca-165">15:12 (MSB)</span><span class="sxs-lookup"><span data-stu-id="c0cca-165">15:12 (MSB)</span></span> | <span data-ttu-id="c0cca-166">\[3 \] \[ 3\]</span><span class="sxs-lookup"><span data-stu-id="c0cca-166">\[3\]\[3\]</span></span> |



 

<span data-ttu-id="c0cca-167">Разница между DXT2 и DXT3 заключается в том, что в формате DXT2 предполагается, что данные цвета были предварительно умножены на альфа.</span><span class="sxs-lookup"><span data-stu-id="c0cca-167">The difference between DXT2 and DXT3 are that, in the DXT2 format, it is assumed that the color data has been premultiplied by alpha.</span></span> <span data-ttu-id="c0cca-168">В формате DXT3 предполагается, что цвет не является предварительно умноженным на альфа.</span><span class="sxs-lookup"><span data-stu-id="c0cca-168">In the DXT3 format, it is assumed that the color is not premultiplied by alpha.</span></span> <span data-ttu-id="c0cca-169">Эти два формата необходимы, так как в большинстве случаев, когда используется текстура, простого изучения данных недостаточно, чтобы определить, были ли значения цвета умножены на альфа.</span><span class="sxs-lookup"><span data-stu-id="c0cca-169">These two formats are needed because, in most cases, by the time a texture is used, just examining the data is not sufficient to determine if the color values have been multiplied by alpha.</span></span> <span data-ttu-id="c0cca-170">Поскольку эти сведения необходимы во время выполнения, для различения этих случаев используются два кода FOURCC.</span><span class="sxs-lookup"><span data-stu-id="c0cca-170">Because this information is needed at run time, the two FOURCC codes are used to differentiate these cases.</span></span> <span data-ttu-id="c0cca-171">Однако данные и метод интерполяции, используемые для этих двух форматов, идентичны.</span><span class="sxs-lookup"><span data-stu-id="c0cca-171">However, the data and interpolation method used for these two formats is identical.</span></span>

<span data-ttu-id="c0cca-172">Сравнение цветов, используемое в DXT1, чтобы определить, является ли шаг текселя прозрачным, не используется в этом формате.</span><span class="sxs-lookup"><span data-stu-id="c0cca-172">The color compare used in DXT1 to determine if the texel is transparent is not used in this format.</span></span> <span data-ttu-id="c0cca-173">Предполагается, что без сравнения цвета цветовые данные всегда обрабатываются в четырехцветном режиме.</span><span class="sxs-lookup"><span data-stu-id="c0cca-173">It is assumed that without the color compare the color data is always treated as if in 4-color mode.</span></span> <span data-ttu-id="c0cca-174">Иными словами, оператор if в верхней части кода DXT1 должен быть следующим:</span><span class="sxs-lookup"><span data-stu-id="c0cca-174">In other words, the if statement at the top of the DXT1 code should be the following:</span></span>


```
if ((color_0 > color_1) OR !DXT1) {
```



## <a name="three-bit-linear-alpha-interpolation"></a><span data-ttu-id="c0cca-175">Three-Bit линейная альфа-интерполяция</span><span class="sxs-lookup"><span data-stu-id="c0cca-175">Three-Bit Linear Alpha Interpolation</span></span>

<span data-ttu-id="c0cca-176">Кодировка прозрачности для форматов DXT4 и DXT5 основана на концепции, аналогичной линейной кодировке, используемой для цвета.</span><span class="sxs-lookup"><span data-stu-id="c0cca-176">The encoding of transparency for the DXT4 and DXT5 formats is based on a concept similar to the linear encoding used for color.</span></span> <span data-ttu-id="c0cca-177">Два 8-разрядных альфа-фактора и точечный рисунок 4x4 с тремя битами на пиксель хранятся в первых восьми байтах блока.</span><span class="sxs-lookup"><span data-stu-id="c0cca-177">Two 8-bit alpha values and a 4x4 bitmap with three bits per pixel are stored in the first eight bytes of the block.</span></span> <span data-ttu-id="c0cca-178">Репрезентативные альфа-факторы используются для интерполяции промежуточных альфа-факторов.</span><span class="sxs-lookup"><span data-stu-id="c0cca-178">The representative alpha values are used to interpolate intermediate alpha values.</span></span> <span data-ttu-id="c0cca-179">Дополнительная информация содержится в способе хранения двух альфа-факторов.</span><span class="sxs-lookup"><span data-stu-id="c0cca-179">Additional information is available in the way the two alpha values are stored.</span></span> <span data-ttu-id="c0cca-180">Если альфа \_ 0 больше альфа \_ 1, то интерполяция создает шесть промежуточных альфа-значений.</span><span class="sxs-lookup"><span data-stu-id="c0cca-180">If alpha\_0 is greater than alpha\_1, then six intermediate alpha values are created by the interpolation.</span></span> <span data-ttu-id="c0cca-181">В противном случае четыре промежуточных альфа-фактора интерполируются между указанными крайними альфа-факторами.</span><span class="sxs-lookup"><span data-stu-id="c0cca-181">Otherwise, four intermediate alpha values are interpolated between the specified alpha extremes.</span></span> <span data-ttu-id="c0cca-182">Два дополнительных неявных альфа-фактора: 0 (полностью прозрачный) и 255 (полностью непрозрачный).</span><span class="sxs-lookup"><span data-stu-id="c0cca-182">The two additional implicit alpha values are 0 (fully transparent) and 255 (fully opaque).</span></span>

<span data-ttu-id="c0cca-183">Следующий пример кода иллюстрирует этот алгоритм.</span><span class="sxs-lookup"><span data-stu-id="c0cca-183">The following code example illustrates this algorithm.</span></span>


```
// 8-alpha or 6-alpha block?    
if (alpha_0 > alpha_1) {    
    // 8-alpha block:  derive the other six alphas.    
    // Bit code 000 = alpha_0, 001 = alpha_1, others are interpolated.
    alpha_2 = (6 * alpha_0 + 1 * alpha_1 + 3) / 7;    // bit code 010
    alpha_3 = (5 * alpha_0 + 2 * alpha_1 + 3) / 7;    // bit code 011
    alpha_4 = (4 * alpha_0 + 3 * alpha_1 + 3) / 7;    // bit code 100
    alpha_5 = (3 * alpha_0 + 4 * alpha_1 + 3) / 7;    // bit code 101
    alpha_6 = (2 * alpha_0 + 5 * alpha_1 + 3) / 7;    // bit code 110
    alpha_7 = (1 * alpha_0 + 6 * alpha_1 + 3) / 7;    // bit code 111  
}    
else {  
    // 6-alpha block.    
    // Bit code 000 = alpha_0, 001 = alpha_1, others are interpolated.
    alpha_2 = (4 * alpha_0 + 1 * alpha_1 + 2) / 5;    // Bit code 010
    alpha_3 = (3 * alpha_0 + 2 * alpha_1 + 2) / 5;    // Bit code 011
    alpha_4 = (2 * alpha_0 + 3 * alpha_1 + 2) / 5;    // Bit code 100
    alpha_5 = (1 * alpha_0 + 4 * alpha_1 + 2) / 5;    // Bit code 101
    alpha_6 = 0;                                      // Bit code 110
    alpha_7 = 255;                                    // Bit code 111
}
```



<span data-ttu-id="c0cca-184">Схема памяти альфа-блока выглядит следующим образом.</span><span class="sxs-lookup"><span data-stu-id="c0cca-184">The memory layout of the alpha block is as follows:</span></span>



| <span data-ttu-id="c0cca-185">Byte</span><span class="sxs-lookup"><span data-stu-id="c0cca-185">Byte</span></span> | <span data-ttu-id="c0cca-186">Коэффициент альфа</span><span class="sxs-lookup"><span data-stu-id="c0cca-186">Alpha</span></span>                                                          |
|------|----------------------------------------------------------------|
| <span data-ttu-id="c0cca-187">0</span><span class="sxs-lookup"><span data-stu-id="c0cca-187">0</span></span>    | <span data-ttu-id="c0cca-188">Альфа \_ 0</span><span class="sxs-lookup"><span data-stu-id="c0cca-188">Alpha\_0</span></span>                                                       |
| <span data-ttu-id="c0cca-189">1</span><span class="sxs-lookup"><span data-stu-id="c0cca-189">1</span></span>    | <span data-ttu-id="c0cca-190">Альфа \_ 1</span><span class="sxs-lookup"><span data-stu-id="c0cca-190">Alpha\_1</span></span>                                                       |
| <span data-ttu-id="c0cca-191">2</span><span class="sxs-lookup"><span data-stu-id="c0cca-191">2</span></span>    | <span data-ttu-id="c0cca-192">\[0 \] \[ 2 \] (2 МСБС), \[ 0 \] \[ 1 \] , \[ 0 \] \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="c0cca-192">\[0\]\[2\] (2 MSBs), \[0\]\[1\], \[0\]\[0\]</span></span>                    |
| <span data-ttu-id="c0cca-193">3</span><span class="sxs-lookup"><span data-stu-id="c0cca-193">3</span></span>    | <span data-ttu-id="c0cca-194">\[1 \] \[ 1 \] (1-е), \[ 1 \] \[ 0 \] , \[ 0 \] \[ 3 \] , \[ 0 \] \[ 2 \] (1 ЛСБ)</span><span class="sxs-lookup"><span data-stu-id="c0cca-194">\[1\]\[1\] (1 MSB), \[1\]\[0\], \[0\]\[3\], \[0\]\[2\] (1 LSB)</span></span> |
| <span data-ttu-id="c0cca-195">4</span><span class="sxs-lookup"><span data-stu-id="c0cca-195">4</span></span>    | <span data-ttu-id="c0cca-196">\[1 \] \[ 3 \] , \[ 1 \] \[ 2 \] , \[ 1 \] \[ 1 \] (2 лсбс)</span><span class="sxs-lookup"><span data-stu-id="c0cca-196">\[1\]\[3\], \[1\]\[2\], \[1\]\[1\] (2 LSBs)</span></span>                    |
| <span data-ttu-id="c0cca-197">5</span><span class="sxs-lookup"><span data-stu-id="c0cca-197">5</span></span>    | <span data-ttu-id="c0cca-198">\[2 \] \[ 2 \] (2 МСБС), \[ 2 \] \[ 1 \] , \[ 2 \] \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="c0cca-198">\[2\]\[2\] (2 MSBs), \[2\]\[1\], \[2\]\[0\]</span></span>                    |
| <span data-ttu-id="c0cca-199">6</span><span class="sxs-lookup"><span data-stu-id="c0cca-199">6</span></span>    | <span data-ttu-id="c0cca-200">\[3 \] \[ 1 \] (1-е \[ \] \[ , 0 – 4, 2 \] \[ \] \[ 3 \] , 2 \[ \] \[ 2 \] (1 ЛСБ)</span><span class="sxs-lookup"><span data-stu-id="c0cca-200">\[3\]\[1\] (1 MSB), \[3\]\[0\], \[2\]\[3\], \[2\]\[2\] (1 LSB)</span></span> |
| <span data-ttu-id="c0cca-201">7</span><span class="sxs-lookup"><span data-stu-id="c0cca-201">7</span></span>    | <span data-ttu-id="c0cca-202">\[3 \] \[ 3 \] , \[ 3 \] \[ 2 \] , \[ 3 \] \[ 1 \] (2 лсбс)</span><span class="sxs-lookup"><span data-stu-id="c0cca-202">\[3\]\[3\], \[3\]\[2\], \[3\]\[1\] (2 LSBs)</span></span>                    |



 

<span data-ttu-id="c0cca-203">Разница между DXT4 и DXT5 заключается в том, что в формате DXT4 предполагается, что данные цвета были предварительно умножены на альфа.</span><span class="sxs-lookup"><span data-stu-id="c0cca-203">The difference between DXT4 and DXT5 is that in the DXT4 format it is assumed that the color data has been premultiplied by alpha.</span></span> <span data-ttu-id="c0cca-204">В формате DXT5 предполагается, что цвет не является предварительно умноженным на альфа.</span><span class="sxs-lookup"><span data-stu-id="c0cca-204">In the DXT5 format, it is assumed the color is not premultiplied by alpha.</span></span> <span data-ttu-id="c0cca-205">Эти два формата необходимы, так как в большинстве случаев, когда используется текстура, простого изучения данных недостаточно, чтобы определить, были ли значения цвета умножены на альфа.</span><span class="sxs-lookup"><span data-stu-id="c0cca-205">These two formats are needed because, in most cases, by the time a texture is used, just examining the data is not sufficient to determine if the color values have been multiplied by alpha.</span></span> <span data-ttu-id="c0cca-206">Поскольку эти сведения необходимы во время выполнения, для различения этих случаев используются два кода FOURCC.</span><span class="sxs-lookup"><span data-stu-id="c0cca-206">Because this information is needed at run time, the two FOURCC codes are used to differentiate these cases.</span></span> <span data-ttu-id="c0cca-207">Однако данные и метод интерполяции, используемые для этих двух форматов, идентичны.</span><span class="sxs-lookup"><span data-stu-id="c0cca-207">However, the data and interpolation method used for these two formats is identical.</span></span>

<span data-ttu-id="c0cca-208">Сравнение цветов, используемое в DXT1, чтобы определить, является ли шаг текселя прозрачным, не используется в этих форматах.</span><span class="sxs-lookup"><span data-stu-id="c0cca-208">The color compare used in DXT1 to determine if the texel is transparent is not used with these formats.</span></span> <span data-ttu-id="c0cca-209">Предполагается, что без сравнения цвета цветовые данные всегда обрабатываются в четырехцветном режиме.</span><span class="sxs-lookup"><span data-stu-id="c0cca-209">It is assumed that without the color compare the color data is always treated as if in 4-color mode.</span></span> <span data-ttu-id="c0cca-210">Иными словами, оператор if в начале кода DXT1 должен быть следующим:</span><span class="sxs-lookup"><span data-stu-id="c0cca-210">In other words, the if statement at the top of the DXT1 code should be:</span></span>


```
if ((color_0 > color_1) OR !DXT1) {
```



## <a name="related-topics"></a><span data-ttu-id="c0cca-211">См. также</span><span class="sxs-lookup"><span data-stu-id="c0cca-211">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c0cca-212">Сжатые ресурсы текстуры</span><span class="sxs-lookup"><span data-stu-id="c0cca-212">Compressed Texture Resources</span></span>](compressed-texture-resources.md)
</dt> </dl>

 

 



