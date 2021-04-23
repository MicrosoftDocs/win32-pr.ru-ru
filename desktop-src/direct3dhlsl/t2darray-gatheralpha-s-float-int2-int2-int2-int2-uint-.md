---
title: 'Функция Texture2DArray:: Гасералфа (S, float, int2, int2, int2, int2, uint)'
description: 'Возвращает альфа-компоненты четырех значений шаг текселя, которые будут использоваться в операции линейной фильтрации, а также состояние сопоставления плиток. | Функция Texture2DArray:: Гасералфа (S, float, int2, int2, int2, int2, uint)'
ms.assetid: 1B069708-FC77-4FD0-A264-3AB170F48D58
keywords:
- Функция Гасералфа HLSL
topic_type:
- apiref
api_name:
- GatherAlpha
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bb9a9911c242a678d9de5aea0d9ec7508ceb8775
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104273559"
---
# <a name="texture2darraygatheralphasfloatint2int2int2int2uint-function"></a><span data-ttu-id="86e14-105">Функция Texture2DArray:: Гасералфа (S, float, int2, int2, int2, int2, uint)</span><span class="sxs-lookup"><span data-stu-id="86e14-105">Texture2DArray::GatherAlpha(S,float,int2,int2,int2,int2,uint) function</span></span>

<span data-ttu-id="86e14-106">Возвращает альфа-компоненты четырех значений шаг текселя, которые будут использоваться в операции линейной фильтрации, а также состояние сопоставления плиток.</span><span class="sxs-lookup"><span data-stu-id="86e14-106">Returns the alpha components of the four texel values that would be used in a bi-linear filtering operation, along with tile-mapping status.</span></span>

## <a name="syntax"></a><span data-ttu-id="86e14-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="86e14-107">Syntax</span></span>


