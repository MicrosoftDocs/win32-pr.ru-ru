---
title: 'Функция Самплекмплевелзеро:: Самплекмплевелзеро (S, float, float, uint) для Текстурекубе'
description: Производит выборку текстуры только на уровне mipmap 0 и сравнивает результат со значением сравнения. Возвращает состояние операции. Для Текстурекубе.
ms.assetid: FE40307D-B9BE-434F-A6EF-7CA3C5BC7D70
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
ms.openlocfilehash: ff58c51919e575260c71f7b58d8f3d0fda6c1dd1
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/16/2021
ms.locfileid: "104987317"
---
# <a name="samplecmplevelzerosamplecmplevelzerosfloatfloatuint-function-for-texturecube"></a><span data-ttu-id="2b9d2-106">Функция Самплекмплевелзеро:: Самплекмплевелзеро (S, float, float, uint) для Текстурекубе</span><span class="sxs-lookup"><span data-stu-id="2b9d2-106">SampleCmpLevelZero::SampleCmpLevelZero(S,float,float,uint) function for TextureCube</span></span>

<span data-ttu-id="2b9d2-107">Производит выборку текстуры только на уровне mipmap 0 и сравнивает результат со значением сравнения.</span><span class="sxs-lookup"><span data-stu-id="2b9d2-107">Samples a texture on mipmap level 0 only and compares the result to a comparison value.</span></span> <span data-ttu-id="2b9d2-108">Возвращает состояние операции.</span><span class="sxs-lookup"><span data-stu-id="2b9d2-108">Returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b9d2-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2b9d2-109">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleCmpLevelZero(
  in  SamplerState S,
  in  float        Location,
  in  float        CompareValue,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="2b9d2-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="2b9d2-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b9d2-111">*S* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="2b9d2-111">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b9d2-112">Тип: **самплерстате**</span><span class="sxs-lookup"><span data-stu-id="2b9d2-112">Type: **SamplerState**</span></span>

<span data-ttu-id="2b9d2-113">[Состояние образца](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="2b9d2-113">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="2b9d2-114">Это объект, объявленный в файле эффектов, который содержит назначения состояний.</span><span class="sxs-lookup"><span data-stu-id="2b9d2-114">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="2b9d2-115">*Расположение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2b9d2-115">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b9d2-116">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="2b9d2-116">Type: **float**</span></span>

<span data-ttu-id="2b9d2-117">Координаты текстуры.</span><span class="sxs-lookup"><span data-stu-id="2b9d2-117">The texture coordinates.</span></span> <span data-ttu-id="2b9d2-118">Тип аргумента зависит от типа объекта текстуры.</span><span class="sxs-lookup"><span data-stu-id="2b9d2-118">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="2b9d2-119">Тип Texture-Object</span><span class="sxs-lookup"><span data-stu-id="2b9d2-119">Texture-Object Type</span></span>                    | <span data-ttu-id="2b9d2-120">Тип параметра</span><span class="sxs-lookup"><span data-stu-id="2b9d2-120">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="2b9d2-121">Texture1D</span><span class="sxs-lookup"><span data-stu-id="2b9d2-121">Texture1D</span></span>                              | <span data-ttu-id="2b9d2-122">FLOAT</span><span class="sxs-lookup"><span data-stu-id="2b9d2-122">float</span></span>          |
| <span data-ttu-id="2b9d2-123">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="2b9d2-123">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="2b9d2-124">float2</span><span class="sxs-lookup"><span data-stu-id="2b9d2-124">float2</span></span>         |
| <span data-ttu-id="2b9d2-125">Texture2DArray, Texture3D, Текстурекубе</span><span class="sxs-lookup"><span data-stu-id="2b9d2-125">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="2b9d2-126">float3</span><span class="sxs-lookup"><span data-stu-id="2b9d2-126">float3</span></span>         |
| <span data-ttu-id="2b9d2-127">текстурекубеаррай</span><span class="sxs-lookup"><span data-stu-id="2b9d2-127">TextureCubeArray</span></span>                       | <span data-ttu-id="2b9d2-128">float4</span><span class="sxs-lookup"><span data-stu-id="2b9d2-128">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="2b9d2-129">*Компаревалуе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2b9d2-129">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b9d2-130">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="2b9d2-130">Type: **float**</span></span>

<span data-ttu-id="2b9d2-131">Значение с плавающей запятой, используемое в качестве значения сравнения.</span><span class="sxs-lookup"><span data-stu-id="2b9d2-131">A floating-point value to use as a comparison value.</span></span>

</dd> <dt>

<span data-ttu-id="2b9d2-132">*Состояние* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="2b9d2-132">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2b9d2-133">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="2b9d2-133">Type: **uint**</span></span>

<span data-ttu-id="2b9d2-134">Состояние операции.</span><span class="sxs-lookup"><span data-stu-id="2b9d2-134">The status of the operation.</span></span> <span data-ttu-id="2b9d2-135">Вы не можете получить доступ к состоянию напрямую; Вместо этого передайте состояние в подставляемую функцию [**чеккакцессфуллимаппед**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="2b9d2-135">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="2b9d2-136">**Чеккакцессфуллимаппед** возвращает **значение true** , если все значения из соответствующего **образца**, **сбора** или операции **загрузки** обращались к сопоставленным плиткам в [мозаичном ресурсе](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="2b9d2-136">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="2b9d2-137">Если какие бы то ни было значения были взяты из несопоставленной плитки, **чеккакцессфуллимаппед** возвращает **значение false**.</span><span class="sxs-lookup"><span data-stu-id="2b9d2-137">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2b9d2-138">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2b9d2-138">Return value</span></span>

<span data-ttu-id="2b9d2-139">Тип: **[ **\_ Формат DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="2b9d2-139">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="2b9d2-140">Формат текстуры, который является одним из типизированных значений, перечисленных в [**\_ формате DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="2b9d2-140">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="2b9d2-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2b9d2-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b9d2-142">Методы Самплекмплевелзеро</span><span class="sxs-lookup"><span data-stu-id="2b9d2-142">SampleCmpLevelZero methods</span></span>](texturecube-samplecmplevelzero.md)
</dt> <dt>

[<span data-ttu-id="2b9d2-143">**текстурекубе**</span><span class="sxs-lookup"><span data-stu-id="2b9d2-143">**TextureCube**</span></span>](texturecube.md)
</dt> </dl>

 

 
