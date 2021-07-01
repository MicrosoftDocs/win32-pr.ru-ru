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
ms.openlocfilehash: 4659ba19e9fa950a659969f2491533858f4658fb
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120549"
---
# <a name="gather-directx-hlsl-texture-object"></a><span data-ttu-id="b8395-103">Сбор данных (объект текстуры DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b8395-103">Gather (DirectX HLSL Texture Object)</span></span>

<span data-ttu-id="b8395-104">Получает четыре образца (только красный компонент), которые будут использоваться для интерполяции билинейной при выборке текстуры.</span><span class="sxs-lookup"><span data-stu-id="b8395-104">Gets the four samples (red component only) that would be used for bilinear interpolation when sampling a texture.</span></span>

<span data-ttu-id="b8395-105">&lt;Тип шаблона &gt; 4 Object. сбор данных (образец \_ состояния, \| Расположение float2 3 \| 4 \[ , смещение int2 \] );</span><span class="sxs-lookup"><span data-stu-id="b8395-105">&lt;Template Type&gt;4 Object.Gather( sampler\_state S, float2\|3\|4 Location \[, int2 Offset\] );</span></span>



 

## <a name="parameters"></a><span data-ttu-id="b8395-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b8395-106">Parameters</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b8395-107">Элемент</span><span class="sxs-lookup"><span data-stu-id="b8395-107">Item</span></span></th>
<th><span data-ttu-id="b8395-108">Описание</span><span class="sxs-lookup"><span data-stu-id="b8395-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b8395-109"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Объектами</em></span><span class="sxs-lookup"><span data-stu-id="b8395-109"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Object</em></span></span><br/></td>
<td><span data-ttu-id="b8395-110">Поддерживаются следующие типы <a href="dx-graphics-hlsl-to-type.md">объектов текстуры</a> : Texture2D, Texture2DArray, Текстурекубе, текстурекубеаррай.</span><span class="sxs-lookup"><span data-stu-id="b8395-110">The following <a href="dx-graphics-hlsl-to-type.md">texture-object</a> types are supported: Texture2D, Texture2DArray, TextureCube, TextureCubeArray.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b8395-111"><span id="S"></span><span id="s"></span><em>#D0</em></span><span class="sxs-lookup"><span data-stu-id="b8395-111"><span id="S"></span><span id="s"></span><em>S</em></span></span><br/></td>
<td><span data-ttu-id="b8395-112">окне <a href="dx-graphics-hlsl-sampler.md">Состояние образца</a>.</span><span class="sxs-lookup"><span data-stu-id="b8395-112">[in] A <a href="dx-graphics-hlsl-sampler.md">Sampler state</a>.</span></span> <span data-ttu-id="b8395-113">Это объект, объявленный в файле эффектов, который содержит назначения состояний.</span><span class="sxs-lookup"><span data-stu-id="b8395-113">This is an object declared in an effect file that contains state assignments.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b8395-114"><span id="Location"></span><span id="location"></span><span id="LOCATION"></span><em>Места</em></span><span class="sxs-lookup"><span data-stu-id="b8395-114"><span id="Location"></span><span id="location"></span><span id="LOCATION"></span><em>Location</em></span></span><br/></td>
<td><span data-ttu-id="b8395-115">окне Координаты текстуры.</span><span class="sxs-lookup"><span data-stu-id="b8395-115">[in] The texture coordinates.</span></span> <span data-ttu-id="b8395-116">Тип аргумента зависит от типа объекта текстуры.</span><span class="sxs-lookup"><span data-stu-id="b8395-116">The argument type is dependent on the texture-object type.</span></span> <br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="b8395-117">Тип Texture-Object</span><span class="sxs-lookup"><span data-stu-id="b8395-117">Texture-Object Type</span></span></th>
<th><span data-ttu-id="b8395-118">Тип параметра</span><span class="sxs-lookup"><span data-stu-id="b8395-118">Parameter Type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b8395-119">Texture2D</span><span class="sxs-lookup"><span data-stu-id="b8395-119">Texture2D</span></span></td>
<td><span data-ttu-id="b8395-120">float2</span><span class="sxs-lookup"><span data-stu-id="b8395-120">float2</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b8395-121">Texture2DArray, Текстурекубе</span><span class="sxs-lookup"><span data-stu-id="b8395-121">Texture2DArray, TextureCube</span></span></td>
<td><span data-ttu-id="b8395-122">float3</span><span class="sxs-lookup"><span data-stu-id="b8395-122">float3</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b8395-123">текстурекубеаррай</span><span class="sxs-lookup"><span data-stu-id="b8395-123">TextureCubeArray</span></span> </td>
<td><span data-ttu-id="b8395-124">float4</span><span class="sxs-lookup"><span data-stu-id="b8395-124">float4</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b8395-125"><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span><em>Собой</em></span><span class="sxs-lookup"><span data-stu-id="b8395-125"><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span><em>Offset</em></span></span></p></td>
<td><p><span data-ttu-id="b8395-126">окне Необязательное Смещение координаты текстуры, которое может использоваться для любого типа объекта текстуры. смещение применяется к расположению перед выборкой.</span><span class="sxs-lookup"><span data-stu-id="b8395-126">[in] An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="b8395-127">Тип аргумента зависит от типа объекта текстуры.</span><span class="sxs-lookup"><span data-stu-id="b8395-127">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="b8395-128">Для шейдеров, предназначенных для Shader Model 5,0 и более поздних версий, 6 наименее значимых битов каждого значения смещения учитываются как значение со знаком, а возвращает диапазон [-32.. 31].</span><span class="sxs-lookup"><span data-stu-id="b8395-128">For shaders targeting Shader Model 5.0 and above, the 6 least significant bits of each offset value is honored as a signed value, yielding [-32..31] range.</span></span> <span data-ttu-id="b8395-129">Для предыдущих шейдеров модели шейдера смещения должны быть прямыми целыми числами от-8 до 7.</span><span class="sxs-lookup"><span data-stu-id="b8395-129">For previous shader model shaders, offsets need to be immediate integers between -8 and 7.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="b8395-130">Тип Texture-Object</span><span class="sxs-lookup"><span data-stu-id="b8395-130">Texture-Object Type</span></span></th>
<th><span data-ttu-id="b8395-131">Тип параметра</span><span class="sxs-lookup"><span data-stu-id="b8395-131">Parameter Type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b8395-132">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="b8395-132">Texture2D, Texture2DArray</span></span></td>
<td><span data-ttu-id="b8395-133">int2</span><span class="sxs-lookup"><span data-stu-id="b8395-133">int2</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b8395-134">Текстурекубе, Текстурекубеаррай</span><span class="sxs-lookup"><span data-stu-id="b8395-134">TextureCube, TextureCubeArray</span></span> </td>
<td><span data-ttu-id="b8395-135">не поддерживается</span><span class="sxs-lookup"><span data-stu-id="b8395-135">not supported</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="return-value"></a><span data-ttu-id="b8395-136">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b8395-136">Return Value</span></span>

