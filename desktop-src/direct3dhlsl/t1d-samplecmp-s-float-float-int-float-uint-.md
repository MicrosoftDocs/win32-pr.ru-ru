---
title: 'Функция Самплекмп:: Самплекмп (S, float, float, int, float, uint) для Texture1D'
description: Функция выбирает текстуру, используя значение сравнения для отклонения выборок, с необязательным значением для среза образцов значений уровня детализации (Лод) в. Для Texture1D.
ms.assetid: D2320225-4BC6-4229-A624-6D0F105DD788
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
ms.openlocfilehash: 690ede3cac45d05a3000fe60654255daef5202f7
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/16/2021
ms.locfileid: "104987353"
---
# <a name="samplecmpsamplecmpsfloatfloatintfloatuint-function-for-texture1d"></a><span data-ttu-id="c9a52-105">Функция Самплекмп:: Самплекмп (S, float, float, int, float, uint) для Texture1D</span><span class="sxs-lookup"><span data-stu-id="c9a52-105">SampleCmp::SampleCmp(S,float,float,int,float,uint) function for Texture1D</span></span>

<span data-ttu-id="c9a52-106">Выбор текстуры с использованием значения сравнения для отклонения выборок с необязательным значением для фиксации значений уровня детализации (Лод) в.</span><span class="sxs-lookup"><span data-stu-id="c9a52-106">Samples a texture, using a comparison value to reject samples, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span> <span data-ttu-id="c9a52-107">Возвращает состояние операции.</span><span class="sxs-lookup"><span data-stu-id="c9a52-107">Returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9a52-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c9a52-108">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="c9a52-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="c9a52-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9a52-110">*S* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="c9a52-110">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9a52-111">Тип: **самплерстате**</span><span class="sxs-lookup"><span data-stu-id="c9a52-111">Type: **SamplerState**</span></span>

