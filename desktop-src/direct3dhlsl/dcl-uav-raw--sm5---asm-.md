---
title: dcl_uav_raw (SM5-ASM)
description: Объявите неупорядоченное представление доступа (UAV) для использования шейдером. | dcl_uav_raw (SM5-ASM)
ms.assetid: D0F43FF8-FF1C-4E42-AF42-F528C98FD680
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f47614d5a9327f2d686a36db6bfe4afeb653788
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104998094"
---
# <a name="dcl_uav_raw-sm5---asm"></a><span data-ttu-id="ec83c-104">дкл \_ UAV \_ RAW (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="ec83c-104">dcl\_uav\_raw (sm5 - asm)</span></span>

<span data-ttu-id="ec83c-105">Объявите неупорядоченное представление доступа (UAV) для использования шейдером.</span><span class="sxs-lookup"><span data-stu-id="ec83c-105">Declare an unordered access view (UAV) for use by a shader.</span></span>



| <span data-ttu-id="ec83c-106">дкл \_ UAV \_ RAW \[ \_ ГЛК \] дстуав</span><span class="sxs-lookup"><span data-stu-id="ec83c-106">dcl\_uav\_raw\[\_glc\] dstUAV</span></span> |
|-------------------------------|



 



| <span data-ttu-id="ec83c-107">Элемент</span><span class="sxs-lookup"><span data-stu-id="ec83c-107">Item</span></span>                                                                                           | <span data-ttu-id="ec83c-108">Описание</span><span class="sxs-lookup"><span data-stu-id="ec83c-108">Description</span></span>                |
|------------------------------------------------------------------------------------------------|----------------------------|
| <span data-ttu-id="ec83c-109"><span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*дстуав*</span><span class="sxs-lookup"><span data-stu-id="ec83c-109"><span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*dstUAV*</span></span><br/> | <span data-ttu-id="ec83c-110">\[в \] UAV.</span><span class="sxs-lookup"><span data-stu-id="ec83c-110">\[in\] The UAV.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ec83c-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="ec83c-111">Remarks</span></span>

<span data-ttu-id="ec83c-112">*дстуав* — это \# Регистрация в формате u, объявленная как ссылка на унордередакцессвиев буфера, где буфер отображается как простой одномерной массив 32-разрядных нетипизированных записей.</span><span class="sxs-lookup"><span data-stu-id="ec83c-112">*dstUAV* is a u\# register declared as a reference to an UnorderedAccessView of a Buffer, where the buffer appears as a simple 1D array of 32-bit untyped entries.</span></span>

<span data-ttu-id="ec83c-113">Операции, выполняемые в памяти, могут неявно интерпретировать данные как имеющие тип.</span><span class="sxs-lookup"><span data-stu-id="ec83c-113">Operations performed on the memory may implicitly interpret the data as having a type.</span></span>

<span data-ttu-id="ec83c-114">\_Флаг ГЛК означает «глобально согласованность».</span><span class="sxs-lookup"><span data-stu-id="ec83c-114">The \_glc flag means "globally coherent".</span></span> <span data-ttu-id="ec83c-115">Отсутствие \_ ГЛК означает, что UAV объявляется только как "согласование с группами" в шейдере вычислений или "локальное согласование" в одном вызове шейдера пикселей.</span><span class="sxs-lookup"><span data-stu-id="ec83c-115">The absence of \_glc means the UAV is being declared only as "group coherent" in the compute shader, or "locally coherent" in a single pixel shader invocation.</span></span>

<span data-ttu-id="ec83c-116">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="ec83c-116">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="ec83c-117">Вершина</span><span class="sxs-lookup"><span data-stu-id="ec83c-117">Vertex</span></span> | <span data-ttu-id="ec83c-118">Поверхности</span><span class="sxs-lookup"><span data-stu-id="ec83c-118">Hull</span></span> | <span data-ttu-id="ec83c-119">Домен</span><span class="sxs-lookup"><span data-stu-id="ec83c-119">Domain</span></span> | <span data-ttu-id="ec83c-120">Геометрия</span><span class="sxs-lookup"><span data-stu-id="ec83c-120">Geometry</span></span> | <span data-ttu-id="ec83c-121">Пиксель</span><span class="sxs-lookup"><span data-stu-id="ec83c-121">Pixel</span></span> | <span data-ttu-id="ec83c-122">Вычисления</span><span class="sxs-lookup"><span data-stu-id="ec83c-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="ec83c-123">X</span><span class="sxs-lookup"><span data-stu-id="ec83c-123">X</span></span>     | <span data-ttu-id="ec83c-124">X</span><span class="sxs-lookup"><span data-stu-id="ec83c-124">X</span></span>       |



 

