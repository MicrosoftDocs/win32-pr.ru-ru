---
description: В этом разделе перечислены коды двоичных растровых операций, используемых функциями GetROP2 и SetROP2. Коды операций растрового изображения определяют, как GDI объединяет биты из выбранного пера с битами в битовой карте назначения.
ms.assetid: 9a3a5b5d-b41f-4859-8830-98272983a635
title: Двоичные растровые операции
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd8a70030b1940c31d036505a80a6b1868aececd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155702"
---
# <a name="binary-raster-operations"></a><span data-ttu-id="84365-104">Двоичные растровые операции</span><span class="sxs-lookup"><span data-stu-id="84365-104">Binary Raster Operations</span></span>

<span data-ttu-id="84365-105">В этом разделе перечислены коды двоичных растровых операций, используемых функциями [**GetROP2**](/windows/desktop/api/Wingdi/nf-wingdi-getrop2) и [**SetROP2**](/windows/desktop/api/Wingdi/nf-wingdi-setrop2) .</span><span class="sxs-lookup"><span data-stu-id="84365-105">This section lists the binary raster-operation codes used by the [**GetROP2**](/windows/desktop/api/Wingdi/nf-wingdi-getrop2) and [**SetROP2**](/windows/desktop/api/Wingdi/nf-wingdi-setrop2) functions.</span></span> <span data-ttu-id="84365-106">Коды операций растрового изображения определяют, как GDI объединяет биты из выбранного пера с битами в битовой карте назначения.</span><span class="sxs-lookup"><span data-stu-id="84365-106">Raster-operation codes define how GDI combines the bits from the selected pen with the bits in the destination bitmap.</span></span>

<span data-ttu-id="84365-107">Каждый код точечной операции представляет логическую операцию, в которой значения пикселей в выбранном пере и битовой карте назначения объединяются.</span><span class="sxs-lookup"><span data-stu-id="84365-107">Each raster-operation code represents a Boolean operation in which the values of the pixels in the selected pen and the destination bitmap are combined.</span></span> <span data-ttu-id="84365-108">Ниже приведены два операнда, используемые в этих операциях.</span><span class="sxs-lookup"><span data-stu-id="84365-108">The following are the two operands used in these operations.</span></span>



| <span data-ttu-id="84365-109">Операнд</span><span class="sxs-lookup"><span data-stu-id="84365-109">Operand</span></span> | <span data-ttu-id="84365-110">Значение</span><span class="sxs-lookup"><span data-stu-id="84365-110">Meaning</span></span>            |
|---------|--------------------|
| <span data-ttu-id="84365-111">С</span><span class="sxs-lookup"><span data-stu-id="84365-111">P</span></span>       | <span data-ttu-id="84365-112">Выбранное перо</span><span class="sxs-lookup"><span data-stu-id="84365-112">Selected pen</span></span>       |
| <span data-ttu-id="84365-113">D</span><span class="sxs-lookup"><span data-stu-id="84365-113">D</span></span>       | <span data-ttu-id="84365-114">Точечный рисунок назначения</span><span class="sxs-lookup"><span data-stu-id="84365-114">Destination bitmap</span></span> |



 

<span data-ttu-id="84365-115">Далее следуют логические операторы, используемые в этих операциях.</span><span class="sxs-lookup"><span data-stu-id="84365-115">The Boolean operators used in these operations follow.</span></span>



| <span data-ttu-id="84365-116">Оператор</span><span class="sxs-lookup"><span data-stu-id="84365-116">Operator</span></span> | <span data-ttu-id="84365-117">Значение</span><span class="sxs-lookup"><span data-stu-id="84365-117">Meaning</span></span>                    |
|----------|----------------------------|
| <span data-ttu-id="84365-118">а</span><span class="sxs-lookup"><span data-stu-id="84365-118">a</span></span>        | <span data-ttu-id="84365-119">Побитовое И</span><span class="sxs-lookup"><span data-stu-id="84365-119">Bitwise AND</span></span>                |
| <span data-ttu-id="84365-120">n</span><span class="sxs-lookup"><span data-stu-id="84365-120">n</span></span>        | <span data-ttu-id="84365-121">Побитовое не (обратная)</span><span class="sxs-lookup"><span data-stu-id="84365-121">Bitwise NOT (inverse)</span></span>      |
| <span data-ttu-id="84365-122">o</span><span class="sxs-lookup"><span data-stu-id="84365-122">o</span></span>        | <span data-ttu-id="84365-123">Побитовое ИЛИ</span><span class="sxs-lookup"><span data-stu-id="84365-123">Bitwise OR</span></span>                 |
| <span data-ttu-id="84365-124">x</span><span class="sxs-lookup"><span data-stu-id="84365-124">x</span></span>        | <span data-ttu-id="84365-125">Побитовое исключающее или (XOR)</span><span class="sxs-lookup"><span data-stu-id="84365-125">Bitwise exclusive OR (XOR)</span></span> |



 

