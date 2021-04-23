---
title: дфма (SM5-ASM)
description: Выполняет добавление с помощью предохранителя.
ms.assetid: 5BE96CDB-1756-4EBE-B4CC-69EFF098A4F1
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2e6cafc71dbc7d57655524b1b87c9c5b9ba20f3
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104335504"
---
# <a name="dfma-sm5---asm"></a><span data-ttu-id="5f000-103">дфма (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="5f000-103">dfma (sm5 - asm)</span></span>

<span data-ttu-id="5f000-104">Выполняет добавление с помощью предохранителя.</span><span class="sxs-lookup"><span data-stu-id="5f000-104">Performs a fused-multiply add.</span></span>



| <span data-ttu-id="5f000-105">дфма \[ \_ \] \[ . Маска \] , \[ - \] src0 \[ \_ ABS \] \[ . свиззле \] , \[ - \] src1 \[ \_ ABS \] \[ . свиззле \] , \[ - \] src2 \[ \_ ABS \] \[ . свиззле\]</span><span class="sxs-lookup"><span data-stu-id="5f000-105">dfma\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\],\[-\]src2\[\_abs\]\[.swizzle\]</span></span> |
|----------------------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="5f000-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="5f000-106">Item</span></span>                                                            | <span data-ttu-id="5f000-107">Описание</span><span class="sxs-lookup"><span data-stu-id="5f000-107">Description</span></span>                                                                                                                                               |
|-----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f000-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="5f000-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="5f000-109">\[в \] адресе результата операции.</span><span class="sxs-lookup"><span data-stu-id="5f000-109">\[in\] The address of the result of the operation.</span></span> <span data-ttu-id="5f000-110">Значение результата должно быть точным до 0,5 ULP.</span><span class="sxs-lookup"><span data-stu-id="5f000-110">The result value must be accurate to 0.5 ULP.</span></span><br/> <span data-ttu-id="5f000-111">*конечный адрес*  =  *src0* \* *src1*  +  *src2*</span><span class="sxs-lookup"><span data-stu-id="5f000-111">*dest* = *src0* \* *src1* + *src2*</span></span><br/> |
| <span data-ttu-id="5f000-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="5f000-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="5f000-113">\[в \] компонентах для перемножения с *src1*.</span><span class="sxs-lookup"><span data-stu-id="5f000-113">\[in\] The components to multiply with *src1*.</span></span><br/>                                                                                                 |
| <span data-ttu-id="5f000-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="5f000-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="5f000-115">\[в \] компонентах для перемножения с *src0*.</span><span class="sxs-lookup"><span data-stu-id="5f000-115">\[in\] The components to multiply with *src0*.</span></span><br/>                                                                                                 |
| <span data-ttu-id="5f000-116"><span id="src2"></span><span id="SRC2"></span>*src2*</span><span class="sxs-lookup"><span data-stu-id="5f000-116"><span id="src2"></span><span id="SRC2"></span>*src2*</span></span><br/> | <span data-ttu-id="5f000-117">\[в \] компонентах, добавляемых в *src0* \* *src1*.</span><span class="sxs-lookup"><span data-stu-id="5f000-117">\[in\] The components to add to *src0* \* *src1*.</span></span><br/>                                                                                               |



 

## <a name="remarks"></a><span data-ttu-id="5f000-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="5f000-118">Remarks</span></span>

<span data-ttu-id="5f000-119">Шейдеры, использующие эту инструкцию, будут помечены флагом построителя текстуры, который приведет к сбою привязки, если не выполняются все следующие условия.</span><span class="sxs-lookup"><span data-stu-id="5f000-119">Shaders that use this instruction will be marked with a shader flag that will cause them to fail to bind unless all the following conditions are met.</span></span>

