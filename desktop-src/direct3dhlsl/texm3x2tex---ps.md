---
title: texm3x2tex-PS
description: Выполняет заполнение последней строки матрицы 3x2 и использует результат для поиска текстур. texm3x2tex необходимо использовать в сочетании с инструкцией texm3x2pad-PS.
ms.assetid: c6cfbf75-4a63-4c82-9fb6-286b51b7f883
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 62206bc4ef1e1b64ec760a240a087ec13526d896
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104996914"
---
# <a name="texm3x2tex---ps"></a><span data-ttu-id="e137e-104">texm3x2tex-PS</span><span class="sxs-lookup"><span data-stu-id="e137e-104">texm3x2tex - ps</span></span>

<span data-ttu-id="e137e-105">Выполняет заполнение последней строки матрицы 3x2 и использует результат для поиска текстур.</span><span class="sxs-lookup"><span data-stu-id="e137e-105">Performs the final row of a 3x2 matrix multiply and uses the result to do a texture lookup.</span></span> <span data-ttu-id="e137e-106">texm3x2tex необходимо использовать в сочетании с инструкцией [texm3x2pad-PS](texm3x2pad---ps.md) .</span><span class="sxs-lookup"><span data-stu-id="e137e-106">texm3x2tex must be used in conjunction with the [texm3x2pad - ps](texm3x2pad---ps.md) instruction.</span></span>

## <a name="syntax"></a><span data-ttu-id="e137e-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e137e-107">Syntax</span></span>



| <span data-ttu-id="e137e-108">texm3x2tex DST, src</span><span class="sxs-lookup"><span data-stu-id="e137e-108">texm3x2tex dst, src</span></span> |
|---------------------|



 

<span data-ttu-id="e137e-109">где</span><span class="sxs-lookup"><span data-stu-id="e137e-109">where</span></span>

-   <span data-ttu-id="e137e-110">DST — это регистр назначения.</span><span class="sxs-lookup"><span data-stu-id="e137e-110">dst is the destination register.</span></span>
-   <span data-ttu-id="e137e-111">src является исходным регистром.</span><span class="sxs-lookup"><span data-stu-id="e137e-111">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="e137e-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="e137e-112">Remarks</span></span>



| <span data-ttu-id="e137e-113">Версии шейдеров пикселей</span><span class="sxs-lookup"><span data-stu-id="e137e-113">Pixel shader versions</span></span> | <span data-ttu-id="e137e-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="e137e-114">1\_1</span></span> | <span data-ttu-id="e137e-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="e137e-115">1\_2</span></span> | <span data-ttu-id="e137e-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="e137e-116">1\_3</span></span> | <span data-ttu-id="e137e-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="e137e-117">1\_4</span></span> | <span data-ttu-id="e137e-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="e137e-118">2\_0</span></span> | <span data-ttu-id="e137e-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="e137e-119">2\_x</span></span> | <span data-ttu-id="e137e-120">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="e137e-120">2\_sw</span></span> | <span data-ttu-id="e137e-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="e137e-121">3\_0</span></span> | <span data-ttu-id="e137e-122">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="e137e-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="e137e-123">texm3x2tex</span><span class="sxs-lookup"><span data-stu-id="e137e-123">texm3x2tex</span></span>            | <span data-ttu-id="e137e-124">x</span><span class="sxs-lookup"><span data-stu-id="e137e-124">x</span></span>    | <span data-ttu-id="e137e-125">x</span><span class="sxs-lookup"><span data-stu-id="e137e-125">x</span></span>    | <span data-ttu-id="e137e-126">x</span><span class="sxs-lookup"><span data-stu-id="e137e-126">x</span></span>    |      |      |      |       |      |       |



 

<span data-ttu-id="e137e-127">Инструкция используется как одна из двух инструкций, представляющих операцию умножения матрицы 3x2.</span><span class="sxs-lookup"><span data-stu-id="e137e-127">The instruction is used as one of two instructions representing a 3x2 matrix multiply operation.</span></span> <span data-ttu-id="e137e-128">Эта инструкция должна использоваться с инструкцией [texm3x2pad-PS](texm3x2pad---ps.md) .</span><span class="sxs-lookup"><span data-stu-id="e137e-128">This instruction must be used with the [texm3x2pad - ps](texm3x2pad---ps.md) instruction.</span></span>

<span data-ttu-id="e137e-129">При использовании этих двух инструкций регистры текстур должны использовать следующую последовательность.</span><span class="sxs-lookup"><span data-stu-id="e137e-129">When using these two instructions, texture registers must use the following sequence.</span></span>


```
 
tex t(n)                      // Define tn as a standard 3-vector (tn must 
                              // be defined in some way before it is used)
texm3x2pad  t(m),   t(n)      // where m > n
                              // Perform first row of matrix multiply
texm3x2tex  t(m+1), t(n)      // Perform second row of matrix multiply 
                              // to get (u,v) to sample texture 
                              // associated with stage m+1
```



