---
title: dcl_uav_structured (SM5-ASM)
description: Объявите неупорядоченное представление доступа (UAV) для использования шейдером. | dcl_uav_structured (SM5-ASM)
ms.assetid: 40D6B8F7-8A41-4EFE-A8A3-44A646B4D43B
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3dc02396f4837a095506e736d81ea8c00eb0669f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104273474"
---
# <a name="dcl_uav_structured-sm5---asm"></a><span data-ttu-id="a8713-104">дкл \_ UAV \_ Structured (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="a8713-104">dcl\_uav\_structured (sm5 - asm)</span></span>

<span data-ttu-id="a8713-105">Объявите неупорядоченное представление доступа (UAV) для использования шейдером.</span><span class="sxs-lookup"><span data-stu-id="a8713-105">Declare an unordered access view (UAV) for use by a shader.</span></span>



| <span data-ttu-id="a8713-106">дкл \_ UAV \_ Structured \[ \_ ГЛК \] дстуав, структбитестриде</span><span class="sxs-lookup"><span data-stu-id="a8713-106">dcl\_uav\_structured\[\_glc\] dstUAV, structByteStride</span></span> |
|--------------------------------------------------------|



 



| <span data-ttu-id="a8713-107">Элемент</span><span class="sxs-lookup"><span data-stu-id="a8713-107">Item</span></span>                                                                                                                                   | <span data-ttu-id="a8713-108">Описание</span><span class="sxs-lookup"><span data-stu-id="a8713-108">Description</span></span>                                           |
|----------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <span data-ttu-id="a8713-109"><span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*дстуав*</span><span class="sxs-lookup"><span data-stu-id="a8713-109"><span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*dstUAV*</span></span><br/>                                         | <span data-ttu-id="a8713-110">\[в \] UAV.</span><span class="sxs-lookup"><span data-stu-id="a8713-110">\[in\] The UAV.</span></span><br/>                            |
| <span data-ttu-id="a8713-111"><span id="structByteStride"></span><span id="structbytestride"></span><span id="STRUCTBYTESTRIDE"></span>*структбитестриде*</span><span class="sxs-lookup"><span data-stu-id="a8713-111"><span id="structByteStride"></span><span id="structbytestride"></span><span id="STRUCTBYTESTRIDE"></span>*structByteStride*</span></span><br/> | <span data-ttu-id="a8713-112">\[\]Размер структуры в байтах.</span><span class="sxs-lookup"><span data-stu-id="a8713-112">\[in\] The size of the structure in bytes.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a8713-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="a8713-113">Remarks</span></span>

<span data-ttu-id="a8713-114">*дстуав* — это регистрация в формате u, \# объявленная как ссылка на унордередакцессвиев структурированного буфера с заданным шагом, который должен быть привязан к слоту UAV \# в API.</span><span class="sxs-lookup"><span data-stu-id="a8713-114">*dstUAV* is a u\# register declared as a reference to an UnorderedAccessView of a structured buffer with the specified stride that must be bound to UAV slot \# at the API.</span></span>

<span data-ttu-id="a8713-115">Содержимое структуры не имеет типа; операции, выполняемые в памяти, могут неявно интерпретировать данные как имеющие тип.</span><span class="sxs-lookup"><span data-stu-id="a8713-115">The contents of the structure have no type; operations performed on the memory may implicitly interpret the data as having a type.</span></span>

<span data-ttu-id="a8713-116">*структбитестриде* — это размер структуры в байтах в объявляемом буфере.</span><span class="sxs-lookup"><span data-stu-id="a8713-116">*structByteStride* is the size of the structure in bytes in the buffer being declared.</span></span> <span data-ttu-id="a8713-117">Это значение должно быть больше нуля.</span><span class="sxs-lookup"><span data-stu-id="a8713-117">This value must be greater than zero.</span></span> <span data-ttu-id="a8713-118">*структбитестриде* имеет тип uint и должен быть кратен 4.</span><span class="sxs-lookup"><span data-stu-id="a8713-118">*structByteStride* is of type uint, and must be a multiple of 4.</span></span>

<span data-ttu-id="a8713-119">Инструкции, которые ссылаются на структурированный u \# , принимают 2D-адрес, где первый компонент выбирает \[ структуру \] , а второй компонент выбирает \[ смещение в пределах структуры в соответствии с выделенными байтами \] .</span><span class="sxs-lookup"><span data-stu-id="a8713-119">Instructions that reference a structured u\# take a 2D address, where the first component picks \[struct\], and the second component picks \[offset within struct, in aligned bytes\].</span></span>

