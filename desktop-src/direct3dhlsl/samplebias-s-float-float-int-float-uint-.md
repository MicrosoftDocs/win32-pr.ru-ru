---
title: 'Функция Самплебиас:: Самплебиас (S, float, float, int, float, uint) для Texture2D'
description: 'Функция Самплебиас:: Самплебиас (S, float, float, int, float, uint) выбирает Texture2D, после применения значения смещения к уровню mipmap.'
ms.assetid: ACABF551-1DBF-4979-B0B1-D025E04EC08C
keywords:
- Функция Самплебиас HLSL
topic_type:
- apiref
api_name:
- SampleBias
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 86840748d12a92eca24b8d0d2bfba26eee69cff5
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/16/2021
ms.locfileid: "104987380"
---
# <a name="samplebiassamplebiassfloatfloatintfloatuint-function-for-texture2d"></a><span data-ttu-id="a9a2c-104">Функция Самплебиас:: Самплебиас (S, float, float, int, float, uint) для Texture2D</span><span class="sxs-lookup"><span data-stu-id="a9a2c-104">SampleBias::SampleBias(S,float,float,int,float,uint) function for Texture2D</span></span>

<span data-ttu-id="a9a2c-105">Пример [**Texture2D**](sm5-object-texture2d.md). После применения значения смещения к уровню mipmap с необязательным значением для создания среза образца уровня детализации (Лод) до значения.</span><span class="sxs-lookup"><span data-stu-id="a9a2c-105">Samples a [**Texture2D**](sm5-object-texture2d.md), after applying the bias value to the mipmap level, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span> <span data-ttu-id="a9a2c-106">Возвращает состояние операции.</span><span class="sxs-lookup"><span data-stu-id="a9a2c-106">Returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9a2c-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a9a2c-107">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleBias(
  in  SamplerState S,
  in  float        Location,
  in  float        Bias,
  in  int          Offset,
  in  float        Clamp,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="a9a2c-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="a9a2c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a9a2c-109">*S* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="a9a2c-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9a2c-110">Тип: **самплерстате**</span><span class="sxs-lookup"><span data-stu-id="a9a2c-110">Type: **SamplerState**</span></span>

