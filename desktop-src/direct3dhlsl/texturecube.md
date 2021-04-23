---
title: Объект TextureCube
description: Тип Текстурекубе (как он существует в модели шейдеров 4) и переменные ресурсов. Этот объект текстуры поддерживает эти методы в дополнение к методам в модели шейдера 4.
ms.assetid: BC96D7BB-992E-48CC-A774-E211E1BB1720
keywords:
- HLSL объекта Текстурекубе
- Текстурекубе объект HLSL, описание
topic_type:
- apiref
api_name:
- TextureCube
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 939c79895ae1c24665fc70d6b6cf2ced19854e2b
ms.sourcegitcommit: 5724b38883e518ac565e1b266defa85ad0941bb2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/14/2021
ms.locfileid: "104156983"
---
# <a name="texturecube-object"></a><span data-ttu-id="0582e-106">Объект TextureCube</span><span class="sxs-lookup"><span data-stu-id="0582e-106">TextureCube object</span></span>

<span data-ttu-id="0582e-107">Тип **текстурекубе** ([как он существует в модели шейдеров 4](dx-graphics-hlsl-to-type.md)) и переменные ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0582e-107">**TextureCube** type ([as it exists in Shader Model 4](dx-graphics-hlsl-to-type.md)) plus resource variables.</span></span> <span data-ttu-id="0582e-108">Этот объект текстуры поддерживает эти методы в дополнение к методам в модели шейдера 4.</span><span class="sxs-lookup"><span data-stu-id="0582e-108">This texture object supports these methods in addition to the methods in Shader Model 4.</span></span>

