---
title: 'Функция Самплелевел:: Самплелевел (S, float, float, int, uint) для Texture2D'
description: Пример Texture2D на указанном уровне mipmap и возвращает состояние операции.
ms.assetid: B021D42E-9F63-4CCE-939B-F93D91F7CB80
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
ms.openlocfilehash: 1455454649e24bd984948a81837181a7bcdba11a
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/16/2021
ms.locfileid: "104998846"
---
# <a name="samplelevelsamplelevelsfloatfloatintuint-function-for-texture2d"></a><span data-ttu-id="73e96-104">Функция Самплелевел:: Самплелевел (S, float, float, int, uint) для Texture2D</span><span class="sxs-lookup"><span data-stu-id="73e96-104">SampleLevel::SampleLevel(S,float,float,int,uint) function for Texture2D</span></span>

<span data-ttu-id="73e96-105">Пример [**Texture2D**](sm5-object-texture2d.md) на указанном уровне mipmap и возвращает состояние операции.</span><span class="sxs-lookup"><span data-stu-id="73e96-105">Samples a [**Texture2D**](sm5-object-texture2d.md) on the specified mipmap level and returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="73e96-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="73e96-106">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleLevel(
  in  SamplerState S,
  in  float        Location,
  in  float        LOD,
  in  int          Offset,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="73e96-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="73e96-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73e96-108">*S* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="73e96-108">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73e96-109">Тип: **самплерстате**</span><span class="sxs-lookup"><span data-stu-id="73e96-109">Type: **SamplerState**</span></span>

