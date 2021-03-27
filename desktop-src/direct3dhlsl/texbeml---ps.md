---
title: тексбемл-PS
description: Применение имитации предельного преобразования схемы окружения с коррекцией светимости. Это достигается путем изменения данных адреса текстуры в регистре назначения с использованием данных адреса пертурбатион (du, DV), матрицы среды 2D-выпуклости и освещенности.
ms.assetid: 345a0b77-8d4e-4a0b-a31a-1153f8cb5961
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d97877c67970f43a995fcfbe21d9aead2d792e09
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103987835"
---
# <a name="texbeml---ps"></a><span data-ttu-id="222db-104">тексбемл-PS</span><span class="sxs-lookup"><span data-stu-id="222db-104">texbeml - ps</span></span>

<span data-ttu-id="222db-105">Применение имитации предельного преобразования схемы окружения с коррекцией светимости.</span><span class="sxs-lookup"><span data-stu-id="222db-105">Apply a fake bump environment-map transform with luminance correction.</span></span> <span data-ttu-id="222db-106">Это достигается путем изменения данных адреса текстуры в регистре назначения с использованием данных адреса пертурбатион (du, DV), матрицы среды 2D-выпуклости и освещенности.</span><span class="sxs-lookup"><span data-stu-id="222db-106">This is accomplished by modifying the texture address data of the destination register, using address perturbation data (du,dv), a 2D bump environment matrix, and luminance.</span></span>

## <a name="syntax"></a><span data-ttu-id="222db-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="222db-107">Syntax</span></span>



| <span data-ttu-id="222db-108">тексбемл DST, src</span><span class="sxs-lookup"><span data-stu-id="222db-108">texbeml dst, src</span></span> |
|------------------|



 

<span data-ttu-id="222db-109">где</span><span class="sxs-lookup"><span data-stu-id="222db-109">where</span></span>

-   <span data-ttu-id="222db-110">DST — это регистр назначения.</span><span class="sxs-lookup"><span data-stu-id="222db-110">dst is the destination register.</span></span>
-   <span data-ttu-id="222db-111">src является исходным регистром.</span><span class="sxs-lookup"><span data-stu-id="222db-111">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="222db-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="222db-112">Remarks</span></span>



| <span data-ttu-id="222db-113">Версии шейдеров пикселей</span><span class="sxs-lookup"><span data-stu-id="222db-113">Pixel shader versions</span></span> | <span data-ttu-id="222db-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="222db-114">1\_1</span></span> | <span data-ttu-id="222db-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="222db-115">1\_2</span></span> | <span data-ttu-id="222db-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="222db-116">1\_3</span></span> | <span data-ttu-id="222db-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="222db-117">1\_4</span></span> | <span data-ttu-id="222db-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="222db-118">2\_0</span></span> | <span data-ttu-id="222db-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="222db-119">2\_x</span></span> | <span data-ttu-id="222db-120">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="222db-120">2\_sw</span></span> | <span data-ttu-id="222db-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="222db-121">3\_0</span></span> | <span data-ttu-id="222db-122">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="222db-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="222db-123">тексбемл</span><span class="sxs-lookup"><span data-stu-id="222db-123">texbeml</span></span>               | <span data-ttu-id="222db-124">x</span><span class="sxs-lookup"><span data-stu-id="222db-124">x</span></span>    | <span data-ttu-id="222db-125">x</span><span class="sxs-lookup"><span data-stu-id="222db-125">x</span></span>    | <span data-ttu-id="222db-126">x</span><span class="sxs-lookup"><span data-stu-id="222db-126">x</span></span>    |      |      |      |       |      |       |



 

<span data-ttu-id="222db-127">Красный и зеленый цветовые данные в регистре src интерпретируется как данные пертурбатион (du, DV).</span><span class="sxs-lookup"><span data-stu-id="222db-127">The red and green color data in the src register is interpreted as the perturbation data (du,dv).</span></span> <span data-ttu-id="222db-128">Синий цвет данных в регистре src интерпретируется как данные светимости.</span><span class="sxs-lookup"><span data-stu-id="222db-128">The blue color data in the src register is interpreted as the luminance data.</span></span>

