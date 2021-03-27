---
title: Самплекмп (объект текстуры DirectX HLSL)
description: Выполняет выборку текстуры и сравнивает один компонент с указанным значением сравнения.
ms.assetid: e21894c4-e8c5-4c3d-92c1-727964f8fd94
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6991bead4bfc42451c26fe5476b4c114626eb7e8
ms.sourcegitcommit: 0d6365d4e852b09a9100d9cfb9a5334922ebf478
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/17/2020
ms.locfileid: "104997194"
---
# <a name="samplecmp-directx-hlsl-texture-object"></a><span data-ttu-id="e565b-103">Самплекмп (объект текстуры DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e565b-103">SampleCmp (DirectX HLSL Texture Object)</span></span>

<span data-ttu-id="e565b-104">Выполняет выборку текстуры и сравнивает один компонент с указанным значением сравнения.</span><span class="sxs-lookup"><span data-stu-id="e565b-104">Samples a texture and compares a single component against the specified comparison value.</span></span>

<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e565b-105">float Object. Самплекмп (</span><span class="sxs-lookup"><span data-stu-id="e565b-105">float Object.SampleCmp(</span></span> <dl> <span data-ttu-id="e565b-106">Самплеркомпарисонстате S,</span><span class="sxs-lookup"><span data-stu-id="e565b-106">SamplerComparisonState S,</span></span><br />
<span data-ttu-id="e565b-107">Расположение с плавающей запятой,</span><span class="sxs-lookup"><span data-stu-id="e565b-107">float Location,</span></span><br />
<span data-ttu-id="e565b-108">float Компаревалуе,</span><span class="sxs-lookup"><span data-stu-id="e565b-108">float CompareValue,</span></span><br />
<span data-ttu-id="e565b-109">[смещение int]</span><span class="sxs-lookup"><span data-stu-id="e565b-109">[int Offset]</span></span><br />
</dl><span data-ttu-id="e565b-110">);</span><span class="sxs-lookup"><span data-stu-id="e565b-110">);</span></span></td>
</tr>
</tbody>
</table>
 

<span data-ttu-id="e565b-111">Сравнение — это сравнение одного компонента между первым компонентом, хранящимся в текстуре, и значением сравнения, переданным в метод.</span><span class="sxs-lookup"><span data-stu-id="e565b-111">The comparison is a single-component comparison between the first component stored in the texture, and the comparison value passed into the method.</span></span>

<span data-ttu-id="e565b-112">Этот метод может быть вызван только из шейдера пикселей. Он не поддерживается в шейдере вершин или геометрии.</span><span class="sxs-lookup"><span data-stu-id="e565b-112">This method can be invoked only from a pixel shader; it isn't supported in a vertex or geometry shader.</span></span>

## <a name="parameters"></a><span data-ttu-id="e565b-113">Параметры</span><span class="sxs-lookup"><span data-stu-id="e565b-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e565b-114"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span>*Объектами*</span><span class="sxs-lookup"><span data-stu-id="e565b-114"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span>*Object*</span></span>
</dt> <dd>

<span data-ttu-id="e565b-115">Любой тип [объекта текстуры](dx-graphics-hlsl-to-type.md) (кроме Texture2DMS, Texture2DMSArray или Texture3D).</span><span class="sxs-lookup"><span data-stu-id="e565b-115">Any [texture-object](dx-graphics-hlsl-to-type.md) type (except Texture2DMS, Texture2DMSArray, or Texture3D).</span></span>

</dd> <dt>

<span data-ttu-id="e565b-116"><span id="S"></span><span id="s"></span>*#D0*</span><span class="sxs-lookup"><span data-stu-id="e565b-116"><span id="S"></span><span id="s"></span>*S*</span></span>
</dt> <dd>

