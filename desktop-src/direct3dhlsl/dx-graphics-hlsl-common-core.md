---
title: Ядро Common-Shader
description: Ядро Common-Shader
ms.assetid: f3cf2969-83a4-461f-8177-d336536194ba
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 66c1f763c4771a8406acd2f3401445d1a29cde79
ms.sourcegitcommit: 7e4322a6ec1f964d5ad26e2e5e06cc8ce840030e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/01/2021
ms.locfileid: "113129721"
---
# <a name="common-shader-core"></a><span data-ttu-id="36178-103">Ядро Common-Shader</span><span class="sxs-lookup"><span data-stu-id="36178-103">Common-Shader Core</span></span>

<span data-ttu-id="36178-104">В модели шейдера 4 каждый этап шейдера реализует одну и ту же базовую функциональность с помощью ядра общего шейдера.</span><span class="sxs-lookup"><span data-stu-id="36178-104">In Shader Model 4, all shader stages implement the same base functionality using a common-shader core.</span></span> <span data-ttu-id="36178-105">Кроме того, каждый из трех этапов шейдера (вершина, геометрия и пиксель) обеспечивает функциональность, уникальную для каждого этапа, например возможность создания новых примитивов на основе шейдера геометрии или для удаления определенного пикселя на этапе шейдера пикселей.</span><span class="sxs-lookup"><span data-stu-id="36178-105">In addition, each of the three shader stages (vertex, geometry, and pixel) offer functionality unique to each stage, such as the ability to generate new primitives from the geometry shader stage or to discard a specific pixel in the pixel shader stage.</span></span> <span data-ttu-id="36178-106">На следующей диаграмме показано, как потоки данных проходят через стадию шейдера, а также отношение ядра общего шейдера с ресурсами памяти шейдера.</span><span class="sxs-lookup"><span data-stu-id="36178-106">The following diagram shows how data flows through a shader stage, and the relationship of the common-shader core with shader memory resources.</span></span>

![Схема потока данных на этапе шейдера](images/d3d10-shader-unit.png)

