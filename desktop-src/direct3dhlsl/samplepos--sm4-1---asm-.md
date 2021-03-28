---
title: самплепос (SM 4.1-ASM)
description: Запрашивает расположение образца в заданном представлении ресурсов шейдера или в средство программной прорисовки.
ms.assetid: 5A53B342-3A1D-4016-ABF2-CA6236D562C9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 910a542dafddb8b855e218f8702c746220780d6e
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104412224"
---
# <a name="samplepos-sm41---asm"></a><span data-ttu-id="616a1-103">самплепос (SM 4.1-ASM)</span><span class="sxs-lookup"><span data-stu-id="616a1-103">samplepos (sm4.1 - asm)</span></span>

<span data-ttu-id="616a1-104">Запрашивает расположение образца в заданном представлении ресурсов шейдера или в средство программной прорисовки.</span><span class="sxs-lookup"><span data-stu-id="616a1-104">Queries the position of a sample in a given shader resource view or in the rasterizer.</span></span>



| <span data-ttu-id="616a1-105">самплепос dest \[ . Mask \] , сркресаурце \[ . свиззле \] , sampleIndex (скалярный операнд)</span><span class="sxs-lookup"><span data-stu-id="616a1-105">samplepos dest\[.mask\], srcResource\[.swizzle\], sampleIndex (scalar operand)</span></span> |
|--------------------------------------------------------------------------------|



 



| <span data-ttu-id="616a1-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="616a1-106">Item</span></span>                                                                                                               | <span data-ttu-id="616a1-107">Описание</span><span class="sxs-lookup"><span data-stu-id="616a1-107">Description</span></span>                                                    |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="616a1-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="616a1-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/>                                                    | <span data-ttu-id="616a1-109">\[в \] адресе результатов операции.</span><span class="sxs-lookup"><span data-stu-id="616a1-109">\[in\] The address of the results of the operation.</span></span><br/> |
| <span data-ttu-id="616a1-110"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*сркресаурце*</span><span class="sxs-lookup"><span data-stu-id="616a1-110"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span></span><br/> | <span data-ttu-id="616a1-111">\[в \] ресурсе шейдера.</span><span class="sxs-lookup"><span data-stu-id="616a1-111">\[in\] The shader resource.</span></span><br/>                         |
| <span data-ttu-id="616a1-112"><span id="sampleIndex"></span><span id="sampleindex"></span><span id="SAMPLEINDEX"></span>*sampleIndex*</span><span class="sxs-lookup"><span data-stu-id="616a1-112"><span id="sampleIndex"></span><span id="sampleindex"></span><span id="SAMPLEINDEX"></span>*sampleIndex*</span></span><br/> | <span data-ttu-id="616a1-113">\[в \] индексе образца.</span><span class="sxs-lookup"><span data-stu-id="616a1-113">\[in\] The index of the sample.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="616a1-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="616a1-114">Remarks</span></span>

<span data-ttu-id="616a1-115">Эта инструкция возвращает 2D-пример расположения образца *sampleIndex* для заданного ресурса.</span><span class="sxs-lookup"><span data-stu-id="616a1-115">This instruction returns the 2D sample position of sample *sampleIndex* for the given resource.</span></span> <span data-ttu-id="616a1-116">Он действителен только для ресурсов, которые могут быть загружены с помощью [**ld2dms**](ld2dms--sm4-1---asm-.md) , если средство программной прорисовки не задано как *сркресаурце*.</span><span class="sxs-lookup"><span data-stu-id="616a1-116">It is valid only for resources that can be loaded using [**ld2dms**](ld2dms--sm4-1---asm-.md) unless the rasterizer is specified as *srcResource*.</span></span>

<span data-ttu-id="616a1-117">*сркресаурце* может быть t \# -регистром (представление ресурсов шейдера) или регистром средства прорисовки.</span><span class="sxs-lookup"><span data-stu-id="616a1-117">*srcResource* can be a t\# register (a shader resource view) or a rasterizer register.</span></span>

