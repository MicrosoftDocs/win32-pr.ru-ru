---
title: тексбем-PS
description: Примените фиктивное преобразование «среда выпуклости». Это достигается путем изменения данных адреса текстуры в регистре назначения с использованием данных адреса пертурбатион (du, DV) и матрицы среды 2D-выпуклости.
ms.assetid: 8e773f4a-c7a2-4caf-973f-8f50dccc9c04
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f026819b268836fd7d4c1d550033ceefdf0bbbf9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104984008"
---
# <a name="texbem---ps"></a><span data-ttu-id="4a1ff-104">тексбем-PS</span><span class="sxs-lookup"><span data-stu-id="4a1ff-104">texbem - ps</span></span>

<span data-ttu-id="4a1ff-105">Примените фиктивное преобразование «среда выпуклости».</span><span class="sxs-lookup"><span data-stu-id="4a1ff-105">Apply a fake bump environment-map transform.</span></span> <span data-ttu-id="4a1ff-106">Это достигается путем изменения данных адреса текстуры в регистре назначения с использованием данных адреса пертурбатион (du, DV) и матрицы среды 2D-выпуклости.</span><span class="sxs-lookup"><span data-stu-id="4a1ff-106">This is accomplished by modifying the texture address data of the destination register, using address perturbation data (du,dv), and a 2D bump environment matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a1ff-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4a1ff-107">Syntax</span></span>



| <span data-ttu-id="4a1ff-108">тексбем DST, src</span><span class="sxs-lookup"><span data-stu-id="4a1ff-108">texbem dst, src</span></span> |
|-----------------|



 

<span data-ttu-id="4a1ff-109">где</span><span class="sxs-lookup"><span data-stu-id="4a1ff-109">where</span></span>

-   <span data-ttu-id="4a1ff-110">DST — это регистр назначения.</span><span class="sxs-lookup"><span data-stu-id="4a1ff-110">dst is the destination register.</span></span>
-   <span data-ttu-id="4a1ff-111">src является исходным регистром.</span><span class="sxs-lookup"><span data-stu-id="4a1ff-111">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="4a1ff-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="4a1ff-112">Remarks</span></span>



| <span data-ttu-id="4a1ff-113">Версии шейдеров пикселей</span><span class="sxs-lookup"><span data-stu-id="4a1ff-113">Pixel shader versions</span></span> | <span data-ttu-id="4a1ff-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="4a1ff-114">1\_1</span></span> | <span data-ttu-id="4a1ff-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="4a1ff-115">1\_2</span></span> | <span data-ttu-id="4a1ff-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="4a1ff-116">1\_3</span></span> | <span data-ttu-id="4a1ff-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="4a1ff-117">1\_4</span></span> | <span data-ttu-id="4a1ff-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="4a1ff-118">2\_0</span></span> | <span data-ttu-id="4a1ff-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="4a1ff-119">2\_x</span></span> | <span data-ttu-id="4a1ff-120">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="4a1ff-120">2\_sw</span></span> | <span data-ttu-id="4a1ff-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="4a1ff-121">3\_0</span></span> | <span data-ttu-id="4a1ff-122">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="4a1ff-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="4a1ff-123">тексбем</span><span class="sxs-lookup"><span data-stu-id="4a1ff-123">texbem</span></span>                | <span data-ttu-id="4a1ff-124">x</span><span class="sxs-lookup"><span data-stu-id="4a1ff-124">x</span></span>    | <span data-ttu-id="4a1ff-125">x</span><span class="sxs-lookup"><span data-stu-id="4a1ff-125">x</span></span>    | <span data-ttu-id="4a1ff-126">x</span><span class="sxs-lookup"><span data-stu-id="4a1ff-126">x</span></span>    |      |      |      |       |      |       |



 

<span data-ttu-id="4a1ff-127">Красный и зеленый цветовые данные в регистре src интерпретируется как данные пертурбатион (du, DV).</span><span class="sxs-lookup"><span data-stu-id="4a1ff-127">The red and green color data in the src register is interpreted as the perturbation data (du,dv).</span></span>

