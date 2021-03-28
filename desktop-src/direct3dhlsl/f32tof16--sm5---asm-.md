---
title: f32tof16 (SM5-ASM)
description: Float16 на уровне компонентов для преобразования float32. | f32tof16 (SM5-ASM)
ms.assetid: 36BCCFC5-722A-45EB-8A66-7544833BBBA5
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b54a101f370f9c53d1d3f43f9e1cf6c4da82933d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986705"
---
# <a name="f32tof16-sm5---asm"></a><span data-ttu-id="6b959-104">f32tof16 (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="6b959-104">f32tof16 (sm5 - asm)</span></span>

<span data-ttu-id="6b959-105">Float16 на уровне компонентов для преобразования float32.</span><span class="sxs-lookup"><span data-stu-id="6b959-105">Component-wise float16 to float32 conversion.</span></span>



| <span data-ttu-id="6b959-106">f32tof16 dest \[ . Mask \] , \[ - \] src \[ . свиззле\]</span><span class="sxs-lookup"><span data-stu-id="6b959-106">f32tof16 dest\[.mask\], \[-\]src\[.swizzle\]</span></span> |
|----------------------------------------------|



 



| <span data-ttu-id="6b959-107">Элемент</span><span class="sxs-lookup"><span data-stu-id="6b959-107">Item</span></span>                                                            | <span data-ttu-id="6b959-108">Описание</span><span class="sxs-lookup"><span data-stu-id="6b959-108">Description</span></span>                                      |
|-----------------------------------------------------------------|--------------------------------------------------|
| <span data-ttu-id="6b959-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="6b959-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="6b959-110">\[в \] адресе результата float16.</span><span class="sxs-lookup"><span data-stu-id="6b959-110">\[in\] The address of float16 result.</span></span><br/> |
| <span data-ttu-id="6b959-111"><span id="src"></span><span id="SRC"></span>*src*</span><span class="sxs-lookup"><span data-stu-id="6b959-111"><span id="src"></span><span id="SRC"></span>*src*</span></span><br/>    | <span data-ttu-id="6b959-112">\[в \] преобразуемом значении float32.</span><span class="sxs-lookup"><span data-stu-id="6b959-112">\[in\] The float32 value to convert.</span></span><br/>  |



 

## <a name="remarks"></a><span data-ttu-id="6b959-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="6b959-113">Remarks</span></span>

<span data-ttu-id="6b959-114">Эта инструкция выполняет покомпонентное преобразование значения float32 в результат float16, который помещается в ЛСБ 16 бит.</span><span class="sxs-lookup"><span data-stu-id="6b959-114">This instruction performs a component-wise conversion of a float32 value to a float16 value result placed in LSB 16 bits.</span></span>

<span data-ttu-id="6b959-115">Эта инструкция соответствует правилам D3D для преобразования с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="6b959-115">This instruction follows D3D rules for floating point conversion.</span></span>

<span data-ttu-id="6b959-116">Используйте эту инструкцию для сжатия данных, основанного на шейдере.</span><span class="sxs-lookup"><span data-stu-id="6b959-116">Use this instruction for shader-driven data compression.</span></span>

<span data-ttu-id="6b959-117">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="6b959-117">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="6b959-118">Вершина</span><span class="sxs-lookup"><span data-stu-id="6b959-118">Vertex</span></span> | <span data-ttu-id="6b959-119">Поверхности</span><span class="sxs-lookup"><span data-stu-id="6b959-119">Hull</span></span> | <span data-ttu-id="6b959-120">Домен</span><span class="sxs-lookup"><span data-stu-id="6b959-120">Domain</span></span> | <span data-ttu-id="6b959-121">Геометрия</span><span class="sxs-lookup"><span data-stu-id="6b959-121">Geometry</span></span> | <span data-ttu-id="6b959-122">Пиксель</span><span class="sxs-lookup"><span data-stu-id="6b959-122">Pixel</span></span> | <span data-ttu-id="6b959-123">Вычисления</span><span class="sxs-lookup"><span data-stu-id="6b959-123">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="6b959-124">X</span><span class="sxs-lookup"><span data-stu-id="6b959-124">X</span></span>      | <span data-ttu-id="6b959-125">X</span><span class="sxs-lookup"><span data-stu-id="6b959-125">X</span></span>    | <span data-ttu-id="6b959-126">X</span><span class="sxs-lookup"><span data-stu-id="6b959-126">X</span></span>      | <span data-ttu-id="6b959-127">X</span><span class="sxs-lookup"><span data-stu-id="6b959-127">X</span></span>        | <span data-ttu-id="6b959-128">X</span><span class="sxs-lookup"><span data-stu-id="6b959-128">X</span></span>     | <span data-ttu-id="6b959-129">X</span><span class="sxs-lookup"><span data-stu-id="6b959-129">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="6b959-130">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="6b959-130">Minimum Shader Model</span></span>

<span data-ttu-id="6b959-131">Эта инструкция поддерживается в следующих моделях шейдеров:</span><span class="sxs-lookup"><span data-stu-id="6b959-131">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="6b959-132">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="6b959-132">Shader Model</span></span>                                              | <span data-ttu-id="6b959-133">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="6b959-133">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="6b959-134">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="6b959-134">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="6b959-135">да</span><span class="sxs-lookup"><span data-stu-id="6b959-135">yes</span></span>       |
| [<span data-ttu-id="6b959-136">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="6b959-136">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="6b959-137">Нет</span><span class="sxs-lookup"><span data-stu-id="6b959-137">no</span></span>        |
| [<span data-ttu-id="6b959-138">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="6b959-138">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="6b959-139">Нет</span><span class="sxs-lookup"><span data-stu-id="6b959-139">no</span></span>        |
| [<span data-ttu-id="6b959-140">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6b959-140">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="6b959-141">Нет</span><span class="sxs-lookup"><span data-stu-id="6b959-141">no</span></span>        |
| [<span data-ttu-id="6b959-142">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6b959-142">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="6b959-143">Нет</span><span class="sxs-lookup"><span data-stu-id="6b959-143">no</span></span>        |
| [<span data-ttu-id="6b959-144">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6b959-144">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="6b959-145">Нет</span><span class="sxs-lookup"><span data-stu-id="6b959-145">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="6b959-146">См. также</span><span class="sxs-lookup"><span data-stu-id="6b959-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6b959-147">Сборка Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6b959-147">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





