---
title: store_raw (SM5-ASM)
description: Произвольная запись в 1-4 32-разрядных компонентов в память с нетипизированным типом.
ms.assetid: D166116A-CF4E-4020-9F6A-F9CEEFCDAB21
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c44b4d22a576853fb8b7d2c43fcb6a2d7fc9a448
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104412223"
---
# <a name="store_raw-sm5---asm"></a><span data-ttu-id="c3758-103">хранилище \_ RAW (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="c3758-103">store\_raw (sm5 - asm)</span></span>

<span data-ttu-id="c3758-104">Произвольная запись в 1-4 32-разрядных компонентов в память с нетипизированным типом.</span><span class="sxs-lookup"><span data-stu-id="c3758-104">Random-access write of 1-4 32bit components into typeless memory.</span></span>



| <span data-ttu-id="c3758-105">Сохранить \_ необработанный dst0 \[ . \_ Mask \] , дстбитеоффсет \[ . Select \_ Component \] , src0 \[ . свиззле\]</span><span class="sxs-lookup"><span data-stu-id="c3758-105">store\_raw dst0\[.write\_mask\], dstByteOffset\[.select\_component\], src0\[.swizzle\]</span></span> |
|----------------------------------------------------------------------------------------|



 



| <span data-ttu-id="c3758-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="c3758-106">Item</span></span>                                                                                                                       | <span data-ttu-id="c3758-107">Описание</span><span class="sxs-lookup"><span data-stu-id="c3758-107">Description</span></span>                                |
|----------------------------------------------------------------------------------------------------------------------------|--------------------------------------------|
| <span data-ttu-id="c3758-108"><span id="dst0"></span><span id="DST0"></span>*dst0*</span><span class="sxs-lookup"><span data-stu-id="c3758-108"><span id="dst0"></span><span id="DST0"></span>*dst0*</span></span><br/>                                                            | <span data-ttu-id="c3758-109">\[в \] адресе памяти.</span><span class="sxs-lookup"><span data-stu-id="c3758-109">\[in\] The memory address.</span></span><br/>      |
| <span data-ttu-id="c3758-110"><span id="dstByteOffset"></span><span id="dstbyteoffset"></span><span id="DSTBYTEOFFSET"></span>*дстбитеоффсет*</span><span class="sxs-lookup"><span data-stu-id="c3758-110"><span id="dstByteOffset"></span><span id="dstbyteoffset"></span><span id="DSTBYTEOFFSET"></span>*dstByteOffset*</span></span><br/> | <span data-ttu-id="c3758-111">\[в \] смещении.</span><span class="sxs-lookup"><span data-stu-id="c3758-111">\[in\] The offset.</span></span><br/>              |
| <span data-ttu-id="c3758-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="c3758-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>                                                            | <span data-ttu-id="c3758-113">\[в \] компонентах для записи.</span><span class="sxs-lookup"><span data-stu-id="c3758-113">\[in\] The components to write.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c3758-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="c3758-114">Remarks</span></span>

<span data-ttu-id="c3758-115">Эта инструкция выполняет 1-4 компонентов \* 32-bit, записанных из *src0* в *dst0* со смещением в *дстбитеоффсет*.</span><span class="sxs-lookup"><span data-stu-id="c3758-115">This instruction performs 1-4 component \*32-bit components written from *src0* to *dst0* at the offset in *dstByteOffset*.</span></span> <span data-ttu-id="c3758-116">Преобразование формата отсутствует.</span><span class="sxs-lookup"><span data-stu-id="c3758-116">There is no format conversion.</span></span>

