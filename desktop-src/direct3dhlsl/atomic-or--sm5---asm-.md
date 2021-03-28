---
title: atomic_or (SM5-ASM)
description: Атомарная Побитовая операция или в память.
ms.assetid: 5AFB96AA-267B-454E-9526-BA61A876ED42
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 245f1b02edd74712471206b095f0c8a9040962b6
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104532885"
---
# <a name="atomic_or-sm5---asm"></a><span data-ttu-id="9b765-103">Atomic \_ или (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="9b765-103">atomic\_or (sm5 - asm)</span></span>

<span data-ttu-id="9b765-104">Атомарная Побитовая операция или в память.</span><span class="sxs-lookup"><span data-stu-id="9b765-104">Atomic bitwise OR to memory.</span></span>



| <span data-ttu-id="9b765-105">Атомарный \_ или DST, дстаддресс \[ . свиззле \] , src0 \[ . SELECT, \_ компонент\]</span><span class="sxs-lookup"><span data-stu-id="9b765-105">atomic\_or dst, dstAddress\[.swizzle\], src0\[.select\_component\]</span></span> |
|--------------------------------------------------------------------|



 



| <span data-ttu-id="9b765-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="9b765-106">Item</span></span>                                                                                                           | <span data-ttu-id="9b765-107">Описание</span><span class="sxs-lookup"><span data-stu-id="9b765-107">Description</span></span>                                                                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b765-108"><span id="dst"></span><span id="DST"></span>*кон*</span><span class="sxs-lookup"><span data-stu-id="9b765-108"><span id="dst"></span><span id="DST"></span>*dst*</span></span><br/>                                                   | <span data-ttu-id="9b765-109">\[в \] компонентах или с *src0*.</span><span class="sxs-lookup"><span data-stu-id="9b765-109">\[in\] The components to OR with *src0*.</span></span> <span data-ttu-id="9b765-110">Это значение должно быть неупорядоченным представлением доступа (UAV) (u \# ).</span><span class="sxs-lookup"><span data-stu-id="9b765-110">This value must be an unordered access view (UAV) (u\#).</span></span> <span data-ttu-id="9b765-111">В шейдере вычислений он также может быть общей памятью группы потоков (g \# ).</span><span class="sxs-lookup"><span data-stu-id="9b765-111">In the compute shader it can also be thread group shared memory (g\#).</span></span> <br/> |
| <span data-ttu-id="9b765-112"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*дстаддресс*</span><span class="sxs-lookup"><span data-stu-id="9b765-112"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*</span></span><br/> | <span data-ttu-id="9b765-113">\[в \] адресе памяти.</span><span class="sxs-lookup"><span data-stu-id="9b765-113">\[in\] The memory address.</span></span><br/>                                                                                                                                                |
| <span data-ttu-id="9b765-114"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="9b765-114"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>                                                | <span data-ttu-id="9b765-115">\[в \] компонентах или с *летнего времени*.</span><span class="sxs-lookup"><span data-stu-id="9b765-115">\[in\] The components to OR with *dst*.</span></span><br/>                                                                                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="9b765-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="9b765-116">Remarks</span></span>

<span data-ttu-id="9b765-117">Эта инструкция выполняет атомарную операцию с одним компонентом 32-битным побитовым или операндом *src0* в *летнее* время в 32-бит на компонент, адрес *дстаддресс*.</span><span class="sxs-lookup"><span data-stu-id="9b765-117">This instruction performs a single component 32-bit bitwise OR of operand *src0* into *dst* at 32-bit per component address *dstAddress*, performed atomically.</span></span>

<span data-ttu-id="9b765-118">Количество компонентов, взятых из адреса, определяется размерностью *летнего времени* \# или g \# .</span><span class="sxs-lookup"><span data-stu-id="9b765-118">The number of components taken from the address is determined by the dimensionality of *dst* u\# or g\#.</span></span>

<span data-ttu-id="9b765-119">Если *DST* имеет тип u \# , его можно объявить как необработанный, типизированный или структурированный.</span><span class="sxs-lookup"><span data-stu-id="9b765-119">If *dst* is a u\#, it can be declared as raw, typed or structured.</span></span> <span data-ttu-id="9b765-120">При вводе он должен быть объявлен как UINT/Синт с форматом привязанного ресурса, R32 \_ uint/ \_ Синт.</span><span class="sxs-lookup"><span data-stu-id="9b765-120">If typed, it must be declared as UINT/SINT with the bound resource format being R32\_UINT/\_SINT.</span></span>

<span data-ttu-id="9b765-121">Если *DST* имеет значение g \# , его необходимо объявить как необработанный или структурированный.</span><span class="sxs-lookup"><span data-stu-id="9b765-121">If *dst* is g\#, it must be declared as raw or structured.</span></span>

<span data-ttu-id="9b765-122">В шейдере ничего не возвращается.</span><span class="sxs-lookup"><span data-stu-id="9b765-122">Nothing is returned to the shader.</span></span>

<span data-ttu-id="9b765-123">Если вызов шейдера неактивен, например, если точка была удалена раньше при выполнении или если обнаружено попиксельное или примерное обращение только в качестве вспомогательного метода к реальному пикселу или примеру для производных, эта инструкция не изменяет память на *летнее* время (без предупреждения).</span><span class="sxs-lookup"><span data-stu-id="9b765-123">If the shader invocation is inactive, for example if the pixel has been discarded earlier in its execution, or if a pixel/sample invocation only exists to serve as a helper to a real pixel/sample for derivatives, this instruction does not alter the *dst* memory at all (silently).</span></span>

<span data-ttu-id="9b765-124">Исходящие адреса в u \# не записываются в память, за исключением случаев, когда значение u \# структурировано, а смещение в байтах в структуре (второй компонент адреса) вызывает неограниченный доступ, а все содержимое UAV становится неопределенным.</span><span class="sxs-lookup"><span data-stu-id="9b765-124">Out of bounds addressing on u\# causes nothing to be written to memory, except if the u\# is structured, and the byte offset into the struct (second component of the address) is causing the out of bounds access, then the entire contents of the UAV become undefined.</span></span>

<span data-ttu-id="9b765-125">Исходящие адреса в g \# (границы этого конкретного g \# , а не всю общую память) приводят к тому, что все содержимое всей общей памяти становится неопределенным.</span><span class="sxs-lookup"><span data-stu-id="9b765-125">Out of bounds addressing on g\# (the bounds of that particular g\#, as opposed to all shared memory) causes the entire contents of all shared memory to become undefined.</span></span>

<span data-ttu-id="9b765-126">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="9b765-126">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="9b765-127">Вершина</span><span class="sxs-lookup"><span data-stu-id="9b765-127">Vertex</span></span> | <span data-ttu-id="9b765-128">Поверхности</span><span class="sxs-lookup"><span data-stu-id="9b765-128">Hull</span></span> | <span data-ttu-id="9b765-129">Домен</span><span class="sxs-lookup"><span data-stu-id="9b765-129">Domain</span></span> | <span data-ttu-id="9b765-130">Геометрия</span><span class="sxs-lookup"><span data-stu-id="9b765-130">Geometry</span></span> | <span data-ttu-id="9b765-131">Пиксель</span><span class="sxs-lookup"><span data-stu-id="9b765-131">Pixel</span></span> | <span data-ttu-id="9b765-132">Вычисления</span><span class="sxs-lookup"><span data-stu-id="9b765-132">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="9b765-133">X</span><span class="sxs-lookup"><span data-stu-id="9b765-133">X</span></span>     | <span data-ttu-id="9b765-134">X</span><span class="sxs-lookup"><span data-stu-id="9b765-134">X</span></span>       |



 

<span data-ttu-id="9b765-135">Так как Уавс доступны на всех стадиях шейдера для Direct3D 11,1, эта инструкция применяется ко всем этапам шейдера для среды выполнения Direct3D 11,1, которая доступна начиная с Windows 8.</span><span class="sxs-lookup"><span data-stu-id="9b765-135">Because UAVs are available at all shader stages for Direct3D 11.1, this instruction applies to all shader stages for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="9b765-136">Вершина</span><span class="sxs-lookup"><span data-stu-id="9b765-136">Vertex</span></span> | <span data-ttu-id="9b765-137">Поверхности</span><span class="sxs-lookup"><span data-stu-id="9b765-137">Hull</span></span> | <span data-ttu-id="9b765-138">Домен</span><span class="sxs-lookup"><span data-stu-id="9b765-138">Domain</span></span> | <span data-ttu-id="9b765-139">Геометрия</span><span class="sxs-lookup"><span data-stu-id="9b765-139">Geometry</span></span> | <span data-ttu-id="9b765-140">Пиксель</span><span class="sxs-lookup"><span data-stu-id="9b765-140">Pixel</span></span> | <span data-ttu-id="9b765-141">Вычисления</span><span class="sxs-lookup"><span data-stu-id="9b765-141">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="9b765-142">X</span><span class="sxs-lookup"><span data-stu-id="9b765-142">X</span></span>      | <span data-ttu-id="9b765-143">X</span><span class="sxs-lookup"><span data-stu-id="9b765-143">X</span></span>    | <span data-ttu-id="9b765-144">X</span><span class="sxs-lookup"><span data-stu-id="9b765-144">X</span></span>      | <span data-ttu-id="9b765-145">X</span><span class="sxs-lookup"><span data-stu-id="9b765-145">X</span></span>        | <span data-ttu-id="9b765-146">X</span><span class="sxs-lookup"><span data-stu-id="9b765-146">X</span></span>     | <span data-ttu-id="9b765-147">X</span><span class="sxs-lookup"><span data-stu-id="9b765-147">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="9b765-148">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="9b765-148">Minimum Shader Model</span></span>

<span data-ttu-id="9b765-149">Эта инструкция поддерживается в следующих моделях шейдеров:</span><span class="sxs-lookup"><span data-stu-id="9b765-149">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="9b765-150">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="9b765-150">Shader Model</span></span>                                              | <span data-ttu-id="9b765-151">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="9b765-151">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="9b765-152">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="9b765-152">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="9b765-153">да</span><span class="sxs-lookup"><span data-stu-id="9b765-153">yes</span></span>       |
| [<span data-ttu-id="9b765-154">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="9b765-154">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="9b765-155">Нет</span><span class="sxs-lookup"><span data-stu-id="9b765-155">no</span></span>        |
| [<span data-ttu-id="9b765-156">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="9b765-156">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="9b765-157">Нет</span><span class="sxs-lookup"><span data-stu-id="9b765-157">no</span></span>        |
| [<span data-ttu-id="9b765-158">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9b765-158">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="9b765-159">Нет</span><span class="sxs-lookup"><span data-stu-id="9b765-159">no</span></span>        |
| [<span data-ttu-id="9b765-160">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9b765-160">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="9b765-161">Нет</span><span class="sxs-lookup"><span data-stu-id="9b765-161">no</span></span>        |
| [<span data-ttu-id="9b765-162">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9b765-162">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="9b765-163">Нет</span><span class="sxs-lookup"><span data-stu-id="9b765-163">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="9b765-164">См. также</span><span class="sxs-lookup"><span data-stu-id="9b765-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9b765-165">Сборка Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9b765-165">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