<span data-ttu-id="e137e-130">Ниже приведены более подробные сведения о том, как выполняется умножение 3x2.</span><span class="sxs-lookup"><span data-stu-id="e137e-130">Here is more detail about how the 3x2 multiply is accomplished.</span></span>

<span data-ttu-id="e137e-131">Инструкция texm3x2pad выполняет первую строку умножения<sup>, чтобы найти u.</sup></span><span class="sxs-lookup"><span data-stu-id="e137e-131">The texm3x2pad instruction performs the first row of the multiply to find u<sup>'</sup>.</span></span>

<span data-ttu-id="e137e-132">u<sup>"</sup> = t (n)<sub>RGB</sub> \* TextureCoordinates (этап m)<sub>УВВ</sub></span><span class="sxs-lookup"><span data-stu-id="e137e-132">u<sup>'</sup> = t(n)<sub>RGB</sub> \* TextureCoordinates(stage m)<sub>UVW</sub></span></span>

<span data-ttu-id="e137e-133">Инструкция texm3x2tex выполняет вторую строку умножения, чтобы<sup>найти v.</sup></span><span class="sxs-lookup"><span data-stu-id="e137e-133">The texm3x2tex instruction performs the second row of the multiply to find v<sup>'</sup>.</span></span>

<span data-ttu-id="e137e-134">v<sup>'</sup> = t (n) TextureCoordinates<sub>RGB</sub> \* (этап m + 1)<sub>УВВ</sub></span><span class="sxs-lookup"><span data-stu-id="e137e-134">v<sup>'</sup> = t(n)<sub>RGB</sub> \* TextureCoordinates(stage m+1)<sub>UVW</sub></span></span>

<span data-ttu-id="e137e-135">Инструкция texm3x2tex выбирает текстуру на этапе (m + 1) с (u<sup>"</sup>, v<sup>"</sup>) и сохраняет результат в t (m + 1).</span><span class="sxs-lookup"><span data-stu-id="e137e-135">The texm3x2tex instruction samples the texture on stage (m+1) with (u<sup>'</sup>,v<sup>'</sup>) and stores the result in t(m+1).</span></span>

<span data-ttu-id="e137e-136">t (m + 1)<sub>RGB</sub> = текстуресампле (этап m + 1)<sub>RGB</sub> using (u<sup>"</sup>, v<sup>"</sup> ) в качестве координат</span><span class="sxs-lookup"><span data-stu-id="e137e-136">t(m+1)<sub>RGB</sub> = TextureSample(stage m+1)<sub>RGB</sub> using (u<sup>'</sup>, v<sup>'</sup> ) as coordinates</span></span>

## <a name="examples"></a><span data-ttu-id="e137e-137">Примеры</span><span class="sxs-lookup"><span data-stu-id="e137e-137">Examples</span></span>

<span data-ttu-id="e137e-138">Ниже приведен пример шейдера с текстурными картами и идентифицированными стадиями текстуры.</span><span class="sxs-lookup"><span data-stu-id="e137e-138">Here is an example shader with the texture maps and the texture stages identified.</span></span>


```
ps_1_1
tex t0                // Bind texture in stage 0 to register t0
texm3x2pad  t1,  t0   // First row of matrix multiply
texm3x2tex  t2,  t0   // Second row of matrix multiply to get (u,v)
                      // with which to sample texture in stage 2
mov r0, t2            // Output result
```



<span data-ttu-id="e137e-139">Для этого примера требуются следующие текстуры на следующих стадиях текстуры.</span><span class="sxs-lookup"><span data-stu-id="e137e-139">This example requires the following textures in the following texture stages.</span></span>

-   <span data-ttu-id="e137e-140">Этап 0 принимает карту с данными (x, y, z) пертурбатион.</span><span class="sxs-lookup"><span data-stu-id="e137e-140">Stage 0 takes a map with (x,y,z) perturbation data.</span></span>
-   <span data-ttu-id="e137e-141">Этап 1 содержит координаты текстуры.</span><span class="sxs-lookup"><span data-stu-id="e137e-141">Stage 1 holds texture coordinates.</span></span> <span data-ttu-id="e137e-142">На стадии текстуры текстура не требуется.</span><span class="sxs-lookup"><span data-stu-id="e137e-142">No texture is required in the texture stage.</span></span>
-   <span data-ttu-id="e137e-143">Этап 2 содержит как координаты текстуры, так и набор 2D-текстур на этой стадии текстуры.</span><span class="sxs-lookup"><span data-stu-id="e137e-143">Stage 2 holds both texture coordinates as well as a 2D texture set at that texture stage.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e137e-144">См. также</span><span class="sxs-lookup"><span data-stu-id="e137e-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e137e-145">Инструкции шейдера пикселей</span><span class="sxs-lookup"><span data-stu-id="e137e-145">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




