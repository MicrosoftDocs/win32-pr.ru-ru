---
title: imm_atomic_umin (SM5-ASM)
description: Непосредственный атомарный неподписанный минимум в память. Возвращает значение в памяти перед операцией Max.
ms.assetid: B4556DA0-EE34-4420-A3AE-B340B4B1EB83
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8c65b2b5a58859e0729f567d9575f889b589821
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104069324"
---
# <a name="imm_atomic_umin-sm5---asm"></a><span data-ttu-id="266a8-104">IMM \_ Atomic \_ Умин (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="266a8-104">imm\_atomic\_umin (sm5 - asm)</span></span>

<span data-ttu-id="266a8-105">Непосредственный атомарный неподписанный минимум в память.</span><span class="sxs-lookup"><span data-stu-id="266a8-105">Immediate atomic unsigned min to memory.</span></span> <span data-ttu-id="266a8-106">Возвращает значение в памяти перед операцией Max.</span><span class="sxs-lookup"><span data-stu-id="266a8-106">Returns value in memory before the max operation.</span></span>



| <span data-ttu-id="266a8-107">IMM \_ Atomic \_ Умин dst0 \[ . единственная \_ \_ Маска компонента \] , dst1, дстаддресс \[ . свиззле \] , src0 \[ . Select \_ Component\]</span><span class="sxs-lookup"><span data-stu-id="266a8-107">imm\_atomic\_umin dst0\[.single\_component\_mask\], dst1, dstAddress\[.swizzle\], src0\[.select\_component\]</span></span> |
|--------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="266a8-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="266a8-108">Item</span></span>                                                                                                           | <span data-ttu-id="266a8-109">Описание</span><span class="sxs-lookup"><span data-stu-id="266a8-109">Description</span></span>                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="266a8-110"><span id="dst0"></span><span id="DST0"></span>*dst0*</span><span class="sxs-lookup"><span data-stu-id="266a8-110"><span id="dst0"></span><span id="DST0"></span>*dst0*</span></span><br/>                                                | <span data-ttu-id="266a8-111">\[в \] содержит значение из *dst1* перед этой инструкцией.</span><span class="sxs-lookup"><span data-stu-id="266a8-111">\[in\] Contains the value from *dst1* before this instruction.</span></span><br/>                                                         |
| <span data-ttu-id="266a8-112"><span id="dst1"></span><span id="DST1"></span>*dst1*</span><span class="sxs-lookup"><span data-stu-id="266a8-112"><span id="dst1"></span><span id="DST1"></span>*dst1*</span></span><br/>                                                | <span data-ttu-id="266a8-113">\[в \] представлении неупорядоченного доступа (UAV) (u \# ).</span><span class="sxs-lookup"><span data-stu-id="266a8-113">\[in\] An unordered access view (UAV) (u\#).</span></span> <span data-ttu-id="266a8-114">В шейдере вычислений это также может быть общей памятью группы потоков (g \# ).</span><span class="sxs-lookup"><span data-stu-id="266a8-114">In the compute shader this can also be thread group shared memory (g\#).</span></span> <br/> |
| <span data-ttu-id="266a8-115"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*дстаддресс*</span><span class="sxs-lookup"><span data-stu-id="266a8-115"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*</span></span><br/> | <span data-ttu-id="266a8-116">\[в \] адресе памяти.</span><span class="sxs-lookup"><span data-stu-id="266a8-116">\[in\] The memory address.</span></span><br/>                                                                                             |
| <span data-ttu-id="266a8-117"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="266a8-117"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>                                                | <span data-ttu-id="266a8-118">\[в \] значении, сравниваемом с *dst1* по адресу *дстаддресс*.</span><span class="sxs-lookup"><span data-stu-id="266a8-118">\[in\] The value to compare to *dst1* at *dstAddress*.</span></span><br/>                                                                 |



 

## <a name="remarks"></a><span data-ttu-id="266a8-119">Примечания</span><span class="sxs-lookup"><span data-stu-id="266a8-119">Remarks</span></span>

<span data-ttu-id="266a8-120">Эта инструкция выполняет один компонент 32-bit без знака *src0* с *dst1* в 32-бит на компонент, адрес *дстаддресс*.</span><span class="sxs-lookup"><span data-stu-id="266a8-120">This instruction performs a single component 32-bit unsigned minimum of operand *src0* with *dst1* at 32-bit per component address *dstAddress*.</span></span>

<span data-ttu-id="266a8-121">Если *dst1* имеет тип u \# , то он мог быть объявлен как необработанный, типизированный или структурированный.</span><span class="sxs-lookup"><span data-stu-id="266a8-121">If *dst1* is a u\#, it may have been declared as raw, typed or structured.</span></span> <span data-ttu-id="266a8-122">При вводе он должен быть объявлен как UINT/Синт с форматом привязанного ресурса, R32 \_ uint/ \_ Синт.</span><span class="sxs-lookup"><span data-stu-id="266a8-122">If typed, it must be declared as UINT/SINT with the bound resource format being R32\_UINT/\_SINT.</span></span>

<span data-ttu-id="266a8-123">Если *dst1* имеет значение g \# , то его необходимо объявить как необработанный или структурированный.</span><span class="sxs-lookup"><span data-stu-id="266a8-123">If *dst1* is g\#, it must be declared as raw or structured.</span></span>

<span data-ttu-id="266a8-124">Значение в памяти *dst1* до min возвращается в *dst0*.</span><span class="sxs-lookup"><span data-stu-id="266a8-124">The value in *dst1* memory before min is returned to *dst0*.</span></span>

<span data-ttu-id="266a8-125">Количество компонентов, взятых из адреса, определяется размерностью *dst1*.</span><span class="sxs-lookup"><span data-stu-id="266a8-125">The number of components taken from the address is determined by the dimensionality of *dst1*.</span></span>

<span data-ttu-id="266a8-126">Вся операция выполняется атомарно.</span><span class="sxs-lookup"><span data-stu-id="266a8-126">The entire operation is performed atomically.</span></span>

<span data-ttu-id="266a8-127">Если вызов шейдера неактивен, например, если точка, которая была удалена раньше при выполнении, или вызов в качестве вспомогательного метода к реальному пикселу или примеру для производных, эта инструкция не изменяет память *dst1* , а возвращаемое значение не определено.</span><span class="sxs-lookup"><span data-stu-id="266a8-127">If the shader invocation is inactive, for example if the pixel having been discarded earlier in its execution, or a pixel/sample invocation only exists to serve as a helper to a real pixel/sample for derivatives, this instruction does not alter the *dst1* memory at all, and the returned value is undefined.</span></span>

<span data-ttu-id="266a8-128">Исходящие адреса в u \# не записываются в память, за исключением случаев, когда u \# является структурированным, а смещение в байтах в структуре (второй компонент адреса) вызывает неограниченный доступ, а все содержимое UAV становится неопределенным.</span><span class="sxs-lookup"><span data-stu-id="266a8-128">Out of bounds addressing on u\# causes nothing to be written to memory, except if the u\# is structured, and byte offset into the struct (second component of the address) is causing the out of bounds access, then the entire contents of the UAV become undefined.</span></span>

<span data-ttu-id="266a8-129">Исходящие адреса в u \# или g \# вызывают неопределенный результат, возвращаемый шейдеру в *dst0*.</span><span class="sxs-lookup"><span data-stu-id="266a8-129">Out of bounds addressing on u\# or g\# causes an undefined result to be returned to the shader in *dst0*.</span></span>

<span data-ttu-id="266a8-130">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="266a8-130">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="266a8-131">Вершина</span><span class="sxs-lookup"><span data-stu-id="266a8-131">Vertex</span></span> | <span data-ttu-id="266a8-132">Поверхности</span><span class="sxs-lookup"><span data-stu-id="266a8-132">Hull</span></span> | <span data-ttu-id="266a8-133">Домен</span><span class="sxs-lookup"><span data-stu-id="266a8-133">Domain</span></span> | <span data-ttu-id="266a8-134">Геометрия</span><span class="sxs-lookup"><span data-stu-id="266a8-134">Geometry</span></span> | <span data-ttu-id="266a8-135">Пиксель</span><span class="sxs-lookup"><span data-stu-id="266a8-135">Pixel</span></span> | <span data-ttu-id="266a8-136">Вычисления</span><span class="sxs-lookup"><span data-stu-id="266a8-136">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="266a8-137">X</span><span class="sxs-lookup"><span data-stu-id="266a8-137">X</span></span>     | <span data-ttu-id="266a8-138">X</span><span class="sxs-lookup"><span data-stu-id="266a8-138">X</span></span>       |



 

<span data-ttu-id="266a8-139">Так как Уавс доступны на всех стадиях шейдера для Direct3D 11,1, эта инструкция применяется ко всем этапам шейдера для среды выполнения Direct3D 11,1, которая доступна начиная с Windows 8.</span><span class="sxs-lookup"><span data-stu-id="266a8-139">Because UAVs are available at all shader stages for Direct3D 11.1, this instruction applies to all shader stages for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="266a8-140">Вершина</span><span class="sxs-lookup"><span data-stu-id="266a8-140">Vertex</span></span> | <span data-ttu-id="266a8-141">Поверхности</span><span class="sxs-lookup"><span data-stu-id="266a8-141">Hull</span></span> | <span data-ttu-id="266a8-142">Домен</span><span class="sxs-lookup"><span data-stu-id="266a8-142">Domain</span></span> | <span data-ttu-id="266a8-143">Геометрия</span><span class="sxs-lookup"><span data-stu-id="266a8-143">Geometry</span></span> | <span data-ttu-id="266a8-144">Пиксель</span><span class="sxs-lookup"><span data-stu-id="266a8-144">Pixel</span></span> | <span data-ttu-id="266a8-145">Вычисления</span><span class="sxs-lookup"><span data-stu-id="266a8-145">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="266a8-146">X</span><span class="sxs-lookup"><span data-stu-id="266a8-146">X</span></span>      | <span data-ttu-id="266a8-147">X</span><span class="sxs-lookup"><span data-stu-id="266a8-147">X</span></span>    | <span data-ttu-id="266a8-148">X</span><span class="sxs-lookup"><span data-stu-id="266a8-148">X</span></span>      | <span data-ttu-id="266a8-149">X</span><span class="sxs-lookup"><span data-stu-id="266a8-149">X</span></span>        | <span data-ttu-id="266a8-150">X</span><span class="sxs-lookup"><span data-stu-id="266a8-150">X</span></span>     | <span data-ttu-id="266a8-151">X</span><span class="sxs-lookup"><span data-stu-id="266a8-151">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="266a8-152">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="266a8-152">Minimum Shader Model</span></span>

<span data-ttu-id="266a8-153">Эта инструкция поддерживается в следующих моделях шейдеров:</span><span class="sxs-lookup"><span data-stu-id="266a8-153">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="266a8-154">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="266a8-154">Shader Model</span></span>                                              | <span data-ttu-id="266a8-155">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="266a8-155">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="266a8-156">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="266a8-156">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="266a8-157">да</span><span class="sxs-lookup"><span data-stu-id="266a8-157">yes</span></span>       |
| [<span data-ttu-id="266a8-158">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="266a8-158">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="266a8-159">Нет</span><span class="sxs-lookup"><span data-stu-id="266a8-159">no</span></span>        |
| [<span data-ttu-id="266a8-160">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="266a8-160">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="266a8-161">Нет</span><span class="sxs-lookup"><span data-stu-id="266a8-161">no</span></span>        |
| [<span data-ttu-id="266a8-162">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="266a8-162">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="266a8-163">Нет</span><span class="sxs-lookup"><span data-stu-id="266a8-163">no</span></span>        |
| [<span data-ttu-id="266a8-164">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="266a8-164">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="266a8-165">Нет</span><span class="sxs-lookup"><span data-stu-id="266a8-165">no</span></span>        |
| [<span data-ttu-id="266a8-166">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="266a8-166">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="266a8-167">Нет</span><span class="sxs-lookup"><span data-stu-id="266a8-167">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="266a8-168">См. также</span><span class="sxs-lookup"><span data-stu-id="266a8-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="266a8-169">Сборка Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="266a8-169">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





