---
title: Texture1DArray
description: Texture1DArray
ms.assetid: 3d793423-3d79-48c1-aa78-f9d93b79e0b6
keywords:
- Texture1DArray HLSL
topic_type:
- apiref
api_name:
- Texture1DArray
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 39cea5692e29ead74ba20c4a35ab8d43a1b19d42
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104069112"
---
# <a name="texture1darray"></a><span data-ttu-id="35dc6-104">Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="35dc6-104">Texture1DArray</span></span>

<span data-ttu-id="35dc6-105">Тип Texture1DArray ([как он существует в модели шейдеров 4](dx-graphics-hlsl-to-type.md)) и переменные ресурсов.</span><span class="sxs-lookup"><span data-stu-id="35dc6-105">Texture1DArray type ([as it exists in Shader Model 4](dx-graphics-hlsl-to-type.md)) plus resource variables.</span></span> <span data-ttu-id="35dc6-106">Этот объект текстуры поддерживает следующие методы в дополнение к методам в модели шейдера 4.</span><span class="sxs-lookup"><span data-stu-id="35dc6-106">This texture object supports the following methods in addition to the methods in Shader Model 4.</span></span>



| <span data-ttu-id="35dc6-107">Метод</span><span class="sxs-lookup"><span data-stu-id="35dc6-107">Method</span></span>                                                                       | <span data-ttu-id="35dc6-108">Описание</span><span class="sxs-lookup"><span data-stu-id="35dc6-108">Description</span></span>                                                                                |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="35dc6-109">**GetDimensions**</span><span class="sxs-lookup"><span data-stu-id="35dc6-109">**GetDimensions**</span></span>](sm5-object-texture1darray-getdimensions.md)             | <span data-ttu-id="35dc6-110">Возвращает размеры ресурсов.</span><span class="sxs-lookup"><span data-stu-id="35dc6-110">Gets the resource dimensions.</span></span>                                                              |
| [<span data-ttu-id="35dc6-111">**Загрузить**</span><span class="sxs-lookup"><span data-stu-id="35dc6-111">**Load**</span></span>](texture1darray-load.md)                                          | <span data-ttu-id="35dc6-112">Считывает данные текстуры.</span><span class="sxs-lookup"><span data-stu-id="35dc6-112">Reads texture data.</span></span>                                                                        |
| <span data-ttu-id="35dc6-113">[**MIPS. Станции\[\]\[\]**](sm5-object-texture1darray-mipsoperatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="35dc6-113">[**mips.Operator\[\]\[\]**](sm5-object-texture1darray-mipsoperatorindex.md)</span></span> | <span data-ttu-id="35dc6-114">Возвращает переменную ресурса, доступную только для чтения.</span><span class="sxs-lookup"><span data-stu-id="35dc6-114">Gets a read-only resource variable.</span></span>                                                        |
| <span data-ttu-id="35dc6-115">[**Оператор\[\]**](sm5-object-texture1darray-operatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="35dc6-115">[**Operator\[\]**](sm5-object-texture1darray-operatorindex.md)</span></span>              | <span data-ttu-id="35dc6-116">Возвращает переменную ресурса, доступную только для чтения.</span><span class="sxs-lookup"><span data-stu-id="35dc6-116">Gets a read-only resource variable.</span></span>                                                        |
| [<span data-ttu-id="35dc6-117">**Пример**</span><span class="sxs-lookup"><span data-stu-id="35dc6-117">**Sample**</span></span>](texture1darray-sample.md)                                      | <span data-ttu-id="35dc6-118">Выбор текстуры.</span><span class="sxs-lookup"><span data-stu-id="35dc6-118">Samples a texture.</span></span>                                                                         |
| [<span data-ttu-id="35dc6-119">**самплебиас**</span><span class="sxs-lookup"><span data-stu-id="35dc6-119">**SampleBias**</span></span>](texture1darray-samplebias.md)                              | <span data-ttu-id="35dc6-120">Выбор текстуры после применения значения смещения к уровню mipmap.</span><span class="sxs-lookup"><span data-stu-id="35dc6-120">Samples a texture, after applying the bias value to the mipmap level.</span></span>                      |
| [<span data-ttu-id="35dc6-121">**самплекмп**</span><span class="sxs-lookup"><span data-stu-id="35dc6-121">**SampleCmp**</span></span>](texture1darray-samplecmp.md)                                | <span data-ttu-id="35dc6-122">Выбор текстуры с использованием значения сравнения для отклонения выборок.</span><span class="sxs-lookup"><span data-stu-id="35dc6-122">Samples a texture, using a comparison value to reject samples.</span></span>                             |
| [<span data-ttu-id="35dc6-123">**SampleCmpLevelZero**</span><span class="sxs-lookup"><span data-stu-id="35dc6-123">**SampleCmpLevelZero**</span></span>](texture1darray-samplecmplevelzero.md)              | <span data-ttu-id="35dc6-124">Производит выборку текстуры (только mipmap уровень 0), используя значение сравнения для отклонения выборок.</span><span class="sxs-lookup"><span data-stu-id="35dc6-124">Samples a texture (mipmap level 0 only), using a comparison value to reject samples.</span></span>       |
| [<span data-ttu-id="35dc6-125">**самплеград**</span><span class="sxs-lookup"><span data-stu-id="35dc6-125">**SampleGrad**</span></span>](texture1darray-samplegrad.md)                              | <span data-ttu-id="35dc6-126">Выбор текстуры с помощью градиента, чтобы повлиять на способ вычисления расположения образца.</span><span class="sxs-lookup"><span data-stu-id="35dc6-126">Samples a texture using a gradient to influence the way the sample location is calculated.</span></span> |
| [<span data-ttu-id="35dc6-127">**SampleLevel**</span><span class="sxs-lookup"><span data-stu-id="35dc6-127">**SampleLevel**</span></span>](texture1darray-samplelevel.md)                            | <span data-ttu-id="35dc6-128">Выбирает текстуру на указанном уровне mipmap.</span><span class="sxs-lookup"><span data-stu-id="35dc6-128">Samples a texture on the specified mipmap level.</span></span>                                           |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="35dc6-129">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="35dc6-129">Minimum Shader Model</span></span>

<span data-ttu-id="35dc6-130">Этот объект поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="35dc6-130">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="35dc6-131">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="35dc6-131">Shader Model</span></span>                                                                | <span data-ttu-id="35dc6-132">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="35dc6-132">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="35dc6-133">[Модели шейдера 5](d3d11-graphics-reference-sm5.md) и более поздних моделей шейдеров</span><span class="sxs-lookup"><span data-stu-id="35dc6-133">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="35dc6-134">да</span><span class="sxs-lookup"><span data-stu-id="35dc6-134">yes</span></span>       |



 

<span data-ttu-id="35dc6-135">Этот объект поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="35dc6-135">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="35dc6-136">Вершина</span><span class="sxs-lookup"><span data-stu-id="35dc6-136">Vertex</span></span> | <span data-ttu-id="35dc6-137">Поверхности</span><span class="sxs-lookup"><span data-stu-id="35dc6-137">Hull</span></span> | <span data-ttu-id="35dc6-138">Домен</span><span class="sxs-lookup"><span data-stu-id="35dc6-138">Domain</span></span> | <span data-ttu-id="35dc6-139">Геометрия</span><span class="sxs-lookup"><span data-stu-id="35dc6-139">Geometry</span></span> | <span data-ttu-id="35dc6-140">Пиксель</span><span class="sxs-lookup"><span data-stu-id="35dc6-140">Pixel</span></span> | <span data-ttu-id="35dc6-141">Вычисления</span><span class="sxs-lookup"><span data-stu-id="35dc6-141">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="35dc6-142">x</span><span class="sxs-lookup"><span data-stu-id="35dc6-142">x</span></span>      | <span data-ttu-id="35dc6-143">x</span><span class="sxs-lookup"><span data-stu-id="35dc6-143">x</span></span>    | <span data-ttu-id="35dc6-144">x</span><span class="sxs-lookup"><span data-stu-id="35dc6-144">x</span></span>      | <span data-ttu-id="35dc6-145">x</span><span class="sxs-lookup"><span data-stu-id="35dc6-145">x</span></span>        | <span data-ttu-id="35dc6-146">x</span><span class="sxs-lookup"><span data-stu-id="35dc6-146">x</span></span>     | <span data-ttu-id="35dc6-147">x</span><span class="sxs-lookup"><span data-stu-id="35dc6-147">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="35dc6-148">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="35dc6-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35dc6-149">Объекты модели шейдеров 5</span><span class="sxs-lookup"><span data-stu-id="35dc6-149">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 




