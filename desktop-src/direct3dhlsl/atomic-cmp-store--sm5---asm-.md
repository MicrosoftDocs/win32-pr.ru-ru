---
title: atomic_cmp_store (SM5-ASM)
description: Атомарное сравнение и запись в память.
ms.assetid: 1B97E983-11A9-47E4-B274-E94083837C6E
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26a5292d65b32988017044a2ec52680848dffbef
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "103784977"
---
# <a name="atomic_cmp_store-sm5---asm"></a><span data-ttu-id="0bdab-103">атомарное \_ \_ хранилище CMP (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="0bdab-103">atomic\_cmp\_store (sm5 - asm)</span></span>

<span data-ttu-id="0bdab-104">Атомарное сравнение и запись в память.</span><span class="sxs-lookup"><span data-stu-id="0bdab-104">Atomic compare and write to memory.</span></span>



| <span data-ttu-id="0bdab-105">атомарное \_ \_ хранилище CMP, дстаддресс \[ . свиззле \] , src0 \[ . Select \_ \] , src1 \[ . Выбор \_ компонента\]</span><span class="sxs-lookup"><span data-stu-id="0bdab-105">atomic\_cmp\_store dst, dstAddress\[.swizzle\], src0\[.select\_component\], src1\[.select\_component\]</span></span> |
|--------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="0bdab-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="0bdab-106">Item</span></span>                                                                                                           | <span data-ttu-id="0bdab-107">Описание</span><span class="sxs-lookup"><span data-stu-id="0bdab-107">Description</span></span>                                                                                                                                                                               |
|----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0bdab-108"><span id="dst"></span><span id="DST"></span>*кон*</span><span class="sxs-lookup"><span data-stu-id="0bdab-108"><span id="dst"></span><span id="DST"></span>*dst*</span></span><br/>                                                   | <span data-ttu-id="0bdab-109">\[в \] компонентах, сравниваемых с *src0*.</span><span class="sxs-lookup"><span data-stu-id="0bdab-109">\[in\] The components to compare with *src0*.</span></span> <span data-ttu-id="0bdab-110">Это значение должно быть неупорядоченным представлением доступа (UAV) (u \# ).</span><span class="sxs-lookup"><span data-stu-id="0bdab-110">This value must be an unordered access view (UAV) (u\#).</span></span> <span data-ttu-id="0bdab-111">В шейдере вычислений он также может быть общей памятью группы потоков (g \# ).</span><span class="sxs-lookup"><span data-stu-id="0bdab-111">In the compute shader it can also be thread group shared memory (g\#).</span></span> <br/> |
| <span data-ttu-id="0bdab-112"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*дстаддресс*</span><span class="sxs-lookup"><span data-stu-id="0bdab-112"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*</span></span><br/> | <span data-ttu-id="0bdab-113">\[в \] адресе памяти.</span><span class="sxs-lookup"><span data-stu-id="0bdab-113">\[in\] The memory address.</span></span><br/>                                                                                                                                                     |
| <span data-ttu-id="0bdab-114"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="0bdab-114"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>                                                | <span data-ttu-id="0bdab-115">\[в \] 32-разрядном значении для сравнения с *DST*.</span><span class="sxs-lookup"><span data-stu-id="0bdab-115">\[in\] The 32-bit value to compare with *dst*.</span></span><br/>                                                                                                                                 |
| <span data-ttu-id="0bdab-116"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="0bdab-116"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/>                                                | <span data-ttu-id="0bdab-117">\[\]значение для записи в память, если сравниваемые значения идентичны.</span><span class="sxs-lookup"><span data-stu-id="0bdab-117">\[in\] The value to write to memory if the compared values are identical.</span></span> <br/>                                                                                                     |



 

## <a name="remarks"></a><span data-ttu-id="0bdab-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="0bdab-118">Remarks</span></span>

<span data-ttu-id="0bdab-119">Эта инструкция выполняет одно 32-разрядное значение одного компонента, сравнивая операнд *src0* с *DST* в 32-бит на компонент, адрес *дстаддресс*.</span><span class="sxs-lookup"><span data-stu-id="0bdab-119">This instruction performs a single component 32-bit value compare of operand *src0* with *dst* at 32-bit per component address *dstAddress*.</span></span>

