---
title: Модификаторы для ps_1_X
description: Модификаторы инструкций влияют на результат инструкции перед его записью в регистр назначения.
ms.assetid: 15b892da-b6fd-4bd5-8889-bc48035e7819
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bbc8a9b13f7ffc29cf84bc839409f29bea6c8c8b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103889195"
---
# <a name="modifiers-for-ps_1_x"></a><span data-ttu-id="0bf88-103">Модификаторы для PS \_ 1 \_ X</span><span class="sxs-lookup"><span data-stu-id="0bf88-103">Modifiers for ps\_1\_X</span></span>

<span data-ttu-id="0bf88-104">Модификаторы инструкций влияют на результат инструкции перед его записью в регистр назначения.</span><span class="sxs-lookup"><span data-stu-id="0bf88-104">Instruction modifiers affect the result of the instruction before it is written into the destination register.</span></span> <span data-ttu-id="0bf88-105">Например, используйте их для умножения или деления результата на множитель двух или для фиксации результата между нулем и единицей.</span><span class="sxs-lookup"><span data-stu-id="0bf88-105">For instance, use them to multiply or divide the result by a factor of two, or to clamp the result between zero and one.</span></span> <span data-ttu-id="0bf88-106">Модификаторы инструкций применяются после выполнения инструкции, но перед записью результата в регистр назначения.</span><span class="sxs-lookup"><span data-stu-id="0bf88-106">Instruction modifiers are applied after the instruction runs but before writing the result to the destination register.</span></span>

<span data-ttu-id="0bf88-107">Ниже показан список модификаторов.</span><span class="sxs-lookup"><span data-stu-id="0bf88-107">A list of the modifiers is shown below.</span></span>



