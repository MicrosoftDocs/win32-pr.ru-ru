---
title: и (SM4-ASM)
description: Битовый AND.
ms.assetid: 403DA289-E2CF-4736-8882-4131F884F777
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7ec9474322aafda2706502898902d01d0e13143
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "103784980"
---
# <a name="and-sm4---asm"></a><span data-ttu-id="84b3b-103">и (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="84b3b-103">and (sm4 - asm)</span></span>

<span data-ttu-id="84b3b-104">Побитовое **и**.</span><span class="sxs-lookup"><span data-stu-id="84b3b-104">Bitwise **AND**.</span></span>



| <span data-ttu-id="84b3b-105">и dest \[ . Mask \] , src0 \[ . свиззле \] , src1 \[ . свиззле\]</span><span class="sxs-lookup"><span data-stu-id="84b3b-105">and dest\[.mask\], src0\[.swizzle\], src1\[.swizzle\]</span></span> |
|-------------------------------------------------------|



 



| <span data-ttu-id="84b3b-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="84b3b-106">Item</span></span>                                                            | <span data-ttu-id="84b3b-107">Описание</span><span class="sxs-lookup"><span data-stu-id="84b3b-107">Description</span></span>                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="84b3b-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="84b3b-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="84b3b-109">\[в \] адресе результата операции.</span><span class="sxs-lookup"><span data-stu-id="84b3b-109">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="84b3b-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="84b3b-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="84b3b-111">\[в \] 32-разрядном значении **и** с *src1*.</span><span class="sxs-lookup"><span data-stu-id="84b3b-111">\[in\] The 32-bit value to **AND** with *src1*.</span></span><br/>    |
| <span data-ttu-id="84b3b-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="84b3b-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="84b3b-113">\[в \] 32-разрядном значении **и** с *src0*.</span><span class="sxs-lookup"><span data-stu-id="84b3b-113">\[in\] The 32-bit value to **AND** with *src0*.</span></span><br/>    |



 

## <a name="remarks"></a><span data-ttu-id="84b3b-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="84b3b-114">Remarks</span></span>

<span data-ttu-id="84b3b-115">Покомпонентное логическое **и** для каждой пары 32-разрядных значений из *src0* и *src1*.</span><span class="sxs-lookup"><span data-stu-id="84b3b-115">Component-wise logical **AND** of each pair of 32-bit values from *src0* and *src1*.</span></span> <span data-ttu-id="84b3b-116">32-разрядные результаты помещаются в *dest*.</span><span class="sxs-lookup"><span data-stu-id="84b3b-116">The 32-bit results are placed in *dest*.</span></span>

<span data-ttu-id="84b3b-117">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="84b3b-117">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="84b3b-118">Вершинный построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="84b3b-118">Vertex Shader</span></span> | <span data-ttu-id="84b3b-119">Шейдер геометрии</span><span class="sxs-lookup"><span data-stu-id="84b3b-119">Geometry Shader</span></span> | <span data-ttu-id="84b3b-120">Построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="84b3b-120">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="84b3b-121">x</span><span class="sxs-lookup"><span data-stu-id="84b3b-121">x</span></span>             | <span data-ttu-id="84b3b-122">x</span><span class="sxs-lookup"><span data-stu-id="84b3b-122">x</span></span>               | <span data-ttu-id="84b3b-123">x</span><span class="sxs-lookup"><span data-stu-id="84b3b-123">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="84b3b-124">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="84b3b-124">Minimum Shader Model</span></span>

<span data-ttu-id="84b3b-125">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="84b3b-125">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="84b3b-126">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="84b3b-126">Shader Model</span></span>                                              | <span data-ttu-id="84b3b-127">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="84b3b-127">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="84b3b-128">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="84b3b-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="84b3b-129">да</span><span class="sxs-lookup"><span data-stu-id="84b3b-129">yes</span></span>       |
| [<span data-ttu-id="84b3b-130">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="84b3b-130">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="84b3b-131">да</span><span class="sxs-lookup"><span data-stu-id="84b3b-131">yes</span></span>       |
| [<span data-ttu-id="84b3b-132">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="84b3b-132">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="84b3b-133">да</span><span class="sxs-lookup"><span data-stu-id="84b3b-133">yes</span></span>       |
| [<span data-ttu-id="84b3b-134">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="84b3b-134">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="84b3b-135">Нет</span><span class="sxs-lookup"><span data-stu-id="84b3b-135">no</span></span>        |
| [<span data-ttu-id="84b3b-136">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="84b3b-136">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="84b3b-137">Нет</span><span class="sxs-lookup"><span data-stu-id="84b3b-137">no</span></span>        |
| [<span data-ttu-id="84b3b-138">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="84b3b-138">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="84b3b-139">Нет</span><span class="sxs-lookup"><span data-stu-id="84b3b-139">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="84b3b-140">См. также</span><span class="sxs-lookup"><span data-stu-id="84b3b-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="84b3b-141">Сборка Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="84b3b-141">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





