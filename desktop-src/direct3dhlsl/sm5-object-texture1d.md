---
title: Texture1D
description: Texture1D
ms.assetid: 5f6fd0e4-a73e-4d13-b3a0-c884b7912581
keywords:
- Texture1D HLSL
topic_type:
- apiref
api_name:
- Texture1D
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8b8a60706ea2752109cdda9907ffe7c654efe531
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "103987005"
---
# <a name="texture1d"></a><span data-ttu-id="90ae7-104">Texture1D</span><span class="sxs-lookup"><span data-stu-id="90ae7-104">Texture1D</span></span>

<span data-ttu-id="90ae7-105">Тип одномерной текстуры ([в том виде, в котором он существует в модели шейдеров 4](dx-graphics-hlsl-to-type.md)) и переменные ресурса.</span><span class="sxs-lookup"><span data-stu-id="90ae7-105">A 1D texture type ([as it exists in Shader Model 4](dx-graphics-hlsl-to-type.md)) plus resource variables.</span></span> <span data-ttu-id="90ae7-106">Этот объект текстуры поддерживает следующие методы в дополнение к методам в модели шейдера 4.</span><span class="sxs-lookup"><span data-stu-id="90ae7-106">This texture object supports the following methods in addition to the methods in Shader Model 4.</span></span>



