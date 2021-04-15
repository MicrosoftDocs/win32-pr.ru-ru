---
title: ушр (SM5-ASM)
description: Сдвиг вправо. | ушр (SM5-ASM)
ms.assetid: C695CB6C-A6C9-4DC8-8EBE-70A0CFFC4981
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f33c627ec4aa985b5ac8a27cf0babd6219c9247c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986504"
---
# <a name="ushr-sm5---asm"></a><span data-ttu-id="eb285-104">ушр (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="eb285-104">ushr (sm5 - asm)</span></span>

<span data-ttu-id="eb285-105">Сдвиг вправо.</span><span class="sxs-lookup"><span data-stu-id="eb285-105">Shift right.</span></span>



| <span data-ttu-id="eb285-106">убфе dest \[ . Mask \] , src0 \[ . свиззле \] , src1 \[ . свиззле\]</span><span class="sxs-lookup"><span data-stu-id="eb285-106">ubfe dest\[.mask\], src0\[.swizzle\], src1\[.swizzle\]</span></span> |
|--------------------------------------------------------|



 



| <span data-ttu-id="eb285-107">Элемент</span><span class="sxs-lookup"><span data-stu-id="eb285-107">Item</span></span>                                                            | <span data-ttu-id="eb285-108">Описание</span><span class="sxs-lookup"><span data-stu-id="eb285-108">Description</span></span>                                                                  |
|-----------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="eb285-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="eb285-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="eb285-110">\[в \] содержит результаты выполнения инструкции.</span><span class="sxs-lookup"><span data-stu-id="eb285-110">\[in\] Contains the results of the instruction.</span></span><br/>                   |
| <span data-ttu-id="eb285-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="eb285-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="eb285-112">\[в \] 32-разрядных значениях для сдвига.</span><span class="sxs-lookup"><span data-stu-id="eb285-112">\[in\] The 32-bit values to shift.</span></span><br/>                                |
| <span data-ttu-id="eb285-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="eb285-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="eb285-114">\[в \] ЛСБ 5 битов укажите число битов для сдвига (0-31).</span><span class="sxs-lookup"><span data-stu-id="eb285-114">\[in\] The LSB 5 bits provide the number of bits to shift (0-31).</span></span><br/> |



 

<span data-ttu-id="eb285-115">Эта инструкция выполняет покомпонентную смену каждого 32-битного значения в *src0* прямо на число беззнаковых разрядов, обеспечиваемое количеством битов ЛСБ 5 (диапазон 0-31) в *src1*, вставляя 0.</span><span class="sxs-lookup"><span data-stu-id="eb285-115">This instruction performs a component-wise shift of each 32-bit value in *src0* right by an unsigned integer bit count provided by the LSB 5 bits (0-31 range) in *src1*, inserting 0.</span></span> <span data-ttu-id="eb285-116">Результаты 32-бит на компонент помещаются в *dest*.</span><span class="sxs-lookup"><span data-stu-id="eb285-116">The 32-bit per component results is placed in *dest*.</span></span>

<span data-ttu-id="eb285-117">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="eb285-117">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="eb285-118">Вершина</span><span class="sxs-lookup"><span data-stu-id="eb285-118">Vertex</span></span> | <span data-ttu-id="eb285-119">Поверхности</span><span class="sxs-lookup"><span data-stu-id="eb285-119">Hull</span></span> | <span data-ttu-id="eb285-120">Домен</span><span class="sxs-lookup"><span data-stu-id="eb285-120">Domain</span></span> | <span data-ttu-id="eb285-121">Геометрия</span><span class="sxs-lookup"><span data-stu-id="eb285-121">Geometry</span></span> | <span data-ttu-id="eb285-122">Пиксель</span><span class="sxs-lookup"><span data-stu-id="eb285-122">Pixel</span></span> | <span data-ttu-id="eb285-123">Вычисления</span><span class="sxs-lookup"><span data-stu-id="eb285-123">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="eb285-124">X</span><span class="sxs-lookup"><span data-stu-id="eb285-124">X</span></span>      | <span data-ttu-id="eb285-125">X</span><span class="sxs-lookup"><span data-stu-id="eb285-125">X</span></span>    | <span data-ttu-id="eb285-126">X</span><span class="sxs-lookup"><span data-stu-id="eb285-126">X</span></span>      | <span data-ttu-id="eb285-127">X</span><span class="sxs-lookup"><span data-stu-id="eb285-127">X</span></span>        | <span data-ttu-id="eb285-128">X</span><span class="sxs-lookup"><span data-stu-id="eb285-128">X</span></span>     | <span data-ttu-id="eb285-129">X</span><span class="sxs-lookup"><span data-stu-id="eb285-129">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="eb285-130">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="eb285-130">Minimum Shader Model</span></span>

<span data-ttu-id="eb285-131">Эта инструкция поддерживается в следующих моделях шейдеров:</span><span class="sxs-lookup"><span data-stu-id="eb285-131">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="eb285-132">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="eb285-132">Shader Model</span></span>                                              | <span data-ttu-id="eb285-133">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="eb285-133">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="eb285-134">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="eb285-134">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="eb285-135">да</span><span class="sxs-lookup"><span data-stu-id="eb285-135">yes</span></span>       |
| [<span data-ttu-id="eb285-136">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="eb285-136">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="eb285-137">Нет</span><span class="sxs-lookup"><span data-stu-id="eb285-137">no</span></span>        |
| [<span data-ttu-id="eb285-138">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="eb285-138">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="eb285-139">Нет</span><span class="sxs-lookup"><span data-stu-id="eb285-139">no</span></span>        |
| [<span data-ttu-id="eb285-140">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="eb285-140">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="eb285-141">Нет</span><span class="sxs-lookup"><span data-stu-id="eb285-141">no</span></span>        |
| [<span data-ttu-id="eb285-142">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="eb285-142">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="eb285-143">Нет</span><span class="sxs-lookup"><span data-stu-id="eb285-143">no</span></span>        |
| [<span data-ttu-id="eb285-144">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="eb285-144">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="eb285-145">Нет</span><span class="sxs-lookup"><span data-stu-id="eb285-145">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="eb285-146">См. также</span><span class="sxs-lookup"><span data-stu-id="eb285-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eb285-147">Сборка Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="eb285-147">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





