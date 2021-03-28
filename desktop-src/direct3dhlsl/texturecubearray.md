---
title: Объект TextureCubeArray
description: Тип Текстурекубеаррай (как он существует в модели шейдеров 4) и переменные ресурсов. Этот объект текстуры поддерживает эти методы в дополнение к методам в модели шейдера 4.
ms.assetid: 62AAF0F9-D552-4FFA-B681-749D6DC205BD
keywords:
- HLSL объекта Текстурекубеаррай
- Текстурекубеаррай объект HLSL, описание
topic_type:
- apiref
api_name:
- TextureCubeArray
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e559214626fadbc08b8e9cd4d5568358f130779c
ms.sourcegitcommit: 5724b38883e518ac565e1b266defa85ad0941bb2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/14/2021
ms.locfileid: "104997990"
---
# <a name="texturecubearray-object"></a><span data-ttu-id="26724-106">Объект TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="26724-106">TextureCubeArray object</span></span>

<span data-ttu-id="26724-107">Тип **текстурекубеаррай** ([как он существует в модели шейдеров 4](dx-graphics-hlsl-to-type.md)) и переменные ресурсов.</span><span class="sxs-lookup"><span data-stu-id="26724-107">**TextureCubeArray** type ([as it exists in Shader Model 4](dx-graphics-hlsl-to-type.md)) plus resource variables.</span></span> <span data-ttu-id="26724-108">Этот объект текстуры поддерживает эти методы в дополнение к методам в модели шейдера 4.</span><span class="sxs-lookup"><span data-stu-id="26724-108">This texture object supports these methods in addition to the methods in Shader Model 4.</span></span>