<span data-ttu-id="84365-126">Все логические операции представлены в виде инвертированной нотации.</span><span class="sxs-lookup"><span data-stu-id="84365-126">All Boolean operations are presented in reverse Polish notation.</span></span> <span data-ttu-id="84365-127">Например, следующая операция заменяет значения пикселов в целевом точечном рисунке на сочетание значений пикселей пера и выбранной кисти:</span><span class="sxs-lookup"><span data-stu-id="84365-127">For example, the following operation replaces the values of the pixels in the destination bitmap with a combination of the pixel values of the pen and the selected brush:</span></span>


```C++
DPo 
```



<span data-ttu-id="84365-128">Каждый код операции с растровой операцией — это 32-разрядное целое число, которое является значением индекса логической операции, а младшее слово — кодом операции.</span><span class="sxs-lookup"><span data-stu-id="84365-128">Each raster-operation code is a 32-bit integer whose high-order word is a Boolean operation index and whose low-order word is the operation code.</span></span> <span data-ttu-id="84365-129">16-разрядный индекс операции — это 8-разрядное значение, которое представляет все возможные результаты, полученные в результате логической операции с двумя параметрами (в данном случае перо и значения назначения).</span><span class="sxs-lookup"><span data-stu-id="84365-129">The 16-bit operation index is a zero-extended 8-bit value that represents all possible outcomes resulting from the Boolean operation on two parameters (in this case, the pen and destination values).</span></span> <span data-ttu-id="84365-130">Например, индексы операции для операций ДПО и Дпан показаны в следующем списке.</span><span class="sxs-lookup"><span data-stu-id="84365-130">For example, the operation indexes for the DPo and DPan operations are shown in the following list.</span></span>



| <span data-ttu-id="84365-131">С</span><span class="sxs-lookup"><span data-stu-id="84365-131">P</span></span>   | <span data-ttu-id="84365-132">D</span><span class="sxs-lookup"><span data-stu-id="84365-132">D</span></span>   | <span data-ttu-id="84365-133">дпо</span><span class="sxs-lookup"><span data-stu-id="84365-133">DPo</span></span> | <span data-ttu-id="84365-134">дпан</span><span class="sxs-lookup"><span data-stu-id="84365-134">Dpan</span></span> |
|-----|-----|-----|------|
| <span data-ttu-id="84365-135">0</span><span class="sxs-lookup"><span data-stu-id="84365-135">0</span></span>   | <span data-ttu-id="84365-136">0</span><span class="sxs-lookup"><span data-stu-id="84365-136">0</span></span>   | <span data-ttu-id="84365-137">0</span><span class="sxs-lookup"><span data-stu-id="84365-137">0</span></span>   | <span data-ttu-id="84365-138">1</span><span class="sxs-lookup"><span data-stu-id="84365-138">1</span></span>    |
| <span data-ttu-id="84365-139">0</span><span class="sxs-lookup"><span data-stu-id="84365-139">0</span></span>   | <span data-ttu-id="84365-140">1</span><span class="sxs-lookup"><span data-stu-id="84365-140">1</span></span>   | <span data-ttu-id="84365-141">1</span><span class="sxs-lookup"><span data-stu-id="84365-141">1</span></span>   | <span data-ttu-id="84365-142">1</span><span class="sxs-lookup"><span data-stu-id="84365-142">1</span></span>    |
| <span data-ttu-id="84365-143">1</span><span class="sxs-lookup"><span data-stu-id="84365-143">1</span></span>   | <span data-ttu-id="84365-144">0</span><span class="sxs-lookup"><span data-stu-id="84365-144">0</span></span>   | <span data-ttu-id="84365-145">1</span><span class="sxs-lookup"><span data-stu-id="84365-145">1</span></span>   | <span data-ttu-id="84365-146">1</span><span class="sxs-lookup"><span data-stu-id="84365-146">1</span></span>    |
| <span data-ttu-id="84365-147">1</span><span class="sxs-lookup"><span data-stu-id="84365-147">1</span></span>   | <span data-ttu-id="84365-148">1</span><span class="sxs-lookup"><span data-stu-id="84365-148">1</span></span>   | <span data-ttu-id="84365-149">1</span><span class="sxs-lookup"><span data-stu-id="84365-149">1</span></span>   | <span data-ttu-id="84365-150">0</span><span class="sxs-lookup"><span data-stu-id="84365-150">0</span></span>    |



 