<span data-ttu-id="ec83c-125">Так как Уавс доступны на всех стадиях шейдера для Direct3D 11,1, эта инструкция применяется ко всем этапам шейдера для среды выполнения Direct3D 11,1, которая доступна начиная с Windows 8.</span><span class="sxs-lookup"><span data-stu-id="ec83c-125">Because UAVs are available at all shader stages for Direct3D 11.1, this instruction applies to all shader stages for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="ec83c-126">Вершина</span><span class="sxs-lookup"><span data-stu-id="ec83c-126">Vertex</span></span> | <span data-ttu-id="ec83c-127">Поверхности</span><span class="sxs-lookup"><span data-stu-id="ec83c-127">Hull</span></span> | <span data-ttu-id="ec83c-128">Домен</span><span class="sxs-lookup"><span data-stu-id="ec83c-128">Domain</span></span> | <span data-ttu-id="ec83c-129">Геометрия</span><span class="sxs-lookup"><span data-stu-id="ec83c-129">Geometry</span></span> | <span data-ttu-id="ec83c-130">Пиксель</span><span class="sxs-lookup"><span data-stu-id="ec83c-130">Pixel</span></span> | <span data-ttu-id="ec83c-131">Вычисления</span><span class="sxs-lookup"><span data-stu-id="ec83c-131">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="ec83c-132">X</span><span class="sxs-lookup"><span data-stu-id="ec83c-132">X</span></span>      | <span data-ttu-id="ec83c-133">X</span><span class="sxs-lookup"><span data-stu-id="ec83c-133">X</span></span>    | <span data-ttu-id="ec83c-134">X</span><span class="sxs-lookup"><span data-stu-id="ec83c-134">X</span></span>      | <span data-ttu-id="ec83c-135">X</span><span class="sxs-lookup"><span data-stu-id="ec83c-135">X</span></span>        | <span data-ttu-id="ec83c-136">X</span><span class="sxs-lookup"><span data-stu-id="ec83c-136">X</span></span>     | <span data-ttu-id="ec83c-137">X</span><span class="sxs-lookup"><span data-stu-id="ec83c-137">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="ec83c-138">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="ec83c-138">Minimum Shader Model</span></span>

<span data-ttu-id="ec83c-139">Эта инструкция поддерживается в следующих моделях шейдеров:</span><span class="sxs-lookup"><span data-stu-id="ec83c-139">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="ec83c-140">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="ec83c-140">Shader Model</span></span>                                              | <span data-ttu-id="ec83c-141">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="ec83c-141">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="ec83c-142">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="ec83c-142">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="ec83c-143">да</span><span class="sxs-lookup"><span data-stu-id="ec83c-143">yes</span></span>       |
| [<span data-ttu-id="ec83c-144">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="ec83c-144">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="ec83c-145">Нет</span><span class="sxs-lookup"><span data-stu-id="ec83c-145">no</span></span>        |
| [<span data-ttu-id="ec83c-146">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="ec83c-146">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="ec83c-147">Нет</span><span class="sxs-lookup"><span data-stu-id="ec83c-147">no</span></span>        |
| [<span data-ttu-id="ec83c-148">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ec83c-148">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="ec83c-149">Нет</span><span class="sxs-lookup"><span data-stu-id="ec83c-149">no</span></span>        |
| [<span data-ttu-id="ec83c-150">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ec83c-150">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="ec83c-151">Нет</span><span class="sxs-lookup"><span data-stu-id="ec83c-151">no</span></span>        |
| [<span data-ttu-id="ec83c-152">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ec83c-152">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="ec83c-153">Нет</span><span class="sxs-lookup"><span data-stu-id="ec83c-153">no</span></span>        |



 

> [!Note]  
> <span data-ttu-id="ec83c-154">Эта инструкция поддерживается в CS \_ 4 \_ 0 и CS \_ 4 \_ 1.</span><span class="sxs-lookup"><span data-stu-id="ec83c-154">This instruction is supported in cs\_4\_0 and cs\_4\_1.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="ec83c-155">См. также</span><span class="sxs-lookup"><span data-stu-id="ec83c-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ec83c-156">Сборка Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ec83c-156">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





