---
title: усубб (SM5-ASM)
description: Вычитание целых чисел без знака с помощью займа.
ms.assetid: 6D42E3CA-5A37-4194-AB42-7A2337C5AB9D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 111ffd134a75b8cfe19f63597cd80655201359c4
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104412139"
---
# <a name="usubb-sm5---asm"></a><span data-ttu-id="b2ed5-103">усубб (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="b2ed5-103">usubb (sm5 - asm)</span></span>

<span data-ttu-id="b2ed5-104">Вычитание целых чисел без знака с помощью займа.</span><span class="sxs-lookup"><span data-stu-id="b2ed5-104">Unsigned integer subtract with borrow.</span></span>



| <span data-ttu-id="b2ed5-105">усубб dest0 \[ . Mask \] , dest1 \[ . Mask \] , src0 \[ . свиззле \] , src1 \[ . свиззле\]</span><span class="sxs-lookup"><span data-stu-id="b2ed5-105">usubb dest0\[.mask\], dest1\[.mask\], src0\[.swizzle\], src1\[.swizzle\]</span></span> |
|--------------------------------------------------------------------------|



 



| <span data-ttu-id="b2ed5-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="b2ed5-106">Item</span></span>                                                               | <span data-ttu-id="b2ed5-107">Описание</span><span class="sxs-lookup"><span data-stu-id="b2ed5-107">Description</span></span>                                                                                       |
|--------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2ed5-108"><span id="dest0"></span><span id="DEST0"></span>*dest0*</span><span class="sxs-lookup"><span data-stu-id="b2ed5-108"><span id="dest0"></span><span id="DEST0"></span>*dest0*</span></span><br/> | <span data-ttu-id="b2ed5-109">\[в \] содержит лсаб результаты инструкции.</span><span class="sxs-lookup"><span data-stu-id="b2ed5-109">\[in\] Contains the LSAB results of the instruction.</span></span><br/>                                   |
| <span data-ttu-id="b2ed5-110"><span id="dest1"></span><span id="DEST1"></span>*dest1*</span><span class="sxs-lookup"><span data-stu-id="b2ed5-110"><span id="dest1"></span><span id="DEST1"></span>*dest1*</span></span><br/> | <span data-ttu-id="b2ed5-111">\[в \] соответствующем компоненте *dest0* , который указывает, было ли создано позаимствование.</span><span class="sxs-lookup"><span data-stu-id="b2ed5-111">\[in\] The corresponding component of *dest0* that specifies if a borrow was produced.</span></span><br/> |
| <span data-ttu-id="b2ed5-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="b2ed5-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>    | <span data-ttu-id="b2ed5-113">\[\]значение, из которого вычитается.</span><span class="sxs-lookup"><span data-stu-id="b2ed5-113">\[in\] The value from which to subtract.</span></span><br/>                                               |
| <span data-ttu-id="b2ed5-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="b2ed5-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/>    | <span data-ttu-id="b2ed5-115">\[\]Сумма, вычитаемая из *src0*.</span><span class="sxs-lookup"><span data-stu-id="b2ed5-115">\[in\] The amount to subtract from *src0*.</span></span><br/>                                             |



 

## <a name="remarks"></a><span data-ttu-id="b2ed5-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="b2ed5-116">Remarks</span></span>

<span data-ttu-id="b2ed5-117">Эта инструкция выполняет неподписанный вычитание 32-разрядных операндов *src1* из *src0*, помещая ЛСБ часть из 32-разрядного результата в *dest0*.</span><span class="sxs-lookup"><span data-stu-id="b2ed5-117">This instruction performs a component-wise unsigned subtract of 32-bit operands *src1* from *src0*, placing the LSB part of the 32-bit result in *dest0*.</span></span>

<span data-ttu-id="b2ed5-118">Соответствующий компонент в *dest1* записывается с помощью 1, если создается аренда, в противном случае — 0.</span><span class="sxs-lookup"><span data-stu-id="b2ed5-118">The corresponding component in *dest1* is written with 1 if a borrow is produced, 0 otherwise.</span></span>

