---
title: 'Функция Самплелевел:: Самплелевел (S, float, float, int, uint) для Texture3D'
description: 'Производит выборку текстуры на указанном уровне mipmap и возвращает состояние операции. Для Texture3D. | Функция Самплелевел:: Самплелевел (S, float, float, int, uint)'
ms.assetid: D79247AC-A922-49C7-BAC6-807C31F279B1
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
ms.openlocfilehash: 2ae92245b6a8b6cff89805a73dd724e5aeac43a9
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/16/2021
ms.locfileid: "104987398"
---
# <a name="samplelevelsamplelevelsfloatfloatintuint-function-for-texture3d"></a><span data-ttu-id="f5f76-106">Функция Самплелевел:: Самплелевел (S, float, float, int, uint) для Texture3D</span><span class="sxs-lookup"><span data-stu-id="f5f76-106">SampleLevel::SampleLevel(S,float,float,int,uint) function for Texture3D</span></span>

<span data-ttu-id="f5f76-107">Производит выборку текстуры на указанном уровне mipmap и возвращает состояние операции.</span><span class="sxs-lookup"><span data-stu-id="f5f76-107">Samples a texture on the specified mipmap level and returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5f76-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f5f76-108">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleLevel(
  in  SamplerState S,
  in  float        Location,
  in  float        LOD,
  in  int          Offset,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="f5f76-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="f5f76-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5f76-110">*S* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="f5f76-110">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5f76-111">Тип: **самплерстате**</span><span class="sxs-lookup"><span data-stu-id="f5f76-111">Type: **SamplerState**</span></span>

