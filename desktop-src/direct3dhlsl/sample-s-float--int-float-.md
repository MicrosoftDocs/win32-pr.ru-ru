---
title: Функция Sample (S, float, int, float) (Справочник по HLSL)
description: Примеры Texture2D с необязательным значением для фиксации примера значения уровня детализации (Лод) в.
ms.assetid: 899FACB6-40BB-471B-82A7-BDBBC63B206E
keywords:
- Пример функции HLSL
topic_type:
- apiref
api_name:
- Sample
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e5c151c3d93f5e2fe374f0f60fd06798cf1ce52a
ms.sourcegitcommit: 0d6365d4e852b09a9100d9cfb9a5334922ebf478
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/17/2020
ms.locfileid: "104134819"
---
# <a name="samplesfloatintfloat-function-hlsl-reference"></a><span data-ttu-id="817bf-104">Функция Sample (S, float, int, float) (Справочник по HLSL)</span><span class="sxs-lookup"><span data-stu-id="817bf-104">Sample(S,float,int,float) function (HLSL reference)</span></span>

<span data-ttu-id="817bf-105">Примеры [**Texture2D**](sm5-object-texture2d.md) с необязательным значением для фиксации примера значения уровня детализации (Лод) в.</span><span class="sxs-lookup"><span data-stu-id="817bf-105">Samples a [**Texture2D**](sm5-object-texture2d.md) with an optional value to clamp sample level-of-detail (LOD) values to.</span></span>

> [!Note]  
> <span data-ttu-id="817bf-106">Требуется [модель шейдера 5](d3d11-graphics-reference-sm5.md) или более поздняя.</span><span class="sxs-lookup"><span data-stu-id="817bf-106">Requires [shader model 5](d3d11-graphics-reference-sm5.md) or higher.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="817bf-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="817bf-107">Syntax</span></span>

``` syntax
DXGI_FORMAT Sample(
  in SamplerState S,
  in float Location,
  in int Offset,
  in float Clamp
);
```

