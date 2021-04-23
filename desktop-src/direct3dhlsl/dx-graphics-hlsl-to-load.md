---
title: Load (объект текстуры DirectX HLSL)
description: Считывает данные шаг текселя без какой бы то ни было фильтрации или выборки.
ms.assetid: a2fbda88-29c7-4d28-bd3e-df1d9aa36ee8
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 08d3964788a238492ff7d5189544603b35808465
ms.sourcegitcommit: 4c00910ed754d7d0a68c9a833751d714c06e3b39
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "104139198"
---
# <a name="load-directx-hlsl-texture-object"></a><span data-ttu-id="c10f6-103">Load (объект текстуры DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c10f6-103">Load (DirectX HLSL Texture Object)</span></span>

<span data-ttu-id="c10f6-104">Считывает данные шаг текселя без какой бы то ни было фильтрации или выборки.</span><span class="sxs-lookup"><span data-stu-id="c10f6-104">Reads texel data without any filtering or sampling.</span></span>



<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c10f6-105">Объект Ret. Load (</span><span class="sxs-lookup"><span data-stu-id="c10f6-105">ret Object.Load(</span></span><dl> <span data-ttu-id="c10f6-106">Расположение Типекс,</span><span class="sxs-lookup"><span data-stu-id="c10f6-106">typeX Location,</span></span><br />
<span data-ttu-id="c10f6-107">[Типекс SampleIndex,]</span><span class="sxs-lookup"><span data-stu-id="c10f6-107">[typeX SampleIndex, ]</span></span><br />
<span data-ttu-id="c10f6-108">[смещение Типекс]</span><span class="sxs-lookup"><span data-stu-id="c10f6-108">[typeX Offset ]</span></span><br />
</dl><span data-ttu-id="c10f6-109">);</span><span class="sxs-lookup"><span data-stu-id="c10f6-109">);</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c10f6-110">Типекс указывает, что существует четыре возможных типа: **int**, **int2**,, **корпус** или **INT4**.</span><span class="sxs-lookup"><span data-stu-id="c10f6-110">typeX denotes that there are four possible types: **int**, **int2**, **int3** or **int4**.</span></span>

 

## <a name="parameters"></a><span data-ttu-id="c10f6-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="c10f6-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c10f6-112"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span>*Объектами*</span><span class="sxs-lookup"><span data-stu-id="c10f6-112"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span>*Object*</span></span>
</dt> <dd>

<span data-ttu-id="c10f6-113">Тип [объекта текстуры](dx-graphics-hlsl-to-type.md) (за исключением Текстурекубе или текстурекубеаррай).</span><span class="sxs-lookup"><span data-stu-id="c10f6-113">A [texture-object](dx-graphics-hlsl-to-type.md) type (except TextureCube or TextureCubeArray).</span></span>

</dd> <dt>

<span data-ttu-id="c10f6-114"><span id="Location"></span><span id="location"></span><span id="LOCATION"></span>*Места*</span><span class="sxs-lookup"><span data-stu-id="c10f6-114"><span id="Location"></span><span id="location"></span><span id="LOCATION"></span>*Location*</span></span>
</dt> <dd>

