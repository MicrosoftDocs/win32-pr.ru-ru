---
title: sample_c (SM4-ASM)
description: Выполняет фильтр сравнения.
ms.assetid: 59786ED2-48FB-494E-A5A4-F732D63BF01B
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23563fe52bbc943e8756d04085b66d156ab259d7
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104996879"
---
# <a name="sample_c-sm4---asm"></a><span data-ttu-id="a5b9a-103">Пример \_ c (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="a5b9a-103">sample\_c (sm4 - asm)</span></span>

<span data-ttu-id="a5b9a-104">Выполняет фильтр сравнения.</span><span class="sxs-lookup"><span data-stu-id="a5b9a-104">Performs a comparison filter.</span></span>



| <span data-ttu-id="a5b9a-105">образец \_ c \[ \_ аоффимми (u, v, w) \] dest \[ . Mask \] , сркаддресс \[ . свиззле \] , сркресаурце. r,//должен быть. r свиззле срксамплер, сркреференцевалуе//один выбранный компонент</span><span class="sxs-lookup"><span data-stu-id="a5b9a-105">sample\_c\[\_aoffimmi(u,v,w)\] dest\[.mask\], srcAddress\[.swizzle\], srcResource.r, // must be .r swizzle srcSampler, srcReferenceValue // single component selected</span></span> |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="a5b9a-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="a5b9a-106">Item</span></span>                                                                                                                                       | <span data-ttu-id="a5b9a-107">Описание</span><span class="sxs-lookup"><span data-stu-id="a5b9a-107">Description</span></span>                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5b9a-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="a5b9a-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/>                                                                            | <span data-ttu-id="a5b9a-109">\[в \] адресе результатов операции.</span><span class="sxs-lookup"><span data-stu-id="a5b9a-109">\[in\] The address of the results of the operation.</span></span><br/>                                                             |
| <span data-ttu-id="a5b9a-110"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*сркаддресс*</span><span class="sxs-lookup"><span data-stu-id="a5b9a-110"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span></span><br/>                             | <span data-ttu-id="a5b9a-111">\[в \] наборе координат текстуры.</span><span class="sxs-lookup"><span data-stu-id="a5b9a-111">\[in\] A set of texture coordinates.</span></span> <span data-ttu-id="a5b9a-112">Дополнительные сведения см. в [примере](sample--sm4---asm-.md) инструкции.</span><span class="sxs-lookup"><span data-stu-id="a5b9a-112">For more information see the [sample](sample--sm4---asm-.md) instruction.</span></span><br/> |
| <span data-ttu-id="a5b9a-113"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*сркресаурце*</span><span class="sxs-lookup"><span data-stu-id="a5b9a-113"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span></span><br/>                         | <span data-ttu-id="a5b9a-114">\[в \] регистре текстуры.</span><span class="sxs-lookup"><span data-stu-id="a5b9a-114">\[in\] A texture register.</span></span> <span data-ttu-id="a5b9a-115">Дополнительные сведения см. в **примере** инструкции.</span><span class="sxs-lookup"><span data-stu-id="a5b9a-115">For more information see the **sample** instruction.</span></span><br/>                                 |
| <span data-ttu-id="a5b9a-116"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*срксамплер*</span><span class="sxs-lookup"><span data-stu-id="a5b9a-116"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span></span><br/>                             | <span data-ttu-id="a5b9a-117">\[в \] регистре образца.</span><span class="sxs-lookup"><span data-stu-id="a5b9a-117">\[in\] A sampler register.</span></span> <span data-ttu-id="a5b9a-118">Дополнительные сведения см. в **примере** инструкции.</span><span class="sxs-lookup"><span data-stu-id="a5b9a-118">For more information see the **sample** instruction.</span></span><br/>                                 |
| <span data-ttu-id="a5b9a-119"><span id="srcReferenceValue"></span><span id="srcreferencevalue"></span><span id="SRCREFERENCEVALUE"></span>*сркреференцевалуе*</span><span class="sxs-lookup"><span data-stu-id="a5b9a-119"><span id="srcReferenceValue"></span><span id="srcreferencevalue"></span><span id="SRCREFERENCEVALUE"></span>*srcReferenceValue*</span></span><br/> | <span data-ttu-id="a5b9a-120">\[в \] регистре с выбранным одним компонентом, который используется в сравнении.</span><span class="sxs-lookup"><span data-stu-id="a5b9a-120">\[in\] A register with a single component selected, which is used in the comparison.</span></span><br/>                            |



 

## <a name="remarks"></a><span data-ttu-id="a5b9a-121">Примечания</span><span class="sxs-lookup"><span data-stu-id="a5b9a-121">Remarks</span></span>

