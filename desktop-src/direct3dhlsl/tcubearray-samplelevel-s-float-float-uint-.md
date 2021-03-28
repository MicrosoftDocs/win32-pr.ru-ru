---
title: 'Функция Самплелевел:: Самплелевел (S, float, float, uint)'
description: 'Производит выборку текстуры на указанном уровне mipmap и возвращает состояние операции. | Функция Самплелевел:: Самплелевел (S, float, float, uint)'
ms.assetid: 3794D17F-BC70-4D3A-9F2C-ADF900983D2C
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
ms.openlocfilehash: 356e2779d82e886946e93d2071ae693279c07eb8
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104273530"
---
# <a name="samplelevelsamplelevelsfloatfloatuint-function"></a><span data-ttu-id="3e51d-105">Функция Самплелевел:: Самплелевел (S, float, float, uint)</span><span class="sxs-lookup"><span data-stu-id="3e51d-105">SampleLevel::SampleLevel(S,float,float,uint) function</span></span>

<span data-ttu-id="3e51d-106">Производит выборку текстуры на указанном уровне mipmap и возвращает состояние операции.</span><span class="sxs-lookup"><span data-stu-id="3e51d-106">Samples a texture on the specified mipmap level and returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e51d-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3e51d-107">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleLevel(
  in  SamplerState S,
  in  float        Location,
  in  float        LOD,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="3e51d-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="3e51d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e51d-109">*S* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="3e51d-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e51d-110">Тип: **самплерстате**</span><span class="sxs-lookup"><span data-stu-id="3e51d-110">Type: **SamplerState**</span></span>

<span data-ttu-id="3e51d-111">[Состояние образца](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="3e51d-111">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="3e51d-112">Это объект, объявленный в файле эффектов, который содержит назначения состояний.</span><span class="sxs-lookup"><span data-stu-id="3e51d-112">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="3e51d-113">*Расположение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3e51d-113">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e51d-114">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="3e51d-114">Type: **float**</span></span>

<span data-ttu-id="3e51d-115">Координаты текстуры.</span><span class="sxs-lookup"><span data-stu-id="3e51d-115">The texture coordinates.</span></span> <span data-ttu-id="3e51d-116">Тип аргумента зависит от типа объекта текстуры.</span><span class="sxs-lookup"><span data-stu-id="3e51d-116">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="3e51d-117">Тип Texture-Object</span><span class="sxs-lookup"><span data-stu-id="3e51d-117">Texture-Object Type</span></span>                    | <span data-ttu-id="3e51d-118">Тип параметра</span><span class="sxs-lookup"><span data-stu-id="3e51d-118">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="3e51d-119">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3e51d-119">Texture1D</span></span>                              | <span data-ttu-id="3e51d-120">FLOAT</span><span class="sxs-lookup"><span data-stu-id="3e51d-120">float</span></span>          |
| <span data-ttu-id="3e51d-121">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="3e51d-121">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="3e51d-122">float2</span><span class="sxs-lookup"><span data-stu-id="3e51d-122">float2</span></span>         |
| <span data-ttu-id="3e51d-123">Texture2DArray, Texture3D, Текстурекубе</span><span class="sxs-lookup"><span data-stu-id="3e51d-123">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="3e51d-124">float3</span><span class="sxs-lookup"><span data-stu-id="3e51d-124">float3</span></span>         |
| <span data-ttu-id="3e51d-125">текстурекубеаррай</span><span class="sxs-lookup"><span data-stu-id="3e51d-125">TextureCubeArray</span></span>                       | <span data-ttu-id="3e51d-126">float4</span><span class="sxs-lookup"><span data-stu-id="3e51d-126">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="3e51d-127">*Лод* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3e51d-127">*LOD* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e51d-128">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="3e51d-128">Type: **float**</span></span>

<span data-ttu-id="3e51d-129">\[\]число, указывающее уровень mipmap.</span><span class="sxs-lookup"><span data-stu-id="3e51d-129">\[in\] A number that specifies the mipmap level.</span></span> <span data-ttu-id="3e51d-130">Если значение равно ≤ 0, то используется mipmap уровень 0 (самая большая схема).</span><span class="sxs-lookup"><span data-stu-id="3e51d-130">If the value is ≤ 0, mipmap level 0 (biggest map) is used.</span></span> <span data-ttu-id="3e51d-131">Дробное значение (если оно указано) используется для интерполяции между двумя уровнями mipmap.</span><span class="sxs-lookup"><span data-stu-id="3e51d-131">The fractional value (if supplied) is used to interpolate between two mipmap levels.</span></span>

</dd> <dt>

<span data-ttu-id="3e51d-132">*Состояние* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="3e51d-132">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3e51d-133">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="3e51d-133">Type: **uint**</span></span>

<span data-ttu-id="3e51d-134">Состояние операции.</span><span class="sxs-lookup"><span data-stu-id="3e51d-134">The status of the operation.</span></span> <span data-ttu-id="3e51d-135">Вы не можете получить доступ к состоянию напрямую; Вместо этого передайте состояние в подставляемую функцию [**чеккакцессфуллимаппед**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="3e51d-135">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="3e51d-136">**Чеккакцессфуллимаппед** возвращает **значение true** , если все значения из соответствующего **образца**, **сбора** или операции **загрузки** обращались к сопоставленным плиткам в [мозаичном ресурсе](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="3e51d-136">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="3e51d-137">Если какие бы то ни было значения были взяты из несопоставленной плитки, **чеккакцессфуллимаппед** возвращает **значение false**.</span><span class="sxs-lookup"><span data-stu-id="3e51d-137">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3e51d-138">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3e51d-138">Return value</span></span>

<span data-ttu-id="3e51d-139">Тип: **[ **\_ Формат DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="3e51d-139">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="3e51d-140">Формат текстуры, который является одним из типизированных значений, перечисленных в [**\_ формате DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="3e51d-140">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="3e51d-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3e51d-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e51d-142">Методы Самплелевел</span><span class="sxs-lookup"><span data-stu-id="3e51d-142">SampleLevel methods</span></span>](texturecubearray-samplelevel.md)
</dt> <dt>

[<span data-ttu-id="3e51d-143">**текстурекубеаррай**</span><span class="sxs-lookup"><span data-stu-id="3e51d-143">**TextureCubeArray**</span></span>](texturecubearray.md)
</dt> </dl>

 

 
