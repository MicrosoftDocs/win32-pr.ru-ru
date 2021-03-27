---
title: imm_atomic_alloc (SM5-ASM)
description: Атомарное увеличение скрытого 32-битного счетчика, хранящегося в представлении Count или Append UAV (неупорядоченное представление доступа), возвращая исходное значение.
ms.assetid: 534FA3C3-6FAC-41DC-AC07-0E53FEED000C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28a97709629497bae9af0298789453ef1d1172b7
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "103784962"
---
# <a name="imm_atomic_alloc-sm5---asm"></a><span data-ttu-id="8be33-103">IMM \_ Atomic \_ Alloc (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="8be33-103">imm\_atomic\_alloc (sm5 - asm)</span></span>

<span data-ttu-id="8be33-104">Атомарное увеличение скрытого 32-битного счетчика, хранящегося в представлении Count или Append UAV (неупорядоченное представление доступа), возвращая исходное значение.</span><span class="sxs-lookup"><span data-stu-id="8be33-104">Atomically increment the hidden 32-bit counter stored with a Count or Append unordered access view (UAV), returning the original value.</span></span>



| <span data-ttu-id="8be33-105">IMM \_ Atomic \_ Alloc dst0 \[ . единственная \_ \_ Маска компонента \] , дстуав</span><span class="sxs-lookup"><span data-stu-id="8be33-105">imm\_atomic\_alloc dst0\[.single\_component\_mask\], dstUAV</span></span> |
|-------------------------------------------------------------|



 



| <span data-ttu-id="8be33-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="8be33-106">Item</span></span>                                                                                           | <span data-ttu-id="8be33-107">Описание</span><span class="sxs-lookup"><span data-stu-id="8be33-107">Description</span></span>                                                               |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <span data-ttu-id="8be33-108"><span id="dst0"></span><span id="DST0"></span>*dst0*</span><span class="sxs-lookup"><span data-stu-id="8be33-108"><span id="dst0"></span><span id="DST0"></span>*dst0*</span></span><br/>                                | <span data-ttu-id="8be33-109">\[в \] содержит возвращенное значение счетчика.</span><span class="sxs-lookup"><span data-stu-id="8be33-109">\[in\] Contains the returned counter value.</span></span><br/>                    |
| <span data-ttu-id="8be33-110"><span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*дстуав*</span><span class="sxs-lookup"><span data-stu-id="8be33-110"><span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*dstUAV*</span></span><br/> | <span data-ttu-id="8be33-111">\[в \] структурированном буфере UAV с флагом Count или Append.</span><span class="sxs-lookup"><span data-stu-id="8be33-111">\[in\] A Structured Buffer UAV with the Count or Append flag.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="8be33-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="8be33-112">Remarks</span></span>

<span data-ttu-id="8be33-113">Существует скрытое значение счетчика без знака 32-разрядного целого числа, связанное с каждым представлением счетчика или с добавлением буфера, которое инициализируется при привязке представления к конвейеру, включая параметр для сохранения предыдущего значения.</span><span class="sxs-lookup"><span data-stu-id="8be33-113">There is a hidden unsigned 32-bit integer counter value associated with each Count or Append Buffer view which is initialized when the view is bound to the pipeline, including the option to keep the previous value.</span></span>

<span data-ttu-id="8be33-114">Эта инструкция выполняет атомарное приращение значения счетчика, возвращая исходный объект в *dst0*.</span><span class="sxs-lookup"><span data-stu-id="8be33-114">This instruction does an atomic increment of the counter value, returning the original to *dst0*.</span></span>

<span data-ttu-id="8be33-115">Для добавления UAV возвращаемое значение допустимо только на время вызова шейдера.</span><span class="sxs-lookup"><span data-stu-id="8be33-115">For an Append UAV, the returned value is only valid for the duration of the shader invocation.</span></span> <span data-ttu-id="8be33-116">После этого реализация может изменить макет памяти.</span><span class="sxs-lookup"><span data-stu-id="8be33-116">after that the implementation may rearrange the memory layout.</span></span> <span data-ttu-id="8be33-117">Любая адресация памяти на основе возвращаемого значения должна быть ограничена вызовом шейдера.</span><span class="sxs-lookup"><span data-stu-id="8be33-117">Any memory addressing based on the returned value must be limited to the shader invocation.</span></span>

