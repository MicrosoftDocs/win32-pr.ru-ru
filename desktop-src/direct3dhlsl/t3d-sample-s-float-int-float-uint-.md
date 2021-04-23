---
title: 'Функция Texture3D:: Sample (S, float, int, float, uint)'
description: 'Выбирает текстуру с необязательным значением для фиксации в качестве примера значений уровня детализации (Лод) и возвращает состояние операции. | Функция Texture3D:: Sample (S, float, int, float, uint)'
ms.assetid: DB8401A1-1065-4616-BDDE-9ADB59B09C8B
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
ms.openlocfilehash: 1f1704a30ba689d50bc9c551ac6a43a4a38f90a9
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104998038"
---
# <a name="texture3dsamplesfloatintfloatuint-function"></a><span data-ttu-id="e9d66-105">Функция Texture3D:: Sample (S, float, int, float, uint)</span><span class="sxs-lookup"><span data-stu-id="e9d66-105">Texture3D::Sample(S,float,int,float,uint) function</span></span>

<span data-ttu-id="e9d66-106">Выбирает текстуру с необязательным значением для фиксации в качестве примера значений уровня детализации (Лод) и возвращает состояние операции.</span><span class="sxs-lookup"><span data-stu-id="e9d66-106">Samples a texture with an optional value to clamp sample level-of-detail (LOD) values to, and returns status of the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9d66-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e9d66-107">Syntax</span></span>


``` syntax
DXGI_FORMAT Sample(
  in  SamplerState S,
  in  float        Location,
  in  int          Offset,
  in  float        Clamp,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="e9d66-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="e9d66-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9d66-109">*S* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="e9d66-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9d66-110">[Состояние образца](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="e9d66-110">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="e9d66-111">Это объект, объявленный в файле эффектов, который содержит назначения состояний.</span><span class="sxs-lookup"><span data-stu-id="e9d66-111">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="e9d66-112">*Расположение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e9d66-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9d66-113">Координаты текстуры.</span><span class="sxs-lookup"><span data-stu-id="e9d66-113">The texture coordinates.</span></span> <span data-ttu-id="e9d66-114">Тип аргумента зависит от типа объекта текстуры.</span><span class="sxs-lookup"><span data-stu-id="e9d66-114">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="e9d66-115">Тип Texture-Object</span><span class="sxs-lookup"><span data-stu-id="e9d66-115">Texture-Object Type</span></span>                    | <span data-ttu-id="e9d66-116">Тип параметра</span><span class="sxs-lookup"><span data-stu-id="e9d66-116">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="e9d66-117">Texture1D</span><span class="sxs-lookup"><span data-stu-id="e9d66-117">Texture1D</span></span>                              | <span data-ttu-id="e9d66-118">FLOAT</span><span class="sxs-lookup"><span data-stu-id="e9d66-118">float</span></span>          |
| <span data-ttu-id="e9d66-119">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="e9d66-119">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="e9d66-120">float2</span><span class="sxs-lookup"><span data-stu-id="e9d66-120">float2</span></span>         |
| <span data-ttu-id="e9d66-121">Texture2DArray, Texture3D, Текстурекубе</span><span class="sxs-lookup"><span data-stu-id="e9d66-121">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="e9d66-122">float3</span><span class="sxs-lookup"><span data-stu-id="e9d66-122">float3</span></span>         |
| <span data-ttu-id="e9d66-123">текстурекубеаррай</span><span class="sxs-lookup"><span data-stu-id="e9d66-123">TextureCubeArray</span></span>                       | <span data-ttu-id="e9d66-124">float4</span><span class="sxs-lookup"><span data-stu-id="e9d66-124">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="e9d66-125">*Смещение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e9d66-125">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9d66-126">Необязательное Смещение координаты текстуры, которое может использоваться для любого типа объекта текстуры. смещение применяется к расположению перед выборкой.</span><span class="sxs-lookup"><span data-stu-id="e9d66-126">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="e9d66-127">Используйте смещение только с целочисленным миплевел; в противном случае можно получить результаты, которые не могут быть правильно преобразованы в оборудование.</span><span class="sxs-lookup"><span data-stu-id="e9d66-127">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="e9d66-128">Тип аргумента зависит от типа объекта текстуры.</span><span class="sxs-lookup"><span data-stu-id="e9d66-128">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="e9d66-129">Дополнительные сведения см. в разделе [применение целочисленных смещений](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="e9d66-129">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="e9d66-130">Тип Texture-Object</span><span class="sxs-lookup"><span data-stu-id="e9d66-130">Texture-Object Type</span></span>           | <span data-ttu-id="e9d66-131">Тип параметра</span><span class="sxs-lookup"><span data-stu-id="e9d66-131">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="e9d66-132">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="e9d66-132">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="e9d66-133">INT</span><span class="sxs-lookup"><span data-stu-id="e9d66-133">int</span></span>            |
| <span data-ttu-id="e9d66-134">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="e9d66-134">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="e9d66-135">int2</span><span class="sxs-lookup"><span data-stu-id="e9d66-135">int2</span></span>           |
| <span data-ttu-id="e9d66-136">Texture3D</span><span class="sxs-lookup"><span data-stu-id="e9d66-136">Texture3D</span></span>                     | <span data-ttu-id="e9d66-137">int3</span><span class="sxs-lookup"><span data-stu-id="e9d66-137">int3</span></span>           |
| <span data-ttu-id="e9d66-138">Текстурекубе, Текстурекубеаррай</span><span class="sxs-lookup"><span data-stu-id="e9d66-138">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="e9d66-139">не поддерживается</span><span class="sxs-lookup"><span data-stu-id="e9d66-139">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="e9d66-140">*Срез* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e9d66-140">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9d66-141">Необязательное значение для примера среза Лод значений.</span><span class="sxs-lookup"><span data-stu-id="e9d66-141">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="e9d66-142">Например, если передать значение среза 2.0 f, вы убедитесь, что ни один из отдельных примеров не имеет доступа к MIP уровню менее 2.0.</span><span class="sxs-lookup"><span data-stu-id="e9d66-142">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> <dt>

<span data-ttu-id="e9d66-143">*Состояние* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e9d66-143">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e9d66-144">Состояние операции.</span><span class="sxs-lookup"><span data-stu-id="e9d66-144">The status of the operation.</span></span> <span data-ttu-id="e9d66-145">Вы не можете получить доступ к состоянию напрямую; Вместо этого передайте состояние в подставляемую функцию [**чеккакцессфуллимаппед**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="e9d66-145">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="e9d66-146">**Чеккакцессфуллимаппед** возвращает **значение true** , если все значения из соответствующего **образца**, **сбора** или операции **загрузки** обращались к сопоставленным плиткам в [мозаичном ресурсе](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="e9d66-146">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="e9d66-147">Если какие бы то ни было значения были взяты из несопоставленной плитки, **чеккакцессфуллимаппед** возвращает **значение false**.</span><span class="sxs-lookup"><span data-stu-id="e9d66-147">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9d66-148">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e9d66-148">Return value</span></span>

<span data-ttu-id="e9d66-149">Формат текстуры, который является одним из типизированных значений, перечисленных в [**\_ формате DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="e9d66-149">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="e9d66-150">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e9d66-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9d66-151">Примеры методов</span><span class="sxs-lookup"><span data-stu-id="e9d66-151">Sample methods</span></span>](texture3d-sample.md)
</dt> <dt>

[<span data-ttu-id="e9d66-152">**Texture3D**</span><span class="sxs-lookup"><span data-stu-id="e9d66-152">**Texture3D**</span></span>](sm5-object-texture3d.md)
</dt> </dl>

 

 
