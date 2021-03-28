---
title: XOR (SM4-ASM)
description: Битовая операция XOR.
ms.assetid: 6B949653-6DDA-402B-8ABE-B93858B68470
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7a998bd1e95793f463d7f234b464a542bed4fc0
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104412135"
---
# <a name="xor-sm4---asm"></a><span data-ttu-id="7ac1a-103">XOR (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="7ac1a-103">xor (sm4 - asm)</span></span>

<span data-ttu-id="7ac1a-104">Битовая операция XOR.</span><span class="sxs-lookup"><span data-stu-id="7ac1a-104">Bitwise xor.</span></span>



| <span data-ttu-id="7ac1a-105">XOR dest \[ . Mask \] , src0 \[ . свиззле \] , src1 \[ . свиззле\]</span><span class="sxs-lookup"><span data-stu-id="7ac1a-105">xor dest\[.mask\], src0\[.swizzle\], src1\[.swizzle\]</span></span> |
|-------------------------------------------------------|



 



| <span data-ttu-id="7ac1a-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="7ac1a-106">Item</span></span>                                                            | <span data-ttu-id="7ac1a-107">Описание</span><span class="sxs-lookup"><span data-stu-id="7ac1a-107">Description</span></span>                                          |
|-----------------------------------------------------------------|------------------------------------------------------|
| <span data-ttu-id="7ac1a-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="7ac1a-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="7ac1a-109">\[в \] результате операции.</span><span class="sxs-lookup"><span data-stu-id="7ac1a-109">\[in\] The result of the operation.</span></span><br/>       |
| <span data-ttu-id="7ac1a-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="7ac1a-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="7ac1a-111">\[в \] компонентах для XOR с *src1*.</span><span class="sxs-lookup"><span data-stu-id="7ac1a-111">\[in\] The components to XOR with *src1*.</span></span><br/> |
| <span data-ttu-id="7ac1a-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="7ac1a-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="7ac1a-113">\[в \] компонентах для XOR с *src0*.</span><span class="sxs-lookup"><span data-stu-id="7ac1a-113">\[in\] The components to XOR with *src0*.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="7ac1a-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="7ac1a-114">Remarks</span></span>

<span data-ttu-id="7ac1a-115">Эта инструкция выполняет покомпонентное Логическое исключающее XOR каждой пары 32-разрядных значений из *src0* и *src1*.</span><span class="sxs-lookup"><span data-stu-id="7ac1a-115">This instruction performs a component-wise logical XOR of each pair of 32-bit values from *src0* and *src1*.</span></span> <span data-ttu-id="7ac1a-116">32-разрядные результаты помещаются в *dest*.</span><span class="sxs-lookup"><span data-stu-id="7ac1a-116">32-bit results are placed in *dest*.</span></span>

<span data-ttu-id="7ac1a-117">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="7ac1a-117">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="7ac1a-118">Вершинный построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="7ac1a-118">Vertex Shader</span></span> | <span data-ttu-id="7ac1a-119">Шейдер геометрии</span><span class="sxs-lookup"><span data-stu-id="7ac1a-119">Geometry Shader</span></span> | <span data-ttu-id="7ac1a-120">Построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="7ac1a-120">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="7ac1a-121">x</span><span class="sxs-lookup"><span data-stu-id="7ac1a-121">x</span></span>             | <span data-ttu-id="7ac1a-122">x</span><span class="sxs-lookup"><span data-stu-id="7ac1a-122">x</span></span>               | <span data-ttu-id="7ac1a-123">x</span><span class="sxs-lookup"><span data-stu-id="7ac1a-123">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="7ac1a-124">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="7ac1a-124">Minimum Shader Model</span></span>

<span data-ttu-id="7ac1a-125">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="7ac1a-125">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="7ac1a-126">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="7ac1a-126">Shader Model</span></span>                                              | <span data-ttu-id="7ac1a-127">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="7ac1a-127">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="7ac1a-128">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="7ac1a-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="7ac1a-129">да</span><span class="sxs-lookup"><span data-stu-id="7ac1a-129">yes</span></span>       |
| [<span data-ttu-id="7ac1a-130">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="7ac1a-130">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="7ac1a-131">да</span><span class="sxs-lookup"><span data-stu-id="7ac1a-131">yes</span></span>       |
| [<span data-ttu-id="7ac1a-132">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="7ac1a-132">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="7ac1a-133">да</span><span class="sxs-lookup"><span data-stu-id="7ac1a-133">yes</span></span>       |
| [<span data-ttu-id="7ac1a-134">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7ac1a-134">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="7ac1a-135">Нет</span><span class="sxs-lookup"><span data-stu-id="7ac1a-135">no</span></span>        |
| [<span data-ttu-id="7ac1a-136">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7ac1a-136">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="7ac1a-137">Нет</span><span class="sxs-lookup"><span data-stu-id="7ac1a-137">no</span></span>        |
| [<span data-ttu-id="7ac1a-138">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7ac1a-138">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="7ac1a-139">Нет</span><span class="sxs-lookup"><span data-stu-id="7ac1a-139">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="7ac1a-140">См. также</span><span class="sxs-lookup"><span data-stu-id="7ac1a-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7ac1a-141">Сборка Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7ac1a-141">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