<span data-ttu-id="c10f6-115">\[в \] координатах текстуры последний компонент указывает уровень mipmap.</span><span class="sxs-lookup"><span data-stu-id="c10f6-115">\[in\] The texture coordinates; the last component specifies the mipmap level.</span></span> <span data-ttu-id="c10f6-116">Этот метод использует систему координат на основе 0, а не систему 0,0-1,0 UV.</span><span class="sxs-lookup"><span data-stu-id="c10f6-116">This method uses a 0-based coordinate system and not a 0.0-1.0 UV system.</span></span> <span data-ttu-id="c10f6-117">Тип аргумента зависит от типа объекта текстуры.</span><span class="sxs-lookup"><span data-stu-id="c10f6-117">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="c10f6-118">Тип объекта</span><span class="sxs-lookup"><span data-stu-id="c10f6-118">Object Type</span></span>                                  | <span data-ttu-id="c10f6-119">Тип параметра</span><span class="sxs-lookup"><span data-stu-id="c10f6-119">Parameter Type</span></span> |
|----------------------------------------------|----------------|
| <span data-ttu-id="c10f6-120">Буфер</span><span class="sxs-lookup"><span data-stu-id="c10f6-120">Buffer</span></span>                                       | <span data-ttu-id="c10f6-121">INT</span><span class="sxs-lookup"><span data-stu-id="c10f6-121">int</span></span>            |
| <span data-ttu-id="c10f6-122">Texture1D, Texture2DMS</span><span class="sxs-lookup"><span data-stu-id="c10f6-122">Texture1D, Texture2DMS</span></span>                       | <span data-ttu-id="c10f6-123">int2</span><span class="sxs-lookup"><span data-stu-id="c10f6-123">int2</span></span>           |
| <span data-ttu-id="c10f6-124">Texture1DArray, 2D-текстура, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="c10f6-124">Texture1DArray, Texture 2D, Texture2DMSArray</span></span> | <span data-ttu-id="c10f6-125">int3</span><span class="sxs-lookup"><span data-stu-id="c10f6-125">int3</span></span>           |
| <span data-ttu-id="c10f6-126">Texture2DArray, Texture3D</span><span class="sxs-lookup"><span data-stu-id="c10f6-126">Texture2DArray, Texture3D</span></span>                    | <span data-ttu-id="c10f6-127">int4</span><span class="sxs-lookup"><span data-stu-id="c10f6-127">int4</span></span>           |



 

<span data-ttu-id="c10f6-128">Например, чтобы получить доступ к двухмерной текстуре, укажите UV-координаты для первых двух компонентов и уровень mipmap для третьего компонента.</span><span class="sxs-lookup"><span data-stu-id="c10f6-128">For example, to access a 2D texture, supply UV coordinates for the first two components and a mipmap level for the third component.</span></span>

> [!Note]  
> <span data-ttu-id="c10f6-129">Если одно или несколько координат в *расположении* превышают размеры mipmap в единицах измерения u, v или w, то **Load** возвращает ноль во всех компонентах.</span><span class="sxs-lookup"><span data-stu-id="c10f6-129">When one or more of the coordinates in *Location* exceed the u, v, or w mipmap level dimensions of the texture, **Load** returns zero in all components.</span></span> <span data-ttu-id="c10f6-130">Direct3D гарантирует возврат нуля для любого ресурса, доступ к которому осуществляется вне границ.</span><span class="sxs-lookup"><span data-stu-id="c10f6-130">Direct3D guarantees to return zero for any resource that is accessed out of bounds.</span></span>

 

</dd> <dt>

<span data-ttu-id="c10f6-131"><span id="SampleIndex"></span><span id="sampleindex"></span><span id="SAMPLEINDEX"></span>*SampleIndex*</span><span class="sxs-lookup"><span data-stu-id="c10f6-131"><span id="SampleIndex"></span><span id="sampleindex"></span><span id="SAMPLEINDEX"></span>*SampleIndex*</span></span>
</dt> <dd>

<span data-ttu-id="c10f6-132">\[в \] необязательном индексе выборки.</span><span class="sxs-lookup"><span data-stu-id="c10f6-132">\[in\] An optional sampling index.</span></span>