## <a name="parameters"></a><span data-ttu-id="817bf-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="817bf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="817bf-109">*S* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="817bf-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="817bf-110">[Состояние образца](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="817bf-110">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="817bf-111">Это объект, объявленный в файле эффектов, который содержит назначения состояний.</span><span class="sxs-lookup"><span data-stu-id="817bf-111">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="817bf-112">*Расположение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="817bf-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="817bf-113">Координаты текстуры.</span><span class="sxs-lookup"><span data-stu-id="817bf-113">The texture coordinates.</span></span> <span data-ttu-id="817bf-114">Тип аргумента зависит от типа объекта текстуры.</span><span class="sxs-lookup"><span data-stu-id="817bf-114">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="817bf-115">Тип Texture-Object</span><span class="sxs-lookup"><span data-stu-id="817bf-115">Texture-Object Type</span></span>                    | <span data-ttu-id="817bf-116">Тип параметра</span><span class="sxs-lookup"><span data-stu-id="817bf-116">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="817bf-117">Texture1D</span><span class="sxs-lookup"><span data-stu-id="817bf-117">Texture1D</span></span>                              | <span data-ttu-id="817bf-118">FLOAT</span><span class="sxs-lookup"><span data-stu-id="817bf-118">float</span></span>          |
| <span data-ttu-id="817bf-119">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="817bf-119">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="817bf-120">float2</span><span class="sxs-lookup"><span data-stu-id="817bf-120">float2</span></span>         |
| <span data-ttu-id="817bf-121">Texture2DArray, Texture3D, Текстурекубе</span><span class="sxs-lookup"><span data-stu-id="817bf-121">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="817bf-122">float3</span><span class="sxs-lookup"><span data-stu-id="817bf-122">float3</span></span>         |
| <span data-ttu-id="817bf-123">текстурекубеаррай</span><span class="sxs-lookup"><span data-stu-id="817bf-123">TextureCubeArray</span></span>                       | <span data-ttu-id="817bf-124">float4</span><span class="sxs-lookup"><span data-stu-id="817bf-124">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="817bf-125">*Смещение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="817bf-125">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="817bf-126">Необязательное Смещение координаты текстуры, которое может использоваться для любого типа объекта текстуры. смещение применяется к расположению перед выборкой.</span><span class="sxs-lookup"><span data-stu-id="817bf-126">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="817bf-127">Смещение текстуры должно быть статическим.</span><span class="sxs-lookup"><span data-stu-id="817bf-127">The texture offsets need to be static.</span></span> <span data-ttu-id="817bf-128">Тип аргумента зависит от типа объекта текстуры.</span><span class="sxs-lookup"><span data-stu-id="817bf-128">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="817bf-129">Дополнительные сведения см. в разделе [применение смещения координат текстуры](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="817bf-129">For more info, see [Applying texture coordinate offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="817bf-130">Тип Texture-Object</span><span class="sxs-lookup"><span data-stu-id="817bf-130">Texture-Object Type</span></span>           | <span data-ttu-id="817bf-131">Тип параметра</span><span class="sxs-lookup"><span data-stu-id="817bf-131">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="817bf-132">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="817bf-132">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="817bf-133">INT</span><span class="sxs-lookup"><span data-stu-id="817bf-133">int</span></span>            |
| <span data-ttu-id="817bf-134">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="817bf-134">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="817bf-135">int2</span><span class="sxs-lookup"><span data-stu-id="817bf-135">int2</span></span>           |
| <span data-ttu-id="817bf-136">Texture3D</span><span class="sxs-lookup"><span data-stu-id="817bf-136">Texture3D</span></span>                     | <span data-ttu-id="817bf-137">int3</span><span class="sxs-lookup"><span data-stu-id="817bf-137">int3</span></span>           |
| <span data-ttu-id="817bf-138">Текстурекубе, Текстурекубеаррай</span><span class="sxs-lookup"><span data-stu-id="817bf-138">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="817bf-139">не поддерживается</span><span class="sxs-lookup"><span data-stu-id="817bf-139">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="817bf-140">*Срез* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="817bf-140">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="817bf-141">Необязательное значение для примера среза Лод значений.</span><span class="sxs-lookup"><span data-stu-id="817bf-141">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="817bf-142">Например, если передать значение среза 2.0 f, вы убедитесь, что ни один из отдельных примеров не имеет доступа к MIP уровню менее 2.0.</span><span class="sxs-lookup"><span data-stu-id="817bf-142">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="817bf-143">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="817bf-143">Return value</span></span>

<span data-ttu-id="817bf-144">Формат текстуры, который является одним из типизированных значений, перечисленных в [**\_ формате DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="817bf-144">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="remarks"></a><span data-ttu-id="817bf-145">Примечания</span><span class="sxs-lookup"><span data-stu-id="817bf-145">Remarks</span></span>

<span data-ttu-id="817bf-146">Выбор текстуры использует расположение шаг текселя для поиска значения шаг текселя.</span><span class="sxs-lookup"><span data-stu-id="817bf-146">Texture sampling uses the texel position to look up a texel value.</span></span> <span data-ttu-id="817bf-147">Смещение можно применить к положению перед подстановкой.</span><span class="sxs-lookup"><span data-stu-id="817bf-147">An offset can be applied to the position before lookup.</span></span> <span data-ttu-id="817bf-148">Состояние образца содержит параметры выборки и фильтрации.</span><span class="sxs-lookup"><span data-stu-id="817bf-148">The sampler state contains the sampling and filtering options.</span></span> <span data-ttu-id="817bf-149">Этот метод может быть вызван в шейдере пикселей, но не поддерживается в шейдере вершин или шейдере Geometry.</span><span class="sxs-lookup"><span data-stu-id="817bf-149">This method can be invoked within a pixel shader, but it is not supported in a vertex shader or a geometry shader.</span></span>

<span data-ttu-id="817bf-150">Используйте смещение только с целочисленным миплевел; в противном случае вы можете получить разные результаты в зависимости от аппаратной реализации или параметров драйверов.</span><span class="sxs-lookup"><span data-stu-id="817bf-150">Use an offset only at an integer miplevel; otherwise, you may get different results depending on hardware implementation or driver settings.</span></span>

### <a name="calculating-texel-positions"></a><span data-ttu-id="817bf-151">Вычисление позиций шаг текселя</span><span class="sxs-lookup"><span data-stu-id="817bf-151">Calculating Texel Positions</span></span>

<span data-ttu-id="817bf-152">Координаты текстуры — это значения с плавающей запятой, которые ссылаются на данные текстуры, которые также называются нормализованной областью текстуры.</span><span class="sxs-lookup"><span data-stu-id="817bf-152">Texture coordinates are floating-point values that reference texture data, which is also known as normalized texture space.</span></span> <span data-ttu-id="817bf-153">Режимы переноса адреса применяются в этом порядке (координаты текстуры + смещения + режим переноса) для изменения координат текстуры за пределами \[ диапазона 0... 1 \] .</span><span class="sxs-lookup"><span data-stu-id="817bf-153">Address wrapping modes are applied in this order (texture coordinates + offsets + wrap mode) to modify texture coordinates outside the \[0...1\] range.</span></span>

<span data-ttu-id="817bf-154">Для массивов текстуры дополнительное значение параметра Location указывает индекс в массиве текстуры.</span><span class="sxs-lookup"><span data-stu-id="817bf-154">For texture arrays, an additional value in the location parameter specifies an index into a texture array.</span></span> <span data-ttu-id="817bf-155">Этот индекс рассматривается как масштабированное значение с плавающей запятой (вместо нормализованного пространства для стандартных координат текстуры).</span><span class="sxs-lookup"><span data-stu-id="817bf-155">This index is treated as a scaled float value (instead of the normalized space for standard texture coordinates).</span></span> <span data-ttu-id="817bf-156">Преобразование в целочисленный индекс выполняется в следующем порядке (float + Round-To-ближайшего-четного целое число + срез в диапазон массива).</span><span class="sxs-lookup"><span data-stu-id="817bf-156">The conversion to an integer index is done in the following order (float + round-to-nearest-even integer + clamp to the array range).</span></span>

### <a name="applying-texture-coordinate-offsets"></a><span data-ttu-id="817bf-157">Применение смещений для координат текстуры</span><span class="sxs-lookup"><span data-stu-id="817bf-157">Applying Texture Coordinate Offsets</span></span>

<span data-ttu-id="817bf-158">Параметр offset изменяет координаты текстуры в шаг текселя пространстве.</span><span class="sxs-lookup"><span data-stu-id="817bf-158">The offset parameter modifies the texture coordinates, in texel space.</span></span> <span data-ttu-id="817bf-159">Несмотря на то, что координаты текстуры являются нормализованными числами с плавающей запятой, смещение применяет целочисленное смещение.</span><span class="sxs-lookup"><span data-stu-id="817bf-159">Even though texture coordinates are normalized floating-point numbers, the offset applies an integer offset.</span></span> <span data-ttu-id="817bf-160">Также обратите внимание, что смещение текстуры должно быть статическим.</span><span class="sxs-lookup"><span data-stu-id="817bf-160">Also note that the texture offsets need to be static.</span></span>

<span data-ttu-id="817bf-161">Возвращаемый формат данных определяется форматом текстуры.</span><span class="sxs-lookup"><span data-stu-id="817bf-161">The data format returned is determined by the texture format.</span></span> <span data-ttu-id="817bf-162">Например, если ресурс текстуры был определен в \_ \_ формате DXGI A8B8G8R8 \_ UNORM \_ sRGB, операция выборки преобразует пример пикселей текстуры из гаммы 2,0 в 1,0, отфильтрует и записывает результат в виде значения с плавающей запятой в диапазоне \[ 0.. 1 \] .</span><span class="sxs-lookup"><span data-stu-id="817bf-162">For example, if the texture resource was defined with the DXGI\_FORMAT\_A8B8G8R8\_UNORM\_SRGB format, the sampling operation converts sampled texels from gamma 2.0 to 1.0, filter, and writes the result as a floating-point value in the range \[0..1\].</span></span>

<span data-ttu-id="817bf-163">Используйте смещение только с целочисленным миплевел; в противном случае можно получить результаты, которые не могут быть правильно преобразованы в оборудование.</span><span class="sxs-lookup"><span data-stu-id="817bf-163">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span>

## <a name="see-also"></a><span data-ttu-id="817bf-164">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="817bf-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="817bf-165">Примеры методов</span><span class="sxs-lookup"><span data-stu-id="817bf-165">Sample methods</span></span>](texture-sample-overload.md)
</dt> <dt>

[<span data-ttu-id="817bf-166">Текстура-объект</span><span class="sxs-lookup"><span data-stu-id="817bf-166">Texture-Object</span></span>](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

 