<span data-ttu-id="a8713-120">\_Флаг ГЛК означает «глобально согласованность».</span><span class="sxs-lookup"><span data-stu-id="a8713-120">The \_glc flag means for"globally coherent".</span></span> <span data-ttu-id="a8713-121">Отсутствие \_ ГЛК означает, что UAV объявляется только как "согласование с группами" в шейдере вычислений или "локальное согласование" в одном вызове шейдера пикселей.</span><span class="sxs-lookup"><span data-stu-id="a8713-121">The absence of \_glc means the UAV is being declared only as "group coherent" in the compute shader, or "locally coherent" in a single pixel shader invocation.</span></span>

<span data-ttu-id="a8713-122">\_Флаг OPC — это счетчик с сохранением заказов.</span><span class="sxs-lookup"><span data-stu-id="a8713-122">The \_opc flag is the order preserving counter.</span></span> <span data-ttu-id="a8713-123">Это означает, что если UAV привязан к слоту \# (u \# ), он должен быть создан с ФЛАГом счетчика.</span><span class="sxs-lookup"><span data-stu-id="a8713-123">It indicates that if a UAV is bound to slot \# (u\#), it must have been created with the COUNTER flag.</span></span> <span data-ttu-id="a8713-124">Это означает, что операции [ \_ \_ распределения IMM Atomic](imm-atomic-alloc--sm5---asm-.md) или [IMM \_ атомарных операций \_ использования](imm-atomic-consume--sm5---asm-.md) в шейдере управляют счетчиком, значения которого можно использовать в шейдере в качестве постоянной ссылки на расположение в UAV.</span><span class="sxs-lookup"><span data-stu-id="a8713-124">This means that [imm\_atomic\_alloc](imm-atomic-alloc--sm5---asm-.md) or [imm\_atomic\_consume](imm-atomic-consume--sm5---asm-.md) operations in the shader manipulate a counter whose values can be used in the shader as a permanent reference to a location in the UAV.</span></span> <span data-ttu-id="a8713-125">Невозможно изменить порядок данных после поверх шейдера.</span><span class="sxs-lookup"><span data-stu-id="a8713-125">Data cannot be reordered after the shader is over.</span></span>

<span data-ttu-id="a8713-126">Отсутствие \_ флага OPC означает, что если шейдер использует инструкции[IMM \_ Atomic \_ Alloc](imm-atomic-alloc--sm5---asm-.md) или [IMM \_ Atomic \_ ](imm-atomic-consume--sm5---asm-.md) , а UAV привязан к слоту \# (u), он должен быть создан с флагом Append, который предоставляет счетчик, не гарантирующий, что порядок сохраняется после вызова шейдера.</span><span class="sxs-lookup"><span data-stu-id="a8713-126">The absence of the \_opc flag means that if the shader uses[imm\_atomic\_alloc](imm-atomic-alloc--sm5---asm-.md) or [imm\_atomic\_consume](imm-atomic-consume--sm5---asm-.md) instructions and a UAV is bound to slot \# (u), it must have been created with the APPEND flag, which provides a counter that does not guarantee order is preserved after the shader invocation.</span></span>

<span data-ttu-id="a8713-127">Если \_ флаг OPC отсутствует, а шейдер не содержит инструкций [IMM \_ Atomic \_ Alloc](imm-atomic-alloc--sm5---asm-.md) или [IMM \_ Atomic \_ ](imm-atomic-consume--sm5---asm-.md) , то можно создать UAV, привязанный к СЛОТу \# (u), с флагом счетчика (счетчик будет использоваться этим шейдером), флаг (нет счетчика), но не с флагом Append.</span><span class="sxs-lookup"><span data-stu-id="a8713-127">If the \_opc flag is absent and the shader does not contain [imm\_atomic\_alloc](imm-atomic-alloc--sm5---asm-.md) or [imm\_atomic\_consume](imm-atomic-consume--sm5---asm-.md) instructions, a UAV bound to slot \# (u) is permitted to have been created with the COUNTER flag (the counter will go unused by this shader), no flag (no counter), but not with the APPEND flag.</span></span>

> [!Note]  
> <span data-ttu-id="a8713-128">CS \_ 4 \_ 0 и CS \_ 4 \_ 1 поддерживают **дкл \_ тгсм \_ Structured**, но не [дкл \_ тгсм \_ RAW](dcl-tgsm-raw--sm5---asm-.md).</span><span class="sxs-lookup"><span data-stu-id="a8713-128">cs\_4\_0 and cs\_4\_1 supports **dcl\_tgsm\_structured**, but not [dcl\_tgsm\_raw](dcl-tgsm-raw--sm5---asm-.md).</span></span>

 

