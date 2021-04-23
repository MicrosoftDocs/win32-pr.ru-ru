---
title: 'Функция Texture2DArray:: Гасеркмпблуе (S, float, float, int2, int2, int2, int2, uint)'
description: 'Для четырех значений шаг текселя, которые будут использоваться в операции линейной фильтрации, функция возвращает сравнение их синего компонента со значением сравнения вместе с состоянием сопоставления плиток. | Функция Texture2DArray:: Гасеркмпблуе (S, float, float, int2, int2, int2, int2, uint)'
ms.assetid: C47FD97F-2848-44F7-91E0-2120D08D89C7
keywords:
- Функция Гасеркмпблуе HLSL
topic_type:
- apiref
api_name:
- GatherCmpBlue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 059c81d64520df98846b4b9397a5eb3ab0488991
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986717"
---
# <a name="texture2darraygathercmpbluesfloatfloatint2int2int2int2uint-function"></a><span data-ttu-id="4eb1e-105">Функция Texture2DArray:: Гасеркмпблуе (S, float, float, int2, int2, int2, int2, uint)</span><span class="sxs-lookup"><span data-stu-id="4eb1e-105">Texture2DArray::GatherCmpBlue(S,float,float,int2,int2,int2,int2,uint) function</span></span>

<span data-ttu-id="4eb1e-106">Для четырех значений шаг текселя, которые будут использоваться в операции линейной фильтрации, функция возвращает сравнение их синего компонента со значением сравнения вместе с состоянием сопоставления плиток.</span><span class="sxs-lookup"><span data-stu-id="4eb1e-106">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their blue component against a compare value along with tile-mapping status.</span></span>

## <a name="syntax"></a><span data-ttu-id="4eb1e-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4eb1e-107">Syntax</span></span>