| <span data-ttu-id="0bf88-108">Модификатор</span><span class="sxs-lookup"><span data-stu-id="0bf88-108">Modifier</span></span> | <span data-ttu-id="0bf88-109">Описание</span><span class="sxs-lookup"><span data-stu-id="0bf88-109">Description</span></span>                   | <span data-ttu-id="0bf88-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0bf88-110">Syntax</span></span>           | <span data-ttu-id="0bf88-111">Version</span><span class="sxs-lookup"><span data-stu-id="0bf88-111">Version</span></span> |      |      |      |
|----------|-------------------------------|------------------|---------|------|------|------|
|          |                               |                  | <span data-ttu-id="0bf88-112">1\_1</span><span class="sxs-lookup"><span data-stu-id="0bf88-112">1\_1</span></span>    | <span data-ttu-id="0bf88-113">1\_2</span><span class="sxs-lookup"><span data-stu-id="0bf88-113">1\_2</span></span> | <span data-ttu-id="0bf88-114">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="0bf88-114">1\_3</span></span> | <span data-ttu-id="0bf88-115">1\_4</span><span class="sxs-lookup"><span data-stu-id="0bf88-115">1\_4</span></span> |
| <span data-ttu-id="0bf88-116">\_штук</span><span class="sxs-lookup"><span data-stu-id="0bf88-116">\_x2</span></span>     | <span data-ttu-id="0bf88-117">Умножить на 2</span><span class="sxs-lookup"><span data-stu-id="0bf88-117">Multiply by 2</span></span>                 | <span data-ttu-id="0bf88-118">Инструкция \_ x2</span><span class="sxs-lookup"><span data-stu-id="0bf88-118">instruction\_x2</span></span>  | <span data-ttu-id="0bf88-119">X</span><span class="sxs-lookup"><span data-stu-id="0bf88-119">X</span></span>       | <span data-ttu-id="0bf88-120">X</span><span class="sxs-lookup"><span data-stu-id="0bf88-120">X</span></span>    | <span data-ttu-id="0bf88-121">X</span><span class="sxs-lookup"><span data-stu-id="0bf88-121">X</span></span>    | <span data-ttu-id="0bf88-122">X</span><span class="sxs-lookup"><span data-stu-id="0bf88-122">X</span></span>    |
| <span data-ttu-id="0bf88-123">\_X4</span><span class="sxs-lookup"><span data-stu-id="0bf88-123">\_x4</span></span>     | <span data-ttu-id="0bf88-124">Умножить на 4</span><span class="sxs-lookup"><span data-stu-id="0bf88-124">Multiply by 4</span></span>                 | <span data-ttu-id="0bf88-125">Инструкция \_ X4</span><span class="sxs-lookup"><span data-stu-id="0bf88-125">instruction\_x4</span></span>  | <span data-ttu-id="0bf88-126">X</span><span class="sxs-lookup"><span data-stu-id="0bf88-126">X</span></span>       | <span data-ttu-id="0bf88-127">X</span><span class="sxs-lookup"><span data-stu-id="0bf88-127">X</span></span>    | <span data-ttu-id="0bf88-128">X</span><span class="sxs-lookup"><span data-stu-id="0bf88-128">X</span></span>    | <span data-ttu-id="0bf88-129">X</span><span class="sxs-lookup"><span data-stu-id="0bf88-129">X</span></span>    |
| <span data-ttu-id="0bf88-130">\_скорости</span><span class="sxs-lookup"><span data-stu-id="0bf88-130">\_x8</span></span>     | <span data-ttu-id="0bf88-131">Умножить на 8</span><span class="sxs-lookup"><span data-stu-id="0bf88-131">Multiply by 8</span></span>                 | <span data-ttu-id="0bf88-132">Инструкция \_ x8</span><span class="sxs-lookup"><span data-stu-id="0bf88-132">instruction\_x8</span></span>  |         |      |      | <span data-ttu-id="0bf88-133">X</span><span class="sxs-lookup"><span data-stu-id="0bf88-133">X</span></span>    |
| <span data-ttu-id="0bf88-134">\_D2</span><span class="sxs-lookup"><span data-stu-id="0bf88-134">\_d2</span></span>     | <span data-ttu-id="0bf88-135">Разделить на 2</span><span class="sxs-lookup"><span data-stu-id="0bf88-135">Divide by 2</span></span>                   | <span data-ttu-id="0bf88-136">Инструкция \_ D2</span><span class="sxs-lookup"><span data-stu-id="0bf88-136">instruction\_d2</span></span>  | <span data-ttu-id="0bf88-137">X</span><span class="sxs-lookup"><span data-stu-id="0bf88-137">X</span></span>       | <span data-ttu-id="0bf88-138">X</span><span class="sxs-lookup"><span data-stu-id="0bf88-138">X</span></span>    | <span data-ttu-id="0bf88-139">X</span><span class="sxs-lookup"><span data-stu-id="0bf88-139">X</span></span>    | <span data-ttu-id="0bf88-140">X</span><span class="sxs-lookup"><span data-stu-id="0bf88-140">X</span></span>    |
| <span data-ttu-id="0bf88-141">\_D4</span><span class="sxs-lookup"><span data-stu-id="0bf88-141">\_d4</span></span>     | <span data-ttu-id="0bf88-142">Разделить на 4</span><span class="sxs-lookup"><span data-stu-id="0bf88-142">Divide by 4</span></span>                   | <span data-ttu-id="0bf88-143">Инструкция \_ D4</span><span class="sxs-lookup"><span data-stu-id="0bf88-143">instruction\_d4</span></span>  |         |      |      | <span data-ttu-id="0bf88-144">X</span><span class="sxs-lookup"><span data-stu-id="0bf88-144">X</span></span>    |
| <span data-ttu-id="0bf88-145">\_D8</span><span class="sxs-lookup"><span data-stu-id="0bf88-145">\_d8</span></span>     | <span data-ttu-id="0bf88-146">Разделить на 8</span><span class="sxs-lookup"><span data-stu-id="0bf88-146">Divide by 8</span></span>                   | <span data-ttu-id="0bf88-147">Инструкция \_ D8</span><span class="sxs-lookup"><span data-stu-id="0bf88-147">instruction\_d8</span></span>  |         |      |      | <span data-ttu-id="0bf88-148">X</span><span class="sxs-lookup"><span data-stu-id="0bf88-148">X</span></span>    |
| <span data-ttu-id="0bf88-149">\_Кот</span><span class="sxs-lookup"><span data-stu-id="0bf88-149">\_sat</span></span>    | <span data-ttu-id="0bf88-150">Насыщенность (срез от 0 до 1)</span><span class="sxs-lookup"><span data-stu-id="0bf88-150">Saturate (clamp from 0 and 1)</span></span> | <span data-ttu-id="0bf88-151">Инструкция \_ Кот</span><span class="sxs-lookup"><span data-stu-id="0bf88-151">instruction\_sat</span></span> | <span data-ttu-id="0bf88-152">X</span><span class="sxs-lookup"><span data-stu-id="0bf88-152">X</span></span>       | <span data-ttu-id="0bf88-153">X</span><span class="sxs-lookup"><span data-stu-id="0bf88-153">X</span></span>    | <span data-ttu-id="0bf88-154">X</span><span class="sxs-lookup"><span data-stu-id="0bf88-154">X</span></span>    | <span data-ttu-id="0bf88-155">X</span><span class="sxs-lookup"><span data-stu-id="0bf88-155">X</span></span>    |



 