<span data-ttu-id="222db-129">Эта инструкция преобразует красные и зеленые компоненты в исходном регистре с помощью матрицы сопоставления среды 2D-выпуклости.</span><span class="sxs-lookup"><span data-stu-id="222db-129">This instruction transforms the red and green components in the source register using the 2D bump environment mapping matrix.</span></span> <span data-ttu-id="222db-130">Результат добавляется в набор координат текстуры, соответствующий номеру регистра назначения.</span><span class="sxs-lookup"><span data-stu-id="222db-130">The result is added to the texture coordinate set corresponding to the destination register number.</span></span> <span data-ttu-id="222db-131">Корректировка светимости применяется с использованием значений светимости и этапа текстуры смещения.</span><span class="sxs-lookup"><span data-stu-id="222db-131">A luminance correction is applied using the luminance value and the bias texture stage values.</span></span> <span data-ttu-id="222db-132">Результат используется для выборки текущей стадии текстуры.</span><span class="sxs-lookup"><span data-stu-id="222db-132">The result is used to sample the current texture stage.</span></span>

<span data-ttu-id="222db-133">Это можно использовать для различных методов, основанных на пертурбатионах адресов, таких как имитация сопоставления среды на пиксель.</span><span class="sxs-lookup"><span data-stu-id="222db-133">This can be used for a variety of techniques based on address perturbation such as fake per-pixel environment mapping.</span></span>

