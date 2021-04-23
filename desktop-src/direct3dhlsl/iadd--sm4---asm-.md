---
title: IAdd (SM4-ASM)
description: Сложение целых чисел.
ms.assetid: EF78EA65-DC16-469A-9E45-52844FF4BD93
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b593484aa7c1ef376bb5febf141b144ddef338e0
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104412215"
---
# <a name="iadd-sm4---asm"></a><span data-ttu-id="65cef-103">IAdd (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="65cef-103">iadd (sm4 - asm)</span></span>

<span data-ttu-id="65cef-104">Сложение целых чисел.</span><span class="sxs-lookup"><span data-stu-id="65cef-104">Integer addition.</span></span>



| <span data-ttu-id="65cef-105">IAdd dest \[ . Mask \] , \[ - \] src0 \[ . свиззле \] , \[ - \] src1 \[ . свиззле\]</span><span class="sxs-lookup"><span data-stu-id="65cef-105">iadd dest\[.mask\], \[-\]src0\[.swizzle\], \[-\]src1\[.swizzle\]</span></span> |
|------------------------------------------------------------------|



 



| <span data-ttu-id="65cef-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="65cef-106">Item</span></span>                                                            | <span data-ttu-id="65cef-107">Описание</span><span class="sxs-lookup"><span data-stu-id="65cef-107">Description</span></span>                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="65cef-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="65cef-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="65cef-109">\[в \] адресе результата операции.</span><span class="sxs-lookup"><span data-stu-id="65cef-109">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="65cef-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="65cef-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="65cef-111">\[\]число, добавляемое в *src1*.</span><span class="sxs-lookup"><span data-stu-id="65cef-111">\[in\] The number to be added to *src1*.</span></span><br/>           |
| <span data-ttu-id="65cef-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="65cef-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="65cef-113">\[\]число, добавляемое в *src0*.</span><span class="sxs-lookup"><span data-stu-id="65cef-113">\[in\] The number to be added to *src0*.</span></span><br/>           |



 

## <a name="remarks"></a><span data-ttu-id="65cef-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="65cef-114">Remarks</span></span>

<span data-ttu-id="65cef-115">Покомпонентное Добавление 32-разрядных операндов *src0* и *src1*, помещая правильный 32-разрядный результат в *dest*.</span><span class="sxs-lookup"><span data-stu-id="65cef-115">Component-wise add of 32-bit operands *src0* and *src1*, placing the correct 32-bit result in *dest*.</span></span> <span data-ttu-id="65cef-116">Не учитывается и не заимствовано 32-разрядных значений каждого компонента, поэтому эта инструкция не чувствительна к подписанному rvalue характеристикиу своих операндов.</span><span class="sxs-lookup"><span data-stu-id="65cef-116">No carry or borrow beyond the 32-bit values of each component is performed, so this instruction is not sensitive to the signed-ness of its operands.</span></span>

<span data-ttu-id="65cef-117">Необязательный модификатор отрицания в исходных операндах перед выполнением операции принимает 2 дополнения.</span><span class="sxs-lookup"><span data-stu-id="65cef-117">Optional negate modifier on source operands takes 2's complement before performing operation.</span></span>

<span data-ttu-id="65cef-118">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="65cef-118">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="65cef-119">Вершинный построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="65cef-119">Vertex Shader</span></span> | <span data-ttu-id="65cef-120">Шейдер геометрии</span><span class="sxs-lookup"><span data-stu-id="65cef-120">Geometry Shader</span></span> | <span data-ttu-id="65cef-121">Построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="65cef-121">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="65cef-122">x</span><span class="sxs-lookup"><span data-stu-id="65cef-122">x</span></span>             | <span data-ttu-id="65cef-123">x</span><span class="sxs-lookup"><span data-stu-id="65cef-123">x</span></span>               | <span data-ttu-id="65cef-124">x</span><span class="sxs-lookup"><span data-stu-id="65cef-124">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="65cef-125">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="65cef-125">Minimum Shader Model</span></span>

<span data-ttu-id="65cef-126">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="65cef-126">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="65cef-127">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="65cef-127">Shader Model</span></span>                                              | <span data-ttu-id="65cef-128">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="65cef-128">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="65cef-129">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="65cef-129">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="65cef-130">да</span><span class="sxs-lookup"><span data-stu-id="65cef-130">yes</span></span>       |
| [<span data-ttu-id="65cef-131">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="65cef-131">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="65cef-132">да</span><span class="sxs-lookup"><span data-stu-id="65cef-132">yes</span></span>       |
| [<span data-ttu-id="65cef-133">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="65cef-133">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="65cef-134">да</span><span class="sxs-lookup"><span data-stu-id="65cef-134">yes</span></span>       |
| [<span data-ttu-id="65cef-135">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="65cef-135">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="65cef-136">Нет</span><span class="sxs-lookup"><span data-stu-id="65cef-136">no</span></span>        |
| [<span data-ttu-id="65cef-137">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="65cef-137">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="65cef-138">Нет</span><span class="sxs-lookup"><span data-stu-id="65cef-138">no</span></span>        |
| [<span data-ttu-id="65cef-139">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="65cef-139">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="65cef-140">Нет</span><span class="sxs-lookup"><span data-stu-id="65cef-140">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="65cef-141">См. также</span><span class="sxs-lookup"><span data-stu-id="65cef-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="65cef-142">Сборка Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="65cef-142">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





