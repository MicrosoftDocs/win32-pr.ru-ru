---
title: f16tof32 (SM5-ASM)
description: Float16 на уровне компонентов для преобразования float32. | f16tof32 (SM5-ASM)
ms.assetid: CFAA1350-DA7F-4105-A90A-72052C5E2FB3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d53af1f2eab1f50dfded820bf27b2cda8f23e6b4
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986428"
---
# <a name="f16tof32-sm5---asm"></a><span data-ttu-id="3a4df-104">f16tof32 (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="3a4df-104">f16tof32 (sm5 - asm)</span></span>

<span data-ttu-id="3a4df-105">Float16 на уровне компонентов для преобразования float32.</span><span class="sxs-lookup"><span data-stu-id="3a4df-105">Component-wise float16 to float32 conversion.</span></span>



| <span data-ttu-id="3a4df-106">f16tof32 dest \[ . Mask \] , \[ - \] src \[ . свиззле\]</span><span class="sxs-lookup"><span data-stu-id="3a4df-106">f16tof32 dest\[.mask\], \[-\]src\[.swizzle\]</span></span> |
|----------------------------------------------|



 



| <span data-ttu-id="3a4df-107">Элемент</span><span class="sxs-lookup"><span data-stu-id="3a4df-107">Item</span></span>                                                            | <span data-ttu-id="3a4df-108">Описание</span><span class="sxs-lookup"><span data-stu-id="3a4df-108">Description</span></span>                                          |
|-----------------------------------------------------------------|------------------------------------------------------|
| <span data-ttu-id="3a4df-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="3a4df-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="3a4df-110">\[в \] адресе результата float32.</span><span class="sxs-lookup"><span data-stu-id="3a4df-110">\[in\] The address of the float32 result.</span></span><br/> |
| <span data-ttu-id="3a4df-111"><span id="src"></span><span id="SRC"></span>*src*</span><span class="sxs-lookup"><span data-stu-id="3a4df-111"><span id="src"></span><span id="SRC"></span>*src*</span></span><br/>    | <span data-ttu-id="3a4df-112">\[в \] значении float16 для преобразования.</span><span class="sxs-lookup"><span data-stu-id="3a4df-112">\[in\] The float16 value to convert.</span></span><br/>      |



 

## <a name="remarks"></a><span data-ttu-id="3a4df-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="3a4df-113">Remarks</span></span>

<span data-ttu-id="3a4df-114">Эта операция выполняет покомпонентное преобразование значения float16 из ЛСБ разрядов в результат float32.</span><span class="sxs-lookup"><span data-stu-id="3a4df-114">This operation performs a component-wise conversion of a float16 value from LSB bits to a float32 result.</span></span>

<span data-ttu-id="3a4df-115">Эта операция соответствует правилам D3D для преобразования плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="3a4df-115">This operation follows D3D rules for floating point conversion.</span></span>

<span data-ttu-id="3a4df-116">Используйте эту инструкцию для распаковки данных, управляемой шейдером.</span><span class="sxs-lookup"><span data-stu-id="3a4df-116">Use this instruction for shader-driven data decompression.</span></span>

<span data-ttu-id="3a4df-117">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="3a4df-117">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="3a4df-118">Вершина</span><span class="sxs-lookup"><span data-stu-id="3a4df-118">Vertex</span></span> | <span data-ttu-id="3a4df-119">Поверхности</span><span class="sxs-lookup"><span data-stu-id="3a4df-119">Hull</span></span> | <span data-ttu-id="3a4df-120">Домен</span><span class="sxs-lookup"><span data-stu-id="3a4df-120">Domain</span></span> | <span data-ttu-id="3a4df-121">Геометрия</span><span class="sxs-lookup"><span data-stu-id="3a4df-121">Geometry</span></span> | <span data-ttu-id="3a4df-122">Пиксель</span><span class="sxs-lookup"><span data-stu-id="3a4df-122">Pixel</span></span> | <span data-ttu-id="3a4df-123">Вычисления</span><span class="sxs-lookup"><span data-stu-id="3a4df-123">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="3a4df-124">X</span><span class="sxs-lookup"><span data-stu-id="3a4df-124">X</span></span>      | <span data-ttu-id="3a4df-125">X</span><span class="sxs-lookup"><span data-stu-id="3a4df-125">X</span></span>    | <span data-ttu-id="3a4df-126">X</span><span class="sxs-lookup"><span data-stu-id="3a4df-126">X</span></span>      | <span data-ttu-id="3a4df-127">X</span><span class="sxs-lookup"><span data-stu-id="3a4df-127">X</span></span>        | <span data-ttu-id="3a4df-128">X</span><span class="sxs-lookup"><span data-stu-id="3a4df-128">X</span></span>     | <span data-ttu-id="3a4df-129">X</span><span class="sxs-lookup"><span data-stu-id="3a4df-129">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="3a4df-130">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="3a4df-130">Minimum Shader Model</span></span>

<span data-ttu-id="3a4df-131">Эта инструкция поддерживается в следующих моделях шейдеров:</span><span class="sxs-lookup"><span data-stu-id="3a4df-131">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="3a4df-132">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="3a4df-132">Shader Model</span></span>                                              | <span data-ttu-id="3a4df-133">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="3a4df-133">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="3a4df-134">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="3a4df-134">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="3a4df-135">да</span><span class="sxs-lookup"><span data-stu-id="3a4df-135">yes</span></span>       |
| [<span data-ttu-id="3a4df-136">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="3a4df-136">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="3a4df-137">Нет</span><span class="sxs-lookup"><span data-stu-id="3a4df-137">no</span></span>        |
| [<span data-ttu-id="3a4df-138">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="3a4df-138">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="3a4df-139">Нет</span><span class="sxs-lookup"><span data-stu-id="3a4df-139">no</span></span>        |
| [<span data-ttu-id="3a4df-140">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3a4df-140">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="3a4df-141">Нет</span><span class="sxs-lookup"><span data-stu-id="3a4df-141">no</span></span>        |
| [<span data-ttu-id="3a4df-142">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3a4df-142">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="3a4df-143">Нет</span><span class="sxs-lookup"><span data-stu-id="3a4df-143">no</span></span>        |
| [<span data-ttu-id="3a4df-144">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3a4df-144">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="3a4df-145">Нет</span><span class="sxs-lookup"><span data-stu-id="3a4df-145">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="3a4df-146">См. также</span><span class="sxs-lookup"><span data-stu-id="3a4df-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3a4df-147">Сборка Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3a4df-147">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