| <span data-ttu-id="c10f6-133">Тип текстуры</span><span class="sxs-lookup"><span data-stu-id="c10f6-133">Texture Type</span></span>                                                                                                   | <span data-ttu-id="c10f6-134">Тип параметра</span><span class="sxs-lookup"><span data-stu-id="c10f6-134">Parameter Type</span></span> |
|----------------------------------------------------------------------------------------------------------------|----------------|
| <span data-ttu-id="c10f6-135">Texture1D, Texture1DArray, Texture2D, Texture2DArray, Texture3D, Texture2DArray, Текстурекубе, Текстурекубеаррай</span><span class="sxs-lookup"><span data-stu-id="c10f6-135">Texture1D, Texture1DArray, Texture2D, Texture2DArray, Texture3D, Texture2DArray, TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="c10f6-136">не поддерживается</span><span class="sxs-lookup"><span data-stu-id="c10f6-136">not supported</span></span>  |
| <span data-ttu-id="c10f6-137">Texture2DMS, Texture2DMSArray ¹</span><span class="sxs-lookup"><span data-stu-id="c10f6-137">Texture2DMS, Texture2DMSArray¹</span></span>                                                                                 | <span data-ttu-id="c10f6-138">INT</span><span class="sxs-lookup"><span data-stu-id="c10f6-138">int</span></span>            |



 

> [!Note]  
> <span data-ttu-id="c10f6-139">*SampleIndex* доступен только для многопримерных текстур.</span><span class="sxs-lookup"><span data-stu-id="c10f6-139">*SampleIndex* is only available for multi-sample textures.</span></span>

 

</dd> <dt>

<span data-ttu-id="c10f6-140"><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span>*Собой*</span><span class="sxs-lookup"><span data-stu-id="c10f6-140"><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span>*Offset*</span></span>
</dt> <dd>

<span data-ttu-id="c10f6-141">\[в \] необязательном смещении, применяемом к координатам текстуры перед выборкой.</span><span class="sxs-lookup"><span data-stu-id="c10f6-141">\[in\] An optional offset applied to the texture coordinates before sampling.</span></span> <span data-ttu-id="c10f6-142">Тип смещения зависит от типа объекта «текстура» и должен быть статическим.</span><span class="sxs-lookup"><span data-stu-id="c10f6-142">The offset type is dependent on the texture-object type, and needs to be static.</span></span>



| <span data-ttu-id="c10f6-143">Тип текстуры</span><span class="sxs-lookup"><span data-stu-id="c10f6-143">Texture Type</span></span>                                             | <span data-ttu-id="c10f6-144">Тип параметра</span><span class="sxs-lookup"><span data-stu-id="c10f6-144">Parameter Type</span></span> |
|----------------------------------------------------------|----------------|
| <span data-ttu-id="c10f6-145">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="c10f6-145">Texture1D, Texture1DArray</span></span>                                | <span data-ttu-id="c10f6-146">INT</span><span class="sxs-lookup"><span data-stu-id="c10f6-146">int</span></span>            |
| <span data-ttu-id="c10f6-147">Texture2D, Texture2DArray, Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="c10f6-147">Texture2D, Texture2DArray, Texture2DMS, Texture2DMSArray</span></span> | <span data-ttu-id="c10f6-148">int2</span><span class="sxs-lookup"><span data-stu-id="c10f6-148">int2</span></span>           |
| <span data-ttu-id="c10f6-149">Texture3D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="c10f6-149">Texture3D, Texture2DArray</span></span>                                | <span data-ttu-id="c10f6-150">int3</span><span class="sxs-lookup"><span data-stu-id="c10f6-150">int3</span></span>           |



 

> [!Note]  
> <span data-ttu-id="c10f6-151">Если используется *смещение* с несколькими образцами текстур, необходимо также указать *SampleIndex*.</span><span class="sxs-lookup"><span data-stu-id="c10f6-151">If you use *Offset* with multi-sample textures, you must also specify *SampleIndex*.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c10f6-152">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c10f6-152">Return Value</span></span>