-   [<span data-ttu-id="0582e-109">Методы</span><span class="sxs-lookup"><span data-stu-id="0582e-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="0582e-110">Методы</span><span class="sxs-lookup"><span data-stu-id="0582e-110">Methods</span></span>

<span data-ttu-id="0582e-111">Объект **текстурекубе** содержит эти методы.</span><span class="sxs-lookup"><span data-stu-id="0582e-111">The **TextureCube** object has these methods.</span></span>



| <span data-ttu-id="0582e-112">Метод</span><span class="sxs-lookup"><span data-stu-id="0582e-112">Method</span></span>                                                      | <span data-ttu-id="0582e-113">Описание</span><span class="sxs-lookup"><span data-stu-id="0582e-113">Description</span></span>                                                                                                                                             |
|:------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0582e-114">**Собрать**</span><span class="sxs-lookup"><span data-stu-id="0582e-114">**Gather**</span></span>](texturecube-gather.md)                         | <span data-ttu-id="0582e-115">Возвращает четыре значения шаг текселя, которые будут использоваться в операции линейной фильтрации.</span><span class="sxs-lookup"><span data-stu-id="0582e-115">Returns the four texel values that would be used in a bi-linear filtering operation.</span></span><br/>                                                                |
| [<span data-ttu-id="0582e-116">**GatherAlpha**</span><span class="sxs-lookup"><span data-stu-id="0582e-116">**GatherAlpha**</span></span>](texturecube-gatheralpha.md)               | <span data-ttu-id="0582e-117">Возвращает альфа-компоненты четырех значений шаг текселя, которые будут использоваться в операции линейной фильтрации.</span><span class="sxs-lookup"><span data-stu-id="0582e-117">Returns the alpha components of the four texel values that would be used in a bi-linear filtering operation.</span></span><br/>                                        |
| [<span data-ttu-id="0582e-118">**GatherBlue**</span><span class="sxs-lookup"><span data-stu-id="0582e-118">**GatherBlue**</span></span>](texturecube-gatherblue.md)                 | <span data-ttu-id="0582e-119">Возвращает синие компоненты четырех шаг текселя значений, которые будут использоваться в операции линейной фильтрации.</span><span class="sxs-lookup"><span data-stu-id="0582e-119">Returns the blue components of the four texel values that would be used in a bi-linear filtering operation.</span></span><br/>                                         |
| [<span data-ttu-id="0582e-120">**GatherCmp**</span><span class="sxs-lookup"><span data-stu-id="0582e-120">**GatherCmp**</span></span>](texturecube-gathercmp.md)                   | <span data-ttu-id="0582e-121">Для четырех значений шаг текселя, которые будут использоваться в операции линейной фильтрации, возвращает их сравнение со значением сравнения.</span><span class="sxs-lookup"><span data-stu-id="0582e-121">For four texel values that would be used in a bi-linear filtering operation, returns their comparison against a compare value.</span></span><br/>                      |
| [<span data-ttu-id="0582e-122">**GatherCmpAlpha**</span><span class="sxs-lookup"><span data-stu-id="0582e-122">**GatherCmpAlpha**</span></span>](texturecube-gathercmpalpha.md)         | <span data-ttu-id="0582e-123">Для четырех значений шаг текселя, которые будут использоваться в операции линейной фильтрации, функция возвращает сравнение альфа-компонента со значением сравнения.</span><span class="sxs-lookup"><span data-stu-id="0582e-123">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their alpha component against a compare value.</span></span><br/> |
| [<span data-ttu-id="0582e-124">**GatherCmpBlue**</span><span class="sxs-lookup"><span data-stu-id="0582e-124">**GatherCmpBlue**</span></span>](texturecube-gathercmpblue.md)           | <span data-ttu-id="0582e-125">Для четырех значений шаг текселя, которые будут использоваться в операции линейной фильтрации, функция возвращает сравнение их синего компонента со значением сравнения.</span><span class="sxs-lookup"><span data-stu-id="0582e-125">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their blue component against a compare value.</span></span><br/>  |
| [<span data-ttu-id="0582e-126">**GatherCmpGreen**</span><span class="sxs-lookup"><span data-stu-id="0582e-126">**GatherCmpGreen**</span></span>](texturecube-gathercmpgreen.md)         | <span data-ttu-id="0582e-127">Для четырех значений шаг текселя, которые будут использоваться в операции линейной фильтрации, функция возвращает сравнение зеленого компонента со значением сравнения.</span><span class="sxs-lookup"><span data-stu-id="0582e-127">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their green component against a compare value.</span></span><br/> |
| [<span data-ttu-id="0582e-128">**GatherCmpRed**</span><span class="sxs-lookup"><span data-stu-id="0582e-128">**GatherCmpRed**</span></span>](texturecube-gathercmpred.md)             | <span data-ttu-id="0582e-129">Для четырех значений шаг текселя, которые будут использоваться в операции линейной фильтрации, функция возвращает сравнение их красного компонента со значением сравнения.</span><span class="sxs-lookup"><span data-stu-id="0582e-129">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their red component against a compare value.</span></span><br/>   |
| [<span data-ttu-id="0582e-130">**GatherGreen**</span><span class="sxs-lookup"><span data-stu-id="0582e-130">**GatherGreen**</span></span>](texturecube-gathergreen.md)               | <span data-ttu-id="0582e-131">Возвращает зеленые компоненты четырех значений шаг текселя, которые будут использоваться в операции линейной фильтрации.</span><span class="sxs-lookup"><span data-stu-id="0582e-131">Returns the green components of the four texel values that would be used in a bi-linear filtering operation.</span></span><br/>                                        |
| [<span data-ttu-id="0582e-132">**GatherRed**</span><span class="sxs-lookup"><span data-stu-id="0582e-132">**GatherRed**</span></span>](texturecube-gatherred.md)                   | <span data-ttu-id="0582e-133">Возвращает красные компоненты четырех значений шаг текселя, которые будут использоваться в операции линейной фильтрации.</span><span class="sxs-lookup"><span data-stu-id="0582e-133">Returns the red components of the four texel values that would be used in a bi-linear filtering operation.</span></span><br/>                                          |
| [<span data-ttu-id="0582e-134">**Пример**</span><span class="sxs-lookup"><span data-stu-id="0582e-134">**Sample**</span></span>](texturecube-sample.md)                         | <span data-ttu-id="0582e-135">Выбор текстуры.</span><span class="sxs-lookup"><span data-stu-id="0582e-135">Samples a texture.</span></span><br/>                                                                                                                                  |
| [<span data-ttu-id="0582e-136">**самплебиас**</span><span class="sxs-lookup"><span data-stu-id="0582e-136">**SampleBias**</span></span>](texturecube-samplebias.md)                 | <span data-ttu-id="0582e-137">Выбор текстуры после применения значения смещения к уровню mipmap.</span><span class="sxs-lookup"><span data-stu-id="0582e-137">Samples a texture, after applying the bias value to the mipmap level.</span></span><br/>                                                                               |
| [<span data-ttu-id="0582e-138">**самплекмп**</span><span class="sxs-lookup"><span data-stu-id="0582e-138">**SampleCmp**</span></span>](texturecube-samplecmp.md)                   | <span data-ttu-id="0582e-139">Выбор текстуры с использованием значения сравнения для отклонения выборок.</span><span class="sxs-lookup"><span data-stu-id="0582e-139">Samples a texture, using a comparison value to reject samples.</span></span><br/>                                                                                      |
| [<span data-ttu-id="0582e-140">**SampleCmpLevelZero**</span><span class="sxs-lookup"><span data-stu-id="0582e-140">**SampleCmpLevelZero**</span></span>](texturecube-samplecmplevelzero.md) | <span data-ttu-id="0582e-141">Производит выборку текстуры (только mipmap уровень 0), используя значение сравнения для отклонения выборок.</span><span class="sxs-lookup"><span data-stu-id="0582e-141">Samples a texture (mipmap level 0 only), using a comparison value to reject samples.</span></span><br/>                                                                |
| [<span data-ttu-id="0582e-142">**самплеград**</span><span class="sxs-lookup"><span data-stu-id="0582e-142">**SampleGrad**</span></span>](texturecube-samplegrad.md)                 | <span data-ttu-id="0582e-143">Выбор текстуры с помощью градиента, чтобы повлиять на способ вычисления расположения образца.</span><span class="sxs-lookup"><span data-stu-id="0582e-143">Samples a texture using a gradient to influence the way the sample location is calculated.</span></span><br/>                                                          |
| [<span data-ttu-id="0582e-144">**SampleLevel**</span><span class="sxs-lookup"><span data-stu-id="0582e-144">**SampleLevel**</span></span>](texturecube-samplelevel.md)               | <span data-ttu-id="0582e-145">Выбирает текстуру на указанном уровне mipmap.</span><span class="sxs-lookup"><span data-stu-id="0582e-145">Samples a texture on the specified mipmap level.</span></span><br/>                                                                                                    |



 

## <a name="remarks"></a><span data-ttu-id="0582e-146">Примечания</span><span class="sxs-lookup"><span data-stu-id="0582e-146">Remarks</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="0582e-147">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="0582e-147">Minimum Shader Model</span></span>

<span data-ttu-id="0582e-148">Этот объект поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="0582e-148">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="0582e-149">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="0582e-149">Shader Model</span></span>                                                                | <span data-ttu-id="0582e-150">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="0582e-150">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="0582e-151">[Модели шейдера 5](d3d11-graphics-reference-sm5.md) и более поздних моделей шейдеров</span><span class="sxs-lookup"><span data-stu-id="0582e-151">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="0582e-152">да</span><span class="sxs-lookup"><span data-stu-id="0582e-152">yes</span></span>       |



 

<span data-ttu-id="0582e-153">Этот объект поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="0582e-153">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="0582e-154">Вершина</span><span class="sxs-lookup"><span data-stu-id="0582e-154">Vertex</span></span> | <span data-ttu-id="0582e-155">Поверхности</span><span class="sxs-lookup"><span data-stu-id="0582e-155">Hull</span></span> | <span data-ttu-id="0582e-156">Домен</span><span class="sxs-lookup"><span data-stu-id="0582e-156">Domain</span></span> | <span data-ttu-id="0582e-157">Геометрия</span><span class="sxs-lookup"><span data-stu-id="0582e-157">Geometry</span></span> | <span data-ttu-id="0582e-158">Пиксель</span><span class="sxs-lookup"><span data-stu-id="0582e-158">Pixel</span></span> | <span data-ttu-id="0582e-159">Вычисления</span><span class="sxs-lookup"><span data-stu-id="0582e-159">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="0582e-160">x</span><span class="sxs-lookup"><span data-stu-id="0582e-160">x</span></span>      | <span data-ttu-id="0582e-161">x</span><span class="sxs-lookup"><span data-stu-id="0582e-161">x</span></span>    | <span data-ttu-id="0582e-162">x</span><span class="sxs-lookup"><span data-stu-id="0582e-162">x</span></span>      | <span data-ttu-id="0582e-163">x</span><span class="sxs-lookup"><span data-stu-id="0582e-163">x</span></span>        | <span data-ttu-id="0582e-164">x</span><span class="sxs-lookup"><span data-stu-id="0582e-164">x</span></span>     | <span data-ttu-id="0582e-165">x</span><span class="sxs-lookup"><span data-stu-id="0582e-165">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="0582e-166">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0582e-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0582e-167">Объекты модели шейдеров 5</span><span class="sxs-lookup"><span data-stu-id="0582e-167">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 





