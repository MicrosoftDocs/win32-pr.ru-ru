---
title: 'Функция Самплекмплевелзеро:: Самплекмплевелзеро (S, float, float, int, uint) для Texture1D'
description: Производит выборку текстуры только на уровне mipmap 0 и сравнивает результат со значением сравнения, а затем возвращает состояние операции. Для Texture1D.
ms.assetid: A2F7FD4A-49D8-41B3-A5AF-7B54A8B5266C
keywords:
- Функция Самплекмплевелзеро HLSL
topic_type:
- apiref
api_name:
- SampleCmpLevelZero
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a63644cff0bcc5a437ff4ae3e1dffba8f5a0676c
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/16/2021
ms.locfileid: "104274001"
---
# <a name="samplecmplevelzerosamplecmplevelzerosfloatfloatintuint-function-for-texture1d"></a><span data-ttu-id="f1eed-105">Функция Самплекмплевелзеро:: Самплекмплевелзеро (S, float, float, int, uint) для Texture1D</span><span class="sxs-lookup"><span data-stu-id="f1eed-105">SampleCmpLevelZero::SampleCmpLevelZero(S,float,float,int,uint) function for Texture1D</span></span>

<span data-ttu-id="f1eed-106">Производит выборку текстуры только на уровне mipmap 0 и сравнивает результат со значением сравнения.</span><span class="sxs-lookup"><span data-stu-id="f1eed-106">Samples a texture on mipmap level 0 only and compares the result to a comparison value.</span></span> <span data-ttu-id="f1eed-107">Возвращает состояние операции.</span><span class="sxs-lookup"><span data-stu-id="f1eed-107">Returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1eed-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f1eed-108">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleCmpLevelZero(
  in  SamplerState S,
  in  float        Location,
  in  float        CompareValue,
  in  int          Offset,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="f1eed-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="f1eed-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1eed-110">*S* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="f1eed-110">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1eed-111">Тип: **самплерстате**</span><span class="sxs-lookup"><span data-stu-id="f1eed-111">Type: **SamplerState**</span></span>