-   <span data-ttu-id="0bf88-156">Модификатор перемножения умножает данные регистров на степень двух после считывания.</span><span class="sxs-lookup"><span data-stu-id="0bf88-156">The multiply modifier multiplies the register data by a power of two after it is read.</span></span> <span data-ttu-id="0bf88-157">Это то же самое, что и сдвиг влево.</span><span class="sxs-lookup"><span data-stu-id="0bf88-157">This is the same as a shift left.</span></span>
-   <span data-ttu-id="0bf88-158">Модификатор деления делит данные регистров на степень двух после считывания.</span><span class="sxs-lookup"><span data-stu-id="0bf88-158">The divide modifier divides the register data by a power of two after it is read.</span></span> <span data-ttu-id="0bf88-159">Это то же самое, что и право сдвига вправо.</span><span class="sxs-lookup"><span data-stu-id="0bf88-159">This is the same as a shift right.</span></span>
-   <span data-ttu-id="0bf88-160">Модификатор «насыщенность» служит для фиксации диапазона значений регистров от нуля до одного.</span><span class="sxs-lookup"><span data-stu-id="0bf88-160">The saturate modifier clamps the range of register values from zero to one.</span></span>

<span data-ttu-id="0bf88-161">В арифметических инструкциях можно использовать модификаторы инструкций.</span><span class="sxs-lookup"><span data-stu-id="0bf88-161">Instruction modifiers can be used on arithmetic instructions.</span></span> <span data-ttu-id="0bf88-162">Они не могут использоваться в инструкциях по адресам текстур.</span><span class="sxs-lookup"><span data-stu-id="0bf88-162">They may not be used on texture address instructions.</span></span>

<span data-ttu-id="0bf88-163">Модификатор умножения</span><span class="sxs-lookup"><span data-stu-id="0bf88-163">Multiply modifier</span></span>

<span data-ttu-id="0bf88-164">В этом примере загружается регистр назначения (dest) с суммой двух цветов в исходных операндах (src0 и src1) и результат умножается на два.</span><span class="sxs-lookup"><span data-stu-id="0bf88-164">This example loads the destination register (dest) with the sum of the two colors in the source operands (src0 and src1) and multiplies the result by two.</span></span>


```
add_x2 dest, src0, src1
```



<span data-ttu-id="0bf88-165">В этом примере объединяются два модификатора инструкции.</span><span class="sxs-lookup"><span data-stu-id="0bf88-165">This example combines two instruction modifiers.</span></span> <span data-ttu-id="0bf88-166">Во-первых, добавляются два цвета в исходных операндах (src0 и src1).</span><span class="sxs-lookup"><span data-stu-id="0bf88-166">First, two colors in the source operands (src0 and src1) are added.</span></span> <span data-ttu-id="0bf88-167">Затем результат умножается на два, а между 0,0 — 1,0 для каждого компонента.</span><span class="sxs-lookup"><span data-stu-id="0bf88-167">The result is then multiplied by two, and clamped between 0.0 to 1.0 for each component.</span></span> <span data-ttu-id="0bf88-168">Результат сохраняется в реестре назначения.</span><span class="sxs-lookup"><span data-stu-id="0bf88-168">The result is saved in the destination register.</span></span>


```
add_x2_sat dest, src0, src1
```



<span data-ttu-id="0bf88-169">Модификатор деления</span><span class="sxs-lookup"><span data-stu-id="0bf88-169">Divide modifier</span></span>

