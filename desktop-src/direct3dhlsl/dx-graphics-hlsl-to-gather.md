---
title: Сбор данных (объект текстуры DirectX HLSL)
description: Получает четыре образца (только красный компонент), которые будут использоваться для интерполяции билинейной при выборке текстуры.
ms.assetid: a394d8c2-99cc-4a38-9ac9-34afc666ebe0
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f333c204b77d6e0c64119e16f31e170fec1d0f6c
ms.sourcegitcommit: 07ba02719c9779e082b108ae74f9699fb0236c34
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/06/2021
ms.locfileid: "108644106"
---
# <a name="gather-directx-hlsl-texture-object"></a><span data-ttu-id="113e4-103">Сбор данных (объект текстуры DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="113e4-103">Gather (DirectX HLSL Texture Object)</span></span>

<span data-ttu-id="113e4-104">Получает четыре образца (только красный компонент), которые будут использоваться для интерполяции билинейной при выборке текстуры.</span><span class="sxs-lookup"><span data-stu-id="113e4-104">Gets the four samples (red component only) that would be used for bilinear interpolation when sampling a texture.</span></span>



|                                                                                                    |
|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="113e4-105">&lt;Тип шаблона &gt; 4 Object. сбор данных (образец \_ состояния, \| Расположение float2 3 \| 4 \[ , смещение int2 \] );</span><span class="sxs-lookup"><span data-stu-id="113e4-105">&lt;Template Type&gt;4 Object.Gather( sampler\_state S, float2\|3\|4 Location \[, int2 Offset\] );</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="113e4-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="113e4-106">Parameters</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="113e4-107">Item</span><span class="sxs-lookup"><span data-stu-id="113e4-107">Item</span></span></th>
<th><span data-ttu-id="113e4-108">Описание</span><span class="sxs-lookup"><span data-stu-id="113e4-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="113e4-109"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Объектами</em></span><span class="sxs-lookup"><span data-stu-id="113e4-109"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Object</em></span></span><br/></td>
<td><span data-ttu-id="113e4-110">Поддерживаются следующие типы <a href="dx-graphics-hlsl-to-type.md">объектов текстуры</a> : Texture2D, Texture2DArray, Текстурекубе, текстурекубеаррай.</span><span class="sxs-lookup"><span data-stu-id="113e4-110">The following <a href="dx-graphics-hlsl-to-type.md">texture-object</a> types are supported: Texture2D, Texture2DArray, TextureCube, TextureCubeArray.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="113e4-111"><span id="S"></span><span id="s"></span><em>#D0</em></span><span class="sxs-lookup"><span data-stu-id="113e4-111"><span id="S"></span><span id="s"></span><em>S</em></span></span><br/></td>
<td><span data-ttu-id="113e4-112">окне <a href="dx-graphics-hlsl-sampler.md">Состояние образца</a>.</span><span class="sxs-lookup"><span data-stu-id="113e4-112">[in] A <a href="dx-graphics-hlsl-sampler.md">Sampler state</a>.</span></span> <span data-ttu-id="113e4-113">Это объект, объявленный в файле эффектов, который содержит назначения состояний.</span><span class="sxs-lookup"><span data-stu-id="113e4-113">This is an object declared in an effect file that contains state assignments.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="113e4-114"><span id="Location"></span><span id="location"></span><span id="LOCATION"></span><em>Места</em></span><span class="sxs-lookup"><span data-stu-id="113e4-114"><span id="Location"></span><span id="location"></span><span id="LOCATION"></span><em>Location</em></span></span><br/></td>
<td><span data-ttu-id="113e4-115">окне Координаты текстуры.</span><span class="sxs-lookup"><span data-stu-id="113e4-115">[in] The texture coordinates.</span></span> <span data-ttu-id="113e4-116">Тип аргумента зависит от типа объекта текстуры.</span><span class="sxs-lookup"><span data-stu-id="113e4-116">The argument type is dependent on the texture-object type.</span></span> <br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="113e4-117">Тип Texture-Object</span><span class="sxs-lookup"><span data-stu-id="113e4-117">Texture-Object Type</span></span></th>
<th><span data-ttu-id="113e4-118">Тип параметра</span><span class="sxs-lookup"><span data-stu-id="113e4-118">Parameter Type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="113e4-119">Texture2D</span><span class="sxs-lookup"><span data-stu-id="113e4-119">Texture2D</span></span></td>
<td><span data-ttu-id="113e4-120">float2</span><span class="sxs-lookup"><span data-stu-id="113e4-120">float2</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="113e4-121">Texture2DArray, Текстурекубе</span><span class="sxs-lookup"><span data-stu-id="113e4-121">Texture2DArray, TextureCube</span></span></td>
<td><span data-ttu-id="113e4-122">float3</span><span class="sxs-lookup"><span data-stu-id="113e4-122">float3</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="113e4-123">текстурекубеаррай</span><span class="sxs-lookup"><span data-stu-id="113e4-123">TextureCubeArray</span></span> </td>
<td><span data-ttu-id="113e4-124">float4</span><span class="sxs-lookup"><span data-stu-id="113e4-124">float4</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="113e4-125"><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span><em>Собой</em></span><span class="sxs-lookup"><span data-stu-id="113e4-125"><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span><em>Offset</em></span></span></p></td>
<td><p><span data-ttu-id="113e4-126">окне Необязательное Смещение координаты текстуры, которое может использоваться для любого типа объекта текстуры. смещение применяется к расположению перед выборкой.</span><span class="sxs-lookup"><span data-stu-id="113e4-126">[in] An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="113e4-127">Тип аргумента зависит от типа объекта текстуры.</span><span class="sxs-lookup"><span data-stu-id="113e4-127">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="113e4-128">Для шейдеров, предназначенных для Shader Model 5,0 и более поздних версий, 6 наименее значимых битов каждого значения смещения учитываются как значение со знаком, а возвращает диапазон [-32.. 31].</span><span class="sxs-lookup"><span data-stu-id="113e4-128">For shaders targeting Shader Model 5.0 and above, the 6 least significant bits of each offset value is honored as a signed value, yielding [-32..31] range.</span></span> <span data-ttu-id="113e4-129">Для предыдущих шейдеров модели шейдера смещения должны быть прямыми целыми числами от-8 до 7.</span><span class="sxs-lookup"><span data-stu-id="113e4-129">For previous shader model shaders, offsets need to be immediate integers between -8 and 7.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="113e4-130">Тип Texture-Object</span><span class="sxs-lookup"><span data-stu-id="113e4-130">Texture-Object Type</span></span></th>
<th><span data-ttu-id="113e4-131">Тип параметра</span><span class="sxs-lookup"><span data-stu-id="113e4-131">Parameter Type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="113e4-132">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="113e4-132">Texture2D, Texture2DArray</span></span></td>
<td><span data-ttu-id="113e4-133">int2</span><span class="sxs-lookup"><span data-stu-id="113e4-133">int2</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="113e4-134">Текстурекубе, Текстурекубеаррай</span><span class="sxs-lookup"><span data-stu-id="113e4-134">TextureCube, TextureCubeArray</span></span> </td>
<td><span data-ttu-id="113e4-135">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="113e4-135">not supported</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="return-value"></a><span data-ttu-id="113e4-136">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="113e4-136">Return Value</span></span>