<span data-ttu-id="e565b-117">\[в \] состоянии сравнения образцов, которое является состоянием выборки, а также состоянием сравнения (функция сравнения и фильтр сравнения).</span><span class="sxs-lookup"><span data-stu-id="e565b-117">\[in\] A sampler-comparison state, which is the sampler state plus a comparison state (a comparison function and a comparison filter).</span></span> <span data-ttu-id="e565b-118">Дополнительные сведения и пример см. в описании [типа образца](dx-graphics-hlsl-sampler.md) .</span><span class="sxs-lookup"><span data-stu-id="e565b-118">See the [sampler type](dx-graphics-hlsl-sampler.md) for details and an example.</span></span>

</dd> <dt>

<span data-ttu-id="e565b-119"><span id="Location"></span><span id="location"></span><span id="LOCATION"></span>*Места*</span><span class="sxs-lookup"><span data-stu-id="e565b-119"><span id="Location"></span><span id="location"></span><span id="LOCATION"></span>*Location*</span></span>
</dt> <dd>

<span data-ttu-id="e565b-120">\[в \] координатах текстуры.</span><span class="sxs-lookup"><span data-stu-id="e565b-120">\[in\] The texture coordinates.</span></span> <span data-ttu-id="e565b-121">Тип аргумента зависит от типа объекта текстуры.</span><span class="sxs-lookup"><span data-stu-id="e565b-121">The argument type is dependent on the texture-object type.</span></span>

| <span data-ttu-id="e565b-122">Тип Texture-Object</span><span class="sxs-lookup"><span data-stu-id="e565b-122">Texture-Object Type</span></span>          | <span data-ttu-id="e565b-123">Тип параметра</span><span class="sxs-lookup"><span data-stu-id="e565b-123">Parameter Type</span></span> |
|------------------------------|----------------|
| <span data-ttu-id="e565b-124">Texture1D</span><span class="sxs-lookup"><span data-stu-id="e565b-124">Texture1D</span></span>                    | <span data-ttu-id="e565b-125">FLOAT</span><span class="sxs-lookup"><span data-stu-id="e565b-125">float</span></span>          |
| <span data-ttu-id="e565b-126">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="e565b-126">Texture1DArray, Texture2D</span></span>    | <span data-ttu-id="e565b-127">float2</span><span class="sxs-lookup"><span data-stu-id="e565b-127">float2</span></span>         |
| <span data-ttu-id="e565b-128">Texture2DArray ¹, Текстурекубе</span><span class="sxs-lookup"><span data-stu-id="e565b-128">Texture2DArray¹, TextureCube</span></span> | <span data-ttu-id="e565b-129">float3</span><span class="sxs-lookup"><span data-stu-id="e565b-129">float3</span></span>         |
| <span data-ttu-id="e565b-130">Текстурекубеаррай ¹</span><span class="sxs-lookup"><span data-stu-id="e565b-130">TextureCubeArray¹</span></span>            | <span data-ttu-id="e565b-131">float4</span><span class="sxs-lookup"><span data-stu-id="e565b-131">float4</span></span>         |

</dd> <dt>

<span data-ttu-id="e565b-132"><span id="CompareValue"></span><span id="comparevalue"></span><span id="COMPAREVALUE"></span>*компаревалуе*</span><span class="sxs-lookup"><span data-stu-id="e565b-132"><span id="CompareValue"></span><span id="comparevalue"></span><span id="COMPAREVALUE"></span>*CompareValue*</span></span>
</dt> <dd>

<span data-ttu-id="e565b-133">Значение с плавающей запятой, используемое в качестве значения сравнения.</span><span class="sxs-lookup"><span data-stu-id="e565b-133">A floating-point value to use as a comparison value.</span></span>

</dd> <dt>

<span data-ttu-id="e565b-134"><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span>*Собой*</span><span class="sxs-lookup"><span data-stu-id="e565b-134"><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span>*Offset*</span></span>
</dt> <dd>

