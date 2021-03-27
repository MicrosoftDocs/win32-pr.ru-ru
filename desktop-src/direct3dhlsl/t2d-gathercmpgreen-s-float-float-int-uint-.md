---
title: 'Функция Texture2D:: Гасеркмпгрин (S, float, float, int, uint)'
description: 'Для четырех значений шаг текселя, которые будут использоваться в операции линейной фильтрации, функция возвращает сравнение зеленого компонента со значением сравнения вместе с состоянием сопоставления плиток. | Функция Texture2D:: Гасеркмпгрин (S, float, float, int, uint)'
ms.assetid: 4A23DE5B-F9DE-45BC-ADF7-D952E4355F7F
keywords:
- Функция Гасеркмпгрин HLSL
topic_type:
- apiref
api_name:
- GatherCmpGreen
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c7fe71d52a39fae3486e9afd86ca126717b7409c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986663"
---
# <a name="texture2dgathercmpgreensfloatfloatintuint-function"></a><span data-ttu-id="3bb68-105">Функция Texture2D:: Гасеркмпгрин (S, float, float, int, uint)</span><span class="sxs-lookup"><span data-stu-id="3bb68-105">Texture2D::GatherCmpGreen(S,float,float,int,uint) function</span></span>

<span data-ttu-id="3bb68-106">Для четырех значений шаг текселя, которые будут использоваться в операции линейной фильтрации, функция возвращает сравнение зеленого компонента со значением сравнения вместе с состоянием сопоставления плиток.</span><span class="sxs-lookup"><span data-stu-id="3bb68-106">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their green component against a compare value along with tile-mapping status.</span></span>

## <a name="syntax"></a><span data-ttu-id="3bb68-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3bb68-107">Syntax</span></span>


``` syntax
TemplateType GatherCmpGreen(
  in  SamplerState S,
  in  float        Location,
  in  float        CompareValue,
  in  int          Offset,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="3bb68-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="3bb68-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3bb68-109">*S* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="3bb68-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3bb68-110">Тип: **самплерстате**</span><span class="sxs-lookup"><span data-stu-id="3bb68-110">Type: **SamplerState**</span></span>

<span data-ttu-id="3bb68-111">Индекс выборки с отсчетом от нуля.</span><span class="sxs-lookup"><span data-stu-id="3bb68-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="3bb68-112">*Расположение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3bb68-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3bb68-113">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="3bb68-113">Type: **float**</span></span>

<span data-ttu-id="3bb68-114">Образцы координат (u, v).</span><span class="sxs-lookup"><span data-stu-id="3bb68-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="3bb68-115">*Компаревалуе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3bb68-115">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3bb68-116">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="3bb68-116">Type: **float**</span></span>

<span data-ttu-id="3bb68-117">Значение, сравниваемое по каждому значению выборки.</span><span class="sxs-lookup"><span data-stu-id="3bb68-117">A value to compare each against each sampled value.</span></span>

</dd> <dt>

<span data-ttu-id="3bb68-118">*Смещение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3bb68-118">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3bb68-119">Тип: **int**</span><span class="sxs-lookup"><span data-stu-id="3bb68-119">Type: **int**</span></span>

<span data-ttu-id="3bb68-120">Смещение, применяемое к координатам текстуры перед выборкой.</span><span class="sxs-lookup"><span data-stu-id="3bb68-120">The offset applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="3bb68-121">*Состояние* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="3bb68-121">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3bb68-122">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="3bb68-122">Type: **uint**</span></span>

<span data-ttu-id="3bb68-123">Состояние операции.</span><span class="sxs-lookup"><span data-stu-id="3bb68-123">The status of the operation.</span></span> <span data-ttu-id="3bb68-124">Вы не можете получить доступ к состоянию напрямую; Вместо этого передайте состояние в подставляемую функцию [**чеккакцессфуллимаппед**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="3bb68-124">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="3bb68-125">**Чеккакцессфуллимаппед** возвращает **значение true** , если все значения из соответствующего **образца**, **сбора** или операции **загрузки** обращались к сопоставленным плиткам в [мозаичном ресурсе](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="3bb68-125">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="3bb68-126">Если какие бы то ни было значения были взяты из несопоставленной плитки, **чеккакцессфуллимаппед** возвращает **значение false**.</span><span class="sxs-lookup"><span data-stu-id="3bb68-126">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3bb68-127">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3bb68-127">Return value</span></span>

<span data-ttu-id="3bb68-128">Тип: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="3bb68-128">Type: **TemplateType**</span></span>

<span data-ttu-id="3bb68-129">Значение из четырех компонентов, тип которого совпадает с типом шаблона.</span><span class="sxs-lookup"><span data-stu-id="3bb68-129">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="3bb68-130">Примечания</span><span class="sxs-lookup"><span data-stu-id="3bb68-130">Remarks</span></span>

<span data-ttu-id="3bb68-131">Примеры текстур можно использовать для интерполяции билинейной.</span><span class="sxs-lookup"><span data-stu-id="3bb68-131">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="3bb68-132">Эта функция поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="3bb68-132">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="3bb68-133">Вершина</span><span class="sxs-lookup"><span data-stu-id="3bb68-133">Vertex</span></span> | <span data-ttu-id="3bb68-134">Поверхности</span><span class="sxs-lookup"><span data-stu-id="3bb68-134">Hull</span></span> | <span data-ttu-id="3bb68-135">Домен</span><span class="sxs-lookup"><span data-stu-id="3bb68-135">Domain</span></span> | <span data-ttu-id="3bb68-136">Геометрия</span><span class="sxs-lookup"><span data-stu-id="3bb68-136">Geometry</span></span> | <span data-ttu-id="3bb68-137">Пиксель</span><span class="sxs-lookup"><span data-stu-id="3bb68-137">Pixel</span></span> | <span data-ttu-id="3bb68-138">Вычисления</span><span class="sxs-lookup"><span data-stu-id="3bb68-138">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="3bb68-139">x</span><span class="sxs-lookup"><span data-stu-id="3bb68-139">x</span></span>      | <span data-ttu-id="3bb68-140">x</span><span class="sxs-lookup"><span data-stu-id="3bb68-140">x</span></span>    | <span data-ttu-id="3bb68-141">x</span><span class="sxs-lookup"><span data-stu-id="3bb68-141">x</span></span>      | <span data-ttu-id="3bb68-142">x</span><span class="sxs-lookup"><span data-stu-id="3bb68-142">x</span></span>        | <span data-ttu-id="3bb68-143">x</span><span class="sxs-lookup"><span data-stu-id="3bb68-143">x</span></span>     | <span data-ttu-id="3bb68-144">x</span><span class="sxs-lookup"><span data-stu-id="3bb68-144">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="3bb68-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3bb68-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3bb68-146">Методы Гасеркмпгрин</span><span class="sxs-lookup"><span data-stu-id="3bb68-146">GatherCmpGreen methods</span></span>](texture2d-gathercmpgreen.md)
</dt> </dl>

 

 
