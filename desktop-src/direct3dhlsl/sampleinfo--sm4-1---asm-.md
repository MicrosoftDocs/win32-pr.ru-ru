---
title: самплеинфо (SM 4.1-ASM)
description: Запрашивает количество выборок в заданном представлении ресурсов шейдера или в средство программной прорисовки.
ms.assetid: 1F0968D7-01E9-4213-9F83-172B88374C3C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d307dbc8c79618a6401737874a9f6e060a899ccc
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "103890047"
---
# <a name="sampleinfo-sm41---asm"></a><span data-ttu-id="a865a-103">самплеинфо (SM 4.1-ASM)</span><span class="sxs-lookup"><span data-stu-id="a865a-103">sampleinfo (sm4.1 - asm)</span></span>

<span data-ttu-id="a865a-104">Запрашивает количество выборок в заданном представлении ресурсов шейдера или в средство программной прорисовки.</span><span class="sxs-lookup"><span data-stu-id="a865a-104">Queries the number of samples in a given shader resource view or in the rasterizer.</span></span>



| <span data-ttu-id="a865a-105">\[\_uint \] dest \[ . Mask \] , сркресаурце \[ . свиззле\]</span><span class="sxs-lookup"><span data-stu-id="a865a-105">\[\_uint\] dest\[.mask\], srcResource\[.swizzle\]</span></span> |
|---------------------------------------------------|



 



| <span data-ttu-id="a865a-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="a865a-106">Item</span></span>                                                                                                               | <span data-ttu-id="a865a-107">Описание</span><span class="sxs-lookup"><span data-stu-id="a865a-107">Description</span></span>                                                    |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="a865a-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="a865a-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/>                                                    | <span data-ttu-id="a865a-109">\[в \] адресе результатов операции.</span><span class="sxs-lookup"><span data-stu-id="a865a-109">\[in\] The address of the results of the operation.</span></span><br/> |
| <span data-ttu-id="a865a-110"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*сркресаурце*</span><span class="sxs-lookup"><span data-stu-id="a865a-110"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span></span><br/> | <span data-ttu-id="a865a-111">\[в \] ресурсе шейдера.</span><span class="sxs-lookup"><span data-stu-id="a865a-111">\[in\] The shader resource.</span></span><br/>                         |



 

## <a name="remarks"></a><span data-ttu-id="a865a-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="a865a-112">Remarks</span></span>

<span data-ttu-id="a865a-113">Эта инструкция возвращает число выборок для данного ресурса или средства программной прорисовки.</span><span class="sxs-lookup"><span data-stu-id="a865a-113">This instruction returns the number of samples for the given resource or the rasterizer.</span></span> <span data-ttu-id="a865a-114">Он действителен только для ресурсов, которые могут быть загружены с помощью [**ld2dms**](ld2dms--sm4-1---asm-.md) , если средство программной прорисовки не задано как *сркресаурце*.</span><span class="sxs-lookup"><span data-stu-id="a865a-114">It is valid only for resources that can be loaded using [**ld2dms**](ld2dms--sm4-1---asm-.md) unless the rasterizer is specified as *srcResource*.</span></span> <span data-ttu-id="a865a-115">*сркресаурце* может быть t \# -регистром (представление ресурсов шейдера) или регистром средства прорисовки.</span><span class="sxs-lookup"><span data-stu-id="a865a-115">*srcResource* could be a t\# register (a shader resource view) or a rasterizer register.</span></span>

<span data-ttu-id="a865a-116">Инструкция выполняет вычисление вектора (SampleCount, 0, 0, 0).</span><span class="sxs-lookup"><span data-stu-id="a865a-116">The instruction computes the vector (SampleCount,0,0,0).</span></span>

<span data-ttu-id="a865a-117">Свиззле On *сркресаурце* позволяет свиззлед возвращаемые значения произвольно, прежде чем они записываются в место назначения.</span><span class="sxs-lookup"><span data-stu-id="a865a-117">The swizzle on *srcResource* allows the returned values to be swizzled arbitrarily before they are written to the destination.</span></span> <span data-ttu-id="a865a-118">Возвращаемое значение является плавающей запятой, если только \_ не используется модификатор uint. в этом случае возвращаемое значение является целым числом.</span><span class="sxs-lookup"><span data-stu-id="a865a-118">The returned value is floating point, unless the \_uint modifier is used, in which case the returned value is integer.</span></span> <span data-ttu-id="a865a-119">Если нет ресурса, привязанного к указанному слоту, возвращается значение 0.</span><span class="sxs-lookup"><span data-stu-id="a865a-119">If there is no resource bound to the specified slot, 0 is returned.</span></span>

<span data-ttu-id="a865a-120">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="a865a-120">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="a865a-121">Вершинный построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="a865a-121">Vertex Shader</span></span> | <span data-ttu-id="a865a-122">Шейдер геометрии</span><span class="sxs-lookup"><span data-stu-id="a865a-122">Geometry Shader</span></span> | <span data-ttu-id="a865a-123">Построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="a865a-123">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="a865a-124">X</span><span class="sxs-lookup"><span data-stu-id="a865a-124">X</span></span>             | <span data-ttu-id="a865a-125">X</span><span class="sxs-lookup"><span data-stu-id="a865a-125">X</span></span>               | <span data-ttu-id="a865a-126">x</span><span class="sxs-lookup"><span data-stu-id="a865a-126">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="a865a-127">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="a865a-127">Minimum Shader Model</span></span>

<span data-ttu-id="a865a-128">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="a865a-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="a865a-129">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="a865a-129">Shader Model</span></span>                                              | <span data-ttu-id="a865a-130">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="a865a-130">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="a865a-131">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="a865a-131">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="a865a-132">да</span><span class="sxs-lookup"><span data-stu-id="a865a-132">yes</span></span>       |
| [<span data-ttu-id="a865a-133">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="a865a-133">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="a865a-134">да</span><span class="sxs-lookup"><span data-stu-id="a865a-134">yes</span></span>       |
| [<span data-ttu-id="a865a-135">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="a865a-135">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="a865a-136">Нет</span><span class="sxs-lookup"><span data-stu-id="a865a-136">no</span></span>        |
| [<span data-ttu-id="a865a-137">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a865a-137">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="a865a-138">Нет</span><span class="sxs-lookup"><span data-stu-id="a865a-138">no</span></span>        |
| [<span data-ttu-id="a865a-139">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a865a-139">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="a865a-140">Нет</span><span class="sxs-lookup"><span data-stu-id="a865a-140">no</span></span>        |
| [<span data-ttu-id="a865a-141">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a865a-141">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="a865a-142">Нет</span><span class="sxs-lookup"><span data-stu-id="a865a-142">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="a865a-143">См. также</span><span class="sxs-lookup"><span data-stu-id="a865a-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a865a-144">Сборка Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a865a-144">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





