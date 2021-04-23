---
title: dcl_resource Structured (SM5-ASM)
description: Объявите входные данные ресурса шейдера и назначьте его t \-a заполнитель для ресурса. | dcl_resource Structured (SM5-ASM)
ms.assetid: 87FC8A56-9DB2-424B-889C-2AB59885DA13
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ab993e0cb260529c3419210c33f5d735a625bce
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104273445"
---
# <a name="dcl_resource-structured-sm5---asm"></a><span data-ttu-id="0035a-104">\_структурированный ресурс дкл (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="0035a-104">dcl\_resource structured (sm5 - asm)</span></span>

<span data-ttu-id="0035a-105">Объявите входные данные ресурса шейдера и присвойте его \# заполнительу t-a для ресурса.</span><span class="sxs-lookup"><span data-stu-id="0035a-105">Declare a shader resource input and assign it to a t\# - a placeholder register for the resource.</span></span>



| <span data-ttu-id="0035a-106">дкл \_ Resource \_ Structured Дстсрв, структбитестриде</span><span class="sxs-lookup"><span data-stu-id="0035a-106">dcl\_resource\_structured dstSRV, structByteStride</span></span> |
|----------------------------------------------------|



 



| <span data-ttu-id="0035a-107">Элемент</span><span class="sxs-lookup"><span data-stu-id="0035a-107">Item</span></span>                                                                                                                                   | <span data-ttu-id="0035a-108">Описание</span><span class="sxs-lookup"><span data-stu-id="0035a-108">Description</span></span>                                                                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0035a-109"><span id="dstSRV"></span><span id="dstsrv"></span><span id="DSTSRV"></span>*дстсрв*</span><span class="sxs-lookup"><span data-stu-id="0035a-109"><span id="dstSRV"></span><span id="dstsrv"></span><span id="DSTSRV"></span>*dstSRV*</span></span><br/>                                         | <span data-ttu-id="0035a-110">\[в \] регистре t, \# объявленном как ссылка на шадерресаурцевиев структурированного буфера с указанным шагом, который должен быть привязан к СЛОТу SRV в \# API.</span><span class="sxs-lookup"><span data-stu-id="0035a-110">\[in\] A t\# register declared as a reference to a ShaderResourceView of a structured buffer with the specified stride that must be bound to SRV slot \# at the API.</span></span> <br/> |
| <span data-ttu-id="0035a-111"><span id="structByteStride"></span><span id="structbytestride"></span><span id="STRUCTBYTESTRIDE"></span>*структбитестриде*</span><span class="sxs-lookup"><span data-stu-id="0035a-111"><span id="structByteStride"></span><span id="structbytestride"></span><span id="STRUCTBYTESTRIDE"></span>*structByteStride*</span></span><br/> | <span data-ttu-id="0035a-112">\[в \] uint, определяющем размер структуры в байтах в объявляемом буфере.</span><span class="sxs-lookup"><span data-stu-id="0035a-112">\[in\] A uint that specifies the size of the structure in bytes in the buffer being declared.</span></span> <span data-ttu-id="0035a-113">Это значение должно быть больше нуля.</span><span class="sxs-lookup"><span data-stu-id="0035a-113">This value must be greater than zero.</span></span><br/>                                   |



 

## <a name="remarks"></a><span data-ttu-id="0035a-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="0035a-114">Remarks</span></span>

<span data-ttu-id="0035a-115">Содержимое структуры не имеет типа; операции, выполняемые в памяти, могут неявно интерпретировать данные как имеющие тип.</span><span class="sxs-lookup"><span data-stu-id="0035a-115">The contents of the structure have no type; operations performed on the memory may implicitly interpret the data as having a type.</span></span>

