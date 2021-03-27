---
title: 'Функция Texture2DArray:: Гасеркмпред (S, float, float, int, uint)'
description: 'Для четырех значений шаг текселя, которые будут использоваться в операции линейной фильтрации, функция возвращает сравнение их красного компонента со значением сравнения вместе с состоянием сопоставления плиток. | Функция Texture2DArray:: Гасеркмпред (S, float, float, int, uint)'
ms.assetid: 83974A85-26CB-4724-A60F-64F214800723
keywords:
- Функция Гасеркмпред HLSL
topic_type:
- apiref
api_name:
- GatherCmpRed
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 79743d4d2b30049a580309aa79bf6b3d79c73d3f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986637"
---
# <a name="texture2darraygathercmpredsfloatfloatintuint-function"></a><span data-ttu-id="9cd5b-105">Функция Texture2DArray:: Гасеркмпред (S, float, float, int, uint)</span><span class="sxs-lookup"><span data-stu-id="9cd5b-105">Texture2DArray::GatherCmpRed(S,float,float,int,uint) function</span></span>

<span data-ttu-id="9cd5b-106">Для четырех значений шаг текселя, которые будут использоваться в операции линейной фильтрации, функция возвращает сравнение их красного компонента со значением сравнения вместе с состоянием сопоставления плиток.</span><span class="sxs-lookup"><span data-stu-id="9cd5b-106">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their red component against a compare value along with tile-mapping status.</span></span>

## <a name="syntax"></a><span data-ttu-id="9cd5b-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9cd5b-107">Syntax</span></span>


``` syntax
TemplateType GatherCmpRed(
  in  SamplerState S,
  in  float        Location,
  in  float        CompareValue,
  in  int          Offset,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="9cd5b-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="9cd5b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9cd5b-109">*S* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="9cd5b-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9cd5b-110">Тип: **самплерстате**</span><span class="sxs-lookup"><span data-stu-id="9cd5b-110">Type: **SamplerState**</span></span>

<span data-ttu-id="9cd5b-111">Индекс выборки с отсчетом от нуля.</span><span class="sxs-lookup"><span data-stu-id="9cd5b-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="9cd5b-112">*Расположение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9cd5b-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9cd5b-113">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="9cd5b-113">Type: **float**</span></span>

<span data-ttu-id="9cd5b-114">Образцы координат (u, v).</span><span class="sxs-lookup"><span data-stu-id="9cd5b-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="9cd5b-115">*Компаревалуе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9cd5b-115">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9cd5b-116">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="9cd5b-116">Type: **float**</span></span>

<span data-ttu-id="9cd5b-117">Значение, сравниваемое по каждому значению выборки.</span><span class="sxs-lookup"><span data-stu-id="9cd5b-117">A value to compare each against each sampled value.</span></span>

</dd> <dt>

<span data-ttu-id="9cd5b-118">*Смещение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9cd5b-118">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9cd5b-119">Тип: **int**</span><span class="sxs-lookup"><span data-stu-id="9cd5b-119">Type: **int**</span></span>

<span data-ttu-id="9cd5b-120">Смещение, применяемое к координатам текстуры перед выборкой.</span><span class="sxs-lookup"><span data-stu-id="9cd5b-120">The offset applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="9cd5b-121">*Состояние* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="9cd5b-121">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9cd5b-122">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="9cd5b-122">Type: **uint**</span></span>

<span data-ttu-id="9cd5b-123">Состояние операции.</span><span class="sxs-lookup"><span data-stu-id="9cd5b-123">The status of the operation.</span></span> <span data-ttu-id="9cd5b-124">Вы не можете получить доступ к состоянию напрямую; Вместо этого передайте состояние в подставляемую функцию [**чеккакцессфуллимаппед**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="9cd5b-124">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="9cd5b-125">**Чеккакцессфуллимаппед** возвращает **значение true** , если все значения из соответствующего **образца**, **сбора** или операции **загрузки** обращались к сопоставленным плиткам в [мозаичном ресурсе](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="9cd5b-125">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="9cd5b-126">Если какие бы то ни было значения были взяты из несопоставленной плитки, **чеккакцессфуллимаппед** возвращает **значение false**.</span><span class="sxs-lookup"><span data-stu-id="9cd5b-126">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9cd5b-127">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9cd5b-127">Return value</span></span>

<span data-ttu-id="9cd5b-128">Тип: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="9cd5b-128">Type: **TemplateType**</span></span>

<span data-ttu-id="9cd5b-129">Значение из четырех компонентов, тип которого совпадает с типом шаблона.</span><span class="sxs-lookup"><span data-stu-id="9cd5b-129">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="9cd5b-130">Примечания</span><span class="sxs-lookup"><span data-stu-id="9cd5b-130">Remarks</span></span>

<span data-ttu-id="9cd5b-131">Примеры текстур можно использовать для интерполяции билинейной.</span><span class="sxs-lookup"><span data-stu-id="9cd5b-131">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="9cd5b-132">Эта функция поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="9cd5b-132">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="9cd5b-133">Вершина</span><span class="sxs-lookup"><span data-stu-id="9cd5b-133">Vertex</span></span> | <span data-ttu-id="9cd5b-134">Поверхности</span><span class="sxs-lookup"><span data-stu-id="9cd5b-134">Hull</span></span> | <span data-ttu-id="9cd5b-135">Домен</span><span class="sxs-lookup"><span data-stu-id="9cd5b-135">Domain</span></span> | <span data-ttu-id="9cd5b-136">Геометрия</span><span class="sxs-lookup"><span data-stu-id="9cd5b-136">Geometry</span></span> | <span data-ttu-id="9cd5b-137">Пиксель</span><span class="sxs-lookup"><span data-stu-id="9cd5b-137">Pixel</span></span> | <span data-ttu-id="9cd5b-138">Вычисления</span><span class="sxs-lookup"><span data-stu-id="9cd5b-138">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="9cd5b-139">x</span><span class="sxs-lookup"><span data-stu-id="9cd5b-139">x</span></span>      | <span data-ttu-id="9cd5b-140">x</span><span class="sxs-lookup"><span data-stu-id="9cd5b-140">x</span></span>    | <span data-ttu-id="9cd5b-141">x</span><span class="sxs-lookup"><span data-stu-id="9cd5b-141">x</span></span>      | <span data-ttu-id="9cd5b-142">x</span><span class="sxs-lookup"><span data-stu-id="9cd5b-142">x</span></span>        | <span data-ttu-id="9cd5b-143">x</span><span class="sxs-lookup"><span data-stu-id="9cd5b-143">x</span></span>     | <span data-ttu-id="9cd5b-144">x</span><span class="sxs-lookup"><span data-stu-id="9cd5b-144">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="9cd5b-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9cd5b-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9cd5b-146">Методы Гасеркмпред</span><span class="sxs-lookup"><span data-stu-id="9cd5b-146">GatherCmpRed methods</span></span>](texture2darray-gathercmpred.md)
</dt> </dl>

 

 
