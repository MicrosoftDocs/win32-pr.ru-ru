---
title: удив (SM4-ASM)
description: Деление целых чисел без знака.
ms.assetid: 87C81418-0F74-4C67-9D4A-DA952EFD008E
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07a3dd2f4170a3c8fe522af12d412cfae49396da
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104412177"
---
# <a name="udiv-sm4---asm"></a><span data-ttu-id="ee455-103">удив (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="ee455-103">udiv (sm4 - asm)</span></span>

<span data-ttu-id="ee455-104">Деление целых чисел без знака.</span><span class="sxs-lookup"><span data-stu-id="ee455-104">Unsigned integer divide.</span></span>



| <span data-ttu-id="ee455-105">удив Десткуот \[ . Mask \] , дестрем \[ . Mask \] , src0 \[ . свиззле \] , src1 \[ . свиззле\]</span><span class="sxs-lookup"><span data-stu-id="ee455-105">udiv destQUOT\[.mask\], destREM\[.mask\], src0\[.swizzle\], src1\[.swizzle\]</span></span> |
|------------------------------------------------------------------------------|



 



| <span data-ttu-id="ee455-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="ee455-106">Item</span></span>                                                                                                   | <span data-ttu-id="ee455-107">Описание</span><span class="sxs-lookup"><span data-stu-id="ee455-107">Description</span></span>                                                |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="ee455-108"><span id="destQUOT"></span><span id="destquot"></span><span id="DESTQUOT"></span>*десткуот*</span><span class="sxs-lookup"><span data-stu-id="ee455-108"><span id="destQUOT"></span><span id="destquot"></span><span id="DESTQUOT"></span>*destQUOT*</span></span><br/> | <span data-ttu-id="ee455-109">\[в \] адресе полученного частного.</span><span class="sxs-lookup"><span data-stu-id="ee455-109">\[in\] The address of the resulting quotient.</span></span><br/>   |
| <span data-ttu-id="ee455-110"><span id="destREM"></span><span id="destrem"></span><span id="DESTREM"></span>*дестрем*</span><span class="sxs-lookup"><span data-stu-id="ee455-110"><span id="destREM"></span><span id="destrem"></span><span id="DESTREM"></span>*destREM*</span></span><br/>     | <span data-ttu-id="ee455-111">\[в \] адресе итогового остатка.</span><span class="sxs-lookup"><span data-stu-id="ee455-111">\[in\] The address of the resulting remainder.</span></span><br/>  |
| <span data-ttu-id="ee455-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="ee455-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>                                        | <span data-ttu-id="ee455-113">\[в \] компонентах, разделенных *src1*.</span><span class="sxs-lookup"><span data-stu-id="ee455-113">\[in\] The components to be divided by *src1*.</span></span><br/>  |
| <span data-ttu-id="ee455-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="ee455-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/>                                        | <span data-ttu-id="ee455-115">\[в \] компонентах вхч, чтобы разделить *src0*.</span><span class="sxs-lookup"><span data-stu-id="ee455-115">\[in\] The components by whch to divide *src0*.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ee455-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="ee455-116">Remarks</span></span>

<span data-ttu-id="ee455-117">Эта инструкция выполняет поэлементное деление 32-разрядного операнда, *src0* с помощью 32-разрядного операнда *src1*, на уровне компонентов.</span><span class="sxs-lookup"><span data-stu-id="ee455-117">This instruction performs a component-wise unsigned divide of the 32-bit operand *src0* by the 32-bit operand *src1*.</span></span> <span data-ttu-id="ee455-118">Результаты деления являются 32-разрядными частями, помещенными в *десткуот* и 32-разрядные остатки в *дестрем*.</span><span class="sxs-lookup"><span data-stu-id="ee455-118">The results of the divides are the 32-bit quotients placed in *destQUOT* and 32-bit remainders placed in *destREM*.</span></span>

<span data-ttu-id="ee455-119">Деление на ноль возвращает значение 0xFFFFFFFF как для частного, так и для остатка.</span><span class="sxs-lookup"><span data-stu-id="ee455-119">Divide by zero returns 0xffffffff for both quotient and remainder.</span></span>

<span data-ttu-id="ee455-120">Можно задать значение *десткуот* или *дестрем* как NULL вместо указания регистра, если частное или остаток не требуется.</span><span class="sxs-lookup"><span data-stu-id="ee455-120">You can specifiy either *destQUOT* or *destREM* as NULL instead of specifying a register, if the quotient or remainder are not needed.</span></span>

<span data-ttu-id="ee455-121">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="ee455-121">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="ee455-122">Вершинный построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="ee455-122">Vertex Shader</span></span> | <span data-ttu-id="ee455-123">Шейдер геометрии</span><span class="sxs-lookup"><span data-stu-id="ee455-123">Geometry Shader</span></span> | <span data-ttu-id="ee455-124">Построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="ee455-124">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="ee455-125">x</span><span class="sxs-lookup"><span data-stu-id="ee455-125">x</span></span>             | <span data-ttu-id="ee455-126">x</span><span class="sxs-lookup"><span data-stu-id="ee455-126">x</span></span>               | <span data-ttu-id="ee455-127">x</span><span class="sxs-lookup"><span data-stu-id="ee455-127">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="ee455-128">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="ee455-128">Minimum Shader Model</span></span>

<span data-ttu-id="ee455-129">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="ee455-129">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="ee455-130">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="ee455-130">Shader Model</span></span>                                              | <span data-ttu-id="ee455-131">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="ee455-131">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="ee455-132">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="ee455-132">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="ee455-133">да</span><span class="sxs-lookup"><span data-stu-id="ee455-133">yes</span></span>       |
| [<span data-ttu-id="ee455-134">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="ee455-134">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="ee455-135">да</span><span class="sxs-lookup"><span data-stu-id="ee455-135">yes</span></span>       |
| [<span data-ttu-id="ee455-136">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="ee455-136">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="ee455-137">да</span><span class="sxs-lookup"><span data-stu-id="ee455-137">yes</span></span>       |
| [<span data-ttu-id="ee455-138">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ee455-138">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="ee455-139">Нет</span><span class="sxs-lookup"><span data-stu-id="ee455-139">no</span></span>        |
| [<span data-ttu-id="ee455-140">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ee455-140">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="ee455-141">Нет</span><span class="sxs-lookup"><span data-stu-id="ee455-141">no</span></span>        |
| [<span data-ttu-id="ee455-142">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ee455-142">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="ee455-143">Нет</span><span class="sxs-lookup"><span data-stu-id="ee455-143">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="ee455-144">См. также</span><span class="sxs-lookup"><span data-stu-id="ee455-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ee455-145">Сборка Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ee455-145">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





