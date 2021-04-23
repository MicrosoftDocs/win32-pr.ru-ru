---
title: store_uav_typed (SM5-ASM)
description: Произвольный доступ к записи элемента в типизированном представлении неупорядоченного доступа (UAV).
ms.assetid: AD8E035B-DACD-4241-A05B-7D6DC8E3222C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6243e6fbb2092bac699dbbce04cb3c3478880866
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104069334"
---
# <a name="store_uav_typed-sm5---asm"></a><span data-ttu-id="aa5d5-103">хранить \_ UAV в \_ типизированном виде (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="aa5d5-103">store\_uav\_typed (sm5 - asm)</span></span>

<span data-ttu-id="aa5d5-104">Произвольный доступ к записи элемента в типизированном представлении неупорядоченного доступа (UAV).</span><span class="sxs-lookup"><span data-stu-id="aa5d5-104">Random-access write of an element into a typed unordered access view (UAV).</span></span>



| <span data-ttu-id="aa5d5-105">Store \_ UAV \_ Typed дстуав. Ксизв, дстаддресс \[ . свиззле \] , src0 \[ . свиззле\]</span><span class="sxs-lookup"><span data-stu-id="aa5d5-105">store\_uav\_typed dstUAV.xyzw, dstAddress\[.swizzle\], src0\[.swizzle\]</span></span> |
|-------------------------------------------------------------------------|



 



| <span data-ttu-id="aa5d5-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="aa5d5-106">Item</span></span>                                                                                                           | <span data-ttu-id="aa5d5-107">Описание</span><span class="sxs-lookup"><span data-stu-id="aa5d5-107">Description</span></span>                                             |
|----------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="aa5d5-108"><span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*дстуав*</span><span class="sxs-lookup"><span data-stu-id="aa5d5-108"><span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*dstUAV*</span></span><br/>                 | <span data-ttu-id="aa5d5-109">\[в \] содержит результат операции.</span><span class="sxs-lookup"><span data-stu-id="aa5d5-109">\[in\] Contains the result of the operation.</span></span><br/> |
| <span data-ttu-id="aa5d5-110"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*дстаддресс*</span><span class="sxs-lookup"><span data-stu-id="aa5d5-110"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*</span></span><br/> | <span data-ttu-id="aa5d5-111">\[в \] адрес для записи.</span><span class="sxs-lookup"><span data-stu-id="aa5d5-111">\[in\] The address at which to write.</span></span><br/>        |
| <span data-ttu-id="aa5d5-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="aa5d5-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>                                                | <span data-ttu-id="aa5d5-113">\[в \] компонентах для записи.</span><span class="sxs-lookup"><span data-stu-id="aa5d5-113">\[in\] The components to write.</span></span><br/>              |



 

## <a name="remarks"></a><span data-ttu-id="aa5d5-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="aa5d5-114">Remarks</span></span>

