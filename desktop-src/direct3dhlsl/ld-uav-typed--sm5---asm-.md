---
title: ld_uav_typed (SM5-ASM)
description: Чтение произвольного доступа к элементу из типизированного представления неупорядоченного доступа (UAV).
ms.assetid: E5E03311-3596-4497-9271-FE6445DBFC62
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61b22392c802378c094b443c8ff2f2282909bd1f
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104335536"
---
# <a name="ld_uav_typed-sm5---asm"></a><span data-ttu-id="2fd79-103">LD \_ UAV \_ типизированный (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="2fd79-103">ld\_uav\_typed (sm5 - asm)</span></span>

<span data-ttu-id="2fd79-104">Чтение произвольного доступа к элементу из типизированного представления неупорядоченного доступа (UAV).</span><span class="sxs-lookup"><span data-stu-id="2fd79-104">Random-access read of an element from a typed unordered access view (UAV).</span></span>



| <span data-ttu-id="2fd79-105">LD \_ UAV \_ типизированный dst0 \[ . Mask \] , сркаддресс \[ . свиззле \] , сркуав \[ . свиззле\]</span><span class="sxs-lookup"><span data-stu-id="2fd79-105">ld\_uav\_typed dst0\[.mask\], srcAddress\[.swizzle\], srcUAV\[.swizzle\]</span></span> |
|--------------------------------------------------------------------------|



 



| <span data-ttu-id="2fd79-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="2fd79-106">Item</span></span>                                                                                                           | <span data-ttu-id="2fd79-107">Описание</span><span class="sxs-lookup"><span data-stu-id="2fd79-107">Description</span></span>                                                    |
|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="2fd79-108"><span id="dst0"></span><span id="DST0"></span>*dst0*</span><span class="sxs-lookup"><span data-stu-id="2fd79-108"><span id="dst0"></span><span id="DST0"></span>*dst0*</span></span><br/>                                                | <span data-ttu-id="2fd79-109">\[в \] адресе результатов операции.</span><span class="sxs-lookup"><span data-stu-id="2fd79-109">\[in\] The address of the results of the operation.</span></span><br/> |
| <span data-ttu-id="2fd79-110"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*сркаддресс*</span><span class="sxs-lookup"><span data-stu-id="2fd79-110"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span></span><br/> | <span data-ttu-id="2fd79-111">\[в поле \] указывает адрес для чтения.</span><span class="sxs-lookup"><span data-stu-id="2fd79-111">\[in\] Specifies the address to read from.</span></span><br/>          |
| <span data-ttu-id="2fd79-112"><span id="srcUAV"></span><span id="srcuav"></span><span id="SRCUAV"></span>*сркуав*</span><span class="sxs-lookup"><span data-stu-id="2fd79-112"><span id="srcUAV"></span><span id="srcuav"></span><span id="SRCUAV"></span>*srcUAV*</span></span><br/>                 | <span data-ttu-id="2fd79-113">\[в \] источнике, из которого производится чтение.</span><span class="sxs-lookup"><span data-stu-id="2fd79-113">\[in\] The source to read from.</span></span> <br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="2fd79-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="2fd79-114">Remarks</span></span>

<span data-ttu-id="2fd79-115">Эта инструкция выполняет 4-компонентный элемент, считанный из *сркуав* на неподписанном целочисленном адресе в *сркаддресс*, который преобразуется в 32-разрядный на каждый компонент в зависимости от формата, а затем записывается в *dst0* в шейдере.</span><span class="sxs-lookup"><span data-stu-id="2fd79-115">This instruction performs a 4-component element read from *srcUAV* at the unsigned integer address in *srcAddress*, converted to 32bit per component based on the format, then written to *dst0* in the shader.</span></span>