| <span data-ttu-id="90ae7-107">Метод</span><span class="sxs-lookup"><span data-stu-id="90ae7-107">Method</span></span>                                                                  | <span data-ttu-id="90ae7-108">Описание</span><span class="sxs-lookup"><span data-stu-id="90ae7-108">Description</span></span>                                                                                |
|-------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="90ae7-109">**GetDimensions**</span><span class="sxs-lookup"><span data-stu-id="90ae7-109">**GetDimensions**</span></span>](sm5-object-texture1d-getdimensions.md)             | <span data-ttu-id="90ae7-110">Возвращает размеры ресурсов.</span><span class="sxs-lookup"><span data-stu-id="90ae7-110">Gets the resource dimensions.</span></span>                                                              |
| [<span data-ttu-id="90ae7-111">**Загрузить**</span><span class="sxs-lookup"><span data-stu-id="90ae7-111">**Load**</span></span>](texture1d-load.md)                                          | <span data-ttu-id="90ae7-112">Считывает данные текстуры.</span><span class="sxs-lookup"><span data-stu-id="90ae7-112">Reads texture data.</span></span>                                                                        |
| <span data-ttu-id="90ae7-113">[**Оператор\[\]**](sm5-object-texture1d-operatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="90ae7-113">[**Operator\[\]**](sm5-object-texture1d-operatorindex.md)</span></span>              | <span data-ttu-id="90ae7-114">Возвращает переменную ресурса, доступную только для чтения.</span><span class="sxs-lookup"><span data-stu-id="90ae7-114">Gets a read-only resource variable.</span></span>                                                        |
| <span data-ttu-id="90ae7-115">[**MIPS. Станции\[\]\[\]**](sm5-object-texture1d-mipsoperatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="90ae7-115">[**mips.Operator\[\]\[\]**](sm5-object-texture1d-mipsoperatorindex.md)</span></span> | <span data-ttu-id="90ae7-116">Возвращает переменную ресурса, доступную только для чтения.</span><span class="sxs-lookup"><span data-stu-id="90ae7-116">Gets a read-only resource variable.</span></span>                                                        |
| [<span data-ttu-id="90ae7-117">**Пример**</span><span class="sxs-lookup"><span data-stu-id="90ae7-117">**Sample**</span></span>](texture1d-sample.md)                                      | <span data-ttu-id="90ae7-118">Выбор текстуры.</span><span class="sxs-lookup"><span data-stu-id="90ae7-118">Samples a texture.</span></span>                                                                         |
| [<span data-ttu-id="90ae7-119">**самплебиас**</span><span class="sxs-lookup"><span data-stu-id="90ae7-119">**SampleBias**</span></span>](texture1d-samplebias.md)                              | <span data-ttu-id="90ae7-120">Выбор текстуры после применения значения смещения к уровню mipmap.</span><span class="sxs-lookup"><span data-stu-id="90ae7-120">Samples a texture, after applying the bias value to the mipmap level.</span></span>                      |
| [<span data-ttu-id="90ae7-121">**самплекмп**</span><span class="sxs-lookup"><span data-stu-id="90ae7-121">**SampleCmp**</span></span>](texture1d-samplecmp.md)                                | <span data-ttu-id="90ae7-122">Выбор текстуры с использованием значения сравнения для отклонения выборок.</span><span class="sxs-lookup"><span data-stu-id="90ae7-122">Samples a texture, using a comparison value to reject samples.</span></span>                             |
| [<span data-ttu-id="90ae7-123">**SampleCmpLevelZero**</span><span class="sxs-lookup"><span data-stu-id="90ae7-123">**SampleCmpLevelZero**</span></span>](texture1d-samplecmplevelzero.md)              | <span data-ttu-id="90ae7-124">Производит выборку текстуры (только mipmap уровень 0), используя значение сравнения для отклонения выборок.</span><span class="sxs-lookup"><span data-stu-id="90ae7-124">Samples a texture (mipmap level 0 only), using a comparison value to reject samples.</span></span>       |
| [<span data-ttu-id="90ae7-125">**самплеград**</span><span class="sxs-lookup"><span data-stu-id="90ae7-125">**SampleGrad**</span></span>](texture1d-samplegrad.md)                              | <span data-ttu-id="90ae7-126">Выбор текстуры с помощью градиента, чтобы повлиять на способ вычисления расположения образца.</span><span class="sxs-lookup"><span data-stu-id="90ae7-126">Samples a texture using a gradient to influence the way the sample location is calculated.</span></span> |
| [<span data-ttu-id="90ae7-127">**SampleLevel**</span><span class="sxs-lookup"><span data-stu-id="90ae7-127">**SampleLevel**</span></span>](texture1d-samplelevel.md)                            | <span data-ttu-id="90ae7-128">Выбирает текстуру на указанном уровне mipmap.</span><span class="sxs-lookup"><span data-stu-id="90ae7-128">Samples a texture on the specified mipmap level.</span></span>                                           |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="90ae7-129">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="90ae7-129">Minimum Shader Model</span></span>

<span data-ttu-id="90ae7-130">Этот объект поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="90ae7-130">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="90ae7-131">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="90ae7-131">Shader Model</span></span>                                                                | <span data-ttu-id="90ae7-132">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="90ae7-132">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="90ae7-133">[Модели шейдера 5](d3d11-graphics-reference-sm5.md) и более поздних моделей шейдеров</span><span class="sxs-lookup"><span data-stu-id="90ae7-133">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="90ae7-134">да</span><span class="sxs-lookup"><span data-stu-id="90ae7-134">yes</span></span>       |



 

<span data-ttu-id="90ae7-135">Этот объект поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="90ae7-135">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="90ae7-136">Вершина</span><span class="sxs-lookup"><span data-stu-id="90ae7-136">Vertex</span></span> | <span data-ttu-id="90ae7-137">Поверхности</span><span class="sxs-lookup"><span data-stu-id="90ae7-137">Hull</span></span> | <span data-ttu-id="90ae7-138">Домен</span><span class="sxs-lookup"><span data-stu-id="90ae7-138">Domain</span></span> | <span data-ttu-id="90ae7-139">Геометрия</span><span class="sxs-lookup"><span data-stu-id="90ae7-139">Geometry</span></span> | <span data-ttu-id="90ae7-140">Пиксель</span><span class="sxs-lookup"><span data-stu-id="90ae7-140">Pixel</span></span> | <span data-ttu-id="90ae7-141">Вычисления</span><span class="sxs-lookup"><span data-stu-id="90ae7-141">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="90ae7-142">x</span><span class="sxs-lookup"><span data-stu-id="90ae7-142">x</span></span>      | <span data-ttu-id="90ae7-143">x</span><span class="sxs-lookup"><span data-stu-id="90ae7-143">x</span></span>    | <span data-ttu-id="90ae7-144">x</span><span class="sxs-lookup"><span data-stu-id="90ae7-144">x</span></span>      | <span data-ttu-id="90ae7-145">x</span><span class="sxs-lookup"><span data-stu-id="90ae7-145">x</span></span>        | <span data-ttu-id="90ae7-146">x</span><span class="sxs-lookup"><span data-stu-id="90ae7-146">x</span></span>     | <span data-ttu-id="90ae7-147">x</span><span class="sxs-lookup"><span data-stu-id="90ae7-147">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="90ae7-148">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="90ae7-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90ae7-149">Объекты модели шейдеров 5</span><span class="sxs-lookup"><span data-stu-id="90ae7-149">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 




