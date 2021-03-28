---
title: deriv_rtx_fine (SM5-ASM)
description: Вычисление частоты изменения компонентов. | deriv_rtx_fine (SM5-ASM)
ms.assetid: 5752C85B-2965-489C-BF27-968FAF5EAA52
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73061e3220704cf2c19e28b4d6d434fda43fb941
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104998171"
---
# <a name="deriv_rtx_fine-sm5---asm"></a><span data-ttu-id="cf468-104">наследование \_ RTX \_ прекрасно (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="cf468-104">deriv\_rtx\_fine (sm5 - asm)</span></span>

<span data-ttu-id="cf468-105">Вычисление частоты изменения компонентов.</span><span class="sxs-lookup"><span data-stu-id="cf468-105">Computes the rate of change of components.</span></span>



| <span data-ttu-id="cf468-106">наследование \_ RTX \_ \[ \_ \] \[ . Маска \] , \[ - \] src0 \[ \_ ABS \] \[ . свиззле \] ,</span><span class="sxs-lookup"><span data-stu-id="cf468-106">deriv\_rtx\_fine\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\],</span></span> |
|--------------------------------------------------------------------------|



 



| <span data-ttu-id="cf468-107">Элемент</span><span class="sxs-lookup"><span data-stu-id="cf468-107">Item</span></span>                                                            | <span data-ttu-id="cf468-108">Описание</span><span class="sxs-lookup"><span data-stu-id="cf468-108">Description</span></span>                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="cf468-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="cf468-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="cf468-110">\[в \] адресе результатов операции.</span><span class="sxs-lookup"><span data-stu-id="cf468-110">\[in\] The address of the results of the operation.</span></span><br/> |
| <span data-ttu-id="cf468-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="cf468-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="cf468-112">\[в \] компонентах операции.</span><span class="sxs-lookup"><span data-stu-id="cf468-112">\[in\] The components in the operation.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="cf468-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="cf468-113">Remarks</span></span>

<span data-ttu-id="cf468-114">Эта инструкция оценивает скорость изменения содержимого каждого компонента float32 класса *src0* (POST-свиззле) с точки зрения рендертаржет x Direction (RTX) или рендертаржет y (см. статью о [наследовании \_ РТИ \_](deriv-rty-fine--sm5---asm-.md)).</span><span class="sxs-lookup"><span data-stu-id="cf468-114">This instruction computes the rate of change of contents of each float32 component of *src0* (post-swizzle), with regard to RenderTarget x direction (rtx) or RenderTarget y direction (see [deriv\_rty\_fine](deriv-rty-fine--sm5---asm-.md)).</span></span> <span data-ttu-id="cf468-115">Каждый пиксель в отметке 2x2 получает уникальную пару вычислений, производных от x/y.</span><span class="sxs-lookup"><span data-stu-id="cf468-115">Each pixel in the 2x2 stamp gets a unique pair of x/y derivative calculations</span></span>

<span data-ttu-id="cf468-116">Данные в текущем вызове шейдера пикселей всегда участвуют в вычислении запрошенного производного.</span><span class="sxs-lookup"><span data-stu-id="cf468-116">The data in the current pixel shader invocation always participates in the calculation of the requested derivative.</span></span> <span data-ttu-id="cf468-117">В 1-пиксельном пикселе, находящихся на уровне 2x2, лежит в пределах, производный x — это Дельта строки из 2 пикселей, включая текущий пиксель.</span><span class="sxs-lookup"><span data-stu-id="cf468-117">In the 2x2 pixel quad the current pixel falls within, the x derivative is the delta of the row of 2 pixels including the current pixel.</span></span> <span data-ttu-id="cf468-118">Производный y является разностью столбца в 2 пикселах, включая текущий пиксель.</span><span class="sxs-lookup"><span data-stu-id="cf468-118">The y derivative is the delta of the column of 2 pixels including the current pixel.</span></span> <span data-ttu-id="cf468-119">Нет никакой спецификации, определяющей, как четыре четырехъядерия будут выставляться или накладывается на примитив.</span><span class="sxs-lookup"><span data-stu-id="cf468-119">There is no specification dictating how the 2x2 quads will be aligned or tiled over a primitive.</span></span>