<span data-ttu-id="8be33-118">В случае добавления UAV компилятор HLSL может использовать возвращаемое значение в качестве индекса структуры, используемого для доступа к структурированному буферу.</span><span class="sxs-lookup"><span data-stu-id="8be33-118">For an Append UAV, within the shader invocation the HLSL compiler can use the returned value as the struct index to use for accessing the structured buffer.</span></span> <span data-ttu-id="8be33-119">При доступе к любому индексу структуры, отличному от расположений, возвращенных вызовами с помощью вызова **IMM \_ атомарного \_ распределения** или [ \_ использования](imm-atomic-consume--sm5---asm-.md) , выдается неопределенное значение, в котором доступ к КАКОМУ-то расположению памяти в UAV осуществляется случайным образом и фиксированным только на время существования вызова шейдера.</span><span class="sxs-lookup"><span data-stu-id="8be33-119">Accessing any struct index other than those locations returned by call(s) to **imm\_atomic\_alloc** or [\_consume](imm-atomic-consume--sm5---asm-.md) produce undefined results in that exactly which memory location within the UAV is being accessed is random and only fixed for the lifetime of the shader invocation.</span></span>

<span data-ttu-id="8be33-120">Для счетчика UAV возвращаемое значение может быть сохранено приложением как ссылка на фиксированное расположение в UAV, которое имеет смысл после того, как вызов шейдера не будет выполнен.</span><span class="sxs-lookup"><span data-stu-id="8be33-120">For a Count UAV, the returned value can be saved by the application as a reference to a fixed location within the UAV that is meaningful after the shader invocation is over.</span></span> <span data-ttu-id="8be33-121">Любое расположение в UAVе Count всегда может быть доступно независимо от значения счетчика.</span><span class="sxs-lookup"><span data-stu-id="8be33-121">Any location in a Count UAV may always be accessed independent of what the count value is.</span></span>

<span data-ttu-id="8be33-122">Фиксация счетчика не производится, поэтому он переносится на переполнение.</span><span class="sxs-lookup"><span data-stu-id="8be33-122">There is no clamping of the count, so it wraps on overflow.</span></span>

<span data-ttu-id="8be33-123">Один и тот же шейдер не может попытаться одновременно **\_ \_ использовать** и IMM **\_ Atomic \_ Alloc** , и IMM Atomic на одном UAV.</span><span class="sxs-lookup"><span data-stu-id="8be33-123">The same shader cannot attempt both **imm\_atomic\_alloc** and **imm\_atomic\_consume** on the same UAV.</span></span> <span data-ttu-id="8be33-124">Кроме того, GPU не может разрешить несколько вызовов шейдера для смешения **\_ \_ распределения IMM Atomic** и **IMM \_ Atomic \_** на одном UAV.</span><span class="sxs-lookup"><span data-stu-id="8be33-124">Further, the GPU cannot allow multiple shader invocations to mix **imm\_atomic\_alloc** and **imm\_atomic\_consume** on the same UAV.</span></span>

<span data-ttu-id="8be33-125">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="8be33-125">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="8be33-126">Вершина</span><span class="sxs-lookup"><span data-stu-id="8be33-126">Vertex</span></span> | <span data-ttu-id="8be33-127">Поверхности</span><span class="sxs-lookup"><span data-stu-id="8be33-127">Hull</span></span> | <span data-ttu-id="8be33-128">Домен</span><span class="sxs-lookup"><span data-stu-id="8be33-128">Domain</span></span> | <span data-ttu-id="8be33-129">Геометрия</span><span class="sxs-lookup"><span data-stu-id="8be33-129">Geometry</span></span> | <span data-ttu-id="8be33-130">Пиксель</span><span class="sxs-lookup"><span data-stu-id="8be33-130">Pixel</span></span> | <span data-ttu-id="8be33-131">Вычисления</span><span class="sxs-lookup"><span data-stu-id="8be33-131">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="8be33-132">X</span><span class="sxs-lookup"><span data-stu-id="8be33-132">X</span></span>     | <span data-ttu-id="8be33-133">X</span><span class="sxs-lookup"><span data-stu-id="8be33-133">X</span></span>       |



 

