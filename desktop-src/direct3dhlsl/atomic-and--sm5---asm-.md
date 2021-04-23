---
title: atomic_and (SM5-ASM)
description: Атомарная операция и в память.
ms.assetid: 5FA731E0-7D18-4416-9579-FCA01FF5FC38
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ef21f2f9d49a05f1eeb828ee1ce54ad1f162d7a
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104983893"
---
# <a name="atomic_and-sm5---asm"></a><span data-ttu-id="4bf86-103">Atomic \_ и (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="4bf86-103">atomic\_and (sm5 - asm)</span></span>

<span data-ttu-id="4bf86-104">Атомарная операция и в память.</span><span class="sxs-lookup"><span data-stu-id="4bf86-104">Atomic bitwise AND to memory.</span></span>



| <span data-ttu-id="4bf86-105">атомарные \_ и DST, дстаддресс \[ . свиззле \] , src0 \[ . Select \_ Component\]</span><span class="sxs-lookup"><span data-stu-id="4bf86-105">atomic\_and dst, dstAddress\[.swizzle\], src0\[.select\_component\]</span></span> |
|---------------------------------------------------------------------|



 



| <span data-ttu-id="4bf86-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="4bf86-106">Item</span></span>                                                                                                           | <span data-ttu-id="4bf86-107">Описание</span><span class="sxs-lookup"><span data-stu-id="4bf86-107">Description</span></span>                                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4bf86-108"><span id="dst"></span><span id="DST"></span>*кон*</span><span class="sxs-lookup"><span data-stu-id="4bf86-108"><span id="dst"></span><span id="DST"></span>*dst*</span></span><br/>                                                   | <span data-ttu-id="4bf86-109">\[в \] компонентах и с *src0*.</span><span class="sxs-lookup"><span data-stu-id="4bf86-109">\[in\] The components to AND with *src0*.</span></span> <span data-ttu-id="4bf86-110">Это значение должно быть неупорядоченным представлением доступа (UAV) (u \# ).</span><span class="sxs-lookup"><span data-stu-id="4bf86-110">This value must be an unordered access view (UAV) (u\#).</span></span> <span data-ttu-id="4bf86-111">В шейдере вычислений он также может быть общей памятью группы потоков (g \# ).</span><span class="sxs-lookup"><span data-stu-id="4bf86-111">In the compute shader it can also be thread group shared memory (g\#).</span></span> <br/> |
| <span data-ttu-id="4bf86-112"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*дстаддресс*</span><span class="sxs-lookup"><span data-stu-id="4bf86-112"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*</span></span><br/> | <span data-ttu-id="4bf86-113">\[в \] адресе памяти.</span><span class="sxs-lookup"><span data-stu-id="4bf86-113">\[in\] The memory address.</span></span><br/>                                                                                                                                                 |
| <span data-ttu-id="4bf86-114"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="4bf86-114"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>                                                | <span data-ttu-id="4bf86-115">\[в \] компонентах и с *летнего времени*.</span><span class="sxs-lookup"><span data-stu-id="4bf86-115">\[in\] The components to AND with *dst*.</span></span><br/>                                                                                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="4bf86-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="4bf86-116">Remarks</span></span>

<span data-ttu-id="4bf86-117">Эта операция выполняет атомарную операцию с одним компонентом, 32-битным побитовым и операндом *src0* в *летнее* время в 32-бит на компонент, адрес *дстаддресс*.</span><span class="sxs-lookup"><span data-stu-id="4bf86-117">This operation performs a single component 32-bit bitwise AND of operand *src0* into *dst* at 32-bit per component address *dstAddress*, performed atomically.</span></span>

<span data-ttu-id="4bf86-118">Количество компонентов, взятых из адреса, определяется размерностью *летнего времени* \# или g \# .</span><span class="sxs-lookup"><span data-stu-id="4bf86-118">The number of components taken from the address is determined by the dimensionality of *dst* u\# or g\#.</span></span>

<span data-ttu-id="4bf86-119">Если *DST* имеет тип u \# , его можно объявить как необработанный, типизированный или структурированный.</span><span class="sxs-lookup"><span data-stu-id="4bf86-119">If *dst* is a u\#, it can be declared as raw, typed or structured.</span></span> <span data-ttu-id="4bf86-120">При вводе он должен быть объявлен как UINT/Синт с форматом привязанного ресурса, R32 \_ uint/ \_ Синт.</span><span class="sxs-lookup"><span data-stu-id="4bf86-120">If typed, it must be declared as UINT/SINT with the bound resource format being R32\_UINT/\_SINT.</span></span>

<span data-ttu-id="4bf86-121">Если *DST* имеет значение g \# , его необходимо объявить как необработанный или структурированный.</span><span class="sxs-lookup"><span data-stu-id="4bf86-121">If *dst* is g\#, it must be declared as raw or structured.</span></span>

<span data-ttu-id="4bf86-122">В шейдере ничего не возвращается.</span><span class="sxs-lookup"><span data-stu-id="4bf86-122">Nothing is returned to the shader.</span></span>

<span data-ttu-id="4bf86-123">Если вызов шейдера неактивен, например, если точка была удалена раньше при выполнении, или только один из них существует, чтобы служить вспомогательным классом для реального пикселя или примера для производных, эта инструкция не изменяет память *летнего времени* (без предупреждения).</span><span class="sxs-lookup"><span data-stu-id="4bf86-123">If the shader invocation is inactive, for example if the pixel has been discarded earlier in its execution, or a pixel/sample invocation only exists to serve as a helper to a real pixel/sample for derivatives, this instruction does not alter the *dst* memory at all (silently).</span></span>

<span data-ttu-id="4bf86-124">Исходящие адреса в u \# не записываются в память, за исключением случаев, когда u \# является структурированным, а смещение в байтах в структуре (второй компонент адреса) вызывает неограниченный доступ, а все содержимое UAV становится неопределенным.</span><span class="sxs-lookup"><span data-stu-id="4bf86-124">Out of bounds addressing on u\# causes nothing to be written to memory, except if the u\# is structured, and byte offset into the struct (second component of the address) is causing the out of bounds access, then the entire contents of the UAV become undefined.</span></span>

<span data-ttu-id="4bf86-125">Исходящие адреса в g \# (границы этого конкретного g \# , а не всю общую память) приводят к тому, что все содержимое всей общей памяти становится неопределенным.</span><span class="sxs-lookup"><span data-stu-id="4bf86-125">Out of bounds addressing on g\# (the bounds of that particular g\#, as opposed to all shared memory) causes the entire contents of all shared memory to become undefined.</span></span>

<span data-ttu-id="4bf86-126">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="4bf86-126">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="4bf86-127">Вершина</span><span class="sxs-lookup"><span data-stu-id="4bf86-127">Vertex</span></span> | <span data-ttu-id="4bf86-128">Поверхности</span><span class="sxs-lookup"><span data-stu-id="4bf86-128">Hull</span></span> | <span data-ttu-id="4bf86-129">Домен</span><span class="sxs-lookup"><span data-stu-id="4bf86-129">Domain</span></span> | <span data-ttu-id="4bf86-130">Геометрия</span><span class="sxs-lookup"><span data-stu-id="4bf86-130">Geometry</span></span> | <span data-ttu-id="4bf86-131">Пиксель</span><span class="sxs-lookup"><span data-stu-id="4bf86-131">Pixel</span></span> | <span data-ttu-id="4bf86-132">Вычисления</span><span class="sxs-lookup"><span data-stu-id="4bf86-132">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="4bf86-133">X</span><span class="sxs-lookup"><span data-stu-id="4bf86-133">X</span></span>     | <span data-ttu-id="4bf86-134">X</span><span class="sxs-lookup"><span data-stu-id="4bf86-134">X</span></span>       |



 

<span data-ttu-id="4bf86-135">Так как Уавс доступны на всех стадиях шейдера для Direct3D 11,1, эта инструкция применяется ко всем этапам шейдера для среды выполнения Direct3D 11,1, которая доступна начиная с Windows 8.</span><span class="sxs-lookup"><span data-stu-id="4bf86-135">Because UAVs are available at all shader stages for Direct3D 11.1, this instruction applies to all shader stages for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="4bf86-136">Вершина</span><span class="sxs-lookup"><span data-stu-id="4bf86-136">Vertex</span></span> | <span data-ttu-id="4bf86-137">Поверхности</span><span class="sxs-lookup"><span data-stu-id="4bf86-137">Hull</span></span> | <span data-ttu-id="4bf86-138">Домен</span><span class="sxs-lookup"><span data-stu-id="4bf86-138">Domain</span></span> | <span data-ttu-id="4bf86-139">Геометрия</span><span class="sxs-lookup"><span data-stu-id="4bf86-139">Geometry</span></span> | <span data-ttu-id="4bf86-140">Пиксель</span><span class="sxs-lookup"><span data-stu-id="4bf86-140">Pixel</span></span> | <span data-ttu-id="4bf86-141">Вычисления</span><span class="sxs-lookup"><span data-stu-id="4bf86-141">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="4bf86-142">X</span><span class="sxs-lookup"><span data-stu-id="4bf86-142">X</span></span>      | <span data-ttu-id="4bf86-143">X</span><span class="sxs-lookup"><span data-stu-id="4bf86-143">X</span></span>    | <span data-ttu-id="4bf86-144">X</span><span class="sxs-lookup"><span data-stu-id="4bf86-144">X</span></span>      | <span data-ttu-id="4bf86-145">X</span><span class="sxs-lookup"><span data-stu-id="4bf86-145">X</span></span>        | <span data-ttu-id="4bf86-146">X</span><span class="sxs-lookup"><span data-stu-id="4bf86-146">X</span></span>     | <span data-ttu-id="4bf86-147">X</span><span class="sxs-lookup"><span data-stu-id="4bf86-147">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="4bf86-148">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="4bf86-148">Minimum Shader Model</span></span>

<span data-ttu-id="4bf86-149">Эта инструкция поддерживается в следующих моделях шейдеров:</span><span class="sxs-lookup"><span data-stu-id="4bf86-149">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="4bf86-150">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="4bf86-150">Shader Model</span></span>                                              | <span data-ttu-id="4bf86-151">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="4bf86-151">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="4bf86-152">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="4bf86-152">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="4bf86-153">да</span><span class="sxs-lookup"><span data-stu-id="4bf86-153">yes</span></span>       |
| [<span data-ttu-id="4bf86-154">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="4bf86-154">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="4bf86-155">Нет</span><span class="sxs-lookup"><span data-stu-id="4bf86-155">no</span></span>        |
| [<span data-ttu-id="4bf86-156">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="4bf86-156">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="4bf86-157">Нет</span><span class="sxs-lookup"><span data-stu-id="4bf86-157">no</span></span>        |
| [<span data-ttu-id="4bf86-158">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4bf86-158">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="4bf86-159">Нет</span><span class="sxs-lookup"><span data-stu-id="4bf86-159">no</span></span>        |
| [<span data-ttu-id="4bf86-160">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4bf86-160">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="4bf86-161">Нет</span><span class="sxs-lookup"><span data-stu-id="4bf86-161">no</span></span>        |
| [<span data-ttu-id="4bf86-162">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4bf86-162">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="4bf86-163">Нет</span><span class="sxs-lookup"><span data-stu-id="4bf86-163">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="4bf86-164">См. также</span><span class="sxs-lookup"><span data-stu-id="4bf86-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4bf86-165">Сборка Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4bf86-165">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





