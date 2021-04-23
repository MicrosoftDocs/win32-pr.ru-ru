---
title: 'Функция Текстурекубеаррай:: Гасеркмпалфа (S, float, float, uint)'
description: 'Для четырех значений шаг текселя, которые будут использоваться в операции линейной фильтрации, функция возвращает сравнение альфа-компонента со значением сравнения вместе с состоянием сопоставления плиток. | Функция Текстурекубеаррай:: Гасеркмпалфа (S, float, float, uint)'
ms.assetid: EA1D7176-3F70-4867-9854-80206A871B23
keywords:
- Функция Гасеркмпалфа HLSL
topic_type:
- apiref
api_name:
- GatherCmpAlpha
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 198179b67a2812417e60a0a1e1512b686d52e98a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104998178"
---
# <a name="texturecubearraygathercmpalphasfloatfloatuint-function"></a><span data-ttu-id="95a2c-105">Функция Текстурекубеаррай:: Гасеркмпалфа (S, float, float, uint)</span><span class="sxs-lookup"><span data-stu-id="95a2c-105">TextureCubeArray::GatherCmpAlpha(S,float,float,uint) function</span></span>

<span data-ttu-id="95a2c-106">Для четырех значений шаг текселя, которые будут использоваться в операции линейной фильтрации, функция возвращает сравнение альфа-компонента со значением сравнения вместе с состоянием сопоставления плиток.</span><span class="sxs-lookup"><span data-stu-id="95a2c-106">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their alpha component against a compare value along with tile-mapping status.</span></span>

## <a name="syntax"></a><span data-ttu-id="95a2c-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="95a2c-107">Syntax</span></span>


``` syntax
TemplateType GatherCmpAlpha(
  in  SamplerState S,
  in  float        Location,
  in  float        CompareValue,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="95a2c-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="95a2c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95a2c-109">*S* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="95a2c-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95a2c-110">Тип: **самплерстате**</span><span class="sxs-lookup"><span data-stu-id="95a2c-110">Type: **SamplerState**</span></span>

<span data-ttu-id="95a2c-111">Индекс выборки с отсчетом от нуля.</span><span class="sxs-lookup"><span data-stu-id="95a2c-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="95a2c-112">*Расположение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="95a2c-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95a2c-113">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="95a2c-113">Type: **float**</span></span>

<span data-ttu-id="95a2c-114">Образцы координат (u, v).</span><span class="sxs-lookup"><span data-stu-id="95a2c-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="95a2c-115">*Компаревалуе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="95a2c-115">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95a2c-116">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="95a2c-116">Type: **float**</span></span>

<span data-ttu-id="95a2c-117">Значение, сравниваемое по каждому значению выборки.</span><span class="sxs-lookup"><span data-stu-id="95a2c-117">A value to compare each against each sampled value.</span></span>

</dd> <dt>

<span data-ttu-id="95a2c-118">*Состояние* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="95a2c-118">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="95a2c-119">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="95a2c-119">Type: **uint**</span></span>

<span data-ttu-id="95a2c-120">Состояние операции.</span><span class="sxs-lookup"><span data-stu-id="95a2c-120">The status of the operation.</span></span> <span data-ttu-id="95a2c-121">Вы не можете получить доступ к состоянию напрямую; Вместо этого передайте состояние в подставляемую функцию [**чеккакцессфуллимаппед**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="95a2c-121">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="95a2c-122">**Чеккакцессфуллимаппед** возвращает **значение true** , если все значения из соответствующего **образца**, **сбора** или операции **загрузки** обращались к сопоставленным плиткам в [мозаичном ресурсе](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="95a2c-122">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="95a2c-123">Если какие бы то ни было значения были взяты из несопоставленной плитки, **чеккакцессфуллимаппед** возвращает **значение false**.</span><span class="sxs-lookup"><span data-stu-id="95a2c-123">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95a2c-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="95a2c-124">Return value</span></span>

<span data-ttu-id="95a2c-125">Тип: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="95a2c-125">Type: **TemplateType**</span></span>

<span data-ttu-id="95a2c-126">Значение из четырех компонентов, тип которого совпадает с типом шаблона.</span><span class="sxs-lookup"><span data-stu-id="95a2c-126">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="95a2c-127">Примечания</span><span class="sxs-lookup"><span data-stu-id="95a2c-127">Remarks</span></span>

<span data-ttu-id="95a2c-128">Примеры текстур можно использовать для интерполяции билинейной.</span><span class="sxs-lookup"><span data-stu-id="95a2c-128">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="95a2c-129">Эта функция поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="95a2c-129">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="95a2c-130">Вершина</span><span class="sxs-lookup"><span data-stu-id="95a2c-130">Vertex</span></span> | <span data-ttu-id="95a2c-131">Поверхности</span><span class="sxs-lookup"><span data-stu-id="95a2c-131">Hull</span></span> | <span data-ttu-id="95a2c-132">Домен</span><span class="sxs-lookup"><span data-stu-id="95a2c-132">Domain</span></span> | <span data-ttu-id="95a2c-133">Геометрия</span><span class="sxs-lookup"><span data-stu-id="95a2c-133">Geometry</span></span> | <span data-ttu-id="95a2c-134">Пиксель</span><span class="sxs-lookup"><span data-stu-id="95a2c-134">Pixel</span></span> | <span data-ttu-id="95a2c-135">Вычисления</span><span class="sxs-lookup"><span data-stu-id="95a2c-135">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="95a2c-136">x</span><span class="sxs-lookup"><span data-stu-id="95a2c-136">x</span></span>      | <span data-ttu-id="95a2c-137">x</span><span class="sxs-lookup"><span data-stu-id="95a2c-137">x</span></span>    | <span data-ttu-id="95a2c-138">x</span><span class="sxs-lookup"><span data-stu-id="95a2c-138">x</span></span>      | <span data-ttu-id="95a2c-139">x</span><span class="sxs-lookup"><span data-stu-id="95a2c-139">x</span></span>        | <span data-ttu-id="95a2c-140">x</span><span class="sxs-lookup"><span data-stu-id="95a2c-140">x</span></span>     | <span data-ttu-id="95a2c-141">x</span><span class="sxs-lookup"><span data-stu-id="95a2c-141">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="95a2c-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="95a2c-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95a2c-143">Методы Гасеркмпалфа</span><span class="sxs-lookup"><span data-stu-id="95a2c-143">GatherCmpAlpha methods</span></span>](texturecubearray-gathercmpalpha.md)
</dt> <dt>

[<span data-ttu-id="95a2c-144">**текстурекубеаррай**</span><span class="sxs-lookup"><span data-stu-id="95a2c-144">**TextureCubeArray**</span></span>](texturecubearray.md)
</dt> </dl>

 

 
