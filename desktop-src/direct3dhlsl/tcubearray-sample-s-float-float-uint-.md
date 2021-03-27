---
title: 'Функция Текстурекубеаррай:: Sample (S, float, float, uint)'
description: 'Выбирает текстуру с необязательным значением для фиксации в качестве примера значений уровня детализации (Лод) и возвращает состояние операции. | Функция Текстурекубеаррай:: Sample (S, float, float, uint)'
ms.assetid: 5645841D-A32E-452E-873C-E070CF6A4C00
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
ms.openlocfilehash: 24e6d77698507f0d1673b66954db8e78466ac728
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "103820628"
---
# <a name="texturecubearraysamplesfloatfloatuint-function"></a><span data-ttu-id="41fc9-105">Функция Текстурекубеаррай:: Sample (S, float, float, uint)</span><span class="sxs-lookup"><span data-stu-id="41fc9-105">TextureCubeArray::Sample(S,float,float,uint) function</span></span>

<span data-ttu-id="41fc9-106">Выбирает текстуру с необязательным значением для фиксации в качестве примера значений уровня детализации (Лод) и возвращает состояние операции.</span><span class="sxs-lookup"><span data-stu-id="41fc9-106">Samples a texture with an optional value to clamp sample level-of-detail (LOD) values to, and returns status of the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="41fc9-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="41fc9-107">Syntax</span></span>


``` syntax
DXGI_FORMAT Sample(
  in  SamplerState S,
  in  float        Location,
  in  float        Clamp,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="41fc9-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="41fc9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41fc9-109">*S* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="41fc9-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41fc9-110">[Состояние образца](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="41fc9-110">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="41fc9-111">Это объект, объявленный в файле эффектов, который содержит назначения состояний.</span><span class="sxs-lookup"><span data-stu-id="41fc9-111">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="41fc9-112">*Расположение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="41fc9-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41fc9-113">Координаты текстуры.</span><span class="sxs-lookup"><span data-stu-id="41fc9-113">The texture coordinates.</span></span> <span data-ttu-id="41fc9-114">Тип аргумента зависит от типа объекта текстуры.</span><span class="sxs-lookup"><span data-stu-id="41fc9-114">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="41fc9-115">Тип Texture-Object</span><span class="sxs-lookup"><span data-stu-id="41fc9-115">Texture-Object Type</span></span>                    | <span data-ttu-id="41fc9-116">Тип параметра</span><span class="sxs-lookup"><span data-stu-id="41fc9-116">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="41fc9-117">Texture1D</span><span class="sxs-lookup"><span data-stu-id="41fc9-117">Texture1D</span></span>                              | <span data-ttu-id="41fc9-118">FLOAT</span><span class="sxs-lookup"><span data-stu-id="41fc9-118">float</span></span>          |
| <span data-ttu-id="41fc9-119">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="41fc9-119">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="41fc9-120">float2</span><span class="sxs-lookup"><span data-stu-id="41fc9-120">float2</span></span>         |
| <span data-ttu-id="41fc9-121">Texture2DArray, Texture3D, Текстурекубе</span><span class="sxs-lookup"><span data-stu-id="41fc9-121">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="41fc9-122">float3</span><span class="sxs-lookup"><span data-stu-id="41fc9-122">float3</span></span>         |
| <span data-ttu-id="41fc9-123">текстурекубеаррай</span><span class="sxs-lookup"><span data-stu-id="41fc9-123">TextureCubeArray</span></span>                       | <span data-ttu-id="41fc9-124">float4</span><span class="sxs-lookup"><span data-stu-id="41fc9-124">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="41fc9-125">*Срез* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="41fc9-125">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41fc9-126">Необязательное значение для примера среза Лод значений.</span><span class="sxs-lookup"><span data-stu-id="41fc9-126">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="41fc9-127">Например, если передать значение среза 2.0 f, вы убедитесь, что ни один из отдельных примеров не имеет доступа к MIP уровню менее 2.0.</span><span class="sxs-lookup"><span data-stu-id="41fc9-127">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> <dt>

<span data-ttu-id="41fc9-128">*Состояние* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="41fc9-128">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="41fc9-129">Состояние операции.</span><span class="sxs-lookup"><span data-stu-id="41fc9-129">The status of the operation.</span></span> <span data-ttu-id="41fc9-130">Вы не можете получить доступ к состоянию напрямую; Вместо этого передайте состояние в подставляемую функцию [**чеккакцессфуллимаппед**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="41fc9-130">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="41fc9-131">**Чеккакцессфуллимаппед** возвращает **значение true** , если все значения из соответствующего **образца**, **сбора** или операции **загрузки** обращались к сопоставленным плиткам в [мозаичном ресурсе](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="41fc9-131">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="41fc9-132">Если какие бы то ни было значения были взяты из несопоставленной плитки, **чеккакцессфуллимаппед** возвращает **значение false**.</span><span class="sxs-lookup"><span data-stu-id="41fc9-132">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41fc9-133">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="41fc9-133">Return value</span></span>

<span data-ttu-id="41fc9-134">Формат текстуры, который является одним из типизированных значений, перечисленных в [**\_ формате DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="41fc9-134">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="41fc9-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="41fc9-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41fc9-136">Примеры методов</span><span class="sxs-lookup"><span data-stu-id="41fc9-136">Sample methods</span></span>](texturecubearray-sample.md)
</dt> <dt>

[<span data-ttu-id="41fc9-137">**текстурекубеаррай**</span><span class="sxs-lookup"><span data-stu-id="41fc9-137">**TextureCubeArray**</span></span>](texturecubearray.md)
</dt> </dl>

 

 