<span data-ttu-id="0035a-116">Инструкции, которые ссылаются на структурированный t \# , принимают 2D-адрес, где первый компонент выбирает \[ структуру \] , а второй компонент выбирает \[ смещение в структуре, кратное 32 бит \] .</span><span class="sxs-lookup"><span data-stu-id="0035a-116">Instructions that reference a structured t\# take a 2D address, where the first component picks \[struct\], and the second component picks \[offset within struct, multiple of 32-bits\].</span></span>

<span data-ttu-id="0035a-117">\_инструкция CS 4 \_ 0 и CS \_ 4 \_ 1 поддерживают эту инструкцию.</span><span class="sxs-lookup"><span data-stu-id="0035a-117">cs\_4\_0 and cs\_4\_1 support this instruction.</span></span>

<span data-ttu-id="0035a-118">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="0035a-118">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="0035a-119">Вершина</span><span class="sxs-lookup"><span data-stu-id="0035a-119">Vertex</span></span> | <span data-ttu-id="0035a-120">Поверхности</span><span class="sxs-lookup"><span data-stu-id="0035a-120">Hull</span></span> | <span data-ttu-id="0035a-121">Домен</span><span class="sxs-lookup"><span data-stu-id="0035a-121">Domain</span></span> | <span data-ttu-id="0035a-122">Геометрия</span><span class="sxs-lookup"><span data-stu-id="0035a-122">Geometry</span></span> | <span data-ttu-id="0035a-123">Пиксель</span><span class="sxs-lookup"><span data-stu-id="0035a-123">Pixel</span></span> | <span data-ttu-id="0035a-124">Вычисления</span><span class="sxs-lookup"><span data-stu-id="0035a-124">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="0035a-125">X</span><span class="sxs-lookup"><span data-stu-id="0035a-125">X</span></span>      | <span data-ttu-id="0035a-126">X</span><span class="sxs-lookup"><span data-stu-id="0035a-126">X</span></span>    | <span data-ttu-id="0035a-127">X</span><span class="sxs-lookup"><span data-stu-id="0035a-127">X</span></span>      | <span data-ttu-id="0035a-128">X</span><span class="sxs-lookup"><span data-stu-id="0035a-128">X</span></span>        | <span data-ttu-id="0035a-129">X</span><span class="sxs-lookup"><span data-stu-id="0035a-129">X</span></span>     | <span data-ttu-id="0035a-130">X</span><span class="sxs-lookup"><span data-stu-id="0035a-130">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="0035a-131">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="0035a-131">Minimum Shader Model</span></span>

<span data-ttu-id="0035a-132">Эта инструкция поддерживается в следующих моделях шейдеров:</span><span class="sxs-lookup"><span data-stu-id="0035a-132">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="0035a-133">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="0035a-133">Shader Model</span></span>                                              | <span data-ttu-id="0035a-134">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="0035a-134">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="0035a-135">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="0035a-135">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="0035a-136">да</span><span class="sxs-lookup"><span data-stu-id="0035a-136">yes</span></span>       |
| [<span data-ttu-id="0035a-137">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="0035a-137">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="0035a-138">Нет</span><span class="sxs-lookup"><span data-stu-id="0035a-138">no</span></span>        |
| [<span data-ttu-id="0035a-139">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="0035a-139">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="0035a-140">Нет</span><span class="sxs-lookup"><span data-stu-id="0035a-140">no</span></span>        |
| [<span data-ttu-id="0035a-141">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0035a-141">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="0035a-142">Нет</span><span class="sxs-lookup"><span data-stu-id="0035a-142">no</span></span>        |
| [<span data-ttu-id="0035a-143">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0035a-143">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="0035a-144">Нет</span><span class="sxs-lookup"><span data-stu-id="0035a-144">no</span></span>        |
| [<span data-ttu-id="0035a-145">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0035a-145">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="0035a-146">Нет</span><span class="sxs-lookup"><span data-stu-id="0035a-146">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="0035a-147">См. также</span><span class="sxs-lookup"><span data-stu-id="0035a-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0035a-148">Сборка Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0035a-148">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





