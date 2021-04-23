---
title: deriv_rtx (SM4-ASM)
description: Интенсивность изменения содержимого каждого компонента float32 src0 (POST-свиззле) по отношению к Рендертаржет x Direction (RTX) или Рендертаржет y.
ms.assetid: 2438DB36-C348-4854-AE1B-EC3C890B0B42
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21d4543805c02cf70d9c6b7856461c427788f616
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104412143"
---
# <a name="deriv_rtx-sm4---asm"></a><span data-ttu-id="eb620-103">наследование \_ RTX (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="eb620-103">deriv\_rtx (sm4 - asm)</span></span>

<span data-ttu-id="eb620-104">Интенсивность изменения содержимого каждого компонента float32 *src0* (POST-свиззле) по отношению к рендертаржет x Direction (RTX) или рендертаржет y.</span><span class="sxs-lookup"><span data-stu-id="eb620-104">Rate of change of contents of each float32 component of *src0* (post-swizzle), with regard to RenderTarget x direction (rtx) or RenderTarget y direction.</span></span>



| <span data-ttu-id="eb620-105">наследование \_ RTX \[ \_ \] \[ . Маска \] , \[ - \] src0 \[ \_ ABS \] \[ . свиззле \] ,</span><span class="sxs-lookup"><span data-stu-id="eb620-105">deriv\_rtx\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\],</span></span> |
|--------------------------------------------------------------------|



 



| <span data-ttu-id="eb620-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="eb620-106">Item</span></span>                                                            | <span data-ttu-id="eb620-107">Описание</span><span class="sxs-lookup"><span data-stu-id="eb620-107">Description</span></span>                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="eb620-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="eb620-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="eb620-109">\[в \] адресе результата операции.</span><span class="sxs-lookup"><span data-stu-id="eb620-109">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="eb620-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="eb620-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="eb620-111">\[в \] компоненте операции.</span><span class="sxs-lookup"><span data-stu-id="eb620-111">\[in\] The component in the operation.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="eb620-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="eb620-112">Remarks</span></span>

<span data-ttu-id="eb620-113">Для каждой отметки 2x2 пикселей вычислена только одна производная пара x, y.</span><span class="sxs-lookup"><span data-stu-id="eb620-113">Only a single x,y derivative pair is computed for each 2x2 stamp of pixels.</span></span>

<span data-ttu-id="eb620-114">Эта операция зависит от оборудования.</span><span class="sxs-lookup"><span data-stu-id="eb620-114">This operation is hardware dependent.</span></span>

<span data-ttu-id="eb620-115">Ссылка на реализацию средства программной прорисовки для треугольников:</span><span class="sxs-lookup"><span data-stu-id="eb620-115">Reference rasterizer implementation for triangles:</span></span>

-   <span data-ttu-id="eb620-116">Шейдер пикселей всегда запускает шейдер на четырех пикселях в локкстеп (даже через Управление потоком, маскирование отключенных пикселов).</span><span class="sxs-lookup"><span data-stu-id="eb620-116">Pixel Shader always runs Shader over 2x2 quad of pixels in lockstep (even through flow control, masking disabled pixels).</span></span>
-   <span data-ttu-id="eb620-117">Четыре всегда имеют даже пронумерованные координаты пикселей (x и y) для верхнего левого пикселя.</span><span class="sxs-lookup"><span data-stu-id="eb620-117">Quads always have even numbered pixel coordinates (both x and y) for top-left pixel.</span></span>
-   <span data-ttu-id="eb620-118">Фиктивные Пиксели выключаются из примитивов, если примитив слишком мал для заполнения 2x2 четырех.</span><span class="sxs-lookup"><span data-stu-id="eb620-118">Dummy pixels run off primitive if primitive is too small to fill a 2x2 quad.</span></span>
-   <span data-ttu-id="eb620-119">**наследование \_ RTX** вычислено при первом выборе 2 пикселя: текущего пикселя и другого пикселя с той же координатой y из четырех.</span><span class="sxs-lookup"><span data-stu-id="eb620-119">**deriv\_rtx** is computed by first choosing 2 pixels: the current pixel and the other pixel with the same y coordinate from the quad.</span></span> <span data-ttu-id="eb620-120">Затем результат вычисляется следующим образом: *src0*(нечетный x пиксель) — *src0*(даже x пиксель) \[ для каждого компонента\]</span><span class="sxs-lookup"><span data-stu-id="eb620-120">Then, the result is calculated as: *src0*(odd x pixel) - *src0*(even x pixel) \[per-component\]</span></span>
-   <span data-ttu-id="eb620-121">[наследование \_ РТИ](deriv-rty--sm4---asm-.md) вычислено при первом выборе 2 пикселя: текущего пикселя и другого пикселя с той же координатой x из четырех.</span><span class="sxs-lookup"><span data-stu-id="eb620-121">[deriv\_rty](deriv-rty--sm4---asm-.md) is computed by first choosing 2 pixels: the current pixel and the other pixel with the same x coordinate from the quad.</span></span> <span data-ttu-id="eb620-122">Затем результат вычисляется следующим образом: *src0*(нечетный y пиксель) — *src0*(даже y пиксель) \[ для каждого компонента.\]</span><span class="sxs-lookup"><span data-stu-id="eb620-122">Then, the result is calculated as: *src0*(odd y pixel) - *src0*(even y pixel) \[per-component\]</span></span>

<span data-ttu-id="eb620-123">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="eb620-123">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="eb620-124">Вершинный построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="eb620-124">Vertex Shader</span></span> | <span data-ttu-id="eb620-125">Шейдер геометрии</span><span class="sxs-lookup"><span data-stu-id="eb620-125">Geometry Shader</span></span> | <span data-ttu-id="eb620-126">Построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="eb620-126">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
|               |                 | <span data-ttu-id="eb620-127">x</span><span class="sxs-lookup"><span data-stu-id="eb620-127">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="eb620-128">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="eb620-128">Minimum Shader Model</span></span>

<span data-ttu-id="eb620-129">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="eb620-129">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="eb620-130">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="eb620-130">Shader Model</span></span>                                              | <span data-ttu-id="eb620-131">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="eb620-131">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="eb620-132">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="eb620-132">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="eb620-133">да</span><span class="sxs-lookup"><span data-stu-id="eb620-133">yes</span></span>       |
| [<span data-ttu-id="eb620-134">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="eb620-134">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="eb620-135">да</span><span class="sxs-lookup"><span data-stu-id="eb620-135">yes</span></span>       |
| [<span data-ttu-id="eb620-136">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="eb620-136">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="eb620-137">да</span><span class="sxs-lookup"><span data-stu-id="eb620-137">yes</span></span>       |
| [<span data-ttu-id="eb620-138">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="eb620-138">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="eb620-139">Нет</span><span class="sxs-lookup"><span data-stu-id="eb620-139">no</span></span>        |
| [<span data-ttu-id="eb620-140">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="eb620-140">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="eb620-141">Нет</span><span class="sxs-lookup"><span data-stu-id="eb620-141">no</span></span>        |
| [<span data-ttu-id="eb620-142">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="eb620-142">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="eb620-143">Нет</span><span class="sxs-lookup"><span data-stu-id="eb620-143">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="eb620-144">См. также</span><span class="sxs-lookup"><span data-stu-id="eb620-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eb620-145">Сборка Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="eb620-145">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