<span data-ttu-id="8be33-134">Так как Уавс доступны на всех стадиях шейдера для Direct3D 11,1, эта инструкция применяется ко всем этапам шейдера для среды выполнения Direct3D 11,1, которая доступна начиная с Windows 8.</span><span class="sxs-lookup"><span data-stu-id="8be33-134">Because UAVs are available at all shader stages for Direct3D 11.1, this instruction applies to all shader stages for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="8be33-135">Вершина</span><span class="sxs-lookup"><span data-stu-id="8be33-135">Vertex</span></span> | <span data-ttu-id="8be33-136">Поверхности</span><span class="sxs-lookup"><span data-stu-id="8be33-136">Hull</span></span> | <span data-ttu-id="8be33-137">Домен</span><span class="sxs-lookup"><span data-stu-id="8be33-137">Domain</span></span> | <span data-ttu-id="8be33-138">Геометрия</span><span class="sxs-lookup"><span data-stu-id="8be33-138">Geometry</span></span> | <span data-ttu-id="8be33-139">Пиксель</span><span class="sxs-lookup"><span data-stu-id="8be33-139">Pixel</span></span> | <span data-ttu-id="8be33-140">Вычисления</span><span class="sxs-lookup"><span data-stu-id="8be33-140">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="8be33-141">X</span><span class="sxs-lookup"><span data-stu-id="8be33-141">X</span></span>      | <span data-ttu-id="8be33-142">X</span><span class="sxs-lookup"><span data-stu-id="8be33-142">X</span></span>    | <span data-ttu-id="8be33-143">X</span><span class="sxs-lookup"><span data-stu-id="8be33-143">X</span></span>      | <span data-ttu-id="8be33-144">X</span><span class="sxs-lookup"><span data-stu-id="8be33-144">X</span></span>        | <span data-ttu-id="8be33-145">X</span><span class="sxs-lookup"><span data-stu-id="8be33-145">X</span></span>     | <span data-ttu-id="8be33-146">X</span><span class="sxs-lookup"><span data-stu-id="8be33-146">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="8be33-147">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="8be33-147">Minimum Shader Model</span></span>

<span data-ttu-id="8be33-148">Эта инструкция поддерживается в следующих моделях шейдеров:</span><span class="sxs-lookup"><span data-stu-id="8be33-148">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="8be33-149">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="8be33-149">Shader Model</span></span>                                              | <span data-ttu-id="8be33-150">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="8be33-150">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="8be33-151">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="8be33-151">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="8be33-152">да</span><span class="sxs-lookup"><span data-stu-id="8be33-152">yes</span></span>       |
| [<span data-ttu-id="8be33-153">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="8be33-153">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="8be33-154">Нет</span><span class="sxs-lookup"><span data-stu-id="8be33-154">no</span></span>        |
| [<span data-ttu-id="8be33-155">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="8be33-155">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="8be33-156">Нет</span><span class="sxs-lookup"><span data-stu-id="8be33-156">no</span></span>        |
| [<span data-ttu-id="8be33-157">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8be33-157">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="8be33-158">Нет</span><span class="sxs-lookup"><span data-stu-id="8be33-158">no</span></span>        |
| [<span data-ttu-id="8be33-159">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8be33-159">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="8be33-160">Нет</span><span class="sxs-lookup"><span data-stu-id="8be33-160">no</span></span>        |
| [<span data-ttu-id="8be33-161">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8be33-161">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="8be33-162">Нет</span><span class="sxs-lookup"><span data-stu-id="8be33-162">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="8be33-163">См. также</span><span class="sxs-lookup"><span data-stu-id="8be33-163">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8be33-164">Сборка Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8be33-164">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





