---
title: 'Функция Самплекмп:: Самплекмп (S, float, float, float, uint) для Текстурекубе'
description: 'Эта функция выбирает текстуру, используя значение сравнения для отклонения выборок, с необязательным значением для фиксации образцов значений уровня детализации (Лод) до. | Функция Самплекмп:: Самплекмп (S, float, float, float, uint) для Текстурекубе'
ms.assetid: 050E2856-1E93-4C69-8213-EEC082E82D40
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
ms.openlocfilehash: b73bf86b0c24feae87ea0bb4150d313fff604002
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/16/2021
ms.locfileid: "104987284"
---
# <a name="samplecmpsamplecmpsfloatfloatfloatuint-function-for-texturecube"></a><span data-ttu-id="fe10f-105">Функция Самплекмп:: Самплекмп (S, float, float, float, uint) для Текстурекубе</span><span class="sxs-lookup"><span data-stu-id="fe10f-105">SampleCmp::SampleCmp(S,float,float,float,uint) function for TextureCube</span></span>

<span data-ttu-id="fe10f-106">Выбор текстуры с использованием значения сравнения для отклонения выборок с необязательным значением для фиксации значений уровня детализации (Лод) в.</span><span class="sxs-lookup"><span data-stu-id="fe10f-106">Samples a texture, using a comparison value to reject samples, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span> <span data-ttu-id="fe10f-107">Возвращает состояние операции.</span><span class="sxs-lookup"><span data-stu-id="fe10f-107">Returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe10f-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fe10f-108">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleCmp(
  in  SamplerState S,
  in  float        Location,
  in  float        CompareValue,
  in  float        Clamp,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="fe10f-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="fe10f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe10f-110">*S* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="fe10f-110">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe10f-111">Тип: **самплерстате**</span><span class="sxs-lookup"><span data-stu-id="fe10f-111">Type: **SamplerState**</span></span>

<span data-ttu-id="fe10f-112">[Состояние образца](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="fe10f-112">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="fe10f-113">Это объект, объявленный в файле эффектов, который содержит назначения состояний.</span><span class="sxs-lookup"><span data-stu-id="fe10f-113">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="fe10f-114">*Расположение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fe10f-114">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe10f-115">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="fe10f-115">Type: **float**</span></span>

<span data-ttu-id="fe10f-116">Координаты текстуры.</span><span class="sxs-lookup"><span data-stu-id="fe10f-116">The texture coordinates.</span></span> <span data-ttu-id="fe10f-117">Тип аргумента зависит от типа объекта текстуры.</span><span class="sxs-lookup"><span data-stu-id="fe10f-117">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="fe10f-118">Тип Texture-Object</span><span class="sxs-lookup"><span data-stu-id="fe10f-118">Texture-Object Type</span></span>                    | <span data-ttu-id="fe10f-119">Тип параметра</span><span class="sxs-lookup"><span data-stu-id="fe10f-119">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="fe10f-120">Texture1D</span><span class="sxs-lookup"><span data-stu-id="fe10f-120">Texture1D</span></span>                              | <span data-ttu-id="fe10f-121">FLOAT</span><span class="sxs-lookup"><span data-stu-id="fe10f-121">float</span></span>          |
| <span data-ttu-id="fe10f-122">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="fe10f-122">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="fe10f-123">float2</span><span class="sxs-lookup"><span data-stu-id="fe10f-123">float2</span></span>         |
| <span data-ttu-id="fe10f-124">Texture2DArray, Texture3D, Текстурекубе</span><span class="sxs-lookup"><span data-stu-id="fe10f-124">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="fe10f-125">float3</span><span class="sxs-lookup"><span data-stu-id="fe10f-125">float3</span></span>         |
| <span data-ttu-id="fe10f-126">текстурекубеаррай</span><span class="sxs-lookup"><span data-stu-id="fe10f-126">TextureCubeArray</span></span>                       | <span data-ttu-id="fe10f-127">float4</span><span class="sxs-lookup"><span data-stu-id="fe10f-127">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="fe10f-128">*Компаревалуе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fe10f-128">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe10f-129">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="fe10f-129">Type: **float**</span></span>

<span data-ttu-id="fe10f-130">Значение с плавающей запятой, используемое в качестве значения сравнения.</span><span class="sxs-lookup"><span data-stu-id="fe10f-130">A floating-point value to use as a comparison value.</span></span>

</dd> <dt>

<span data-ttu-id="fe10f-131">*Срез* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fe10f-131">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe10f-132">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="fe10f-132">Type: **float**</span></span>

<span data-ttu-id="fe10f-133">Необязательное значение для примера среза Лод значений.</span><span class="sxs-lookup"><span data-stu-id="fe10f-133">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="fe10f-134">Например, если передать значение среза 2.0 f, вы убедитесь, что ни один из отдельных примеров не имеет доступа к MIP уровню менее 2.0.</span><span class="sxs-lookup"><span data-stu-id="fe10f-134">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> <dt>

<span data-ttu-id="fe10f-135">*Состояние* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="fe10f-135">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fe10f-136">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="fe10f-136">Type: **uint**</span></span>

<span data-ttu-id="fe10f-137">Состояние операции.</span><span class="sxs-lookup"><span data-stu-id="fe10f-137">The status of the operation.</span></span> <span data-ttu-id="fe10f-138">Вы не можете получить доступ к состоянию напрямую; Вместо этого передайте состояние в подставляемую функцию [**чеккакцессфуллимаппед**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="fe10f-138">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="fe10f-139">**Чеккакцессфуллимаппед** возвращает **значение true** , если все значения из соответствующего **образца**, **сбора** или операции **загрузки** обращались к сопоставленным плиткам в [мозаичном ресурсе](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="fe10f-139">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="fe10f-140">Если какие бы то ни было значения были взяты из несопоставленной плитки, **чеккакцессфуллимаппед** возвращает **значение false**.</span><span class="sxs-lookup"><span data-stu-id="fe10f-140">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe10f-141">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fe10f-141">Return value</span></span>

<span data-ttu-id="fe10f-142">Тип: **[ **\_ Формат DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="fe10f-142">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="fe10f-143">Формат текстуры, который является одним из типизированных значений, перечисленных в [**\_ формате DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="fe10f-143">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="fe10f-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fe10f-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe10f-145">Методы Самплекмп</span><span class="sxs-lookup"><span data-stu-id="fe10f-145">SampleCmp methods</span></span>](texturecube-samplecmp.md)
</dt> <dt>

[<span data-ttu-id="fe10f-146">**текстурекубе**</span><span class="sxs-lookup"><span data-stu-id="fe10f-146">**TextureCube**</span></span>](texturecube.md)
</dt> </dl>

 

 