<span data-ttu-id="a5b9a-122">Основной целью этой инструкции является предоставление стандартного блока для фильтрации глубины Percentage-Closer.</span><span class="sxs-lookup"><span data-stu-id="a5b9a-122">The primary purpose for this instruction is to provide a building-block for Percentage-Closer Depth filtering.</span></span> <span data-ttu-id="a5b9a-123">"C" в **образце \_ c** означает сравнение.</span><span class="sxs-lookup"><span data-stu-id="a5b9a-123">The "c" in **sample\_c** stands for Comparison.</span></span>

<span data-ttu-id="a5b9a-124">Операнды для **образца \_ c** идентичны [образцу](sample--sm4---asm-.md) инструкции, за исключением того, что существует дополнительный исходный операнд float32, *сркреференцевалуе*, который должен быть зарегистрирован с выбранным одним компонентом или скалярным литералом.</span><span class="sxs-lookup"><span data-stu-id="a5b9a-124">The operands to **sample\_c** are identical to the [sample](sample--sm4---asm-.md) instruction, except that there is an additional float32 source operand, *srcReferenceValue*, which must be a register with single-component selected, or a scalar literal.</span></span>

<span data-ttu-id="a5b9a-125">Параметр *сркресаурце* должен иметь значение. r (red) свиззле.</span><span class="sxs-lookup"><span data-stu-id="a5b9a-125">The *srcResource* parameter must have a .r (red) swizzle.</span></span> <span data-ttu-id="a5b9a-126">**образец \_ c** работает исключительно на красном компоненте и возвращает одно значение.</span><span class="sxs-lookup"><span data-stu-id="a5b9a-126">**sample\_c** operates exclusively on the red component, and returns a single value.</span></span> <span data-ttu-id="a5b9a-127">Свиззле. r On *сркресаурце* указывает, что скалярный результат реплицируется во все компоненты.</span><span class="sxs-lookup"><span data-stu-id="a5b9a-127">The .r swizzle on *srcResource* indicates that the scalar result is replicated to all components.</span></span>

<span data-ttu-id="a5b9a-128">Если буфер глубины задан как текстура ввода, значение глубины отображается в красном компоненте.</span><span class="sxs-lookup"><span data-stu-id="a5b9a-128">When a Depth Buffer is set as an input texture, the depth value shows up in the red component.</span></span>

<span data-ttu-id="a5b9a-129">Если эта инструкция используется с ресурсом, который не является Texture1D/2D/2DArray/Cube/Кубеаррай, он выдает неопределенные результаты.</span><span class="sxs-lookup"><span data-stu-id="a5b9a-129">If this instruction is used with a Resource that is not a Texture1D/2D/2DArray/Cube/CubeArray, it produces undefined results.</span></span>

<span data-ttu-id="a5b9a-130">При выполнении этой инструкции оборудование выборки использует Компарисонфунктиони текущего образца для сравнения *сркреференцевалуе* с красным значением компонента для исходного ресурса по каждому фильтру "коснуться" расположения (шаг текселя), который настраивается в настоящее время фильтром текстур на основе предоставленных координат в *сркаддресс*.</span><span class="sxs-lookup"><span data-stu-id="a5b9a-130">When this instruction is executed, the sampling hardware uses the current Sampler's ComparisonFunction to compare *srcReferenceValue* against the Red component value for the source Resource at each filter "tap" location (texel) that the currently configured texture filter covers, based on the provided coordinates in *srcAddress*.</span></span>

<span data-ttu-id="a5b9a-131">Сравнение происходит после того, как *сркреференцевалуе* был квантования до точности формата текстуры, точно так же, как я квантования z до глубины буфера, прежде чем сравнивать результаты в результатах проверки видимости слияния.</span><span class="sxs-lookup"><span data-stu-id="a5b9a-131">The comparison occurs after *srcReferenceValue* has been quantized to the precision of the texture format, in exactly the same way that z is quantized to depth buffer precision before Depth Comparison at the Output Merger visibility test.</span></span> <span data-ttu-id="a5b9a-132">Это включает в себя срез в диапазоне формата (например \[ , 0.. 1 \] для формата UNORM).</span><span class="sxs-lookup"><span data-stu-id="a5b9a-132">This includes a clamp to the format range (e.g. \[0..1\] for a UNORM format).</span></span>

<span data-ttu-id="a5b9a-133">Красный компонент исходного шаг текселя сравнивается с квантования *сркреференцевалуе*.</span><span class="sxs-lookup"><span data-stu-id="a5b9a-133">The source texel's Red component is compared against the quantized *srcReferenceValue*.</span></span> <span data-ttu-id="a5b9a-134">Для пикселей текстуры, которые выходят за пределы ресурса, значение красного компонента определяется путем применения режимов адресов (и Бордерколорр в режиме границы) из образца.</span><span class="sxs-lookup"><span data-stu-id="a5b9a-134">For texels that fall off the Resource, the Red component value is determined by applying the Address Modes (and BorderColorR if in Border mode) from the Sampler.</span></span> <span data-ttu-id="a5b9a-135">Сравнение учитывает все правила сравнения D3D11 с плавающей запятой в случае, если формат текстуры является плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="a5b9a-135">The comparison honors all D3D11 floating point comparison rules, in the case the texture format is floating point.</span></span>

