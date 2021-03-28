---
title: Texture2D
description: Texture2D
ms.assetid: e4f9cfd8-65e6-4375-8f87-736bca32cad4
keywords:
- Texture2D HLSL
topic_type:
- apiref
api_name:
- Texture2D
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f0c9b73d66f1c5a38b077b241df8e5859b706e2f
ms.sourcegitcommit: 5724b38883e518ac565e1b266defa85ad0941bb2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/14/2021
ms.locfileid: "104986168"
---
# <a name="texture2d"></a><span data-ttu-id="bd10e-104">Texture2D</span><span class="sxs-lookup"><span data-stu-id="bd10e-104">Texture2D</span></span>

<span data-ttu-id="bd10e-105">Тип Texture2D ([как он существует в модели шейдеров 4](dx-graphics-hlsl-to-type.md)) и переменные ресурсов.</span><span class="sxs-lookup"><span data-stu-id="bd10e-105">Texture2D type ([as it exists in Shader Model 4](dx-graphics-hlsl-to-type.md)) plus resource variables.</span></span> <span data-ttu-id="bd10e-106">Этот объект текстуры поддерживает следующие методы в дополнение к методам в модели шейдера 4.</span><span class="sxs-lookup"><span data-stu-id="bd10e-106">This texture object supports the following methods in addition to the methods in Shader Model 4.</span></span>