-   <span data-ttu-id="5f000-120">Система поддерживает DirectX 11,1.</span><span class="sxs-lookup"><span data-stu-id="5f000-120">The system supports DirectX 11.1.</span></span>
-   <span data-ttu-id="5f000-121">Система включает драйвер WDDM 1,2.</span><span class="sxs-lookup"><span data-stu-id="5f000-121">The system includes a WDDM 1.2 driver.</span></span>
-   <span data-ttu-id="5f000-122">Драйвер сообщает о поддержке этой инструкции с помощью **\_ \_ параметров D3D11 Data Feature D3D11 \_ \_ . Для Екстендеддаублесшадеринструктионс** задано значение **true**.</span><span class="sxs-lookup"><span data-stu-id="5f000-122">The driver reports support for this instruction via **D3D11\_FEATURE\_DATA\_D3D11\_OPTIONS.ExtendedDoublesShaderInstructions** set to **TRUE**.</span></span>

<span data-ttu-id="5f000-123">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="5f000-123">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="5f000-124">Вершина</span><span class="sxs-lookup"><span data-stu-id="5f000-124">Vertex</span></span> | <span data-ttu-id="5f000-125">Поверхности</span><span class="sxs-lookup"><span data-stu-id="5f000-125">Hull</span></span> | <span data-ttu-id="5f000-126">Домен</span><span class="sxs-lookup"><span data-stu-id="5f000-126">Domain</span></span> | <span data-ttu-id="5f000-127">Геометрия</span><span class="sxs-lookup"><span data-stu-id="5f000-127">Geometry</span></span> | <span data-ttu-id="5f000-128">Пиксель</span><span class="sxs-lookup"><span data-stu-id="5f000-128">Pixel</span></span> | <span data-ttu-id="5f000-129">Вычисления</span><span class="sxs-lookup"><span data-stu-id="5f000-129">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="5f000-130">X</span><span class="sxs-lookup"><span data-stu-id="5f000-130">X</span></span>      | <span data-ttu-id="5f000-131">X</span><span class="sxs-lookup"><span data-stu-id="5f000-131">X</span></span>    | <span data-ttu-id="5f000-132">X</span><span class="sxs-lookup"><span data-stu-id="5f000-132">X</span></span>      | <span data-ttu-id="5f000-133">X</span><span class="sxs-lookup"><span data-stu-id="5f000-133">X</span></span>        | <span data-ttu-id="5f000-134">X</span><span class="sxs-lookup"><span data-stu-id="5f000-134">X</span></span>     | <span data-ttu-id="5f000-135">X</span><span class="sxs-lookup"><span data-stu-id="5f000-135">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="5f000-136">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="5f000-136">Minimum Shader Model</span></span>

<span data-ttu-id="5f000-137">Эта инструкция поддерживается в следующих моделях шейдеров:</span><span class="sxs-lookup"><span data-stu-id="5f000-137">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="5f000-138">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="5f000-138">Shader Model</span></span>                                              | <span data-ttu-id="5f000-139">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="5f000-139">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="5f000-140">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="5f000-140">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="5f000-141">да</span><span class="sxs-lookup"><span data-stu-id="5f000-141">yes</span></span>       |
| [<span data-ttu-id="5f000-142">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="5f000-142">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="5f000-143">Нет</span><span class="sxs-lookup"><span data-stu-id="5f000-143">no</span></span>        |
| [<span data-ttu-id="5f000-144">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="5f000-144">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="5f000-145">Нет</span><span class="sxs-lookup"><span data-stu-id="5f000-145">no</span></span>        |
| [<span data-ttu-id="5f000-146">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5f000-146">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="5f000-147">Нет</span><span class="sxs-lookup"><span data-stu-id="5f000-147">no</span></span>        |
| [<span data-ttu-id="5f000-148">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5f000-148">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="5f000-149">Нет</span><span class="sxs-lookup"><span data-stu-id="5f000-149">no</span></span>        |
| [<span data-ttu-id="5f000-150">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5f000-150">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="5f000-151">Нет</span><span class="sxs-lookup"><span data-stu-id="5f000-151">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="5f000-152">См. также</span><span class="sxs-lookup"><span data-stu-id="5f000-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5f000-153">Сборка Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5f000-153">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