<span data-ttu-id="c3758-117">*dst0* должен быть UAV (u \# ) или в шейдере вычислений он также может быть общей памятью группы потоков (g \# ).</span><span class="sxs-lookup"><span data-stu-id="c3758-117">*dst0* must be a UAV (u\#), or in the compute shader it can also be thread group shared memory (g\#).</span></span>

<span data-ttu-id="c3758-118">*дстбитеоффсет* задает базовое 32-разрядное значение в памяти для окна из 4 последовательных 32-разрядных значений, в которых могут записываться данные, в зависимости от свиззле и маски на других параметрах.</span><span class="sxs-lookup"><span data-stu-id="c3758-118">*dstByteOffset* specifies the base 32-bit value in memory for a window of 4 sequential 32-bit values in which data may be written, depending on the swizzle and mask on other parameters.</span></span>

<span data-ttu-id="c3758-119">Расположение записанных данных эквивалентно следующему псевдокоду, который показывает адрес, указатель на содержимое буфера и данные, хранимые линейно.</span><span class="sxs-lookup"><span data-stu-id="c3758-119">The location of the data written is equivalent to the following pseudocode which show the address, pointer to the buffer contents, and the data stored linearly.</span></span>

``` syntax
                    BYTE *BufferContents;          // from src0
                    UINT dstByteOffset;            // source register
                    BYTE *WriteLocation;           // value to calculate

                    // calculate writing location
                    WriteLocation = BufferContents 
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
                             WriteComponents * sizeof(UINT32));
```

<span data-ttu-id="c3758-120">Этот псевдокод показывает, как функционирует операция, но фактические данные не должны храниться линейно.</span><span class="sxs-lookup"><span data-stu-id="c3758-120">This pseudocode shows how the operation functions, but the actual data does not have to be stored linearly.</span></span> <span data-ttu-id="c3758-121">*dst0* может иметь только маску записи, которая является одной из следующих:. x,. XY,. XYZ,. ксизв.</span><span class="sxs-lookup"><span data-stu-id="c3758-121">*dst0* can only have a write mask that is one of the following: .x, .xy, .xyz, .xyzw.</span></span> <span data-ttu-id="c3758-122">Маска записи определяет число 32-разрядных компонентов для записи без зазоров.</span><span class="sxs-lookup"><span data-stu-id="c3758-122">The write mask determines the number of 32bit components to write without gaps.</span></span>

<span data-ttu-id="c3758-123">Исходящие адреса в u \# означает, что ничего не записывается в память вне границ; любая часть, находящиеся в границах, записывается правильно.</span><span class="sxs-lookup"><span data-stu-id="c3758-123">Out of bounds addressing on u\# means nothing is written to the out of bounds memory; any part that is in bounds is written correctly.</span></span>

<span data-ttu-id="c3758-124">Вне пределов на g \# (границы этого конкретного g \# , в отличие от всей общей памяти) для любого заданного 32-разрядного компонента приводят к тому, что все содержимое общей памяти становится неопределенным.</span><span class="sxs-lookup"><span data-stu-id="c3758-124">Out of bounds addressing on g\# (the bounds of that particular g\#, as opposed to all shared memory) for any given 32-bit component causes the entire contents of all shared memory to become undefined.</span></span>

<span data-ttu-id="c3758-125">CS \_ 4 \_ 0 и CS \_ 4 \_ 1 поддерживают эту инструкцию для UAV.</span><span class="sxs-lookup"><span data-stu-id="c3758-125">cs\_4\_0 and cs\_4\_1 support this instruction for UAV.</span></span>

<span data-ttu-id="c3758-126">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="c3758-126">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="c3758-127">Вершина</span><span class="sxs-lookup"><span data-stu-id="c3758-127">Vertex</span></span> | <span data-ttu-id="c3758-128">Поверхности</span><span class="sxs-lookup"><span data-stu-id="c3758-128">Hull</span></span> | <span data-ttu-id="c3758-129">Домен</span><span class="sxs-lookup"><span data-stu-id="c3758-129">Domain</span></span> | <span data-ttu-id="c3758-130">Геометрия</span><span class="sxs-lookup"><span data-stu-id="c3758-130">Geometry</span></span> | <span data-ttu-id="c3758-131">Пиксель</span><span class="sxs-lookup"><span data-stu-id="c3758-131">Pixel</span></span> | <span data-ttu-id="c3758-132">Вычисления</span><span class="sxs-lookup"><span data-stu-id="c3758-132">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="c3758-133">X</span><span class="sxs-lookup"><span data-stu-id="c3758-133">X</span></span>     | <span data-ttu-id="c3758-134">X</span><span class="sxs-lookup"><span data-stu-id="c3758-134">X</span></span>       |



 

<span data-ttu-id="c3758-135">Так как Уавс доступны на всех стадиях шейдера для Direct3D 11,1, эта инструкция применяется ко всем этапам шейдера для среды выполнения Direct3D 11,1, которая доступна начиная с Windows 8.</span><span class="sxs-lookup"><span data-stu-id="c3758-135">Because UAVs are available at all shader stages for Direct3D 11.1, this instruction applies to all shader stages for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="c3758-136">Вершина</span><span class="sxs-lookup"><span data-stu-id="c3758-136">Vertex</span></span> | <span data-ttu-id="c3758-137">Поверхности</span><span class="sxs-lookup"><span data-stu-id="c3758-137">Hull</span></span> | <span data-ttu-id="c3758-138">Домен</span><span class="sxs-lookup"><span data-stu-id="c3758-138">Domain</span></span> | <span data-ttu-id="c3758-139">Геометрия</span><span class="sxs-lookup"><span data-stu-id="c3758-139">Geometry</span></span> | <span data-ttu-id="c3758-140">Пиксель</span><span class="sxs-lookup"><span data-stu-id="c3758-140">Pixel</span></span> | <span data-ttu-id="c3758-141">Вычисления</span><span class="sxs-lookup"><span data-stu-id="c3758-141">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="c3758-142">X</span><span class="sxs-lookup"><span data-stu-id="c3758-142">X</span></span>      | <span data-ttu-id="c3758-143">X</span><span class="sxs-lookup"><span data-stu-id="c3758-143">X</span></span>    | <span data-ttu-id="c3758-144">X</span><span class="sxs-lookup"><span data-stu-id="c3758-144">X</span></span>      | <span data-ttu-id="c3758-145">X</span><span class="sxs-lookup"><span data-stu-id="c3758-145">X</span></span>        | <span data-ttu-id="c3758-146">X</span><span class="sxs-lookup"><span data-stu-id="c3758-146">X</span></span>     | <span data-ttu-id="c3758-147">X</span><span class="sxs-lookup"><span data-stu-id="c3758-147">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="c3758-148">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="c3758-148">Minimum Shader Model</span></span>

<span data-ttu-id="c3758-149">Эта инструкция поддерживается в следующих моделях шейдеров:</span><span class="sxs-lookup"><span data-stu-id="c3758-149">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="c3758-150">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="c3758-150">Shader Model</span></span>                                              | <span data-ttu-id="c3758-151">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="c3758-151">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="c3758-152">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="c3758-152">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="c3758-153">да</span><span class="sxs-lookup"><span data-stu-id="c3758-153">yes</span></span>       |
| [<span data-ttu-id="c3758-154">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="c3758-154">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="c3758-155">Нет</span><span class="sxs-lookup"><span data-stu-id="c3758-155">no</span></span>        |
| [<span data-ttu-id="c3758-156">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="c3758-156">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="c3758-157">Нет</span><span class="sxs-lookup"><span data-stu-id="c3758-157">no</span></span>        |
| [<span data-ttu-id="c3758-158">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c3758-158">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="c3758-159">Нет</span><span class="sxs-lookup"><span data-stu-id="c3758-159">no</span></span>        |
| [<span data-ttu-id="c3758-160">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c3758-160">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="c3758-161">Нет</span><span class="sxs-lookup"><span data-stu-id="c3758-161">no</span></span>        |
| [<span data-ttu-id="c3758-162">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c3758-162">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="c3758-163">Нет</span><span class="sxs-lookup"><span data-stu-id="c3758-163">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="c3758-164">См. также</span><span class="sxs-lookup"><span data-stu-id="c3758-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c3758-165">Сборка Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c3758-165">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





