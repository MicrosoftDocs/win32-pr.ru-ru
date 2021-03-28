---
title: 'Функция Texture1DArray:: Sample (S, float, int, float, uint)'
description: 'Выбирает текстуру с необязательным значением для фиксации в качестве примера значений уровня детализации (Лод) и возвращает состояние операции. | Функция Texture1DArray:: Sample (S, float, int, float, uint)'
ms.assetid: 584901B7-4F58-4491-9543-F27433386292
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
ms.openlocfilehash: 4a2f608d7dbbd4eec51139b6f285529849f708af
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104998264"
---
# <a name="texture1darraysamplesfloatintfloatuint-function"></a><span data-ttu-id="9e34a-105">Функция Texture1DArray:: Sample (S, float, int, float, uint)</span><span class="sxs-lookup"><span data-stu-id="9e34a-105">Texture1DArray::Sample(S,float,int,float,uint) function</span></span>

<span data-ttu-id="9e34a-106">Выбирает текстуру с необязательным значением для фиксации в качестве примера значений уровня детализации (Лод) и возвращает состояние операции.</span><span class="sxs-lookup"><span data-stu-id="9e34a-106">Samples a texture with an optional value to clamp sample level-of-detail (LOD) values to, and returns status of the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e34a-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9e34a-107">Syntax</span></span>


