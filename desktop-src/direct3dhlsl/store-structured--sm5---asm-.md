---
title: store_structured (SM5-ASM)
description: Произвольный доступ для записи 1-4 32-разрядных компонентов в структурированный буфер неупорядоченного представления доступа (UAV).
ms.assetid: 8080B2CA-5BDA-4F01-8B2B-B85BDD58C5AF
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5890d30fac57923365f0bdea89fcce55f7922c7
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104069338"
---
# <a name="store_structured-sm5---asm"></a><span data-ttu-id="ff444-103">\_структурированное хранилище (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="ff444-103">store\_structured (sm5 - asm)</span></span>

<span data-ttu-id="ff444-104">Произвольный доступ для записи 1-4 32-разрядных компонентов в структурированный буфер неупорядоченного представления доступа (UAV).</span><span class="sxs-lookup"><span data-stu-id="ff444-104">Random-access write of 1-4 32-bit components into a structured buffer unordered access view (UAV).</span></span>



| <span data-ttu-id="ff444-105">хранение \_ структурированной dst0 \[ . запись \_ маски \] , дстаддресс \[ . Select \_ компонент \] , дстбитеоффсет \[ . Select \_ Component \] , src0 \[ . свиззле\]</span><span class="sxs-lookup"><span data-stu-id="ff444-105">store\_structured dst0\[.write\_mask\], dstAddress\[.select\_component\], dstByteOffset\[.select\_component\], src0\[.swizzle\]</span></span> |
|---------------------------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="ff444-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="ff444-106">Item</span></span>                                                                                                                       | <span data-ttu-id="ff444-107">Описание</span><span class="sxs-lookup"><span data-stu-id="ff444-107">Description</span></span>                                                    |
|----------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="ff444-108"><span id="dst0"></span><span id="DST0"></span>*dst0*</span><span class="sxs-lookup"><span data-stu-id="ff444-108"><span id="dst0"></span><span id="DST0"></span>*dst0*</span></span><br/>                                                            | <span data-ttu-id="ff444-109">\[в \] адресе результатов операции.</span><span class="sxs-lookup"><span data-stu-id="ff444-109">\[in\] The address of the results of the operation.</span></span><br/> |
| <span data-ttu-id="ff444-110"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*дстаддресс*</span><span class="sxs-lookup"><span data-stu-id="ff444-110"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*</span></span><br/>             | <span data-ttu-id="ff444-111">\[в \] адрес для записи.</span><span class="sxs-lookup"><span data-stu-id="ff444-111">\[in\] The address at which to write.</span></span><br/>               |
| <span data-ttu-id="ff444-112"><span id="dstByteOffset"></span><span id="dstbyteoffset"></span><span id="DSTBYTEOFFSET"></span>*дстбитеоффсет*</span><span class="sxs-lookup"><span data-stu-id="ff444-112"><span id="dstByteOffset"></span><span id="dstbyteoffset"></span><span id="DSTBYTEOFFSET"></span>*dstByteOffset*</span></span><br/> | <span data-ttu-id="ff444-113">\[в \] индексе структуры для записи.</span><span class="sxs-lookup"><span data-stu-id="ff444-113">\[in\] The index of the structure to write.</span></span><br/>         |
| <span data-ttu-id="ff444-114"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="ff444-114"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>                                                            | <span data-ttu-id="ff444-115">\[в \] компонентах для записи.</span><span class="sxs-lookup"><span data-stu-id="ff444-115">\[in\] The components to write.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="ff444-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="ff444-116">Remarks</span></span>

<span data-ttu-id="ff444-117">Эта инструкция выполняет 1-4 компонентов в 32-разрядных компонентах, \* записанных из *src0* в *dst0* по адресу в *дстаддресс* и *дстбитеоффсет*.</span><span class="sxs-lookup"><span data-stu-id="ff444-117">This instruction performs 1-4 component \*32bit components written from *src0* to *dst0* at the address in *dstAddress* and *dstByteOffset*.</span></span> <span data-ttu-id="ff444-118">Нет преобразования формата.</span><span class="sxs-lookup"><span data-stu-id="ff444-118">No format conversion.</span></span>