<span data-ttu-id="b8395-137">Вектор из четырех компонентов с четырьмя компонентами Красного типа данных, тип которых совпадает с типом шаблона текстуры.</span><span class="sxs-lookup"><span data-stu-id="b8395-137">A four-component vector, with four components of red data, whose type is the same as the texture's template type.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="b8395-138">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="b8395-138">Minimum Shader Model</span></span>

<span data-ttu-id="b8395-139">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="b8395-139">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="b8395-140">VS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="b8395-140">vs\_4\_0</span></span> | <span data-ttu-id="b8395-141">VS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="b8395-141">vs\_4\_1</span></span>  | <span data-ttu-id="b8395-142">PS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="b8395-142">ps\_4\_0</span></span> | <span data-ttu-id="b8395-143">PS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="b8395-143">ps\_4\_1</span></span>  | <span data-ttu-id="b8395-144">GS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="b8395-144">gs\_4\_0</span></span> | <span data-ttu-id="b8395-145">GS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="b8395-145">gs\_4\_1</span></span>  |
|----------|-----------|----------|-----------|----------|-----------|
|          | <span data-ttu-id="b8395-146">x</span><span class="sxs-lookup"><span data-stu-id="b8395-146">x</span></span>         |          | <span data-ttu-id="b8395-147">x</span><span class="sxs-lookup"><span data-stu-id="b8395-147">x</span></span>         |          | <span data-ttu-id="b8395-148">x</span><span class="sxs-lookup"><span data-stu-id="b8395-148">x</span></span>         |



 

1.  <span data-ttu-id="b8395-149">Текстурекубеаррай доступен в модели шейдеров 4,1 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="b8395-149">TextureCubeArray is available in Shader Model 4.1 or higher.</span></span>
2.  <span data-ttu-id="b8395-150">Модель шейдеров 4,1 доступна в Direct3D 10,1 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="b8395-150">Shader Model 4.1 is available in Direct3D 10.1 or higher.</span></span>

## <a name="example"></a><span data-ttu-id="b8395-151">Пример</span><span class="sxs-lookup"><span data-stu-id="b8395-151">Example</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="b8395-152">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="b8395-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b8395-153">Текстура-объект</span><span class="sxs-lookup"><span data-stu-id="b8395-153">Texture-Object</span></span>](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

 





