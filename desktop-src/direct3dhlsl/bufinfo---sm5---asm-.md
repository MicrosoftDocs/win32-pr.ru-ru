---
title: буфинфо (SM5-ASM)
description: Запрашивает число элементов в буфере (но не в буфере констант).
ms.assetid: 3A5C28F3-FE59-4C67-92AC-66B10E1D9692
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff8dd33871aa5bd56db6e7375979c6d49f374b74
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104996906"
---
# <a name="bufinfo-sm5---asm"></a><span data-ttu-id="2aa53-103">буфинфо (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="2aa53-103">bufinfo (sm5 - asm)</span></span>

<span data-ttu-id="2aa53-104">Запрашивает число элементов в буфере (но не в буфере констант).</span><span class="sxs-lookup"><span data-stu-id="2aa53-104">Query the element count on a buffer (but not the constant buffer).</span></span>



| <span data-ttu-id="2aa53-105">буфинфо dest \[ . Mask \] , сркресаурце</span><span class="sxs-lookup"><span data-stu-id="2aa53-105">bufinfo dest\[.mask\], srcResource</span></span> |
|------------------------------------|



 



| <span data-ttu-id="2aa53-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="2aa53-106">Item</span></span>                                                                                                               | <span data-ttu-id="2aa53-107">Описание</span><span class="sxs-lookup"><span data-stu-id="2aa53-107">Description</span></span>                                                                           |
|--------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2aa53-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="2aa53-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/>                                                    | <span data-ttu-id="2aa53-109">\[в \] адресе результатов.</span><span class="sxs-lookup"><span data-stu-id="2aa53-109">\[in\] The address of the results.</span></span><br/>                                         |
| <span data-ttu-id="2aa53-110"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*сркресаурце*</span><span class="sxs-lookup"><span data-stu-id="2aa53-110"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span></span><br/> | <span data-ttu-id="2aa53-111">\[в \] буфере, отличном от константного буфера, в SRV (t \# ) или UAV (u \# ).</span><span class="sxs-lookup"><span data-stu-id="2aa53-111">\[in\] Buffer, other than a constant Buffer, in an SRV (t\#) or UAV (u\#).</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="2aa53-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="2aa53-112">Remarks</span></span>

<span data-ttu-id="2aa53-113">Все компоненты в *dest* получают целое число элементов в представлении ресурсов шейдера буфера.</span><span class="sxs-lookup"><span data-stu-id="2aa53-113">All components in *dest* receive the integer number of elements in the buffer s shader resource view.</span></span> <span data-ttu-id="2aa53-114">Количество элементов зависит от параметров представления, таких как формат памяти.</span><span class="sxs-lookup"><span data-stu-id="2aa53-114">The number of elements depends on the view parameters such as memory format.</span></span>

<span data-ttu-id="2aa53-115">Для типизированного буфера SRV или UAV возвращаемое значение — это число элементов в представлении (где элемент является одной единицей типизированного формата).</span><span class="sxs-lookup"><span data-stu-id="2aa53-115">For a typed buffer SRV or UAV, the return value is the number of elements in the view (where an element is one unit of the typed format).</span></span>

<span data-ttu-id="2aa53-116">Для необработанного буфера SRV или UAV возвращаемым значением является число байтов в представлении.</span><span class="sxs-lookup"><span data-stu-id="2aa53-116">For a raw buffer SRV or UAV, the return value is the number of bytes in the view.</span></span>

<span data-ttu-id="2aa53-117">Для структурированного буфера SRV или UAV возвращаемым значением является число структур в представлении.</span><span class="sxs-lookup"><span data-stu-id="2aa53-117">For a structured buffer SRV or UAV, the return value is the number of structures in the view.</span></span>

<span data-ttu-id="2aa53-118">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="2aa53-118">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="2aa53-119">Вершина</span><span class="sxs-lookup"><span data-stu-id="2aa53-119">Vertex</span></span> | <span data-ttu-id="2aa53-120">Поверхности</span><span class="sxs-lookup"><span data-stu-id="2aa53-120">Hull</span></span> | <span data-ttu-id="2aa53-121">Домен</span><span class="sxs-lookup"><span data-stu-id="2aa53-121">Domain</span></span> | <span data-ttu-id="2aa53-122">Геометрия</span><span class="sxs-lookup"><span data-stu-id="2aa53-122">Geometry</span></span> | <span data-ttu-id="2aa53-123">Пиксель</span><span class="sxs-lookup"><span data-stu-id="2aa53-123">Pixel</span></span> | <span data-ttu-id="2aa53-124">Вычисления</span><span class="sxs-lookup"><span data-stu-id="2aa53-124">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="2aa53-125">X</span><span class="sxs-lookup"><span data-stu-id="2aa53-125">X</span></span>      | <span data-ttu-id="2aa53-126">X</span><span class="sxs-lookup"><span data-stu-id="2aa53-126">X</span></span>    | <span data-ttu-id="2aa53-127">X</span><span class="sxs-lookup"><span data-stu-id="2aa53-127">X</span></span>      | <span data-ttu-id="2aa53-128">X</span><span class="sxs-lookup"><span data-stu-id="2aa53-128">X</span></span>        | <span data-ttu-id="2aa53-129">X</span><span class="sxs-lookup"><span data-stu-id="2aa53-129">X</span></span>     | <span data-ttu-id="2aa53-130">X</span><span class="sxs-lookup"><span data-stu-id="2aa53-130">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="2aa53-131">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="2aa53-131">Minimum Shader Model</span></span>

<span data-ttu-id="2aa53-132">Эта инструкция поддерживается в следующих моделях шейдеров:</span><span class="sxs-lookup"><span data-stu-id="2aa53-132">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="2aa53-133">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="2aa53-133">Shader Model</span></span>                                              | <span data-ttu-id="2aa53-134">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="2aa53-134">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="2aa53-135">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="2aa53-135">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="2aa53-136">да</span><span class="sxs-lookup"><span data-stu-id="2aa53-136">yes</span></span>       |
| [<span data-ttu-id="2aa53-137">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="2aa53-137">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="2aa53-138">Нет</span><span class="sxs-lookup"><span data-stu-id="2aa53-138">no</span></span>        |
| [<span data-ttu-id="2aa53-139">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="2aa53-139">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="2aa53-140">Нет</span><span class="sxs-lookup"><span data-stu-id="2aa53-140">no</span></span>        |
| [<span data-ttu-id="2aa53-141">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2aa53-141">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="2aa53-142">Нет</span><span class="sxs-lookup"><span data-stu-id="2aa53-142">no</span></span>        |
| [<span data-ttu-id="2aa53-143">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2aa53-143">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="2aa53-144">Нет</span><span class="sxs-lookup"><span data-stu-id="2aa53-144">no</span></span>        |
| [<span data-ttu-id="2aa53-145">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2aa53-145">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="2aa53-146">Нет</span><span class="sxs-lookup"><span data-stu-id="2aa53-146">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="2aa53-147">См. также</span><span class="sxs-lookup"><span data-stu-id="2aa53-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2aa53-148">Сборка Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2aa53-148">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