<span data-ttu-id="4a1ff-128">Эта инструкция преобразует красные и зеленые компоненты в исходном регистре с помощью матрицы сопоставления среды 2D-выпуклости.</span><span class="sxs-lookup"><span data-stu-id="4a1ff-128">This instruction transforms red and green components in the source register using the 2D bump environment-mapping matrix.</span></span> <span data-ttu-id="4a1ff-129">Результат добавляется в набор координат текстуры, соответствующий номеру регистра назначения, и используется для выборки текущей стадии текстуры.</span><span class="sxs-lookup"><span data-stu-id="4a1ff-129">The result is added to the texture coordinate set corresponding to the destination register number, and is used to sample the current texture stage.</span></span>

<span data-ttu-id="4a1ff-130">Эта операция всегда интерпретирует du и DV как количество со знаком.</span><span class="sxs-lookup"><span data-stu-id="4a1ff-130">This operation always interprets du and dv as signed quantities.</span></span> <span data-ttu-id="4a1ff-131">Для версий 1 \_ 0 и 1 \_ 1 в входном аргументе не разрешается использовать модификатор input для [масштабирования со знаком "Source Register](dx9-graphics-reference-asm-ps-registers-modifiers-signed-scale.md) " ( \_ bx2).</span><span class="sxs-lookup"><span data-stu-id="4a1ff-131">For versions 1\_0 and 1\_1, the [Source Register Signed Scaling](dx9-graphics-reference-asm-ps-registers-modifiers-signed-scale.md) input modifier (\_bx2) is not permitted on the input argument.</span></span>

<span data-ttu-id="4a1ff-132">Эта инструкция формирует определенные результаты, когда текстуры ввода содержат подписанные данные формата.</span><span class="sxs-lookup"><span data-stu-id="4a1ff-132">This instruction produces defined results when input textures contain signed format data.</span></span> <span data-ttu-id="4a1ff-133">Данные в смешанном формате работают только в том случае, если первые два канала содержат подписанные данные.</span><span class="sxs-lookup"><span data-stu-id="4a1ff-133">Mixed format data works only if the first two channels contain signed data.</span></span> <span data-ttu-id="4a1ff-134">Дополнительные сведения о форматах поверхностей см. в разделе [D3DFORMAT](/windows/desktop/direct3d9/d3dformat).</span><span class="sxs-lookup"><span data-stu-id="4a1ff-134">For more information about surface formats, see [D3DFORMAT](/windows/desktop/direct3d9/d3dformat).</span></span>

<span data-ttu-id="4a1ff-135">Это можно использовать для различных методов, основанных на адресах пертурбатион, включая имитацию сопоставления среды на пиксель и рассеянное освещение (отображение выпуклости).</span><span class="sxs-lookup"><span data-stu-id="4a1ff-135">This can be used for a variety of techniques based on address perturbation, including fake per-pixel environment mapping and diffuse lighting (bump mapping).</span></span>

<span data-ttu-id="4a1ff-136">При использовании этой инструкции регистры текстур должны следовать следующей последовательности.</span><span class="sxs-lookup"><span data-stu-id="4a1ff-136">When using this instruction, texture registers must follow the following sequence.</span></span>


```
// The texture assigned to stage t(n) contains the (du,dv) data
// The texture assigned to stage t(m) is sampled
tex     t(n)                    
texbem  t(m),  t(n)      where m > n
```



<span data-ttu-id="4a1ff-137">Ниже показаны вычисления, выполненные в инструкции.</span><span class="sxs-lookup"><span data-stu-id="4a1ff-137">The calculations done within the instruction are shown below.</span></span>


```
// 1. New values for texture addresses (u',v') are calculated
// 2. Sample the texture using (u',v')
```



<span data-ttu-id="4a1ff-138">u "= TextureCoordinates (этап m)<sub>u</sub> + D3DTSS \_ BUMPENVMAT00 (этап m) \* t (n)<sub>R</sub> + D3DTSS \_ BUMPENVMAT10 (этап m) \* t (n)<sub>G</sub> v ' = TextureCoordinates (этап m)<sub>v</sub> + D3DTSS \_ BUMPENVMAT01 (этап m) \* t (n)<sub>R</sub> + D3DTSS \_ BUMPENVMAT11 (этап m) t ( \* n)<sub>G</sub> t (m)<sub>RGBA</sub> = текстуресампле (этап m)</span><span class="sxs-lookup"><span data-stu-id="4a1ff-138">u' = TextureCoordinates(stage m)<sub>u</sub> + D3DTSS\_BUMPENVMAT00(stage m)\*t(n)<sub>R</sub> + D3DTSS\_BUMPENVMAT10(stage m)\*t(n)<sub>G</sub> v' = TextureCoordinates(stage m)<sub>v</sub> + D3DTSS\_BUMPENVMAT01(stage m)\*t(n)<sub>R</sub> + D3DTSS\_BUMPENVMAT11(stage m)\*t(n)<sub>G</sub> t(m)<sub>RGBA</sub> = TextureSample(stage m)</span></span>

<span data-ttu-id="4a1ff-139">использование (u ", v") в качестве координат</span><span class="sxs-lookup"><span data-stu-id="4a1ff-139">// using (u',v') as coordinates</span></span>

<span data-ttu-id="4a1ff-140">Данные регистрации, считанные инструкцией тексбем-PS или [тексбемл-PS](texbeml---ps.md) , не могут быть считаны позже, за исключением других тексбем-PS или тексбемл-PS.</span><span class="sxs-lookup"><span data-stu-id="4a1ff-140">Register data that has been read by a texbem - ps or [texbeml - ps](texbeml---ps.md) instruction cannot be read later, except by another texbem - ps or texbeml - ps.</span></span>


```
// This example demonstrates the validation error caused by t0 being reread:
ps_1_1
tex t0
texbem t1, t0
add r0, t1, t0

(Instruction Error) (Statement 4) Register data that has been read by 
texbem or texbeml instruction cannot be read by other instructions
```



## <a name="examples"></a><span data-ttu-id="4a1ff-141">Примеры</span><span class="sxs-lookup"><span data-stu-id="4a1ff-141">Examples</span></span>

<span data-ttu-id="4a1ff-142">Ниже приведен пример шейдера с идентифицированными картами текстур и идентифицированными стадиями текстуры.</span><span class="sxs-lookup"><span data-stu-id="4a1ff-142">Here is an example shader with the texture maps identified and the texture stages identified.</span></span>


```
ps_1_1
tex t0              ; Define t0 to get a 2-tuple DuDv
texbem t1, t0       ; Compute (u',v')
                    ; Sample t1 using (u',v')
mov r0, t1          ; Output result
```



<span data-ttu-id="4a1ff-143">для тексбем требуются следующие текстуры на следующих стадиях текстуры.</span><span class="sxs-lookup"><span data-stu-id="4a1ff-143">texbem requires the following textures in the following texture stages.</span></span>

-   <span data-ttu-id="4a1ff-144">Этапу 0 назначается схема выпуклости с данными (du, DV) пертурбатион.</span><span class="sxs-lookup"><span data-stu-id="4a1ff-144">Stage 0 is assigned a bump map with (du, dv) perturbation data.</span></span>
-   <span data-ttu-id="4a1ff-145">Этап 1 использует текстурную карту с данными цвета.</span><span class="sxs-lookup"><span data-stu-id="4a1ff-145">Stage 1 uses a texture map with color data.</span></span>
-   <span data-ttu-id="4a1ff-146">Эта инструкция задает данные матрицы на стадии текстуры, которая является выборкой.</span><span class="sxs-lookup"><span data-stu-id="4a1ff-146">This instruction sets the matrix data on the texture stage that is sampled.</span></span>
-   <span data-ttu-id="4a1ff-147">Это отличается от функций конвейера с фиксированной функцией, где данные пертурбатион и матрицы занимают одну и ту же стадию текстуры.</span><span class="sxs-lookup"><span data-stu-id="4a1ff-147">This is different from the functionality of the fixed function pipeline where the perturbation data and the matrices occupy the same texture stage.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4a1ff-148">См. также</span><span class="sxs-lookup"><span data-stu-id="4a1ff-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4a1ff-149">Инструкции шейдера пикселей</span><span class="sxs-lookup"><span data-stu-id="4a1ff-149">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 