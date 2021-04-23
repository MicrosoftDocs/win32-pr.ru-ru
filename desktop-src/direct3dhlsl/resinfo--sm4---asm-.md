---
title: 'Resinfo: (SM4-ASM)'
description: Запрашивает размеры заданного входного ресурса.
ms.assetid: 5D549AC6-E0CB-4395-953C-5E5ECEEE234D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a252195a4b59ed791f6ac625fe1d95bbd9925f1
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104412164"
---
# <a name="resinfo-sm4---asm"></a><span data-ttu-id="6eec2-103">Resinfo: (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="6eec2-103">resinfo (sm4 - asm)</span></span>

<span data-ttu-id="6eec2-104">Запрашивает размеры заданного входного ресурса.</span><span class="sxs-lookup"><span data-stu-id="6eec2-104">Query the dimensions of a given input resource.</span></span>



| <span data-ttu-id="6eec2-105">Resinfo: \[ \_ uint </span><span class="sxs-lookup"><span data-stu-id="6eec2-105">resinfo\[\_uint</span></span>\|<span data-ttu-id="6eec2-106">\_Ркпфлоат \] dest \[ . Mask \] , сркмиплевел. Выбор \_ компонента, сркресаурце \[ . свиззле\]</span><span class="sxs-lookup"><span data-stu-id="6eec2-106">\_rcpFloat\] dest\[.mask\], srcMipLevel.select\_component, srcResource\[.swizzle\]</span></span> |
|-----------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="6eec2-107">Элемент</span><span class="sxs-lookup"><span data-stu-id="6eec2-107">Item</span></span>                                                                                                               | <span data-ttu-id="6eec2-108">Описание</span><span class="sxs-lookup"><span data-stu-id="6eec2-108">Description</span></span>                                                                               |
|--------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="6eec2-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="6eec2-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/>                                                    | <span data-ttu-id="6eec2-110">\[в \] адресе результата операции.</span><span class="sxs-lookup"><span data-stu-id="6eec2-110">\[in\] The address of the result of the operation.</span></span><br/>                             |
| <span data-ttu-id="6eec2-111"><span id="srcMipLevel"></span><span id="srcmiplevel"></span><span id="SRCMIPLEVEL"></span>*сркмиплевел*</span><span class="sxs-lookup"><span data-stu-id="6eec2-111"><span id="srcMipLevel"></span><span id="srcmiplevel"></span><span id="SRCMIPLEVEL"></span>*srcMipLevel*</span></span><br/> | <span data-ttu-id="6eec2-112">\[на \] уровне MIP.</span><span class="sxs-lookup"><span data-stu-id="6eec2-112">\[in\] The mip level.</span></span><br/>                                                          |
| <span data-ttu-id="6eec2-113"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*сркресаурце*</span><span class="sxs-lookup"><span data-stu-id="6eec2-113"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span></span><br/> | <span data-ttu-id="6eec2-114">\[в \] \# текстуре ввода t или u, \# для которой запрашиваются измерения.</span><span class="sxs-lookup"><span data-stu-id="6eec2-114">\[in\] A t\# or u\# input texture for which the dimensions are being queried.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="6eec2-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="6eec2-115">Remarks</span></span>

<span data-ttu-id="6eec2-116">*сркмиплевел* считывается как скалярное целое число без знака, поэтому для исходного регистра требуется один селектор компонента, если он не является скалярным непосредственным значением.</span><span class="sxs-lookup"><span data-stu-id="6eec2-116">*srcMipLevel* is read as an unsigned integer scalar so a single component selector is required for the source register, if it is not a scalar immediate value.</span></span>

<span data-ttu-id="6eec2-117">*dest* получает \[ ширину, высоту, глубину или размер массива, Total — MIP-Count \] , выделенную маской записи.</span><span class="sxs-lookup"><span data-stu-id="6eec2-117">*dest* receives \[width, height, depth or array size, total-mip-count\], selected by the write mask.</span></span>