<span data-ttu-id="113e4-137">Вектор из четырех компонентов с четырьмя компонентами Красного типа данных, тип которых совпадает с типом шаблона текстуры.</span><span class="sxs-lookup"><span data-stu-id="113e4-137">A four-component vector, with four components of red data, whose type is the same as the texture's template type.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="113e4-138">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="113e4-138">Minimum Shader Model</span></span>

<span data-ttu-id="113e4-139">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="113e4-139">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="113e4-140">VS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="113e4-140">vs\_4\_0</span></span> | <span data-ttu-id="113e4-141">VS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="113e4-141">vs\_4\_1</span></span>  | <span data-ttu-id="113e4-142">PS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="113e4-142">ps\_4\_0</span></span> | <span data-ttu-id="113e4-143">PS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="113e4-143">ps\_4\_1</span></span>  | <span data-ttu-id="113e4-144">GS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="113e4-144">gs\_4\_0</span></span> | <span data-ttu-id="113e4-145">GS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="113e4-145">gs\_4\_1</span></span>  |
|----------|-----------|----------|-----------|----------|-----------|
|          | <span data-ttu-id="113e4-146">x</span><span class="sxs-lookup"><span data-stu-id="113e4-146">x</span></span>         |          | <span data-ttu-id="113e4-147">x</span><span class="sxs-lookup"><span data-stu-id="113e4-147">x</span></span>         |          | <span data-ttu-id="113e4-148">x</span><span class="sxs-lookup"><span data-stu-id="113e4-148">x</span></span>         |



 

1.  <span data-ttu-id="113e4-149">Текстурекубеаррай доступен в модели шейдеров 4,1 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="113e4-149">TextureCubeArray is available in Shader Model 4.1 or higher.</span></span>
2.  <span data-ttu-id="113e4-150">Модель шейдеров 4,1 доступна в Direct3D 10,1 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="113e4-150">Shader Model 4.1 is available in Direct3D 10.1 or higher.</span></span>

## <a name="example"></a><span data-ttu-id="113e4-151">Пример</span><span class="sxs-lookup"><span data-stu-id="113e4-151">Example</span></span>


```
Texture2D<int1> Tex2d;
Texture2DArray<int2> Tex2dArray;
TextureCube<int3> TexCube;
TextureCubeArray<float2> TexCubeArray;

SamplerState s;

int4 main (float4 f : SV_Position) : SV_Target
{
    int2 iOffset = int2(2,3);

    int4 i1 = Tex2d.Gather(s, f.xy);
    int4 i2 = Tex2d.Gather(s, f.xy, iOffset);

    int4 i3 = Tex2dArray.Gather(s, f.xyz);
    int4 i4 = Tex2dArray.Gather(s, f.xyz, iOffset);

    int4 i5 = TexCube.Gather(s, f.xyzw);

    float4 f6 = TexCubeArray.Gather(s, f.xyzw);

    return i1+i2+i3+i4+i5+int4(i6);
}
  
```



## <a name="related-topics"></a><span data-ttu-id="113e4-152">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="113e4-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="113e4-153">Текстура-объект</span><span class="sxs-lookup"><span data-stu-id="113e4-153">Texture-Object</span></span>](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

 





