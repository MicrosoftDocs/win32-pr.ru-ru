---
title: ишр (SM4-ASM)
description: Арифметический сдвиг вправо (расширение знака). | ишр (SM4-ASM)
ms.assetid: AFE46BBA-A6B2-4691-A3F4-A4141F1578DB
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7516543c5501ed886c5c1fa98d093062e3099a0f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104998246"
---
# <a name="ishr-sm4---asm"></a><span data-ttu-id="a90f7-104">ишр (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="a90f7-104">ishr (sm4 - asm)</span></span>

<span data-ttu-id="a90f7-105">Арифметический сдвиг вправо (расширение знака).</span><span class="sxs-lookup"><span data-stu-id="a90f7-105">Arithmetic shift right (sign extending).</span></span>



| <span data-ttu-id="a90f7-106">ишр dest \[ . Mask \] , src0 \[ . свиззле \] , src1. Выбор \_ компонента</span><span class="sxs-lookup"><span data-stu-id="a90f7-106">ishr dest\[.mask\], src0\[.swizzle\], src1.select\_component</span></span> |
|--------------------------------------------------------------|



 



| <span data-ttu-id="a90f7-107">Элемент</span><span class="sxs-lookup"><span data-stu-id="a90f7-107">Item</span></span>                                                            | <span data-ttu-id="a90f7-108">Описание</span><span class="sxs-lookup"><span data-stu-id="a90f7-108">Description</span></span>                                             |
|-----------------------------------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="a90f7-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="a90f7-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="a90f7-110">\[в \] содержит результат операции.</span><span class="sxs-lookup"><span data-stu-id="a90f7-110">\[in\] Contains the result of the operation.</span></span><br/> |
| <span data-ttu-id="a90f7-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="a90f7-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="a90f7-112">\[в \] содержит значение для сдвига.</span><span class="sxs-lookup"><span data-stu-id="a90f7-112">\[in\] Contains the value to be shifted.</span></span><br/>     |
| <span data-ttu-id="a90f7-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="a90f7-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="a90f7-114">\[в \] содержит сумму сдвига.</span><span class="sxs-lookup"><span data-stu-id="a90f7-114">\[in\] Contains the shift amount.</span></span><br/>            |



 

## <a name="remarks"></a><span data-ttu-id="a90f7-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="a90f7-115">Remarks</span></span>

<span data-ttu-id="a90f7-116">Эта инструкция выполняет арифметический сдвиг для каждого 32-разрядного значения в *src0* прямо за пределами целого числа без знака, предоставленного числом битов ЛСБ 5 (диапазон 0-31) в *src1. Select \_ ,* реплицирует значение бита 31.</span><span class="sxs-lookup"><span data-stu-id="a90f7-116">This instruction performs a component-wise arithmetic shift of each 32-bit value in *src0* right by an unsigned integer bit count provided by the LSB 5 bits (0-31 range) in *src1.select\_component*, replicating the value of bit 31.</span></span> <span data-ttu-id="a90f7-117">Результат 32-бит на компонент помещается в *dest*.</span><span class="sxs-lookup"><span data-stu-id="a90f7-117">The 32-bit per component result is placed in *dest*.</span></span> <span data-ttu-id="a90f7-118">Счетчик — это скалярное значение, применяемое ко всем компонентам.</span><span class="sxs-lookup"><span data-stu-id="a90f7-118">The count is a scalar value applied to all components.</span></span>

<span data-ttu-id="a90f7-119">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="a90f7-119">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="a90f7-120">Вершинный построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="a90f7-120">Vertex Shader</span></span> | <span data-ttu-id="a90f7-121">Шейдер геометрии</span><span class="sxs-lookup"><span data-stu-id="a90f7-121">Geometry Shader</span></span> | <span data-ttu-id="a90f7-122">Построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="a90f7-122">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="a90f7-123">x</span><span class="sxs-lookup"><span data-stu-id="a90f7-123">x</span></span>             | <span data-ttu-id="a90f7-124">x</span><span class="sxs-lookup"><span data-stu-id="a90f7-124">x</span></span>               | <span data-ttu-id="a90f7-125">x</span><span class="sxs-lookup"><span data-stu-id="a90f7-125">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="a90f7-126">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="a90f7-126">Minimum Shader Model</span></span>

<span data-ttu-id="a90f7-127">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="a90f7-127">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="a90f7-128">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="a90f7-128">Shader Model</span></span>                                              | <span data-ttu-id="a90f7-129">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="a90f7-129">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="a90f7-130">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="a90f7-130">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="a90f7-131">да</span><span class="sxs-lookup"><span data-stu-id="a90f7-131">yes</span></span>       |
| [<span data-ttu-id="a90f7-132">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="a90f7-132">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="a90f7-133">да</span><span class="sxs-lookup"><span data-stu-id="a90f7-133">yes</span></span>       |
| [<span data-ttu-id="a90f7-134">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="a90f7-134">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="a90f7-135">да</span><span class="sxs-lookup"><span data-stu-id="a90f7-135">yes</span></span>       |
| [<span data-ttu-id="a90f7-136">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a90f7-136">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="a90f7-137">Нет</span><span class="sxs-lookup"><span data-stu-id="a90f7-137">no</span></span>        |
| [<span data-ttu-id="a90f7-138">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a90f7-138">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="a90f7-139">Нет</span><span class="sxs-lookup"><span data-stu-id="a90f7-139">no</span></span>        |
| [<span data-ttu-id="a90f7-140">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a90f7-140">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="a90f7-141">Нет</span><span class="sxs-lookup"><span data-stu-id="a90f7-141">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="a90f7-142">См. также</span><span class="sxs-lookup"><span data-stu-id="a90f7-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a90f7-143">Сборка Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a90f7-143">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





