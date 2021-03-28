---
title: LD (SM4-ASM)
description: Извлекает данные из указанного буфера или текстуры без фильтрации (например, выборка точек), используя предоставленный целочисленный адрес. Исходные данные могут поступать из любого типа ресурсов, кроме Текстурекубе.
ms.assetid: DEE9A55F-EDFE-478E-8169-5BF9C43E98AF
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eaacc3d76d49cc2b3043d39036f0ff652d7b8794
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104335539"
---
# <a name="ld-sm4---asm"></a><span data-ttu-id="65af0-104">LD (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="65af0-104">ld (sm4 - asm)</span></span>

<span data-ttu-id="65af0-105">Извлекает данные из указанного буфера или текстуры без фильтрации (например, выборка точек), используя предоставленный целочисленный адрес.</span><span class="sxs-lookup"><span data-stu-id="65af0-105">Fetches data from the specified buffer or texture without any filtering (e.g. point sampling) using the provided integer address.</span></span> <span data-ttu-id="65af0-106">Исходные данные могут поступать из любого типа ресурсов, кроме Текстурекубе.</span><span class="sxs-lookup"><span data-stu-id="65af0-106">The source data may come from any resource type, other than TextureCube.</span></span>



| <span data-ttu-id="65af0-107">LD \[ \_ аоффимми (u, v, w) \] dest \[ . Mask \] , сркаддресс \[ . свиззле \] , сркресаурце \[ . свиззле\]</span><span class="sxs-lookup"><span data-stu-id="65af0-107">ld\[\_aoffimmi(u,v,w)\] dest\[.mask\], srcAddress\[.swizzle\], srcResource\[.swizzle\]</span></span> |
|----------------------------------------------------------------------------------------|



 