<span data-ttu-id="0bdab-120">Если сравниваемые значения идентичны, то 32-разрядное значение одного компонента в *src1* записывается в целевую память.</span><span class="sxs-lookup"><span data-stu-id="0bdab-120">If the compared values are identical, the single-component 32-bit value in *src1* is written to destination memory.</span></span> <span data-ttu-id="0bdab-121">В противном случае назначение не изменяется.</span><span class="sxs-lookup"><span data-stu-id="0bdab-121">Otherwise, the destination is not changed.</span></span>

<span data-ttu-id="0bdab-122">Вся операция сравнения и записи выполняется атомарно.</span><span class="sxs-lookup"><span data-stu-id="0bdab-122">The entire compare and write operation is performed atomically.</span></span>

<span data-ttu-id="0bdab-123">Если *DST* имеет тип u \# , его можно объявить как необработанный, типизированный или структурированный.</span><span class="sxs-lookup"><span data-stu-id="0bdab-123">If *dst* is a u\#, it can be declared as raw, typed or structured.</span></span> <span data-ttu-id="0bdab-124">При вводе он должен быть объявлен как UINT/Синт с форматом привязанного ресурса, R32 \_ uint/ \_ Синт.</span><span class="sxs-lookup"><span data-stu-id="0bdab-124">If typed, it must be declared as UINT/SINT with the bound resource format being R32\_UINT/\_SINT.</span></span>

<span data-ttu-id="0bdab-125">Если *DST* имеет значение g \# , его необходимо объявить как необработанный или структурированный.</span><span class="sxs-lookup"><span data-stu-id="0bdab-125">If *dst* is g\#, it must be declared as raw or structured.</span></span>

<span data-ttu-id="0bdab-126">Количество компонентов, взятых из адреса, определяется размерностью летнего времени \# или g \# .</span><span class="sxs-lookup"><span data-stu-id="0bdab-126">The number of components taken from the address is determined by the dimensionality of dst u\# or g\#.</span></span>

<span data-ttu-id="0bdab-127">В шейдере ничего не возвращается.</span><span class="sxs-lookup"><span data-stu-id="0bdab-127">Nothing is returned to the shader.</span></span>

<span data-ttu-id="0bdab-128">Если вызов шейдера неактивен, например, если пиксел был удален раньше при выполнении, или инструкция пикселей или образца не изменяет память на *летнее* время (без предупреждения).</span><span class="sxs-lookup"><span data-stu-id="0bdab-128">If the shader invocation is inactive, for example if the pixel has been discarded earlier in its execution, or a pixel/sample instruction does not alter the *dst* memory at all (silently).</span></span>

<span data-ttu-id="0bdab-129">Исходящие адреса в u \# не записываются в память, за исключением случаев, когда u \# является структурированным, а смещение в байтах в структуре (второй компонент адреса) вызывает неограниченный доступ, а все содержимое UAV становится неопределенным.</span><span class="sxs-lookup"><span data-stu-id="0bdab-129">Out of bounds addressing on u\# causes nothing to be written to memory, except if the u\# is structured, and byte offset into the struct (second component of the address) is causing the out of bounds access, then the entire contents of the UAV become undefined.</span></span>

<span data-ttu-id="0bdab-130">Исходящие адреса в g \# (границы этого конкретного g \# , а не всю общую память) приводят к тому, что все содержимое всей общей памяти становится неопределенным.</span><span class="sxs-lookup"><span data-stu-id="0bdab-130">Out of bounds addressing on g\# (the bounds of that particular g\#, as opposed to all shared memory) causes the entire contents of all shared memory to become undefined.</span></span>

<span data-ttu-id="0bdab-131">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="0bdab-131">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="0bdab-132">Вершина</span><span class="sxs-lookup"><span data-stu-id="0bdab-132">Vertex</span></span> | <span data-ttu-id="0bdab-133">Поверхности</span><span class="sxs-lookup"><span data-stu-id="0bdab-133">Hull</span></span> | <span data-ttu-id="0bdab-134">Домен</span><span class="sxs-lookup"><span data-stu-id="0bdab-134">Domain</span></span> | <span data-ttu-id="0bdab-135">Геометрия</span><span class="sxs-lookup"><span data-stu-id="0bdab-135">Geometry</span></span> | <span data-ttu-id="0bdab-136">Пиксель</span><span class="sxs-lookup"><span data-stu-id="0bdab-136">Pixel</span></span> | <span data-ttu-id="0bdab-137">Вычисления</span><span class="sxs-lookup"><span data-stu-id="0bdab-137">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="0bdab-138">X</span><span class="sxs-lookup"><span data-stu-id="0bdab-138">X</span></span>     | <span data-ttu-id="0bdab-139">X</span><span class="sxs-lookup"><span data-stu-id="0bdab-139">X</span></span>       |



 