<span data-ttu-id="6eec2-118">Возвращенные значения ширины, высоты и глубины предназначены для MIP уровня, выбранного параметром *сркмиплевел* , и находятся в пикселей текстуры, независимо от размера данных шаг текселя.</span><span class="sxs-lookup"><span data-stu-id="6eec2-118">The returned width, height and depth values are for the mip-level selected by the *srcMipLevel* parameter, and are in number of texels, independent of texel data size.</span></span> <span data-ttu-id="6eec2-119">Для многовыборочных ресурсов (texture2D \[ array \] MS \# ) Ширина и высота также возвращаются в пикселей текстуры, а не в образцах.</span><span class="sxs-lookup"><span data-stu-id="6eec2-119">For multisample resources (texture2D\[Array\]MS\#), width and height are also returned in texels, not samples.</span></span>

<span data-ttu-id="6eec2-120">Параметр *сркмиплевел* не влияет на общее число MIP, возвращенное в *dest. w* .</span><span class="sxs-lookup"><span data-stu-id="6eec2-120">The total mip count returned in *dest.w* is unaffected by the *srcMipLevel* parameter.</span></span>

<span data-ttu-id="6eec2-121">Для Уавс (u \# ) число уровней MIP всегда равно 1.</span><span class="sxs-lookup"><span data-stu-id="6eec2-121">For UAVs (u\#), the number of mip levels is always 1.</span></span>

<span data-ttu-id="6eec2-122">Все аспекты этой инструкции основаны на характеристиках представления ресурсов, привязанных к t \# /u, а \# не базовому базовому ресурсу.</span><span class="sxs-lookup"><span data-stu-id="6eec2-122">All aspects of this instruction are based on the characteristics of the resource view bound at the t\#/u\#, not the underlying base resource.</span></span>

<span data-ttu-id="6eec2-123">Возвращаемые значения — это все операции с плавающей запятой, если \_ не используется модификатор uint. в этом случае возвращаемые значения являются целыми числами.</span><span class="sxs-lookup"><span data-stu-id="6eec2-123">Returned values are all floating point, unless the \_uint modifier is used, in which case the returned values are all integers.</span></span> <span data-ttu-id="6eec2-124">Если \_ используется модификатор ркпфлоат, то все возвращаемые значения являются плавающей запятой, а ширина, высота и глубина возвращаются в виде обратных значений (1,0 f/Width, 1,0 f/Height, 1,0 f/Depth), включая INF, если ширина, высота или глубина равны 0 от поведения *сркмиплевел* вне допустимого диапазона.</span><span class="sxs-lookup"><span data-stu-id="6eec2-124">If the \_rcpFloat modifier is used, all returned values are floating point, and the width, height and depth are returned as reciprocals (1.0f/width, 1.0f/height, 1.0f/depth), including INF if width/height/depth are 0 from out-of-range *srcMipLevel* behavior.</span></span> <span data-ttu-id="6eec2-125">\_Модификатор ркпфлоат применяется только к возвращаемым значениям ширины, высоты и глубины и не применяется к значениям, равным 0 и, таким же, не возвращается и не применяется к возвращению размера массива.</span><span class="sxs-lookup"><span data-stu-id="6eec2-125">The \_rcpFloat modifier only applies to width, height, and depth returned values and does not apply to values that are set to 0 and thus not returned, and also does not apply to array size returns.</span></span>

<span data-ttu-id="6eec2-126">Свиззле On *сркресаурце* позволяет свиззлед возвращаемые значения произвольно, прежде чем они записываются в место назначения.</span><span class="sxs-lookup"><span data-stu-id="6eec2-126">The swizzle on *srcResource* allows the returned values to be swizzled arbitrarily before they are written to the destination.</span></span>

<span data-ttu-id="6eec2-127">Если *сркресаурце* является Texture1D, то значение Width возвращается в *dest. x*, а *dest. из* — в 0.</span><span class="sxs-lookup"><span data-stu-id="6eec2-127">If *srcResource* is a Texture1D, then width is returned in *dest.x*, and *dest.yz* are set to 0.</span></span>

<span data-ttu-id="6eec2-128">Если *сркресаурце* является Texture1DArray, то значение Width возвращается в *dest. x*, а размер массива возвращается в *dest. y*, а *dest. z* — в 0.</span><span class="sxs-lookup"><span data-stu-id="6eec2-128">If *srcResource* is a Texture1DArray, then width is returned in *dest.x*, the array size is returned in *dest.y*, and *dest.z* is set to 0.</span></span>

<span data-ttu-id="6eec2-129">Если *сркресаурце* является Texture2D, то ширина и высота возвращаются в *dest. XY*, а для *dest. z* устанавливается значение 0.</span><span class="sxs-lookup"><span data-stu-id="6eec2-129">If *srcResource* is a Texture2D, then width and height are returned in *dest.xy*, and *dest.z* is set to 0.</span></span>

<span data-ttu-id="6eec2-130">Если *сркресаурце* является Texture2DArray, то ширина и высота возвращаются в *dest. XY*, а размер массива возвращается в *dest. z*.</span><span class="sxs-lookup"><span data-stu-id="6eec2-130">If *srcResource* is a Texture2DArray, then width and height are returned in *dest.xy*, and the array size is returned in *dest.z*.</span></span>

<span data-ttu-id="6eec2-131">Если *сркресаурце* является Texture3D, то ширина, высота и глубина возвращаются в *dest.XYZ*.</span><span class="sxs-lookup"><span data-stu-id="6eec2-131">If *srcResource* is a Texture3D, then width, height and depth are returned in *dest.xyz*.</span></span>

<span data-ttu-id="6eec2-132">Если *сркресаурце* является текстурекубе, то ширина и высота индивидуальных измерений куба возвращаются в *dest. XY*, а для *dest. z* устанавливается значение 0.</span><span class="sxs-lookup"><span data-stu-id="6eec2-132">If *srcResource* is a TextureCube, then the width and height of the individual cube face dimensions are returned in *dest.xy*, and *dest.z* is set to 0.</span></span>

<span data-ttu-id="6eec2-133">Если *сркресаурце* является текстурекубеаррай, то ширина и высота каждого измерения грани куба возвращаются в *dest. XY*.</span><span class="sxs-lookup"><span data-stu-id="6eec2-133">If *srcResource* is a TextureCubeArray, then the width and height the individual cube face dimensions are returned in *dest.xy*.</span></span> <span data-ttu-id="6eec2-134">для *dest. z* задано неопределенное значение.</span><span class="sxs-lookup"><span data-stu-id="6eec2-134">*dest.z* is set to an undefined value.</span></span>

<span data-ttu-id="6eec2-135">Если в *сркресаурце* был указан mipный срез для каждого ресурса, Resinfo: всегда возвращает общее число MIP-карты в представлении для счетчика MIP, независимо от среза.</span><span class="sxs-lookup"><span data-stu-id="6eec2-135">If the a per-resource mip clamp has been specified on *srcResource*, resinfo always returns the total number of mipmaps in the view for the mip count, regardless of the clamp.</span></span> <span data-ttu-id="6eec2-136">Однако, если размеры заданных миплевел запрашиваются Resinfo: и миплевел был обрезан (например, в 2,2 означает, что MIPS 0 и 1 были обрезаны), возвращаемые измерения не определены.</span><span class="sxs-lookup"><span data-stu-id="6eec2-136">However, if the dimensions of a given miplevel are requested by resinfo and the miplevel has been clamped off (e.g. a clamp of 2.2 means that mips 0 and 1 have been clamped off), the dimensions returned are undefined.</span></span> <span data-ttu-id="6eec2-137">Некоторые реализации возвращают поведение вне границ, указанное для Resinfo:, если миплевел выходит за пределы допустимого диапазона.</span><span class="sxs-lookup"><span data-stu-id="6eec2-137">Some implementations will return the out of bounds behavior specified for resinfo when the miplevel is out of range.</span></span> <span data-ttu-id="6eec2-138">Другие реализации возвращают размеры MIP, как если бы оно не было в виде фиксации.</span><span class="sxs-lookup"><span data-stu-id="6eec2-138">Other implementations will return the dimensions of the mip as if it had not been clamped.</span></span>

### <a name="restrictions"></a><span data-ttu-id="6eec2-139">Ограничения</span><span class="sxs-lookup"><span data-stu-id="6eec2-139">Restrictions</span></span>

-   <span data-ttu-id="6eec2-140">*сркресаурце* должен быть \# регистром t или u \# , который не является буфером, но является текстурой \* .</span><span class="sxs-lookup"><span data-stu-id="6eec2-140">*srcResource* must be a t\# or u\# register that is not a Buffer, but is a Texture\*.</span></span>
-   <span data-ttu-id="6eec2-141">Относительная адресация *сркресаурце* не разрешена.</span><span class="sxs-lookup"><span data-stu-id="6eec2-141">Relative addressing of *srcResource* is not permitted.</span></span>
-   <span data-ttu-id="6eec2-142">*сркмиплевел* должен использовать один селектор компонента, если он не является скалярным.</span><span class="sxs-lookup"><span data-stu-id="6eec2-142">*srcMipLevel* must use a single component selector if it is not a scalar immediate.</span></span>
-   <span data-ttu-id="6eec2-143">Выборка из t \# или u \# без привязки к нему возвращает 0 для ширины, высоты, глубины или размера массива и Total-MIP-Count.</span><span class="sxs-lookup"><span data-stu-id="6eec2-143">Fetching from t\# or u\# that has nothing bound to it returns 0 for width, height, depth or arraysize, and total-mip-count.</span></span> <span data-ttu-id="6eec2-144">\_Модификатор ркпфлоат по-прежнему учитывается в этом случае, поэтому ВОЗВРАЩАЕТ INF для применимых возвращаемых значений.</span><span class="sxs-lookup"><span data-stu-id="6eec2-144">The \_rcpFloat modifier is still honored in this case, thus returning INF for the applicable returned values.</span></span>
-   <span data-ttu-id="6eec2-145">Если *сркмиплевел* находится за пределами диапазона доступного числа миплевелс в ресурсе, поведение для возврата размера (*dest.XYZ*) идентично отношению к несвязанному \# ресурсу t или u \# .</span><span class="sxs-lookup"><span data-stu-id="6eec2-145">If *srcMipLevel* is out of the range of the available number of miplevels in the resource, the behavior for the size return (*dest.xyz*) is identical to that of an unbound t\# or u\# resource.</span></span> <span data-ttu-id="6eec2-146">В этом случае в *dest. w* по-прежнему возвращается общее число MIP.</span><span class="sxs-lookup"><span data-stu-id="6eec2-146">The total mip count is still returned in *dest.w* for this case.</span></span>

<span data-ttu-id="6eec2-147">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="6eec2-147">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="6eec2-148">Вершинный построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="6eec2-148">Vertex Shader</span></span> | <span data-ttu-id="6eec2-149">Шейдер геометрии</span><span class="sxs-lookup"><span data-stu-id="6eec2-149">Geometry Shader</span></span> | <span data-ttu-id="6eec2-150">Построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="6eec2-150">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="6eec2-151">x</span><span class="sxs-lookup"><span data-stu-id="6eec2-151">x</span></span>             | <span data-ttu-id="6eec2-152">x</span><span class="sxs-lookup"><span data-stu-id="6eec2-152">x</span></span>               | <span data-ttu-id="6eec2-153">x</span><span class="sxs-lookup"><span data-stu-id="6eec2-153">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="6eec2-154">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="6eec2-154">Minimum Shader Model</span></span>

<span data-ttu-id="6eec2-155">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="6eec2-155">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="6eec2-156">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="6eec2-156">Shader Model</span></span>                                              | <span data-ttu-id="6eec2-157">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="6eec2-157">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="6eec2-158">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="6eec2-158">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="6eec2-159">да</span><span class="sxs-lookup"><span data-stu-id="6eec2-159">yes</span></span>       |
| [<span data-ttu-id="6eec2-160">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="6eec2-160">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="6eec2-161">да</span><span class="sxs-lookup"><span data-stu-id="6eec2-161">yes</span></span>       |
| [<span data-ttu-id="6eec2-162">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="6eec2-162">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="6eec2-163">да</span><span class="sxs-lookup"><span data-stu-id="6eec2-163">yes</span></span>       |
| [<span data-ttu-id="6eec2-164">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6eec2-164">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="6eec2-165">Нет</span><span class="sxs-lookup"><span data-stu-id="6eec2-165">no</span></span>        |
| [<span data-ttu-id="6eec2-166">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6eec2-166">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="6eec2-167">Нет</span><span class="sxs-lookup"><span data-stu-id="6eec2-167">no</span></span>        |
| [<span data-ttu-id="6eec2-168">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6eec2-168">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="6eec2-169">Нет</span><span class="sxs-lookup"><span data-stu-id="6eec2-169">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="6eec2-170">См. также</span><span class="sxs-lookup"><span data-stu-id="6eec2-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6eec2-171">Сборка Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6eec2-171">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





