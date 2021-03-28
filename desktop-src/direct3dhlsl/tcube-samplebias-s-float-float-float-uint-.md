---
title: 'Функция Самплебиас:: Самплебиас (S, float, float, float, uint)'
description: 'Демонстрирует выбор текстуры после применения значения смещения к уровню mipmap с дополнительным значением для создания среза образцов значений уровня детализации (Лод). Возвращает состояние операции. | Функция Самплебиас:: Самплебиас (S, float, float, float, uint)'
ms.assetid: A2F10B9B-5DF2-4389-83A9-F6A29781BF0A
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
ms.openlocfilehash: 2f3a994d7b0f0c2d55ae3203db9f3205932c1a25
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104273557"
---
# <a name="samplebiassamplebiassfloatfloatfloatuint-function"></a><span data-ttu-id="e3ab9-106">Функция Самплебиас:: Самплебиас (S, float, float, float, uint)</span><span class="sxs-lookup"><span data-stu-id="e3ab9-106">SampleBias::SampleBias(S,float,float,float,uint) function</span></span>

<span data-ttu-id="e3ab9-107">Демонстрирует выбор текстуры после применения значения смещения к уровню mipmap с дополнительным значением для создания среза образцов значений уровня детализации (Лод).</span><span class="sxs-lookup"><span data-stu-id="e3ab9-107">Samples a texture, after applying the bias value to the mipmap level, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span> <span data-ttu-id="e3ab9-108">Возвращает состояние операции.</span><span class="sxs-lookup"><span data-stu-id="e3ab9-108">Returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3ab9-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e3ab9-109">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleBias(
  in  SamplerState S,
  in  float        Location,
  in  float        Bias,
  in  float        Clamp,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="e3ab9-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="e3ab9-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3ab9-111">*S* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="e3ab9-111">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3ab9-112">Тип: **самплерстате**</span><span class="sxs-lookup"><span data-stu-id="e3ab9-112">Type: **SamplerState**</span></span>

<span data-ttu-id="e3ab9-113">[Состояние образца](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="e3ab9-113">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="e3ab9-114">Это объект, объявленный в файле эффектов, который содержит назначения состояний.</span><span class="sxs-lookup"><span data-stu-id="e3ab9-114">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="e3ab9-115">*Расположение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e3ab9-115">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3ab9-116">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="e3ab9-116">Type: **float**</span></span>

<span data-ttu-id="e3ab9-117">Координаты текстуры.</span><span class="sxs-lookup"><span data-stu-id="e3ab9-117">The texture coordinates.</span></span> <span data-ttu-id="e3ab9-118">Тип аргумента зависит от типа объекта текстуры.</span><span class="sxs-lookup"><span data-stu-id="e3ab9-118">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="e3ab9-119">Тип Texture-Object</span><span class="sxs-lookup"><span data-stu-id="e3ab9-119">Texture-Object Type</span></span>                    | <span data-ttu-id="e3ab9-120">Тип параметра</span><span class="sxs-lookup"><span data-stu-id="e3ab9-120">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="e3ab9-121">Texture1D</span><span class="sxs-lookup"><span data-stu-id="e3ab9-121">Texture1D</span></span>                              | <span data-ttu-id="e3ab9-122">FLOAT</span><span class="sxs-lookup"><span data-stu-id="e3ab9-122">float</span></span>          |
| <span data-ttu-id="e3ab9-123">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="e3ab9-123">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="e3ab9-124">float2</span><span class="sxs-lookup"><span data-stu-id="e3ab9-124">float2</span></span>         |
| <span data-ttu-id="e3ab9-125">Texture2DArray, Texture3D, Текстурекубе</span><span class="sxs-lookup"><span data-stu-id="e3ab9-125">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="e3ab9-126">float3</span><span class="sxs-lookup"><span data-stu-id="e3ab9-126">float3</span></span>         |
| <span data-ttu-id="e3ab9-127">текстурекубеаррай</span><span class="sxs-lookup"><span data-stu-id="e3ab9-127">TextureCubeArray</span></span>                       | <span data-ttu-id="e3ab9-128">float4</span><span class="sxs-lookup"><span data-stu-id="e3ab9-128">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="e3ab9-129">*Уровень защиты* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e3ab9-129">*Bias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3ab9-130">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="e3ab9-130">Type: **float**</span></span>

<span data-ttu-id="e3ab9-131">Значение смещения, которое является числом с плавающей запятой от 0,0 до 1,0 включительно, применяется к MIP уровню перед выборкой.</span><span class="sxs-lookup"><span data-stu-id="e3ab9-131">The bias value, which is a floating-point number between 0.0 and 1.0 inclusive, is applied to a mip level before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="e3ab9-132">*Срез* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e3ab9-132">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3ab9-133">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="e3ab9-133">Type: **float**</span></span>

<span data-ttu-id="e3ab9-134">Необязательное значение для примера среза Лод значений.</span><span class="sxs-lookup"><span data-stu-id="e3ab9-134">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="e3ab9-135">Например, если передать значение среза 2.0 f, вы убедитесь, что ни один из отдельных примеров не имеет доступа к MIP уровню менее 2.0.</span><span class="sxs-lookup"><span data-stu-id="e3ab9-135">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> <dt>

<span data-ttu-id="e3ab9-136">*Состояние* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e3ab9-136">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e3ab9-137">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="e3ab9-137">Type: **uint**</span></span>

<span data-ttu-id="e3ab9-138">Состояние операции.</span><span class="sxs-lookup"><span data-stu-id="e3ab9-138">The status of the operation.</span></span> <span data-ttu-id="e3ab9-139">Вы не можете получить доступ к состоянию напрямую; Вместо этого передайте состояние в подставляемую функцию [**чеккакцессфуллимаппед**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="e3ab9-139">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="e3ab9-140">**Чеккакцессфуллимаппед** возвращает **значение true** , если все значения из соответствующего **образца**, **сбора** или операции **загрузки** обращались к сопоставленным плиткам в [мозаичном ресурсе](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="e3ab9-140">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="e3ab9-141">Если какие бы то ни было значения были взяты из несопоставленной плитки, **чеккакцессфуллимаппед** возвращает **значение false**.</span><span class="sxs-lookup"><span data-stu-id="e3ab9-141">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3ab9-142">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e3ab9-142">Return value</span></span>

<span data-ttu-id="e3ab9-143">Тип: **[ **\_ Формат DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="e3ab9-143">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="e3ab9-144">Формат текстуры, который является одним из типизированных значений, перечисленных в [**\_ формате DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="e3ab9-144">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="e3ab9-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e3ab9-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3ab9-146">Методы Самплебиас</span><span class="sxs-lookup"><span data-stu-id="e3ab9-146">SampleBias methods</span></span>](texturecube-samplebias.md)
</dt> <dt>

[<span data-ttu-id="e3ab9-147">**текстурекубе**</span><span class="sxs-lookup"><span data-stu-id="e3ab9-147">**TextureCube**</span></span>](texturecube.md)
</dt> </dl>

 

 