<span data-ttu-id="f1eed-112">[Состояние образца](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="f1eed-112">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="f1eed-113">Это объект, объявленный в файле эффектов, который содержит назначения состояний.</span><span class="sxs-lookup"><span data-stu-id="f1eed-113">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="f1eed-114">*Расположение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f1eed-114">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1eed-115">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="f1eed-115">Type: **float**</span></span>

<span data-ttu-id="f1eed-116">Координаты текстуры.</span><span class="sxs-lookup"><span data-stu-id="f1eed-116">The texture coordinates.</span></span> <span data-ttu-id="f1eed-117">Тип аргумента зависит от типа объекта текстуры.</span><span class="sxs-lookup"><span data-stu-id="f1eed-117">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="f1eed-118">Тип Texture-Object</span><span class="sxs-lookup"><span data-stu-id="f1eed-118">Texture-Object Type</span></span>                    | <span data-ttu-id="f1eed-119">Тип параметра</span><span class="sxs-lookup"><span data-stu-id="f1eed-119">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="f1eed-120">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f1eed-120">Texture1D</span></span>                              | <span data-ttu-id="f1eed-121">FLOAT</span><span class="sxs-lookup"><span data-stu-id="f1eed-121">float</span></span>          |
| <span data-ttu-id="f1eed-122">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="f1eed-122">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="f1eed-123">float2</span><span class="sxs-lookup"><span data-stu-id="f1eed-123">float2</span></span>         |
| <span data-ttu-id="f1eed-124">Texture2DArray, Texture3D, Текстурекубе</span><span class="sxs-lookup"><span data-stu-id="f1eed-124">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="f1eed-125">float3</span><span class="sxs-lookup"><span data-stu-id="f1eed-125">float3</span></span>         |
| <span data-ttu-id="f1eed-126">текстурекубеаррай</span><span class="sxs-lookup"><span data-stu-id="f1eed-126">TextureCubeArray</span></span>                       | <span data-ttu-id="f1eed-127">float4</span><span class="sxs-lookup"><span data-stu-id="f1eed-127">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="f1eed-128">*Компаревалуе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f1eed-128">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1eed-129">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="f1eed-129">Type: **float**</span></span>

<span data-ttu-id="f1eed-130">Значение с плавающей запятой, используемое в качестве значения сравнения.</span><span class="sxs-lookup"><span data-stu-id="f1eed-130">A floating-point value to use as a comparison value.</span></span>

</dd> <dt>

<span data-ttu-id="f1eed-131">*Смещение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f1eed-131">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1eed-132">Тип: **int**</span><span class="sxs-lookup"><span data-stu-id="f1eed-132">Type: **int**</span></span>

<span data-ttu-id="f1eed-133">Необязательное Смещение координаты текстуры, которое может использоваться для любого типа объекта текстуры. смещение применяется к расположению перед выборкой.</span><span class="sxs-lookup"><span data-stu-id="f1eed-133">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="f1eed-134">Используйте смещение только с целочисленным миплевел; в противном случае можно получить результаты, которые не могут быть правильно преобразованы в оборудование.</span><span class="sxs-lookup"><span data-stu-id="f1eed-134">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="f1eed-135">Тип аргумента зависит от типа объекта текстуры.</span><span class="sxs-lookup"><span data-stu-id="f1eed-135">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="f1eed-136">Дополнительные сведения см. в разделе [применение целочисленных смещений](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="f1eed-136">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="f1eed-137">Тип Texture-Object</span><span class="sxs-lookup"><span data-stu-id="f1eed-137">Texture-Object Type</span></span>           | <span data-ttu-id="f1eed-138">Тип параметра</span><span class="sxs-lookup"><span data-stu-id="f1eed-138">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="f1eed-139">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="f1eed-139">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="f1eed-140">INT</span><span class="sxs-lookup"><span data-stu-id="f1eed-140">int</span></span>            |
| <span data-ttu-id="f1eed-141">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="f1eed-141">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="f1eed-142">int2</span><span class="sxs-lookup"><span data-stu-id="f1eed-142">int2</span></span>           |
| <span data-ttu-id="f1eed-143">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f1eed-143">Texture3D</span></span>                     | <span data-ttu-id="f1eed-144">int3</span><span class="sxs-lookup"><span data-stu-id="f1eed-144">int3</span></span>           |
| <span data-ttu-id="f1eed-145">Текстурекубе, Текстурекубеаррай</span><span class="sxs-lookup"><span data-stu-id="f1eed-145">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="f1eed-146">не поддерживается</span><span class="sxs-lookup"><span data-stu-id="f1eed-146">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="f1eed-147">*Состояние* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="f1eed-147">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f1eed-148">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="f1eed-148">Type: **uint**</span></span>

<span data-ttu-id="f1eed-149">Состояние операции.</span><span class="sxs-lookup"><span data-stu-id="f1eed-149">The status of the operation.</span></span> <span data-ttu-id="f1eed-150">Вы не можете получить доступ к состоянию напрямую; Вместо этого передайте состояние в подставляемую функцию [**чеккакцессфуллимаппед**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="f1eed-150">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="f1eed-151">**Чеккакцессфуллимаппед** возвращает **значение true** , если все значения из соответствующего **образца**, **сбора** или операции **загрузки** обращались к сопоставленным плиткам в [мозаичном ресурсе](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="f1eed-151">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="f1eed-152">Если какие бы то ни было значения были взяты из несопоставленной плитки, **чеккакцессфуллимаппед** возвращает **значение false**.</span><span class="sxs-lookup"><span data-stu-id="f1eed-152">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f1eed-153">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f1eed-153">Return value</span></span>

<span data-ttu-id="f1eed-154">Тип: **[ **\_ Формат DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="f1eed-154">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="f1eed-155">Формат текстуры, который является одним из типизированных значений, перечисленных в [**\_ формате DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="f1eed-155">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="f1eed-156">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f1eed-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1eed-157">Методы Самплекмплевелзеро</span><span class="sxs-lookup"><span data-stu-id="f1eed-157">SampleCmpLevelZero methods</span></span>](texture1d-samplecmplevelzero.md)
</dt> </dl>

 

 