<span data-ttu-id="73e96-110">[Состояние образца](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="73e96-110">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="73e96-111">Это объект, объявленный в файле эффектов, который содержит назначения состояний.</span><span class="sxs-lookup"><span data-stu-id="73e96-111">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="73e96-112">*Расположение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="73e96-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73e96-113">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="73e96-113">Type: **float**</span></span>

<span data-ttu-id="73e96-114">Координаты текстуры.</span><span class="sxs-lookup"><span data-stu-id="73e96-114">The texture coordinates.</span></span> <span data-ttu-id="73e96-115">Тип аргумента зависит от типа объекта текстуры.</span><span class="sxs-lookup"><span data-stu-id="73e96-115">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="73e96-116">Тип Texture-Object</span><span class="sxs-lookup"><span data-stu-id="73e96-116">Texture-Object Type</span></span>                    | <span data-ttu-id="73e96-117">Тип параметра</span><span class="sxs-lookup"><span data-stu-id="73e96-117">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="73e96-118">Texture1D</span><span class="sxs-lookup"><span data-stu-id="73e96-118">Texture1D</span></span>                              | <span data-ttu-id="73e96-119">FLOAT</span><span class="sxs-lookup"><span data-stu-id="73e96-119">float</span></span>          |
| <span data-ttu-id="73e96-120">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="73e96-120">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="73e96-121">float2</span><span class="sxs-lookup"><span data-stu-id="73e96-121">float2</span></span>         |
| <span data-ttu-id="73e96-122">Texture2DArray, Texture3D, Текстурекубе</span><span class="sxs-lookup"><span data-stu-id="73e96-122">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="73e96-123">float3</span><span class="sxs-lookup"><span data-stu-id="73e96-123">float3</span></span>         |
| <span data-ttu-id="73e96-124">текстурекубеаррай</span><span class="sxs-lookup"><span data-stu-id="73e96-124">TextureCubeArray</span></span>                       | <span data-ttu-id="73e96-125">float4</span><span class="sxs-lookup"><span data-stu-id="73e96-125">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="73e96-126">*Лод* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="73e96-126">*LOD* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73e96-127">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="73e96-127">Type: **float**</span></span>

<span data-ttu-id="73e96-128">\[\]число, указывающее уровень mipmap.</span><span class="sxs-lookup"><span data-stu-id="73e96-128">\[in\] A number that specifies the mipmap level.</span></span> <span data-ttu-id="73e96-129">Если значение равно ≤ 0, то используется mipmap уровень 0 (самая большая схема).</span><span class="sxs-lookup"><span data-stu-id="73e96-129">If the value is ≤ 0, mipmap level 0 (biggest map) is used.</span></span> <span data-ttu-id="73e96-130">Дробное значение (если оно указано) используется для интерполяции между двумя уровнями mipmap.</span><span class="sxs-lookup"><span data-stu-id="73e96-130">The fractional value (if supplied) is used to interpolate between two mipmap levels.</span></span>

</dd> <dt>

<span data-ttu-id="73e96-131">*Смещение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="73e96-131">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73e96-132">Тип: **int**</span><span class="sxs-lookup"><span data-stu-id="73e96-132">Type: **int**</span></span>

<span data-ttu-id="73e96-133">Необязательное Смещение координаты текстуры, которое может использоваться для любого типа объекта текстуры. смещение применяется к расположению перед выборкой.</span><span class="sxs-lookup"><span data-stu-id="73e96-133">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="73e96-134">Используйте смещение только с целочисленным миплевел; в противном случае можно получить результаты, которые не могут быть правильно преобразованы в оборудование.</span><span class="sxs-lookup"><span data-stu-id="73e96-134">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="73e96-135">Тип аргумента зависит от типа объекта текстуры.</span><span class="sxs-lookup"><span data-stu-id="73e96-135">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="73e96-136">Дополнительные сведения см. в разделе [применение целочисленных смещений](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="73e96-136">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="73e96-137">Тип Texture-Object</span><span class="sxs-lookup"><span data-stu-id="73e96-137">Texture-Object Type</span></span>           | <span data-ttu-id="73e96-138">Тип параметра</span><span class="sxs-lookup"><span data-stu-id="73e96-138">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="73e96-139">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="73e96-139">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="73e96-140">INT</span><span class="sxs-lookup"><span data-stu-id="73e96-140">int</span></span>            |
| <span data-ttu-id="73e96-141">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="73e96-141">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="73e96-142">int2</span><span class="sxs-lookup"><span data-stu-id="73e96-142">int2</span></span>           |
| <span data-ttu-id="73e96-143">Texture3D</span><span class="sxs-lookup"><span data-stu-id="73e96-143">Texture3D</span></span>                     | <span data-ttu-id="73e96-144">int3</span><span class="sxs-lookup"><span data-stu-id="73e96-144">int3</span></span>           |
| <span data-ttu-id="73e96-145">Текстурекубе, Текстурекубеаррай</span><span class="sxs-lookup"><span data-stu-id="73e96-145">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="73e96-146">не поддерживается</span><span class="sxs-lookup"><span data-stu-id="73e96-146">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="73e96-147">*Состояние* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="73e96-147">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="73e96-148">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="73e96-148">Type: **uint**</span></span>

<span data-ttu-id="73e96-149">Состояние операции.</span><span class="sxs-lookup"><span data-stu-id="73e96-149">The status of the operation.</span></span> <span data-ttu-id="73e96-150">Вы не можете получить доступ к состоянию напрямую; Вместо этого передайте состояние в подставляемую функцию [**чеккакцессфуллимаппед**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="73e96-150">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="73e96-151">**Чеккакцессфуллимаппед** возвращает **значение true** , если все значения из соответствующего **образца**, **сбора** или операции **загрузки** обращались к сопоставленным плиткам в [мозаичном ресурсе](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="73e96-151">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="73e96-152">Если какие бы то ни было значения были взяты из несопоставленной плитки, **чеккакцессфуллимаппед** возвращает **значение false**.</span><span class="sxs-lookup"><span data-stu-id="73e96-152">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="73e96-153">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="73e96-153">Return value</span></span>

<span data-ttu-id="73e96-154">Тип: **[ **\_ Формат DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="73e96-154">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="73e96-155">Формат текстуры, который является одним из типизированных значений, перечисленных в [**\_ формате DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="73e96-155">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="73e96-156">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="73e96-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73e96-157">Методы Самплелевел</span><span class="sxs-lookup"><span data-stu-id="73e96-157">SampleLevel methods</span></span>](texture2d-samplelevel.md)
</dt> </dl>

 

 
