---
title: 'Функция Самплебиас:: Самплебиас (S, float, float, float, uint) для Текстурекубеаррай'
description: 'Функция Самплебиас:: Самплебиас (S, float, float, float, uint) для Текстурекубеаррай выбирает текстуру после применения значения смещения к уровню mipmap.'
ms.assetid: 376F11E6-4FFF-4685-9285-9D6143C77F2D
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
ms.openlocfilehash: 4bcd5b2239a8b2d219fde28b1c9a00a693906b5c
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/02/2021
ms.locfileid: "106187893"
---
# <a name="samplebiassamplebiassfloatfloatfloatuint-function-for-texturecubearray"></a><span data-ttu-id="7cddd-104">Функция Самплебиас:: Самплебиас (S, float, float, float, uint) для Текстурекубеаррай</span><span class="sxs-lookup"><span data-stu-id="7cddd-104">SampleBias::SampleBias(S,float,float,float,uint) function for TextureCubeArray</span></span>

<span data-ttu-id="7cddd-105">Демонстрирует выбор текстуры после применения значения смещения к уровню mipmap с дополнительным значением для создания среза образцов значений уровня детализации (Лод).</span><span class="sxs-lookup"><span data-stu-id="7cddd-105">Samples a texture, after applying the bias value to the mipmap level, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span> <span data-ttu-id="7cddd-106">Возвращает состояние операции.</span><span class="sxs-lookup"><span data-stu-id="7cddd-106">Returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="7cddd-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7cddd-107">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleBias(
  in  SamplerState S,
  in  float        Location,
  in  float        Bias,
  in  float        Clamp,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="7cddd-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="7cddd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7cddd-109">*S* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="7cddd-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7cddd-110">Тип: **самплерстате**</span><span class="sxs-lookup"><span data-stu-id="7cddd-110">Type: **SamplerState**</span></span>

<span data-ttu-id="7cddd-111">[Состояние образца](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="7cddd-111">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="7cddd-112">Это объект, объявленный в файле эффектов, который содержит назначения состояний.</span><span class="sxs-lookup"><span data-stu-id="7cddd-112">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="7cddd-113">*Расположение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7cddd-113">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7cddd-114">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="7cddd-114">Type: **float**</span></span>

<span data-ttu-id="7cddd-115">Координаты текстуры.</span><span class="sxs-lookup"><span data-stu-id="7cddd-115">The texture coordinates.</span></span> <span data-ttu-id="7cddd-116">Тип аргумента зависит от типа объекта текстуры.</span><span class="sxs-lookup"><span data-stu-id="7cddd-116">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="7cddd-117">Тип Texture-Object</span><span class="sxs-lookup"><span data-stu-id="7cddd-117">Texture-Object Type</span></span>                    | <span data-ttu-id="7cddd-118">Тип параметра</span><span class="sxs-lookup"><span data-stu-id="7cddd-118">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="7cddd-119">Texture1D</span><span class="sxs-lookup"><span data-stu-id="7cddd-119">Texture1D</span></span>                              | <span data-ttu-id="7cddd-120">FLOAT</span><span class="sxs-lookup"><span data-stu-id="7cddd-120">float</span></span>          |
| <span data-ttu-id="7cddd-121">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="7cddd-121">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="7cddd-122">float2</span><span class="sxs-lookup"><span data-stu-id="7cddd-122">float2</span></span>         |
| <span data-ttu-id="7cddd-123">Texture2DArray, Texture3D, Текстурекубе</span><span class="sxs-lookup"><span data-stu-id="7cddd-123">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="7cddd-124">float3</span><span class="sxs-lookup"><span data-stu-id="7cddd-124">float3</span></span>         |
| <span data-ttu-id="7cddd-125">текстурекубеаррай</span><span class="sxs-lookup"><span data-stu-id="7cddd-125">TextureCubeArray</span></span>                       | <span data-ttu-id="7cddd-126">float4</span><span class="sxs-lookup"><span data-stu-id="7cddd-126">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="7cddd-127">*Уровень защиты* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7cddd-127">*Bias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7cddd-128">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="7cddd-128">Type: **float**</span></span>

<span data-ttu-id="7cddd-129">Значение смещения, которое является числом с плавающей запятой от 0,0 до 1,0 включительно, применяется к MIP уровню перед выборкой.</span><span class="sxs-lookup"><span data-stu-id="7cddd-129">The bias value, which is a floating-point number between 0.0 and 1.0 inclusive, is applied to a mip level before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="7cddd-130">*Срез* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7cddd-130">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7cddd-131">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="7cddd-131">Type: **float**</span></span>

<span data-ttu-id="7cddd-132">Необязательное значение для примера среза Лод значений.</span><span class="sxs-lookup"><span data-stu-id="7cddd-132">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="7cddd-133">Например, если передать значение среза 2.0 f, вы убедитесь, что ни один из отдельных примеров не имеет доступа к MIP уровню менее 2.0.</span><span class="sxs-lookup"><span data-stu-id="7cddd-133">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> <dt>

<span data-ttu-id="7cddd-134">*Состояние* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="7cddd-134">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7cddd-135">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="7cddd-135">Type: **uint**</span></span>

<span data-ttu-id="7cddd-136">Состояние операции.</span><span class="sxs-lookup"><span data-stu-id="7cddd-136">The status of the operation.</span></span> <span data-ttu-id="7cddd-137">Вы не можете получить доступ к состоянию напрямую; Вместо этого передайте состояние в подставляемую функцию [**чеккакцессфуллимаппед**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="7cddd-137">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="7cddd-138">**Чеккакцессфуллимаппед** возвращает **значение true** , если все значения из соответствующего **образца**, **сбора** или операции **загрузки** обращались к сопоставленным плиткам в [мозаичном ресурсе](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="7cddd-138">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="7cddd-139">Если какие бы то ни было значения были взяты из несопоставленной плитки, **чеккакцессфуллимаппед** возвращает **значение false**.</span><span class="sxs-lookup"><span data-stu-id="7cddd-139">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7cddd-140">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7cddd-140">Return value</span></span>

<span data-ttu-id="7cddd-141">Тип: **[ **\_ Формат DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="7cddd-141">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="7cddd-142">Формат текстуры, который является одним из типизированных значений, перечисленных в [**\_ формате DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="7cddd-142">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="7cddd-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7cddd-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7cddd-144">Методы Самплебиас</span><span class="sxs-lookup"><span data-stu-id="7cddd-144">SampleBias methods</span></span>](texturecubearray-samplebias.md)
</dt> <dt>

[<span data-ttu-id="7cddd-145">**текстурекубеаррай**</span><span class="sxs-lookup"><span data-stu-id="7cddd-145">**TextureCubeArray**</span></span>](texturecubearray.md)
</dt> </dl>

 

 