<span data-ttu-id="a8713-129">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="a8713-129">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="a8713-130">Вершина</span><span class="sxs-lookup"><span data-stu-id="a8713-130">Vertex</span></span> | <span data-ttu-id="a8713-131">Поверхности</span><span class="sxs-lookup"><span data-stu-id="a8713-131">Hull</span></span> | <span data-ttu-id="a8713-132">Домен</span><span class="sxs-lookup"><span data-stu-id="a8713-132">Domain</span></span> | <span data-ttu-id="a8713-133">Геометрия</span><span class="sxs-lookup"><span data-stu-id="a8713-133">Geometry</span></span> | <span data-ttu-id="a8713-134">Пиксель</span><span class="sxs-lookup"><span data-stu-id="a8713-134">Pixel</span></span> | <span data-ttu-id="a8713-135">Вычисления</span><span class="sxs-lookup"><span data-stu-id="a8713-135">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="a8713-136">X</span><span class="sxs-lookup"><span data-stu-id="a8713-136">X</span></span>     | <span data-ttu-id="a8713-137">X</span><span class="sxs-lookup"><span data-stu-id="a8713-137">X</span></span>       |



 

<span data-ttu-id="a8713-138">Так как Уавс доступны на всех стадиях шейдера для Direct3D 11,1, эта инструкция применяется ко всем этапам шейдера для среды выполнения Direct3D 11,1, которая доступна начиная с Windows 8.</span><span class="sxs-lookup"><span data-stu-id="a8713-138">Because UAVs are available at all shader stages for Direct3D 11.1, this instruction applies to all shader stages for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="a8713-139">Вершина</span><span class="sxs-lookup"><span data-stu-id="a8713-139">Vertex</span></span> | <span data-ttu-id="a8713-140">Поверхности</span><span class="sxs-lookup"><span data-stu-id="a8713-140">Hull</span></span> | <span data-ttu-id="a8713-141">Домен</span><span class="sxs-lookup"><span data-stu-id="a8713-141">Domain</span></span> | <span data-ttu-id="a8713-142">Геометрия</span><span class="sxs-lookup"><span data-stu-id="a8713-142">Geometry</span></span> | <span data-ttu-id="a8713-143">Пиксель</span><span class="sxs-lookup"><span data-stu-id="a8713-143">Pixel</span></span> | <span data-ttu-id="a8713-144">Вычисления</span><span class="sxs-lookup"><span data-stu-id="a8713-144">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="a8713-145">X</span><span class="sxs-lookup"><span data-stu-id="a8713-145">X</span></span>      | <span data-ttu-id="a8713-146">X</span><span class="sxs-lookup"><span data-stu-id="a8713-146">X</span></span>    | <span data-ttu-id="a8713-147">X</span><span class="sxs-lookup"><span data-stu-id="a8713-147">X</span></span>      | <span data-ttu-id="a8713-148">X</span><span class="sxs-lookup"><span data-stu-id="a8713-148">X</span></span>        | <span data-ttu-id="a8713-149">X</span><span class="sxs-lookup"><span data-stu-id="a8713-149">X</span></span>     | <span data-ttu-id="a8713-150">X</span><span class="sxs-lookup"><span data-stu-id="a8713-150">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="a8713-151">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="a8713-151">Minimum Shader Model</span></span>

<span data-ttu-id="a8713-152">Эта инструкция поддерживается в следующих моделях шейдеров:</span><span class="sxs-lookup"><span data-stu-id="a8713-152">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="a8713-153">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="a8713-153">Shader Model</span></span>                                              | <span data-ttu-id="a8713-154">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="a8713-154">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="a8713-155">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="a8713-155">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="a8713-156">да</span><span class="sxs-lookup"><span data-stu-id="a8713-156">yes</span></span>       |
| [<span data-ttu-id="a8713-157">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="a8713-157">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="a8713-158">Нет</span><span class="sxs-lookup"><span data-stu-id="a8713-158">no</span></span>        |
| [<span data-ttu-id="a8713-159">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="a8713-159">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="a8713-160">Нет</span><span class="sxs-lookup"><span data-stu-id="a8713-160">no</span></span>        |
| [<span data-ttu-id="a8713-161">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a8713-161">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="a8713-162">Нет</span><span class="sxs-lookup"><span data-stu-id="a8713-162">no</span></span>        |
| [<span data-ttu-id="a8713-163">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a8713-163">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="a8713-164">Нет</span><span class="sxs-lookup"><span data-stu-id="a8713-164">no</span></span>        |
| [<span data-ttu-id="a8713-165">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a8713-165">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="a8713-166">Нет</span><span class="sxs-lookup"><span data-stu-id="a8713-166">no</span></span>        |



 

> [!Note]  
> <span data-ttu-id="a8713-167">Эта инструкция поддерживается в CS \_ 4 \_ 0 и CS \_ 4 \_ 1.</span><span class="sxs-lookup"><span data-stu-id="a8713-167">This instruction is supported in cs\_4\_0 and cs\_4\_1.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="a8713-168">См. также</span><span class="sxs-lookup"><span data-stu-id="a8713-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a8713-169">Сборка Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a8713-169">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





