---
title: imm_atomic_exch (SM5-ASM)
description: Прямой атомарный обмен данными между Exchange и памятью.
ms.assetid: D06AE57E-52A4-4579-84FF-7DE9E713A5E3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb38cd696af079c5ae7dc896db619b95dd1d1d6c
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104133330"
---
# <a name="imm_atomic_exch-sm5---asm"></a><span data-ttu-id="c2c75-103">IMM \_ Atomic для \_ валюты (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="c2c75-103">imm\_atomic\_exch (sm5 - asm)</span></span>

<span data-ttu-id="c2c75-104">Прямой атомарный обмен данными между Exchange и памятью.</span><span class="sxs-lookup"><span data-stu-id="c2c75-104">Immediate atomic exchange to memory.</span></span>



| <span data-ttu-id="c2c75-105">IMM \_ Atomic \_ dst0 \[ . одна \_ Маска компонента \_ \] , dst1, дстаддресс \[ . свиззле \] , src0 \[ . Select \_ Component\]</span><span class="sxs-lookup"><span data-stu-id="c2c75-105">imm\_atomic\_exch dst0\[.single\_component\_mask\], dst1, dstAddress\[.swizzle\], src0\[.select\_component\]</span></span> |
|--------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="c2c75-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="c2c75-106">Item</span></span>                                                                                                           | <span data-ttu-id="c2c75-107">Описание</span><span class="sxs-lookup"><span data-stu-id="c2c75-107">Description</span></span>                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2c75-108"><span id="dst0"></span><span id="DST0"></span>*dst0*</span><span class="sxs-lookup"><span data-stu-id="c2c75-108"><span id="dst0"></span><span id="DST0"></span>*dst0*</span></span><br/>                                                | <span data-ttu-id="c2c75-109">\[в \] содержит значение из *dst1* перед записью.</span><span class="sxs-lookup"><span data-stu-id="c2c75-109">\[in\] Contains the value from *dst1* before the write.</span></span><br/>                                                                |
| <span data-ttu-id="c2c75-110"><span id="dst1"></span><span id="DST1"></span>*dst1*</span><span class="sxs-lookup"><span data-stu-id="c2c75-110"><span id="dst1"></span><span id="DST1"></span>*dst1*</span></span><br/>                                                | <span data-ttu-id="c2c75-111">\[в \] представлении неупорядоченного доступа (UAV) (u \# ).</span><span class="sxs-lookup"><span data-stu-id="c2c75-111">\[in\] An unordered access view (UAV) (u\#).</span></span> <span data-ttu-id="c2c75-112">В шейдере вычислений это также может быть общей памятью группы потоков (g \# ).</span><span class="sxs-lookup"><span data-stu-id="c2c75-112">In the Compute Shader this can also be Thread Group Shared Memory (g\#).</span></span> <br/> |
| <span data-ttu-id="c2c75-113"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*дстаддресс*</span><span class="sxs-lookup"><span data-stu-id="c2c75-113"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*</span></span><br/> | <span data-ttu-id="c2c75-114">\[в \] адресе памяти.</span><span class="sxs-lookup"><span data-stu-id="c2c75-114">\[in\] The memory address.</span></span><br/>                                                                                             |
| <span data-ttu-id="c2c75-115"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="c2c75-115"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>                                                | <span data-ttu-id="c2c75-116">\[в \] значении, записываемом в *dst1* по адресу *дстаддресс*.</span><span class="sxs-lookup"><span data-stu-id="c2c75-116">\[in\] The value to write to *dst1* at *dstAddress*.</span></span><br/>                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="c2c75-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="c2c75-117">Remarks</span></span>

<span data-ttu-id="c2c75-118">Эта инструкция выполняет однокомпонентное 32-разрядное значение записи операнда *src0* в *dst1* с 32-бит на компонент, адрес *дстаддресс*.</span><span class="sxs-lookup"><span data-stu-id="c2c75-118">This instruction performs a single component 32-bit value write of operand *src0* to *dst1* at 32-bit per component address *dstAddress*.</span></span>

<span data-ttu-id="c2c75-119">Если *dst1* имеет тип u \# , то он мог быть объявлен как необработанный, типизированный или структурированный.</span><span class="sxs-lookup"><span data-stu-id="c2c75-119">If *dst1* is a u\#, it may have been declared as raw, typed or structured.</span></span> <span data-ttu-id="c2c75-120">При вводе он должен быть объявлен как UINT/Синт с форматом привязанного ресурса, R32 \_ uint/ \_ Синт.</span><span class="sxs-lookup"><span data-stu-id="c2c75-120">If typed, it must be declared as UINT/SINT with the bound resource format being R32\_UINT/\_SINT.</span></span>

<span data-ttu-id="c2c75-121">Если *dst1* имеет значение g \# , то его необходимо объявить как необработанный или структурированный.</span><span class="sxs-lookup"><span data-stu-id="c2c75-121">If *dst1* is g\#, it must be declared as raw or structured.</span></span>

<span data-ttu-id="c2c75-122">Количество компонентов, взятых из адреса, определяется размерностью ресурса, объявленного на *dst1*.</span><span class="sxs-lookup"><span data-stu-id="c2c75-122">The number of components taken from the address is determined by the dimensionality of the resource declared at *dst1*.</span></span>

<span data-ttu-id="c2c75-123">Исходное 32-битное значение в целевой памяти записывается в *dst0*.</span><span class="sxs-lookup"><span data-stu-id="c2c75-123">The original 32-bit value in the destination memory is written to *dst0*.</span></span>

<span data-ttu-id="c2c75-124">Вся операция выполняется атомарно.</span><span class="sxs-lookup"><span data-stu-id="c2c75-124">The entire operation is performed atomically.</span></span>

<span data-ttu-id="c2c75-125">Если вызов шейдера неактивен, например, если точка была удалена раньше при выполнении, или вызов в качестве вспомогательного метода к реальному пикселю или примеру для производных, эта инструкция не изменяет память *dst1* , а возвращаемое значение не определено.</span><span class="sxs-lookup"><span data-stu-id="c2c75-125">If the shader invocation is inactive, for example if the pixel has been discarded earlier in its execution, or a pixel/sample invocation only exists to serve as a helper to a real pixel/sample for derivatives, this instruction does not alter the *dst1* memory at all, and the returned value is undefined.</span></span>

<span data-ttu-id="c2c75-126">Исходящие адреса в u \# не записываются в память, за исключением случаев, когда u \# является структурированным, а смещение в байтах в структуре (второй компонент адреса) вызывает неограниченный доступ, а все содержимое UAV становится неопределенным.</span><span class="sxs-lookup"><span data-stu-id="c2c75-126">Out of bounds addressing on u\# causes nothing to be written to memory, except if the u\# is structured, and byte offset into the struct (second component of the address) is causing the out of bounds access, then the entire contents of the UAV become undefined.</span></span>

<span data-ttu-id="c2c75-127">Исходящие адреса в u \# или g \# вызывают неопределенный результат, возвращаемый шейдеру в *dst0*.</span><span class="sxs-lookup"><span data-stu-id="c2c75-127">Out of bounds addressing on u\# or g\# causes an undefined result to be returned to the shader in *dst0*.</span></span>

<span data-ttu-id="c2c75-128">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="c2c75-128">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="c2c75-129">Вершина</span><span class="sxs-lookup"><span data-stu-id="c2c75-129">Vertex</span></span> | <span data-ttu-id="c2c75-130">Поверхности</span><span class="sxs-lookup"><span data-stu-id="c2c75-130">Hull</span></span> | <span data-ttu-id="c2c75-131">Домен</span><span class="sxs-lookup"><span data-stu-id="c2c75-131">Domain</span></span> | <span data-ttu-id="c2c75-132">Геометрия</span><span class="sxs-lookup"><span data-stu-id="c2c75-132">Geometry</span></span> | <span data-ttu-id="c2c75-133">Пиксель</span><span class="sxs-lookup"><span data-stu-id="c2c75-133">Pixel</span></span> | <span data-ttu-id="c2c75-134">Вычисления</span><span class="sxs-lookup"><span data-stu-id="c2c75-134">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="c2c75-135">X</span><span class="sxs-lookup"><span data-stu-id="c2c75-135">X</span></span>     | <span data-ttu-id="c2c75-136">X</span><span class="sxs-lookup"><span data-stu-id="c2c75-136">X</span></span>       |



 

<span data-ttu-id="c2c75-137">Так как Уавс доступны на всех стадиях шейдера для Direct3D 11,1, эта инструкция применяется ко всем этапам шейдера для среды выполнения Direct3D 11,1, которая доступна начиная с Windows 8.</span><span class="sxs-lookup"><span data-stu-id="c2c75-137">Because UAVs are available at all shader stages for Direct3D 11.1, this instruction applies to all shader stages for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="c2c75-138">Вершина</span><span class="sxs-lookup"><span data-stu-id="c2c75-138">Vertex</span></span> | <span data-ttu-id="c2c75-139">Поверхности</span><span class="sxs-lookup"><span data-stu-id="c2c75-139">Hull</span></span> | <span data-ttu-id="c2c75-140">Домен</span><span class="sxs-lookup"><span data-stu-id="c2c75-140">Domain</span></span> | <span data-ttu-id="c2c75-141">Геометрия</span><span class="sxs-lookup"><span data-stu-id="c2c75-141">Geometry</span></span> | <span data-ttu-id="c2c75-142">Пиксель</span><span class="sxs-lookup"><span data-stu-id="c2c75-142">Pixel</span></span> | <span data-ttu-id="c2c75-143">Вычисления</span><span class="sxs-lookup"><span data-stu-id="c2c75-143">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="c2c75-144">X</span><span class="sxs-lookup"><span data-stu-id="c2c75-144">X</span></span>      | <span data-ttu-id="c2c75-145">X</span><span class="sxs-lookup"><span data-stu-id="c2c75-145">X</span></span>    | <span data-ttu-id="c2c75-146">X</span><span class="sxs-lookup"><span data-stu-id="c2c75-146">X</span></span>      | <span data-ttu-id="c2c75-147">X</span><span class="sxs-lookup"><span data-stu-id="c2c75-147">X</span></span>        | <span data-ttu-id="c2c75-148">X</span><span class="sxs-lookup"><span data-stu-id="c2c75-148">X</span></span>     | <span data-ttu-id="c2c75-149">X</span><span class="sxs-lookup"><span data-stu-id="c2c75-149">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="c2c75-150">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="c2c75-150">Minimum Shader Model</span></span>

<span data-ttu-id="c2c75-151">Эта инструкция поддерживается в следующих моделях шейдеров:</span><span class="sxs-lookup"><span data-stu-id="c2c75-151">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="c2c75-152">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="c2c75-152">Shader Model</span></span>                                              | <span data-ttu-id="c2c75-153">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="c2c75-153">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="c2c75-154">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="c2c75-154">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="c2c75-155">да</span><span class="sxs-lookup"><span data-stu-id="c2c75-155">yes</span></span>       |
| [<span data-ttu-id="c2c75-156">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="c2c75-156">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="c2c75-157">Нет</span><span class="sxs-lookup"><span data-stu-id="c2c75-157">no</span></span>        |
| [<span data-ttu-id="c2c75-158">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="c2c75-158">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="c2c75-159">Нет</span><span class="sxs-lookup"><span data-stu-id="c2c75-159">no</span></span>        |
| [<span data-ttu-id="c2c75-160">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c2c75-160">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="c2c75-161">Нет</span><span class="sxs-lookup"><span data-stu-id="c2c75-161">no</span></span>        |
| [<span data-ttu-id="c2c75-162">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c2c75-162">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="c2c75-163">Нет</span><span class="sxs-lookup"><span data-stu-id="c2c75-163">no</span></span>        |
| [<span data-ttu-id="c2c75-164">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c2c75-164">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="c2c75-165">Нет</span><span class="sxs-lookup"><span data-stu-id="c2c75-165">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="c2c75-166">См. также</span><span class="sxs-lookup"><span data-stu-id="c2c75-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c2c75-167">Сборка Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c2c75-167">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