| <span data-ttu-id="65af0-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="65af0-108">Item</span></span>                                                                                                               | <span data-ttu-id="65af0-109">Описание</span><span class="sxs-lookup"><span data-stu-id="65af0-109">Description</span></span>                                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="65af0-110"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="65af0-110"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/>                                                    | <span data-ttu-id="65af0-111">\[в \] адресе результата операции.</span><span class="sxs-lookup"><span data-stu-id="65af0-111">\[in\] The address of the result of the operation.</span></span><br/>                                                               |
| <span data-ttu-id="65af0-112"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*сркаддресс*</span><span class="sxs-lookup"><span data-stu-id="65af0-112"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span></span><br/>     | <span data-ttu-id="65af0-113">\[в \] координатах текстуры, необходимых для выполнения примера.</span><span class="sxs-lookup"><span data-stu-id="65af0-113">\[in\] The texture coordinates needed to perform the sample.</span></span><br/>                                                     |
| <span data-ttu-id="65af0-114"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*сркресаурце*</span><span class="sxs-lookup"><span data-stu-id="65af0-114"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span></span><br/> | <span data-ttu-id="65af0-115">\[в \] регистре текстуры (t \# ), который должен быть объявлен, чтобы определить, из какой текстуры или буфера извлечь.</span><span class="sxs-lookup"><span data-stu-id="65af0-115">\[in\] A texture register (t\#) which must have been declared identifying which Texture or Buffer to fetch from.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="65af0-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="65af0-116">Remarks</span></span>

<span data-ttu-id="65af0-117">Эта инструкция является упрощенной альтернативой инструкции [образца](sample--sm4---asm-.md) .</span><span class="sxs-lookup"><span data-stu-id="65af0-117">This instruction is a simplified alternative to the [sample](sample--sm4---asm-.md) instruction.</span></span> <span data-ttu-id="65af0-118">В отличие от **Sample**, **LD** также может получать данные из буферов.</span><span class="sxs-lookup"><span data-stu-id="65af0-118">Unlike **sample**, **ld** is also capable of fetching data from buffers.</span></span> <span data-ttu-id="65af0-119">**LD** также может получать из нескольких выборок ресурсов (только в шейдере Pixel Shader).</span><span class="sxs-lookup"><span data-stu-id="65af0-119">**ld** is can also fetch from multi-sample resources (on pixel shader only).</span></span>

<span data-ttu-id="65af0-120">*сркаддресс* предоставляет набор координат текстуры, необходимых для выполнения образца в виде целых чисел без знака.</span><span class="sxs-lookup"><span data-stu-id="65af0-120">*srcAddress* provides the set of texture coordinates needed to perform the sample in the form of unsigned integers.</span></span> <span data-ttu-id="65af0-121">Если *сркаддресс* находится за пределами диапазона \[ 0... ( \# пикселей текстуры в измерении-1) \] , то вызывается поведение вне границ, где **LD** возвращает 0 во всех неотсутствующих компонентах формата *сркресаурце* и значение по умолчанию для отсутствующих компонентов.</span><span class="sxs-lookup"><span data-stu-id="65af0-121">If *srcAddress* is out of the range\[0...(\#texels in dimension -1)\], then out-of-bounds behavior is invoked, where **ld** returns 0 in all non-missing components of the format of the *srcResource*, and the default for missing components.</span></span> <span data-ttu-id="65af0-122">Приложение, которому необходимо более гибкое управление поведением адресов вне диапазона, должно использовать **образец** инструкции, так как он учитывает поведение перетекания адресов, зеркального отображения, среза или границы, определенного как состояние выборки.</span><span class="sxs-lookup"><span data-stu-id="65af0-122">An application wishing any more flexible control over out-of-range address behavior should use the **sample** instruction instead, as it honors address wrap/mirror/clamp/border behavior defined as sampler state.</span></span>

<span data-ttu-id="65af0-123">*сркаддресс. a* (POS-свиззле) всегда предоставляет Неподписанный целочисленный уровень mipmap.</span><span class="sxs-lookup"><span data-stu-id="65af0-123">*srcAddress.a* (POS-swizzle) always provides an unsigned integer mipmap level.</span></span> <span data-ttu-id="65af0-124">Если значение выходит за пределы диапазона \[ 0... ( Num миплевелс в Resource-1) \] ), то вызывается поведение вне границ.</span><span class="sxs-lookup"><span data-stu-id="65af0-124">If the value is out of the range \[0...(num miplevels in resource-1)\]), then out-of-bounds behavior is invoked.</span></span> <span data-ttu-id="65af0-125">Если ресурс является буфером, который не может иметь MIP-карты, то *сркаддресс. a* игнорируется.</span><span class="sxs-lookup"><span data-stu-id="65af0-125">If the resource is a buffer, which can not have any mipmaps, then *srcAddress.a* is ignored</span></span>

<span data-ttu-id="65af0-126">*сркаддресс. GB* (POS-свиззле) игнорируется для буферов и texture1D (кроме массива).</span><span class="sxs-lookup"><span data-stu-id="65af0-126">*srcAddress.gb* (POS-swizzle) is ignored for buffers and texture1D (non-Array).</span></span> <span data-ttu-id="65af0-127">*сркаддресс. b* (POS-свиззле) игнорируется для texture1D массивов и texture2Ds.</span><span class="sxs-lookup"><span data-stu-id="65af0-127">*srcAddress.b* (POS-swizzle) is ignored for texture1D arrays and texture2Ds.</span></span>

<span data-ttu-id="65af0-128">Для массивов texture1D *сркаддресс. g* (POS-свиззле) предоставляет индекс массива как целое число без знака.</span><span class="sxs-lookup"><span data-stu-id="65af0-128">For texture1D arrays, *srcAddress.g* (POS-swizzle) provides the array index as an unsigned integer.</span></span> <span data-ttu-id="65af0-129">Если значение выходит за пределы диапазона доступных индексов массива \[ 0... ( Размер массива — 1) \] , то вызывается поведение вне границ.</span><span class="sxs-lookup"><span data-stu-id="65af0-129">If the value is out of the range of available array indices \[0...(array size-1)\], then out-of-bounds behavior is invoked.</span></span>

<span data-ttu-id="65af0-130">Для массивов texture2D *сркаддресс. b* (POS-свиззле) предоставляет индекс массива, в противном случае — с той же семантикой, что и для texture1D.</span><span class="sxs-lookup"><span data-stu-id="65af0-130">For texture2D arrays, *srcAddress.b* (POS-swizzle) provides the array index, otherwise with same semantics as for texture1D.</span></span>

<span data-ttu-id="65af0-131">Выборка из *t \#* без привязки к ней возвращает значение 0 для всех компонентов.</span><span class="sxs-lookup"><span data-stu-id="65af0-131">Fetching from *t\#* that has nothing bound to it returns 0 for all components.</span></span>

### <a name="address-offset"></a><span data-ttu-id="65af0-132">Смещение адреса</span><span class="sxs-lookup"><span data-stu-id="65af0-132">Address Offset</span></span>

<span data-ttu-id="65af0-133">Необязательный \[ \_ суффикс аоффимми (u, v, w) \] (смещение адреса непосредственно целым числом) указывает, что координаты текстуры для **LD** должны быть смещены на набор предоставленных шаг текселя значений целых констант.</span><span class="sxs-lookup"><span data-stu-id="65af0-133">The optional \[\_aoffimmi(u,v,w)\] suffix (address offset by immediate integer) indicates that the texture coordinates for the **ld** are to be offset by a set of provided immediate texel space integer constant values.</span></span> <span data-ttu-id="65af0-134">Литеральные значения представляют собой набор из 4-разрядных чисел 2, имеющих целочисленный диапазон \[ — 8, 7 \] .</span><span class="sxs-lookup"><span data-stu-id="65af0-134">The literal values are a set of 4 bit 2's complement numbers, having integer range \[-8,7\].</span></span> <span data-ttu-id="65af0-135">Этот модификатор определен только для texture1D/2D/3D, включая массивы, а не для буферов.</span><span class="sxs-lookup"><span data-stu-id="65af0-135">This modifier is defined only for texture1D/2D/3D, including arrays, and not for buffers.</span></span>

<span data-ttu-id="65af0-136">Смещения добавляются к координатам текстуры в шаг текселя пространстве относительно миплевел, к которому обращается **LD**.</span><span class="sxs-lookup"><span data-stu-id="65af0-136">The offsets are added to the texture coordinates, in texel space, relative to the miplevel being accessed by the **ld**.</span></span>

<span data-ttu-id="65af0-137">Смещения адресов не применяются вдоль оси массива texture1D и двумерных массивов.</span><span class="sxs-lookup"><span data-stu-id="65af0-137">Address offsets are not applied along the array axis of texture1D/2D arrays.</span></span>

<span data-ttu-id="65af0-138">Компоненты *\_ аоффимми v, w* игнорируются для texture1Ds.</span><span class="sxs-lookup"><span data-stu-id="65af0-138">The *\_aoffimmi v,w* components are ignored for texture1Ds.</span></span>

<span data-ttu-id="65af0-139">Компонент *\_ аоффимми w* не учитывается для texture2Ds.</span><span class="sxs-lookup"><span data-stu-id="65af0-139">The *\_aoffimmi w* component is ignored for texture2Ds.</span></span>

<span data-ttu-id="65af0-140">Так как координаты текстуры для **LD** являются целыми числами без знака, если смещение приводит к тому, что адрес перейдется ниже нуля, он будет переноситься на большой адрес и приведет к выходу за пределы границ.</span><span class="sxs-lookup"><span data-stu-id="65af0-140">Because the texture coordinates for **ld** are unsigned integers, if the offset causes the address to go below zero, it will wrap to a large address, and result in an out of bounds access.</span></span>

### <a name="return-type-control"></a><span data-ttu-id="65af0-141">Контроль возвращаемого типа</span><span class="sxs-lookup"><span data-stu-id="65af0-141">Return Type Control</span></span>

<span data-ttu-id="65af0-142">Формат данных, возвращаемый **LD** в регистр назначения, определяется так же, как описано в **образце** инструкции. Он основан на формате, привязанном к параметру *сркресаурце* (*t \#*).</span><span class="sxs-lookup"><span data-stu-id="65af0-142">The data format returned by **ld** to the destination register is determined in the same way as described for the **sample** instruction; it is based on the format bound to the *srcResource* parameter (*t\#*).</span></span>

<span data-ttu-id="65af0-143">Как и в **примере** инструкции, возвращаемые значения для **LD** являются 4-векторами с заданными по умолчанию форматами для компонентов, которые не представлены в формате.</span><span class="sxs-lookup"><span data-stu-id="65af0-143">As with the **sample** instruction, returned values for **ld** are 4-vectors with format-specific defaults for components not present in the format.</span></span> <span data-ttu-id="65af0-144">Свиззле On *сркресаурце* определяет, как свиззле результат из 4 компонентов, который возвращается из текстуры загрузки, после чего. Mask в *dest* определяет, какие компоненты в *dest* -обновлении будут обновлены.</span><span class="sxs-lookup"><span data-stu-id="65af0-144">The swizzle on *srcResource* determines how to swizzle the 4-component result coming back from the texture load, after which .mask on *dest* determines which components in *dest* get updated.</span></span>

<span data-ttu-id="65af0-145">Если 32-разрядное значение с плавающей запятой *считывается в 32* -разрядный регистр, то биты не затрагиваются. то есть нормальные значения остаются ненормальными.</span><span class="sxs-lookup"><span data-stu-id="65af0-145">When a 32-bit float value is read by *ld* into a 32-bit register, the bits are untouched; that is, denormal values remain denormal.</span></span> <span data-ttu-id="65af0-146">Это не похоже на **образец** инструкции.</span><span class="sxs-lookup"><span data-stu-id="65af0-146">This is unlike the **sample** instruction.</span></span>

### <a name="miscellaneous-details"></a><span data-ttu-id="65af0-147">Прочие сведения</span><span class="sxs-lookup"><span data-stu-id="65af0-147">Miscellaneous Details</span></span>

<span data-ttu-id="65af0-148">Поскольку фильтрация, связанная с инструкцией **LD** , отсутствует, такие понятия, как Лод, не применяются к **LD**.</span><span class="sxs-lookup"><span data-stu-id="65af0-148">As there is no filtering associated with the **ld** instruction, concepts like LOD bias do not apply to **ld**.</span></span> <span data-ttu-id="65af0-149">Таким образом, параметр образца *s \#* отсутствует.</span><span class="sxs-lookup"><span data-stu-id="65af0-149">Accordingly there is no sampler *s\#* parameter.</span></span>

### <a name="restrictions"></a><span data-ttu-id="65af0-150">Ограничения</span><span class="sxs-lookup"><span data-stu-id="65af0-150">Restrictions</span></span>

-   <span data-ttu-id="65af0-151">*сркресаурце* должен быть t- \# регистром, а не текстурекубе.</span><span class="sxs-lookup"><span data-stu-id="65af0-151">*srcResource* must be a t\# register, and not a TextureCube.</span></span> <span data-ttu-id="65af0-152">*сркресаурце* не может иметь значение константбуффер, которое не может быть привязано к \# регистрам t.</span><span class="sxs-lookup"><span data-stu-id="65af0-152">*srcResource* cannot be a constantbuffer either, which cannot be bound to t\# registers.</span></span>
-   <span data-ttu-id="65af0-153">Относительная адресация в *сркресаурце* не разрешена.</span><span class="sxs-lookup"><span data-stu-id="65af0-153">Relative addressing on *srcResource* is not permitted.</span></span>
-   <span data-ttu-id="65af0-154">*сркаддресс* должен быть временным (r \# /x \# ), постоянным (CB \# ) или входным (v \# ) регистром.</span><span class="sxs-lookup"><span data-stu-id="65af0-154">*srcAddress* must be a temp (r\#/x\#), constant (cb\#) or input (v\#) register.</span></span>
-   <span data-ttu-id="65af0-155">*dest* должен быть временным (r \# /x \# ) или выходным \* \# регистром (o).</span><span class="sxs-lookup"><span data-stu-id="65af0-155">*dest* must be a temp (r\#/x\#) or output (o\*\#) register.</span></span>

<span data-ttu-id="65af0-156">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="65af0-156">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="65af0-157">Вершинный построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="65af0-157">Vertex Shader</span></span> | <span data-ttu-id="65af0-158">Шейдер геометрии</span><span class="sxs-lookup"><span data-stu-id="65af0-158">Geometry Shader</span></span> | <span data-ttu-id="65af0-159">Построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="65af0-159">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="65af0-160">x</span><span class="sxs-lookup"><span data-stu-id="65af0-160">x</span></span>             | <span data-ttu-id="65af0-161">x</span><span class="sxs-lookup"><span data-stu-id="65af0-161">x</span></span>               | <span data-ttu-id="65af0-162">x</span><span class="sxs-lookup"><span data-stu-id="65af0-162">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="65af0-163">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="65af0-163">Minimum Shader Model</span></span>

<span data-ttu-id="65af0-164">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="65af0-164">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="65af0-165">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="65af0-165">Shader Model</span></span>                                              | <span data-ttu-id="65af0-166">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="65af0-166">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="65af0-167">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="65af0-167">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="65af0-168">да</span><span class="sxs-lookup"><span data-stu-id="65af0-168">yes</span></span>       |
| [<span data-ttu-id="65af0-169">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="65af0-169">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="65af0-170">да</span><span class="sxs-lookup"><span data-stu-id="65af0-170">yes</span></span>       |
| [<span data-ttu-id="65af0-171">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="65af0-171">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="65af0-172">да</span><span class="sxs-lookup"><span data-stu-id="65af0-172">yes</span></span>       |
| [<span data-ttu-id="65af0-173">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="65af0-173">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="65af0-174">Нет</span><span class="sxs-lookup"><span data-stu-id="65af0-174">no</span></span>        |
| [<span data-ttu-id="65af0-175">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="65af0-175">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="65af0-176">Нет</span><span class="sxs-lookup"><span data-stu-id="65af0-176">no</span></span>        |
| [<span data-ttu-id="65af0-177">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="65af0-177">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="65af0-178">Нет</span><span class="sxs-lookup"><span data-stu-id="65af0-178">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="65af0-179">См. также</span><span class="sxs-lookup"><span data-stu-id="65af0-179">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="65af0-180">Сборка Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="65af0-180">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





