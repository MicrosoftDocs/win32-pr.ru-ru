---
title: deriv_rtx_coarse (SM5-ASM)
description: Вычисление частоты изменения компонентов. | deriv_rtx_coarse (SM5-ASM)
ms.assetid: 57743BB2-251C-4EA7-BDA9-70B2ECEE3B3F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2355b6db6aef9e85959d6359053fea76b48af0a5
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104998066"
---
# <a name="deriv_rtx_coarse-sm5---asm"></a><span data-ttu-id="5f83b-104">производный \_ RTX \_ грубый (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="5f83b-104">deriv\_rtx\_coarse (sm5 - asm)</span></span>

<span data-ttu-id="5f83b-105">Вычисление частоты изменения компонентов.</span><span class="sxs-lookup"><span data-stu-id="5f83b-105">Computes the rate of change of components.</span></span>



| <span data-ttu-id="5f83b-106">наследование \_ RTX \_ грубой \[ \_ \] \[ перекрытия \] , \[ - \] src0 \[ \_ ABS \] \[ . свиззле \] ,</span><span class="sxs-lookup"><span data-stu-id="5f83b-106">deriv\_rtx\_coarse\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\],</span></span> |
|----------------------------------------------------------------------------|



 



| <span data-ttu-id="5f83b-107">Элемент</span><span class="sxs-lookup"><span data-stu-id="5f83b-107">Item</span></span>                                                            | <span data-ttu-id="5f83b-108">Описание</span><span class="sxs-lookup"><span data-stu-id="5f83b-108">Description</span></span>                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="5f83b-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="5f83b-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="5f83b-110">\[в \] адресе результатов операции.</span><span class="sxs-lookup"><span data-stu-id="5f83b-110">\[in\] The address of the results of the operation.</span></span><br/> |
| <span data-ttu-id="5f83b-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="5f83b-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="5f83b-112">\[в \] компонентах операции.</span><span class="sxs-lookup"><span data-stu-id="5f83b-112">\[in\] The components in the operation.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="5f83b-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="5f83b-113">Remarks</span></span>

<span data-ttu-id="5f83b-114">Эта инструкция оценивает скорость изменения содержимого каждого компонента float32 класса *src0* (POST-свиззле) с точки зрения рендертаржет x Direction (RTX) или рендертаржет y (см. статью о [наследовании \_ РТИ по \_ грубой](deriv-rty-coarse--sm5---asm-.md)цене).</span><span class="sxs-lookup"><span data-stu-id="5f83b-114">This instruction computes the rate of change of contents of each float32 component of *src0* (post-swizzle), with regard to RenderTarget x direction (rtx) or RenderTarget y direction (see [deriv\_rty\_coarse](deriv-rty-coarse--sm5---asm-.md)).</span></span> <span data-ttu-id="5f83b-115">Для каждой отметки 2x2 пикселей вычислена только одна производная пара x, y.</span><span class="sxs-lookup"><span data-stu-id="5f83b-115">Only a single x,y derivative pair is computed for each 2x2 stamp of pixels.</span></span>

<span data-ttu-id="5f83b-116">Данные в текущем вызове шейдера пикселей могут принимать или не участвовать в вычислении запрошенного производного, так как производная единица будет вычисляться только один раз на четыре 2x2.</span><span class="sxs-lookup"><span data-stu-id="5f83b-116">The data in the current pixel shader invocation may or may not participate in the calculation of the requested derivative, because the derivative will be calculated only once per 2x2 quad.</span></span> <span data-ttu-id="5f83b-117">Например, производный x может быть Дельта от верхней строки пикселя, а направление оси y ([производное \_ РТИ \_ грубое](deriv-rty-coarse--sm5---asm-.md)) может быть разностью от левого столбца пикселей.</span><span class="sxs-lookup"><span data-stu-id="5f83b-117">For example, the x derivative could be a delta from the top row of pixels, and the y direction ([deriv\_rty\_coarse](deriv-rty-coarse--sm5---asm-.md)) could be a delta from the left column of pixels.</span></span> <span data-ttu-id="5f83b-118">Точный расчет имеет поставщик оборудования.</span><span class="sxs-lookup"><span data-stu-id="5f83b-118">The exact calculation is up to the hardware vendor.</span></span> <span data-ttu-id="5f83b-119">Кроме того, нет никакой спецификации, определяющей, как четыре четырехъядерия будут выставляться или накладывается на примитив.</span><span class="sxs-lookup"><span data-stu-id="5f83b-119">There is also no specification dictating how the 2x2 quads will be aligned or tiled over a primitive.</span></span>

