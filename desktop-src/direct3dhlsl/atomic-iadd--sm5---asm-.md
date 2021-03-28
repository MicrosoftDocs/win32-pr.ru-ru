---
title: atomic_iadd (SM5-ASM)
description: Атомарное целое число добавляет в память.
ms.assetid: 093C7FA5-41BF-4BDD-A35D-1AACE8CB9B5C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6a8652d4e29aae9f32a84f7a4e4d477abd54b7c
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104335603"
---
# <a name="atomic_iadd-sm5---asm"></a><span data-ttu-id="1aefc-103">Атомарный \_ IAdd (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="1aefc-103">atomic\_iadd (sm5 - asm)</span></span>

<span data-ttu-id="1aefc-104">Атомарное целое число добавляет в память.</span><span class="sxs-lookup"><span data-stu-id="1aefc-104">Atomic integer add to memory.</span></span>



| <span data-ttu-id="1aefc-105">Атомарный \_ IAdd DST, дстаддресс \[ . свиззле \] , src0 \[ . Select \_ компонент\]</span><span class="sxs-lookup"><span data-stu-id="1aefc-105">atomic\_iadd dst, dstAddress\[.swizzle\], src0\[.select\_component\]</span></span> |
|----------------------------------------------------------------------|



 



| <span data-ttu-id="1aefc-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="1aefc-106">Item</span></span>                                                                                                           | <span data-ttu-id="1aefc-107">Описание</span><span class="sxs-lookup"><span data-stu-id="1aefc-107">Description</span></span>                                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1aefc-108"><span id="dst"></span><span id="DST"></span>*кон*</span><span class="sxs-lookup"><span data-stu-id="1aefc-108"><span id="dst"></span><span id="DST"></span>*dst*</span></span><br/>                                                   | <span data-ttu-id="1aefc-109">\[в \] компонентах, добавляемых с помощью *src0*.</span><span class="sxs-lookup"><span data-stu-id="1aefc-109">\[in\] The components to add with *src0*.</span></span> <span data-ttu-id="1aefc-110">Это значение должно быть неупорядоченным представлением доступа (UAV) (u \# ).</span><span class="sxs-lookup"><span data-stu-id="1aefc-110">This value must be an unordered access view (UAV) (u\#).</span></span> <span data-ttu-id="1aefc-111">В шейдере вычислений он также может быть общей памятью группы потоков (g \# ).</span><span class="sxs-lookup"><span data-stu-id="1aefc-111">In the compute shader it can also be thread group shared memory (g\#).</span></span> <br/> |
| <span data-ttu-id="1aefc-112"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*дстаддресс*</span><span class="sxs-lookup"><span data-stu-id="1aefc-112"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*</span></span><br/> | <span data-ttu-id="1aefc-113">\[в \] адресе памяти.</span><span class="sxs-lookup"><span data-stu-id="1aefc-113">\[in\] The memory address.</span></span><br/>                                                                                                                                                 |
| <span data-ttu-id="1aefc-114"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="1aefc-114"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>                                                | <span data-ttu-id="1aefc-115">\[в \] компонентах, добавляемых в *летнее* время.</span><span class="sxs-lookup"><span data-stu-id="1aefc-115">\[in\] The components to add to *dst*.</span></span><br/>                                                                                                                                     |



 

## <a name="remarks"></a><span data-ttu-id="1aefc-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="1aefc-116">Remarks</span></span>

<span data-ttu-id="1aefc-117">Эта инструкция выполняет атомарную операцию с одним компонентом, 32-разрядным целым числом, добавляемым в *src0* в течение *летнего времени* в 32-бит на компонент, адрес *дстаддресс*.</span><span class="sxs-lookup"><span data-stu-id="1aefc-117">This instruction performs a single component 32-bit integer add of operand *src0* into *dst* at 32-bit per component address *dstAddress*, performed atomically.</span></span> <span data-ttu-id="1aefc-118">Эта инструкция не зависит от знака.</span><span class="sxs-lookup"><span data-stu-id="1aefc-118">This instruction is insensitive to sign.</span></span>

<span data-ttu-id="1aefc-119">Количество компонентов, взятых из адреса, определяется размерностью *летнего времени* \# или g \# .</span><span class="sxs-lookup"><span data-stu-id="1aefc-119">The number of components taken from the address is determined by the dimensionality of *dst* u\# or g\#.</span></span>

<span data-ttu-id="1aefc-120">Если *DST* имеет тип u \# , его можно объявить как необработанный, типизированный или структурированный.</span><span class="sxs-lookup"><span data-stu-id="1aefc-120">If *dst* is a u\#, it can be declared as raw, typed or structured.</span></span> <span data-ttu-id="1aefc-121">При вводе он должен быть объявлен как UINT/Синт с форматом привязанного ресурса, R32 \_ uint/ \_ Синт.</span><span class="sxs-lookup"><span data-stu-id="1aefc-121">If typed, it must be declared as UINT/SINT with the bound resource format being R32\_UINT/\_SINT.</span></span>

<span data-ttu-id="1aefc-122">Если *DST* имеет значение g \# , его необходимо объявить как необработанный или структурированный.</span><span class="sxs-lookup"><span data-stu-id="1aefc-122">If *dst* is g\#, it must be declared as raw or structured.</span></span>

<span data-ttu-id="1aefc-123">В шейдере ничего не возвращается.</span><span class="sxs-lookup"><span data-stu-id="1aefc-123">Nothing is returned to the shader.</span></span>

<span data-ttu-id="1aefc-124">Если вызов шейдера неактивен, например, если точка была удалена раньше при выполнении или если обнаружено попиксельное или примерное обращение только в качестве вспомогательного метода к реальному пикселу или примеру для производных, эта инструкция не изменяет память на *летнее* время (без предупреждения).</span><span class="sxs-lookup"><span data-stu-id="1aefc-124">If the shader invocation is inactive, for example if the pixel has been discarded earlier in its execution, or if a pixel/sample invocation only exists to serve as a helper to a real pixel/sample for derivatives, this instruction does not alter the *dst* memory at all (silently).</span></span>

<span data-ttu-id="1aefc-125">Исходящие адреса в u \# не записываются в память, за исключением случаев, когда u \# является структурированным, а смещение в байтах в структуре (второй компонент адреса) вызывает неограниченный доступ, а все содержимое UAV становится неопределенным.</span><span class="sxs-lookup"><span data-stu-id="1aefc-125">Out of bounds addressing on u\# causes nothing to be written to memory, except if the u\# is structured, and byte offset into the struct (second component of the address) is causing the out of bounds access, then the entire contents of the UAV become undefined.</span></span>

<span data-ttu-id="1aefc-126">Исходящие адреса в g \# (границы этого конкретного g \# , а не всю общую память) приводят к тому, что все содержимое всей общей памяти становится неопределенным.</span><span class="sxs-lookup"><span data-stu-id="1aefc-126">Out of bounds addressing on g\# (the bounds of that particular g\#, as opposed to all shared memory) causes the entire contents of all shared memory to become undefined.</span></span>

<span data-ttu-id="1aefc-127">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="1aefc-127">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="1aefc-128">Вершина</span><span class="sxs-lookup"><span data-stu-id="1aefc-128">Vertex</span></span> | <span data-ttu-id="1aefc-129">Поверхности</span><span class="sxs-lookup"><span data-stu-id="1aefc-129">Hull</span></span> | <span data-ttu-id="1aefc-130">Домен</span><span class="sxs-lookup"><span data-stu-id="1aefc-130">Domain</span></span> | <span data-ttu-id="1aefc-131">Геометрия</span><span class="sxs-lookup"><span data-stu-id="1aefc-131">Geometry</span></span> | <span data-ttu-id="1aefc-132">Пиксель</span><span class="sxs-lookup"><span data-stu-id="1aefc-132">Pixel</span></span> | <span data-ttu-id="1aefc-133">Вычисления</span><span class="sxs-lookup"><span data-stu-id="1aefc-133">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="1aefc-134">X</span><span class="sxs-lookup"><span data-stu-id="1aefc-134">X</span></span>     | <span data-ttu-id="1aefc-135">X</span><span class="sxs-lookup"><span data-stu-id="1aefc-135">X</span></span>       |



 

<span data-ttu-id="1aefc-136">Так как Уавс доступны на всех стадиях шейдера для Direct3D 11,1, эта инструкция применяется ко всем этапам шейдера для среды выполнения Direct3D 11,1, которая доступна начиная с Windows 8.</span><span class="sxs-lookup"><span data-stu-id="1aefc-136">Because UAVs are available at all shader stages for Direct3D 11.1, this instruction applies to all shader stages for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="1aefc-137">Вершина</span><span class="sxs-lookup"><span data-stu-id="1aefc-137">Vertex</span></span> | <span data-ttu-id="1aefc-138">Поверхности</span><span class="sxs-lookup"><span data-stu-id="1aefc-138">Hull</span></span> | <span data-ttu-id="1aefc-139">Домен</span><span class="sxs-lookup"><span data-stu-id="1aefc-139">Domain</span></span> | <span data-ttu-id="1aefc-140">Геометрия</span><span class="sxs-lookup"><span data-stu-id="1aefc-140">Geometry</span></span> | <span data-ttu-id="1aefc-141">Пиксель</span><span class="sxs-lookup"><span data-stu-id="1aefc-141">Pixel</span></span> | <span data-ttu-id="1aefc-142">Вычисления</span><span class="sxs-lookup"><span data-stu-id="1aefc-142">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="1aefc-143">X</span><span class="sxs-lookup"><span data-stu-id="1aefc-143">X</span></span>      | <span data-ttu-id="1aefc-144">X</span><span class="sxs-lookup"><span data-stu-id="1aefc-144">X</span></span>    | <span data-ttu-id="1aefc-145">X</span><span class="sxs-lookup"><span data-stu-id="1aefc-145">X</span></span>      | <span data-ttu-id="1aefc-146">X</span><span class="sxs-lookup"><span data-stu-id="1aefc-146">X</span></span>        | <span data-ttu-id="1aefc-147">X</span><span class="sxs-lookup"><span data-stu-id="1aefc-147">X</span></span>     | <span data-ttu-id="1aefc-148">X</span><span class="sxs-lookup"><span data-stu-id="1aefc-148">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="1aefc-149">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="1aefc-149">Minimum Shader Model</span></span>

<span data-ttu-id="1aefc-150">Эта инструкция поддерживается в следующих моделях шейдеров:</span><span class="sxs-lookup"><span data-stu-id="1aefc-150">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="1aefc-151">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="1aefc-151">Shader Model</span></span>                                              | <span data-ttu-id="1aefc-152">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="1aefc-152">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="1aefc-153">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="1aefc-153">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="1aefc-154">да</span><span class="sxs-lookup"><span data-stu-id="1aefc-154">yes</span></span>       |
| [<span data-ttu-id="1aefc-155">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="1aefc-155">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="1aefc-156">Нет</span><span class="sxs-lookup"><span data-stu-id="1aefc-156">no</span></span>        |
| [<span data-ttu-id="1aefc-157">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="1aefc-157">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="1aefc-158">Нет</span><span class="sxs-lookup"><span data-stu-id="1aefc-158">no</span></span>        |
| [<span data-ttu-id="1aefc-159">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1aefc-159">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="1aefc-160">Нет</span><span class="sxs-lookup"><span data-stu-id="1aefc-160">no</span></span>        |
| [<span data-ttu-id="1aefc-161">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1aefc-161">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="1aefc-162">Нет</span><span class="sxs-lookup"><span data-stu-id="1aefc-162">no</span></span>        |
| [<span data-ttu-id="1aefc-163">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1aefc-163">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="1aefc-164">Нет</span><span class="sxs-lookup"><span data-stu-id="1aefc-164">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="1aefc-165">См. также</span><span class="sxs-lookup"><span data-stu-id="1aefc-165">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1aefc-166">Сборка Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1aefc-166">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





