---
title: ishl (sm5 — asm)
description: Сдвиг влево. | Ишл (SM5-ASM)
ms.assetid: 3EE669BA-252D-4617-85B0-AEBB7F7E4C5E
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 230034e66ca9adfbd6c94cc99351b485c6577fdf
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104353125"
---
# <a name="ishl-sm5---asm"></a><span data-ttu-id="0997c-104">ishl (sm5 — asm)</span><span class="sxs-lookup"><span data-stu-id="0997c-104">ishl (sm5 - asm)</span></span>

<span data-ttu-id="0997c-105">Сдвиг влево.</span><span class="sxs-lookup"><span data-stu-id="0997c-105">Shift left.</span></span>



| <span data-ttu-id="0997c-106">Ишл dest \[ . Mask \] , src0 \[ . свиззле \] , src1 \[ . свиззле\]</span><span class="sxs-lookup"><span data-stu-id="0997c-106">ishl dest\[.mask\], src0\[.swizzle\], src1\[.swizzle\]</span></span> |
|--------------------------------------------------------|



 



| <span data-ttu-id="0997c-107">Элемент</span><span class="sxs-lookup"><span data-stu-id="0997c-107">Item</span></span>                                                            | <span data-ttu-id="0997c-108">Описание</span><span class="sxs-lookup"><span data-stu-id="0997c-108">Description</span></span>                                          |
|-----------------------------------------------------------------|------------------------------------------------------|
| <span data-ttu-id="0997c-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="0997c-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="0997c-110">\[в \] содержит результаты сдвига.</span><span class="sxs-lookup"><span data-stu-id="0997c-110">\[in\] Contains the results of the shift.</span></span><br/> |
| <span data-ttu-id="0997c-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="0997c-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="0997c-112">\[в \] 32-разрядных значениях для сдвига.</span><span class="sxs-lookup"><span data-stu-id="0997c-112">\[in\] The 32-bit values to shift.</span></span><br/>       |
| <span data-ttu-id="0997c-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="0997c-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="0997c-114">\[в \] поле число битов для сдвига.</span><span class="sxs-lookup"><span data-stu-id="0997c-114">\[in\] The number of bits to shift.</span></span><br/>        |



 

## <a name="remarks"></a><span data-ttu-id="0997c-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="0997c-115">Remarks</span></span>

<span data-ttu-id="0997c-116">Эта инструкция выполняет покомпонентную смену каждого 32-битного значения в *src0* влево на число целых чисел без знака, обеспечиваемое значением ЛСБ 5 бит (диапазон 0-31) в *src1*, вставляя 0.</span><span class="sxs-lookup"><span data-stu-id="0997c-116">This instruction performs a component-wise shift of each 32-bit value in *src0* left by an unsigned integer bit count provided by the LSB 5 bits (0-31 range) in *src1*, inserting 0.</span></span> <span data-ttu-id="0997c-117">Результаты 32-бит на компонент помещаются в *dest*.</span><span class="sxs-lookup"><span data-stu-id="0997c-117">The 32-bit per component results are placed in *dest*.</span></span>

<span data-ttu-id="0997c-118">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="0997c-118">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="0997c-119">Вершина</span><span class="sxs-lookup"><span data-stu-id="0997c-119">Vertex</span></span> | <span data-ttu-id="0997c-120">Поверхности</span><span class="sxs-lookup"><span data-stu-id="0997c-120">Hull</span></span> | <span data-ttu-id="0997c-121">Домен</span><span class="sxs-lookup"><span data-stu-id="0997c-121">Domain</span></span> | <span data-ttu-id="0997c-122">Геометрия</span><span class="sxs-lookup"><span data-stu-id="0997c-122">Geometry</span></span> | <span data-ttu-id="0997c-123">Пиксель</span><span class="sxs-lookup"><span data-stu-id="0997c-123">Pixel</span></span> | <span data-ttu-id="0997c-124">Вычисления</span><span class="sxs-lookup"><span data-stu-id="0997c-124">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="0997c-125">X</span><span class="sxs-lookup"><span data-stu-id="0997c-125">X</span></span>      | <span data-ttu-id="0997c-126">X</span><span class="sxs-lookup"><span data-stu-id="0997c-126">X</span></span>    | <span data-ttu-id="0997c-127">X</span><span class="sxs-lookup"><span data-stu-id="0997c-127">X</span></span>      | <span data-ttu-id="0997c-128">X</span><span class="sxs-lookup"><span data-stu-id="0997c-128">X</span></span>        | <span data-ttu-id="0997c-129">X</span><span class="sxs-lookup"><span data-stu-id="0997c-129">X</span></span>     | <span data-ttu-id="0997c-130">X</span><span class="sxs-lookup"><span data-stu-id="0997c-130">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="0997c-131">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="0997c-131">Minimum Shader Model</span></span>

<span data-ttu-id="0997c-132">Эта инструкция поддерживается в следующих моделях шейдеров:</span><span class="sxs-lookup"><span data-stu-id="0997c-132">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="0997c-133">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="0997c-133">Shader Model</span></span>                                              | <span data-ttu-id="0997c-134">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="0997c-134">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="0997c-135">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="0997c-135">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="0997c-136">да</span><span class="sxs-lookup"><span data-stu-id="0997c-136">yes</span></span>       |
| [<span data-ttu-id="0997c-137">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="0997c-137">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="0997c-138">Нет</span><span class="sxs-lookup"><span data-stu-id="0997c-138">no</span></span>        |
| [<span data-ttu-id="0997c-139">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="0997c-139">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="0997c-140">Нет</span><span class="sxs-lookup"><span data-stu-id="0997c-140">no</span></span>        |
| [<span data-ttu-id="0997c-141">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0997c-141">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="0997c-142">Нет</span><span class="sxs-lookup"><span data-stu-id="0997c-142">no</span></span>        |
| [<span data-ttu-id="0997c-143">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0997c-143">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="0997c-144">Нет</span><span class="sxs-lookup"><span data-stu-id="0997c-144">no</span></span>        |
| [<span data-ttu-id="0997c-145">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0997c-145">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="0997c-146">Нет</span><span class="sxs-lookup"><span data-stu-id="0997c-146">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="0997c-147">См. также</span><span class="sxs-lookup"><span data-stu-id="0997c-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0997c-148">Сборка Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0997c-148">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





