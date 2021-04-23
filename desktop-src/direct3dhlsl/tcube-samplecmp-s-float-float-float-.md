---
title: 'Функция Самплекмп:: Самплекмп (S, float, float, float) для Текстурекубе'
description: 'Выбор текстуры с использованием значения сравнения для отклонения выборок с необязательным значением для фиксации значений уровня детализации (Лод) в. | Функция Самплекмп:: Самплекмп (S, float, float, float) для Текстурекубе'
ms.assetid: FCCF12CF-3F0A-4468-9FC4-27CAAF0BEEE3
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
ms.openlocfilehash: e8a326101df26ab7f4925c9c6cce3673385309fd
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/16/2021
ms.locfileid: "104987335"
---
# <a name="samplecmpsamplecmpsfloatfloatfloat-function-for-texturecube"></a><span data-ttu-id="dc927-105">Функция Самплекмп:: Самплекмп (S, float, float, float) для Текстурекубе</span><span class="sxs-lookup"><span data-stu-id="dc927-105">SampleCmp::SampleCmp(S,float,float,float) function for TextureCube</span></span>

<span data-ttu-id="dc927-106">Выбор текстуры с использованием значения сравнения для отклонения выборок с необязательным значением для фиксации значений уровня детализации (Лод) в.</span><span class="sxs-lookup"><span data-stu-id="dc927-106">Samples a texture, using a comparison value to reject samples, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc927-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dc927-107">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleCmp(
  in SamplerState S,
  in float        Location,
  in float        CompareValue,
  in float        Clamp
);
```



## <a name="parameters"></a><span data-ttu-id="dc927-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="dc927-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc927-109">*S* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="dc927-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc927-110">Тип: **самплерстате**</span><span class="sxs-lookup"><span data-stu-id="dc927-110">Type: **SamplerState**</span></span>

<span data-ttu-id="dc927-111">[Состояние образца](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="dc927-111">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="dc927-112">Это объект, объявленный в файле эффектов, который содержит назначения состояний.</span><span class="sxs-lookup"><span data-stu-id="dc927-112">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="dc927-113">*Расположение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="dc927-113">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc927-114">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="dc927-114">Type: **float**</span></span>

<span data-ttu-id="dc927-115">Координаты текстуры.</span><span class="sxs-lookup"><span data-stu-id="dc927-115">The texture coordinates.</span></span> <span data-ttu-id="dc927-116">Тип аргумента зависит от типа объекта текстуры.</span><span class="sxs-lookup"><span data-stu-id="dc927-116">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="dc927-117">Тип Texture-Object</span><span class="sxs-lookup"><span data-stu-id="dc927-117">Texture-Object Type</span></span>                    | <span data-ttu-id="dc927-118">Тип параметра</span><span class="sxs-lookup"><span data-stu-id="dc927-118">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="dc927-119">Texture1D</span><span class="sxs-lookup"><span data-stu-id="dc927-119">Texture1D</span></span>                              | <span data-ttu-id="dc927-120">FLOAT</span><span class="sxs-lookup"><span data-stu-id="dc927-120">float</span></span>          |
| <span data-ttu-id="dc927-121">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="dc927-121">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="dc927-122">float2</span><span class="sxs-lookup"><span data-stu-id="dc927-122">float2</span></span>         |
| <span data-ttu-id="dc927-123">Texture2DArray, Texture3D, Текстурекубе</span><span class="sxs-lookup"><span data-stu-id="dc927-123">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="dc927-124">float3</span><span class="sxs-lookup"><span data-stu-id="dc927-124">float3</span></span>         |
| <span data-ttu-id="dc927-125">текстурекубеаррай</span><span class="sxs-lookup"><span data-stu-id="dc927-125">TextureCubeArray</span></span>                       | <span data-ttu-id="dc927-126">float4</span><span class="sxs-lookup"><span data-stu-id="dc927-126">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="dc927-127">*Компаревалуе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="dc927-127">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc927-128">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="dc927-128">Type: **float**</span></span>

<span data-ttu-id="dc927-129">Значение с плавающей запятой, используемое в качестве значения сравнения.</span><span class="sxs-lookup"><span data-stu-id="dc927-129">A floating-point value to use as a comparison value.</span></span>

</dd> <dt>

<span data-ttu-id="dc927-130">*Срез* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="dc927-130">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc927-131">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="dc927-131">Type: **float**</span></span>

<span data-ttu-id="dc927-132">Необязательное значение для примера среза Лод значений.</span><span class="sxs-lookup"><span data-stu-id="dc927-132">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="dc927-133">Например, если передать значение среза 2.0 f, вы убедитесь, что ни один из отдельных примеров не имеет доступа к MIP уровню менее 2.0.</span><span class="sxs-lookup"><span data-stu-id="dc927-133">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dc927-134">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dc927-134">Return value</span></span>

<span data-ttu-id="dc927-135">Тип: **[ **\_ Формат DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="dc927-135">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="dc927-136">Формат текстуры, который является одним из типизированных значений, перечисленных в [**\_ формате DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="dc927-136">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="dc927-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dc927-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc927-138">Методы Самплекмп</span><span class="sxs-lookup"><span data-stu-id="dc927-138">SampleCmp methods</span></span>](texturecube-samplecmp.md)
</dt> <dt>

[<span data-ttu-id="dc927-139">**текстурекубе**</span><span class="sxs-lookup"><span data-stu-id="dc927-139">**TextureCube**</span></span>](texturecube.md)
</dt> </dl>

 

 
