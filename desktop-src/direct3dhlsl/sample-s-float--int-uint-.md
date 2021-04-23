---
title: Sample (S, float, int, float, uint), функция (Справочник по HLSL)
description: Пример Texture2D с необязательным значением для фиксации в примере значений уровня детализации (Лод) до и возвращает состояние операции.
ms.assetid: 1B9F48C4-DDB9-4547-B4AF-81A3ADA44C3F
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
ms.openlocfilehash: 9b378cb4031acecb8e0018053c7547e1948cc3e6
ms.sourcegitcommit: 0d6365d4e852b09a9100d9cfb9a5334922ebf478
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/17/2020
ms.locfileid: "103797563"
---
# <a name="samplesfloatintfloatuint-function-hlsl-reference"></a><span data-ttu-id="53244-104">Sample (S, float, int, float, uint), функция (Справочник по HLSL)</span><span class="sxs-lookup"><span data-stu-id="53244-104">Sample(S,float,int,float,uint) function (HLSL reference)</span></span>

<span data-ttu-id="53244-105">Пример [**Texture2D**](sm5-object-texture2d.md) с необязательным значением для фиксации в примере значений уровня детализации (Лод) до и возвращает состояние операции.</span><span class="sxs-lookup"><span data-stu-id="53244-105">Samples a [**Texture2D**](sm5-object-texture2d.md) with an optional value to clamp sample level-of-detail (LOD) values to, and returns status of the operation.</span></span>

> [!Note]  
> <span data-ttu-id="53244-106">Требуется [модель шейдера 5](d3d11-graphics-reference-sm5.md) или более поздняя.</span><span class="sxs-lookup"><span data-stu-id="53244-106">Requires [shader model 5](d3d11-graphics-reference-sm5.md) or higher.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="53244-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="53244-107">Syntax</span></span>

``` syntax
DXGI_FORMAT Sample(
  in  SamplerState S,
  in  float Location,
  in  int Offset,
  in  float Clamp,
  out uint Status
);
```

## <a name="parameters"></a><span data-ttu-id="53244-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="53244-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53244-109">*S* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="53244-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53244-110">[Состояние образца](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="53244-110">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="53244-111">Это объект, объявленный в файле эффектов, который содержит назначения состояний.</span><span class="sxs-lookup"><span data-stu-id="53244-111">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="53244-112">*Расположение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="53244-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53244-113">Координаты текстуры.</span><span class="sxs-lookup"><span data-stu-id="53244-113">The texture coordinates.</span></span> <span data-ttu-id="53244-114">Тип аргумента зависит от типа объекта текстуры.</span><span class="sxs-lookup"><span data-stu-id="53244-114">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="53244-115">Тип Texture-Object</span><span class="sxs-lookup"><span data-stu-id="53244-115">Texture-Object Type</span></span>                    | <span data-ttu-id="53244-116">Тип параметра</span><span class="sxs-lookup"><span data-stu-id="53244-116">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="53244-117">Texture1D</span><span class="sxs-lookup"><span data-stu-id="53244-117">Texture1D</span></span>                              | <span data-ttu-id="53244-118">FLOAT</span><span class="sxs-lookup"><span data-stu-id="53244-118">float</span></span>          |
| <span data-ttu-id="53244-119">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="53244-119">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="53244-120">float2</span><span class="sxs-lookup"><span data-stu-id="53244-120">float2</span></span>         |
| <span data-ttu-id="53244-121">Texture2DArray, Texture3D, Текстурекубе</span><span class="sxs-lookup"><span data-stu-id="53244-121">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="53244-122">float3</span><span class="sxs-lookup"><span data-stu-id="53244-122">float3</span></span>         |
| <span data-ttu-id="53244-123">текстурекубеаррай</span><span class="sxs-lookup"><span data-stu-id="53244-123">TextureCubeArray</span></span>                       | <span data-ttu-id="53244-124">float4</span><span class="sxs-lookup"><span data-stu-id="53244-124">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="53244-125">*Смещение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="53244-125">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53244-126">Необязательное Смещение координаты текстуры, которое может использоваться для любого типа объекта текстуры. смещение применяется к расположению перед выборкой.</span><span class="sxs-lookup"><span data-stu-id="53244-126">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="53244-127">Смещение текстуры должно быть статическим.</span><span class="sxs-lookup"><span data-stu-id="53244-127">The texture offsets need to be static.</span></span> <span data-ttu-id="53244-128">Тип аргумента зависит от типа объекта текстуры.</span><span class="sxs-lookup"><span data-stu-id="53244-128">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="53244-129">Дополнительные сведения см. в разделе [применение смещения координат текстуры](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="53244-129">For more info, see [Applying texture coordinate offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="53244-130">Тип Texture-Object</span><span class="sxs-lookup"><span data-stu-id="53244-130">Texture-Object Type</span></span>           | <span data-ttu-id="53244-131">Тип параметра</span><span class="sxs-lookup"><span data-stu-id="53244-131">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="53244-132">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="53244-132">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="53244-133">INT</span><span class="sxs-lookup"><span data-stu-id="53244-133">int</span></span>            |
| <span data-ttu-id="53244-134">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="53244-134">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="53244-135">int2</span><span class="sxs-lookup"><span data-stu-id="53244-135">int2</span></span>           |
| <span data-ttu-id="53244-136">Texture3D</span><span class="sxs-lookup"><span data-stu-id="53244-136">Texture3D</span></span>                     | <span data-ttu-id="53244-137">int3</span><span class="sxs-lookup"><span data-stu-id="53244-137">int3</span></span>           |
| <span data-ttu-id="53244-138">Текстурекубе, Текстурекубеаррай</span><span class="sxs-lookup"><span data-stu-id="53244-138">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="53244-139">не поддерживается</span><span class="sxs-lookup"><span data-stu-id="53244-139">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="53244-140">*Срез* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="53244-140">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53244-141">Необязательное значение для примера среза Лод значений.</span><span class="sxs-lookup"><span data-stu-id="53244-141">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="53244-142">Например, если передать значение среза 2.0 f, вы убедитесь, что ни один из отдельных примеров не имеет доступа к MIP уровню менее 2.0.</span><span class="sxs-lookup"><span data-stu-id="53244-142">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> <dt>

