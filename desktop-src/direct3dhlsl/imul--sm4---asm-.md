---
title: imul (SM4-ASM)
description: Умножение целого числа со знаком.
ms.assetid: DB95A38F-54E4-4BB6-81DF-CFFEBB4D425B
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 997f62fc389ad1e0fb6b23dd6c419ff8b3933b41
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "103784959"
---
# <a name="imul-sm4---asm"></a><span data-ttu-id="7f224-103">imul (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="7f224-103">imul (sm4 - asm)</span></span>

<span data-ttu-id="7f224-104">Умножение целого числа со знаком.</span><span class="sxs-lookup"><span data-stu-id="7f224-104">Signed integer multiply.</span></span>



| <span data-ttu-id="7f224-105">imul Десси \[ . Mask \] , дестло \[ . Mask \] , \[ - \] src0 \[ . свиззле \] , \[ - \] src1 \[ . свиззле\]</span><span class="sxs-lookup"><span data-stu-id="7f224-105">imul destHI\[.mask\], destLO\[.mask\], \[-\]src0\[.swizzle\], \[-\]src1\[.swizzle\]</span></span> |
|-------------------------------------------------------------------------------------|



 



| <span data-ttu-id="7f224-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="7f224-106">Item</span></span>                                                                                           | <span data-ttu-id="7f224-107">Описание</span><span class="sxs-lookup"><span data-stu-id="7f224-107">Description</span></span>                                                      |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span data-ttu-id="7f224-108"><span id="destHI"></span><span id="desthi"></span><span id="DESTHI"></span>*десси*</span><span class="sxs-lookup"><span data-stu-id="7f224-108"><span id="destHI"></span><span id="desthi"></span><span id="DESTHI"></span>*destHI*</span></span><br/> | <span data-ttu-id="7f224-109">\[в \] адресе старших 32 бит результата.</span><span class="sxs-lookup"><span data-stu-id="7f224-109">\[in\] The address of the high 32 bits of the result.</span></span><br/> |
| <span data-ttu-id="7f224-110"><span id="destLO"></span><span id="destlo"></span><span id="DESTLO"></span>*дестло*</span><span class="sxs-lookup"><span data-stu-id="7f224-110"><span id="destLO"></span><span id="destlo"></span><span id="DESTLO"></span>*destLO*</span></span><br/> | <span data-ttu-id="7f224-111">\[в \] адресе младших 32 бит результата.</span><span class="sxs-lookup"><span data-stu-id="7f224-111">\[in\] The address of the low 32 bits of the result.</span></span><br/>  |
| <span data-ttu-id="7f224-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="7f224-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>                                | <span data-ttu-id="7f224-113">\[в \] значении, умноженном на *src1*.</span><span class="sxs-lookup"><span data-stu-id="7f224-113">\[in\] The value to multiply with *src1*.</span></span><br/>             |
| <span data-ttu-id="7f224-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="7f224-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/>                                | <span data-ttu-id="7f224-115">\[в \] значении, умноженном на *src0*.</span><span class="sxs-lookup"><span data-stu-id="7f224-115">\[in\] The value to multiply with *src0*.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="7f224-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="7f224-116">Remarks</span></span>

<span data-ttu-id="7f224-117">Покомпонентное умножение 32-разрядных операндов *src0* и *src1* (они подписываются), создавая правильный полный 64-разрядный (на каждый компонент) результат.</span><span class="sxs-lookup"><span data-stu-id="7f224-117">Component-wise multiply of 32-bit operands *src0* and *src1* (both are signed), producing the correct full 64-bit (per component) result.</span></span> <span data-ttu-id="7f224-118">Младшие 32 бит (на компонент) помещаются в *дестло*.</span><span class="sxs-lookup"><span data-stu-id="7f224-118">The low 32 bits (per component) are placed in *destLO*.</span></span> <span data-ttu-id="7f224-119">Старшие 32 бит (на компонент) помещаются в *Десси*.</span><span class="sxs-lookup"><span data-stu-id="7f224-119">The high 32 bits (per component) are placed in *destHI*.</span></span>

<span data-ttu-id="7f224-120">Либо *Десси* , либо *дестло* могут быть указаны как NULL вместо указания регистра, если старший или младший 32 бит 64-разрядного результата не требуется.</span><span class="sxs-lookup"><span data-stu-id="7f224-120">Either *destHI* or *destLO* may be specified as NULL instead of specifying a register, if the high or low 32 bits of the 64-bit result are not needed.</span></span>

<span data-ttu-id="7f224-121">Необязательный модификатор отрицания в исходных операндах перед выполнением арифметической операции принимает 2 дополнения.</span><span class="sxs-lookup"><span data-stu-id="7f224-121">Optional negate modifier on source operands takes 2's complement before performing arithmetic operation.</span></span>

<span data-ttu-id="7f224-122">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="7f224-122">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="7f224-123">Вершинный построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="7f224-123">Vertex Shader</span></span> | <span data-ttu-id="7f224-124">Шейдер геометрии</span><span class="sxs-lookup"><span data-stu-id="7f224-124">Geometry Shader</span></span> | <span data-ttu-id="7f224-125">Построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="7f224-125">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="7f224-126">x</span><span class="sxs-lookup"><span data-stu-id="7f224-126">x</span></span>             | <span data-ttu-id="7f224-127">x</span><span class="sxs-lookup"><span data-stu-id="7f224-127">x</span></span>               | <span data-ttu-id="7f224-128">x</span><span class="sxs-lookup"><span data-stu-id="7f224-128">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="7f224-129">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="7f224-129">Minimum Shader Model</span></span>

<span data-ttu-id="7f224-130">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="7f224-130">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="7f224-131">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="7f224-131">Shader Model</span></span>                                              | <span data-ttu-id="7f224-132">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="7f224-132">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="7f224-133">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="7f224-133">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="7f224-134">да</span><span class="sxs-lookup"><span data-stu-id="7f224-134">yes</span></span>       |
| [<span data-ttu-id="7f224-135">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="7f224-135">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="7f224-136">да</span><span class="sxs-lookup"><span data-stu-id="7f224-136">yes</span></span>       |
| [<span data-ttu-id="7f224-137">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="7f224-137">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="7f224-138">да</span><span class="sxs-lookup"><span data-stu-id="7f224-138">yes</span></span>       |
| [<span data-ttu-id="7f224-139">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7f224-139">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="7f224-140">Нет</span><span class="sxs-lookup"><span data-stu-id="7f224-140">no</span></span>        |
| [<span data-ttu-id="7f224-141">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7f224-141">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="7f224-142">Нет</span><span class="sxs-lookup"><span data-stu-id="7f224-142">no</span></span>        |
| [<span data-ttu-id="7f224-143">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7f224-143">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="7f224-144">Нет</span><span class="sxs-lookup"><span data-stu-id="7f224-144">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="7f224-145">См. также</span><span class="sxs-lookup"><span data-stu-id="7f224-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7f224-146">Сборка Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7f224-146">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





