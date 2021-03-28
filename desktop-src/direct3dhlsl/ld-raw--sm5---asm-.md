---
title: ld_raw (SM5-ASM)
description: Чтение произвольного доступа с 1-4 32-разрядных компонентов из необработанного буфера.
ms.assetid: F7DBA80D-4DD5-4271-B571-24FB6188ABFE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd4a9480ef60098b394e0eff2b06043fd9a32e45
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104983860"
---
# <a name="ld_raw-sm5---asm"></a><span data-ttu-id="27238-103">LD \_ необработанных (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="27238-103">ld\_raw (sm5 - asm)</span></span>

<span data-ttu-id="27238-104">Чтение произвольного доступа с 1-4 32-разрядных компонентов из необработанного буфера.</span><span class="sxs-lookup"><span data-stu-id="27238-104">Random-access read of 1-4 32bit components from a raw buffer.</span></span>



| <span data-ttu-id="27238-105">LD \_ необработанных dst0 \[ . Mask \] , сркбитеоффсет \[ . Select \_ компонент \] , src0 \[ . свиззле\]</span><span class="sxs-lookup"><span data-stu-id="27238-105">ld\_raw dst0\[.mask\], srcByteOffset\[.select\_component\], src0\[.swizzle\]</span></span> |
|------------------------------------------------------------------------------|



 



| <span data-ttu-id="27238-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="27238-106">Item</span></span>                                                                                                                       | <span data-ttu-id="27238-107">Описание</span><span class="sxs-lookup"><span data-stu-id="27238-107">Description</span></span>                                                   |
|----------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="27238-108"><span id="dst0"></span><span id="DST0"></span>*dst0*</span><span class="sxs-lookup"><span data-stu-id="27238-108"><span id="dst0"></span><span id="DST0"></span>*dst0*</span></span><br/>                                                            | <span data-ttu-id="27238-109">\[в \] адресе результата операции.</span><span class="sxs-lookup"><span data-stu-id="27238-109">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="27238-110"><span id="srcByteOffset"></span><span id="srcbyteoffset"></span><span id="SRCBYTEOFFSET"></span>*сркбитеоффсет*</span><span class="sxs-lookup"><span data-stu-id="27238-110"><span id="srcByteOffset"></span><span id="srcbyteoffset"></span><span id="SRCBYTEOFFSET"></span>*srcByteOffset*</span></span><br/> | <span data-ttu-id="27238-111">\[в \] задает смещение для чтения.</span><span class="sxs-lookup"><span data-stu-id="27238-111">\[in\] Specifies the offset to read from.</span></span><br/>          |
| <span data-ttu-id="27238-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="27238-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>                                                            | <span data-ttu-id="27238-113">\[в \] компоненте для чтения.</span><span class="sxs-lookup"><span data-stu-id="27238-113">\[in\] The component to read.</span></span> <br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="27238-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="27238-114">Remarks</span></span>

<span data-ttu-id="27238-115">*src0* должен быть:</span><span class="sxs-lookup"><span data-stu-id="27238-115">*src0* must be:</span></span>