<span data-ttu-id="222db-134">Эта операция всегда интерпретирует du и DV как количество со знаком.</span><span class="sxs-lookup"><span data-stu-id="222db-134">This operation always interprets du and dv as signed quantities.</span></span> <span data-ttu-id="222db-135">Для версий 1 \_ 0 и 1 \_ 1 в входном аргументе не разрешается использовать модификатор input для [масштабирования со знаком "Source Register](dx9-graphics-reference-asm-ps-registers-modifiers-signed-scale.md) " ( \_ bx2).</span><span class="sxs-lookup"><span data-stu-id="222db-135">For versions 1\_0 and 1\_1, the [Source Register Signed Scaling](dx9-graphics-reference-asm-ps-registers-modifiers-signed-scale.md) input modifier (\_bx2) is not permitted on the input argument.</span></span>

<span data-ttu-id="222db-136">Эта инструкция формирует определенные результаты, когда текстуры ввода содержат данные в смешанном формате.</span><span class="sxs-lookup"><span data-stu-id="222db-136">This instruction produces defined results when input textures contain mixed format data.</span></span> <span data-ttu-id="222db-137">Дополнительные сведения о форматах поверхностей см. в разделе [D3DFORMAT](/windows/desktop/direct3d9/d3dformat).</span><span class="sxs-lookup"><span data-stu-id="222db-137">For more information about surface formats, see [D3DFORMAT](/windows/desktop/direct3d9/d3dformat).</span></span>


```
// When using this instruction, texture registers must follow 
//   the following sequence:
// The texture assigned to stage tn contains the (du,dv) data
// The texture assigned to stage t(m) is sampled
tex     t(n)                    
texbeml t(m),  t(n)      where m > n
```



<span data-ttu-id="222db-138">В этом примере показаны вычисления, выполненные в рамках инструкции.</span><span class="sxs-lookup"><span data-stu-id="222db-138">This example shows the calculations done within the instruction.</span></span>


```
// 1. New values for texture addresses (u',v') are calculated
// 2. Sample the texture using (u',v')
// 3. Luminance correction is applied
```



<span data-ttu-id="222db-139">u "= TextureCoordinates (этап m)<sub>u</sub> +</span><span class="sxs-lookup"><span data-stu-id="222db-139">u' = TextureCoordinates(stage m)<sub>u</sub> +</span></span>

<span data-ttu-id="222db-140">D3DTSS \_ BUMPENVMAT00 (этап m) \* t (n)<sub>R</sub> +</span><span class="sxs-lookup"><span data-stu-id="222db-140">D3DTSS\_BUMPENVMAT00(stage m)\*t(n)<sub>R</sub> +</span></span>

<span data-ttu-id="222db-141">D3DTSS \_ BUMPENVMAT10 (этап m) \* t (n)<sub>G</sub></span><span class="sxs-lookup"><span data-stu-id="222db-141">D3DTSS\_BUMPENVMAT10(stage m)\*t(n)<sub>G</sub></span></span>

<span data-ttu-id="222db-142">v ' = TextureCoordinates (этап m)<sub>v</sub> +</span><span class="sxs-lookup"><span data-stu-id="222db-142">v' = TextureCoordinates(stage m)<sub>v</sub> +</span></span>

<span data-ttu-id="222db-143">D3DTSS \_ BUMPENVMAT01 (этап m) \* t (n)<sub>R</sub> +</span><span class="sxs-lookup"><span data-stu-id="222db-143">D3DTSS\_BUMPENVMAT01(stage m)\*t(n)<sub>R</sub> +</span></span>

<span data-ttu-id="222db-144">D3DTSS \_ BUMPENVMAT11 (этап m) \* t (n)<sub>G</sub></span><span class="sxs-lookup"><span data-stu-id="222db-144">D3DTSS\_BUMPENVMAT11(stage m)\*t(n)<sub>G</sub></span></span>

<span data-ttu-id="222db-145">t (m)<sub>RGBA</sub> = текстуресампле (этап m) использование (u ", v") в качестве координат</span><span class="sxs-lookup"><span data-stu-id="222db-145">t(m)<sub>RGBA</sub> = TextureSample(stage m) using (u',v') as coordinates</span></span>

<span data-ttu-id="222db-146">t (m)<sub>RGBA</sub> = t (m)<sub>RGBA</sub>\*</span><span class="sxs-lookup"><span data-stu-id="222db-146">t(m)<sub>RGBA</sub> = t(m)<sub>RGBA</sub> \*</span></span>

<span data-ttu-id="222db-147">\[(t (n)<sub>б</sub> \* D3DTSS \_ бумпенвлскале (этап m)) +</span><span class="sxs-lookup"><span data-stu-id="222db-147">\[(t(n)<sub>B</sub> \* D3DTSS\_BUMPENVLSCALE(stage m)) +</span></span>

<span data-ttu-id="222db-148">D3DTSS \_ бумпенвлоффсет (этап m)\]</span><span class="sxs-lookup"><span data-stu-id="222db-148">D3DTSS\_BUMPENVLOFFSET(stage m)\]</span></span>

<span data-ttu-id="222db-149">Данные регистрации, считанные инструкцией [тексбем](texbem---ps.md) или тексбемл, не могут быть считаны позже, за исключением других тексбем или тексбемл.</span><span class="sxs-lookup"><span data-stu-id="222db-149">Register data that has been read by a [texbem](texbem---ps.md) or texbeml instruction cannot be read later, except by another texbem or texbeml.</span></span>


```
// This example demonstrates the validation error caused by 
//   t0 being reread
ps_1_1
tex t0
texbem t1, t0
add r0, t1, t0

(Instruction Error) (Statement 4) Register data that has been read by 
texbem or texbeml instruction cannot be read by other instructions
```



## <a name="examples"></a><span data-ttu-id="222db-150">Примеры</span><span class="sxs-lookup"><span data-stu-id="222db-150">Examples</span></span>

<span data-ttu-id="222db-151">Ниже приведен пример шейдера с идентифицированными картами текстур и идентифицированными стадиями текстуры.</span><span class="sxs-lookup"><span data-stu-id="222db-151">Here is an example shader with the texture maps identified and the texture stages identified.</span></span>


```
ps_1_1
tex t0              ; Define t0 to get a 2-tuple DuDv
texbeml t1, t0      ; Compute (u',v')
                    ; Apply luminance correction                    
                    ; Sample t1 using (u',v')
mov r0, t1          ; Output result
```



<span data-ttu-id="222db-152">Для этого примера требуются следующие текстуры на следующих стадиях текстуры.</span><span class="sxs-lookup"><span data-stu-id="222db-152">This example requires the following textures in the following texture stages.</span></span>

-   <span data-ttu-id="222db-153">Этапу 0 назначается схема выпуклости с данными (du, DV) пертурбатион.</span><span class="sxs-lookup"><span data-stu-id="222db-153">Stage 0 is assigned a bump map with (du, dv) perturbation data.</span></span>
-   <span data-ttu-id="222db-154">Этап 1 назначает текстурную карту с данными цвета.</span><span class="sxs-lookup"><span data-stu-id="222db-154">Stage 1 is assigned a texture map with color data.</span></span>
-   <span data-ttu-id="222db-155">тексбемл задает данные матрицы на стадии текстуры, которая является выборкой.</span><span class="sxs-lookup"><span data-stu-id="222db-155">texbeml sets the matrix data on the texture stage that is sampled.</span></span> <span data-ttu-id="222db-156">Это отличается от функций конвейера с фиксированной функцией, где данные пертурбатион и матрицы занимают одну и ту же стадию текстуры.</span><span class="sxs-lookup"><span data-stu-id="222db-156">This is different from the functionality of the fixed function pipeline where the perturbation data and the matrices occupy the same texture stage.</span></span>

## <a name="related-topics"></a><span data-ttu-id="222db-157">См. также</span><span class="sxs-lookup"><span data-stu-id="222db-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="222db-158">Инструкции шейдера пикселей</span><span class="sxs-lookup"><span data-stu-id="222db-158">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 