``` syntax
TemplateType GatherAlpha(
  in  SamplerState S,
  in  float        Location,
  in  int2         Offset1,
  in  int2         Offset2,
  in  int2         Offset3,
  in  int2         Offset4,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="86e14-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="86e14-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86e14-109">*S* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="86e14-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86e14-110">Тип: **самплерстате**</span><span class="sxs-lookup"><span data-stu-id="86e14-110">Type: **SamplerState**</span></span>

<span data-ttu-id="86e14-111">Индекс выборки с отсчетом от нуля.</span><span class="sxs-lookup"><span data-stu-id="86e14-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="86e14-112">*Расположение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="86e14-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86e14-113">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="86e14-113">Type: **float**</span></span>

<span data-ttu-id="86e14-114">Образцы координат (u, v).</span><span class="sxs-lookup"><span data-stu-id="86e14-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="86e14-115">*Offset1* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="86e14-115">*Offset1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86e14-116">Тип: **int2**</span><span class="sxs-lookup"><span data-stu-id="86e14-116">Type: **int2**</span></span>

<span data-ttu-id="86e14-117">Первый компонент смещения, применяемый к координатам текстуры перед выборкой.</span><span class="sxs-lookup"><span data-stu-id="86e14-117">The first offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="86e14-118">*Offset2* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="86e14-118">*Offset2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86e14-119">Тип: **int2**</span><span class="sxs-lookup"><span data-stu-id="86e14-119">Type: **int2**</span></span>

<span data-ttu-id="86e14-120">Второй компонент смещения, применяемый к координатам текстуры перед выборкой.</span><span class="sxs-lookup"><span data-stu-id="86e14-120">The second offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="86e14-121">*Offset3* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="86e14-121">*Offset3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86e14-122">Тип: **int2**</span><span class="sxs-lookup"><span data-stu-id="86e14-122">Type: **int2**</span></span>

<span data-ttu-id="86e14-123">Третий компонент смещения, применяемый к координатам текстуры перед выборкой.</span><span class="sxs-lookup"><span data-stu-id="86e14-123">The third offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="86e14-124">*Offset4* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="86e14-124">*Offset4* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86e14-125">Тип: **int2**</span><span class="sxs-lookup"><span data-stu-id="86e14-125">Type: **int2**</span></span>

<span data-ttu-id="86e14-126">Четвертый компонент смещения, применяемый к координатам текстуры перед выборкой.</span><span class="sxs-lookup"><span data-stu-id="86e14-126">The fourth offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="86e14-127">*Состояние* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="86e14-127">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="86e14-128">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="86e14-128">Type: **uint**</span></span>

<span data-ttu-id="86e14-129">Состояние операции.</span><span class="sxs-lookup"><span data-stu-id="86e14-129">The status of the operation.</span></span> <span data-ttu-id="86e14-130">Вы не можете получить доступ к состоянию напрямую; Вместо этого передайте состояние в подставляемую функцию [**чеккакцессфуллимаппед**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="86e14-130">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="86e14-131">**Чеккакцессфуллимаппед** возвращает **значение true** , если все значения из соответствующего **образца**, **сбора** или операции **загрузки** обращались к сопоставленным плиткам в [мозаичном ресурсе](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="86e14-131">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="86e14-132">Если какие бы то ни было значения были взяты из несопоставленной плитки, **чеккакцессфуллимаппед** возвращает **значение false**.</span><span class="sxs-lookup"><span data-stu-id="86e14-132">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86e14-133">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="86e14-133">Return value</span></span>

<span data-ttu-id="86e14-134">Тип: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="86e14-134">Type: **TemplateType**</span></span>

<span data-ttu-id="86e14-135">Значение из четырех компонентов, тип которого совпадает с типом шаблона.</span><span class="sxs-lookup"><span data-stu-id="86e14-135">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="86e14-136">Примечания</span><span class="sxs-lookup"><span data-stu-id="86e14-136">Remarks</span></span>

<span data-ttu-id="86e14-137">Примеры текстур можно использовать для интерполяции билинейной.</span><span class="sxs-lookup"><span data-stu-id="86e14-137">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="86e14-138">Эта функция поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="86e14-138">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="86e14-139">Вершина</span><span class="sxs-lookup"><span data-stu-id="86e14-139">Vertex</span></span> | <span data-ttu-id="86e14-140">Поверхности</span><span class="sxs-lookup"><span data-stu-id="86e14-140">Hull</span></span> | <span data-ttu-id="86e14-141">Домен</span><span class="sxs-lookup"><span data-stu-id="86e14-141">Domain</span></span> | <span data-ttu-id="86e14-142">Геометрия</span><span class="sxs-lookup"><span data-stu-id="86e14-142">Geometry</span></span> | <span data-ttu-id="86e14-143">Пиксель</span><span class="sxs-lookup"><span data-stu-id="86e14-143">Pixel</span></span> | <span data-ttu-id="86e14-144">Вычисления</span><span class="sxs-lookup"><span data-stu-id="86e14-144">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="86e14-145">x</span><span class="sxs-lookup"><span data-stu-id="86e14-145">x</span></span>      | <span data-ttu-id="86e14-146">x</span><span class="sxs-lookup"><span data-stu-id="86e14-146">x</span></span>    | <span data-ttu-id="86e14-147">x</span><span class="sxs-lookup"><span data-stu-id="86e14-147">x</span></span>      | <span data-ttu-id="86e14-148">x</span><span class="sxs-lookup"><span data-stu-id="86e14-148">x</span></span>        | <span data-ttu-id="86e14-149">x</span><span class="sxs-lookup"><span data-stu-id="86e14-149">x</span></span>     | <span data-ttu-id="86e14-150">x</span><span class="sxs-lookup"><span data-stu-id="86e14-150">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="86e14-151">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="86e14-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86e14-152">Методы Гасералфа</span><span class="sxs-lookup"><span data-stu-id="86e14-152">GatherAlpha methods</span></span>](texture2darray-gatheralpha.md)
</dt> </dl>

 

 
