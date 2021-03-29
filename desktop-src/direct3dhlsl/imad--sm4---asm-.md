---
title: Имад (SM4-ASM)
description: Целое число со знаком умножение и добавление.
ms.assetid: 1C24AF49-AA32-4D3A-8478-C9BAC4FE7D77
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90db4cb0a36b0d3951e8b0490bb3ca08db8d5354
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104996859"
---
# <a name="imad-sm4---asm"></a><span data-ttu-id="3891f-103">Имад (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="3891f-103">imad (sm4 - asm)</span></span>

<span data-ttu-id="3891f-104">Целое число со знаком умножение и добавление.</span><span class="sxs-lookup"><span data-stu-id="3891f-104">Signed integer multiply and add.</span></span>



| <span data-ttu-id="3891f-105">Имад dest \[ . Mask \] , \[ - \] src0 \[ . свиззле \] , \[ - \] src1 \[ . свиззле \] , \[ - \] src2 \[ . свиззле</span><span class="sxs-lookup"><span data-stu-id="3891f-105">imad dest\[.mask\], \[-\]src0\[.swizzle\], \[-\]src1\[.swizzle\], \[-\]src2\[.swizzle</span></span> |
|---------------------------------------------------------------------------------------|



 



| <span data-ttu-id="3891f-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="3891f-106">Item</span></span>                                                            | <span data-ttu-id="3891f-107">Описание</span><span class="sxs-lookup"><span data-stu-id="3891f-107">Description</span></span>                                                         |
|-----------------------------------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="3891f-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="3891f-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="3891f-109">\[в \] результате операции.</span><span class="sxs-lookup"><span data-stu-id="3891f-109">\[in\] The result of the operation.</span></span><br/>                      |
| <span data-ttu-id="3891f-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="3891f-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="3891f-111">\[\]значение для перемножения с *src1*.</span><span class="sxs-lookup"><span data-stu-id="3891f-111">\[in\] Value to multiply with *src1*.</span></span><br/>                    |
| <span data-ttu-id="3891f-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="3891f-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="3891f-113">\[\]значение для перемножения с *src0*.</span><span class="sxs-lookup"><span data-stu-id="3891f-113">\[in\] Value to multiply with *src0*.</span></span><br/>                    |
| <span data-ttu-id="3891f-114"><span id="src2"></span><span id="SRC2"></span>*src2*</span><span class="sxs-lookup"><span data-stu-id="3891f-114"><span id="src2"></span><span id="SRC2"></span>*src2*</span></span><br/> | <span data-ttu-id="3891f-115">\[в \] поле значение, добавляемое к продукту *src0* и *src1*.</span><span class="sxs-lookup"><span data-stu-id="3891f-115">\[in\] Value to add to the product of *src0* and *src1*.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="3891f-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="3891f-116">Remarks</span></span>

<span data-ttu-id="3891f-117">Компонентно-ориентированное [imul](imul--sm4---asm-.md) для 32-разрядных операндов *src0* и *src1* (со знаком), сохраняя низкий 32-бит (на компонент) результата, за которым следует [IAdd](iadd--sm4---asm-.md) *src2*, создающий верный низкий 32-разрядный (на компонент) результат.</span><span class="sxs-lookup"><span data-stu-id="3891f-117">Component-wise [imul](imul--sm4---asm-.md) of 32-bit operands *src0* and *src1* (signed), keeping low 32-bits (per component) of the result, followed by an [iadd](iadd--sm4---asm-.md) of *src2*, producing the correct low 32-bit (per component) result.</span></span> <span data-ttu-id="3891f-118">32-разрядные результаты помещаются в *dest*.</span><span class="sxs-lookup"><span data-stu-id="3891f-118">The 32-bit results are placed in *dest*.</span></span>

<span data-ttu-id="3891f-119">Необязательный модификатор отрицания в исходных операндах перед выполнением арифметической операции принимает 2 дополнения.</span><span class="sxs-lookup"><span data-stu-id="3891f-119">Optional negate modifier on source operands takes 2's complement before performing arithmetic operation.</span></span>

<span data-ttu-id="3891f-120">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="3891f-120">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="3891f-121">Вершинный построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="3891f-121">Vertex Shader</span></span> | <span data-ttu-id="3891f-122">Шейдер геометрии</span><span class="sxs-lookup"><span data-stu-id="3891f-122">Geometry Shader</span></span> | <span data-ttu-id="3891f-123">Построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="3891f-123">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="3891f-124">x</span><span class="sxs-lookup"><span data-stu-id="3891f-124">x</span></span>             | <span data-ttu-id="3891f-125">x</span><span class="sxs-lookup"><span data-stu-id="3891f-125">x</span></span>               | <span data-ttu-id="3891f-126">x</span><span class="sxs-lookup"><span data-stu-id="3891f-126">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="3891f-127">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="3891f-127">Minimum Shader Model</span></span>

<span data-ttu-id="3891f-128">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="3891f-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="3891f-129">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="3891f-129">Shader Model</span></span>                                              | <span data-ttu-id="3891f-130">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="3891f-130">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="3891f-131">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="3891f-131">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="3891f-132">да</span><span class="sxs-lookup"><span data-stu-id="3891f-132">yes</span></span>       |
| [<span data-ttu-id="3891f-133">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="3891f-133">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="3891f-134">да</span><span class="sxs-lookup"><span data-stu-id="3891f-134">yes</span></span>       |
| [<span data-ttu-id="3891f-135">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="3891f-135">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="3891f-136">да</span><span class="sxs-lookup"><span data-stu-id="3891f-136">yes</span></span>       |
| [<span data-ttu-id="3891f-137">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3891f-137">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="3891f-138">Нет</span><span class="sxs-lookup"><span data-stu-id="3891f-138">no</span></span>        |
| [<span data-ttu-id="3891f-139">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3891f-139">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="3891f-140">Нет</span><span class="sxs-lookup"><span data-stu-id="3891f-140">no</span></span>        |
| [<span data-ttu-id="3891f-141">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3891f-141">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="3891f-142">Нет</span><span class="sxs-lookup"><span data-stu-id="3891f-142">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="3891f-143">См. также</span><span class="sxs-lookup"><span data-stu-id="3891f-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3891f-144">Сборка Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3891f-144">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