| <span data-ttu-id="bd10e-107">Метод</span><span class="sxs-lookup"><span data-stu-id="bd10e-107">Method</span></span>                                                                 | <span data-ttu-id="bd10e-108">Описание</span><span class="sxs-lookup"><span data-stu-id="bd10e-108">Description</span></span>                                                                                                                                        |
|------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bd10e-109">**Собрать**</span><span class="sxs-lookup"><span data-stu-id="bd10e-109">**Gather**</span></span>](texture2d-gather.md)                                      | <span data-ttu-id="bd10e-110">Возвращает четыре значения шаг текселя, которые будут использоваться в операции линейной фильтрации.</span><span class="sxs-lookup"><span data-stu-id="bd10e-110">Returns the four texel values that would be used in a bi-linear filtering operation.</span></span>                                                                |
| [<span data-ttu-id="bd10e-111">**GatherRed**</span><span class="sxs-lookup"><span data-stu-id="bd10e-111">**GatherRed**</span></span>](texture2d-gatherred.md)                                | <span data-ttu-id="bd10e-112">Возвращает красные компоненты четырех значений шаг текселя, которые будут использоваться в операции линейной фильтрации.</span><span class="sxs-lookup"><span data-stu-id="bd10e-112">Returns the red components of the four texel values that would be used in a bi-linear filtering operation.</span></span>                                          |
| [<span data-ttu-id="bd10e-113">**GatherGreen**</span><span class="sxs-lookup"><span data-stu-id="bd10e-113">**GatherGreen**</span></span>](texture2d-gathergreen.md)                            | <span data-ttu-id="bd10e-114">Возвращает зеленые компоненты четырех значений шаг текселя, которые будут использоваться в операции линейной фильтрации.</span><span class="sxs-lookup"><span data-stu-id="bd10e-114">Returns the green components of the four texel values that would be used in a bi-linear filtering operation.</span></span>                                        |
| [<span data-ttu-id="bd10e-115">**GatherBlue**</span><span class="sxs-lookup"><span data-stu-id="bd10e-115">**GatherBlue**</span></span>](texture2d-gatherblue.md)                              | <span data-ttu-id="bd10e-116">Возвращает синие компоненты четырех шаг текселя значений, которые будут использоваться в операции линейной фильтрации.</span><span class="sxs-lookup"><span data-stu-id="bd10e-116">Returns the blue components of the four texel values that would be used in a bi-linear filtering operation.</span></span>                                         |
| [<span data-ttu-id="bd10e-117">**GatherAlpha**</span><span class="sxs-lookup"><span data-stu-id="bd10e-117">**GatherAlpha**</span></span>](texture2d-gatheralpha.md)                            | <span data-ttu-id="bd10e-118">Возвращает альфа-компоненты четырех значений шаг текселя, которые будут использоваться в операции линейной фильтрации.</span><span class="sxs-lookup"><span data-stu-id="bd10e-118">Returns the alpha components of the four texel values that would be used in a bi-linear filtering operation.</span></span>                                        |
| [<span data-ttu-id="bd10e-119">**GatherCmp**</span><span class="sxs-lookup"><span data-stu-id="bd10e-119">**GatherCmp**</span></span>](texture2d-gathercmp.md)                                | <span data-ttu-id="bd10e-120">Для четырех значений шаг текселя, которые будут использоваться в операции линейной фильтрации, возвращает их сравнение со значением сравнения.</span><span class="sxs-lookup"><span data-stu-id="bd10e-120">For four texel values that would be used in a bi-linear filtering operation, returns their comparison against a compare value.</span></span>                      |
| [<span data-ttu-id="bd10e-121">**GatherCmpRed**</span><span class="sxs-lookup"><span data-stu-id="bd10e-121">**GatherCmpRed**</span></span>](texture2d-gathercmpred.md)                          | <span data-ttu-id="bd10e-122">Для четырех значений шаг текселя, которые будут использоваться в операции линейной фильтрации, функция возвращает сравнение их красного компонента со значением сравнения.</span><span class="sxs-lookup"><span data-stu-id="bd10e-122">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their red component against a compare value.</span></span>   |
| [<span data-ttu-id="bd10e-123">**GatherCmpGreen**</span><span class="sxs-lookup"><span data-stu-id="bd10e-123">**GatherCmpGreen**</span></span>](texture2d-gathercmpgreen.md)                      | <span data-ttu-id="bd10e-124">Для четырех значений шаг текселя, которые будут использоваться в операции линейной фильтрации, функция возвращает сравнение зеленого компонента со значением сравнения.</span><span class="sxs-lookup"><span data-stu-id="bd10e-124">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their green component against a compare value.</span></span> |
| [<span data-ttu-id="bd10e-125">**GatherCmpBlue**</span><span class="sxs-lookup"><span data-stu-id="bd10e-125">**GatherCmpBlue**</span></span>](texture2d-gathercmpblue.md)                        | <span data-ttu-id="bd10e-126">Для четырех значений шаг текселя, которые будут использоваться в операции линейной фильтрации, функция возвращает сравнение их синего компонента со значением сравнения.</span><span class="sxs-lookup"><span data-stu-id="bd10e-126">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their blue component against a compare value.</span></span>  |
| [<span data-ttu-id="bd10e-127">**GatherCmpAlpha**</span><span class="sxs-lookup"><span data-stu-id="bd10e-127">**GatherCmpAlpha**</span></span>](texture2d-gathercmpalpha.md)                      | <span data-ttu-id="bd10e-128">Для четырех значений шаг текселя, которые будут использоваться в операции линейной фильтрации, функция возвращает сравнение альфа-компонента со значением сравнения.</span><span class="sxs-lookup"><span data-stu-id="bd10e-128">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their alpha component against a compare value.</span></span> |
| [<span data-ttu-id="bd10e-129">**GetDimensions**</span><span class="sxs-lookup"><span data-stu-id="bd10e-129">**GetDimensions**</span></span>](sm5-object-texture2d-getdimensions.md)             | <span data-ttu-id="bd10e-130">Возвращает размеры ресурсов.</span><span class="sxs-lookup"><span data-stu-id="bd10e-130">Gets the resource dimensions.</span></span>                                                                                                                       |
| [<span data-ttu-id="bd10e-131">**Загрузить**</span><span class="sxs-lookup"><span data-stu-id="bd10e-131">**Load**</span></span>](texture2d-load.md)                                          | <span data-ttu-id="bd10e-132">Считывает данные текстуры.</span><span class="sxs-lookup"><span data-stu-id="bd10e-132">Reads texture data.</span></span>                                                                                                                                 |
| <span data-ttu-id="bd10e-133">[**MIPS. Станции\[\]\[\]**](sm5-object-texture2d-mipsoperatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="bd10e-133">[**mips.Operator\[\]\[\]**](sm5-object-texture2d-mipsoperatorindex.md)</span></span> | <span data-ttu-id="bd10e-134">Возвращает переменную ресурса, доступную только для чтения.</span><span class="sxs-lookup"><span data-stu-id="bd10e-134">Gets a read-only resource variable.</span></span>                                                                                                                 |
| <span data-ttu-id="bd10e-135">[**Оператор\[\]**](sm5-object-texture2d-operatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="bd10e-135">[**Operator\[\]**](sm5-object-texture2d-operatorindex.md)</span></span>              | <span data-ttu-id="bd10e-136">Возвращает переменную ресурса, доступную только для чтения.</span><span class="sxs-lookup"><span data-stu-id="bd10e-136">Gets a read-only resource variable.</span></span>                                                                                                                 |
| [<span data-ttu-id="bd10e-137">**Пример**</span><span class="sxs-lookup"><span data-stu-id="bd10e-137">**Sample**</span></span>](texture-sample-overload.md)                               | <span data-ttu-id="bd10e-138">Выбор текстуры.</span><span class="sxs-lookup"><span data-stu-id="bd10e-138">Samples a texture.</span></span>                                                                                                                                  |
| [<span data-ttu-id="bd10e-139">**самплебиас**</span><span class="sxs-lookup"><span data-stu-id="bd10e-139">**SampleBias**</span></span>](texture2d-samplebias.md)                              | <span data-ttu-id="bd10e-140">Выбор текстуры после применения значения смещения к уровню mipmap.</span><span class="sxs-lookup"><span data-stu-id="bd10e-140">Samples a texture, after applying the bias value to the mipmap level.</span></span>                                                                               |
| [<span data-ttu-id="bd10e-141">**самплекмп**</span><span class="sxs-lookup"><span data-stu-id="bd10e-141">**SampleCmp**</span></span>](texture2d-samplecmp.md)                                | <span data-ttu-id="bd10e-142">Выбор текстуры с использованием значения сравнения для отклонения выборок.</span><span class="sxs-lookup"><span data-stu-id="bd10e-142">Samples a texture, using a comparison value to reject samples.</span></span>                                                                                      |
| [<span data-ttu-id="bd10e-143">**SampleCmpLevelZero**</span><span class="sxs-lookup"><span data-stu-id="bd10e-143">**SampleCmpLevelZero**</span></span>](texture2d-samplecmplevelzero.md)              | <span data-ttu-id="bd10e-144">Производит выборку текстуры (только mipmap уровень 0), используя значение сравнения для отклонения выборок.</span><span class="sxs-lookup"><span data-stu-id="bd10e-144">Samples a texture (mipmap level 0 only), using a comparison value to reject samples.</span></span>                                                                |
| [<span data-ttu-id="bd10e-145">**самплеград**</span><span class="sxs-lookup"><span data-stu-id="bd10e-145">**SampleGrad**</span></span>](texture2d-samplegrad.md)                              | <span data-ttu-id="bd10e-146">Выбор текстуры с помощью градиента, чтобы повлиять на способ вычисления расположения образца.</span><span class="sxs-lookup"><span data-stu-id="bd10e-146">Samples a texture using a gradient to influence the way the sample location is calculated.</span></span>                                                          |
| [<span data-ttu-id="bd10e-147">**SampleLevel**</span><span class="sxs-lookup"><span data-stu-id="bd10e-147">**SampleLevel**</span></span>](texture2d-samplelevel.md)                            | <span data-ttu-id="bd10e-148">Выбирает текстуру на указанном уровне mipmap.</span><span class="sxs-lookup"><span data-stu-id="bd10e-148">Samples a texture on the specified mipmap level.</span></span>                                                                                                    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="bd10e-149">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="bd10e-149">Minimum Shader Model</span></span>

<span data-ttu-id="bd10e-150">Этот объект поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="bd10e-150">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="bd10e-151">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="bd10e-151">Shader Model</span></span>                                                                | <span data-ttu-id="bd10e-152">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="bd10e-152">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="bd10e-153">[Модели шейдера 5](d3d11-graphics-reference-sm5.md) и более поздних моделей шейдеров</span><span class="sxs-lookup"><span data-stu-id="bd10e-153">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="bd10e-154">да</span><span class="sxs-lookup"><span data-stu-id="bd10e-154">yes</span></span>       |



 

<span data-ttu-id="bd10e-155">Этот объект поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="bd10e-155">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="bd10e-156">Вершина</span><span class="sxs-lookup"><span data-stu-id="bd10e-156">Vertex</span></span> | <span data-ttu-id="bd10e-157">Поверхности</span><span class="sxs-lookup"><span data-stu-id="bd10e-157">Hull</span></span> | <span data-ttu-id="bd10e-158">Домен</span><span class="sxs-lookup"><span data-stu-id="bd10e-158">Domain</span></span> | <span data-ttu-id="bd10e-159">Геометрия</span><span class="sxs-lookup"><span data-stu-id="bd10e-159">Geometry</span></span> | <span data-ttu-id="bd10e-160">Пиксель</span><span class="sxs-lookup"><span data-stu-id="bd10e-160">Pixel</span></span> | <span data-ttu-id="bd10e-161">Вычисления</span><span class="sxs-lookup"><span data-stu-id="bd10e-161">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="bd10e-162">x</span><span class="sxs-lookup"><span data-stu-id="bd10e-162">x</span></span>      | <span data-ttu-id="bd10e-163">x</span><span class="sxs-lookup"><span data-stu-id="bd10e-163">x</span></span>    | <span data-ttu-id="bd10e-164">x</span><span class="sxs-lookup"><span data-stu-id="bd10e-164">x</span></span>      | <span data-ttu-id="bd10e-165">x</span><span class="sxs-lookup"><span data-stu-id="bd10e-165">x</span></span>        | <span data-ttu-id="bd10e-166">x</span><span class="sxs-lookup"><span data-stu-id="bd10e-166">x</span></span>     | <span data-ttu-id="bd10e-167">x</span><span class="sxs-lookup"><span data-stu-id="bd10e-167">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="bd10e-168">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bd10e-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd10e-169">Объекты модели шейдеров 5</span><span class="sxs-lookup"><span data-stu-id="bd10e-169">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 