<span data-ttu-id="c9a52-112">[Состояние образца](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="c9a52-112">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="c9a52-113">Это объект, объявленный в файле эффектов, который содержит назначения состояний.</span><span class="sxs-lookup"><span data-stu-id="c9a52-113">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="c9a52-114">*Расположение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c9a52-114">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9a52-115">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="c9a52-115">Type: **float**</span></span>

<span data-ttu-id="c9a52-116">Координаты текстуры.</span><span class="sxs-lookup"><span data-stu-id="c9a52-116">The texture coordinates.</span></span> <span data-ttu-id="c9a52-117">Тип аргумента зависит от типа объекта текстуры.</span><span class="sxs-lookup"><span data-stu-id="c9a52-117">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="c9a52-118">Тип Texture-Object</span><span class="sxs-lookup"><span data-stu-id="c9a52-118">Texture-Object Type</span></span>                    | <span data-ttu-id="c9a52-119">Тип параметра</span><span class="sxs-lookup"><span data-stu-id="c9a52-119">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="c9a52-120">Texture1D</span><span class="sxs-lookup"><span data-stu-id="c9a52-120">Texture1D</span></span>                              | <span data-ttu-id="c9a52-121">FLOAT</span><span class="sxs-lookup"><span data-stu-id="c9a52-121">float</span></span>          |
| <span data-ttu-id="c9a52-122">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="c9a52-122">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="c9a52-123">float2</span><span class="sxs-lookup"><span data-stu-id="c9a52-123">float2</span></span>         |
| <span data-ttu-id="c9a52-124">Texture2DArray, Texture3D, Текстурекубе</span><span class="sxs-lookup"><span data-stu-id="c9a52-124">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="c9a52-125">float3</span><span class="sxs-lookup"><span data-stu-id="c9a52-125">float3</span></span>         |
| <span data-ttu-id="c9a52-126">текстурекубеаррай</span><span class="sxs-lookup"><span data-stu-id="c9a52-126">TextureCubeArray</span></span>                       | <span data-ttu-id="c9a52-127">float4</span><span class="sxs-lookup"><span data-stu-id="c9a52-127">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="c9a52-128">*Компаревалуе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c9a52-128">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9a52-129">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="c9a52-129">Type: **float**</span></span>

<span data-ttu-id="c9a52-130">Значение с плавающей запятой, используемое в качестве значения сравнения.</span><span class="sxs-lookup"><span data-stu-id="c9a52-130">A floating-point value to use as a comparison value.</span></span>

</dd> <dt>

<span data-ttu-id="c9a52-131">*Смещение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c9a52-131">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9a52-132">Тип: **int**</span><span class="sxs-lookup"><span data-stu-id="c9a52-132">Type: **int**</span></span>

<span data-ttu-id="c9a52-133">Необязательное Смещение координаты текстуры, которое может использоваться для любого типа объекта текстуры. смещение применяется к расположению перед выборкой.</span><span class="sxs-lookup"><span data-stu-id="c9a52-133">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="c9a52-134">Используйте смещение только с целочисленным миплевел; в противном случае можно получить результаты, которые не могут быть правильно преобразованы в оборудование.</span><span class="sxs-lookup"><span data-stu-id="c9a52-134">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="c9a52-135">Тип аргумента зависит от типа объекта текстуры.</span><span class="sxs-lookup"><span data-stu-id="c9a52-135">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="c9a52-136">Дополнительные сведения см. в разделе [применение целочисленных смещений](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="c9a52-136">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="c9a52-137">Тип Texture-Object</span><span class="sxs-lookup"><span data-stu-id="c9a52-137">Texture-Object Type</span></span>           | <span data-ttu-id="c9a52-138">Тип параметра</span><span class="sxs-lookup"><span data-stu-id="c9a52-138">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="c9a52-139">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="c9a52-139">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="c9a52-140">INT</span><span class="sxs-lookup"><span data-stu-id="c9a52-140">int</span></span>            |
| <span data-ttu-id="c9a52-141">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="c9a52-141">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="c9a52-142">int2</span><span class="sxs-lookup"><span data-stu-id="c9a52-142">int2</span></span>           |
| <span data-ttu-id="c9a52-143">Texture3D</span><span class="sxs-lookup"><span data-stu-id="c9a52-143">Texture3D</span></span>                     | <span data-ttu-id="c9a52-144">int3</span><span class="sxs-lookup"><span data-stu-id="c9a52-144">int3</span></span>           |
| <span data-ttu-id="c9a52-145">Текстурекубе, Текстурекубеаррай</span><span class="sxs-lookup"><span data-stu-id="c9a52-145">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="c9a52-146">не поддерживается</span><span class="sxs-lookup"><span data-stu-id="c9a52-146">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="c9a52-147">*Срез* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c9a52-147">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9a52-148">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="c9a52-148">Type: **float**</span></span>

<span data-ttu-id="c9a52-149">Необязательное значение для примера среза Лод значений.</span><span class="sxs-lookup"><span data-stu-id="c9a52-149">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="c9a52-150">Например, если передать значение среза 2.0 f, вы убедитесь, что ни один из отдельных примеров не имеет доступа к MIP уровню менее 2.0.</span><span class="sxs-lookup"><span data-stu-id="c9a52-150">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> <dt>

<span data-ttu-id="c9a52-151">*Состояние* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="c9a52-151">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c9a52-152">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="c9a52-152">Type: **uint**</span></span>

<span data-ttu-id="c9a52-153">Состояние операции.</span><span class="sxs-lookup"><span data-stu-id="c9a52-153">The status of the operation.</span></span> <span data-ttu-id="c9a52-154">Вы не можете получить доступ к состоянию напрямую; Вместо этого передайте состояние в подставляемую функцию [**чеккакцессфуллимаппед**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="c9a52-154">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="c9a52-155">**Чеккакцессфуллимаппед** возвращает **значение true** , если все значения из соответствующего **образца**, **сбора** или операции **загрузки** обращались к сопоставленным плиткам в [мозаичном ресурсе](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="c9a52-155">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="c9a52-156">Если какие бы то ни было значения были взяты из несопоставленной плитки, **чеккакцессфуллимаппед** возвращает **значение false**.</span><span class="sxs-lookup"><span data-stu-id="c9a52-156">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9a52-157">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c9a52-157">Return value</span></span>

<span data-ttu-id="c9a52-158">Тип: **[ **\_ Формат DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="c9a52-158">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="c9a52-159">Формат текстуры, который является одним из типизированных значений, перечисленных в [**\_ формате DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="c9a52-159">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="c9a52-160">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c9a52-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9a52-161">Методы Самплекмп</span><span class="sxs-lookup"><span data-stu-id="c9a52-161">SampleCmp methods</span></span>](texture1d-samplecmp.md)
</dt> </dl>

 

 
