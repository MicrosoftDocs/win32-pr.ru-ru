---
title: imm_atomic_consume (SM5-ASM)
description: Атомарное уменьшение скрытого 32-разрядного счетчика, хранящегося в представлении с числом или добавлением неупорядоченного представления доступа (UAV), возвращая новое значение.
ms.assetid: 1115C318-2F86-4161-AC5C-2A61A262DC28
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a1c6fe01ddb92b2ce870b16254f75c52cadd341
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104996931"
---
# <a name="imm_atomic_consume-sm5---asm"></a><span data-ttu-id="92c2b-103">\_атомарное \_ Использование IMM (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="92c2b-103">imm\_atomic\_consume (sm5 - asm)</span></span>

<span data-ttu-id="92c2b-104">Атомарное уменьшение скрытого 32-разрядного счетчика, хранящегося в представлении с числом или добавлением неупорядоченного представления доступа (UAV), возвращая новое значение.</span><span class="sxs-lookup"><span data-stu-id="92c2b-104">Atomically decrement the hidden 32-bit counter stored with a Count or Append unordered access view (UAV), returning the new value.</span></span>



| <span data-ttu-id="92c2b-105">модуль IMM \_ Atomic \_ потребляет dst0 \[ . один \_ компонент \_ Mask \] , дстуав</span><span class="sxs-lookup"><span data-stu-id="92c2b-105">imm\_atomic\_consume dst0\[.single\_component\_mask\], dstUAV</span></span> |
|---------------------------------------------------------------|



 



| <span data-ttu-id="92c2b-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="92c2b-106">Item</span></span>                                                                                           | <span data-ttu-id="92c2b-107">Описание</span><span class="sxs-lookup"><span data-stu-id="92c2b-107">Description</span></span>                                                               |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <span data-ttu-id="92c2b-108"><span id="dst0"></span><span id="DST0"></span>*dst0*</span><span class="sxs-lookup"><span data-stu-id="92c2b-108"><span id="dst0"></span><span id="DST0"></span>*dst0*</span></span><br/>                                | <span data-ttu-id="92c2b-109">\[в \] содержит возвращенное исходное значение счетчика.</span><span class="sxs-lookup"><span data-stu-id="92c2b-109">\[in\] Contains the returned original counter value.</span></span><br/>           |
| <span data-ttu-id="92c2b-110"><span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*дстуав*</span><span class="sxs-lookup"><span data-stu-id="92c2b-110"><span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*dstUAV*</span></span><br/> | <span data-ttu-id="92c2b-111">\[в \] структурированном буфере UAV с флагом Count или Append.</span><span class="sxs-lookup"><span data-stu-id="92c2b-111">\[in\] A structured buffer UAV with the Count or Append flag.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="92c2b-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="92c2b-112">Remarks</span></span>

<span data-ttu-id="92c2b-113">Сведения о допустимости возвращаемого значения счетчика см. в разделе [IMM \_ Atomic \_ Alloc](imm-atomic-alloc--sm5---asm-.md) . в зависимости от того, является ли UAV количеством или дозаписью.</span><span class="sxs-lookup"><span data-stu-id="92c2b-113">See [imm\_atomic\_alloc](imm-atomic-alloc--sm5---asm-.md) for a discussion about the validity of the returned count value depending on whether the UAV is Count or Append.</span></span> <span data-ttu-id="92c2b-114">Это справедливо и для **\_ \_ использования IMM Atomic**.</span><span class="sxs-lookup"><span data-stu-id="92c2b-114">The same applies for **imm\_atomic\_consume**.</span></span>

<span data-ttu-id="92c2b-115">**\_ атомарное \_ Использование IMM Atomic** выполняет Атомарное уменьшение значения счетчика, возвращая новое значение в *dst0*.</span><span class="sxs-lookup"><span data-stu-id="92c2b-115">**imm\_atomic\_consume** does an atomic decrement of the counter value, returning the new value to *dst0*.</span></span>

<span data-ttu-id="92c2b-116">Не существует фиксации количества, поэтому оно переносится в недостаточное количество.</span><span class="sxs-lookup"><span data-stu-id="92c2b-116">There is no clamping of the count, so it wraps on underflow.</span></span>

<span data-ttu-id="92c2b-117">Один и тот же шейдер не может попытаться одновременно **\_ \_ использовать** и IMM **\_ Atomic \_ Alloc** , и IMM Atomic на одном UAV.</span><span class="sxs-lookup"><span data-stu-id="92c2b-117">The same shader cannot attempt both **imm\_atomic\_alloc** and **imm\_atomic\_consume** on the same UAV.</span></span> <span data-ttu-id="92c2b-118">Кроме того, GPU не может разрешить несколько вызовов шейдера для смешения **\_ \_ распределения IMM Atomic** и **IMM \_ Atomic \_** на одном UAV.</span><span class="sxs-lookup"><span data-stu-id="92c2b-118">Further, the GPU cannot allow multiple shader invocations to mix **imm\_atomic\_alloc** and **imm\_atomic\_consume** on the same UAV.</span></span>