<span data-ttu-id="a9a2c-111">[Состояние образца](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="a9a2c-111">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="a9a2c-112">Это объект, объявленный в файле эффектов, который содержит назначения состояний.</span><span class="sxs-lookup"><span data-stu-id="a9a2c-112">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="a9a2c-113">*Расположение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a9a2c-113">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9a2c-114">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="a9a2c-114">Type: **float**</span></span>

<span data-ttu-id="a9a2c-115">Координаты текстуры.</span><span class="sxs-lookup"><span data-stu-id="a9a2c-115">The texture coordinates.</span></span> <span data-ttu-id="a9a2c-116">Тип аргумента зависит от типа объекта текстуры.</span><span class="sxs-lookup"><span data-stu-id="a9a2c-116">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="a9a2c-117">Тип Texture-Object</span><span class="sxs-lookup"><span data-stu-id="a9a2c-117">Texture-Object Type</span></span>                    | <span data-ttu-id="a9a2c-118">Тип параметра</span><span class="sxs-lookup"><span data-stu-id="a9a2c-118">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="a9a2c-119">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a9a2c-119">Texture1D</span></span>                              | <span data-ttu-id="a9a2c-120">FLOAT</span><span class="sxs-lookup"><span data-stu-id="a9a2c-120">float</span></span>          |
| <span data-ttu-id="a9a2c-121">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="a9a2c-121">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="a9a2c-122">float2</span><span class="sxs-lookup"><span data-stu-id="a9a2c-122">float2</span></span>         |
| <span data-ttu-id="a9a2c-123">Texture2DArray, Texture3D, Текстурекубе</span><span class="sxs-lookup"><span data-stu-id="a9a2c-123">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="a9a2c-124">float3</span><span class="sxs-lookup"><span data-stu-id="a9a2c-124">float3</span></span>         |
| <span data-ttu-id="a9a2c-125">текстурекубеаррай</span><span class="sxs-lookup"><span data-stu-id="a9a2c-125">TextureCubeArray</span></span>                       | <span data-ttu-id="a9a2c-126">float4</span><span class="sxs-lookup"><span data-stu-id="a9a2c-126">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="a9a2c-127">*Уровень защиты* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a9a2c-127">*Bias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9a2c-128">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="a9a2c-128">Type: **float**</span></span>

<span data-ttu-id="a9a2c-129">Значение смещения, которое является числом с плавающей запятой от 0,0 до 1,0 включительно, применяется к MIP уровню перед выборкой.</span><span class="sxs-lookup"><span data-stu-id="a9a2c-129">The bias value, which is a floating-point number between 0.0 and 1.0 inclusive, is applied to a mip level before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="a9a2c-130">*Смещение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a9a2c-130">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9a2c-131">Тип: **int**</span><span class="sxs-lookup"><span data-stu-id="a9a2c-131">Type: **int**</span></span>

<span data-ttu-id="a9a2c-132">Необязательное Смещение координаты текстуры, которое может использоваться для любого типа объекта текстуры. смещение применяется к расположению перед выборкой.</span><span class="sxs-lookup"><span data-stu-id="a9a2c-132">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="a9a2c-133">Используйте смещение только с целочисленным миплевел; в противном случае можно получить результаты, которые не могут быть правильно преобразованы в оборудование.</span><span class="sxs-lookup"><span data-stu-id="a9a2c-133">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="a9a2c-134">Тип аргумента зависит от типа объекта текстуры.</span><span class="sxs-lookup"><span data-stu-id="a9a2c-134">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="a9a2c-135">Дополнительные сведения см. в разделе [применение целочисленных смещений](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="a9a2c-135">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="a9a2c-136">Тип Texture-Object</span><span class="sxs-lookup"><span data-stu-id="a9a2c-136">Texture-Object Type</span></span>           | <span data-ttu-id="a9a2c-137">Тип параметра</span><span class="sxs-lookup"><span data-stu-id="a9a2c-137">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="a9a2c-138">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="a9a2c-138">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="a9a2c-139">INT</span><span class="sxs-lookup"><span data-stu-id="a9a2c-139">int</span></span>            |
| <span data-ttu-id="a9a2c-140">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="a9a2c-140">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="a9a2c-141">int2</span><span class="sxs-lookup"><span data-stu-id="a9a2c-141">int2</span></span>           |
| <span data-ttu-id="a9a2c-142">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a9a2c-142">Texture3D</span></span>                     | <span data-ttu-id="a9a2c-143">int3</span><span class="sxs-lookup"><span data-stu-id="a9a2c-143">int3</span></span>           |
| <span data-ttu-id="a9a2c-144">Текстурекубе, Текстурекубеаррай</span><span class="sxs-lookup"><span data-stu-id="a9a2c-144">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="a9a2c-145">не поддерживается</span><span class="sxs-lookup"><span data-stu-id="a9a2c-145">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="a9a2c-146">*Срез* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a9a2c-146">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9a2c-147">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="a9a2c-147">Type: **float**</span></span>

<span data-ttu-id="a9a2c-148">Необязательное значение для примера среза Лод значений.</span><span class="sxs-lookup"><span data-stu-id="a9a2c-148">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="a9a2c-149">Например, если передать значение среза 2.0 f, вы убедитесь, что ни один из отдельных примеров не имеет доступа к MIP уровню менее 2.0.</span><span class="sxs-lookup"><span data-stu-id="a9a2c-149">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> <dt>

<span data-ttu-id="a9a2c-150">*Состояние* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="a9a2c-150">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a9a2c-151">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="a9a2c-151">Type: **uint**</span></span>

<span data-ttu-id="a9a2c-152">Состояние операции.</span><span class="sxs-lookup"><span data-stu-id="a9a2c-152">The status of the operation.</span></span> <span data-ttu-id="a9a2c-153">Вы не можете получить доступ к состоянию напрямую; Вместо этого передайте состояние в подставляемую функцию [**чеккакцессфуллимаппед**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="a9a2c-153">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="a9a2c-154">**Чеккакцессфуллимаппед** возвращает **значение true** , если все значения из соответствующего **образца**, **сбора** или операции **загрузки** обращались к сопоставленным плиткам в [мозаичном ресурсе](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="a9a2c-154">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="a9a2c-155">Если какие бы то ни было значения были взяты из несопоставленной плитки, **чеккакцессфуллимаппед** возвращает **значение false**.</span><span class="sxs-lookup"><span data-stu-id="a9a2c-155">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a9a2c-156">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a9a2c-156">Return value</span></span>

<span data-ttu-id="a9a2c-157">Тип: **[ **\_ Формат DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="a9a2c-157">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="a9a2c-158">Формат текстуры, который является одним из типизированных значений, перечисленных в [**\_ формате DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="a9a2c-158">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="a9a2c-159">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a9a2c-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9a2c-160">Методы Самплебиас</span><span class="sxs-lookup"><span data-stu-id="a9a2c-160">SampleBias methods</span></span>](texture2d-samplebias.md)
</dt> </dl>

 

 
