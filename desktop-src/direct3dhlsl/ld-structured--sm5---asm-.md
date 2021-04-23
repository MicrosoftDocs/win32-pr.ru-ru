---
title: ld_structured (SM5-ASM)
description: Чтение произвольного доступа с 1-4 32-разрядных компонентов из структурированного буфера.
ms.assetid: ED572B76-FF6C-405E-9110-4B12AD5E5AE6
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00a34bafdcfbe0658723dd83d62507e255ff4bfa
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104412197"
---
# <a name="ld_structured-sm5---asm"></a><span data-ttu-id="f4bab-103">LD \_ структурированная (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="f4bab-103">ld\_structured (sm5 - asm)</span></span>

<span data-ttu-id="f4bab-104">Чтение произвольного доступа с 1-4 32-разрядных компонентов из структурированного буфера.</span><span class="sxs-lookup"><span data-stu-id="f4bab-104">Random-access read of 1-4 32bit components from a structured buffer.</span></span>



| <span data-ttu-id="f4bab-105">: LD \_ Structured dst0 \[ . Mask \] , сркаддресс \[ . Select \_ , компонент \] сркбитеоффсет \[ . Select \_ \] , src0 \[ . свиззле\]</span><span class="sxs-lookup"><span data-stu-id="f4bab-105">: ld\_structured dst0\[.mask\], srcAddress\[.select\_component\], srcByteOffset\[.select\_component\], src0\[.swizzle\]</span></span> |
|-------------------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="f4bab-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="f4bab-106">Item</span></span>                                                                                                                       | <span data-ttu-id="f4bab-107">Описание</span><span class="sxs-lookup"><span data-stu-id="f4bab-107">Description</span></span>                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4bab-108"><span id="dst0"></span><span id="DST0"></span>*dst0*</span><span class="sxs-lookup"><span data-stu-id="f4bab-108"><span id="dst0"></span><span id="DST0"></span>*dst0*</span></span><br/>                                                            | <span data-ttu-id="f4bab-109">\[в \] адресе результатов операции.</span><span class="sxs-lookup"><span data-stu-id="f4bab-109">\[in\] The address of the results of the operation.</span></span><br/>                                                                                             |
| <span data-ttu-id="f4bab-110"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*сркаддресс*</span><span class="sxs-lookup"><span data-stu-id="f4bab-110"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span></span><br/>             | <span data-ttu-id="f4bab-111">\[в \] задает индекс структуры для чтения.</span><span class="sxs-lookup"><span data-stu-id="f4bab-111">\[in\] Specifies the index of the structure to read.</span></span><br/>                                                                                            |
| <span data-ttu-id="f4bab-112"><span id="srcByteOffset"></span><span id="srcbyteoffset"></span><span id="SRCBYTEOFFSET"></span>*сркбитеоффсет*</span><span class="sxs-lookup"><span data-stu-id="f4bab-112"><span id="srcByteOffset"></span><span id="srcbyteoffset"></span><span id="SRCBYTEOFFSET"></span>*srcByteOffset*</span></span><br/> | <span data-ttu-id="f4bab-113">\[в \] задает смещение в байтах в структуре, с которой начинается чтение.</span><span class="sxs-lookup"><span data-stu-id="f4bab-113">\[in\] Specifies the byte offset in the structure to start reading from.</span></span> <br/>                                                                       |
| <span data-ttu-id="f4bab-114"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="f4bab-114"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>                                                            | <span data-ttu-id="f4bab-115">Буфер, из которого производится чтение.</span><span class="sxs-lookup"><span data-stu-id="f4bab-115">The buffer to read from.</span></span> <span data-ttu-id="f4bab-116">Этот параметр должен быть SRV (t \# ), UAV (u \# ).</span><span class="sxs-lookup"><span data-stu-id="f4bab-116">This parameter must be a SRV (t\#), UAV (u\#).</span></span> <span data-ttu-id="f4bab-117">В шейдере вычислений он также может быть общей памятью группы потоков (g \# ).</span><span class="sxs-lookup"><span data-stu-id="f4bab-117">In the compute shader it can also be thread group shared memory (g\#).</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="f4bab-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="f4bab-118">Remarks</span></span>

<span data-ttu-id="f4bab-119">Данные, считанные из структуры, эквивалентны следующему псевдокоду: где у нас есть смещение, адрес, указатель на содержимое буфера, шаг источника и данные, хранимые линейно.</span><span class="sxs-lookup"><span data-stu-id="f4bab-119">The data read from the structure is equivalent to the following pseudocode: where we have the offset, address, pointer to the buffer contents, stride of the source, and the data stored linearly.</span></span>

``` syntax
                    BYTE *BufferContents;         // from SRV or UAV
                    UINT BufferStride;            // from base resource
                    UINT srcAddress, srcByteOffset;   // from source registers
                    BYTE *ReadLocation;           // value to calculate
                    ReadLocation = BufferContents 
                                + BufferStride * srcByteOffset
                                + srcOffset;

                    UINT32 Temp[4];  // used to make code shorter

                    // apply the source resource swizzle on source data
                    Temp = read_and_swizzle(ReadLocation, srcSwizzle);

                    // write the components to the output based on mask
                    ApplyWriteMask(dstRegister, dstWriteMask, Temp);
```

<span data-ttu-id="f4bab-120">Этот псевдокод показывает, как функционирует операция, но фактические данные не должны храниться линейно.</span><span class="sxs-lookup"><span data-stu-id="f4bab-120">This pseudocode shows how the operation functions, but the actual data does not have to be stored linearly.</span></span> <span data-ttu-id="f4bab-121">Если данные не хранятся линейно, фактическая операция инструкции должна соответствовать поведению указанной выше операции.</span><span class="sxs-lookup"><span data-stu-id="f4bab-121">If the data is not stored linearly, the actual operation of the instruction needs to match the behavior of the above operation.</span></span>

<span data-ttu-id="f4bab-122">\#Недопустимые значения для параметра u/t для \# всех заданных 32-разрядных компонентов возвращают 0 для этого компонента, за исключением случаев, когда *сркбитеоффсет* и свиззле — это то, что из-за неограниченного доступа к вашему пользователю \# /t \# , возвращаемое значение для всех компонентов не определено.</span><span class="sxs-lookup"><span data-stu-id="f4bab-122">Out of bounds addressing on u\#/t\# of any given 32-bit component returns 0 for that component, except if *srcByteOffset*, plus swizzle is what causes out of bounds access to u\#/t\#, the returned value for all component(s) is undefined.</span></span>

<span data-ttu-id="f4bab-123">Исходящие адреса в g \# (границы этого конкретного g \# , а не всю общую память) для любого заданного 32-разрядного компонента возвращают неопределенный результат.</span><span class="sxs-lookup"><span data-stu-id="f4bab-123">Out of bounds addressing on g\# (the bounds of that particular g\#, as opposed to all shared memory) for any given 32-bit component returns an undefined result.</span></span>

<span data-ttu-id="f4bab-124">*сркбитеоффсет* — это отдельный аргумент из *сркаддресс* , так как он обычно является литералом.</span><span class="sxs-lookup"><span data-stu-id="f4bab-124">*srcByteOffset* is a separate argument from *srcAddress* because it is commonly a literal.</span></span> <span data-ttu-id="f4bab-125">Это разделение параметров не было выполнено для атомарных действий в структурированной памяти.</span><span class="sxs-lookup"><span data-stu-id="f4bab-125">This parameter separation has not been done for atomics on structured memory.</span></span>

<span data-ttu-id="f4bab-126">CS \_ 4 \_ 0 и CS \_ 4 \_ 1 поддерживают эту инструкцию для UAV, SRV и тгсм.</span><span class="sxs-lookup"><span data-stu-id="f4bab-126">cs\_4\_0 and cs\_4\_1 support this instruction for UAV, SRV, and TGSM.</span></span>

<span data-ttu-id="f4bab-127">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="f4bab-127">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="f4bab-128">Вершина</span><span class="sxs-lookup"><span data-stu-id="f4bab-128">Vertex</span></span> | <span data-ttu-id="f4bab-129">Поверхности</span><span class="sxs-lookup"><span data-stu-id="f4bab-129">Hull</span></span> | <span data-ttu-id="f4bab-130">Домен</span><span class="sxs-lookup"><span data-stu-id="f4bab-130">Domain</span></span> | <span data-ttu-id="f4bab-131">Геометрия</span><span class="sxs-lookup"><span data-stu-id="f4bab-131">Geometry</span></span> | <span data-ttu-id="f4bab-132">Пиксель</span><span class="sxs-lookup"><span data-stu-id="f4bab-132">Pixel</span></span> | <span data-ttu-id="f4bab-133">Вычисления</span><span class="sxs-lookup"><span data-stu-id="f4bab-133">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="f4bab-134">X</span><span class="sxs-lookup"><span data-stu-id="f4bab-134">X</span></span>      | <span data-ttu-id="f4bab-135">X</span><span class="sxs-lookup"><span data-stu-id="f4bab-135">X</span></span>    | <span data-ttu-id="f4bab-136">X</span><span class="sxs-lookup"><span data-stu-id="f4bab-136">X</span></span>      | <span data-ttu-id="f4bab-137">X</span><span class="sxs-lookup"><span data-stu-id="f4bab-137">X</span></span>        | <span data-ttu-id="f4bab-138">X</span><span class="sxs-lookup"><span data-stu-id="f4bab-138">X</span></span>     | <span data-ttu-id="f4bab-139">X</span><span class="sxs-lookup"><span data-stu-id="f4bab-139">X</span></span>       |



 

<span data-ttu-id="f4bab-140">Так как Уавс доступны на всех стадиях шейдера для Direct3D 11,1, эта инструкция применяется ко всем этапам шейдера для Уавс в среде выполнения Direct3D 11,1, которая доступна начиная с Windows 8.</span><span class="sxs-lookup"><span data-stu-id="f4bab-140">Because UAVs are available at all shader stages for Direct3D 11.1, this instruction applies to all shader stages for UAVs for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="f4bab-141">Вершина</span><span class="sxs-lookup"><span data-stu-id="f4bab-141">Vertex</span></span> | <span data-ttu-id="f4bab-142">Поверхности</span><span class="sxs-lookup"><span data-stu-id="f4bab-142">Hull</span></span> | <span data-ttu-id="f4bab-143">Домен</span><span class="sxs-lookup"><span data-stu-id="f4bab-143">Domain</span></span> | <span data-ttu-id="f4bab-144">Геометрия</span><span class="sxs-lookup"><span data-stu-id="f4bab-144">Geometry</span></span> | <span data-ttu-id="f4bab-145">Пиксель</span><span class="sxs-lookup"><span data-stu-id="f4bab-145">Pixel</span></span> | <span data-ttu-id="f4bab-146">Вычисления</span><span class="sxs-lookup"><span data-stu-id="f4bab-146">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="f4bab-147">X</span><span class="sxs-lookup"><span data-stu-id="f4bab-147">X</span></span>      | <span data-ttu-id="f4bab-148">X</span><span class="sxs-lookup"><span data-stu-id="f4bab-148">X</span></span>    | <span data-ttu-id="f4bab-149">X</span><span class="sxs-lookup"><span data-stu-id="f4bab-149">X</span></span>      | <span data-ttu-id="f4bab-150">X</span><span class="sxs-lookup"><span data-stu-id="f4bab-150">X</span></span>        | <span data-ttu-id="f4bab-151">X</span><span class="sxs-lookup"><span data-stu-id="f4bab-151">X</span></span>     | <span data-ttu-id="f4bab-152">X</span><span class="sxs-lookup"><span data-stu-id="f4bab-152">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="f4bab-153">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="f4bab-153">Minimum Shader Model</span></span>

<span data-ttu-id="f4bab-154">Эта инструкция поддерживается в следующих моделях шейдеров:</span><span class="sxs-lookup"><span data-stu-id="f4bab-154">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="f4bab-155">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="f4bab-155">Shader Model</span></span>                                              | <span data-ttu-id="f4bab-156">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="f4bab-156">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="f4bab-157">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="f4bab-157">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="f4bab-158">да</span><span class="sxs-lookup"><span data-stu-id="f4bab-158">yes</span></span>       |
| [<span data-ttu-id="f4bab-159">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="f4bab-159">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="f4bab-160">Нет</span><span class="sxs-lookup"><span data-stu-id="f4bab-160">no</span></span>        |
| [<span data-ttu-id="f4bab-161">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="f4bab-161">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="f4bab-162">Нет</span><span class="sxs-lookup"><span data-stu-id="f4bab-162">no</span></span>        |
| [<span data-ttu-id="f4bab-163">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f4bab-163">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="f4bab-164">Нет</span><span class="sxs-lookup"><span data-stu-id="f4bab-164">no</span></span>        |
| [<span data-ttu-id="f4bab-165">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f4bab-165">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="f4bab-166">Нет</span><span class="sxs-lookup"><span data-stu-id="f4bab-166">no</span></span>        |
| [<span data-ttu-id="f4bab-167">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f4bab-167">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="f4bab-168">Нет</span><span class="sxs-lookup"><span data-stu-id="f4bab-168">no</span></span>        |



 

<span data-ttu-id="f4bab-169">CS \_ 4 \_ 0 и CS \_ 4 \_ 1 поддерживают эту инструкцию для UAV, SRV и тгсм.</span><span class="sxs-lookup"><span data-stu-id="f4bab-169">cs\_4\_0 and cs\_4\_1 support this instruction for UAV, SRV and TGSM.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f4bab-170">См. также</span><span class="sxs-lookup"><span data-stu-id="f4bab-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f4bab-171">Сборка Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f4bab-171">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