<span data-ttu-id="53244-143">*Состояние* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="53244-143">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="53244-144">Состояние операции.</span><span class="sxs-lookup"><span data-stu-id="53244-144">The status of the operation.</span></span> <span data-ttu-id="53244-145">Вы не можете получить доступ к состоянию напрямую; Вместо этого передайте состояние в подставляемую функцию [**чеккакцессфуллимаппед**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="53244-145">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="53244-146">**Чеккакцессфуллимаппед** возвращает **значение true** , если все значения из соответствующего **образца**, **сбора** или операции **загрузки** обращались к сопоставленным плиткам в [мозаичном ресурсе](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="53244-146">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="53244-147">Если какие бы то ни было значения были взяты из несопоставленной плитки, **чеккакцессфуллимаппед** возвращает **значение false**.</span><span class="sxs-lookup"><span data-stu-id="53244-147">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53244-148">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="53244-148">Return value</span></span>

<span data-ttu-id="53244-149">Формат текстуры, который является одним из типизированных значений, перечисленных в [**\_ формате DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="53244-149">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="remarks"></a><span data-ttu-id="53244-150">Примечания</span><span class="sxs-lookup"><span data-stu-id="53244-150">Remarks</span></span>

<span data-ttu-id="53244-151">Выбор текстуры использует расположение шаг текселя для поиска значения шаг текселя.</span><span class="sxs-lookup"><span data-stu-id="53244-151">Texture sampling uses the texel position to look up a texel value.</span></span> <span data-ttu-id="53244-152">Смещение можно применить к положению перед подстановкой.</span><span class="sxs-lookup"><span data-stu-id="53244-152">An offset can be applied to the position before lookup.</span></span> <span data-ttu-id="53244-153">Состояние образца содержит параметры выборки и фильтрации.</span><span class="sxs-lookup"><span data-stu-id="53244-153">The sampler state contains the sampling and filtering options.</span></span> <span data-ttu-id="53244-154">Этот метод может быть вызван в шейдере пикселей, но не поддерживается в шейдере вершин или шейдере Geometry.</span><span class="sxs-lookup"><span data-stu-id="53244-154">This method can be invoked within a pixel shader, but it is not supported in a vertex shader or a geometry shader.</span></span>

<span data-ttu-id="53244-155">Используйте смещение только с целочисленным миплевел; в противном случае вы можете получить разные результаты в зависимости от аппаратной реализации или параметров драйверов.</span><span class="sxs-lookup"><span data-stu-id="53244-155">Use an offset only at an integer miplevel; otherwise, you may get different results depending on hardware implementation or driver settings.</span></span>

### <a name="calculating-texel-positions"></a><span data-ttu-id="53244-156">Вычисление позиций шаг текселя</span><span class="sxs-lookup"><span data-stu-id="53244-156">Calculating Texel Positions</span></span>

<span data-ttu-id="53244-157">Координаты текстуры — это значения с плавающей запятой, которые ссылаются на данные текстуры, которые также называются нормализованной областью текстуры.</span><span class="sxs-lookup"><span data-stu-id="53244-157">Texture coordinates are floating-point values that reference texture data, which is also known as normalized texture space.</span></span> <span data-ttu-id="53244-158">Режимы переноса адреса применяются в этом порядке (координаты текстуры + смещения + режим переноса) для изменения координат текстуры за пределами \[ диапазона 0... 1 \] .</span><span class="sxs-lookup"><span data-stu-id="53244-158">Address wrapping modes are applied in this order (texture coordinates + offsets + wrap mode) to modify texture coordinates outside the \[0...1\] range.</span></span>

<span data-ttu-id="53244-159">Для массивов текстуры дополнительное значение параметра Location указывает индекс в массиве текстуры.</span><span class="sxs-lookup"><span data-stu-id="53244-159">For texture arrays, an additional value in the location parameter specifies an index into a texture array.</span></span> <span data-ttu-id="53244-160">Этот индекс рассматривается как масштабированное значение с плавающей запятой (вместо нормализованного пространства для стандартных координат текстуры).</span><span class="sxs-lookup"><span data-stu-id="53244-160">This index is treated as a scaled float value (instead of the normalized space for standard texture coordinates).</span></span> <span data-ttu-id="53244-161">Преобразование в целочисленный индекс выполняется в следующем порядке (float + Round-To-ближайшего-четного целое число + срез в диапазон массива).</span><span class="sxs-lookup"><span data-stu-id="53244-161">The conversion to an integer index is done in the following order (float + round-to-nearest-even integer + clamp to the array range).</span></span>

### <a name="applying-texture-coordinate-offsets"></a><span data-ttu-id="53244-162">Применение смещений для координат текстуры</span><span class="sxs-lookup"><span data-stu-id="53244-162">Applying Texture Coordinate Offsets</span></span>

<span data-ttu-id="53244-163">Параметр offset изменяет координаты текстуры в шаг текселя пространстве.</span><span class="sxs-lookup"><span data-stu-id="53244-163">The offset parameter modifies the texture coordinates, in texel space.</span></span> <span data-ttu-id="53244-164">Несмотря на то, что координаты текстуры являются нормализованными числами с плавающей запятой, смещение применяет целочисленное смещение.</span><span class="sxs-lookup"><span data-stu-id="53244-164">Even though texture coordinates are normalized floating-point numbers, the offset applies an integer offset.</span></span> <span data-ttu-id="53244-165">Также обратите внимание, что смещение текстуры должно быть статическим.</span><span class="sxs-lookup"><span data-stu-id="53244-165">Also note that the texture offsets need to be static.</span></span>

<span data-ttu-id="53244-166">Возвращаемый формат данных определяется форматом текстуры.</span><span class="sxs-lookup"><span data-stu-id="53244-166">The data format returned is determined by the texture format.</span></span> <span data-ttu-id="53244-167">Например, если ресурс текстуры был определен в \_ \_ формате DXGI A8B8G8R8 \_ UNORM \_ sRGB, операция выборки преобразует пример пикселей текстуры из гаммы 2,0 в 1,0, отфильтрует и записывает результат в виде значения с плавающей запятой в диапазоне \[ 0.. 1 \] .</span><span class="sxs-lookup"><span data-stu-id="53244-167">For example, if the texture resource was defined with the DXGI\_FORMAT\_A8B8G8R8\_UNORM\_SRGB format, the sampling operation converts sampled texels from gamma 2.0 to 1.0, filter, and writes the result as a floating-point value in the range \[0..1\].</span></span>

## <a name="see-also"></a><span data-ttu-id="53244-168">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="53244-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53244-169">Примеры методов</span><span class="sxs-lookup"><span data-stu-id="53244-169">Sample methods</span></span>](texture-sample-overload.md)
</dt> <dt>

[<span data-ttu-id="53244-170">Текстура-объект</span><span class="sxs-lookup"><span data-stu-id="53244-170">Texture-Object</span></span>](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

 
