---
title: ишр (SM5-ASM)
description: Арифметический сдвиг вправо (расширение знака). | ишр (SM5-ASM)
ms.assetid: 8124B6C3-4576-4616-85A9-A2DD19EB6BB9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06df958b2e5c6e9cdd2a4dfb3d35c8112453ce9f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104998243"
---
# <a name="ishr-sm5---asm"></a><span data-ttu-id="b4592-104">ишр (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="b4592-104">ishr (sm5 - asm)</span></span>

<span data-ttu-id="b4592-105">Арифметический сдвиг вправо (расширение знака).</span><span class="sxs-lookup"><span data-stu-id="b4592-105">Arithmetic shift right (sign extending).</span></span>



| <span data-ttu-id="b4592-106">Ишл dest \[ . Mask \] , src0 \[ . свиззле \] , src1 \[ . свиззле\]</span><span class="sxs-lookup"><span data-stu-id="b4592-106">ishl dest\[.mask\], src0\[.swizzle\], src1\[.swizzle\]</span></span> |
|--------------------------------------------------------|



 



| <span data-ttu-id="b4592-107">Элемент</span><span class="sxs-lookup"><span data-stu-id="b4592-107">Item</span></span>                                                            | <span data-ttu-id="b4592-108">Описание</span><span class="sxs-lookup"><span data-stu-id="b4592-108">Description</span></span>                                          |
|-----------------------------------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b4592-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="b4592-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="b4592-110">\[в \] содержит результаты сдвига.</span><span class="sxs-lookup"><span data-stu-id="b4592-110">\[in\] Contains the results of the shift.</span></span><br/> |
| <span data-ttu-id="b4592-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="b4592-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="b4592-112">\[в \] поле число битов для сдвига.</span><span class="sxs-lookup"><span data-stu-id="b4592-112">\[in\] The number of bits to shift.</span></span><br/>       |
| <span data-ttu-id="b4592-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="b4592-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="b4592-114">\[в \] 32-разрядных значениях для сдвига.</span><span class="sxs-lookup"><span data-stu-id="b4592-114">\[in\] The 32-bit values to shift.</span></span><br/>        |



 

## <a name="remarks"></a><span data-ttu-id="b4592-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="b4592-115">Remarks</span></span>

<span data-ttu-id="b4592-116">Эта инструкция выполняет арифметический сдвиг для каждого 32-разрядного значения в *src0* прямо на основе числа беззнаковых битов целого числа, предоставляемого ЛСБ 5 бит (диапазон 0-31) в *src1*, реплицирует значение бита 31.</span><span class="sxs-lookup"><span data-stu-id="b4592-116">This instruction performs a component-wise arithmetic shift of each 32-bit value in *src0* right by an unsigned integer bit count provided by the LSB 5 bits (0-31 range) in *src1*, replicating the value of bit 31.</span></span> <span data-ttu-id="b4592-117">Результат 32-бит на компонент помещается в *dest*.</span><span class="sxs-lookup"><span data-stu-id="b4592-117">The 32-bit per component result is placed in *dest*.</span></span>

<span data-ttu-id="b4592-118">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="b4592-118">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="b4592-119">Вершина</span><span class="sxs-lookup"><span data-stu-id="b4592-119">Vertex</span></span> | <span data-ttu-id="b4592-120">Поверхности</span><span class="sxs-lookup"><span data-stu-id="b4592-120">Hull</span></span> | <span data-ttu-id="b4592-121">Домен</span><span class="sxs-lookup"><span data-stu-id="b4592-121">Domain</span></span> | <span data-ttu-id="b4592-122">Геометрия</span><span class="sxs-lookup"><span data-stu-id="b4592-122">Geometry</span></span> | <span data-ttu-id="b4592-123">Пиксель</span><span class="sxs-lookup"><span data-stu-id="b4592-123">Pixel</span></span> | <span data-ttu-id="b4592-124">Вычисления</span><span class="sxs-lookup"><span data-stu-id="b4592-124">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="b4592-125">X</span><span class="sxs-lookup"><span data-stu-id="b4592-125">X</span></span>      | <span data-ttu-id="b4592-126">X</span><span class="sxs-lookup"><span data-stu-id="b4592-126">X</span></span>    | <span data-ttu-id="b4592-127">X</span><span class="sxs-lookup"><span data-stu-id="b4592-127">X</span></span>      | <span data-ttu-id="b4592-128">X</span><span class="sxs-lookup"><span data-stu-id="b4592-128">X</span></span>        | <span data-ttu-id="b4592-129">X</span><span class="sxs-lookup"><span data-stu-id="b4592-129">X</span></span>     | <span data-ttu-id="b4592-130">X</span><span class="sxs-lookup"><span data-stu-id="b4592-130">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="b4592-131">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="b4592-131">Minimum Shader Model</span></span>

<span data-ttu-id="b4592-132">Эта инструкция поддерживается в следующих моделях шейдеров:</span><span class="sxs-lookup"><span data-stu-id="b4592-132">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="b4592-133">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="b4592-133">Shader Model</span></span>                                              | <span data-ttu-id="b4592-134">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="b4592-134">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="b4592-135">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="b4592-135">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="b4592-136">да</span><span class="sxs-lookup"><span data-stu-id="b4592-136">yes</span></span>       |
| [<span data-ttu-id="b4592-137">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="b4592-137">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="b4592-138">Нет</span><span class="sxs-lookup"><span data-stu-id="b4592-138">no</span></span>        |
| [<span data-ttu-id="b4592-139">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="b4592-139">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="b4592-140">Нет</span><span class="sxs-lookup"><span data-stu-id="b4592-140">no</span></span>        |
| [<span data-ttu-id="b4592-141">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b4592-141">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="b4592-142">Нет</span><span class="sxs-lookup"><span data-stu-id="b4592-142">no</span></span>        |
| [<span data-ttu-id="b4592-143">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b4592-143">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="b4592-144">Нет</span><span class="sxs-lookup"><span data-stu-id="b4592-144">no</span></span>        |
| [<span data-ttu-id="b4592-145">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b4592-145">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="b4592-146">Нет</span><span class="sxs-lookup"><span data-stu-id="b4592-146">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="b4592-147">См. также</span><span class="sxs-lookup"><span data-stu-id="b4592-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b4592-148">Сборка Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b4592-148">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