<span data-ttu-id="0bdab-140">Так как Уавс доступны на всех стадиях шейдера для Direct3D 11,1, эта инструкция применяется ко всем этапам шейдера для среды выполнения Direct3D 11,1, которая доступна начиная с Windows 8.</span><span class="sxs-lookup"><span data-stu-id="0bdab-140">Because UAVs are available at all shader stages for Direct3D 11.1, this instruction applies to all shader stages for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="0bdab-141">Вершина</span><span class="sxs-lookup"><span data-stu-id="0bdab-141">Vertex</span></span> | <span data-ttu-id="0bdab-142">Поверхности</span><span class="sxs-lookup"><span data-stu-id="0bdab-142">Hull</span></span> | <span data-ttu-id="0bdab-143">Домен</span><span class="sxs-lookup"><span data-stu-id="0bdab-143">Domain</span></span> | <span data-ttu-id="0bdab-144">Геометрия</span><span class="sxs-lookup"><span data-stu-id="0bdab-144">Geometry</span></span> | <span data-ttu-id="0bdab-145">Пиксель</span><span class="sxs-lookup"><span data-stu-id="0bdab-145">Pixel</span></span> | <span data-ttu-id="0bdab-146">Вычисления</span><span class="sxs-lookup"><span data-stu-id="0bdab-146">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="0bdab-147">X</span><span class="sxs-lookup"><span data-stu-id="0bdab-147">X</span></span>      | <span data-ttu-id="0bdab-148">X</span><span class="sxs-lookup"><span data-stu-id="0bdab-148">X</span></span>    | <span data-ttu-id="0bdab-149">X</span><span class="sxs-lookup"><span data-stu-id="0bdab-149">X</span></span>      | <span data-ttu-id="0bdab-150">X</span><span class="sxs-lookup"><span data-stu-id="0bdab-150">X</span></span>        | <span data-ttu-id="0bdab-151">X</span><span class="sxs-lookup"><span data-stu-id="0bdab-151">X</span></span>     | <span data-ttu-id="0bdab-152">X</span><span class="sxs-lookup"><span data-stu-id="0bdab-152">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="0bdab-153">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="0bdab-153">Minimum Shader Model</span></span>

<span data-ttu-id="0bdab-154">Эта инструкция поддерживается в следующих моделях шейдеров:</span><span class="sxs-lookup"><span data-stu-id="0bdab-154">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="0bdab-155">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="0bdab-155">Shader Model</span></span>                                              | <span data-ttu-id="0bdab-156">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="0bdab-156">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="0bdab-157">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="0bdab-157">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="0bdab-158">да</span><span class="sxs-lookup"><span data-stu-id="0bdab-158">yes</span></span>       |
| [<span data-ttu-id="0bdab-159">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="0bdab-159">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="0bdab-160">Нет</span><span class="sxs-lookup"><span data-stu-id="0bdab-160">no</span></span>        |
| [<span data-ttu-id="0bdab-161">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="0bdab-161">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="0bdab-162">Нет</span><span class="sxs-lookup"><span data-stu-id="0bdab-162">no</span></span>        |
| [<span data-ttu-id="0bdab-163">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0bdab-163">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="0bdab-164">Нет</span><span class="sxs-lookup"><span data-stu-id="0bdab-164">no</span></span>        |
| [<span data-ttu-id="0bdab-165">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0bdab-165">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="0bdab-166">Нет</span><span class="sxs-lookup"><span data-stu-id="0bdab-166">no</span></span>        |
| [<span data-ttu-id="0bdab-167">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0bdab-167">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="0bdab-168">Нет</span><span class="sxs-lookup"><span data-stu-id="0bdab-168">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="0bdab-169">См. также</span><span class="sxs-lookup"><span data-stu-id="0bdab-169">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0bdab-170">Сборка Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0bdab-170">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