<span data-ttu-id="f5f76-112">[Состояние образца](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="f5f76-112">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="f5f76-113">Это объект, объявленный в файле эффектов, который содержит назначения состояний.</span><span class="sxs-lookup"><span data-stu-id="f5f76-113">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="f5f76-114">*Расположение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f5f76-114">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5f76-115">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="f5f76-115">Type: **float**</span></span>

<span data-ttu-id="f5f76-116">Координаты текстуры.</span><span class="sxs-lookup"><span data-stu-id="f5f76-116">The texture coordinates.</span></span> <span data-ttu-id="f5f76-117">Тип аргумента зависит от типа объекта текстуры.</span><span class="sxs-lookup"><span data-stu-id="f5f76-117">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="f5f76-118">Тип Texture-Object</span><span class="sxs-lookup"><span data-stu-id="f5f76-118">Texture-Object Type</span></span>                    | <span data-ttu-id="f5f76-119">Тип параметра</span><span class="sxs-lookup"><span data-stu-id="f5f76-119">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="f5f76-120">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f5f76-120">Texture1D</span></span>                              | <span data-ttu-id="f5f76-121">FLOAT</span><span class="sxs-lookup"><span data-stu-id="f5f76-121">float</span></span>          |
| <span data-ttu-id="f5f76-122">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="f5f76-122">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="f5f76-123">float2</span><span class="sxs-lookup"><span data-stu-id="f5f76-123">float2</span></span>         |
| <span data-ttu-id="f5f76-124">Texture2DArray, Texture3D, Текстурекубе</span><span class="sxs-lookup"><span data-stu-id="f5f76-124">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="f5f76-125">float3</span><span class="sxs-lookup"><span data-stu-id="f5f76-125">float3</span></span>         |
| <span data-ttu-id="f5f76-126">текстурекубеаррай</span><span class="sxs-lookup"><span data-stu-id="f5f76-126">TextureCubeArray</span></span>                       | <span data-ttu-id="f5f76-127">float4</span><span class="sxs-lookup"><span data-stu-id="f5f76-127">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="f5f76-128">*Лод* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f5f76-128">*LOD* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5f76-129">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="f5f76-129">Type: **float**</span></span>

<span data-ttu-id="f5f76-130">\[\]число, указывающее уровень mipmap.</span><span class="sxs-lookup"><span data-stu-id="f5f76-130">\[in\] A number that specifies the mipmap level.</span></span> <span data-ttu-id="f5f76-131">Если значение равно ≤ 0, то используется mipmap уровень 0 (самая большая схема).</span><span class="sxs-lookup"><span data-stu-id="f5f76-131">If the value is ≤ 0, mipmap level 0 (biggest map) is used.</span></span> <span data-ttu-id="f5f76-132">Дробное значение (если оно указано) используется для интерполяции между двумя уровнями mipmap.</span><span class="sxs-lookup"><span data-stu-id="f5f76-132">The fractional value (if supplied) is used to interpolate between two mipmap levels.</span></span>

</dd> <dt>

<span data-ttu-id="f5f76-133">*Смещение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f5f76-133">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5f76-134">Тип: **int**</span><span class="sxs-lookup"><span data-stu-id="f5f76-134">Type: **int**</span></span>

<span data-ttu-id="f5f76-135">Необязательное Смещение координаты текстуры, которое может использоваться для любого типа объекта текстуры. смещение применяется к расположению перед выборкой.</span><span class="sxs-lookup"><span data-stu-id="f5f76-135">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="f5f76-136">Используйте смещение только с целочисленным миплевел; в противном случае можно получить результаты, которые не могут быть правильно преобразованы в оборудование.</span><span class="sxs-lookup"><span data-stu-id="f5f76-136">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="f5f76-137">Тип аргумента зависит от типа объекта текстуры.</span><span class="sxs-lookup"><span data-stu-id="f5f76-137">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="f5f76-138">Дополнительные сведения см. в разделе [применение целочисленных смещений](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="f5f76-138">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="f5f76-139">Тип Texture-Object</span><span class="sxs-lookup"><span data-stu-id="f5f76-139">Texture-Object Type</span></span>           | <span data-ttu-id="f5f76-140">Тип параметра</span><span class="sxs-lookup"><span data-stu-id="f5f76-140">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="f5f76-141">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="f5f76-141">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="f5f76-142">INT</span><span class="sxs-lookup"><span data-stu-id="f5f76-142">int</span></span>            |
| <span data-ttu-id="f5f76-143">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="f5f76-143">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="f5f76-144">int2</span><span class="sxs-lookup"><span data-stu-id="f5f76-144">int2</span></span>           |
| <span data-ttu-id="f5f76-145">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f5f76-145">Texture3D</span></span>                     | <span data-ttu-id="f5f76-146">int3</span><span class="sxs-lookup"><span data-stu-id="f5f76-146">int3</span></span>           |
| <span data-ttu-id="f5f76-147">Текстурекубе, Текстурекубеаррай</span><span class="sxs-lookup"><span data-stu-id="f5f76-147">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="f5f76-148">не поддерживается</span><span class="sxs-lookup"><span data-stu-id="f5f76-148">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="f5f76-149">*Состояние* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="f5f76-149">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f5f76-150">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="f5f76-150">Type: **uint**</span></span>

<span data-ttu-id="f5f76-151">Состояние операции.</span><span class="sxs-lookup"><span data-stu-id="f5f76-151">The status of the operation.</span></span> <span data-ttu-id="f5f76-152">Вы не можете получить доступ к состоянию напрямую; Вместо этого передайте состояние в подставляемую функцию [**чеккакцессфуллимаппед**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="f5f76-152">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="f5f76-153">**Чеккакцессфуллимаппед** возвращает **значение true** , если все значения из соответствующего **образца**, **сбора** или операции **загрузки** обращались к сопоставленным плиткам в [мозаичном ресурсе](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="f5f76-153">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="f5f76-154">Если какие бы то ни было значения были взяты из несопоставленной плитки, **чеккакцессфуллимаппед** возвращает **значение false**.</span><span class="sxs-lookup"><span data-stu-id="f5f76-154">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5f76-155">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f5f76-155">Return value</span></span>

<span data-ttu-id="f5f76-156">Тип: **[ **\_ Формат DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="f5f76-156">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="f5f76-157">Формат текстуры, который является одним из типизированных значений, перечисленных в [**\_ формате DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="f5f76-157">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="f5f76-158">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f5f76-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5f76-159">Методы Самплелевел</span><span class="sxs-lookup"><span data-stu-id="f5f76-159">SampleLevel methods</span></span>](texture3d-samplelevel.md)
</dt> <dt>

[<span data-ttu-id="f5f76-160">**Texture3D**</span><span class="sxs-lookup"><span data-stu-id="f5f76-160">**Texture3D**</span></span>](sm5-object-texture3d.md)
</dt> </dl>

 

 
