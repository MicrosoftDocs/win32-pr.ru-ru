---
title: 'Функция Текстурекубеаррай:: Гасеркмпблуе (S, float, float, uint)'
description: 'Для четырех значений шаг текселя, которые будут использоваться в операции линейной фильтрации, функция возвращает сравнение их синего компонента со значением сравнения вместе с состоянием сопоставления плиток. | Функция Текстурекубеаррай:: Гасеркмпблуе (S, float, float, uint)'
ms.assetid: 81F82EB1-D662-4A18-856F-26AE5C1A41C6
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
ms.openlocfilehash: 9de8d578706cd0799bd2132f05b8a31b7daa8afe
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104273480"
---
# <a name="texturecubearraygathercmpbluesfloatfloatuint-function"></a><span data-ttu-id="1dcd1-105">Функция Текстурекубеаррай:: Гасеркмпблуе (S, float, float, uint)</span><span class="sxs-lookup"><span data-stu-id="1dcd1-105">TextureCubeArray::GatherCmpBlue(S,float,float,uint) function</span></span>

<span data-ttu-id="1dcd1-106">Для четырех значений шаг текселя, которые будут использоваться в операции линейной фильтрации, функция возвращает сравнение их синего компонента со значением сравнения вместе с состоянием сопоставления плиток.</span><span class="sxs-lookup"><span data-stu-id="1dcd1-106">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their blue component against a compare value along with tile-mapping status.</span></span>

## <a name="syntax"></a><span data-ttu-id="1dcd1-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1dcd1-107">Syntax</span></span>


``` syntax
TemplateType GatherCmpBlue(
  in  SamplerState S,
  in  float        Location,
  in  float        CompareValue,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="1dcd1-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="1dcd1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1dcd1-109">*S* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="1dcd1-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1dcd1-110">Тип: **самплерстате**</span><span class="sxs-lookup"><span data-stu-id="1dcd1-110">Type: **SamplerState**</span></span>

<span data-ttu-id="1dcd1-111">Индекс выборки с отсчетом от нуля.</span><span class="sxs-lookup"><span data-stu-id="1dcd1-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="1dcd1-112">*Расположение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1dcd1-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1dcd1-113">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="1dcd1-113">Type: **float**</span></span>

<span data-ttu-id="1dcd1-114">Образцы координат (u, v).</span><span class="sxs-lookup"><span data-stu-id="1dcd1-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="1dcd1-115">*Компаревалуе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1dcd1-115">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1dcd1-116">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="1dcd1-116">Type: **float**</span></span>

<span data-ttu-id="1dcd1-117">Значение, сравниваемое по каждому значению выборки.</span><span class="sxs-lookup"><span data-stu-id="1dcd1-117">A value to compare each against each sampled value.</span></span>

</dd> <dt>

<span data-ttu-id="1dcd1-118">*Состояние* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="1dcd1-118">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1dcd1-119">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="1dcd1-119">Type: **uint**</span></span>

<span data-ttu-id="1dcd1-120">Состояние операции.</span><span class="sxs-lookup"><span data-stu-id="1dcd1-120">The status of the operation.</span></span> <span data-ttu-id="1dcd1-121">Вы не можете получить доступ к состоянию напрямую; Вместо этого передайте состояние в подставляемую функцию [**чеккакцессфуллимаппед**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="1dcd1-121">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="1dcd1-122">**Чеккакцессфуллимаппед** возвращает **значение true** , если все значения из соответствующего **образца**, **сбора** или операции **загрузки** обращались к сопоставленным плиткам в [мозаичном ресурсе](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="1dcd1-122">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="1dcd1-123">Если какие бы то ни было значения были взяты из несопоставленной плитки, **чеккакцессфуллимаппед** возвращает **значение false**.</span><span class="sxs-lookup"><span data-stu-id="1dcd1-123">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1dcd1-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1dcd1-124">Return value</span></span>

<span data-ttu-id="1dcd1-125">Тип: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="1dcd1-125">Type: **TemplateType**</span></span>

<span data-ttu-id="1dcd1-126">Значение из четырех компонентов, тип которого совпадает с типом шаблона.</span><span class="sxs-lookup"><span data-stu-id="1dcd1-126">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="1dcd1-127">Примечания</span><span class="sxs-lookup"><span data-stu-id="1dcd1-127">Remarks</span></span>

<span data-ttu-id="1dcd1-128">Примеры текстур можно использовать для интерполяции билинейной.</span><span class="sxs-lookup"><span data-stu-id="1dcd1-128">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="1dcd1-129">Эта функция поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="1dcd1-129">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="1dcd1-130">Вершина</span><span class="sxs-lookup"><span data-stu-id="1dcd1-130">Vertex</span></span> | <span data-ttu-id="1dcd1-131">Поверхности</span><span class="sxs-lookup"><span data-stu-id="1dcd1-131">Hull</span></span> | <span data-ttu-id="1dcd1-132">Домен</span><span class="sxs-lookup"><span data-stu-id="1dcd1-132">Domain</span></span> | <span data-ttu-id="1dcd1-133">Геометрия</span><span class="sxs-lookup"><span data-stu-id="1dcd1-133">Geometry</span></span> | <span data-ttu-id="1dcd1-134">Пиксель</span><span class="sxs-lookup"><span data-stu-id="1dcd1-134">Pixel</span></span> | <span data-ttu-id="1dcd1-135">Вычисления</span><span class="sxs-lookup"><span data-stu-id="1dcd1-135">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="1dcd1-136">x</span><span class="sxs-lookup"><span data-stu-id="1dcd1-136">x</span></span>      | <span data-ttu-id="1dcd1-137">x</span><span class="sxs-lookup"><span data-stu-id="1dcd1-137">x</span></span>    | <span data-ttu-id="1dcd1-138">x</span><span class="sxs-lookup"><span data-stu-id="1dcd1-138">x</span></span>      | <span data-ttu-id="1dcd1-139">x</span><span class="sxs-lookup"><span data-stu-id="1dcd1-139">x</span></span>        | <span data-ttu-id="1dcd1-140">x</span><span class="sxs-lookup"><span data-stu-id="1dcd1-140">x</span></span>     | <span data-ttu-id="1dcd1-141">x</span><span class="sxs-lookup"><span data-stu-id="1dcd1-141">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="1dcd1-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1dcd1-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1dcd1-143">Методы Гасеркмпблуе</span><span class="sxs-lookup"><span data-stu-id="1dcd1-143">GatherCmpBlue methods</span></span>](texturecubearray-gathercmpblue.md)
</dt> <dt>

[<span data-ttu-id="1dcd1-144">**текстурекубеаррай**</span><span class="sxs-lookup"><span data-stu-id="1dcd1-144">**TextureCubeArray**</span></span>](texturecubearray.md)
</dt> </dl>

 

 
