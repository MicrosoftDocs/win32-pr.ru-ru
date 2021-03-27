---
title: 'Функция Самплекмплевелзеро:: Самплекмплевелзеро (S, float, float, uint) для Текстурекубеаррай'
description: Производит выборку текстуры только на уровне mipmap 0 и сравнивает результат со значением сравнения, а затем возвращает состояние операции. Для Текстурекубеаррай.
ms.assetid: D73447C6-E77C-4027-B265-24F96C679357
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
ms.openlocfilehash: ac042bd2856aa69bbba1293fb91ff74d95c0de53
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/16/2021
ms.locfileid: "103821556"
---
# <a name="samplecmplevelzerosamplecmplevelzerosfloatfloatuint-function-for-texturecubearray"></a><span data-ttu-id="2526f-105">Функция Самплекмплевелзеро:: Самплекмплевелзеро (S, float, float, uint) для Текстурекубеаррай</span><span class="sxs-lookup"><span data-stu-id="2526f-105">SampleCmpLevelZero::SampleCmpLevelZero(S,float,float,uint) function for TextureCubeArray</span></span>

<span data-ttu-id="2526f-106">Производит выборку текстуры только на уровне mipmap 0 и сравнивает результат со значением сравнения.</span><span class="sxs-lookup"><span data-stu-id="2526f-106">Samples a texture on mipmap level 0 only and compares the result to a comparison value.</span></span> <span data-ttu-id="2526f-107">Возвращает состояние операции.</span><span class="sxs-lookup"><span data-stu-id="2526f-107">Returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="2526f-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2526f-108">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleCmpLevelZero(
  in  SamplerState S,
  in  float        Location,
  in  float        CompareValue,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="2526f-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="2526f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2526f-110">*S* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="2526f-110">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2526f-111">Тип: **самплерстате**</span><span class="sxs-lookup"><span data-stu-id="2526f-111">Type: **SamplerState**</span></span>

<span data-ttu-id="2526f-112">[Состояние образца](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="2526f-112">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="2526f-113">Это объект, объявленный в файле эффектов, который содержит назначения состояний.</span><span class="sxs-lookup"><span data-stu-id="2526f-113">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="2526f-114">*Расположение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2526f-114">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2526f-115">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="2526f-115">Type: **float**</span></span>

<span data-ttu-id="2526f-116">Координаты текстуры.</span><span class="sxs-lookup"><span data-stu-id="2526f-116">The texture coordinates.</span></span> <span data-ttu-id="2526f-117">Тип аргумента зависит от типа объекта текстуры.</span><span class="sxs-lookup"><span data-stu-id="2526f-117">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="2526f-118">Тип Texture-Object</span><span class="sxs-lookup"><span data-stu-id="2526f-118">Texture-Object Type</span></span>                    | <span data-ttu-id="2526f-119">Тип параметра</span><span class="sxs-lookup"><span data-stu-id="2526f-119">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="2526f-120">Texture1D</span><span class="sxs-lookup"><span data-stu-id="2526f-120">Texture1D</span></span>                              | <span data-ttu-id="2526f-121">FLOAT</span><span class="sxs-lookup"><span data-stu-id="2526f-121">float</span></span>          |
| <span data-ttu-id="2526f-122">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="2526f-122">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="2526f-123">float2</span><span class="sxs-lookup"><span data-stu-id="2526f-123">float2</span></span>         |
| <span data-ttu-id="2526f-124">Texture2DArray, Texture3D, Текстурекубе</span><span class="sxs-lookup"><span data-stu-id="2526f-124">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="2526f-125">float3</span><span class="sxs-lookup"><span data-stu-id="2526f-125">float3</span></span>         |
| <span data-ttu-id="2526f-126">текстурекубеаррай</span><span class="sxs-lookup"><span data-stu-id="2526f-126">TextureCubeArray</span></span>                       | <span data-ttu-id="2526f-127">float4</span><span class="sxs-lookup"><span data-stu-id="2526f-127">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="2526f-128">*Компаревалуе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2526f-128">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2526f-129">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="2526f-129">Type: **float**</span></span>

<span data-ttu-id="2526f-130">Значение с плавающей запятой, используемое в качестве значения сравнения.</span><span class="sxs-lookup"><span data-stu-id="2526f-130">A floating-point value to use as a comparison value.</span></span>

</dd> <dt>

<span data-ttu-id="2526f-131">*Состояние* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="2526f-131">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2526f-132">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="2526f-132">Type: **uint**</span></span>

<span data-ttu-id="2526f-133">Состояние операции.</span><span class="sxs-lookup"><span data-stu-id="2526f-133">The status of the operation.</span></span> <span data-ttu-id="2526f-134">Вы не можете получить доступ к состоянию напрямую; Вместо этого передайте состояние в подставляемую функцию [**чеккакцессфуллимаппед**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="2526f-134">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="2526f-135">**Чеккакцессфуллимаппед** возвращает **значение true** , если все значения из соответствующего **образца**, **сбора** или операции **загрузки** обращались к сопоставленным плиткам в [мозаичном ресурсе](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="2526f-135">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="2526f-136">Если какие бы то ни было значения были взяты из несопоставленной плитки, **чеккакцессфуллимаппед** возвращает **значение false**.</span><span class="sxs-lookup"><span data-stu-id="2526f-136">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2526f-137">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2526f-137">Return value</span></span>

<span data-ttu-id="2526f-138">Тип: **[ **\_ Формат DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="2526f-138">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="2526f-139">Формат текстуры, который является одним из типизированных значений, перечисленных в [**\_ формате DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="2526f-139">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="2526f-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2526f-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2526f-141">Методы Самплекмплевелзеро</span><span class="sxs-lookup"><span data-stu-id="2526f-141">SampleCmpLevelZero methods</span></span>](texturecubearray-samplecmplevelzero.md)
</dt> <dt>

[<span data-ttu-id="2526f-142">**текстурекубеаррай**</span><span class="sxs-lookup"><span data-stu-id="2526f-142">**TextureCubeArray**</span></span>](texturecubearray.md)
</dt> </dl>

 

 