<span data-ttu-id="aa5d5-115">Эта инструкция выполняет 4 \* -разрядный элемент 32, записанный из *Src0* в *дстуав* по адресу в *дстаддресс*.</span><span class="sxs-lookup"><span data-stu-id="aa5d5-115">This instruction performs a 4 component \*32-bit element written from *src0* to *dstUAV* at the address in *dstAddress*.</span></span> <span data-ttu-id="aa5d5-116">*дстуав* — это типизированный UAV (u \# ).</span><span class="sxs-lookup"><span data-stu-id="aa5d5-116">*dstUAV* is a typed UAV (u\#).</span></span>

<span data-ttu-id="aa5d5-117">Формат UAV определяет преобразование формата.</span><span class="sxs-lookup"><span data-stu-id="aa5d5-117">The format of the UAV determines format conversion.</span></span>

<span data-ttu-id="aa5d5-118">Число 32-разрядных беззнаковых целых чисел, полученных из адреса, определяется размерностью ресурса, объявленного на *дстуав*.</span><span class="sxs-lookup"><span data-stu-id="aa5d5-118">The number of 32-bit unsigned integer components taken from the address are determined by the dimensionality of the resource declared at *dstUAV*.</span></span> <span data-ttu-id="aa5d5-119">Этот адрес находится в элементах.</span><span class="sxs-lookup"><span data-stu-id="aa5d5-119">This address is in elements.</span></span>

<span data-ttu-id="aa5d5-120">Для адресации вне границ означает, что в память ничего не записывается.</span><span class="sxs-lookup"><span data-stu-id="aa5d5-120">Out of bounds addressing means nothing gets written to memory.</span></span>

<span data-ttu-id="aa5d5-121">*дстуав* всегда имеет маску записи. ксизв.</span><span class="sxs-lookup"><span data-stu-id="aa5d5-121">*dstUAV* always has a .xyzw write mask.</span></span> <span data-ttu-id="aa5d5-122">Все компоненты должны быть записаны.</span><span class="sxs-lookup"><span data-stu-id="aa5d5-122">All components must be written.</span></span>

<span data-ttu-id="aa5d5-123">Он недопустим и не определен, чтобы использовать эту инструкцию для UAV, который не объявлен как типизированный.</span><span class="sxs-lookup"><span data-stu-id="aa5d5-123">It is invalid and undefined to use this instruction on a UAV that is not declared as typed.</span></span> <span data-ttu-id="aa5d5-124">Это значит, что выполнение этого действия в структурированном или нетипизированном UAV недопустимо.</span><span class="sxs-lookup"><span data-stu-id="aa5d5-124">That is, doing this on a structured or typeless UAV is invalid.</span></span>

<span data-ttu-id="aa5d5-125">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="aa5d5-125">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="aa5d5-126">Вершина</span><span class="sxs-lookup"><span data-stu-id="aa5d5-126">Vertex</span></span> | <span data-ttu-id="aa5d5-127">Поверхности</span><span class="sxs-lookup"><span data-stu-id="aa5d5-127">Hull</span></span> | <span data-ttu-id="aa5d5-128">Домен</span><span class="sxs-lookup"><span data-stu-id="aa5d5-128">Domain</span></span> | <span data-ttu-id="aa5d5-129">Геометрия</span><span class="sxs-lookup"><span data-stu-id="aa5d5-129">Geometry</span></span> | <span data-ttu-id="aa5d5-130">Пиксель</span><span class="sxs-lookup"><span data-stu-id="aa5d5-130">Pixel</span></span> | <span data-ttu-id="aa5d5-131">Вычисления</span><span class="sxs-lookup"><span data-stu-id="aa5d5-131">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="aa5d5-132">X</span><span class="sxs-lookup"><span data-stu-id="aa5d5-132">X</span></span>     | <span data-ttu-id="aa5d5-133">X</span><span class="sxs-lookup"><span data-stu-id="aa5d5-133">X</span></span>       |



 

<span data-ttu-id="aa5d5-134">Так как Уавс доступны на всех стадиях шейдера для Direct3D 11,1, эта инструкция применяется ко всем этапам шейдера для среды выполнения Direct3D 11,1, которая доступна начиная с Windows 8.</span><span class="sxs-lookup"><span data-stu-id="aa5d5-134">Because UAVs are available at all shader stages for Direct3D 11.1, this instruction applies to all shader stages for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="aa5d5-135">Вершина</span><span class="sxs-lookup"><span data-stu-id="aa5d5-135">Vertex</span></span> | <span data-ttu-id="aa5d5-136">Поверхности</span><span class="sxs-lookup"><span data-stu-id="aa5d5-136">Hull</span></span> | <span data-ttu-id="aa5d5-137">Домен</span><span class="sxs-lookup"><span data-stu-id="aa5d5-137">Domain</span></span> | <span data-ttu-id="aa5d5-138">Геометрия</span><span class="sxs-lookup"><span data-stu-id="aa5d5-138">Geometry</span></span> | <span data-ttu-id="aa5d5-139">Пиксель</span><span class="sxs-lookup"><span data-stu-id="aa5d5-139">Pixel</span></span> | <span data-ttu-id="aa5d5-140">Вычисления</span><span class="sxs-lookup"><span data-stu-id="aa5d5-140">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="aa5d5-141">X</span><span class="sxs-lookup"><span data-stu-id="aa5d5-141">X</span></span>      | <span data-ttu-id="aa5d5-142">X</span><span class="sxs-lookup"><span data-stu-id="aa5d5-142">X</span></span>    | <span data-ttu-id="aa5d5-143">X</span><span class="sxs-lookup"><span data-stu-id="aa5d5-143">X</span></span>      | <span data-ttu-id="aa5d5-144">X</span><span class="sxs-lookup"><span data-stu-id="aa5d5-144">X</span></span>        | <span data-ttu-id="aa5d5-145">X</span><span class="sxs-lookup"><span data-stu-id="aa5d5-145">X</span></span>     | <span data-ttu-id="aa5d5-146">X</span><span class="sxs-lookup"><span data-stu-id="aa5d5-146">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="aa5d5-147">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="aa5d5-147">Minimum Shader Model</span></span>

<span data-ttu-id="aa5d5-148">Эта инструкция поддерживается в следующих моделях шейдеров:</span><span class="sxs-lookup"><span data-stu-id="aa5d5-148">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="aa5d5-149">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="aa5d5-149">Shader Model</span></span>                                              | <span data-ttu-id="aa5d5-150">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="aa5d5-150">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="aa5d5-151">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="aa5d5-151">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="aa5d5-152">да</span><span class="sxs-lookup"><span data-stu-id="aa5d5-152">yes</span></span>       |
| [<span data-ttu-id="aa5d5-153">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="aa5d5-153">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="aa5d5-154">Нет</span><span class="sxs-lookup"><span data-stu-id="aa5d5-154">no</span></span>        |
| [<span data-ttu-id="aa5d5-155">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="aa5d5-155">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="aa5d5-156">Нет</span><span class="sxs-lookup"><span data-stu-id="aa5d5-156">no</span></span>        |
| [<span data-ttu-id="aa5d5-157">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="aa5d5-157">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="aa5d5-158">Нет</span><span class="sxs-lookup"><span data-stu-id="aa5d5-158">no</span></span>        |
| [<span data-ttu-id="aa5d5-159">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="aa5d5-159">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="aa5d5-160">Нет</span><span class="sxs-lookup"><span data-stu-id="aa5d5-160">no</span></span>        |
| [<span data-ttu-id="aa5d5-161">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="aa5d5-161">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="aa5d5-162">Нет</span><span class="sxs-lookup"><span data-stu-id="aa5d5-162">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="aa5d5-163">См. также</span><span class="sxs-lookup"><span data-stu-id="aa5d5-163">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aa5d5-164">Сборка Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="aa5d5-164">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