<span data-ttu-id="e565b-135">\[в \] необязательном смещении координаты текстуры, которое может использоваться для любого типа объекта текстуры; смещение применяется к расположению перед выборкой.</span><span class="sxs-lookup"><span data-stu-id="e565b-135">\[in\] An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="e565b-136">Смещение текстуры должно быть статическим.</span><span class="sxs-lookup"><span data-stu-id="e565b-136">The texture offsets need to be static.</span></span> <span data-ttu-id="e565b-137">Тип аргумента зависит от типа объекта текстуры.</span><span class="sxs-lookup"><span data-stu-id="e565b-137">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="e565b-138">Дополнительные сведения см. в разделе [применение смещения координат текстуры](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="e565b-138">For more info, see [Applying texture coordinate offsets](dx-graphics-hlsl-to-sample.md).</span></span>

| <span data-ttu-id="e565b-139">Тип Texture-Object</span><span class="sxs-lookup"><span data-stu-id="e565b-139">Texture-Object Type</span></span>            | <span data-ttu-id="e565b-140">Тип параметра</span><span class="sxs-lookup"><span data-stu-id="e565b-140">Parameter Type</span></span> |
|--------------------------------|----------------|
| <span data-ttu-id="e565b-141">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="e565b-141">Texture1D, Texture1DArray</span></span>      | <span data-ttu-id="e565b-142">INT</span><span class="sxs-lookup"><span data-stu-id="e565b-142">int</span></span>            |
| <span data-ttu-id="e565b-143">Texture2D, Texture2DArray ¹</span><span class="sxs-lookup"><span data-stu-id="e565b-143">Texture2D, Texture2DArray¹</span></span>     | <span data-ttu-id="e565b-144">int2</span><span class="sxs-lookup"><span data-stu-id="e565b-144">int2</span></span>           |
| <span data-ttu-id="e565b-145">Текстурекубе, Текстурекубеаррай ¹</span><span class="sxs-lookup"><span data-stu-id="e565b-145">TextureCube, TextureCubeArray¹</span></span> | <span data-ttu-id="e565b-146">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="e565b-146">Not supported</span></span>  |

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e565b-147">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e565b-147">Return Value</span></span>

<span data-ttu-id="e565b-148">Возвращает значение с плавающей запятой в диапазоне \[ 0.. 1 \] .</span><span class="sxs-lookup"><span data-stu-id="e565b-148">Returns a floating-point value in the range \[0..1\].</span></span>

<span data-ttu-id="e565b-149">Для каждого шаг текселя, полученного (на основе конфигурации образца режима фильтрации), **самплекмп** выполняет сравнение значения z (третьего компонента входных данных) от шейдера с значением шаг текселя (1, если сравнение пройдет; в противном случае — 0).</span><span class="sxs-lookup"><span data-stu-id="e565b-149">For each texel fetched (based on the sampler configuration of the filter mode), **SampleCmp** performs a comparison of the z value (3rd component of input) from the shader against the texel value (1 if the comparison passes; otherwise 0).</span></span> <span data-ttu-id="e565b-150">Затем **самплекмп** объединяет эти 0 и 1 результаты для каждого шаг текселя, как в обычной фильтрации текстур (не в среднем), и возвращает результирующее \[ значение 0.. 1 \] шейдеру.</span><span class="sxs-lookup"><span data-stu-id="e565b-150">**SampleCmp** then blends these 0 and 1 results for each texel together as in normal texture filtering (not an average) and returns the resulting \[0..1\] value to the shader.</span></span>

## <a name="remarks"></a><span data-ttu-id="e565b-151">Примечания</span><span class="sxs-lookup"><span data-stu-id="e565b-151">Remarks</span></span>

<span data-ttu-id="e565b-152">Фильтрация по сравнению обеспечивает базовую операцию фильтрации, которая полезна для более глубокой фильтрации по процентам.</span><span class="sxs-lookup"><span data-stu-id="e565b-152">Comparison filtering provides a basic filtering operation that is useful for percentage-closer-depth filtering.</span></span>

<span data-ttu-id="e565b-153">При использовании этого метода для ресурса с плавающей запятой (вместо ненормализованного или неподписанного) значение сравнения не будет автоматически переписываться между 0,0 и 1,0.</span><span class="sxs-lookup"><span data-stu-id="e565b-153">When using this method on a floating-point resource (Instead of a signed-normalized or unsigned-normalized format), the comparison value is not automatically clamped between 0.0 and 1.0.</span></span> <span data-ttu-id="e565b-154">Таким образом, для распространенных методов затенения может потребоваться ручной срез значения сравнения.</span><span class="sxs-lookup"><span data-stu-id="e565b-154">Therefore, a manual clamp of the comparison value may be necessary for common shadowing techniques.</span></span>

<span data-ttu-id="e565b-155">Используйте смещение только с целочисленным миплевел; в противном случае вы можете получить разные результаты в зависимости от аппаратной реализации или параметров драйверов.</span><span class="sxs-lookup"><span data-stu-id="e565b-155">Use an offset only at an integer miplevel; otherwise, you may get different results depending on hardware implementation or driver settings.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="e565b-156">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="e565b-156">Minimum Shader Model</span></span>

<span data-ttu-id="e565b-157">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="e565b-157">This function is supported in the following shader models.</span></span>

| <span data-ttu-id="e565b-158">VS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="e565b-158">vs\_4\_0</span></span> | <span data-ttu-id="e565b-159">VS \_ 4 \_ 1 ²</span><span class="sxs-lookup"><span data-stu-id="e565b-159">vs\_4\_1²</span></span> | <span data-ttu-id="e565b-160">PS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="e565b-160">ps\_4\_0</span></span> | <span data-ttu-id="e565b-161">PS \_ 4 \_ 1 ²</span><span class="sxs-lookup"><span data-stu-id="e565b-161">ps\_4\_1²</span></span> | <span data-ttu-id="e565b-162">GS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="e565b-162">gs\_4\_0</span></span> | <span data-ttu-id="e565b-163">GS \_ 4 \_ 1 ²</span><span class="sxs-lookup"><span data-stu-id="e565b-163">gs\_4\_1²</span></span> |
|----------|-----------|----------|-----------|----------|-----------|
|          |           | <span data-ttu-id="e565b-164">x ¹</span><span class="sxs-lookup"><span data-stu-id="e565b-164">x¹</span></span>       | <span data-ttu-id="e565b-165">x</span><span class="sxs-lookup"><span data-stu-id="e565b-165">x</span></span>         |          |           |

1.  <span data-ttu-id="e565b-166">Texture2DArray и Текстурекубеаррай доступны в модели шейдера 4,1 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="e565b-166">Texture2DArray and TextureCubeArray are available in Shader Model 4.1 or higher.</span></span>
2.  <span data-ttu-id="e565b-167">Модель шейдеров 4,1 доступна в Direct3D 10,1 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="e565b-167">Shader Model 4.1 is available in Direct3D 10.1 or higher.</span></span>

> [!NOTE]  
> <span data-ttu-id="e565b-168">**Самплекмп** также доступен на PS 4 \_ 0 \_ уровня \_ 9 \_ 1 и 4 \_ 0 \_ уровня \_ 9 \_ при использовании методов, описанных в разделе [Реализация теневых буферов для уровня функций Direct3D 9](/previous-versions/windows/apps/jj262110(v=win.10)).</span><span class="sxs-lookup"><span data-stu-id="e565b-168">**SampleCmp** is also available in ps 4\_0\_level\_9\_1 and 4\_0\_level\_9\_3 when you use the techniques that are described in [Implementing shadow buffers for Direct3D feature level 9](/previous-versions/windows/apps/jj262110(v=win.10)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e565b-169">См. также</span><span class="sxs-lookup"><span data-stu-id="e565b-169">Related topics</span></span>

[<span data-ttu-id="e565b-170">Текстура-объект</span><span class="sxs-lookup"><span data-stu-id="e565b-170">Texture-Object</span></span>](dx-graphics-hlsl-to-type.md)