<span data-ttu-id="84365-151">В следующем списке описаны режимы рисования и логические операции, которые они представляют.</span><span class="sxs-lookup"><span data-stu-id="84365-151">The following list outlines the drawing modes and the Boolean operations that they represent.</span></span>



| <span data-ttu-id="84365-152">Операция с растровым изображением</span><span class="sxs-lookup"><span data-stu-id="84365-152">Raster operation</span></span> | <span data-ttu-id="84365-153">Логическая операция</span><span class="sxs-lookup"><span data-stu-id="84365-153">Boolean operation</span></span> |
|------------------|-------------------|
| <span data-ttu-id="84365-154">Черный (R2) \_</span><span class="sxs-lookup"><span data-stu-id="84365-154">R2\_BLACK</span></span>        | <span data-ttu-id="84365-155">0</span><span class="sxs-lookup"><span data-stu-id="84365-155">0</span></span>                 |
| <span data-ttu-id="84365-156">\_Копипен R2</span><span class="sxs-lookup"><span data-stu-id="84365-156">R2\_COPYPEN</span></span>      | <span data-ttu-id="84365-157">С</span><span class="sxs-lookup"><span data-stu-id="84365-157">P</span></span>                 |
| <span data-ttu-id="84365-158">\_Маскнотпен R2</span><span class="sxs-lookup"><span data-stu-id="84365-158">R2\_MASKNOTPEN</span></span>   | <span data-ttu-id="84365-159">дпна</span><span class="sxs-lookup"><span data-stu-id="84365-159">DPna</span></span>              |
| <span data-ttu-id="84365-160">\_Маскпен R2</span><span class="sxs-lookup"><span data-stu-id="84365-160">R2\_MASKPEN</span></span>      | <span data-ttu-id="84365-161">DPa</span><span class="sxs-lookup"><span data-stu-id="84365-161">DPa</span></span>               |
| <span data-ttu-id="84365-162">\_Маскпеннот R2</span><span class="sxs-lookup"><span data-stu-id="84365-162">R2\_MASKPENNOT</span></span>   | <span data-ttu-id="84365-163">пдна</span><span class="sxs-lookup"><span data-stu-id="84365-163">PDna</span></span>              |
| <span data-ttu-id="84365-164">\_Мерженотпен R2</span><span class="sxs-lookup"><span data-stu-id="84365-164">R2\_MERGENOTPEN</span></span>  | <span data-ttu-id="84365-165">дпно</span><span class="sxs-lookup"><span data-stu-id="84365-165">DPno</span></span>              |
| <span data-ttu-id="84365-166">\_Мержепен R2</span><span class="sxs-lookup"><span data-stu-id="84365-166">R2\_MERGEPEN</span></span>     | <span data-ttu-id="84365-167">дпо</span><span class="sxs-lookup"><span data-stu-id="84365-167">DPo</span></span>               |
| <span data-ttu-id="84365-168">\_Мержепеннот R2</span><span class="sxs-lookup"><span data-stu-id="84365-168">R2\_MERGEPENNOT</span></span>  | <span data-ttu-id="84365-169">пдно</span><span class="sxs-lookup"><span data-stu-id="84365-169">PDno</span></span>              |
| <span data-ttu-id="84365-170">\_NOP R2</span><span class="sxs-lookup"><span data-stu-id="84365-170">R2\_NOP</span></span>          | <span data-ttu-id="84365-171">D</span><span class="sxs-lookup"><span data-stu-id="84365-171">D</span></span>                 |
| <span data-ttu-id="84365-172">R2 \_ не</span><span class="sxs-lookup"><span data-stu-id="84365-172">R2\_NOT</span></span>          | <span data-ttu-id="84365-173">DN</span><span class="sxs-lookup"><span data-stu-id="84365-173">Dn</span></span>                |
| <span data-ttu-id="84365-174">\_Ноткопипен R2</span><span class="sxs-lookup"><span data-stu-id="84365-174">R2\_NOTCOPYPEN</span></span>   | <span data-ttu-id="84365-175">PN</span><span class="sxs-lookup"><span data-stu-id="84365-175">Pn</span></span>                |
| <span data-ttu-id="84365-176">\_Нотмаскпен R2</span><span class="sxs-lookup"><span data-stu-id="84365-176">R2\_NOTMASKPEN</span></span>   | <span data-ttu-id="84365-177">дпан</span><span class="sxs-lookup"><span data-stu-id="84365-177">DPan</span></span>              |
| <span data-ttu-id="84365-178">\_Нотмержепен R2</span><span class="sxs-lookup"><span data-stu-id="84365-178">R2\_NOTMERGEPEN</span></span>  | <span data-ttu-id="84365-179">дпон</span><span class="sxs-lookup"><span data-stu-id="84365-179">DPon</span></span>              |
| <span data-ttu-id="84365-180">\_Нотксорпен R2</span><span class="sxs-lookup"><span data-stu-id="84365-180">R2\_NOTXORPEN</span></span>    | <span data-ttu-id="84365-181">дпксн</span><span class="sxs-lookup"><span data-stu-id="84365-181">DPxn</span></span>              |
| <span data-ttu-id="84365-182">Белая, R2 \_</span><span class="sxs-lookup"><span data-stu-id="84365-182">R2\_WHITE</span></span>        | <span data-ttu-id="84365-183">1</span><span class="sxs-lookup"><span data-stu-id="84365-183">1</span></span>                 |
| <span data-ttu-id="84365-184">\_Ксорпен R2</span><span class="sxs-lookup"><span data-stu-id="84365-184">R2\_XORPEN</span></span>       | <span data-ttu-id="84365-185">дпкс</span><span class="sxs-lookup"><span data-stu-id="84365-185">DPx</span></span>               |



 