<span data-ttu-id="c10f6-153">Возвращаемый тип соответствует типу в объявлении *объекта* .</span><span class="sxs-lookup"><span data-stu-id="c10f6-153">The return type matches the type in the *Object* declaration.</span></span> <span data-ttu-id="c10f6-154">Например, Объект Texture2D, объявленный как "Texture2d <uint4> митекстуре;", имеет возвращаемое значение типа **uint4**.</span><span class="sxs-lookup"><span data-stu-id="c10f6-154">For example, a Texture2D object that was declared as "Texture2d<uint4> myTexture;" has a return value of type **uint4**.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="c10f6-155">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="c10f6-155">Minimum Shader Model</span></span>

<span data-ttu-id="c10f6-156">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="c10f6-156">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="c10f6-157">VS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="c10f6-157">vs\_4\_0</span></span> | <span data-ttu-id="c10f6-158">VS \_ 4 \_ 1 ¹</span><span class="sxs-lookup"><span data-stu-id="c10f6-158">vs\_4\_1¹</span></span> | <span data-ttu-id="c10f6-159">PS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="c10f6-159">ps\_4\_0</span></span> | <span data-ttu-id="c10f6-160">PS \_ 4 \_ 1 ¹</span><span class="sxs-lookup"><span data-stu-id="c10f6-160">ps\_4\_1¹</span></span> | <span data-ttu-id="c10f6-161">GS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="c10f6-161">gs\_4\_0</span></span> | <span data-ttu-id="c10f6-162">GS \_ 4 \_ 1 ¹</span><span class="sxs-lookup"><span data-stu-id="c10f6-162">gs\_4\_1¹</span></span> |
|----------|-----------|----------|-----------|----------|-----------|
| <span data-ttu-id="c10f6-163">x</span><span class="sxs-lookup"><span data-stu-id="c10f6-163">x</span></span>        | <span data-ttu-id="c10f6-164">x</span><span class="sxs-lookup"><span data-stu-id="c10f6-164">x</span></span>         | <span data-ttu-id="c10f6-165">x</span><span class="sxs-lookup"><span data-stu-id="c10f6-165">x</span></span>        | <span data-ttu-id="c10f6-166">x</span><span class="sxs-lookup"><span data-stu-id="c10f6-166">x</span></span>         | <span data-ttu-id="c10f6-167">x</span><span class="sxs-lookup"><span data-stu-id="c10f6-167">x</span></span>        | <span data-ttu-id="c10f6-168">x</span><span class="sxs-lookup"><span data-stu-id="c10f6-168">x</span></span>         |



 

-   <span data-ttu-id="c10f6-169">Модель шейдеров 4,1 доступна в Direct3D 10,1 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="c10f6-169">Shader Model 4.1 is available in Direct3D 10.1 or higher.</span></span>

## <a name="example"></a><span data-ttu-id="c10f6-170">Например, .</span><span class="sxs-lookup"><span data-stu-id="c10f6-170">Example</span></span>

<span data-ttu-id="c10f6-171">Этот частичный пример кода относится к файлу Paint. FX в [образце адванцедпартиклес](https://msdn.microsoft.com/library/Ee416394(v=VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="c10f6-171">This partial code example is from the Paint.fx file in the [AdvancedParticles Sample](https://msdn.microsoft.com/library/Ee416394(v=VS.85).aspx).</span></span>


```
// Object Declarations
Buffer<float4> g_ParticleBuffer;

// Shader body calling the intrinsic function
float4 PSPaint(PSQuadIn input) : SV_Target
{       
    ... 
    for( int i=g_ParticleStart; i<g_NumParticles; i+=g_ParticleStep )
    {
        ... 
        // load the particle
        float4 particlePos = g_ParticleBuffer.Load( i*4 );
        float4 particleColor = g_ParticleBuffer.Load( (i*4) + 2 );
        ...     
    }
    ...
}   
```



## <a name="related-topics"></a><span data-ttu-id="c10f6-172">См. также</span><span class="sxs-lookup"><span data-stu-id="c10f6-172">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c10f6-173">Текстура-объект</span><span class="sxs-lookup"><span data-stu-id="c10f6-173">Texture-Object</span></span>](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

 




