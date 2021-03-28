---
title: dcl_uav_typed (SM5-ASM)
description: Объявите неупорядоченное представление доступа (UAV) для использования шейдером. | dcl_uav_typed (SM5-ASM)
ms.assetid: F9F5583F-E3D0-447F-9227-BBB1B4E71934
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b789714c7ec825620b73e387fa8a4dd73e1a590d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104998258"
---
# <a name="dcl_uav_typed-sm5---asm"></a><span data-ttu-id="40768-104">дкл \_ UAV \_ типизированный (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="40768-104">dcl\_uav\_typed (sm5 - asm)</span></span>

<span data-ttu-id="40768-105">Объявите неупорядоченное представление доступа (UAV) для использования шейдером.</span><span class="sxs-lookup"><span data-stu-id="40768-105">Declare an unordered access view (UAV) for use by a shader.</span></span>



| <span data-ttu-id="40768-106">дкл \_ UAV \_ типизированный \[ \_ ГЛК \] дстуав, Dimension, Type</span><span class="sxs-lookup"><span data-stu-id="40768-106">dcl\_uav\_typed\[\_glc\] dstUAV, dimension, type</span></span> |
|--------------------------------------------------|



 



| <span data-ttu-id="40768-107">Элемент</span><span class="sxs-lookup"><span data-stu-id="40768-107">Item</span></span>                                                                                           | <span data-ttu-id="40768-108">Описание</span><span class="sxs-lookup"><span data-stu-id="40768-108">Description</span></span>                                                                                       |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="40768-109"><span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*дстуав*</span><span class="sxs-lookup"><span data-stu-id="40768-109"><span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*dstUAV*</span></span><br/> | <span data-ttu-id="40768-110">\[в \] UAV.</span><span class="sxs-lookup"><span data-stu-id="40768-110">\[in\] The UAV.</span></span><br/>                                                                        |
| <span data-ttu-id="40768-111"><span id="dimension"></span><span id="DIMENSION"></span>*фокусирован*</span><span class="sxs-lookup"><span data-stu-id="40768-111"><span id="dimension"></span><span id="DIMENSION"></span>*dimension*</span></span><br/>                 | <span data-ttu-id="40768-112">\[в \] указывает, сколько измерений предоставляет инструкции, обращающиеся к UAV.</span><span class="sxs-lookup"><span data-stu-id="40768-112">\[in\] Specifies how many dimensions the instructions accessing the UAV are providing.</span></span><br/> |
| <span data-ttu-id="40768-113"><span id="type"></span><span id="TYPE"></span>*Тип*</span><span class="sxs-lookup"><span data-stu-id="40768-113"><span id="type"></span><span id="TYPE"></span>*type*</span></span><br/>                                | <span data-ttu-id="40768-114">\[в \] ТИПЕ UAV.</span><span class="sxs-lookup"><span data-stu-id="40768-114">\[in\] The type of the UAV.</span></span><br/>                                                            |



 

## <a name="remarks"></a><span data-ttu-id="40768-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="40768-115">Remarks</span></span>

<span data-ttu-id="40768-116">*дстуав* — это регистр u, \# объявляемый в качестве ссылки на унордередакцессвиев, который должен быть привязан к слоту UAV \# в API.</span><span class="sxs-lookup"><span data-stu-id="40768-116">*dstUAV* is a u\# register being declared as a reference to an UnorderedAccessView that must be bound to UAV slot \# at the API.</span></span>

<span data-ttu-id="40768-117">Измерение должно быть buffer, Texture1D, Texture1DArray, Texture2D, Texture2DArray или Texture3D.</span><span class="sxs-lookup"><span data-stu-id="40768-117">The dimension must be buffer, Texture1D, Texture1DArray, Texture2D, Texture2DArray, or Texture3D.</span></span> <span data-ttu-id="40768-118">Это указывает, сколько измерений все инструкции, обращающиеся к UAV, предоставляют: 1 (Texture1D, buffer), 2 (Texture1DArray, Texture2D) или 3 (Texture2DArray, Texture3D).</span><span class="sxs-lookup"><span data-stu-id="40768-118">This indicates how many dimensions any instructions accessing the UAV are providing: 1 (Texture1D, Buffer), 2 (Texture1DArray, Texture2D) or 3 (Texture2DArray, Texture3D).</span></span>

<span data-ttu-id="40768-119">Тип: {UNORM, СНОРМ, UINT, Синт, FLOAT}.</span><span class="sxs-lookup"><span data-stu-id="40768-119">Type is {UNORM,SNORM,UINT,SINT,FLOAT}.</span></span> <span data-ttu-id="40768-120">Операции, выполняемые с объявленным u, \# должны быть совместимы с типом, объявленным здесь, а UAV, привязанный к слоту, \# также должен иметь один и тот же тип.</span><span class="sxs-lookup"><span data-stu-id="40768-120">Operations done with the declared u\# must be compatible with the type declared here, and the UAV bound to slot \# must also have the same type.</span></span>