<span data-ttu-id="2fd79-116">*сркуав* — это UAV (u \# ), объявленный как типизированный.</span><span class="sxs-lookup"><span data-stu-id="2fd79-116">*srcUAV* is a UAV (u\#) declared as typed.</span></span> <span data-ttu-id="2fd79-117">Однако тип привязанного ресурса должен быть R32 \_ uint/Синт/float.</span><span class="sxs-lookup"><span data-stu-id="2fd79-117">However, the type of the bound resource must be R32\_UINT/SINT/FLOAT.</span></span>

<span data-ttu-id="2fd79-118">Число 32-разрядных беззнаковых целых чисел, полученных из адреса, определяется размерностью ресурса, объявленного на *сркуав*.</span><span class="sxs-lookup"><span data-stu-id="2fd79-118">The number of 32-bit unsigned integer components taken from the address are determined by the dimensionality of the resource declared at *srcUAV*.</span></span> <span data-ttu-id="2fd79-119">Адресация совпадает с инструкцией [LD](ld--sm4---asm-.md) .</span><span class="sxs-lookup"><span data-stu-id="2fd79-119">Addressing is the same as the [ld](ld--sm4---asm-.md) instruction.</span></span>

<span data-ttu-id="2fd79-120">Адресация вне границ совпадает с инструкцией **LD** .</span><span class="sxs-lookup"><span data-stu-id="2fd79-120">Out of bounds addressing is the same as the **ld** instruction.</span></span>

<span data-ttu-id="2fd79-121">Поведение этой инструкции идентично инструкции **LD** , если она вызывается как **LD dst0 \[ . Mask \] , сркаддресс \[ . свиззле \] , сркуав \[ . свиззле \]**</span><span class="sxs-lookup"><span data-stu-id="2fd79-121">The behavior of this instruction is identical to the **ld** instruction if called as **ld dst0\[.mask\], srcAddress\[.swizzle\], srcUAV\[.swizzle\]**</span></span>

<span data-ttu-id="2fd79-122">Он недопустим и не определен, чтобы использовать эту инструкцию для UAV, который не объявлен как типизированный.</span><span class="sxs-lookup"><span data-stu-id="2fd79-122">It is invalid and undefined to use this instruction on a UAV that is not declared as typed.</span></span> <span data-ttu-id="2fd79-123">Это действие для структурированного или нетипизированного UAV является недопустимым.</span><span class="sxs-lookup"><span data-stu-id="2fd79-123">Doing this on a structured or typeless UAV is invalid.</span></span>

<span data-ttu-id="2fd79-124">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="2fd79-124">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="2fd79-125">Вершина</span><span class="sxs-lookup"><span data-stu-id="2fd79-125">Vertex</span></span> | <span data-ttu-id="2fd79-126">Поверхности</span><span class="sxs-lookup"><span data-stu-id="2fd79-126">Hull</span></span> | <span data-ttu-id="2fd79-127">Домен</span><span class="sxs-lookup"><span data-stu-id="2fd79-127">Domain</span></span> | <span data-ttu-id="2fd79-128">Геометрия</span><span class="sxs-lookup"><span data-stu-id="2fd79-128">Geometry</span></span> | <span data-ttu-id="2fd79-129">Пиксель</span><span class="sxs-lookup"><span data-stu-id="2fd79-129">Pixel</span></span> | <span data-ttu-id="2fd79-130">Вычисления</span><span class="sxs-lookup"><span data-stu-id="2fd79-130">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="2fd79-131">X</span><span class="sxs-lookup"><span data-stu-id="2fd79-131">X</span></span>     | <span data-ttu-id="2fd79-132">X</span><span class="sxs-lookup"><span data-stu-id="2fd79-132">X</span></span>       |



 

<span data-ttu-id="2fd79-133">Так как Уавс доступны на всех стадиях шейдера для Direct3D 11,1, эта инструкция применяется ко всем этапам шейдера для среды выполнения Direct3D 11,1, которая доступна начиная с Windows 8.</span><span class="sxs-lookup"><span data-stu-id="2fd79-133">Because UAVs are available at all shader stages for Direct3D 11.1, this instruction applies to all shader stages for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="2fd79-134">Вершина</span><span class="sxs-lookup"><span data-stu-id="2fd79-134">Vertex</span></span> | <span data-ttu-id="2fd79-135">Поверхности</span><span class="sxs-lookup"><span data-stu-id="2fd79-135">Hull</span></span> | <span data-ttu-id="2fd79-136">Домен</span><span class="sxs-lookup"><span data-stu-id="2fd79-136">Domain</span></span> | <span data-ttu-id="2fd79-137">Геометрия</span><span class="sxs-lookup"><span data-stu-id="2fd79-137">Geometry</span></span> | <span data-ttu-id="2fd79-138">Пиксель</span><span class="sxs-lookup"><span data-stu-id="2fd79-138">Pixel</span></span> | <span data-ttu-id="2fd79-139">Вычисления</span><span class="sxs-lookup"><span data-stu-id="2fd79-139">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="2fd79-140">X</span><span class="sxs-lookup"><span data-stu-id="2fd79-140">X</span></span>      | <span data-ttu-id="2fd79-141">X</span><span class="sxs-lookup"><span data-stu-id="2fd79-141">X</span></span>    | <span data-ttu-id="2fd79-142">X</span><span class="sxs-lookup"><span data-stu-id="2fd79-142">X</span></span>      | <span data-ttu-id="2fd79-143">X</span><span class="sxs-lookup"><span data-stu-id="2fd79-143">X</span></span>        | <span data-ttu-id="2fd79-144">X</span><span class="sxs-lookup"><span data-stu-id="2fd79-144">X</span></span>     | <span data-ttu-id="2fd79-145">X</span><span class="sxs-lookup"><span data-stu-id="2fd79-145">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="2fd79-146">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="2fd79-146">Minimum Shader Model</span></span>

<span data-ttu-id="2fd79-147">Эта инструкция поддерживается в следующих моделях шейдеров:</span><span class="sxs-lookup"><span data-stu-id="2fd79-147">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="2fd79-148">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="2fd79-148">Shader Model</span></span>                                              | <span data-ttu-id="2fd79-149">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="2fd79-149">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="2fd79-150">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="2fd79-150">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="2fd79-151">да</span><span class="sxs-lookup"><span data-stu-id="2fd79-151">yes</span></span>       |
| [<span data-ttu-id="2fd79-152">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="2fd79-152">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="2fd79-153">Нет</span><span class="sxs-lookup"><span data-stu-id="2fd79-153">no</span></span>        |
| [<span data-ttu-id="2fd79-154">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="2fd79-154">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="2fd79-155">Нет</span><span class="sxs-lookup"><span data-stu-id="2fd79-155">no</span></span>        |
| [<span data-ttu-id="2fd79-156">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2fd79-156">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="2fd79-157">Нет</span><span class="sxs-lookup"><span data-stu-id="2fd79-157">no</span></span>        |
| [<span data-ttu-id="2fd79-158">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2fd79-158">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="2fd79-159">Нет</span><span class="sxs-lookup"><span data-stu-id="2fd79-159">no</span></span>        |
| [<span data-ttu-id="2fd79-160">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2fd79-160">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="2fd79-161">Нет</span><span class="sxs-lookup"><span data-stu-id="2fd79-161">no</span></span>        |



 

<span data-ttu-id="2fd79-162">CS \_ 4 \_ 0 и CS \_ 4 \_ 1 поддерживают эту инструкцию для UAV, SRV и тгсм.</span><span class="sxs-lookup"><span data-stu-id="2fd79-162">cs\_4\_0 and cs\_4\_1 support this instruction for UAV, SRV and TGSM.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2fd79-163">См. также</span><span class="sxs-lookup"><span data-stu-id="2fd79-163">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2fd79-164">Сборка Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2fd79-164">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