<span data-ttu-id="b2ed5-119">*dest1* может иметь значение null, если это не требуется.</span><span class="sxs-lookup"><span data-stu-id="b2ed5-119">*dest1* can be NULL if the borrow is not needed.</span></span>

<span data-ttu-id="b2ed5-120">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="b2ed5-120">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="b2ed5-121">Вершина</span><span class="sxs-lookup"><span data-stu-id="b2ed5-121">Vertex</span></span> | <span data-ttu-id="b2ed5-122">Поверхности</span><span class="sxs-lookup"><span data-stu-id="b2ed5-122">Hull</span></span> | <span data-ttu-id="b2ed5-123">Домен</span><span class="sxs-lookup"><span data-stu-id="b2ed5-123">Domain</span></span> | <span data-ttu-id="b2ed5-124">Геометрия</span><span class="sxs-lookup"><span data-stu-id="b2ed5-124">Geometry</span></span> | <span data-ttu-id="b2ed5-125">Пиксель</span><span class="sxs-lookup"><span data-stu-id="b2ed5-125">Pixel</span></span> | <span data-ttu-id="b2ed5-126">Вычисления</span><span class="sxs-lookup"><span data-stu-id="b2ed5-126">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="b2ed5-127">X</span><span class="sxs-lookup"><span data-stu-id="b2ed5-127">X</span></span>      | <span data-ttu-id="b2ed5-128">X</span><span class="sxs-lookup"><span data-stu-id="b2ed5-128">X</span></span>    | <span data-ttu-id="b2ed5-129">X</span><span class="sxs-lookup"><span data-stu-id="b2ed5-129">X</span></span>      | <span data-ttu-id="b2ed5-130">X</span><span class="sxs-lookup"><span data-stu-id="b2ed5-130">X</span></span>        | <span data-ttu-id="b2ed5-131">X</span><span class="sxs-lookup"><span data-stu-id="b2ed5-131">X</span></span>     | <span data-ttu-id="b2ed5-132">X</span><span class="sxs-lookup"><span data-stu-id="b2ed5-132">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="b2ed5-133">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="b2ed5-133">Minimum Shader Model</span></span>

<span data-ttu-id="b2ed5-134">Эта инструкция поддерживается в следующих моделях шейдеров:</span><span class="sxs-lookup"><span data-stu-id="b2ed5-134">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="b2ed5-135">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="b2ed5-135">Shader Model</span></span>                                              | <span data-ttu-id="b2ed5-136">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="b2ed5-136">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="b2ed5-137">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="b2ed5-137">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="b2ed5-138">да</span><span class="sxs-lookup"><span data-stu-id="b2ed5-138">yes</span></span>       |
| [<span data-ttu-id="b2ed5-139">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="b2ed5-139">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="b2ed5-140">Нет</span><span class="sxs-lookup"><span data-stu-id="b2ed5-140">no</span></span>        |
| [<span data-ttu-id="b2ed5-141">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="b2ed5-141">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="b2ed5-142">Нет</span><span class="sxs-lookup"><span data-stu-id="b2ed5-142">no</span></span>        |
| [<span data-ttu-id="b2ed5-143">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b2ed5-143">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="b2ed5-144">Нет</span><span class="sxs-lookup"><span data-stu-id="b2ed5-144">no</span></span>        |
| [<span data-ttu-id="b2ed5-145">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b2ed5-145">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="b2ed5-146">Нет</span><span class="sxs-lookup"><span data-stu-id="b2ed5-146">no</span></span>        |
| [<span data-ttu-id="b2ed5-147">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b2ed5-147">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="b2ed5-148">Нет</span><span class="sxs-lookup"><span data-stu-id="b2ed5-148">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="b2ed5-149">См. также</span><span class="sxs-lookup"><span data-stu-id="b2ed5-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b2ed5-150">Сборка Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b2ed5-150">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