<span data-ttu-id="616a1-118">Инструкция выполняет вычисление вектора с плавающей запятой (Кспоситион, Ипоситион, 0, 0).</span><span class="sxs-lookup"><span data-stu-id="616a1-118">The instruction computes the floating point vector (Xposition, Yposition, 0, 0).</span></span>

<span data-ttu-id="616a1-119">Свиззле On *сркресаурце* позволяет свиззлед возвращаемые значения произвольно, прежде чем они записываются в место назначения.</span><span class="sxs-lookup"><span data-stu-id="616a1-119">The swizzle on *srcResource* allows the returned values to be swizzled arbitrarily before they are written to the destination.</span></span> <span data-ttu-id="616a1-120">Положение образца определяется относительно центра пикселя на основе системы координат пикселей.</span><span class="sxs-lookup"><span data-stu-id="616a1-120">The sample position is relative to the pixel's center, based on the Pixel Coordinate System.</span></span>

<span data-ttu-id="616a1-121">Если *sampleIndex* выходит за пределы допустимого диапазона, возвращается нуль-вектор.</span><span class="sxs-lookup"><span data-stu-id="616a1-121">If *sampleIndex* is out of bounds a zero vector is returned.</span></span> <span data-ttu-id="616a1-122">Если нет ресурса, привязанного к указанному слоту, возвращается значение 0.</span><span class="sxs-lookup"><span data-stu-id="616a1-122">If there is no resource bound to the specified slot, 0 is returned.</span></span>

<span data-ttu-id="616a1-123">**самплепос** можно использовать для таких целей, как пользовательские разрешения в коде шейдера.</span><span class="sxs-lookup"><span data-stu-id="616a1-123">**samplepos** can be used for things like custom resolves in shader code.</span></span>

<span data-ttu-id="616a1-124">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="616a1-124">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="616a1-125">Вершинный построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="616a1-125">Vertex Shader</span></span> | <span data-ttu-id="616a1-126">Шейдер геометрии</span><span class="sxs-lookup"><span data-stu-id="616a1-126">Geometry Shader</span></span> | <span data-ttu-id="616a1-127">Построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="616a1-127">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
|               |                 | <span data-ttu-id="616a1-128">x</span><span class="sxs-lookup"><span data-stu-id="616a1-128">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="616a1-129">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="616a1-129">Minimum Shader Model</span></span>

<span data-ttu-id="616a1-130">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="616a1-130">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="616a1-131">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="616a1-131">Shader Model</span></span>                                              | <span data-ttu-id="616a1-132">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="616a1-132">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="616a1-133">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="616a1-133">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="616a1-134">да</span><span class="sxs-lookup"><span data-stu-id="616a1-134">yes</span></span>       |
| [<span data-ttu-id="616a1-135">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="616a1-135">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="616a1-136">да</span><span class="sxs-lookup"><span data-stu-id="616a1-136">yes</span></span>       |
| [<span data-ttu-id="616a1-137">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="616a1-137">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="616a1-138">Нет</span><span class="sxs-lookup"><span data-stu-id="616a1-138">no</span></span>        |
| [<span data-ttu-id="616a1-139">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="616a1-139">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="616a1-140">Нет</span><span class="sxs-lookup"><span data-stu-id="616a1-140">no</span></span>        |
| [<span data-ttu-id="616a1-141">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="616a1-141">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="616a1-142">Нет</span><span class="sxs-lookup"><span data-stu-id="616a1-142">no</span></span>        |
| [<span data-ttu-id="616a1-143">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="616a1-143">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="616a1-144">Нет</span><span class="sxs-lookup"><span data-stu-id="616a1-144">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="616a1-145">См. также</span><span class="sxs-lookup"><span data-stu-id="616a1-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="616a1-146">Сборка Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="616a1-146">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





