---
title: 'Функция Самплелевел:: Самплелевел (S, float, float, int, uint) для Texture2DArray'
description: 'Производит выборку текстуры на указанном уровне mipmap и возвращает состояние операции. Для Texture2DArray. | Функция Самплелевел:: Самплелевел (S, float, float, int, uint)'
ms.assetid: 2A561EE4-D7CF-44D4-AC93-F6841770B868
keywords:
- Функция Самплелевел HLSL
topic_type:
- apiref
api_name:
- SampleLevel
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 60e9f1df1a68d0971ac9d0ddf6be39eca03dd6ae
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/16/2021
ms.locfileid: "104998834"
---
# <a name="samplelevelsamplelevelsfloatfloatintuint-function-for-texture2darray"></a><span data-ttu-id="53501-106">Функция Самплелевел:: Самплелевел (S, float, float, int, uint) для Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="53501-106">SampleLevel::SampleLevel(S,float,float,int,uint) function for Texture2DArray</span></span>

<span data-ttu-id="53501-107">Производит выборку текстуры на указанном уровне mipmap и возвращает состояние операции.</span><span class="sxs-lookup"><span data-stu-id="53501-107">Samples a texture on the specified mipmap level and returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="53501-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="53501-108">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleLevel(
  in  SamplerState S,
  in  float        Location,
  in  float        LOD,
  in  int          Offset,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="53501-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="53501-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53501-110">*S* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="53501-110">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53501-111">Тип: **самплерстате**</span><span class="sxs-lookup"><span data-stu-id="53501-111">Type: **SamplerState**</span></span>

