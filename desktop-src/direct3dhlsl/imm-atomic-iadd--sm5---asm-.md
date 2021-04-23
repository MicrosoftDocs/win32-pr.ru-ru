---
title: imm_atomic_iadd (SM5-ASM)
description: Мгновенное атомарное целое число добавляет в память. Возвращает значение в памяти перед добавлением.
ms.assetid: 24136B4C-D37C-4449-A318-57145BB8D8E9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2695e23707fb61cd576748e2e83829cd7dc65259
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104412209"
---
# <a name="imm_atomic_iadd-sm5---asm"></a><span data-ttu-id="ae4c8-104">IMM \_ Atomic \_ IAdd (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="ae4c8-104">imm\_atomic\_iadd (sm5 - asm)</span></span>

<span data-ttu-id="ae4c8-105">Мгновенное атомарное целое число добавляет в память.</span><span class="sxs-lookup"><span data-stu-id="ae4c8-105">Immediate atomic integer add to memory.</span></span> <span data-ttu-id="ae4c8-106">Возвращает значение в памяти перед добавлением.</span><span class="sxs-lookup"><span data-stu-id="ae4c8-106">Returns the value in memory before the add.</span></span>



| <span data-ttu-id="ae4c8-107">IMM \_ Atomic \_ IAdd dst0 \[ . единственная \_ \_ Маска компонента \] , dst1, дстаддресс \[ . свиззле \] , src0 \[ . Select \_ Component\]</span><span class="sxs-lookup"><span data-stu-id="ae4c8-107">imm\_atomic\_iadd dst0\[.single\_component\_mask\], dst1, dstAddress\[.swizzle\], src0\[.select\_component\]</span></span> |
|--------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="ae4c8-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="ae4c8-108">Item</span></span>                                                                                                           | <span data-ttu-id="ae4c8-109">Описание</span><span class="sxs-lookup"><span data-stu-id="ae4c8-109">Description</span></span>                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae4c8-110"><span id="dst0"></span><span id="DST0"></span>*dst0*</span><span class="sxs-lookup"><span data-stu-id="ae4c8-110"><span id="dst0"></span><span id="DST0"></span>*dst0*</span></span><br/>                                                | <span data-ttu-id="ae4c8-111">\[в \] содержит значение в *dst1* перед записью.</span><span class="sxs-lookup"><span data-stu-id="ae4c8-111">\[in\] Contains the value in *dst1* before the write.</span></span> <br/>                                                                           |
| <span data-ttu-id="ae4c8-112"><span id="dst1"></span><span id="DST1"></span>*dst1*</span><span class="sxs-lookup"><span data-stu-id="ae4c8-112"><span id="dst1"></span><span id="DST1"></span>*dst1*</span></span><br/>                                                | <span data-ttu-id="ae4c8-113">Это значение должно быть неупорядоченным представлением доступа (UAV) (u \# ).</span><span class="sxs-lookup"><span data-stu-id="ae4c8-113">This value must be an unordered access view (UAV) (u\#).</span></span> <span data-ttu-id="ae4c8-114">В шейдере вычислений он также может быть общей памятью группы потоков (g \# ).</span><span class="sxs-lookup"><span data-stu-id="ae4c8-114">In the compute shader it can also be thread group shared memory (g\#).</span></span> <br/> |
| <span data-ttu-id="ae4c8-115"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*дстаддресс*</span><span class="sxs-lookup"><span data-stu-id="ae4c8-115"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*</span></span><br/> | <span data-ttu-id="ae4c8-116">\[в \] наддресс памяти.</span><span class="sxs-lookup"><span data-stu-id="ae4c8-116">\[in\] The memory naddress.</span></span><br/>                                                                                                      |
| <span data-ttu-id="ae4c8-117"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="ae4c8-117"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>                                                | <span data-ttu-id="ae4c8-118">\[\]значение, добавляемое в *dst1*.</span><span class="sxs-lookup"><span data-stu-id="ae4c8-118">\[in\] The value to add to *dst1*.</span></span><br/>                                                                                               |



 

## <a name="remarks"></a><span data-ttu-id="ae4c8-119">Примечания</span><span class="sxs-lookup"><span data-stu-id="ae4c8-119">Remarks</span></span>

<span data-ttu-id="ae4c8-120">Эта инструкция выполняет одно 32-разрядное целочисленное Добавление операнда *src0* с *dst1* в 32-бит на компонент адрес *дстаддресс*.</span><span class="sxs-lookup"><span data-stu-id="ae4c8-120">This instruction performs a single component 32-bit integer add of operand *src0* with *dst1* at 32-bit per component address *dstAddress*.</span></span> <span data-ttu-id="ae4c8-121">Он не чувствителен к подписанию.</span><span class="sxs-lookup"><span data-stu-id="ae4c8-121">It is insensitive to sign.</span></span>

<span data-ttu-id="ae4c8-122">Если *dst1* имеет тип u \# , то он мог быть объявлен как необработанный, типизированный или структурированный.</span><span class="sxs-lookup"><span data-stu-id="ae4c8-122">If *dst1* is a u\#, it may have been declared as raw, typed or structured.</span></span> <span data-ttu-id="ae4c8-123">При вводе он должен быть объявлен как UINT/Синт с форматом привязанного ресурса, R32 \_ uint/ \_ Синт.</span><span class="sxs-lookup"><span data-stu-id="ae4c8-123">If typed, it must be declared as UINT/SINT with the bound resource format being R32\_UINT/\_SINT.</span></span>

<span data-ttu-id="ae4c8-124">Если *dst1* имеет значение g \# , то его необходимо объявить как необработанный или структурированный.</span><span class="sxs-lookup"><span data-stu-id="ae4c8-124">If *dst1* is g\#, it must be declared as raw or structured.</span></span>

<span data-ttu-id="ae4c8-125">Значение в памяти *dst1* перед добавлением возвращается в *dst0*.</span><span class="sxs-lookup"><span data-stu-id="ae4c8-125">The value in *dst1* memory before addition is returned to *dst0*.</span></span>

<span data-ttu-id="ae4c8-126">Количество компонентов, взятых из адреса, определяется размерностью *dst1*.</span><span class="sxs-lookup"><span data-stu-id="ae4c8-126">The number of components taken from the address is determined by the dimensionality of *dst1*.</span></span>

<span data-ttu-id="ae4c8-127">Вся операция выполняется атомарно.</span><span class="sxs-lookup"><span data-stu-id="ae4c8-127">The entire operation is performed atomically.</span></span>

<span data-ttu-id="ae4c8-128">Если вызов шейдера неактивен, например, если точка была удалена раньше при выполнении, или вызов в качестве вспомогательного метода к реальному пикселю или примеру для производных, эта инструкция не изменяет память *dst1* , а возвращаемое значение не определено.</span><span class="sxs-lookup"><span data-stu-id="ae4c8-128">If the shader invocation is inactive, for example if the pixel has been discarded earlier in its execution, or a pixel/sample invocation only exists to serve as a helper to a real pixel/sample for derivatives, this instruction does not alter the *dst1* memory at all, and the returned value is undefined.</span></span>

<span data-ttu-id="ae4c8-129">Исходящие адреса в u \# не записываются в память, за исключением случаев, когда u \# является структурированным, а смещение в байтах в структуре (второй компонент адреса) вызывает неограниченный доступ, а все содержимое UAV становится неопределенным.</span><span class="sxs-lookup"><span data-stu-id="ae4c8-129">Out of bounds addressing on u\# causes nothing to be written to memory, except if the u\# is structured, and byte offset into the struct (second component of the address) is causing the out of bounds access, then the entire contents of the UAV become undefined.</span></span>

<span data-ttu-id="ae4c8-130">Исходящие адреса в u \# или g \# вызывают неопределенный результат, возвращаемый шейдеру в *dst0*.</span><span class="sxs-lookup"><span data-stu-id="ae4c8-130">Out of bounds addressing on u\# or g\# causes an undefined result to be returned to the shader in *dst0*.</span></span>

<span data-ttu-id="ae4c8-131">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="ae4c8-131">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="ae4c8-132">Вершина</span><span class="sxs-lookup"><span data-stu-id="ae4c8-132">Vertex</span></span> | <span data-ttu-id="ae4c8-133">Поверхности</span><span class="sxs-lookup"><span data-stu-id="ae4c8-133">Hull</span></span> | <span data-ttu-id="ae4c8-134">Домен</span><span class="sxs-lookup"><span data-stu-id="ae4c8-134">Domain</span></span> | <span data-ttu-id="ae4c8-135">Геометрия</span><span class="sxs-lookup"><span data-stu-id="ae4c8-135">Geometry</span></span> | <span data-ttu-id="ae4c8-136">Пиксель</span><span class="sxs-lookup"><span data-stu-id="ae4c8-136">Pixel</span></span> | <span data-ttu-id="ae4c8-137">Вычисления</span><span class="sxs-lookup"><span data-stu-id="ae4c8-137">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="ae4c8-138">X</span><span class="sxs-lookup"><span data-stu-id="ae4c8-138">X</span></span>     | <span data-ttu-id="ae4c8-139">X</span><span class="sxs-lookup"><span data-stu-id="ae4c8-139">X</span></span>       |



 

<span data-ttu-id="ae4c8-140">Так как Уавс доступны на всех стадиях шейдера для Direct3D 11,1, эта инструкция применяется ко всем этапам шейдера для среды выполнения Direct3D 11,1, которая доступна начиная с Windows 8.</span><span class="sxs-lookup"><span data-stu-id="ae4c8-140">Because UAVs are available at all shader stages for Direct3D 11.1, this instruction applies to all shader stages for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="ae4c8-141">Вершина</span><span class="sxs-lookup"><span data-stu-id="ae4c8-141">Vertex</span></span> | <span data-ttu-id="ae4c8-142">Поверхности</span><span class="sxs-lookup"><span data-stu-id="ae4c8-142">Hull</span></span> | <span data-ttu-id="ae4c8-143">Домен</span><span class="sxs-lookup"><span data-stu-id="ae4c8-143">Domain</span></span> | <span data-ttu-id="ae4c8-144">Геометрия</span><span class="sxs-lookup"><span data-stu-id="ae4c8-144">Geometry</span></span> | <span data-ttu-id="ae4c8-145">Пиксель</span><span class="sxs-lookup"><span data-stu-id="ae4c8-145">Pixel</span></span> | <span data-ttu-id="ae4c8-146">Вычисления</span><span class="sxs-lookup"><span data-stu-id="ae4c8-146">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="ae4c8-147">X</span><span class="sxs-lookup"><span data-stu-id="ae4c8-147">X</span></span>      | <span data-ttu-id="ae4c8-148">X</span><span class="sxs-lookup"><span data-stu-id="ae4c8-148">X</span></span>    | <span data-ttu-id="ae4c8-149">X</span><span class="sxs-lookup"><span data-stu-id="ae4c8-149">X</span></span>      | <span data-ttu-id="ae4c8-150">X</span><span class="sxs-lookup"><span data-stu-id="ae4c8-150">X</span></span>        | <span data-ttu-id="ae4c8-151">X</span><span class="sxs-lookup"><span data-stu-id="ae4c8-151">X</span></span>     | <span data-ttu-id="ae4c8-152">X</span><span class="sxs-lookup"><span data-stu-id="ae4c8-152">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="ae4c8-153">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="ae4c8-153">Minimum Shader Model</span></span>

<span data-ttu-id="ae4c8-154">Эта инструкция поддерживается в следующих моделях шейдеров:</span><span class="sxs-lookup"><span data-stu-id="ae4c8-154">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="ae4c8-155">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="ae4c8-155">Shader Model</span></span>                                              | <span data-ttu-id="ae4c8-156">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="ae4c8-156">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="ae4c8-157">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="ae4c8-157">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="ae4c8-158">да</span><span class="sxs-lookup"><span data-stu-id="ae4c8-158">yes</span></span>       |
| [<span data-ttu-id="ae4c8-159">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="ae4c8-159">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="ae4c8-160">Нет</span><span class="sxs-lookup"><span data-stu-id="ae4c8-160">no</span></span>        |
| [<span data-ttu-id="ae4c8-161">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="ae4c8-161">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="ae4c8-162">Нет</span><span class="sxs-lookup"><span data-stu-id="ae4c8-162">no</span></span>        |
| [<span data-ttu-id="ae4c8-163">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ae4c8-163">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="ae4c8-164">Нет</span><span class="sxs-lookup"><span data-stu-id="ae4c8-164">no</span></span>        |
| [<span data-ttu-id="ae4c8-165">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ae4c8-165">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="ae4c8-166">Нет</span><span class="sxs-lookup"><span data-stu-id="ae4c8-166">no</span></span>        |
| [<span data-ttu-id="ae4c8-167">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ae4c8-167">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="ae4c8-168">Нет</span><span class="sxs-lookup"><span data-stu-id="ae4c8-168">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="ae4c8-169">См. также</span><span class="sxs-lookup"><span data-stu-id="ae4c8-169">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ae4c8-170">Сборка Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ae4c8-170">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