<span data-ttu-id="40768-121">\_Флаг ГЛК означает «глобально согласованность».</span><span class="sxs-lookup"><span data-stu-id="40768-121">The \_glc flag stands for "globally coherent".</span></span> <span data-ttu-id="40768-122">Отсутствие \_ ГЛК означает, что UAV объявляется только как "согласование с группами" в шейдере вычислений или "локальное согласование" в одном вызове шейдера пикселей.</span><span class="sxs-lookup"><span data-stu-id="40768-122">The absence of \_glc means the UAV is being declared only as "group coherent" in the compute shader, or "locally coherent" in a single pixel shader invocation.</span></span>

<span data-ttu-id="40768-123">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="40768-123">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="40768-124">Вершина</span><span class="sxs-lookup"><span data-stu-id="40768-124">Vertex</span></span> | <span data-ttu-id="40768-125">Поверхности</span><span class="sxs-lookup"><span data-stu-id="40768-125">Hull</span></span> | <span data-ttu-id="40768-126">Домен</span><span class="sxs-lookup"><span data-stu-id="40768-126">Domain</span></span> | <span data-ttu-id="40768-127">Геометрия</span><span class="sxs-lookup"><span data-stu-id="40768-127">Geometry</span></span> | <span data-ttu-id="40768-128">Пиксель</span><span class="sxs-lookup"><span data-stu-id="40768-128">Pixel</span></span> | <span data-ttu-id="40768-129">Вычисления</span><span class="sxs-lookup"><span data-stu-id="40768-129">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="40768-130">X</span><span class="sxs-lookup"><span data-stu-id="40768-130">X</span></span>     | <span data-ttu-id="40768-131">X</span><span class="sxs-lookup"><span data-stu-id="40768-131">X</span></span>       |



 

<span data-ttu-id="40768-132">Так как Уавс доступны на всех стадиях шейдера для Direct3D 11,1, эта инструкция применяется ко всем этапам шейдера для среды выполнения Direct3D 11,1, которая доступна начиная с Windows 8.</span><span class="sxs-lookup"><span data-stu-id="40768-132">Because UAVs are available at all shader stages for Direct3D 11.1, this instruction applies to all shader stages for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="40768-133">Вершина</span><span class="sxs-lookup"><span data-stu-id="40768-133">Vertex</span></span> | <span data-ttu-id="40768-134">Поверхности</span><span class="sxs-lookup"><span data-stu-id="40768-134">Hull</span></span> | <span data-ttu-id="40768-135">Домен</span><span class="sxs-lookup"><span data-stu-id="40768-135">Domain</span></span> | <span data-ttu-id="40768-136">Геометрия</span><span class="sxs-lookup"><span data-stu-id="40768-136">Geometry</span></span> | <span data-ttu-id="40768-137">Пиксель</span><span class="sxs-lookup"><span data-stu-id="40768-137">Pixel</span></span> | <span data-ttu-id="40768-138">Вычисления</span><span class="sxs-lookup"><span data-stu-id="40768-138">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="40768-139">X</span><span class="sxs-lookup"><span data-stu-id="40768-139">X</span></span>      | <span data-ttu-id="40768-140">X</span><span class="sxs-lookup"><span data-stu-id="40768-140">X</span></span>    | <span data-ttu-id="40768-141">X</span><span class="sxs-lookup"><span data-stu-id="40768-141">X</span></span>      | <span data-ttu-id="40768-142">X</span><span class="sxs-lookup"><span data-stu-id="40768-142">X</span></span>        | <span data-ttu-id="40768-143">X</span><span class="sxs-lookup"><span data-stu-id="40768-143">X</span></span>     | <span data-ttu-id="40768-144">X</span><span class="sxs-lookup"><span data-stu-id="40768-144">X</span></span>       |



 

> [!Note]  
> <span data-ttu-id="40768-145">Эта инструкция не поддерживается в Compute Shader 4. x.</span><span class="sxs-lookup"><span data-stu-id="40768-145">This instruction is not supported in compute shader 4.x.</span></span>

 

## <a name="minimum-shader-model"></a><span data-ttu-id="40768-146">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="40768-146">Minimum Shader Model</span></span>

<span data-ttu-id="40768-147">Эта инструкция поддерживается в следующих моделях шейдеров:</span><span class="sxs-lookup"><span data-stu-id="40768-147">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="40768-148">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="40768-148">Shader Model</span></span>                                              | <span data-ttu-id="40768-149">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="40768-149">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="40768-150">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="40768-150">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="40768-151">да</span><span class="sxs-lookup"><span data-stu-id="40768-151">yes</span></span>       |
| [<span data-ttu-id="40768-152">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="40768-152">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="40768-153">Нет</span><span class="sxs-lookup"><span data-stu-id="40768-153">no</span></span>        |
| [<span data-ttu-id="40768-154">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="40768-154">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="40768-155">Нет</span><span class="sxs-lookup"><span data-stu-id="40768-155">no</span></span>        |
| [<span data-ttu-id="40768-156">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="40768-156">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="40768-157">Нет</span><span class="sxs-lookup"><span data-stu-id="40768-157">no</span></span>        |
| [<span data-ttu-id="40768-158">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="40768-158">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="40768-159">Нет</span><span class="sxs-lookup"><span data-stu-id="40768-159">no</span></span>        |
| [<span data-ttu-id="40768-160">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="40768-160">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="40768-161">Нет</span><span class="sxs-lookup"><span data-stu-id="40768-161">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="40768-162">См. также</span><span class="sxs-lookup"><span data-stu-id="40768-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="40768-163">Сборка Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="40768-163">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