<span data-ttu-id="84365-186">Для устройства с монохромным интерфейсом GDI сопоставляет нулевое значение черному, а значение от 1 до белого.</span><span class="sxs-lookup"><span data-stu-id="84365-186">For a monochrome device, GDI maps the value zero to black and the value 1 to white.</span></span> <span data-ttu-id="84365-187">Если приложение пытается рисовать с помощью черного пера в белом месте назначения с использованием доступных двоичных растровых операций, выполняются следующие результаты.</span><span class="sxs-lookup"><span data-stu-id="84365-187">If an application attempts to draw with a black pen on a white destination by using the available binary raster operations, the following results occur.</span></span>



| <span data-ttu-id="84365-188">Операция с растровым изображением</span><span class="sxs-lookup"><span data-stu-id="84365-188">Raster operation</span></span> | <span data-ttu-id="84365-189">Результат</span><span class="sxs-lookup"><span data-stu-id="84365-189">Result</span></span>             |
|------------------|--------------------|
| <span data-ttu-id="84365-190">Черный (R2) \_</span><span class="sxs-lookup"><span data-stu-id="84365-190">R2\_BLACK</span></span>        | <span data-ttu-id="84365-191">Видимая черная линия</span><span class="sxs-lookup"><span data-stu-id="84365-191">Visible black line</span></span> |
| <span data-ttu-id="84365-192">\_Копипен R2</span><span class="sxs-lookup"><span data-stu-id="84365-192">R2\_COPYPEN</span></span>      | <span data-ttu-id="84365-193">Видимая черная линия</span><span class="sxs-lookup"><span data-stu-id="84365-193">Visible black line</span></span> |
| <span data-ttu-id="84365-194">\_Маскнотпен R2</span><span class="sxs-lookup"><span data-stu-id="84365-194">R2\_MASKNOTPEN</span></span>   | <span data-ttu-id="84365-195">Нет видимой строки</span><span class="sxs-lookup"><span data-stu-id="84365-195">No visible line</span></span>    |
| <span data-ttu-id="84365-196">\_Маскпен R2</span><span class="sxs-lookup"><span data-stu-id="84365-196">R2\_MASKPEN</span></span>      | <span data-ttu-id="84365-197">Видимая черная линия</span><span class="sxs-lookup"><span data-stu-id="84365-197">Visible black line</span></span> |
| <span data-ttu-id="84365-198">\_Маскпеннот R2</span><span class="sxs-lookup"><span data-stu-id="84365-198">R2\_MASKPENNOT</span></span>   | <span data-ttu-id="84365-199">Видимая черная линия</span><span class="sxs-lookup"><span data-stu-id="84365-199">Visible black line</span></span> |
| <span data-ttu-id="84365-200">\_Мерженотпен R2</span><span class="sxs-lookup"><span data-stu-id="84365-200">R2\_MERGENOTPEN</span></span>  | <span data-ttu-id="84365-201">Нет видимой строки</span><span class="sxs-lookup"><span data-stu-id="84365-201">No visible line</span></span>    |
| <span data-ttu-id="84365-202">\_Мержепен R2</span><span class="sxs-lookup"><span data-stu-id="84365-202">R2\_MERGEPEN</span></span>     | <span data-ttu-id="84365-203">Видимая черная линия</span><span class="sxs-lookup"><span data-stu-id="84365-203">Visible black line</span></span> |
| <span data-ttu-id="84365-204">\_Мержепеннот R2</span><span class="sxs-lookup"><span data-stu-id="84365-204">R2\_MERGEPENNOT</span></span>  | <span data-ttu-id="84365-205">Видимая черная линия</span><span class="sxs-lookup"><span data-stu-id="84365-205">Visible black line</span></span> |
| <span data-ttu-id="84365-206">\_NOP R2</span><span class="sxs-lookup"><span data-stu-id="84365-206">R2\_NOP</span></span>          | <span data-ttu-id="84365-207">Нет видимой строки</span><span class="sxs-lookup"><span data-stu-id="84365-207">No visible line</span></span>    |
| <span data-ttu-id="84365-208">R2 \_ не</span><span class="sxs-lookup"><span data-stu-id="84365-208">R2\_NOT</span></span>          | <span data-ttu-id="84365-209">Видимая черная линия</span><span class="sxs-lookup"><span data-stu-id="84365-209">Visible black line</span></span> |
| <span data-ttu-id="84365-210">\_Ноткопипен R2</span><span class="sxs-lookup"><span data-stu-id="84365-210">R2\_NOTCOPYPEN</span></span>   | <span data-ttu-id="84365-211">Нет видимой строки</span><span class="sxs-lookup"><span data-stu-id="84365-211">No visible line</span></span>    |
| <span data-ttu-id="84365-212">\_Нотмаскпен R2</span><span class="sxs-lookup"><span data-stu-id="84365-212">R2\_NOTMASKPEN</span></span>   | <span data-ttu-id="84365-213">Нет видимой строки</span><span class="sxs-lookup"><span data-stu-id="84365-213">No visible line</span></span>    |
| <span data-ttu-id="84365-214">\_Нотмержепен R2</span><span class="sxs-lookup"><span data-stu-id="84365-214">R2\_NOTMERGEPEN</span></span>  | <span data-ttu-id="84365-215">Видимая черная линия</span><span class="sxs-lookup"><span data-stu-id="84365-215">Visible black line</span></span> |
| <span data-ttu-id="84365-216">\_Нотксорпен R2</span><span class="sxs-lookup"><span data-stu-id="84365-216">R2\_NOTXORPEN</span></span>    | <span data-ttu-id="84365-217">Видимая черная линия</span><span class="sxs-lookup"><span data-stu-id="84365-217">Visible black line</span></span> |
| <span data-ttu-id="84365-218">Белая, R2 \_</span><span class="sxs-lookup"><span data-stu-id="84365-218">R2\_WHITE</span></span>        | <span data-ttu-id="84365-219">Нет видимой строки</span><span class="sxs-lookup"><span data-stu-id="84365-219">No visible line</span></span>    |
| <span data-ttu-id="84365-220">\_Ксорпен R2</span><span class="sxs-lookup"><span data-stu-id="84365-220">R2\_XORPEN</span></span>       | <span data-ttu-id="84365-221">Нет видимой строки</span><span class="sxs-lookup"><span data-stu-id="84365-221">No visible line</span></span>    |



 