<span data-ttu-id="92c2b-119">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="92c2b-119">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="92c2b-120">Вершина</span><span class="sxs-lookup"><span data-stu-id="92c2b-120">Vertex</span></span> | <span data-ttu-id="92c2b-121">Поверхности</span><span class="sxs-lookup"><span data-stu-id="92c2b-121">Hull</span></span> | <span data-ttu-id="92c2b-122">Домен</span><span class="sxs-lookup"><span data-stu-id="92c2b-122">Domain</span></span> | <span data-ttu-id="92c2b-123">Геометрия</span><span class="sxs-lookup"><span data-stu-id="92c2b-123">Geometry</span></span> | <span data-ttu-id="92c2b-124">Пиксель</span><span class="sxs-lookup"><span data-stu-id="92c2b-124">Pixel</span></span> | <span data-ttu-id="92c2b-125">Вычисления</span><span class="sxs-lookup"><span data-stu-id="92c2b-125">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="92c2b-126">X</span><span class="sxs-lookup"><span data-stu-id="92c2b-126">X</span></span>     | <span data-ttu-id="92c2b-127">X</span><span class="sxs-lookup"><span data-stu-id="92c2b-127">X</span></span>       |



 

<span data-ttu-id="92c2b-128">Так как Уавс доступны на всех стадиях шейдера для Direct3D 11,1, эта инструкция применяется ко всем этапам шейдера для среды выполнения Direct3D 11,1, которая доступна начиная с Windows 8.</span><span class="sxs-lookup"><span data-stu-id="92c2b-128">Because UAVs are available at all shader stages for Direct3D 11.1, this instruction applies to all shader stages for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="92c2b-129">Вершина</span><span class="sxs-lookup"><span data-stu-id="92c2b-129">Vertex</span></span> | <span data-ttu-id="92c2b-130">Поверхности</span><span class="sxs-lookup"><span data-stu-id="92c2b-130">Hull</span></span> | <span data-ttu-id="92c2b-131">Домен</span><span class="sxs-lookup"><span data-stu-id="92c2b-131">Domain</span></span> | <span data-ttu-id="92c2b-132">Геометрия</span><span class="sxs-lookup"><span data-stu-id="92c2b-132">Geometry</span></span> | <span data-ttu-id="92c2b-133">Пиксель</span><span class="sxs-lookup"><span data-stu-id="92c2b-133">Pixel</span></span> | <span data-ttu-id="92c2b-134">Вычисления</span><span class="sxs-lookup"><span data-stu-id="92c2b-134">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="92c2b-135">X</span><span class="sxs-lookup"><span data-stu-id="92c2b-135">X</span></span>      | <span data-ttu-id="92c2b-136">X</span><span class="sxs-lookup"><span data-stu-id="92c2b-136">X</span></span>    | <span data-ttu-id="92c2b-137">X</span><span class="sxs-lookup"><span data-stu-id="92c2b-137">X</span></span>      | <span data-ttu-id="92c2b-138">X</span><span class="sxs-lookup"><span data-stu-id="92c2b-138">X</span></span>        | <span data-ttu-id="92c2b-139">X</span><span class="sxs-lookup"><span data-stu-id="92c2b-139">X</span></span>     | <span data-ttu-id="92c2b-140">X</span><span class="sxs-lookup"><span data-stu-id="92c2b-140">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="92c2b-141">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="92c2b-141">Minimum Shader Model</span></span>

<span data-ttu-id="92c2b-142">Эта инструкция поддерживается в следующих моделях шейдеров:</span><span class="sxs-lookup"><span data-stu-id="92c2b-142">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="92c2b-143">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="92c2b-143">Shader Model</span></span>                                              | <span data-ttu-id="92c2b-144">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="92c2b-144">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="92c2b-145">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="92c2b-145">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="92c2b-146">да</span><span class="sxs-lookup"><span data-stu-id="92c2b-146">yes</span></span>       |
| [<span data-ttu-id="92c2b-147">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="92c2b-147">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="92c2b-148">Нет</span><span class="sxs-lookup"><span data-stu-id="92c2b-148">no</span></span>        |
| [<span data-ttu-id="92c2b-149">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="92c2b-149">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="92c2b-150">Нет</span><span class="sxs-lookup"><span data-stu-id="92c2b-150">no</span></span>        |
| [<span data-ttu-id="92c2b-151">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="92c2b-151">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="92c2b-152">Нет</span><span class="sxs-lookup"><span data-stu-id="92c2b-152">no</span></span>        |
| [<span data-ttu-id="92c2b-153">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="92c2b-153">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="92c2b-154">Нет</span><span class="sxs-lookup"><span data-stu-id="92c2b-154">no</span></span>        |
| [<span data-ttu-id="92c2b-155">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="92c2b-155">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="92c2b-156">Нет</span><span class="sxs-lookup"><span data-stu-id="92c2b-156">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="92c2b-157">См. также</span><span class="sxs-lookup"><span data-stu-id="92c2b-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="92c2b-158">Сборка Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="92c2b-158">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