``` syntax
DXGI_FORMAT Sample(
  in  SamplerState S,
  in  float        Location,
  in  int          Offset,
  in  float        Clamp,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="9e34a-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="9e34a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e34a-109">*S* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="9e34a-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e34a-110">Тип: **самплерстате**</span><span class="sxs-lookup"><span data-stu-id="9e34a-110">Type: **SamplerState**</span></span>

<span data-ttu-id="9e34a-111">[Состояние образца](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="9e34a-111">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="9e34a-112">Это объект, объявленный в файле эффектов, который содержит назначения состояний.</span><span class="sxs-lookup"><span data-stu-id="9e34a-112">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="9e34a-113">*Расположение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9e34a-113">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e34a-114">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="9e34a-114">Type: **float**</span></span>

<span data-ttu-id="9e34a-115">Координаты текстуры.</span><span class="sxs-lookup"><span data-stu-id="9e34a-115">The texture coordinates.</span></span> <span data-ttu-id="9e34a-116">Тип аргумента зависит от типа объекта текстуры.</span><span class="sxs-lookup"><span data-stu-id="9e34a-116">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="9e34a-117">Тип Texture-Object</span><span class="sxs-lookup"><span data-stu-id="9e34a-117">Texture-Object Type</span></span>                    | <span data-ttu-id="9e34a-118">Тип параметра</span><span class="sxs-lookup"><span data-stu-id="9e34a-118">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="9e34a-119">Texture1D</span><span class="sxs-lookup"><span data-stu-id="9e34a-119">Texture1D</span></span>                              | <span data-ttu-id="9e34a-120">FLOAT</span><span class="sxs-lookup"><span data-stu-id="9e34a-120">float</span></span>          |
| <span data-ttu-id="9e34a-121">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="9e34a-121">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="9e34a-122">float2</span><span class="sxs-lookup"><span data-stu-id="9e34a-122">float2</span></span>         |
| <span data-ttu-id="9e34a-123">Texture2DArray, Texture3D, Текстурекубе</span><span class="sxs-lookup"><span data-stu-id="9e34a-123">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="9e34a-124">float3</span><span class="sxs-lookup"><span data-stu-id="9e34a-124">float3</span></span>         |
| <span data-ttu-id="9e34a-125">текстурекубеаррай</span><span class="sxs-lookup"><span data-stu-id="9e34a-125">TextureCubeArray</span></span>                       | <span data-ttu-id="9e34a-126">float4</span><span class="sxs-lookup"><span data-stu-id="9e34a-126">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="9e34a-127">*Смещение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9e34a-127">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e34a-128">Тип: **int**</span><span class="sxs-lookup"><span data-stu-id="9e34a-128">Type: **int**</span></span>

<span data-ttu-id="9e34a-129">Необязательное Смещение координаты текстуры, которое может использоваться для любого типа объекта текстуры. смещение применяется к расположению перед выборкой.</span><span class="sxs-lookup"><span data-stu-id="9e34a-129">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="9e34a-130">Используйте смещение только с целочисленным миплевел; в противном случае можно получить результаты, которые не могут быть правильно преобразованы в оборудование.</span><span class="sxs-lookup"><span data-stu-id="9e34a-130">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="9e34a-131">Тип аргумента зависит от типа объекта текстуры.</span><span class="sxs-lookup"><span data-stu-id="9e34a-131">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="9e34a-132">Дополнительные сведения см. в разделе [применение целочисленных смещений](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="9e34a-132">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="9e34a-133">Тип Texture-Object</span><span class="sxs-lookup"><span data-stu-id="9e34a-133">Texture-Object Type</span></span>           | <span data-ttu-id="9e34a-134">Тип параметра</span><span class="sxs-lookup"><span data-stu-id="9e34a-134">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="9e34a-135">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="9e34a-135">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="9e34a-136">INT</span><span class="sxs-lookup"><span data-stu-id="9e34a-136">int</span></span>            |
| <span data-ttu-id="9e34a-137">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="9e34a-137">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="9e34a-138">int2</span><span class="sxs-lookup"><span data-stu-id="9e34a-138">int2</span></span>           |
| <span data-ttu-id="9e34a-139">Texture3D</span><span class="sxs-lookup"><span data-stu-id="9e34a-139">Texture3D</span></span>                     | <span data-ttu-id="9e34a-140">int3</span><span class="sxs-lookup"><span data-stu-id="9e34a-140">int3</span></span>           |
| <span data-ttu-id="9e34a-141">Текстурекубе, Текстурекубеаррай</span><span class="sxs-lookup"><span data-stu-id="9e34a-141">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="9e34a-142">не поддерживается</span><span class="sxs-lookup"><span data-stu-id="9e34a-142">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="9e34a-143">*Срез* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9e34a-143">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e34a-144">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="9e34a-144">Type: **float**</span></span>

<span data-ttu-id="9e34a-145">Необязательное значение для примера среза Лод значений.</span><span class="sxs-lookup"><span data-stu-id="9e34a-145">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="9e34a-146">Например, если передать значение среза 2.0 f, вы убедитесь, что ни один из отдельных примеров не имеет доступа к MIP уровню менее 2.0.</span><span class="sxs-lookup"><span data-stu-id="9e34a-146">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> <dt>

<span data-ttu-id="9e34a-147">*Состояние* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="9e34a-147">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9e34a-148">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="9e34a-148">Type: **uint**</span></span>

<span data-ttu-id="9e34a-149">Состояние операции.</span><span class="sxs-lookup"><span data-stu-id="9e34a-149">The status of the operation.</span></span> <span data-ttu-id="9e34a-150">Вы не можете получить доступ к состоянию напрямую; Вместо этого передайте состояние в подставляемую функцию [**чеккакцессфуллимаппед**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="9e34a-150">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="9e34a-151">**Чеккакцессфуллимаппед** возвращает **значение true** , если все значения из соответствующего **образца**, **сбора** или операции **загрузки** обращались к сопоставленным плиткам в [мозаичном ресурсе](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="9e34a-151">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="9e34a-152">Если какие бы то ни было значения были взяты из несопоставленной плитки, **чеккакцессфуллимаппед** возвращает **значение false**.</span><span class="sxs-lookup"><span data-stu-id="9e34a-152">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9e34a-153">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9e34a-153">Return value</span></span>

<span data-ttu-id="9e34a-154">Тип: **[ **\_ Формат DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="9e34a-154">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="9e34a-155">Формат текстуры, который является одним из типизированных значений, перечисленных в [**\_ формате DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="9e34a-155">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="9e34a-156">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9e34a-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e34a-157">Примеры методов</span><span class="sxs-lookup"><span data-stu-id="9e34a-157">Sample methods</span></span>](texture1darray-sample.md)
</dt> </dl>

 

 
