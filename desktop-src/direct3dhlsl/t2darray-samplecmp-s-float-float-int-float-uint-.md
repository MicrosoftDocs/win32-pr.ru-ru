---
title: 'Функция Самплекмп:: Самплекмп (S, float, float, int, float, uint) для Texture2DArray'
description: Эта функция выбирает текстуру, используя значение сравнения для отклонения выборок, с необязательным значением для фиксации образцов значений уровня детализации (Лод) до. Для Texture2DArray.
ms.assetid: 847A6B79-3A66-4209-AB01-7C1FDA8A433A
keywords:
- Функция Самплекмп HLSL
topic_type:
- apiref
api_name:
- SampleCmp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cc8957ca2f6c1eb3e4a665b5d6df134c854ccc3c
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/16/2021
ms.locfileid: "104273999"
---
# <a name="samplecmpsamplecmpsfloatfloatintfloatuint-function-for-texture2darray"></a><span data-ttu-id="3991c-105">Функция Самплекмп:: Самплекмп (S, float, float, int, float, uint) для Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="3991c-105">SampleCmp::SampleCmp(S,float,float,int,float,uint) function for Texture2DArray</span></span>

<span data-ttu-id="3991c-106">Выбор текстуры с использованием значения сравнения для отклонения выборок с необязательным значением для фиксации значений уровня детализации (Лод) в.</span><span class="sxs-lookup"><span data-stu-id="3991c-106">Samples a texture, using a comparison value to reject samples, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span> <span data-ttu-id="3991c-107">Возвращает состояние операции.</span><span class="sxs-lookup"><span data-stu-id="3991c-107">Returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="3991c-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3991c-108">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleCmp(
  in  SamplerState S,
  in  float        Location,
  in  float        CompareValue,
  in  int          Offset,
  in  float        Clamp,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="3991c-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="3991c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3991c-110">*S* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="3991c-110">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3991c-111">Тип: **самплерстате**</span><span class="sxs-lookup"><span data-stu-id="3991c-111">Type: **SamplerState**</span></span>

<span data-ttu-id="3991c-112">[Состояние образца](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="3991c-112">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="3991c-113">Это объект, объявленный в файле эффектов, который содержит назначения состояний.</span><span class="sxs-lookup"><span data-stu-id="3991c-113">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="3991c-114">*Расположение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3991c-114">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3991c-115">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="3991c-115">Type: **float**</span></span>

<span data-ttu-id="3991c-116">Координаты текстуры.</span><span class="sxs-lookup"><span data-stu-id="3991c-116">The texture coordinates.</span></span> <span data-ttu-id="3991c-117">Тип аргумента зависит от типа объекта текстуры.</span><span class="sxs-lookup"><span data-stu-id="3991c-117">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="3991c-118">Тип Texture-Object</span><span class="sxs-lookup"><span data-stu-id="3991c-118">Texture-Object Type</span></span>                    | <span data-ttu-id="3991c-119">Тип параметра</span><span class="sxs-lookup"><span data-stu-id="3991c-119">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="3991c-120">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3991c-120">Texture1D</span></span>                              | <span data-ttu-id="3991c-121">FLOAT</span><span class="sxs-lookup"><span data-stu-id="3991c-121">float</span></span>          |
| <span data-ttu-id="3991c-122">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="3991c-122">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="3991c-123">float2</span><span class="sxs-lookup"><span data-stu-id="3991c-123">float2</span></span>         |
| <span data-ttu-id="3991c-124">Texture2DArray, Texture3D, Текстурекубе</span><span class="sxs-lookup"><span data-stu-id="3991c-124">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="3991c-125">float3</span><span class="sxs-lookup"><span data-stu-id="3991c-125">float3</span></span>         |
| <span data-ttu-id="3991c-126">текстурекубеаррай</span><span class="sxs-lookup"><span data-stu-id="3991c-126">TextureCubeArray</span></span>                       | <span data-ttu-id="3991c-127">float4</span><span class="sxs-lookup"><span data-stu-id="3991c-127">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="3991c-128">*Компаревалуе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3991c-128">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3991c-129">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="3991c-129">Type: **float**</span></span>

<span data-ttu-id="3991c-130">Значение с плавающей запятой, используемое в качестве значения сравнения.</span><span class="sxs-lookup"><span data-stu-id="3991c-130">A floating-point value to use as a comparison value.</span></span>

</dd> <dt>

<span data-ttu-id="3991c-131">*Смещение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3991c-131">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3991c-132">Тип: **int**</span><span class="sxs-lookup"><span data-stu-id="3991c-132">Type: **int**</span></span>

<span data-ttu-id="3991c-133">Необязательное Смещение координаты текстуры, которое может использоваться для любого типа объекта текстуры. смещение применяется к расположению перед выборкой.</span><span class="sxs-lookup"><span data-stu-id="3991c-133">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="3991c-134">Используйте смещение только с целочисленным миплевел; в противном случае можно получить результаты, которые не могут быть правильно преобразованы в оборудование.</span><span class="sxs-lookup"><span data-stu-id="3991c-134">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="3991c-135">Тип аргумента зависит от типа объекта текстуры.</span><span class="sxs-lookup"><span data-stu-id="3991c-135">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="3991c-136">Дополнительные сведения см. в разделе [применение целочисленных смещений](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="3991c-136">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="3991c-137">Тип Texture-Object</span><span class="sxs-lookup"><span data-stu-id="3991c-137">Texture-Object Type</span></span>           | <span data-ttu-id="3991c-138">Тип параметра</span><span class="sxs-lookup"><span data-stu-id="3991c-138">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="3991c-139">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="3991c-139">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="3991c-140">INT</span><span class="sxs-lookup"><span data-stu-id="3991c-140">int</span></span>            |
| <span data-ttu-id="3991c-141">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="3991c-141">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="3991c-142">int2</span><span class="sxs-lookup"><span data-stu-id="3991c-142">int2</span></span>           |
| <span data-ttu-id="3991c-143">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3991c-143">Texture3D</span></span>                     | <span data-ttu-id="3991c-144">int3</span><span class="sxs-lookup"><span data-stu-id="3991c-144">int3</span></span>           |
| <span data-ttu-id="3991c-145">Текстурекубе, Текстурекубеаррай</span><span class="sxs-lookup"><span data-stu-id="3991c-145">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="3991c-146">не поддерживается</span><span class="sxs-lookup"><span data-stu-id="3991c-146">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="3991c-147">*Срез* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3991c-147">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3991c-148">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="3991c-148">Type: **float**</span></span>

<span data-ttu-id="3991c-149">Необязательное значение для примера среза Лод значений.</span><span class="sxs-lookup"><span data-stu-id="3991c-149">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="3991c-150">Например, если передать значение среза 2.0 f, вы убедитесь, что ни один из отдельных примеров не имеет доступа к MIP уровню менее 2.0.</span><span class="sxs-lookup"><span data-stu-id="3991c-150">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> <dt>

<span data-ttu-id="3991c-151">*Состояние* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="3991c-151">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3991c-152">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="3991c-152">Type: **uint**</span></span>

<span data-ttu-id="3991c-153">Состояние операции.</span><span class="sxs-lookup"><span data-stu-id="3991c-153">The status of the operation.</span></span> <span data-ttu-id="3991c-154">Вы не можете получить доступ к состоянию напрямую; Вместо этого передайте состояние в подставляемую функцию [**чеккакцессфуллимаппед**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="3991c-154">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="3991c-155">**Чеккакцессфуллимаппед** возвращает **значение true** , если все значения из соответствующего **образца**, **сбора** или операции **загрузки** обращались к сопоставленным плиткам в [мозаичном ресурсе](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="3991c-155">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="3991c-156">Если какие бы то ни было значения были взяты из несопоставленной плитки, **чеккакцессфуллимаппед** возвращает **значение false**.</span><span class="sxs-lookup"><span data-stu-id="3991c-156">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3991c-157">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3991c-157">Return value</span></span>

<span data-ttu-id="3991c-158">Тип: **[ **\_ Формат DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="3991c-158">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="3991c-159">Формат текстуры, который является одним из типизированных значений, перечисленных в [**\_ формате DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="3991c-159">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="3991c-160">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3991c-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3991c-161">Методы Самплекмп</span><span class="sxs-lookup"><span data-stu-id="3991c-161">SampleCmp methods</span></span>](texture2darray-samplecmp.md)
</dt> <dt>

[<span data-ttu-id="3991c-162">**Texture2DArray**</span><span class="sxs-lookup"><span data-stu-id="3991c-162">**Texture2DArray**</span></span>](sm5-object-texture2darray.md)
</dt> </dl>

 

 
