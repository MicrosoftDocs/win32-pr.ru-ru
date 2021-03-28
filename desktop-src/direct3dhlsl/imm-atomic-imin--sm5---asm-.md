---
title: imm_atomic_imin (SM5-ASM)
description: Немедленное неатомарное подписанное значение min в память. Возвращает значение в памяти перед операцией Max.
ms.assetid: 8E104FFA-D086-49FD-9063-B950B6B1548B
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c48b39da642105cacc0936abe1874d81c88e79b4
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104335560"
---
# <a name="imm_atomic_imin-sm5---asm"></a><span data-ttu-id="47a67-104">IMM \_ Atomic \_ Имин (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="47a67-104">imm\_atomic\_imin (sm5 - asm)</span></span>

<span data-ttu-id="47a67-105">Немедленное неатомарное подписанное значение min в память.</span><span class="sxs-lookup"><span data-stu-id="47a67-105">Immediate atomic signed min to memory.</span></span> <span data-ttu-id="47a67-106">Возвращает значение в памяти перед операцией Max.</span><span class="sxs-lookup"><span data-stu-id="47a67-106">Returns value in memory before the max operation.</span></span>



| <span data-ttu-id="47a67-107">IMM \_ Atomic \_ Имин dst0 \[ . единственная \_ \_ Маска компонента \] , dst1, дстаддресс \[ . свиззле \] , src0 \[ . Select \_ Component\]</span><span class="sxs-lookup"><span data-stu-id="47a67-107">imm\_atomic\_imin dst0\[.single\_component\_mask\], dst1, dstAddress\[.swizzle\], src0\[.select\_component\]</span></span> |
|--------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="47a67-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="47a67-108">Item</span></span>                                                                                                           | <span data-ttu-id="47a67-109">Описание</span><span class="sxs-lookup"><span data-stu-id="47a67-109">Description</span></span>                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="47a67-110"><span id="dst0"></span><span id="DST0"></span>*dst0*</span><span class="sxs-lookup"><span data-stu-id="47a67-110"><span id="dst0"></span><span id="DST0"></span>*dst0*</span></span><br/>                                                | <span data-ttu-id="47a67-111">\[в \] содержит значение из *dst1* перед этой инструкцией.</span><span class="sxs-lookup"><span data-stu-id="47a67-111">\[in\] Contains the value from *dst1* before this instruction.</span></span><br/>                                                         |
| <span data-ttu-id="47a67-112"><span id="dst1"></span><span id="DST1"></span>*dst1*</span><span class="sxs-lookup"><span data-stu-id="47a67-112"><span id="dst1"></span><span id="DST1"></span>*dst1*</span></span><br/>                                                | <span data-ttu-id="47a67-113">\[в \] представлении неупорядоченного доступа (UAV) (u \# ).</span><span class="sxs-lookup"><span data-stu-id="47a67-113">\[in\] An unordered access view (UAV) (u\#).</span></span> <span data-ttu-id="47a67-114">В шейдере вычислений это также может быть общей памятью группы потоков (g \# ).</span><span class="sxs-lookup"><span data-stu-id="47a67-114">In the compute shader this can also be thread group shared memory (g\#).</span></span> <br/> |
| <span data-ttu-id="47a67-115"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*дстаддресс*</span><span class="sxs-lookup"><span data-stu-id="47a67-115"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*</span></span><br/> | <span data-ttu-id="47a67-116">\[в \] адресе памяти.</span><span class="sxs-lookup"><span data-stu-id="47a67-116">\[in\] The memory address.</span></span><br/>                                                                                             |
| <span data-ttu-id="47a67-117"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="47a67-117"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>                                                | <span data-ttu-id="47a67-118">\[в \] значении, сравниваемом с *dst1* по адресу *дстаддресс*.</span><span class="sxs-lookup"><span data-stu-id="47a67-118">\[in\] The value to compare to *dst1* at *dstAddress*.</span></span><br/>                                                                 |



 

## <a name="remarks"></a><span data-ttu-id="47a67-119">Примечания</span><span class="sxs-lookup"><span data-stu-id="47a67-119">Remarks</span></span>

<span data-ttu-id="47a67-120">Инструкция Сиси выполняет один компонент 32-bit со знаком *src0* с *dst1* в 32-бит на компонент, адрес *дстаддресс*.</span><span class="sxs-lookup"><span data-stu-id="47a67-120">Thisi instruction performs a single component 32-bit signed minimum of operand *src0* with *dst1* at 32-bit per component address *dstAddress*.</span></span>

<span data-ttu-id="47a67-121">Если *dst1* имеет тип u \# , то он мог быть объявлен как необработанный, типизированный или структурированный.</span><span class="sxs-lookup"><span data-stu-id="47a67-121">If *dst1* is a u\#, it may have been declared as raw, typed or structured.</span></span> <span data-ttu-id="47a67-122">При вводе он должен быть объявлен как UINT/Синт с форматом привязанного ресурса, R32 \_ uint/ \_ Синт.</span><span class="sxs-lookup"><span data-stu-id="47a67-122">If typed, it must be declared as UINT/SINT with the bound resource format being R32\_UINT/\_SINT.</span></span>

<span data-ttu-id="47a67-123">Если *dst1* имеет значение g \# , то его необходимо объявить как необработанный или структурированный.</span><span class="sxs-lookup"><span data-stu-id="47a67-123">If *dst1* is g\#, it must be declared as raw or structured.</span></span>

<span data-ttu-id="47a67-124">Значение в памяти *dst1* до min возвращается в *dst0*.</span><span class="sxs-lookup"><span data-stu-id="47a67-124">The value in *dst1* memory before min is returned to *dst0*.</span></span>

<span data-ttu-id="47a67-125">Количество компонентов, взятых из адреса, определяется размерностью *dst1*.</span><span class="sxs-lookup"><span data-stu-id="47a67-125">The number of components taken from the address is determined by the dimensionality of *dst1*.</span></span>

<span data-ttu-id="47a67-126">Вся операция выполняется атомарно.</span><span class="sxs-lookup"><span data-stu-id="47a67-126">The entire operation is performed atomically.</span></span>

<span data-ttu-id="47a67-127">Если вызов шейдера неактивен, например, если точка была удалена раньше при выполнении, или вызов в качестве вспомогательного метода к реальному пикселю или примеру для производных, эта инструкция не изменяет память *dst1* , а возвращаемое значение не определено.</span><span class="sxs-lookup"><span data-stu-id="47a67-127">If the shader invocation is inactive, for example if the pixel has been discarded earlier in its execution, or a pixel/sample invocation only exists to serve as a helper to a real pixel/sample for derivatives, this instruction does not alter the *dst1* memory at all, and the returned value is undefined.</span></span>

<span data-ttu-id="47a67-128">Исходящие адреса в u \# не записываются в память, за исключением случаев, когда u \# является структурированным, а смещение в байтах в структуре (второй компонент адреса) вызывает неограниченный доступ, а все содержимое UAV становится неопределенным.</span><span class="sxs-lookup"><span data-stu-id="47a67-128">Out of bounds addressing on u\# causes nothing to be written to memory, except if the u\# is structured, and byte offset into the struct (second component of the address) is causing the out of bounds access, then the entire contents of the UAV become undefined.</span></span>

<span data-ttu-id="47a67-129">Исходящие адреса в u \# или g \# вызывают неопределенный результат, возвращаемый шейдеру в *dst0*.</span><span class="sxs-lookup"><span data-stu-id="47a67-129">Out of bounds addressing on u\# or g\# causes an undefined result to be returned to the shader in *dst0*.</span></span>

<span data-ttu-id="47a67-130">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="47a67-130">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="47a67-131">Вершина</span><span class="sxs-lookup"><span data-stu-id="47a67-131">Vertex</span></span> | <span data-ttu-id="47a67-132">Поверхности</span><span class="sxs-lookup"><span data-stu-id="47a67-132">Hull</span></span> | <span data-ttu-id="47a67-133">Домен</span><span class="sxs-lookup"><span data-stu-id="47a67-133">Domain</span></span> | <span data-ttu-id="47a67-134">Геометрия</span><span class="sxs-lookup"><span data-stu-id="47a67-134">Geometry</span></span> | <span data-ttu-id="47a67-135">Пиксель</span><span class="sxs-lookup"><span data-stu-id="47a67-135">Pixel</span></span> | <span data-ttu-id="47a67-136">Вычисления</span><span class="sxs-lookup"><span data-stu-id="47a67-136">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="47a67-137">X</span><span class="sxs-lookup"><span data-stu-id="47a67-137">X</span></span>     | <span data-ttu-id="47a67-138">X</span><span class="sxs-lookup"><span data-stu-id="47a67-138">X</span></span>       |



 

<span data-ttu-id="47a67-139">Так как Уавс доступны на всех стадиях шейдера для Direct3D 11,1, эта инструкция применяется ко всем этапам шейдера для среды выполнения Direct3D 11,1, которая доступна начиная с Windows 8.</span><span class="sxs-lookup"><span data-stu-id="47a67-139">Because UAVs are available at all shader stages for Direct3D 11.1, this instruction applies to all shader stages for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="47a67-140">Вершина</span><span class="sxs-lookup"><span data-stu-id="47a67-140">Vertex</span></span> | <span data-ttu-id="47a67-141">Поверхности</span><span class="sxs-lookup"><span data-stu-id="47a67-141">Hull</span></span> | <span data-ttu-id="47a67-142">Домен</span><span class="sxs-lookup"><span data-stu-id="47a67-142">Domain</span></span> | <span data-ttu-id="47a67-143">Геометрия</span><span class="sxs-lookup"><span data-stu-id="47a67-143">Geometry</span></span> | <span data-ttu-id="47a67-144">Пиксель</span><span class="sxs-lookup"><span data-stu-id="47a67-144">Pixel</span></span> | <span data-ttu-id="47a67-145">Вычисления</span><span class="sxs-lookup"><span data-stu-id="47a67-145">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="47a67-146">X</span><span class="sxs-lookup"><span data-stu-id="47a67-146">X</span></span>      | <span data-ttu-id="47a67-147">X</span><span class="sxs-lookup"><span data-stu-id="47a67-147">X</span></span>    | <span data-ttu-id="47a67-148">X</span><span class="sxs-lookup"><span data-stu-id="47a67-148">X</span></span>      | <span data-ttu-id="47a67-149">X</span><span class="sxs-lookup"><span data-stu-id="47a67-149">X</span></span>        | <span data-ttu-id="47a67-150">X</span><span class="sxs-lookup"><span data-stu-id="47a67-150">X</span></span>     | <span data-ttu-id="47a67-151">X</span><span class="sxs-lookup"><span data-stu-id="47a67-151">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="47a67-152">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="47a67-152">Minimum Shader Model</span></span>

<span data-ttu-id="47a67-153">Эта инструкция поддерживается в следующих моделях шейдеров:</span><span class="sxs-lookup"><span data-stu-id="47a67-153">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="47a67-154">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="47a67-154">Shader Model</span></span>                                              | <span data-ttu-id="47a67-155">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="47a67-155">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="47a67-156">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="47a67-156">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="47a67-157">да</span><span class="sxs-lookup"><span data-stu-id="47a67-157">yes</span></span>       |
| [<span data-ttu-id="47a67-158">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="47a67-158">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="47a67-159">Нет</span><span class="sxs-lookup"><span data-stu-id="47a67-159">no</span></span>        |
| [<span data-ttu-id="47a67-160">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="47a67-160">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="47a67-161">Нет</span><span class="sxs-lookup"><span data-stu-id="47a67-161">no</span></span>        |
| [<span data-ttu-id="47a67-162">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="47a67-162">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="47a67-163">Нет</span><span class="sxs-lookup"><span data-stu-id="47a67-163">no</span></span>        |
| [<span data-ttu-id="47a67-164">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="47a67-164">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="47a67-165">Нет</span><span class="sxs-lookup"><span data-stu-id="47a67-165">no</span></span>        |
| [<span data-ttu-id="47a67-166">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="47a67-166">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="47a67-167">Нет</span><span class="sxs-lookup"><span data-stu-id="47a67-167">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="47a67-168">См. также</span><span class="sxs-lookup"><span data-stu-id="47a67-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="47a67-169">Сборка Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="47a67-169">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





