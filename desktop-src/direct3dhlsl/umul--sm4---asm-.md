---
title: умул (SM4-ASM)
description: Умножение целого числа без знака.
ms.assetid: C84AF349-32E6-40C4-9973-BCFA73EFBF0B
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 581696ef5aa7d027c30b4ae866d06401275ef4bc
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104412175"
---
# <a name="umul-sm4---asm"></a><span data-ttu-id="ab4c2-103">умул (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="ab4c2-103">umul (sm4 - asm)</span></span>

<span data-ttu-id="ab4c2-104">Умножение целого числа без знака.</span><span class="sxs-lookup"><span data-stu-id="ab4c2-104">Unsigned integer multiply.</span></span>



| <span data-ttu-id="ab4c2-105">умул Десси \[ . Mask \] , дестло \[ . Mask \] , src0 \[ . свиззле \] , src1 \[ . свиззле\]</span><span class="sxs-lookup"><span data-stu-id="ab4c2-105">umul destHI\[.mask\], destLO\[.mask\], src0\[.swizzle\], src1\[.swizzle\]</span></span> |
|---------------------------------------------------------------------------|



 



| <span data-ttu-id="ab4c2-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="ab4c2-106">Item</span></span>                                                                                           | <span data-ttu-id="ab4c2-107">Описание</span><span class="sxs-lookup"><span data-stu-id="ab4c2-107">Description</span></span>                                                      |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span data-ttu-id="ab4c2-108"><span id="destHI"></span><span id="desthi"></span><span id="DESTHI"></span>*десси*</span><span class="sxs-lookup"><span data-stu-id="ab4c2-108"><span id="destHI"></span><span id="desthi"></span><span id="DESTHI"></span>*destHI*</span></span><br/> | <span data-ttu-id="ab4c2-109">\[в \] 32 старших бит результата для каждого компонента.</span><span class="sxs-lookup"><span data-stu-id="ab4c2-109">\[in\] The high 32 bits of the result, per component.</span></span><br/> |
| <span data-ttu-id="ab4c2-110"><span id="destLO"></span><span id="destlo"></span><span id="DESTLO"></span>*дестло*</span><span class="sxs-lookup"><span data-stu-id="ab4c2-110"><span id="destLO"></span><span id="destlo"></span><span id="DESTLO"></span>*destLO*</span></span><br/> | <span data-ttu-id="ab4c2-111">\[в \] младших 32 битах результата для каждого компонента.</span><span class="sxs-lookup"><span data-stu-id="ab4c2-111">\[in\] The low 32 bits of the result, per component.</span></span><br/>  |
| <span data-ttu-id="ab4c2-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="ab4c2-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>                                | <span data-ttu-id="ab4c2-113">\[в \] компонентах, по которым умножается *src1*.</span><span class="sxs-lookup"><span data-stu-id="ab4c2-113">\[in\] The components by which to multiply *src1*.</span></span><br/>    |
| <span data-ttu-id="ab4c2-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="ab4c2-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/>                                | <span data-ttu-id="ab4c2-115">\[в \] компонентах, по которым умножается *src0*.</span><span class="sxs-lookup"><span data-stu-id="ab4c2-115">\[in\] The components by which to multiply *src0*.</span></span><br/>    |



 

## <a name="remarks"></a><span data-ttu-id="ab4c2-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="ab4c2-116">Remarks</span></span>

<span data-ttu-id="ab4c2-117">Эта инструкция выполняет покомпонентное умножение беззнаковых 32-разрядных операндов *src0* и *src1*, создавая правильный полный 64-разрядный результат для каждого компонента.</span><span class="sxs-lookup"><span data-stu-id="ab4c2-117">This instruction performs a component-wise multiply of unsigned 32-bit operands *src0* and *src1*, producing the correct full 64-bit result per component.</span></span> <span data-ttu-id="ab4c2-118">Младшие 32 бит на компонент помещаются в *дестло*.</span><span class="sxs-lookup"><span data-stu-id="ab4c2-118">The low 32 bits per component are placed in *destLO*.</span></span> <span data-ttu-id="ab4c2-119">Старшие 32 бит на компонент помещаются в *Десси*.</span><span class="sxs-lookup"><span data-stu-id="ab4c2-119">The high 32 bits per component are placed in *destHI*.</span></span>

<span data-ttu-id="ab4c2-120">Можно указать либо *Десси* , либо *дестло* как NULL вместо указания регистра, если не требуется высокий или младший 32 бит 64-разрядного результата.</span><span class="sxs-lookup"><span data-stu-id="ab4c2-120">You can specify either *destHI* or *destLO* as NULL instead of specifying a register if the high or low 32 bits of the 64-bit result are not needed.</span></span>

<span data-ttu-id="ab4c2-121">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="ab4c2-121">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="ab4c2-122">Вершинный построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="ab4c2-122">Vertex Shader</span></span> | <span data-ttu-id="ab4c2-123">Шейдер геометрии</span><span class="sxs-lookup"><span data-stu-id="ab4c2-123">Geometry Shader</span></span> | <span data-ttu-id="ab4c2-124">Построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="ab4c2-124">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="ab4c2-125">x</span><span class="sxs-lookup"><span data-stu-id="ab4c2-125">x</span></span>             | <span data-ttu-id="ab4c2-126">x</span><span class="sxs-lookup"><span data-stu-id="ab4c2-126">x</span></span>               | <span data-ttu-id="ab4c2-127">x</span><span class="sxs-lookup"><span data-stu-id="ab4c2-127">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="ab4c2-128">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="ab4c2-128">Minimum Shader Model</span></span>

<span data-ttu-id="ab4c2-129">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="ab4c2-129">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="ab4c2-130">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="ab4c2-130">Shader Model</span></span>                                              | <span data-ttu-id="ab4c2-131">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="ab4c2-131">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="ab4c2-132">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="ab4c2-132">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="ab4c2-133">да</span><span class="sxs-lookup"><span data-stu-id="ab4c2-133">yes</span></span>       |
| [<span data-ttu-id="ab4c2-134">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="ab4c2-134">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="ab4c2-135">да</span><span class="sxs-lookup"><span data-stu-id="ab4c2-135">yes</span></span>       |
| [<span data-ttu-id="ab4c2-136">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="ab4c2-136">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="ab4c2-137">да</span><span class="sxs-lookup"><span data-stu-id="ab4c2-137">yes</span></span>       |
| [<span data-ttu-id="ab4c2-138">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ab4c2-138">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="ab4c2-139">Нет</span><span class="sxs-lookup"><span data-stu-id="ab4c2-139">no</span></span>        |
| [<span data-ttu-id="ab4c2-140">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ab4c2-140">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="ab4c2-141">Нет</span><span class="sxs-lookup"><span data-stu-id="ab4c2-141">no</span></span>        |
| [<span data-ttu-id="ab4c2-142">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ab4c2-142">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="ab4c2-143">Нет</span><span class="sxs-lookup"><span data-stu-id="ab4c2-143">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="ab4c2-144">См. также</span><span class="sxs-lookup"><span data-stu-id="ab4c2-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ab4c2-145">Сборка Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ab4c2-145">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