<span data-ttu-id="53501-112">[Состояние образца](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="53501-112">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="53501-113">Это объект, объявленный в файле эффектов, который содержит назначения состояний.</span><span class="sxs-lookup"><span data-stu-id="53501-113">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="53501-114">*Расположение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="53501-114">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53501-115">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="53501-115">Type: **float**</span></span>

<span data-ttu-id="53501-116">Координаты текстуры.</span><span class="sxs-lookup"><span data-stu-id="53501-116">The texture coordinates.</span></span> <span data-ttu-id="53501-117">Тип аргумента зависит от типа объекта текстуры.</span><span class="sxs-lookup"><span data-stu-id="53501-117">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="53501-118">Тип Texture-Object</span><span class="sxs-lookup"><span data-stu-id="53501-118">Texture-Object Type</span></span>                    | <span data-ttu-id="53501-119">Тип параметра</span><span class="sxs-lookup"><span data-stu-id="53501-119">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="53501-120">Texture1D</span><span class="sxs-lookup"><span data-stu-id="53501-120">Texture1D</span></span>                              | <span data-ttu-id="53501-121">FLOAT</span><span class="sxs-lookup"><span data-stu-id="53501-121">float</span></span>          |
| <span data-ttu-id="53501-122">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="53501-122">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="53501-123">float2</span><span class="sxs-lookup"><span data-stu-id="53501-123">float2</span></span>         |
| <span data-ttu-id="53501-124">Texture2DArray, Texture3D, Текстурекубе</span><span class="sxs-lookup"><span data-stu-id="53501-124">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="53501-125">float3</span><span class="sxs-lookup"><span data-stu-id="53501-125">float3</span></span>         |
| <span data-ttu-id="53501-126">текстурекубеаррай</span><span class="sxs-lookup"><span data-stu-id="53501-126">TextureCubeArray</span></span>                       | <span data-ttu-id="53501-127">float4</span><span class="sxs-lookup"><span data-stu-id="53501-127">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="53501-128">*Лод* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="53501-128">*LOD* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53501-129">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="53501-129">Type: **float**</span></span>

<span data-ttu-id="53501-130">\[\]число, указывающее уровень mipmap.</span><span class="sxs-lookup"><span data-stu-id="53501-130">\[in\] A number that specifies the mipmap level.</span></span> <span data-ttu-id="53501-131">Если значение равно ≤ 0, то используется mipmap уровень 0 (самая большая схема).</span><span class="sxs-lookup"><span data-stu-id="53501-131">If the value is ≤ 0, mipmap level 0 (biggest map) is used.</span></span> <span data-ttu-id="53501-132">Дробное значение (если оно указано) используется для интерполяции между двумя уровнями mipmap.</span><span class="sxs-lookup"><span data-stu-id="53501-132">The fractional value (if supplied) is used to interpolate between two mipmap levels.</span></span>

</dd> <dt>

<span data-ttu-id="53501-133">*Смещение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="53501-133">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53501-134">Тип: **int**</span><span class="sxs-lookup"><span data-stu-id="53501-134">Type: **int**</span></span>

<span data-ttu-id="53501-135">Необязательное Смещение координаты текстуры, которое может использоваться для любого типа объекта текстуры. смещение применяется к расположению перед выборкой.</span><span class="sxs-lookup"><span data-stu-id="53501-135">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="53501-136">Используйте смещение только с целочисленным миплевел; в противном случае можно получить результаты, которые не могут быть правильно преобразованы в оборудование.</span><span class="sxs-lookup"><span data-stu-id="53501-136">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="53501-137">Тип аргумента зависит от типа объекта текстуры.</span><span class="sxs-lookup"><span data-stu-id="53501-137">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="53501-138">Дополнительные сведения см. в разделе [применение целочисленных смещений](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="53501-138">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="53501-139">Тип Texture-Object</span><span class="sxs-lookup"><span data-stu-id="53501-139">Texture-Object Type</span></span>           | <span data-ttu-id="53501-140">Тип параметра</span><span class="sxs-lookup"><span data-stu-id="53501-140">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="53501-141">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="53501-141">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="53501-142">INT</span><span class="sxs-lookup"><span data-stu-id="53501-142">int</span></span>            |
| <span data-ttu-id="53501-143">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="53501-143">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="53501-144">int2</span><span class="sxs-lookup"><span data-stu-id="53501-144">int2</span></span>           |
| <span data-ttu-id="53501-145">Texture3D</span><span class="sxs-lookup"><span data-stu-id="53501-145">Texture3D</span></span>                     | <span data-ttu-id="53501-146">int3</span><span class="sxs-lookup"><span data-stu-id="53501-146">int3</span></span>           |
| <span data-ttu-id="53501-147">Текстурекубе, Текстурекубеаррай</span><span class="sxs-lookup"><span data-stu-id="53501-147">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="53501-148">не поддерживается</span><span class="sxs-lookup"><span data-stu-id="53501-148">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="53501-149">*Состояние* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="53501-149">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="53501-150">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="53501-150">Type: **uint**</span></span>

<span data-ttu-id="53501-151">Состояние операции.</span><span class="sxs-lookup"><span data-stu-id="53501-151">The status of the operation.</span></span> <span data-ttu-id="53501-152">Вы не можете получить доступ к состоянию напрямую; Вместо этого передайте состояние в подставляемую функцию [**чеккакцессфуллимаппед**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="53501-152">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="53501-153">**Чеккакцессфуллимаппед** возвращает **значение true** , если все значения из соответствующего **образца**, **сбора** или операции **загрузки** обращались к сопоставленным плиткам в [мозаичном ресурсе](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="53501-153">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="53501-154">Если какие бы то ни было значения были взяты из несопоставленной плитки, **чеккакцессфуллимаппед** возвращает **значение false**.</span><span class="sxs-lookup"><span data-stu-id="53501-154">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53501-155">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="53501-155">Return value</span></span>

<span data-ttu-id="53501-156">Тип: **[ **\_ Формат DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="53501-156">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="53501-157">Формат текстуры, который является одним из типизированных значений, перечисленных в [**\_ формате DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="53501-157">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="53501-158">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="53501-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53501-159">Методы Самплелевел</span><span class="sxs-lookup"><span data-stu-id="53501-159">SampleLevel methods</span></span>](texture2darray-samplelevel.md)
</dt> <dt>

[<span data-ttu-id="53501-160">**Texture2DArray**</span><span class="sxs-lookup"><span data-stu-id="53501-160">**Texture2DArray**</span></span>](sm5-object-texture2darray.md)
</dt> </dl>

 

 