<span data-ttu-id="0bf88-170">В этом примере загружается регистр назначения (dest) с суммой двух цветов в исходных операндах (src0 и src1) и делит результат на два.</span><span class="sxs-lookup"><span data-stu-id="0bf88-170">This example loads the destination register (dest) with the sum of the two colors in the source operands (src0 and src1) and divides the result by two.</span></span>


```
add_d2 dest, src0, src1
```



<span data-ttu-id="0bf88-171">Модификатор насыщенности</span><span class="sxs-lookup"><span data-stu-id="0bf88-171">Saturate modifier</span></span>

<span data-ttu-id="0bf88-172">Для арифметических инструкций модификатор насыщенности преобразует результат этой инструкции в диапазон от 0,0 до 1,0 для каждого компонента.</span><span class="sxs-lookup"><span data-stu-id="0bf88-172">For arithmetic instructions, the saturation modifier clamps the result of this instruction into the range 0.0 to 1.0 for each component.</span></span> <span data-ttu-id="0bf88-173">В следующем примере показано, как использовать этот модификатор инструкции.</span><span class="sxs-lookup"><span data-stu-id="0bf88-173">The following example shows how to use this instruction modifier.</span></span>


```
dp3_sat r0, t0_bx2, v0_bx2    ; t0 is bump, v0 is light direction
```



<span data-ttu-id="0bf88-174">Эта операция выполняется после любого модификатора инструкции умножения или деления.</span><span class="sxs-lookup"><span data-stu-id="0bf88-174">This operation occurs after any multiply or divide instruction modifier.</span></span> <span data-ttu-id="0bf88-175">\_почти чаще всего используется для фиксации результатов продукта в виде точки.</span><span class="sxs-lookup"><span data-stu-id="0bf88-175">\_sat is most often used to clamp dot product results.</span></span> <span data-ttu-id="0bf88-176">Однако он также обеспечивает последовательную эмуляцию многопроходных методов, где буфер фрейма всегда находится в диапазоне от 0 до 1, а также синтаксиса многотекстуры DirectX 6 и 7,0, в котором насыщенность определяется на каждом этапе.</span><span class="sxs-lookup"><span data-stu-id="0bf88-176">However, it also enables consistent emulation of multipass methods where the frame buffer is always in the range 0 to 1, and of DirectX 6 and 7.0 multitexture syntax, in which saturation is defined to occur at every stage.</span></span>

<span data-ttu-id="0bf88-177">В этом примере загружается регистр назначения (dest) с суммой двух цветов в исходных операндах (src0 и src1) и выполняется фиксация результата в диапазоне от 0,0 до 1,0 для каждого компонента.</span><span class="sxs-lookup"><span data-stu-id="0bf88-177">This example loads the destination register (dest) with the sum of the two colors in the source operands (src0 and src1), and clamps the result into the range 0.0 to 1.0 for each component.</span></span>


```
add_sat dest, src0, src1
```



<span data-ttu-id="0bf88-178">В этом примере объединяются два модификатора инструкции.</span><span class="sxs-lookup"><span data-stu-id="0bf88-178">This example combines two instruction modifiers.</span></span> <span data-ttu-id="0bf88-179">Во-первых, добавляются два цвета в исходных операндах (src0 и src1).</span><span class="sxs-lookup"><span data-stu-id="0bf88-179">First, two colors in the source operands (src0 and src1) are added.</span></span> <span data-ttu-id="0bf88-180">Результат умножается на два и обменяются в диапазоне от 0,0 до 1,0 для каждого компонента.</span><span class="sxs-lookup"><span data-stu-id="0bf88-180">The result is multiplied by two and clamped between 0.0 to 1.0 for each component.</span></span> <span data-ttu-id="0bf88-181">Результат сохраняется в реестре назначения.</span><span class="sxs-lookup"><span data-stu-id="0bf88-181">The result is saved in the destination register.</span></span>


```
add_x2_sat dest, src0, src1
```



## <a name="related-topics"></a><span data-ttu-id="0bf88-182">См. также</span><span class="sxs-lookup"><span data-stu-id="0bf88-182">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0bf88-183">Инструкции шейдера пикселей</span><span class="sxs-lookup"><span data-stu-id="0bf88-183">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