<span data-ttu-id="5f83b-120">Производные вычисления рассчитываются на грубом уровне, по одному разу на четыре пиксела 2x2.</span><span class="sxs-lookup"><span data-stu-id="5f83b-120">Derivatives are calculated at a coarse level, once per 2x2 pixel quad.</span></span> <span data-ttu-id="5f83b-121">Эта инструкция и [наследование \_ РТИ « \_ грубые](deriv-rty-coarse--sm5---asm-.md) » являются альтернативами, которые [наследуют \_ RTX « \_ прекрасно](deriv-rtx-fine--sm5---asm-.md) » и [наследуют \_ РТИ \_ ](deriv-rty-fine--sm5---asm-.md).</span><span class="sxs-lookup"><span data-stu-id="5f83b-121">This instruction and [deriv\_rty\_coarse](deriv-rty-coarse--sm5---asm-.md) are alternatives to [deriv\_rtx\_fine](deriv-rtx-fine--sm5---asm-.md) and [deriv\_rty\_fine](deriv-rty-fine--sm5---asm-.md).</span></span> <span data-ttu-id="5f83b-122">Эти \_ грубые и \_ точные инструкции являются заменой для **наследования \_ ртксдерив \_ РТИ** от предыдущих моделей шейдеров.</span><span class="sxs-lookup"><span data-stu-id="5f83b-122">These \_coarse and \_fine derivative instructions are a replacement for **deriv\_rtxderiv\_rty** from previous shader models .</span></span>

<span data-ttu-id="5f83b-123">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="5f83b-123">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="5f83b-124">Вершина</span><span class="sxs-lookup"><span data-stu-id="5f83b-124">Vertex</span></span> | <span data-ttu-id="5f83b-125">Поверхности</span><span class="sxs-lookup"><span data-stu-id="5f83b-125">Hull</span></span> | <span data-ttu-id="5f83b-126">Домен</span><span class="sxs-lookup"><span data-stu-id="5f83b-126">Domain</span></span> | <span data-ttu-id="5f83b-127">Геометрия</span><span class="sxs-lookup"><span data-stu-id="5f83b-127">Geometry</span></span> | <span data-ttu-id="5f83b-128">Пиксель</span><span class="sxs-lookup"><span data-stu-id="5f83b-128">Pixel</span></span> | <span data-ttu-id="5f83b-129">Вычисления</span><span class="sxs-lookup"><span data-stu-id="5f83b-129">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="5f83b-130">X</span><span class="sxs-lookup"><span data-stu-id="5f83b-130">X</span></span>     |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="5f83b-131">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="5f83b-131">Minimum Shader Model</span></span>

<span data-ttu-id="5f83b-132">Эта инструкция поддерживается в следующих моделях шейдеров:</span><span class="sxs-lookup"><span data-stu-id="5f83b-132">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="5f83b-133">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="5f83b-133">Shader Model</span></span>                                              | <span data-ttu-id="5f83b-134">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="5f83b-134">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="5f83b-135">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="5f83b-135">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="5f83b-136">да</span><span class="sxs-lookup"><span data-stu-id="5f83b-136">yes</span></span>       |
| [<span data-ttu-id="5f83b-137">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="5f83b-137">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="5f83b-138">Нет</span><span class="sxs-lookup"><span data-stu-id="5f83b-138">no</span></span>        |
| [<span data-ttu-id="5f83b-139">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="5f83b-139">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="5f83b-140">Нет</span><span class="sxs-lookup"><span data-stu-id="5f83b-140">no</span></span>        |
| [<span data-ttu-id="5f83b-141">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5f83b-141">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="5f83b-142">Нет</span><span class="sxs-lookup"><span data-stu-id="5f83b-142">no</span></span>        |
| [<span data-ttu-id="5f83b-143">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5f83b-143">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="5f83b-144">Нет</span><span class="sxs-lookup"><span data-stu-id="5f83b-144">no</span></span>        |
| [<span data-ttu-id="5f83b-145">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5f83b-145">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="5f83b-146">Нет</span><span class="sxs-lookup"><span data-stu-id="5f83b-146">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="5f83b-147">См. также</span><span class="sxs-lookup"><span data-stu-id="5f83b-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5f83b-148">Сборка Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5f83b-148">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





