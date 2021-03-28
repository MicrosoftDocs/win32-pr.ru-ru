---
title: DP3-PS
description: Выполняет вычисление 3-компонентного произведения исходных регистров. | DP3-PS
ms.assetid: a365acd1-89c0-4340-8f51-8e478f84ddc0
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 09e4178f6aedbfb5242f4c545d624f1d07796008
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986364"
---
# <a name="dp3---ps"></a><span data-ttu-id="42b58-104">DP3-PS</span><span class="sxs-lookup"><span data-stu-id="42b58-104">dp3 - ps</span></span>

<span data-ttu-id="42b58-105">Выполняет вычисление 3-компонентного произведения исходных регистров.</span><span class="sxs-lookup"><span data-stu-id="42b58-105">Computes the three-component dot product of the source registers.</span></span>

## <a name="syntax"></a><span data-ttu-id="42b58-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="42b58-106">Syntax</span></span>



| <span data-ttu-id="42b58-107">DP3 DST, src0, src1</span><span class="sxs-lookup"><span data-stu-id="42b58-107">dp3 dst, src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="42b58-108">где</span><span class="sxs-lookup"><span data-stu-id="42b58-108">where</span></span>

-   <span data-ttu-id="42b58-109">DST — это регистр назначения.</span><span class="sxs-lookup"><span data-stu-id="42b58-109">dst is the destination register.</span></span>
-   <span data-ttu-id="42b58-110">src0 является исходным регистром.</span><span class="sxs-lookup"><span data-stu-id="42b58-110">src0 is a source register.</span></span>
-   <span data-ttu-id="42b58-111">src1 является исходным регистром.</span><span class="sxs-lookup"><span data-stu-id="42b58-111">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="42b58-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="42b58-112">Remarks</span></span>



| <span data-ttu-id="42b58-113">Версии шейдеров пикселей</span><span class="sxs-lookup"><span data-stu-id="42b58-113">Pixel shader versions</span></span> | <span data-ttu-id="42b58-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="42b58-114">1\_1</span></span> | <span data-ttu-id="42b58-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="42b58-115">1\_2</span></span> | <span data-ttu-id="42b58-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="42b58-116">1\_3</span></span> | <span data-ttu-id="42b58-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="42b58-117">1\_4</span></span> | <span data-ttu-id="42b58-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="42b58-118">2\_0</span></span> | <span data-ttu-id="42b58-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="42b58-119">2\_x</span></span> | <span data-ttu-id="42b58-120">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="42b58-120">2\_sw</span></span> | <span data-ttu-id="42b58-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="42b58-121">3\_0</span></span> | <span data-ttu-id="42b58-122">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="42b58-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="42b58-123">dp3</span><span class="sxs-lookup"><span data-stu-id="42b58-123">dp3</span></span>                   | <span data-ttu-id="42b58-124">x</span><span class="sxs-lookup"><span data-stu-id="42b58-124">x</span></span>    | <span data-ttu-id="42b58-125">x</span><span class="sxs-lookup"><span data-stu-id="42b58-125">x</span></span>    | <span data-ttu-id="42b58-126">x</span><span class="sxs-lookup"><span data-stu-id="42b58-126">x</span></span>    | <span data-ttu-id="42b58-127">x</span><span class="sxs-lookup"><span data-stu-id="42b58-127">x</span></span>    | <span data-ttu-id="42b58-128">x</span><span class="sxs-lookup"><span data-stu-id="42b58-128">x</span></span>    | <span data-ttu-id="42b58-129">x</span><span class="sxs-lookup"><span data-stu-id="42b58-129">x</span></span>    | <span data-ttu-id="42b58-130">x</span><span class="sxs-lookup"><span data-stu-id="42b58-130">x</span></span>     | <span data-ttu-id="42b58-131">x</span><span class="sxs-lookup"><span data-stu-id="42b58-131">x</span></span>    | <span data-ttu-id="42b58-132">x</span><span class="sxs-lookup"><span data-stu-id="42b58-132">x</span></span>     |



 

<span data-ttu-id="42b58-133">В следующем фрагменте кода показаны выполняемые операции.</span><span class="sxs-lookup"><span data-stu-id="42b58-133">The following code snippet shows the operations performed:</span></span>


```
dest.x = dest.y = dest.z = dest.w = 
  (src0.x * src1.x) + (src0.y * src1.y) + (src0.z * src1.z);
```



<span data-ttu-id="42b58-134">Эта инструкция выполняется в векторном конвейере и всегда записывается в цветовые каналы.</span><span class="sxs-lookup"><span data-stu-id="42b58-134">This instruction runs in the vector pipeline, always writing out to the color channels.</span></span> <span data-ttu-id="42b58-135">Для версии 1 \_ 4 Эта инструкция по-прежнему использует Векторный конвейер, но может выполнять запись в любой канал.</span><span class="sxs-lookup"><span data-stu-id="42b58-135">For version 1\_4, this instruction still uses the vector pipeline but may write to any channel.</span></span>

<span data-ttu-id="42b58-136">Инструкция с конечной точкой Register. RGB (. XYZ) может быть выпущена совместно с DP3, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="42b58-136">An instruction with a destination register .rgb (.xyz) write mask may be co-issued with dp3 As shown below.</span></span>


```
dp3 r0.rgb, t0, v0            // Copy scalar result to color components
+mov r2.a, t0                 // Copy alpha component from t0 in parallel 
```



<span data-ttu-id="42b58-137">Инструкцию DP3 можно изменить с помощью модификатора входного аргумента " [Регистрация регистра](dx9-graphics-reference-asm-ps-registers-modifiers-signed-scale.md) " ( \_ bx2), применяемого к входным аргументам, если они еще не развернуты в динамическом диапазоне со знаком.</span><span class="sxs-lookup"><span data-stu-id="42b58-137">The dp3 instruction can be modified using the [Source Register Signed Scaling](dx9-graphics-reference-asm-ps-registers-modifiers-signed-scale.md) input argument modifier (\_bx2) applied to its input arguments if they are not already expanded to signed dynamic range.</span></span> <span data-ttu-id="42b58-138">Для шейдера освещения часто используется модификатор инструкции «насыщенность» ( \_ Кот) для фиксации отрицательных значений до черного, как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="42b58-138">For a lighting shader, the saturate instruction modifier (\_sat) is often used to clamp the negative values to black, as shown in the following example.</span></span>


```
dp3_sat r0, t0_bx2, v0_bx2    // t0 is a bump map, v0 contains the light direction
```



## <a name="related-topics"></a><span data-ttu-id="42b58-139">См. также</span><span class="sxs-lookup"><span data-stu-id="42b58-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="42b58-140">Инструкции шейдера пикселей</span><span class="sxs-lookup"><span data-stu-id="42b58-140">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




