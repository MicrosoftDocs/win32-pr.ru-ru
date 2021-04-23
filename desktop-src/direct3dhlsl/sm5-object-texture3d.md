---
title: Texture3D
description: Texture3D
ms.assetid: a3640aac-b503-4716-8bc6-105e96bea03c
keywords:
- Texture3D HLSL
topic_type:
- apiref
api_name:
- Texture3D
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 50b12f2184f6eca0fd7a68feb3e96d8d6fc65a61
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104068882"
---
# <a name="texture3d"></a><span data-ttu-id="87470-104">Texture3D</span><span class="sxs-lookup"><span data-stu-id="87470-104">Texture3D</span></span>

<span data-ttu-id="87470-105">Тип Texture3D ([как он существует в модели шейдеров 4](dx-graphics-hlsl-to-type.md)) и переменные ресурсов.</span><span class="sxs-lookup"><span data-stu-id="87470-105">Texture3D type ([as it exists in Shader Model 4](dx-graphics-hlsl-to-type.md)) plus resource variables.</span></span> <span data-ttu-id="87470-106">Этот объект текстуры поддерживает следующие методы в дополнение к методам в модели шейдера 4.</span><span class="sxs-lookup"><span data-stu-id="87470-106">This texture object supports the following methods in addition to the methods in Shader Model 4.</span></span>



| <span data-ttu-id="87470-107">Метод</span><span class="sxs-lookup"><span data-stu-id="87470-107">Method</span></span>                                                                  | <span data-ttu-id="87470-108">Описание</span><span class="sxs-lookup"><span data-stu-id="87470-108">Description</span></span>                                                                                |
|-------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="87470-109">**GetDimensions**</span><span class="sxs-lookup"><span data-stu-id="87470-109">**GetDimensions**</span></span>](sm5-object-texture3d-getdimensions.md)             | <span data-ttu-id="87470-110">Возвращает размеры ресурсов.</span><span class="sxs-lookup"><span data-stu-id="87470-110">Gets the resource dimensions.</span></span>                                                              |
| [<span data-ttu-id="87470-111">**Загрузить**</span><span class="sxs-lookup"><span data-stu-id="87470-111">**Load**</span></span>](texture3d-load.md)                                          | <span data-ttu-id="87470-112">Считывает данные текстуры.</span><span class="sxs-lookup"><span data-stu-id="87470-112">Reads texture data.</span></span>                                                                        |
| <span data-ttu-id="87470-113">[**MIPS. Станции\[\]\[\]**](sm5-object-texture3d-mipsoperatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="87470-113">[**mips.Operator\[\]\[\]**](sm5-object-texture3d-mipsoperatorindex.md)</span></span> | <span data-ttu-id="87470-114">Возвращает переменную ресурса, доступную только для чтения.</span><span class="sxs-lookup"><span data-stu-id="87470-114">Gets a read-only resource variable.</span></span>                                                        |
| <span data-ttu-id="87470-115">[**Оператор\[\]**](sm5-object-texture3d-operatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="87470-115">[**Operator\[\]**](sm5-object-texture3d-operatorindex.md)</span></span>              | <span data-ttu-id="87470-116">Возвращает переменную ресурса, доступную только для чтения.</span><span class="sxs-lookup"><span data-stu-id="87470-116">Gets a read-only resource variable.</span></span>                                                        |
| [<span data-ttu-id="87470-117">**Пример**</span><span class="sxs-lookup"><span data-stu-id="87470-117">**Sample**</span></span>](texture3d-sample.md)                                      | <span data-ttu-id="87470-118">Выбор текстуры.</span><span class="sxs-lookup"><span data-stu-id="87470-118">Samples a texture.</span></span>                                                                         |
| [<span data-ttu-id="87470-119">**самплебиас**</span><span class="sxs-lookup"><span data-stu-id="87470-119">**SampleBias**</span></span>](texture3d-samplebias.md)                              | <span data-ttu-id="87470-120">Выбор текстуры после применения значения смещения к уровню mipmap.</span><span class="sxs-lookup"><span data-stu-id="87470-120">Samples a texture, after applying the bias value to the mipmap level.</span></span>                      |
| [<span data-ttu-id="87470-121">**самплеград**</span><span class="sxs-lookup"><span data-stu-id="87470-121">**SampleGrad**</span></span>](texture3d-samplegrad.md)                              | <span data-ttu-id="87470-122">Выбор текстуры с помощью градиента, чтобы повлиять на способ вычисления расположения образца.</span><span class="sxs-lookup"><span data-stu-id="87470-122">Samples a texture using a gradient to influence the way the sample location is calculated.</span></span> |
| [<span data-ttu-id="87470-123">**SampleLevel**</span><span class="sxs-lookup"><span data-stu-id="87470-123">**SampleLevel**</span></span>](texture3d-samplelevel.md)                            | <span data-ttu-id="87470-124">Выбирает текстуру на указанном уровне mipmap.</span><span class="sxs-lookup"><span data-stu-id="87470-124">Samples a texture on the specified mipmap level.</span></span>                                           |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="87470-125">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="87470-125">Minimum Shader Model</span></span>

<span data-ttu-id="87470-126">Этот объект поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="87470-126">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="87470-127">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="87470-127">Shader Model</span></span>                                                                | <span data-ttu-id="87470-128">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="87470-128">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="87470-129">[Модели шейдера 5](d3d11-graphics-reference-sm5.md) и более поздних моделей шейдеров</span><span class="sxs-lookup"><span data-stu-id="87470-129">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="87470-130">да</span><span class="sxs-lookup"><span data-stu-id="87470-130">yes</span></span>       |



 

<span data-ttu-id="87470-131">Этот объект поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="87470-131">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="87470-132">Вершина</span><span class="sxs-lookup"><span data-stu-id="87470-132">Vertex</span></span> | <span data-ttu-id="87470-133">Поверхности</span><span class="sxs-lookup"><span data-stu-id="87470-133">Hull</span></span> | <span data-ttu-id="87470-134">Домен</span><span class="sxs-lookup"><span data-stu-id="87470-134">Domain</span></span> | <span data-ttu-id="87470-135">Геометрия</span><span class="sxs-lookup"><span data-stu-id="87470-135">Geometry</span></span> | <span data-ttu-id="87470-136">Пиксель</span><span class="sxs-lookup"><span data-stu-id="87470-136">Pixel</span></span> | <span data-ttu-id="87470-137">Вычисления</span><span class="sxs-lookup"><span data-stu-id="87470-137">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="87470-138">x</span><span class="sxs-lookup"><span data-stu-id="87470-138">x</span></span>      | <span data-ttu-id="87470-139">x</span><span class="sxs-lookup"><span data-stu-id="87470-139">x</span></span>    | <span data-ttu-id="87470-140">x</span><span class="sxs-lookup"><span data-stu-id="87470-140">x</span></span>      | <span data-ttu-id="87470-141">x</span><span class="sxs-lookup"><span data-stu-id="87470-141">x</span></span>        | <span data-ttu-id="87470-142">x</span><span class="sxs-lookup"><span data-stu-id="87470-142">x</span></span>     | <span data-ttu-id="87470-143">x</span><span class="sxs-lookup"><span data-stu-id="87470-143">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="87470-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="87470-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87470-145">Объекты модели шейдеров 5</span><span class="sxs-lookup"><span data-stu-id="87470-145">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 