-   <span data-ttu-id="27238-116">Любой этап шейдера: SRV (t \# ) LD St</span><span class="sxs-lookup"><span data-stu-id="27238-116">Any shader stage: SRV (t\#)ld st</span></span>
-   <span data-ttu-id="27238-117">Вычисление шейдера или шейдера пикселей: UAV (u \# )</span><span class="sxs-lookup"><span data-stu-id="27238-117">Compute shader or pixel shader: UAV (u\#)</span></span>
-   <span data-ttu-id="27238-118">Шейдер вычислений: Общая память группы потоков (g \# )</span><span class="sxs-lookup"><span data-stu-id="27238-118">Compute shader: thread group shared memory (g\#)</span></span>

<span data-ttu-id="27238-119">*сркбитеоффсет* задает базовое 32-разрядное значение в памяти для окна из 4 последовательных 32-разрядных значений, в которых данные могут быть считаны, в зависимости от свиззле и маски на других параметрах.</span><span class="sxs-lookup"><span data-stu-id="27238-119">*srcByteOffset* specifies the base 32-bit value in memory for a window of 4 sequential 32-bit values in which data may be read, depending on the swizzle and mask on other parameters.</span></span>

<span data-ttu-id="27238-120">Данные, считанные из необработанного буфера, эквивалентны следующему псевдокоду: где у нас есть смещение, адрес, указатель на содержимое буфера, шаг источника и данные, хранимые линейно.</span><span class="sxs-lookup"><span data-stu-id="27238-120">The data read from the raw buffer is equivalent to the following pseudocode: where we have the offset, address, pointer to the buffer contents, stride of the source, and the data stored linearly.</span></span>

``` syntax
                    BYTE *BufferContents;         // from src0
                    UINT srcByteOffset;           // from srcRegister
                    BYTE *ReadLocation;           // value to calculate
                    ReadLocation = BufferContents 
                                + srcByteOffset;

                    UINT32 Temp[4];  // used to make code shorter

                    // apply the source resource swizzle on source data
                    Temp = read_and_swizzle(ReadLocation, srcSwizzle);

                    // write the components to the output based on mask
                    ApplyWriteMask(dstRegister, dstWriteMask, Temp);
```

<span data-ttu-id="27238-121">Недопустимые адреса в u \# /t для \# любого заданного 32-разрядного компонента возвращают 0 для этого компонента.</span><span class="sxs-lookup"><span data-stu-id="27238-121">Out of bounds addressing on u\#/t\# of any given 32-bit component returns 0 for that component.</span></span>

<span data-ttu-id="27238-122">Исходящие адреса в g \# (границы этого конкретного g \# , а не всю общую память) для любого заданного 32-разрядного компонента возвращают неопределенный результат.</span><span class="sxs-lookup"><span data-stu-id="27238-122">Out of bounds addressing on g\# (the bounds of that particular g\#, as opposed to all shared memory) for any given 32-bit component returns an undefined result.</span></span>

<span data-ttu-id="27238-123">CS \_ 4 \_ 0 и CS \_ 4 \_ 1 поддерживают эту инструкцию для UAV и SRV.</span><span class="sxs-lookup"><span data-stu-id="27238-123">cs\_4\_0 and cs\_4\_1 support this instruction for UAV and SRV.</span></span>

<span data-ttu-id="27238-124">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="27238-124">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="27238-125">Вершина</span><span class="sxs-lookup"><span data-stu-id="27238-125">Vertex</span></span> | <span data-ttu-id="27238-126">Поверхности</span><span class="sxs-lookup"><span data-stu-id="27238-126">Hull</span></span> | <span data-ttu-id="27238-127">Домен</span><span class="sxs-lookup"><span data-stu-id="27238-127">Domain</span></span> | <span data-ttu-id="27238-128">Геометрия</span><span class="sxs-lookup"><span data-stu-id="27238-128">Geometry</span></span> | <span data-ttu-id="27238-129">Пиксель</span><span class="sxs-lookup"><span data-stu-id="27238-129">Pixel</span></span> | <span data-ttu-id="27238-130">Вычисления</span><span class="sxs-lookup"><span data-stu-id="27238-130">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="27238-131">X</span><span class="sxs-lookup"><span data-stu-id="27238-131">X</span></span>      | <span data-ttu-id="27238-132">X</span><span class="sxs-lookup"><span data-stu-id="27238-132">X</span></span>    | <span data-ttu-id="27238-133">X</span><span class="sxs-lookup"><span data-stu-id="27238-133">X</span></span>      | <span data-ttu-id="27238-134">X</span><span class="sxs-lookup"><span data-stu-id="27238-134">X</span></span>        | <span data-ttu-id="27238-135">X</span><span class="sxs-lookup"><span data-stu-id="27238-135">X</span></span>     | <span data-ttu-id="27238-136">X</span><span class="sxs-lookup"><span data-stu-id="27238-136">X</span></span>       |



 

<span data-ttu-id="27238-137">Так как Уавс доступны на всех стадиях шейдера для Direct3D 11,1, эта инструкция применяется ко всем этапам шейдера для Уавс в среде выполнения Direct3D 11,1, которая доступна начиная с Windows 8.</span><span class="sxs-lookup"><span data-stu-id="27238-137">Because UAVs are available at all shader stages for Direct3D 11.1, this instruction applies to all shader stages for UAVs for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="27238-138">Вершина</span><span class="sxs-lookup"><span data-stu-id="27238-138">Vertex</span></span> | <span data-ttu-id="27238-139">Поверхности</span><span class="sxs-lookup"><span data-stu-id="27238-139">Hull</span></span> | <span data-ttu-id="27238-140">Домен</span><span class="sxs-lookup"><span data-stu-id="27238-140">Domain</span></span> | <span data-ttu-id="27238-141">Геометрия</span><span class="sxs-lookup"><span data-stu-id="27238-141">Geometry</span></span> | <span data-ttu-id="27238-142">Пиксель</span><span class="sxs-lookup"><span data-stu-id="27238-142">Pixel</span></span> | <span data-ttu-id="27238-143">Вычисления</span><span class="sxs-lookup"><span data-stu-id="27238-143">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="27238-144">X</span><span class="sxs-lookup"><span data-stu-id="27238-144">X</span></span>      | <span data-ttu-id="27238-145">X</span><span class="sxs-lookup"><span data-stu-id="27238-145">X</span></span>    | <span data-ttu-id="27238-146">X</span><span class="sxs-lookup"><span data-stu-id="27238-146">X</span></span>      | <span data-ttu-id="27238-147">X</span><span class="sxs-lookup"><span data-stu-id="27238-147">X</span></span>        | <span data-ttu-id="27238-148">X</span><span class="sxs-lookup"><span data-stu-id="27238-148">X</span></span>     | <span data-ttu-id="27238-149">X</span><span class="sxs-lookup"><span data-stu-id="27238-149">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="27238-150">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="27238-150">Minimum Shader Model</span></span>

<span data-ttu-id="27238-151">Эта инструкция поддерживается в следующих моделях шейдеров:</span><span class="sxs-lookup"><span data-stu-id="27238-151">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="27238-152">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="27238-152">Shader Model</span></span>                                              | <span data-ttu-id="27238-153">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="27238-153">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="27238-154">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="27238-154">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="27238-155">да</span><span class="sxs-lookup"><span data-stu-id="27238-155">yes</span></span>       |
| [<span data-ttu-id="27238-156">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="27238-156">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="27238-157">Нет</span><span class="sxs-lookup"><span data-stu-id="27238-157">no</span></span>        |
| [<span data-ttu-id="27238-158">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="27238-158">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="27238-159">Нет</span><span class="sxs-lookup"><span data-stu-id="27238-159">no</span></span>        |
| [<span data-ttu-id="27238-160">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="27238-160">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="27238-161">Нет</span><span class="sxs-lookup"><span data-stu-id="27238-161">no</span></span>        |
| [<span data-ttu-id="27238-162">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="27238-162">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="27238-163">Нет</span><span class="sxs-lookup"><span data-stu-id="27238-163">no</span></span>        |
| [<span data-ttu-id="27238-164">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="27238-164">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="27238-165">Нет</span><span class="sxs-lookup"><span data-stu-id="27238-165">no</span></span>        |



 

<span data-ttu-id="27238-166">CS \_ 4 \_ 0 и CS \_ 4 \_ 1 поддерживают эту инструкцию для UAV и SRV.</span><span class="sxs-lookup"><span data-stu-id="27238-166">cs\_4\_0 and cs\_4\_1 support this instruction for UAV and SRV.</span></span>

## <a name="related-topics"></a><span data-ttu-id="27238-167">См. также</span><span class="sxs-lookup"><span data-stu-id="27238-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="27238-168">Сборка Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="27238-168">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