<span data-ttu-id="84365-222">Для цветового устройства GDI использует значения RGB для представления цветов пера и места назначения.</span><span class="sxs-lookup"><span data-stu-id="84365-222">For a color device, GDI uses RGB values to represent the colors of the pen and the destination.</span></span> <span data-ttu-id="84365-223">Значение цвета RGB — это длинное целое число, содержащее красный, зеленый и синий цвет, каждый из которых задает интенсивность заданного цвета.</span><span class="sxs-lookup"><span data-stu-id="84365-223">An RGB color value is a long integer that contains a red, a green, and a blue color field, each specifying the intensity of the specified color.</span></span> <span data-ttu-id="84365-224">Интенситиес в диапазоне от 0 до 255.</span><span class="sxs-lookup"><span data-stu-id="84365-224">Intensities range from 0 through 255.</span></span> <span data-ttu-id="84365-225">Значения упаковываются в три младших байта длинного целого числа.</span><span class="sxs-lookup"><span data-stu-id="84365-225">The values are packed in the three low-order bytes of the long integer.</span></span> <span data-ttu-id="84365-226">Цвет пера всегда является сплошным цветом, но цвет назначения может быть сочетанием любого из двух или трех цветов.</span><span class="sxs-lookup"><span data-stu-id="84365-226">The color of a pen is always a solid color, but the color of the destination may be a mixture of any two or three colors.</span></span> <span data-ttu-id="84365-227">Если приложение пытается рисовать с помощью белого пера на синем месте, используя доступные двоичные растровые операции, выполняются следующие результаты.</span><span class="sxs-lookup"><span data-stu-id="84365-227">If an application attempts to draw with a white pen on a blue destination by using the available binary raster operations, the following results occur.</span></span>



