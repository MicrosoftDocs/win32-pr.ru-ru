---
title: dcl_resource RAW (SM5-ASM)
description: Объявите входные данные ресурса шейдера и назначьте его t \-a заполнитель для ресурса. | dcl_resource RAW (SM5-ASM)
ms.assetid: ECBA9DAB-F217-47FB-9588-F35866004E72
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8dd6ccc5990e34990772a072086d9e080cde67b4
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104273508"
---
# <a name="dcl_resource-raw-sm5---asm"></a><span data-ttu-id="ba432-104">дкл \_ ресурс необработанных ресурсов (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="ba432-104">dcl\_resource raw (sm5 - asm)</span></span>

<span data-ttu-id="ba432-105">Объявите входные данные ресурса шейдера и присвойте его \# заполнительу t-a для ресурса.</span><span class="sxs-lookup"><span data-stu-id="ba432-105">Declare a shader resource input and assign it to a t\# - a placeholder register for the resource.</span></span>



| <span data-ttu-id="ba432-106">дкл \_ ресурс \_ необработанных дстсрв</span><span class="sxs-lookup"><span data-stu-id="ba432-106">dcl\_resource\_raw dstSRV</span></span> |
|---------------------------|



 



| <span data-ttu-id="ba432-107">Элемент</span><span class="sxs-lookup"><span data-stu-id="ba432-107">Item</span></span>                                                                                           | <span data-ttu-id="ba432-108">Описание</span><span class="sxs-lookup"><span data-stu-id="ba432-108">Description</span></span>                                                                                       |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba432-109"><span id="dstSRV"></span><span id="dstsrv"></span><span id="DSTSRV"></span>*дстсрв*</span><span class="sxs-lookup"><span data-stu-id="ba432-109"><span id="dstSRV"></span><span id="dstsrv"></span><span id="DSTSRV"></span>*dstSRV*</span></span><br/> | <span data-ttu-id="ba432-110">\[в \] регистре t, \# объявленном как ссылка на шадерресаурцевиев необработанного буфера.</span><span class="sxs-lookup"><span data-stu-id="ba432-110">\[in\] A t\# register declared as a reference to a ShaderResourceView of a raw buffer.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ba432-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="ba432-111">Remarks</span></span>

<span data-ttu-id="ba432-112">Содержимое структуры не имеет типа; операции, выполняемые в памяти, могут неявно интерпретировать данные как имеющие тип.</span><span class="sxs-lookup"><span data-stu-id="ba432-112">The contents of the structure have no type; operations performed on the memory may implicitly interpret the data as having a type.</span></span>

<span data-ttu-id="ba432-113">Инструкции, которые ссылаются на необработанный t- \# адрес, принимают одномерное (не32 подписанное) значение, которое задает смещение в байтах до 32-битного расположения в буфере.</span><span class="sxs-lookup"><span data-stu-id="ba432-113">Instructions that reference a raw t\# take a 1D address, an unsigned 32-bit value specifying the byte offset to a 32-bit aligned location in the Buffer.</span></span> <span data-ttu-id="ba432-114">Адрес должен быть кратен 4 (байт).</span><span class="sxs-lookup"><span data-stu-id="ba432-114">The address must be a multiple of 4 (bytes).</span></span>

<span data-ttu-id="ba432-115">Представления, привязанные к t \# , объявленные как RAW, должны иметь НЕобработанные значения для их создания; иначе поведение при доступе из шейдера не определено.</span><span class="sxs-lookup"><span data-stu-id="ba432-115">Views bound to t\# declared as raw must have RAW specified on their creation; otherwise behavior when accessed from a shader is undefined.</span></span>

<span data-ttu-id="ba432-116">\_инструкция CS 4 \_ 0 и CS \_ 4 \_ 1 поддерживают эту инструкцию.</span><span class="sxs-lookup"><span data-stu-id="ba432-116">cs\_4\_0 and cs\_4\_1 support this instruction.</span></span>

<span data-ttu-id="ba432-117">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="ba432-117">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="ba432-118">Вершина</span><span class="sxs-lookup"><span data-stu-id="ba432-118">Vertex</span></span> | <span data-ttu-id="ba432-119">Поверхности</span><span class="sxs-lookup"><span data-stu-id="ba432-119">Hull</span></span> | <span data-ttu-id="ba432-120">Домен</span><span class="sxs-lookup"><span data-stu-id="ba432-120">Domain</span></span> | <span data-ttu-id="ba432-121">Геометрия</span><span class="sxs-lookup"><span data-stu-id="ba432-121">Geometry</span></span> | <span data-ttu-id="ba432-122">Пиксель</span><span class="sxs-lookup"><span data-stu-id="ba432-122">Pixel</span></span> | <span data-ttu-id="ba432-123">Вычисления</span><span class="sxs-lookup"><span data-stu-id="ba432-123">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="ba432-124">X</span><span class="sxs-lookup"><span data-stu-id="ba432-124">X</span></span>      | <span data-ttu-id="ba432-125">X</span><span class="sxs-lookup"><span data-stu-id="ba432-125">X</span></span>    | <span data-ttu-id="ba432-126">X</span><span class="sxs-lookup"><span data-stu-id="ba432-126">X</span></span>      | <span data-ttu-id="ba432-127">X</span><span class="sxs-lookup"><span data-stu-id="ba432-127">X</span></span>        | <span data-ttu-id="ba432-128">X</span><span class="sxs-lookup"><span data-stu-id="ba432-128">X</span></span>     | <span data-ttu-id="ba432-129">X</span><span class="sxs-lookup"><span data-stu-id="ba432-129">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="ba432-130">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="ba432-130">Minimum Shader Model</span></span>

<span data-ttu-id="ba432-131">Эта инструкция поддерживается в следующих моделях шейдеров:</span><span class="sxs-lookup"><span data-stu-id="ba432-131">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="ba432-132">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="ba432-132">Shader Model</span></span>                                              | <span data-ttu-id="ba432-133">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="ba432-133">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="ba432-134">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="ba432-134">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="ba432-135">да</span><span class="sxs-lookup"><span data-stu-id="ba432-135">yes</span></span>       |
| [<span data-ttu-id="ba432-136">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="ba432-136">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="ba432-137">Нет</span><span class="sxs-lookup"><span data-stu-id="ba432-137">no</span></span>        |
| [<span data-ttu-id="ba432-138">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="ba432-138">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="ba432-139">Нет</span><span class="sxs-lookup"><span data-stu-id="ba432-139">no</span></span>        |
| [<span data-ttu-id="ba432-140">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ba432-140">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="ba432-141">Нет</span><span class="sxs-lookup"><span data-stu-id="ba432-141">no</span></span>        |
| [<span data-ttu-id="ba432-142">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ba432-142">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="ba432-143">Нет</span><span class="sxs-lookup"><span data-stu-id="ba432-143">no</span></span>        |
| [<span data-ttu-id="ba432-144">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ba432-144">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="ba432-145">Нет</span><span class="sxs-lookup"><span data-stu-id="ba432-145">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="ba432-146">См. также</span><span class="sxs-lookup"><span data-stu-id="ba432-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ba432-147">Сборка Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ba432-147">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