-   <span data-ttu-id="36178-108">**Входные данные**: шейдер вершин получает свои входные данные с этапа ассемблера ввода; геометрические и пиксельные шейдеры получают свои входные данные с предыдущей стадии шейдера.</span><span class="sxs-lookup"><span data-stu-id="36178-108">**Input Data**: A vertex shader receives its inputs from the input assembler stage; geometry and pixel shaders receive their inputs from the previous shader stage.</span></span> <span data-ttu-id="36178-109">Дополнительные входы включают [семантику "система — значение](dx-graphics-hlsl-semantics.md)", которая используется первой единицей в конвейере, к которой они применимы.</span><span class="sxs-lookup"><span data-stu-id="36178-109">Additional inputs include [system-value semantics](dx-graphics-hlsl-semantics.md), which are consumable by the first unit in the pipeline to which they are applicable.</span></span>
-   <span data-ttu-id="36178-110">**Выходные данные**: шейдеры создают выходные результаты, которые передаются на последующий этап в конвейере.</span><span class="sxs-lookup"><span data-stu-id="36178-110">**Output Data**: Shaders generate output results to be passed onto the subsequent stage in the pipeline.</span></span> <span data-ttu-id="36178-111">Для шейдера Geometry объем выходных данных одного вызова может различаться.</span><span class="sxs-lookup"><span data-stu-id="36178-111">For a geometry shader, the amount of data output from a single invocation can vary.</span></span> <span data-ttu-id="36178-112">Некоторые выходные данные обрабатываются ядром общего шейдера (например, положением вершины и индексом-целевым массивом), а другие предназначены для интерпретации приложением.</span><span class="sxs-lookup"><span data-stu-id="36178-112">Some outputs are interpreted by the common-shader core (such as vertex position and render-target-array index), others are designed to be interpreted by an application.</span></span>
-   <span data-ttu-id="36178-113">**Код шейдера**. шейдеры могут считывать из памяти, выполнять векторные операции с плавающей запятой и целочисленными арифметическими операциями, а также операции управления потоком.</span><span class="sxs-lookup"><span data-stu-id="36178-113">**Shader Code**: Shaders can read from memory, perform vector floating point and integer arithmetic operations, or flow control operations.</span></span> <span data-ttu-id="36178-114">Количество инструкций, которые могут быть реализованы в шейдере, не ограничено.</span><span class="sxs-lookup"><span data-stu-id="36178-114">There is no limit to the number of statements that can be implemented in a shader.</span></span>
-   <span data-ttu-id="36178-115">**Пробы**: пробы определяют, как выдаются образцы и отфильтруются текстуры.</span><span class="sxs-lookup"><span data-stu-id="36178-115">**Samplers**: Samplers define how to sample and filter textures.</span></span> <span data-ttu-id="36178-116">Можно одновременно привязать к шейдеру до 16 проб.</span><span class="sxs-lookup"><span data-stu-id="36178-116">As many as 16 samplers can be bound to a shader simultaneously.</span></span>
-   <span data-ttu-id="36178-117">**Текстуры**. текстуры можно отфильтровать с помощью проб или прочесть на основе шаг текселя непосредственно с помощью встроенной функции [Load](dx-graphics-hlsl-to-load.md) .</span><span class="sxs-lookup"><span data-stu-id="36178-117">**Textures**: Textures can be filtered using samplers or read on a per-texel basis directly with the [load](dx-graphics-hlsl-to-load.md) intrinsic function.</span></span>
-   <span data-ttu-id="36178-118">**Буферы**. буферы никогда не фильтруются, но их можно считывать из памяти в отдельности по элементам непосредственно с помощью встроенной функции [Load](dx-graphics-hlsl-to-load.md) .</span><span class="sxs-lookup"><span data-stu-id="36178-118">**Buffers**: Buffers are never filtered, but can be read from memory on a per-element basis directly with the [load](dx-graphics-hlsl-to-load.md) intrinsic function.</span></span> <span data-ttu-id="36178-119">Столько же, сколько и буферных ресурсов 128, и ресурсы буфера (Объединенные) могут одновременно привязываться к шейдеру.</span><span class="sxs-lookup"><span data-stu-id="36178-119">As many as 128 texture and buffer resources (combined) can be bound to a shader simultaneously.</span></span>
-   <span data-ttu-id="36178-120">**Буферы констант**. буферы констант оптимизированы для переменных констант-шейдеров.</span><span class="sxs-lookup"><span data-stu-id="36178-120">**Constant Buffers**: Constant buffers are optimized for shader constant-variables.</span></span> <span data-ttu-id="36178-121">Так как 16 буферов констант можно привязать к этапу шейдера одновременно.</span><span class="sxs-lookup"><span data-stu-id="36178-121">As many as 16 constant buffers can be bound to a shader stage simultaneously.</span></span> <span data-ttu-id="36178-122">Они предназначены для более частых обновлений ЦП; Поэтому у них есть дополнительные ограничения по размеру, макету и доступу.</span><span class="sxs-lookup"><span data-stu-id="36178-122">They are designed for more frequent update from the CPU; therefore, they have additional size, layout, and access restrictions.</span></span>


<span data-ttu-id="36178-123">Различия между Direct3D 9 и Direct3D 10:</span><span class="sxs-lookup"><span data-stu-id="36178-123">Differences between Direct3D 9 and Direct3D 10:</span></span>

- <span data-ttu-id="36178-124">В Direct3D 9 каждая единица шейдера имела один и небольшой файл регистра констант для хранения всех переменных шейдера констант.</span><span class="sxs-lookup"><span data-stu-id="36178-124">In Direct3D 9, each shader unit had a single, small constant register file to store all constant shader variables.</span></span> <span data-ttu-id="36178-125">Разведение всех шейдеров с ограниченным пространством, необходимым для частого перезапуска констант с помощью ЦП.</span><span class="sxs-lookup"><span data-stu-id="36178-125">Accommodating all shaders with this limited constant space required frequent recycling of constants by the CPU.</span></span>
- <span data-ttu-id="36178-126">В Direct3D 10 константы хранятся в неизменяемых буферах в памяти и управляются как любые другие ресурсы.</span><span class="sxs-lookup"><span data-stu-id="36178-126">In Direct3D 10, constants are stored in immutable buffers in memory and are managed like any other resource.</span></span> <span data-ttu-id="36178-127">Количество буферов констант, которые может создать приложение, не ограничено.</span><span class="sxs-lookup"><span data-stu-id="36178-127">There is no limit to the number of constant buffers an application can create.</span></span> <span data-ttu-id="36178-128">Организуя константы в буферы по частоте обновления и использования, объем пропускной способности, необходимый для обновления констант в соответствии со всеми шейдерами, может значительно снизиться.</span><span class="sxs-lookup"><span data-stu-id="36178-128">By organizing constants into buffers by frequency of update and usage, the amount of bandwidth required to update constants to accommodate all shaders can be significantly reduced.</span></span>



 

## <a name="integer-and-bitwise-support"></a><span data-ttu-id="36178-129">Целочисленная и Побитовая поддержка</span><span class="sxs-lookup"><span data-stu-id="36178-129">Integer and Bitwise Support</span></span>

<span data-ttu-id="36178-130">Общее ядро шейдера предоставляет полный набор стандартных и побитовых операций, 32 соответствующих стандарту IEEE.</span><span class="sxs-lookup"><span data-stu-id="36178-130">The common shader core provides a full set of IEEE-compliant 32-bit integer and bitwise operations.</span></span> <span data-ttu-id="36178-131">Эти операции включают в себя новый класс алгоритмов в примерах графических устройств, включая методы сжатия и упаковки, Ффтс и битовую программу управления потоком.</span><span class="sxs-lookup"><span data-stu-id="36178-131">These operations enable a new class of algorithms in graphics hardware examples include compression and packing techniques, FFTs, and bitfield program-flow control.</span></span>

<span data-ttu-id="36178-132">Типы данных **int** и **uint** в Direct3D 10 HLSL сопоставляются с 32-разрядными целыми числами в оборудовании.</span><span class="sxs-lookup"><span data-stu-id="36178-132">The **int** and **uint** data types in Direct3D 10 HLSL map to 32-bit integers in hardware.</span></span>



|                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36178-133">Различия между Direct3D 9 и Direct3D 10:</span><span class="sxs-lookup"><span data-stu-id="36178-133">Differences between Direct3D 9 and Direct3D 10:</span></span><br/> <span data-ttu-id="36178-134">Входные потоки Direct3D 9, помеченные как целые числа в HLSL, были интерпретированы как операции с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="36178-134">In Direct3D 9 stream inputs marked as integer in HLSL were interpreted as floating-point.</span></span> <span data-ttu-id="36178-135">В Direct3D 10 входные данные потока, помеченные как целые числа, обрабатываются как 32-разрядное целое число.</span><span class="sxs-lookup"><span data-stu-id="36178-135">In Direct3D 10, stream inputs marked as integer are interpreted as a 32- bit integer.</span></span><br/> <span data-ttu-id="36178-136">Кроме того, логические значения теперь задаются все биты или все биты заменяются.</span><span class="sxs-lookup"><span data-stu-id="36178-136">In addition, boolean values are now all bits set or all bits unset.</span></span> <span data-ttu-id="36178-137">Данные, преобразованные в **bool** , будут интерпретироваться как true, если значение не равно 0,0 f (как положительные, так и отрицательные нули могут быть ложными) и false в противном случае.</span><span class="sxs-lookup"><span data-stu-id="36178-137">Data converted to **bool** will be interpreted as true if the value is not equal to 0.0f (both positive and negative zero are allowed to be false) and false otherwise.</span></span><br/> |



 

## <a name="bitwise-operators"></a><span data-ttu-id="36178-138">битовые операторы;</span><span class="sxs-lookup"><span data-stu-id="36178-138">Bitwise operators</span></span>

<span data-ttu-id="36178-139">Общее ядро шейдера поддерживает следующие Побитовые операторы:</span><span class="sxs-lookup"><span data-stu-id="36178-139">The common shader core supports the following bitwise operators:</span></span>



| <span data-ttu-id="36178-140">Оператор</span><span class="sxs-lookup"><span data-stu-id="36178-140">Operator</span></span>  | <span data-ttu-id="36178-141">Функция</span><span class="sxs-lookup"><span data-stu-id="36178-141">Function</span></span>          |
|-----------|-------------------|
| ~         | <span data-ttu-id="36178-142">Логическое не</span><span class="sxs-lookup"><span data-stu-id="36178-142">Logical Not</span></span>       |
| <<  | <span data-ttu-id="36178-143">Сдвиг влево</span><span class="sxs-lookup"><span data-stu-id="36178-143">Left Shift</span></span>        |
| >>  | <span data-ttu-id="36178-144">Сдвиг вправо</span><span class="sxs-lookup"><span data-stu-id="36178-144">Right Shift</span></span>       |
| &         | <span data-ttu-id="36178-145">Логическое «И»</span><span class="sxs-lookup"><span data-stu-id="36178-145">Logical And</span></span>       |
| \|        | <span data-ttu-id="36178-146">Логическое "или".</span><span class="sxs-lookup"><span data-stu-id="36178-146">Logical Or</span></span>        |
| ^         | <span data-ttu-id="36178-147">Логическое исключающее или</span><span class="sxs-lookup"><span data-stu-id="36178-147">Logical Xor</span></span>       |
| <<= | <span data-ttu-id="36178-148">Сдвиг влево равен</span><span class="sxs-lookup"><span data-stu-id="36178-148">Left shift Equal</span></span>  |
| >>= | <span data-ttu-id="36178-149">Сдвиг вправо равно</span><span class="sxs-lookup"><span data-stu-id="36178-149">Right Shift Equal</span></span> |
| &=        | <span data-ttu-id="36178-150">И равно</span><span class="sxs-lookup"><span data-stu-id="36178-150">And Equal</span></span>         |
| \|=       | <span data-ttu-id="36178-151">Или равно</span><span class="sxs-lookup"><span data-stu-id="36178-151">Or Equal</span></span>          |
| ^=        | <span data-ttu-id="36178-152">XOR равно</span><span class="sxs-lookup"><span data-stu-id="36178-152">Xor Equal</span></span>         |



 

<span data-ttu-id="36178-153">Битовые операторы определяются только для типов данных **int** и **uint** .</span><span class="sxs-lookup"><span data-stu-id="36178-153">Bitwise operators are defined to operate only on **int** and **uint** data types.</span></span> <span data-ttu-id="36178-154">Попытка использовать побитовые операторы для типов данных с **плавающей запятой** или **структуры** приведет к ошибке.</span><span class="sxs-lookup"><span data-stu-id="36178-154">Attempting to use bitwise operators on **float** or **struct** data types will result in an error.</span></span> <span data-ttu-id="36178-155">Побитовые операторы имеют тот же приоритет, что и C, в отношении других операторов.</span><span class="sxs-lookup"><span data-stu-id="36178-155">Bitwise operators follow the same precedence as C with regard to other operators.</span></span>

## <a name="binary-casts"></a><span data-ttu-id="36178-156">Двоичные приведения</span><span class="sxs-lookup"><span data-stu-id="36178-156">Binary Casts</span></span>

<span data-ttu-id="36178-157">При приведении между целым числом и типом с плавающей запятой будет преобразовано числовое значение после правил усечения C.</span><span class="sxs-lookup"><span data-stu-id="36178-157">Casting between an integer and a floating-point type will convert the numeric value following C truncation rules.</span></span> <span data-ttu-id="36178-158">Приведение значения с **плавающей запятой** к типу **int** и обратно в тип **float** — это преобразование, зависящее от точности целевого типа данных.</span><span class="sxs-lookup"><span data-stu-id="36178-158">Casting a value from a **float**, to an **int**, and back to a **float** is a lossy conversion dependent on the precision of the target data type.</span></span> <span data-ttu-id="36178-159">Ниже приведены некоторые функции преобразования: [**асфлоат (DirectX HLSL)**](dx-graphics-hlsl-asfloat.md), [**ASIN (DirectX HLSL)**](dx-graphics-hlsl-asint.md), [**асуинт (DirectX HLSL)**](dx-graphics-hlsl-asuint.md).</span><span class="sxs-lookup"><span data-stu-id="36178-159">Here are some of the conversion functions: [**asfloat (DirectX HLSL)**](dx-graphics-hlsl-asfloat.md), [**asint (DirectX HLSL)**](dx-graphics-hlsl-asint.md), [**asuint (DirectX HLSL)**](dx-graphics-hlsl-asuint.md).</span></span>

<span data-ttu-id="36178-160">Двоичные приведения также можно выполнять с помощью встроенных функций HLSL.</span><span class="sxs-lookup"><span data-stu-id="36178-160">Binary casts can also be performed using HLSL intrinsic functions.</span></span> <span data-ttu-id="36178-161">Это приводит к тому, что компилятор переинтерпретирует битовое представление числа в целевой тип данных.</span><span class="sxs-lookup"><span data-stu-id="36178-161">These cause the compiler to reinterpret the bit representation of a number into the target data type.</span></span>

## <a name="related-topics"></a><span data-ttu-id="36178-162">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="36178-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="36178-163">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="36178-163">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 