-   [<span data-ttu-id="26724-109">Методы</span><span class="sxs-lookup"><span data-stu-id="26724-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="26724-110">Методы</span><span class="sxs-lookup"><span data-stu-id="26724-110">Methods</span></span>

<span data-ttu-id="26724-111">Объект **текстурекубеаррай** содержит эти методы.</span><span class="sxs-lookup"><span data-stu-id="26724-111">The **TextureCubeArray** object has these methods.</span></span>



| <span data-ttu-id="26724-112">Метод</span><span class="sxs-lookup"><span data-stu-id="26724-112">Method</span></span>                                                           | <span data-ttu-id="26724-113">Описание</span><span class="sxs-lookup"><span data-stu-id="26724-113">Description</span></span>                                                                                                                                              |
|:-----------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="26724-114">**Собрать**</span><span class="sxs-lookup"><span data-stu-id="26724-114">**Gather**</span></span>](texturecubearray-gather.md)                         | <span data-ttu-id="26724-115">Возвращает четыре значения шаг текселя, которые будут использоваться в операции линейной фильтрации.</span><span class="sxs-lookup"><span data-stu-id="26724-115">Returns the four texel values that would be used in a bi-linear filtering operation.</span></span><br/>                                                                |
| [<span data-ttu-id="26724-116">**GatherAlpha**</span><span class="sxs-lookup"><span data-stu-id="26724-116">**GatherAlpha**</span></span>](texturecubearray-gatheralpha.md)               | <span data-ttu-id="26724-117">Возвращает альфа-компоненты четырех значений шаг текселя, которые будут использоваться в операции линейной фильтрации.</span><span class="sxs-lookup"><span data-stu-id="26724-117">Returns the alpha components of the four texel values that would be used in a bi-linear filtering operation.</span></span><br/>                                        |
| [<span data-ttu-id="26724-118">**GatherBlue**</span><span class="sxs-lookup"><span data-stu-id="26724-118">**GatherBlue**</span></span>](texturecubearray-gatherblue.md)                 | <span data-ttu-id="26724-119">Возвращает синие компоненты четырех шаг текселя значений, которые будут использоваться в операции линейной фильтрации.</span><span class="sxs-lookup"><span data-stu-id="26724-119">Returns the blue components of the four texel values that would be used in a bi-linear filtering operation.</span></span><br/>                                         |
| [<span data-ttu-id="26724-120">**GatherCmp**</span><span class="sxs-lookup"><span data-stu-id="26724-120">**GatherCmp**</span></span>](texturecubearray-gathercmp.md)                   | <span data-ttu-id="26724-121">Для четырех значений шаг текселя, которые будут использоваться в операции линейной фильтрации, возвращает их сравнение со значением сравнения.</span><span class="sxs-lookup"><span data-stu-id="26724-121">For four texel values that would be used in a bi-linear filtering operation, returns their comparison against a compare value.</span></span><br/>                      |
| [<span data-ttu-id="26724-122">**GatherCmpAlpha**</span><span class="sxs-lookup"><span data-stu-id="26724-122">**GatherCmpAlpha**</span></span>](texturecubearray-gathercmpalpha.md)         | <span data-ttu-id="26724-123">Для четырех значений шаг текселя, которые будут использоваться в операции линейной фильтрации, функция возвращает сравнение альфа-компонента со значением сравнения.</span><span class="sxs-lookup"><span data-stu-id="26724-123">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their alpha component against a compare value.</span></span><br/> |
| [<span data-ttu-id="26724-124">**GatherCmpBlue**</span><span class="sxs-lookup"><span data-stu-id="26724-124">**GatherCmpBlue**</span></span>](texturecubearray-gathercmpblue.md)           | <span data-ttu-id="26724-125">Для четырех значений шаг текселя, которые будут использоваться в операции линейной фильтрации, функция возвращает сравнение их синего компонента со значением сравнения.</span><span class="sxs-lookup"><span data-stu-id="26724-125">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their blue component against a compare value.</span></span><br/>  |
| [<span data-ttu-id="26724-126">**GatherCmpGreen**</span><span class="sxs-lookup"><span data-stu-id="26724-126">**GatherCmpGreen**</span></span>](texturecubearray-gathercmpgreen.md)         | <span data-ttu-id="26724-127">Для четырех значений шаг текселя, которые будут использоваться в операции линейной фильтрации, функция возвращает сравнение зеленого компонента со значением сравнения.</span><span class="sxs-lookup"><span data-stu-id="26724-127">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their green component against a compare value.</span></span><br/> |
| [<span data-ttu-id="26724-128">**GatherCmpRed**</span><span class="sxs-lookup"><span data-stu-id="26724-128">**GatherCmpRed**</span></span>](texturecubearray-gathercmpred.md)             | <span data-ttu-id="26724-129">Для четырех значений шаг текселя, которые будут использоваться в операции линейной фильтрации, функция возвращает сравнение их красного компонента со значением сравнения.</span><span class="sxs-lookup"><span data-stu-id="26724-129">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their red component against a compare value.</span></span><br/>   |
| [<span data-ttu-id="26724-130">**GatherGreen**</span><span class="sxs-lookup"><span data-stu-id="26724-130">**GatherGreen**</span></span>](texturecubearray-gathergreen.md)               | <span data-ttu-id="26724-131">Возвращает зеленые компоненты четырех значений шаг текселя, которые будут использоваться в операции линейной фильтрации.</span><span class="sxs-lookup"><span data-stu-id="26724-131">Returns the green components of the four texel values that would be used in a bi-linear filtering operation.</span></span><br/>                                        |
| [<span data-ttu-id="26724-132">**GatherRed**</span><span class="sxs-lookup"><span data-stu-id="26724-132">**GatherRed**</span></span>](texturecubearray-gatherred.md)                   | <span data-ttu-id="26724-133">Возвращает красные компоненты четырех значений шаг текселя, которые будут использоваться в операции линейной фильтрации.</span><span class="sxs-lookup"><span data-stu-id="26724-133">Returns the red components of the four texel values that would be used in a bi-linear filtering operation.</span></span><br/>                                          |
| [<span data-ttu-id="26724-134">**Пример**</span><span class="sxs-lookup"><span data-stu-id="26724-134">**Sample**</span></span>](texturecubearray-sample.md)                         | <span data-ttu-id="26724-135">Выбор текстуры.</span><span class="sxs-lookup"><span data-stu-id="26724-135">Samples a texture.</span></span><br/>                                                                                                                                  |
| [<span data-ttu-id="26724-136">**самплебиас**</span><span class="sxs-lookup"><span data-stu-id="26724-136">**SampleBias**</span></span>](texturecubearray-samplebias.md)                 | <span data-ttu-id="26724-137">Выбор текстуры после применения значения смещения к уровню mipmap.</span><span class="sxs-lookup"><span data-stu-id="26724-137">Samples a texture, after applying the bias value to the mipmap level.</span></span><br/>                                                                               |
| [<span data-ttu-id="26724-138">**самплекмп**</span><span class="sxs-lookup"><span data-stu-id="26724-138">**SampleCmp**</span></span>](texturecubearray-samplecmp.md)                   | <span data-ttu-id="26724-139">Выбор текстуры с использованием значения сравнения для отклонения выборок.</span><span class="sxs-lookup"><span data-stu-id="26724-139">Samples a texture, using a comparison value to reject samples.</span></span><br/>                                                                                      |
| [<span data-ttu-id="26724-140">**SampleCmpLevelZero**</span><span class="sxs-lookup"><span data-stu-id="26724-140">**SampleCmpLevelZero**</span></span>](texturecubearray-samplecmplevelzero.md) | <span data-ttu-id="26724-141">Производит выборку текстуры (только mipmap уровень 0), используя значение сравнения для отклонения выборок.</span><span class="sxs-lookup"><span data-stu-id="26724-141">Samples a texture (mipmap level 0 only), using a comparison value to reject samples.</span></span><br/>                                                                |
| [<span data-ttu-id="26724-142">**самплеград**</span><span class="sxs-lookup"><span data-stu-id="26724-142">**SampleGrad**</span></span>](texturecubearray-samplegrad.md)                 | <span data-ttu-id="26724-143">Выбор текстуры с помощью градиента, чтобы повлиять на способ вычисления расположения образца.</span><span class="sxs-lookup"><span data-stu-id="26724-143">Samples a texture using a gradient to influence the way the sample location is calculated.</span></span><br/>                                                          |
| [<span data-ttu-id="26724-144">**SampleLevel**</span><span class="sxs-lookup"><span data-stu-id="26724-144">**SampleLevel**</span></span>](texturecubearray-samplelevel.md)               | <span data-ttu-id="26724-145">Выбирает текстуру на указанном уровне mipmap.</span><span class="sxs-lookup"><span data-stu-id="26724-145">Samples a texture on the specified mipmap level.</span></span><br/>                                                                                                    |



 