<span data-ttu-id="cf468-120">Производные вычисления рассчитываются на детализированном уровне (уникальное вычисление пары «x/y» для каждого пикселя в 2x2 четырех).</span><span class="sxs-lookup"><span data-stu-id="cf468-120">Derivatives are calculated at a fine level (unique calculation of the x/y derivative pair for each pixel in a 2x2 quad).</span></span> <span data-ttu-id="cf468-121">Эта инструкция и [наследование \_ РТИ \_ прекрасно](deriv-rty-fine--sm5---asm-.md) являются альтернативами, которые [наследуют \_ RTX \_ грубые](deriv-rtx-coarse--sm5---asm-.md) и [наследуют \_ РТИ \_ грубыми](deriv-rty-coarse--sm5---asm-.md).</span><span class="sxs-lookup"><span data-stu-id="cf468-121">This instruction and [deriv\_rty\_fine](deriv-rty-fine--sm5---asm-.md) are alternatives to [deriv\_rtx\_coarse](deriv-rtx-coarse--sm5---asm-.md) and [deriv\_rty\_coarse](deriv-rty-coarse--sm5---asm-.md).</span></span> <span data-ttu-id="cf468-122">Эти \_ грубые и \_ точные инструкции являются заменой для **наследования \_ RTX** . Эти \_ грубые и \_ точные инструкции являются заменой для **наследования \_ RTX** и **наследования \_ РТИ** от предыдущих моделей шейдеров.</span><span class="sxs-lookup"><span data-stu-id="cf468-122">These \_coarse and \_fine derivative instructions are a replacement for **deriv\_rtx** These \_coarse and \_fine derivative instructions are a replacement for **deriv\_rtx** and **deriv\_rty** from previous shader models.</span></span>

<span data-ttu-id="cf468-123">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="cf468-123">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="cf468-124">Вершина</span><span class="sxs-lookup"><span data-stu-id="cf468-124">Vertex</span></span> | <span data-ttu-id="cf468-125">Поверхности</span><span class="sxs-lookup"><span data-stu-id="cf468-125">Hull</span></span> | <span data-ttu-id="cf468-126">Домен</span><span class="sxs-lookup"><span data-stu-id="cf468-126">Domain</span></span> | <span data-ttu-id="cf468-127">Геометрия</span><span class="sxs-lookup"><span data-stu-id="cf468-127">Geometry</span></span> | <span data-ttu-id="cf468-128">Пиксель</span><span class="sxs-lookup"><span data-stu-id="cf468-128">Pixel</span></span> | <span data-ttu-id="cf468-129">Вычисления</span><span class="sxs-lookup"><span data-stu-id="cf468-129">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="cf468-130">X</span><span class="sxs-lookup"><span data-stu-id="cf468-130">X</span></span>     |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="cf468-131">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="cf468-131">Minimum Shader Model</span></span>

<span data-ttu-id="cf468-132">Эта инструкция поддерживается в следующих моделях шейдеров:</span><span class="sxs-lookup"><span data-stu-id="cf468-132">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="cf468-133">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="cf468-133">Shader Model</span></span>                                              | <span data-ttu-id="cf468-134">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="cf468-134">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="cf468-135">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="cf468-135">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="cf468-136">да</span><span class="sxs-lookup"><span data-stu-id="cf468-136">yes</span></span>       |
| [<span data-ttu-id="cf468-137">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="cf468-137">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="cf468-138">Нет</span><span class="sxs-lookup"><span data-stu-id="cf468-138">no</span></span>        |
| [<span data-ttu-id="cf468-139">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="cf468-139">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="cf468-140">Нет</span><span class="sxs-lookup"><span data-stu-id="cf468-140">no</span></span>        |
| [<span data-ttu-id="cf468-141">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="cf468-141">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="cf468-142">Нет</span><span class="sxs-lookup"><span data-stu-id="cf468-142">no</span></span>        |
| [<span data-ttu-id="cf468-143">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="cf468-143">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="cf468-144">Нет</span><span class="sxs-lookup"><span data-stu-id="cf468-144">no</span></span>        |
| [<span data-ttu-id="cf468-145">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="cf468-145">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="cf468-146">Нет</span><span class="sxs-lookup"><span data-stu-id="cf468-146">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="cf468-147">См. также</span><span class="sxs-lookup"><span data-stu-id="cf468-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cf468-148">Сборка Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="cf468-148">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