<span data-ttu-id="a5b9a-136">Каждое сравнение, которое передает, возвращает 1.0 f как значение красного компонента для шаг текселя, и каждое сравнение, которое завершается сбоем, возвращает 0,0 f в качестве Красного значения текстуры.</span><span class="sxs-lookup"><span data-stu-id="a5b9a-136">Each comparison that passes returns 1.0f as the Red component value for the texel, and each comparison that fails returns 0.0f as the Red value for the texture.</span></span> <span data-ttu-id="a5b9a-137">Фильтрация выполняется точно так же, как указано в состояниях образца, работает только в красном компоненте и возвращает один скалярный результат фильтра обратно шейдеру, который реплицируется во все компоненты маскированных *приемников* .</span><span class="sxs-lookup"><span data-stu-id="a5b9a-137">Filtering then occurs exactly as specified by the Sampler states, operating only in the Red component, and returning a single scalar filter result back to the Shader, replicated to all masked *dest* components.</span></span>

<span data-ttu-id="a5b9a-138">Использование **образца \_ c** является ортогональным для всех других элементов управления фильтрации общего назначения.</span><span class="sxs-lookup"><span data-stu-id="a5b9a-138">The use of **sample\_c** is orthogonal to all other general purpose filtering controls.</span></span> <span data-ttu-id="a5b9a-139">**образец \_ c** работает без проблем с другими режимами фильтрации общего назначения.</span><span class="sxs-lookup"><span data-stu-id="a5b9a-139">**sample\_c** works seamlessly with the other general purpose filter modes.</span></span> <span data-ttu-id="a5b9a-140">**пример \_ c** изменяет поведение фильтров общего назначения таким образом, чтобы Фильтруемые значения стали 1,0 f или 0,0 f из-за результатов сравнения.</span><span class="sxs-lookup"><span data-stu-id="a5b9a-140">**sample\_c** changes the behavior of the general purpose filters such that the values being filtered all become 1.0f or 0.0f due to comparison results.</span></span>

<span data-ttu-id="a5b9a-141">При попытке получить из входного слота, к которому не привязано ничего, возвращается значение 0 для всех компонентов.</span><span class="sxs-lookup"><span data-stu-id="a5b9a-141">Fetching from an input slot that has nothing bound to it returns 0 for all components.</span></span>

<span data-ttu-id="a5b9a-142">Дополнительные сведения см. в [образце](sample--sm4---asm-.md) инструкции.</span><span class="sxs-lookup"><span data-stu-id="a5b9a-142">For more information, see the [sample](sample--sm4---asm-.md) instruction.</span></span>

<span data-ttu-id="a5b9a-143">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="a5b9a-143">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="a5b9a-144">Вершинный построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="a5b9a-144">Vertex Shader</span></span> | <span data-ttu-id="a5b9a-145">Шейдер геометрии</span><span class="sxs-lookup"><span data-stu-id="a5b9a-145">Geometry Shader</span></span> | <span data-ttu-id="a5b9a-146">Построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="a5b9a-146">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
|               |                 | <span data-ttu-id="a5b9a-147">x</span><span class="sxs-lookup"><span data-stu-id="a5b9a-147">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="a5b9a-148">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="a5b9a-148">Minimum Shader Model</span></span>

<span data-ttu-id="a5b9a-149">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="a5b9a-149">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="a5b9a-150">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="a5b9a-150">Shader Model</span></span>                                              | <span data-ttu-id="a5b9a-151">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="a5b9a-151">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="a5b9a-152">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="a5b9a-152">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="a5b9a-153">да</span><span class="sxs-lookup"><span data-stu-id="a5b9a-153">yes</span></span>       |
| [<span data-ttu-id="a5b9a-154">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="a5b9a-154">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="a5b9a-155">да</span><span class="sxs-lookup"><span data-stu-id="a5b9a-155">yes</span></span>       |
| [<span data-ttu-id="a5b9a-156">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="a5b9a-156">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="a5b9a-157">да</span><span class="sxs-lookup"><span data-stu-id="a5b9a-157">yes</span></span>       |
| [<span data-ttu-id="a5b9a-158">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a5b9a-158">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="a5b9a-159">Нет</span><span class="sxs-lookup"><span data-stu-id="a5b9a-159">no</span></span>        |
| [<span data-ttu-id="a5b9a-160">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a5b9a-160">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="a5b9a-161">Нет</span><span class="sxs-lookup"><span data-stu-id="a5b9a-161">no</span></span>        |
| [<span data-ttu-id="a5b9a-162">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a5b9a-162">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="a5b9a-163">Нет</span><span class="sxs-lookup"><span data-stu-id="a5b9a-163">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="a5b9a-164">См. также</span><span class="sxs-lookup"><span data-stu-id="a5b9a-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a5b9a-165">Сборка Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a5b9a-165">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





