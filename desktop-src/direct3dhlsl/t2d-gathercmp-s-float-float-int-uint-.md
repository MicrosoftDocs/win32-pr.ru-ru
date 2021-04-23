---
title: 'Функция Texture2D:: Гасеркмп (S, float, float, int, uint)'
description: 'Для четырех шаг текселя значений, которые будут использоваться в операции линейной фильтрации, возвращает их сравнение со значением сравнения вместе с состоянием сопоставления плиток. | Функция Texture2D:: Гасеркмп (S, float, float, int, uint)'
ms.assetid: A6610587-97C3-4CE5-86A7-3411D422BC8F
keywords:
- Функция Гасеркмп HLSL
topic_type:
- apiref
api_name:
- GatherCmp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: be8246053e0f7ba6357bdd68dc59059fd225bbc8
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986596"
---
# <a name="texture2dgathercmpsfloatfloatintuint-function"></a><span data-ttu-id="06a27-105">Функция Texture2D:: Гасеркмп (S, float, float, int, uint)</span><span class="sxs-lookup"><span data-stu-id="06a27-105">Texture2D::GatherCmp(S,float,float,int,uint) function</span></span>

<span data-ttu-id="06a27-106">Для четырех шаг текселя значений, которые будут использоваться в операции линейной фильтрации, возвращает их сравнение со значением сравнения вместе с состоянием сопоставления плиток.</span><span class="sxs-lookup"><span data-stu-id="06a27-106">For four texel values that would be used in a bi-linear filtering operation, returns their comparison against a compare value along with tile-mapping status.</span></span>

## <a name="syntax"></a><span data-ttu-id="06a27-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="06a27-107">Syntax</span></span>


``` syntax
TemplateType GatherCmp(
  in  SamplerState S,
  in  float        Location,
  in  float        CompareValue,
  in  int2         Offset,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="06a27-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="06a27-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06a27-109">*S* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="06a27-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06a27-110">Тип: **самплерстате**</span><span class="sxs-lookup"><span data-stu-id="06a27-110">Type: **SamplerState**</span></span>

<span data-ttu-id="06a27-111">Индекс выборки с отсчетом от нуля.</span><span class="sxs-lookup"><span data-stu-id="06a27-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="06a27-112">*Расположение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="06a27-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06a27-113">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="06a27-113">Type: **float**</span></span>

<span data-ttu-id="06a27-114">Образцы координат (u, v).</span><span class="sxs-lookup"><span data-stu-id="06a27-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="06a27-115">*Компаревалуе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="06a27-115">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06a27-116">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="06a27-116">Type: **float**</span></span>

<span data-ttu-id="06a27-117">Значение, сравниваемое по каждому значению выборки.</span><span class="sxs-lookup"><span data-stu-id="06a27-117">A value to compare each against each sampled value.</span></span>

</dd> <dt>

<span data-ttu-id="06a27-118">*Смещение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="06a27-118">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06a27-119">Тип: **int2**</span><span class="sxs-lookup"><span data-stu-id="06a27-119">Type: **int2**</span></span>

<span data-ttu-id="06a27-120">Смещение в пикселей текстуры, применяемое к координатам текстуры перед выборкой.</span><span class="sxs-lookup"><span data-stu-id="06a27-120">The offset in texels applied to the texture coordinates before sampling.</span></span> <span data-ttu-id="06a27-121">Должно быть литеральным значением.</span><span class="sxs-lookup"><span data-stu-id="06a27-121">Must be a literal value.</span></span>

</dd> <dt>

<span data-ttu-id="06a27-122">*Состояние* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="06a27-122">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="06a27-123">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="06a27-123">Type: **uint**</span></span>

<span data-ttu-id="06a27-124">Состояние операции.</span><span class="sxs-lookup"><span data-stu-id="06a27-124">The status of the operation.</span></span> <span data-ttu-id="06a27-125">Вы не можете получить доступ к состоянию напрямую; Вместо этого передайте состояние в подставляемую функцию [**чеккакцессфуллимаппед**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="06a27-125">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="06a27-126">**Чеккакцессфуллимаппед** возвращает **значение true** , если все значения из соответствующего **образца**, **сбора** или операции **загрузки** обращались к сопоставленным плиткам в [мозаичном ресурсе](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="06a27-126">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="06a27-127">Если какие бы то ни было значения были взяты из несопоставленной плитки, **чеккакцессфуллимаппед** возвращает **значение false**.</span><span class="sxs-lookup"><span data-stu-id="06a27-127">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06a27-128">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="06a27-128">Return value</span></span>

<span data-ttu-id="06a27-129">Тип: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="06a27-129">Type: **TemplateType**</span></span>

<span data-ttu-id="06a27-130">Значение из четырех компонентов, тип которого совпадает с типом шаблона.</span><span class="sxs-lookup"><span data-stu-id="06a27-130">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="06a27-131">Примечания</span><span class="sxs-lookup"><span data-stu-id="06a27-131">Remarks</span></span>

<span data-ttu-id="06a27-132">Примеры текстур можно использовать для интерполяции билинейной.</span><span class="sxs-lookup"><span data-stu-id="06a27-132">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="06a27-133">Эта функция поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="06a27-133">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="06a27-134">Вершина</span><span class="sxs-lookup"><span data-stu-id="06a27-134">Vertex</span></span> | <span data-ttu-id="06a27-135">Поверхности</span><span class="sxs-lookup"><span data-stu-id="06a27-135">Hull</span></span> | <span data-ttu-id="06a27-136">Домен</span><span class="sxs-lookup"><span data-stu-id="06a27-136">Domain</span></span> | <span data-ttu-id="06a27-137">Геометрия</span><span class="sxs-lookup"><span data-stu-id="06a27-137">Geometry</span></span> | <span data-ttu-id="06a27-138">Пиксель</span><span class="sxs-lookup"><span data-stu-id="06a27-138">Pixel</span></span> | <span data-ttu-id="06a27-139">Вычисления</span><span class="sxs-lookup"><span data-stu-id="06a27-139">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="06a27-140">x</span><span class="sxs-lookup"><span data-stu-id="06a27-140">x</span></span>      | <span data-ttu-id="06a27-141">x</span><span class="sxs-lookup"><span data-stu-id="06a27-141">x</span></span>    | <span data-ttu-id="06a27-142">x</span><span class="sxs-lookup"><span data-stu-id="06a27-142">x</span></span>      | <span data-ttu-id="06a27-143">x</span><span class="sxs-lookup"><span data-stu-id="06a27-143">x</span></span>        | <span data-ttu-id="06a27-144">x</span><span class="sxs-lookup"><span data-stu-id="06a27-144">x</span></span>     | <span data-ttu-id="06a27-145">x</span><span class="sxs-lookup"><span data-stu-id="06a27-145">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="06a27-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="06a27-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06a27-147">Методы Гасеркмп</span><span class="sxs-lookup"><span data-stu-id="06a27-147">GatherCmp methods</span></span>](texture2d-gathercmp.md)
</dt> </dl>

 

 