``` syntax
TemplateType GatherCmpBlue(
  in  SamplerState S,
  in  float        Location,
  in  float        CompareValue,
  in  int2         Offset1,
  in  int2         Offset2,
  in  int2         Offset3,
  in  int2         Offset4,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="4eb1e-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="4eb1e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4eb1e-109">*S* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="4eb1e-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4eb1e-110">Тип: **самплерстате**</span><span class="sxs-lookup"><span data-stu-id="4eb1e-110">Type: **SamplerState**</span></span>

<span data-ttu-id="4eb1e-111">Индекс выборки с отсчетом от нуля.</span><span class="sxs-lookup"><span data-stu-id="4eb1e-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="4eb1e-112">*Расположение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4eb1e-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4eb1e-113">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="4eb1e-113">Type: **float**</span></span>

<span data-ttu-id="4eb1e-114">Образцы координат (u, v).</span><span class="sxs-lookup"><span data-stu-id="4eb1e-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="4eb1e-115">*Компаревалуе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4eb1e-115">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4eb1e-116">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="4eb1e-116">Type: **float**</span></span>

<span data-ttu-id="4eb1e-117">Значение, сравниваемое по каждому значению выборки.</span><span class="sxs-lookup"><span data-stu-id="4eb1e-117">A value to compare each against each sampled value.</span></span>

</dd> <dt>

<span data-ttu-id="4eb1e-118">*Offset1* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4eb1e-118">*Offset1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4eb1e-119">Тип: **int2**</span><span class="sxs-lookup"><span data-stu-id="4eb1e-119">Type: **int2**</span></span>

<span data-ttu-id="4eb1e-120">Первый компонент смещения, применяемый к координатам текстуры перед выборкой.</span><span class="sxs-lookup"><span data-stu-id="4eb1e-120">The first offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="4eb1e-121">*Offset2* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4eb1e-121">*Offset2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4eb1e-122">Тип: **int2**</span><span class="sxs-lookup"><span data-stu-id="4eb1e-122">Type: **int2**</span></span>

<span data-ttu-id="4eb1e-123">Второй компонент смещения, применяемый к координатам текстуры перед выборкой.</span><span class="sxs-lookup"><span data-stu-id="4eb1e-123">The second offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="4eb1e-124">*Offset3* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4eb1e-124">*Offset3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4eb1e-125">Тип: **int2**</span><span class="sxs-lookup"><span data-stu-id="4eb1e-125">Type: **int2**</span></span>

<span data-ttu-id="4eb1e-126">Третий компонент смещения, применяемый к координатам текстуры перед выборкой.</span><span class="sxs-lookup"><span data-stu-id="4eb1e-126">The third offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="4eb1e-127">*Offset4* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4eb1e-127">*Offset4* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4eb1e-128">Тип: **int2**</span><span class="sxs-lookup"><span data-stu-id="4eb1e-128">Type: **int2**</span></span>

<span data-ttu-id="4eb1e-129">Четвертый компонент смещения, применяемый к координатам текстуры перед выборкой.</span><span class="sxs-lookup"><span data-stu-id="4eb1e-129">The fourth offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="4eb1e-130">*Состояние* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="4eb1e-130">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4eb1e-131">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="4eb1e-131">Type: **uint**</span></span>

<span data-ttu-id="4eb1e-132">Состояние операции.</span><span class="sxs-lookup"><span data-stu-id="4eb1e-132">The status of the operation.</span></span> <span data-ttu-id="4eb1e-133">Вы не можете получить доступ к состоянию напрямую; Вместо этого передайте состояние в подставляемую функцию [**чеккакцессфуллимаппед**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="4eb1e-133">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="4eb1e-134">**Чеккакцессфуллимаппед** возвращает **значение true** , если все значения из соответствующего **образца**, **сбора** или операции **загрузки** обращались к сопоставленным плиткам в [мозаичном ресурсе](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="4eb1e-134">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="4eb1e-135">Если какие бы то ни было значения были взяты из несопоставленной плитки, **чеккакцессфуллимаппед** возвращает **значение false**.</span><span class="sxs-lookup"><span data-stu-id="4eb1e-135">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4eb1e-136">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4eb1e-136">Return value</span></span>

<span data-ttu-id="4eb1e-137">Тип: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="4eb1e-137">Type: **TemplateType**</span></span>

<span data-ttu-id="4eb1e-138">Значение из четырех компонентов, тип которого совпадает с типом шаблона.</span><span class="sxs-lookup"><span data-stu-id="4eb1e-138">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="4eb1e-139">Примечания</span><span class="sxs-lookup"><span data-stu-id="4eb1e-139">Remarks</span></span>

<span data-ttu-id="4eb1e-140">Примеры текстур можно использовать для интерполяции билинейной.</span><span class="sxs-lookup"><span data-stu-id="4eb1e-140">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="4eb1e-141">Эта функция поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="4eb1e-141">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="4eb1e-142">Вершина</span><span class="sxs-lookup"><span data-stu-id="4eb1e-142">Vertex</span></span> | <span data-ttu-id="4eb1e-143">Поверхности</span><span class="sxs-lookup"><span data-stu-id="4eb1e-143">Hull</span></span> | <span data-ttu-id="4eb1e-144">Домен</span><span class="sxs-lookup"><span data-stu-id="4eb1e-144">Domain</span></span> | <span data-ttu-id="4eb1e-145">Геометрия</span><span class="sxs-lookup"><span data-stu-id="4eb1e-145">Geometry</span></span> | <span data-ttu-id="4eb1e-146">Пиксель</span><span class="sxs-lookup"><span data-stu-id="4eb1e-146">Pixel</span></span> | <span data-ttu-id="4eb1e-147">Вычисления</span><span class="sxs-lookup"><span data-stu-id="4eb1e-147">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="4eb1e-148">x</span><span class="sxs-lookup"><span data-stu-id="4eb1e-148">x</span></span>      | <span data-ttu-id="4eb1e-149">x</span><span class="sxs-lookup"><span data-stu-id="4eb1e-149">x</span></span>    | <span data-ttu-id="4eb1e-150">x</span><span class="sxs-lookup"><span data-stu-id="4eb1e-150">x</span></span>      | <span data-ttu-id="4eb1e-151">x</span><span class="sxs-lookup"><span data-stu-id="4eb1e-151">x</span></span>        | <span data-ttu-id="4eb1e-152">x</span><span class="sxs-lookup"><span data-stu-id="4eb1e-152">x</span></span>     | <span data-ttu-id="4eb1e-153">x</span><span class="sxs-lookup"><span data-stu-id="4eb1e-153">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="4eb1e-154">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4eb1e-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4eb1e-155">Методы Гасеркмпблуе</span><span class="sxs-lookup"><span data-stu-id="4eb1e-155">GatherCmpBlue methods</span></span>](texture2darray-gathercmpblue.md)
</dt> </dl>

 

 