<span data-ttu-id="ff444-119">*dst0* должен быть UAV (u \# ).</span><span class="sxs-lookup"><span data-stu-id="ff444-119">*dst0* must be a UAV (u\#).</span></span> <span data-ttu-id="ff444-120">В шейдере вычислений он также может быть общей памятью группы потоков (g \# ).</span><span class="sxs-lookup"><span data-stu-id="ff444-120">In the compute shader it can also be thread group shared memory (g\#).</span></span>

<span data-ttu-id="ff444-121">*дстаддресс* указывает индекс структуры для записи.</span><span class="sxs-lookup"><span data-stu-id="ff444-121">*dstAddress* specifies the index of the structure to write.</span></span>

<span data-ttu-id="ff444-122">Расположение записанных данных эквивалентно следующему псевдокоду, который показывает смещение, адрес, указатель на содержимое буфера, шаг источника и данные, хранящиеся линейно.</span><span class="sxs-lookup"><span data-stu-id="ff444-122">The location of the data written is equivalent to the following pseudocode which shows the offset, address, pointer to the buffer contents, stride of the source, and the data stored linearly.</span></span>

``` syntax
                    BYTE *BufferContents;             // from dst0
                    UINT BufferStride;                // from dst0
                    UINT dstAddress, dstByteOffset;   // source registers
                    BYTE *WriteLocation;              // value to calculate

                    // calculate writing location
                     WriteLocation = BufferContents 
                                + BufferStride * dstAddress 
                                + dstByteOffset;

                    // calculate the number of components to write
                    switch (dstWriteMask)
                    {
                        x:    WriteComponents = 1; break;
                        xy:   WriteComponents = 2; break;
                        xyz:  WriteComponents = 3; break;
                        xyzw: WriteComponents = 4; break;
                        default:  // only these masks are valid                              
                    }

                    // copy the data from the source register with
                    //    the swizzle applied
                    memcpy(WriteLocation, swizzle(src0, src0.swizzle), 
                             WriteComponents * sizeof(INT32));
```

<span data-ttu-id="ff444-123">Этот псевдокод показывает, как функционирует операция, но фактические данные не должны храниться линейно.</span><span class="sxs-lookup"><span data-stu-id="ff444-123">This pseudocode shows how the operation functions, but the actual data does not have to be stored linearly.</span></span> <span data-ttu-id="ff444-124">Если данные не хранятся линейно, фактическая операция инструкции должна соответствовать поведению указанной выше операции.</span><span class="sxs-lookup"><span data-stu-id="ff444-124">If the data is not stored linearly, the actual operation of the instruction needs to match the behavior of the above operation.</span></span>

<span data-ttu-id="ff444-125">*dst0* может иметь только маску записи, которая является одной из следующих:. x,. XY,. XYZ,. ксизв.</span><span class="sxs-lookup"><span data-stu-id="ff444-125">*dst0* can only have a write mask that is one of the following: .x, .xy, .xyz, .xyzw.</span></span> <span data-ttu-id="ff444-126">Маска записи определяет число 32-разрядных компонентов, записываемых без пробелов.</span><span class="sxs-lookup"><span data-stu-id="ff444-126">The write mask determines the number of 32-bit components to write without gaps.</span></span>

<span data-ttu-id="ff444-127">Исходящие адреса в u \# касуед by *дстаддресс* означает, что ничего не записывается в память вне границ.</span><span class="sxs-lookup"><span data-stu-id="ff444-127">Out of bounds addressing on u\# casued by *dstAddress* means nothing is written to the out of bounds memory.</span></span>

<span data-ttu-id="ff444-128">Если *дстбитеоффсет*, в том числе *дствритемаск*, вызывает неограниченный доступ \# , все содержимое UAV становится неопределенным.</span><span class="sxs-lookup"><span data-stu-id="ff444-128">If the *dstByteOffset*, including *dstWriteMask*, is what causes out of bounds access to u\#, the entire contents of the UAV become undefined.</span></span>

<span data-ttu-id="ff444-129">Вне пределов на g \# (границы этого конкретного g \# , в отличие от всей общей памяти) для любого заданного 32-разрядного компонента приводят к тому, что все содержимое общей памяти становится неопределенным.</span><span class="sxs-lookup"><span data-stu-id="ff444-129">Out of bounds addressing on g\# (the bounds of that particular g\#, as opposed to all shared memory) for any given 32-bit component causes the entire contents of all shared memory to become undefined.</span></span>

<span data-ttu-id="ff444-130">*дстбитеоффсет* — это отдельный аргумент из *дстаддресс* , так как он обычно является литералом.</span><span class="sxs-lookup"><span data-stu-id="ff444-130">*dstByteOffset* is a separate argument from *dstAddress* because it is commonly a literal.</span></span> <span data-ttu-id="ff444-131">Это разделение параметров не было выполнено для атомарных действий в структурированной памяти.</span><span class="sxs-lookup"><span data-stu-id="ff444-131">This parameter separation has not been done for atomics on structured memory.</span></span>

<span data-ttu-id="ff444-132">CS \_ 4 \_ 0 и CS \_ 4 \_ 1 поддерживают эту инструкцию для UAV и тгсм.</span><span class="sxs-lookup"><span data-stu-id="ff444-132">cs\_4\_0 and cs\_4\_1 support this instruction for UAV and TGSM.</span></span>

<span data-ttu-id="ff444-133">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="ff444-133">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="ff444-134">Вершина</span><span class="sxs-lookup"><span data-stu-id="ff444-134">Vertex</span></span> | <span data-ttu-id="ff444-135">Поверхности</span><span class="sxs-lookup"><span data-stu-id="ff444-135">Hull</span></span> | <span data-ttu-id="ff444-136">Домен</span><span class="sxs-lookup"><span data-stu-id="ff444-136">Domain</span></span> | <span data-ttu-id="ff444-137">Геометрия</span><span class="sxs-lookup"><span data-stu-id="ff444-137">Geometry</span></span> | <span data-ttu-id="ff444-138">Пиксель</span><span class="sxs-lookup"><span data-stu-id="ff444-138">Pixel</span></span> | <span data-ttu-id="ff444-139">Вычисления</span><span class="sxs-lookup"><span data-stu-id="ff444-139">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="ff444-140">X</span><span class="sxs-lookup"><span data-stu-id="ff444-140">X</span></span>     | <span data-ttu-id="ff444-141">X</span><span class="sxs-lookup"><span data-stu-id="ff444-141">X</span></span>       |



 

<span data-ttu-id="ff444-142">Так как Уавс доступны на всех стадиях шейдера для Direct3D 11,1, эта инструкция применяется ко всем этапам шейдера для среды выполнения Direct3D 11,1, которая доступна начиная с Windows 8.</span><span class="sxs-lookup"><span data-stu-id="ff444-142">Because UAVs are available at all shader stages for Direct3D 11.1, this instruction applies to all shader stages for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="ff444-143">Вершина</span><span class="sxs-lookup"><span data-stu-id="ff444-143">Vertex</span></span> | <span data-ttu-id="ff444-144">Поверхности</span><span class="sxs-lookup"><span data-stu-id="ff444-144">Hull</span></span> | <span data-ttu-id="ff444-145">Домен</span><span class="sxs-lookup"><span data-stu-id="ff444-145">Domain</span></span> | <span data-ttu-id="ff444-146">Геометрия</span><span class="sxs-lookup"><span data-stu-id="ff444-146">Geometry</span></span> | <span data-ttu-id="ff444-147">Пиксель</span><span class="sxs-lookup"><span data-stu-id="ff444-147">Pixel</span></span> | <span data-ttu-id="ff444-148">Вычисления</span><span class="sxs-lookup"><span data-stu-id="ff444-148">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="ff444-149">X</span><span class="sxs-lookup"><span data-stu-id="ff444-149">X</span></span>      | <span data-ttu-id="ff444-150">X</span><span class="sxs-lookup"><span data-stu-id="ff444-150">X</span></span>    | <span data-ttu-id="ff444-151">X</span><span class="sxs-lookup"><span data-stu-id="ff444-151">X</span></span>      | <span data-ttu-id="ff444-152">X</span><span class="sxs-lookup"><span data-stu-id="ff444-152">X</span></span>        | <span data-ttu-id="ff444-153">X</span><span class="sxs-lookup"><span data-stu-id="ff444-153">X</span></span>     | <span data-ttu-id="ff444-154">X</span><span class="sxs-lookup"><span data-stu-id="ff444-154">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="ff444-155">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="ff444-155">Minimum Shader Model</span></span>

<span data-ttu-id="ff444-156">Эта инструкция поддерживается в следующих моделях шейдеров:</span><span class="sxs-lookup"><span data-stu-id="ff444-156">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="ff444-157">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="ff444-157">Shader Model</span></span>                                              | <span data-ttu-id="ff444-158">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="ff444-158">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="ff444-159">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="ff444-159">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="ff444-160">да</span><span class="sxs-lookup"><span data-stu-id="ff444-160">yes</span></span>       |
| [<span data-ttu-id="ff444-161">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="ff444-161">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="ff444-162">Нет</span><span class="sxs-lookup"><span data-stu-id="ff444-162">no</span></span>        |
| [<span data-ttu-id="ff444-163">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="ff444-163">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="ff444-164">Нет</span><span class="sxs-lookup"><span data-stu-id="ff444-164">no</span></span>        |
| [<span data-ttu-id="ff444-165">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ff444-165">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="ff444-166">Нет</span><span class="sxs-lookup"><span data-stu-id="ff444-166">no</span></span>        |
| [<span data-ttu-id="ff444-167">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ff444-167">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="ff444-168">Нет</span><span class="sxs-lookup"><span data-stu-id="ff444-168">no</span></span>        |
| [<span data-ttu-id="ff444-169">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ff444-169">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="ff444-170">Нет</span><span class="sxs-lookup"><span data-stu-id="ff444-170">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="ff444-171">См. также</span><span class="sxs-lookup"><span data-stu-id="ff444-171">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ff444-172">Сборка Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ff444-172">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