| <span data-ttu-id="84365-228">Операция с растровым изображением</span><span class="sxs-lookup"><span data-stu-id="84365-228">Raster operation</span></span> | <span data-ttu-id="84365-229">Результат</span><span class="sxs-lookup"><span data-stu-id="84365-229">Result</span></span>                 |
|------------------|------------------------|
| <span data-ttu-id="84365-230">Черный (R2) \_</span><span class="sxs-lookup"><span data-stu-id="84365-230">R2\_BLACK</span></span>        | <span data-ttu-id="84365-231">Видимая черная линия</span><span class="sxs-lookup"><span data-stu-id="84365-231">Visible black line</span></span>     |
| <span data-ttu-id="84365-232">\_Копипен R2</span><span class="sxs-lookup"><span data-stu-id="84365-232">R2\_COPYPEN</span></span>      | <span data-ttu-id="84365-233">Видимая белая линия</span><span class="sxs-lookup"><span data-stu-id="84365-233">Visible white line</span></span>     |
| <span data-ttu-id="84365-234">\_Маскнотпен R2</span><span class="sxs-lookup"><span data-stu-id="84365-234">R2\_MASKNOTPEN</span></span>   | <span data-ttu-id="84365-235">Видимая черная линия</span><span class="sxs-lookup"><span data-stu-id="84365-235">Visible black line</span></span>     |
| <span data-ttu-id="84365-236">\_Маскпен R2</span><span class="sxs-lookup"><span data-stu-id="84365-236">R2\_MASKPEN</span></span>      | <span data-ttu-id="84365-237">Невидимая синяя линия</span><span class="sxs-lookup"><span data-stu-id="84365-237">Invisible blue line</span></span>    |
| <span data-ttu-id="84365-238">\_Маскпеннот R2</span><span class="sxs-lookup"><span data-stu-id="84365-238">R2\_MASKPENNOT</span></span>   | <span data-ttu-id="84365-239">Видимая красная/зеленая линия</span><span class="sxs-lookup"><span data-stu-id="84365-239">Visible red/green line</span></span> |
| <span data-ttu-id="84365-240">\_Мерженотпен R2</span><span class="sxs-lookup"><span data-stu-id="84365-240">R2\_MERGENOTPEN</span></span>  | <span data-ttu-id="84365-241">Невидимая синяя линия</span><span class="sxs-lookup"><span data-stu-id="84365-241">Invisible blue line</span></span>    |
| <span data-ttu-id="84365-242">\_Мержепен R2</span><span class="sxs-lookup"><span data-stu-id="84365-242">R2\_MERGEPEN</span></span>     | <span data-ttu-id="84365-243">Видимая белая линия</span><span class="sxs-lookup"><span data-stu-id="84365-243">Visible white line</span></span>     |
| <span data-ttu-id="84365-244">\_Мержепеннот R2</span><span class="sxs-lookup"><span data-stu-id="84365-244">R2\_MERGEPENNOT</span></span>  | <span data-ttu-id="84365-245">Видимая белая линия</span><span class="sxs-lookup"><span data-stu-id="84365-245">Visible white line</span></span>     |
| <span data-ttu-id="84365-246">\_NOP R2</span><span class="sxs-lookup"><span data-stu-id="84365-246">R2\_NOP</span></span>          | <span data-ttu-id="84365-247">Невидимая синяя линия</span><span class="sxs-lookup"><span data-stu-id="84365-247">Invisible blue line</span></span>    |
| <span data-ttu-id="84365-248">R2 \_ не</span><span class="sxs-lookup"><span data-stu-id="84365-248">R2\_NOT</span></span>          | <span data-ttu-id="84365-249">Видимая красная/зеленая линия</span><span class="sxs-lookup"><span data-stu-id="84365-249">Visible red/green line</span></span> |
| <span data-ttu-id="84365-250">\_Ноткопипен R2</span><span class="sxs-lookup"><span data-stu-id="84365-250">R2\_NOTCOPYPEN</span></span>   | <span data-ttu-id="84365-251">Видимая черная линия</span><span class="sxs-lookup"><span data-stu-id="84365-251">Visible black line</span></span>     |
| <span data-ttu-id="84365-252">\_Нотмаскпен R2</span><span class="sxs-lookup"><span data-stu-id="84365-252">R2\_NOTMASKPEN</span></span>   | <span data-ttu-id="84365-253">Видимая красная/зеленая линия</span><span class="sxs-lookup"><span data-stu-id="84365-253">Visible red/green line</span></span> |
| <span data-ttu-id="84365-254">\_Нотмержепен R2</span><span class="sxs-lookup"><span data-stu-id="84365-254">R2\_NOTMERGEPEN</span></span>  | <span data-ttu-id="84365-255">Видимая черная линия</span><span class="sxs-lookup"><span data-stu-id="84365-255">Visible black line</span></span>     |
| <span data-ttu-id="84365-256">\_Нотксорпен R2</span><span class="sxs-lookup"><span data-stu-id="84365-256">R2\_NOTXORPEN</span></span>    | <span data-ttu-id="84365-257">Невидимая синяя линия</span><span class="sxs-lookup"><span data-stu-id="84365-257">Invisible blue line</span></span>    |
| <span data-ttu-id="84365-258">Белая, R2 \_</span><span class="sxs-lookup"><span data-stu-id="84365-258">R2\_WHITE</span></span>        | <span data-ttu-id="84365-259">Видимая белая линия</span><span class="sxs-lookup"><span data-stu-id="84365-259">Visible white line</span></span>     |
| <span data-ttu-id="84365-260">\_Ксорпен R2</span><span class="sxs-lookup"><span data-stu-id="84365-260">R2\_XORPEN</span></span>       | <span data-ttu-id="84365-261">Видимая красная/зеленая линия</span><span class="sxs-lookup"><span data-stu-id="84365-261">Visible red/green line</span></span> |



 

 

 