## <a name="remarks"></a><span data-ttu-id="26724-146">Примечания</span><span class="sxs-lookup"><span data-stu-id="26724-146">Remarks</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="26724-147">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="26724-147">Minimum Shader Model</span></span>

<span data-ttu-id="26724-148">Этот объект поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="26724-148">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="26724-149">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="26724-149">Shader Model</span></span>                                                                | <span data-ttu-id="26724-150">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="26724-150">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="26724-151">[Модели шейдера 5](d3d11-graphics-reference-sm5.md) и более поздних моделей шейдеров</span><span class="sxs-lookup"><span data-stu-id="26724-151">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="26724-152">да</span><span class="sxs-lookup"><span data-stu-id="26724-152">yes</span></span>       |



 

<span data-ttu-id="26724-153">Этот объект поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="26724-153">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="26724-154">Вершина</span><span class="sxs-lookup"><span data-stu-id="26724-154">Vertex</span></span> | <span data-ttu-id="26724-155">Поверхности</span><span class="sxs-lookup"><span data-stu-id="26724-155">Hull</span></span> | <span data-ttu-id="26724-156">Домен</span><span class="sxs-lookup"><span data-stu-id="26724-156">Domain</span></span> | <span data-ttu-id="26724-157">Геометрия</span><span class="sxs-lookup"><span data-stu-id="26724-157">Geometry</span></span> | <span data-ttu-id="26724-158">Пиксель</span><span class="sxs-lookup"><span data-stu-id="26724-158">Pixel</span></span> | <span data-ttu-id="26724-159">Вычисления</span><span class="sxs-lookup"><span data-stu-id="26724-159">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="26724-160">x</span><span class="sxs-lookup"><span data-stu-id="26724-160">x</span></span>      | <span data-ttu-id="26724-161">x</span><span class="sxs-lookup"><span data-stu-id="26724-161">x</span></span>    | <span data-ttu-id="26724-162">x</span><span class="sxs-lookup"><span data-stu-id="26724-162">x</span></span>      | <span data-ttu-id="26724-163">x</span><span class="sxs-lookup"><span data-stu-id="26724-163">x</span></span>        | <span data-ttu-id="26724-164">x</span><span class="sxs-lookup"><span data-stu-id="26724-164">x</span></span>     | <span data-ttu-id="26724-165">x</span><span class="sxs-lookup"><span data-stu-id="26724-165">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="26724-166">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="26724-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26724-167">Объекты модели шейдеров 5</span><span class="sxs-lookup"><span data-stu-id="26724-167">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 





