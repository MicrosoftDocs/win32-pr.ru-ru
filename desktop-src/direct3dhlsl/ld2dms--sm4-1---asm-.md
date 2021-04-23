---
title: ld2dms (SM 4.1-ASM)
description: Считывает отдельные выборки из двухмерных многоуровневой текстуры.
ms.assetid: 8D92BFA8-4B22-46F3-876D-8D84BB3A96E7
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e9dd03b7c07f3fb25294dd0ad6aa382eb203560
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104133322"
---
# <a name="ld2dms-sm41---asm"></a><span data-ttu-id="b342d-103">ld2dms (SM 4.1-ASM)</span><span class="sxs-lookup"><span data-stu-id="b342d-103">ld2dms (sm4.1 - asm)</span></span>

<span data-ttu-id="b342d-104">Считывает отдельные выборки из двухмерных многоуровневой текстуры.</span><span class="sxs-lookup"><span data-stu-id="b342d-104">Reads individual samples out of 2-dimensional multi-sample textures.</span></span>



| <span data-ttu-id="b342d-105">ld2dms \[ \_ аоффимми (u, v) \] dest \[ . Mask \] , сркаддресс \[ . свиззле \] , сркресаурце \[ . свиззле \] , sampleIndex (скалярный операнд)</span><span class="sxs-lookup"><span data-stu-id="b342d-105">ld2dms\[\_aoffimmi(u,v)\] dest\[.mask\], srcAddress\[.swizzle\], srcResource\[.swizzle\], sampleIndex (scalar operand)</span></span> |
|------------------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="b342d-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="b342d-106">Item</span></span>                                                                                                               | <span data-ttu-id="b342d-107">Описание</span><span class="sxs-lookup"><span data-stu-id="b342d-107">Description</span></span>                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b342d-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="b342d-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/>                                                    | <span data-ttu-id="b342d-109">\[в \] адресе результата операции.</span><span class="sxs-lookup"><span data-stu-id="b342d-109">\[in\] The address of result of the operation.</span></span> <br/>                                                                 |
| <span data-ttu-id="b342d-110"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*сркаддресс*</span><span class="sxs-lookup"><span data-stu-id="b342d-110"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span></span><br/>     | <span data-ttu-id="b342d-111">\[в \] координатах текстуры, необходимых для выполнения примера.</span><span class="sxs-lookup"><span data-stu-id="b342d-111">\[in\] The texture coordinates needed to perform the sample.</span></span><br/>                                                    |
| <span data-ttu-id="b342d-112"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*сркресаурце*</span><span class="sxs-lookup"><span data-stu-id="b342d-112"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span></span><br/> | <span data-ttu-id="b342d-113">\[в \] регистре текстуры (t \# ), который должен быть объявлен, чтобы определить, из какой текстуры или буфера извлечь</span><span class="sxs-lookup"><span data-stu-id="b342d-113">\[in\] A texture register (t\#) which must have been declared identifying which Texture or Buffer to fetch from</span></span><br/> |
| <span data-ttu-id="b342d-114"><span id="sampleIndex"></span><span id="sampleindex"></span><span id="SAMPLEINDEX"></span>*sampleIndex*</span><span class="sxs-lookup"><span data-stu-id="b342d-114"><span id="sampleIndex"></span><span id="sampleindex"></span><span id="SAMPLEINDEX"></span>*sampleIndex*</span></span><br/> | <span data-ttu-id="b342d-115">\[в \] идендифиес примеры для чтения из *сркресаурце*.</span><span class="sxs-lookup"><span data-stu-id="b342d-115">\[in\] Idendifies the samples to read from *srcResource*.</span></span><br/>                                                       |



 

## <a name="remarks"></a><span data-ttu-id="b342d-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="b342d-116">Remarks</span></span>

<span data-ttu-id="b342d-117">Эта инструкция является упрощенной альтернативой инструкции [образца](sample--sm4---asm-.md) .</span><span class="sxs-lookup"><span data-stu-id="b342d-117">This instruction is a simplified alternative to the [sample](sample--sm4---asm-.md) instruction.</span></span> <span data-ttu-id="b342d-118">Он извлекает данные из указанной текстуры без какой-либо фильтрации (например, выборки точек) с помощью предоставленного целого числа *сркаддресс* и *sampleIndex*.</span><span class="sxs-lookup"><span data-stu-id="b342d-118">It fetches data from the specified Texture without any filtering (e.g. point sampling) using the provided integer *srcAddress* and *sampleIndex*.</span></span>

<span data-ttu-id="b342d-119">*сркаддресс* предоставляет набор координат текстуры, необходимых для выполнения образца в виде целых чисел без знака.</span><span class="sxs-lookup"><span data-stu-id="b342d-119">*srcAddress* provides the set of texture coordinates needed to perform the sample in the form of unsigned integers.</span></span> <span data-ttu-id="b342d-120">Если *сркаддресс* находится за пределами диапазона \[ 0... ( \# пикселей текстуры в измерении-1 \] ) **ld2dms** всегда возвращает 0 во всех компонентах, представленных в формате ресурса, и значения по умолчанию (0, 0, 0, 1,0 f/0x00000001) для отсутствующих компонентов.</span><span class="sxs-lookup"><span data-stu-id="b342d-120">If *srcAddress* is out of the range\[0...(\#texels in dimension -1)\], **ld2dms** always returns 0 in all components present in the format of the resource, and defaults (0,0,0,1.0f/0x00000001) for missing components.</span></span>

<span data-ttu-id="b342d-121">*sampleIndex* не обязательно должен быть литералом.</span><span class="sxs-lookup"><span data-stu-id="b342d-121">*sampleIndex* does not have to be a literal.</span></span> <span data-ttu-id="b342d-122">Количество нескольких выборок не обязательно указывать на ресурсе текстуры, оно работает с представлениями глубины или трафарета.</span><span class="sxs-lookup"><span data-stu-id="b342d-122">The multi-sample count does not have to be specified on the texture resource, and it works with depth or stencil views.</span></span>

<span data-ttu-id="b342d-123">Приложение, которому необходимо более гибкое управление поведением адресов вне диапазона, должно использовать **образец** инструкции, так как он учитывает поведение перетекания адресов, зеркального отображения, среза или границы, определенного как состояние выборки.</span><span class="sxs-lookup"><span data-stu-id="b342d-123">An application wishing any more flexible control over out-of-range address behavior should use the **sample** instruction instead, as it honors address wrap/mirror/clamp/border behavior defined as sampler state.</span></span>

<span data-ttu-id="b342d-124">*сркаддресс. b* (POST-свиззле) игнорируется для Texture2Ds.</span><span class="sxs-lookup"><span data-stu-id="b342d-124">*srcAddress.b* (post-swizzle) is ignored for Texture2Ds.</span></span> <span data-ttu-id="b342d-125">Если значение выходит за пределы диапазона доступных индексов массива \[ 0... ( Размер массива — 1) \] , то **ld2dms** всегда возвращает 0 во всех компонентах, представленных в формате ресурса, и значения по умолчанию (0, 0, 0, 1,0 f/0x00000001) для отсутствующих компонентов.</span><span class="sxs-lookup"><span data-stu-id="b342d-125">If the value is out of the range of available array indices \[0...(array size-1)\], then **ld2dms** always returns 0 in all components present in the format of the resource, and defaults (0,0,0,1.0f/0x00000001) for missing components.</span></span>

<span data-ttu-id="b342d-126">Для массивов Texture2D *сркаддресс. b* (после свиззле) предоставляет индекс массива.</span><span class="sxs-lookup"><span data-stu-id="b342d-126">For Texture2D Arrays, *srcAddress.b* (post-swizzle) provides the array index.</span></span> <span data-ttu-id="b342d-127">Охервисе имеет то же поведение, что и Texture2D.</span><span class="sxs-lookup"><span data-stu-id="b342d-127">Oherwise it has the same behavior as Texture2D.</span></span>

<span data-ttu-id="b342d-128">*сркаддресс. a* (POST-свиззле) всегда игнорируется.</span><span class="sxs-lookup"><span data-stu-id="b342d-128">*srcAddress.a* (post-swizzle) is always ignored.</span></span> <span data-ttu-id="b342d-129">Компилятор HLSL никогда не будет выводить ничего.</span><span class="sxs-lookup"><span data-stu-id="b342d-129">The HLSL compiler will never output anything there.</span></span>

<span data-ttu-id="b342d-130">*сркресаурце* — это регистр текстуры (t \# ), который должен быть объявлен (22.3.11), определяющий, из какой текстуры извлечь.</span><span class="sxs-lookup"><span data-stu-id="b342d-130">*srcResource* is a texture register (t\#) which must have been declared(22.3.11), identifying which Texture to fetch from.</span></span>

<span data-ttu-id="b342d-131">Выборка из t без \# привязки к ней возвращает значение 0 для всех компонентов.</span><span class="sxs-lookup"><span data-stu-id="b342d-131">Fetching from t\# that has nothing bound to it returns 0 for all components.</span></span>

### <a name="address-offset"></a><span data-ttu-id="b342d-132">Смещение адреса</span><span class="sxs-lookup"><span data-stu-id="b342d-132">Address Offset</span></span>

<span data-ttu-id="b342d-133">Необязательный \[ \_ суффикс аоффимми (u, v, w) \] (смещение адреса непосредственно целым числом) указывает на то, что координаты текстуры для **ld2dms** должны быть смещены по набору заданных непосредственных значений целочисленных констант шаг текселяого пространства.</span><span class="sxs-lookup"><span data-stu-id="b342d-133">The optional \[\_aoffimmi(u,v,w)\] suffix (address offset by immediate integer) indicates that the texture coordinates for the **ld2dms** are to be offset by a set of provided immediate texel space integer constant values.</span></span> <span data-ttu-id="b342d-134">Литеральные значения представляют собой набор из 4-разрядных чисел 2, имеющих целочисленный диапазон \[ — 8, 7 \] .</span><span class="sxs-lookup"><span data-stu-id="b342d-134">The literal values are a set of 4 bit 2's complement numbers, having integer range \[-8,7\].</span></span>

<span data-ttu-id="b342d-135">Смещения добавляются к координатам текстуры в шаг текселя пространстве.</span><span class="sxs-lookup"><span data-stu-id="b342d-135">The offsets are added to the texture coordinates, in texel space.</span></span>

<span data-ttu-id="b342d-136">Смещения адресов не применяются вдоль оси массива Texture1D и двумерных массивов.</span><span class="sxs-lookup"><span data-stu-id="b342d-136">Address offsets are not applied along the array axis of Texture1D/2D Arrays.</span></span>

<span data-ttu-id="b342d-137">Компоненты *\_ аоффимми v, w* игнорируются для Texture1Ds.</span><span class="sxs-lookup"><span data-stu-id="b342d-137">The *\_aoffimmi v,w* components are ignored for Texture1Ds.</span></span>

<span data-ttu-id="b342d-138">Компонент *\_ аоффимми w* не учитывается для Texture2Ds.</span><span class="sxs-lookup"><span data-stu-id="b342d-138">The *\_aoffimmi w* component is ignored for Texture2Ds.</span></span>

<span data-ttu-id="b342d-139">Так как координаты текстуры для **ld2dms** являются целыми числами без знака, если смещение приводит к тому, что адрес перейдется ниже нуля, он будет переноситься на большой адрес и приведет к выходу за пределы допустимого диапазона, который, например, **LD** возвращает 0 во всех компонентах в формате ресурса, и значения по умолчанию (0, 0, 0, 1,0 f/0x00000001)</span><span class="sxs-lookup"><span data-stu-id="b342d-139">Because the texture coordinates for **ld2dms** are unsigned integers, if the offset causes the address to go below zero, it will wrap to a large address, and result in an out of bounds access, which like **ld** returns 0 in all components present in the format of the resource, and the defaults (0,0,0,1.0f/0x00000001) for missing components.</span></span>

### <a name="sample-number"></a><span data-ttu-id="b342d-140">Образец числа</span><span class="sxs-lookup"><span data-stu-id="b342d-140">Sample Number</span></span>

<span data-ttu-id="b342d-141">**ld2dms** доступен для использования с любым ресурсом.</span><span class="sxs-lookup"><span data-stu-id="b342d-141">**ld2dms** is available for use on any resource.</span></span> <span data-ttu-id="b342d-142">**ld2dms** работает **идентично, за исключением** ресурсов 2D мултсампле, с помощью дополнительного операнда *sampleIndex* (от 0), который определяет, какой пример следует считать из ресурса.</span><span class="sxs-lookup"><span data-stu-id="b342d-142">**ld2dms** operates identically to **ld** except on 2D multsample resources, by using the additional (0-based) *sampleIndex* operand to identify which sample to read from the resource.</span></span>

<span data-ttu-id="b342d-143">Результат указания *sampleIndex* , превышающего число выборок в ресурсе, не определен, но не может возвращать данные за пределами адресного пространства контекста устройства.</span><span class="sxs-lookup"><span data-stu-id="b342d-143">The result of specifying a *sampleIndex* that exceeds the number of samples in the resource is undefined, but cannot return data outside of the address space of the device context.</span></span>

### <a name="return-type-control"></a><span data-ttu-id="b342d-144">Контроль возвращаемого типа</span><span class="sxs-lookup"><span data-stu-id="b342d-144">Return Type Control</span></span>

<span data-ttu-id="b342d-145">Формат данных, возвращаемый функцией **ld2dms** в регистр назначения, определяется так же, как описано в **образце** инструкции.</span><span class="sxs-lookup"><span data-stu-id="b342d-145">The data format returned by **ld2dms** to the destination register is determined in the same way as described for the **sample** instruction.</span></span> <span data-ttu-id="b342d-146">Он основан на формате, привязанном к параметру *сркресаурце* (t \# ).</span><span class="sxs-lookup"><span data-stu-id="b342d-146">It is based on the format bound to the *srcResource* parameter (t\#).</span></span>

<span data-ttu-id="b342d-147">Как и в **образце** инструкции, возвращаемые значения для **ld2dms** — это 4-векторы с использованием значений по умолчанию, относящихся к формату для компонентов, отсутствующих в формате.</span><span class="sxs-lookup"><span data-stu-id="b342d-147">As with the **sample** instruction, returned values for **ld2dms** are 4-vectors with format-specific defaults for components not present in the format.</span></span> <span data-ttu-id="b342d-148">Свиззле On *сркресаурце* определяет, как свиззле результат из 4 компонентов, который возвращается из текстуры загрузки, после чего. Mask в *dest* определяет, какие компоненты в *dest* -обновлении будут обновлены.</span><span class="sxs-lookup"><span data-stu-id="b342d-148">The swizzle on *srcResource* determines how to swizzle the 4-component result coming back from the texture load, after which .mask on *dest* determines which components in *dest* get updated.</span></span>

<span data-ttu-id="b342d-149">При считывании 32-разрядного значения с плавающей запятой с помощью **ld2dms** в 32-разрядный регистр бит не затрагивается. то есть нормальные значения остаются ненормальными.</span><span class="sxs-lookup"><span data-stu-id="b342d-149">When a 32-bit float value is read by **ld2dms** into a 32-bit register, the bits are untouched; that is, denormal values remain denormal.</span></span> <span data-ttu-id="b342d-150">Это не похоже на **образец** инструкции.</span><span class="sxs-lookup"><span data-stu-id="b342d-150">This is unlike the **sample** instruction.</span></span>

### <a name="miscellaneous-details"></a><span data-ttu-id="b342d-151">Прочие сведения</span><span class="sxs-lookup"><span data-stu-id="b342d-151">Miscellaneous Details</span></span>

<span data-ttu-id="b342d-152">Так как фильтрация, связанная с этой инструкцией, отсутствует, такие понятия, как Лод-смещение, не применяются.</span><span class="sxs-lookup"><span data-stu-id="b342d-152">As there is no filtering associated with this instruction, concepts like LOD bias do not apply.</span></span> <span data-ttu-id="b342d-153">Таким образом, параметр *образца s \#* отсутствует.</span><span class="sxs-lookup"><span data-stu-id="b342d-153">Accordingly there is no *sampler s\#* parameter.</span></span>

### <a name="restrictions"></a><span data-ttu-id="b342d-154">Ограничения</span><span class="sxs-lookup"><span data-stu-id="b342d-154">Restrictions</span></span>

-   <span data-ttu-id="b342d-155">*сркресаурце* должен быть t- \# регистром, а не текстурекубе, Texture1D или Texture1DArray.</span><span class="sxs-lookup"><span data-stu-id="b342d-155">*srcResource* must be a t\# register, and not a TextureCube, Texture1D or Texture1DArray.</span></span> <span data-ttu-id="b342d-156">*сркресаурце* не может быть константбуффер, который не может быть привязан к \# регистрам t.</span><span class="sxs-lookup"><span data-stu-id="b342d-156">*srcResource* cannot be a ConstantBuffer, which cannot be bound to t\# registers.</span></span>
-   <span data-ttu-id="b342d-157">Относительная адресация в *сркресаурце* не разрешена.</span><span class="sxs-lookup"><span data-stu-id="b342d-157">Relative addressing on *srcResource* is not permitted.</span></span>
-   <span data-ttu-id="b342d-158">*сркаддресс* и *sampleIndex* должны быть временным (r \# /x \# ), постоянным (CB \# ) или входным (v \# ) регистром.</span><span class="sxs-lookup"><span data-stu-id="b342d-158">*srcAddress* and *sampleIndex* must be a temp (r\#/x\#), constant (cb\#) or input (v\#) register.</span></span>
-   <span data-ttu-id="b342d-159">*dest* должен быть временным (r \# /x \# ) или выходным \* \# регистром (o).</span><span class="sxs-lookup"><span data-stu-id="b342d-159">*dest* must be a temp (r\#/x\#) or output (o\*\#) register.</span></span>

<span data-ttu-id="b342d-160">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="b342d-160">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="b342d-161">Вершинный построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="b342d-161">Vertex Shader</span></span> | <span data-ttu-id="b342d-162">Шейдер геометрии</span><span class="sxs-lookup"><span data-stu-id="b342d-162">Geometry Shader</span></span> | <span data-ttu-id="b342d-163">Построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="b342d-163">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="b342d-164">x</span><span class="sxs-lookup"><span data-stu-id="b342d-164">x</span></span>             | <span data-ttu-id="b342d-165">x</span><span class="sxs-lookup"><span data-stu-id="b342d-165">x</span></span>               | <span data-ttu-id="b342d-166">x</span><span class="sxs-lookup"><span data-stu-id="b342d-166">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="b342d-167">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="b342d-167">Minimum Shader Model</span></span>

<span data-ttu-id="b342d-168">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="b342d-168">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="b342d-169">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="b342d-169">Shader Model</span></span>                                              | <span data-ttu-id="b342d-170">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="b342d-170">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="b342d-171">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="b342d-171">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="b342d-172">да</span><span class="sxs-lookup"><span data-stu-id="b342d-172">yes</span></span>       |
| [<span data-ttu-id="b342d-173">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="b342d-173">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="b342d-174">да</span><span class="sxs-lookup"><span data-stu-id="b342d-174">yes</span></span>       |
| [<span data-ttu-id="b342d-175">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="b342d-175">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="b342d-176">Нет</span><span class="sxs-lookup"><span data-stu-id="b342d-176">no</span></span>        |
| [<span data-ttu-id="b342d-177">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b342d-177">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="b342d-178">Нет</span><span class="sxs-lookup"><span data-stu-id="b342d-178">no</span></span>        |
| [<span data-ttu-id="b342d-179">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b342d-179">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="b342d-180">Нет</span><span class="sxs-lookup"><span data-stu-id="b342d-180">no</span></span>        |
| [<span data-ttu-id="b342d-181">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b342d-181">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="b342d-182">Нет</span><span class="sxs-lookup"><span data-stu-id="b342d-182">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="b342d-183">См. также</span><span class="sxs-lookup"><span data-stu-id="b342d-183">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b342d-184">Сборка Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b342d-184">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





