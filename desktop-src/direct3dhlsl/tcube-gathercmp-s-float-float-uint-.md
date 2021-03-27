---
title: 'Функция Текстурекубе:: Гасеркмп (S, float, float, uint)'
description: 'Для четырех значений шаг текселя, которые будут использоваться в операции линейной фильтрации, возвращает их сравнение со значением сравнения. | Функция Текстурекубе:: Гасеркмп (S, float, float, uint)'
ms.assetid: 655F4851-708A-478B-BB31-9DC8CDD480D0
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
ms.openlocfilehash: 827132338c3ba2b858a329ec108ef37b36ed54c2
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986584"
---
# <a name="texturecubegathercmpsfloatfloatuint-function"></a><span data-ttu-id="05858-105">Функция Текстурекубе:: Гасеркмп (S, float, float, uint)</span><span class="sxs-lookup"><span data-stu-id="05858-105">TextureCube::GatherCmp(S,float,float,uint) function</span></span>

<span data-ttu-id="05858-106">Для четырех значений шаг текселя, которые будут использоваться в операции линейной фильтрации, возвращает их сравнение со значением сравнения.</span><span class="sxs-lookup"><span data-stu-id="05858-106">For four texel values that would be used in a bi-linear filtering operation, returns their comparison against a compare value.</span></span>

## <a name="syntax"></a><span data-ttu-id="05858-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="05858-107">Syntax</span></span>


``` syntax
TemplateType GatherCmp(
  in  SamplerState S,
  in  float        Location,
  in  float        CompareValue,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="05858-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="05858-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05858-109">*S* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="05858-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="05858-110">Тип: **самплерстате**</span><span class="sxs-lookup"><span data-stu-id="05858-110">Type: **SamplerState**</span></span>

<span data-ttu-id="05858-111">Индекс выборки с отсчетом от нуля.</span><span class="sxs-lookup"><span data-stu-id="05858-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="05858-112">*Расположение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="05858-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="05858-113">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="05858-113">Type: **float**</span></span>

<span data-ttu-id="05858-114">Образцы координат (u, v).</span><span class="sxs-lookup"><span data-stu-id="05858-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="05858-115">*Компаревалуе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="05858-115">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="05858-116">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="05858-116">Type: **float**</span></span>

<span data-ttu-id="05858-117">Значение, сравниваемое по каждому значению выборки.</span><span class="sxs-lookup"><span data-stu-id="05858-117">A value to compare each against each sampled value.</span></span>

</dd> <dt>

<span data-ttu-id="05858-118">*Состояние* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="05858-118">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="05858-119">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="05858-119">Type: **uint**</span></span>

<span data-ttu-id="05858-120">Состояние операции.</span><span class="sxs-lookup"><span data-stu-id="05858-120">The status of the operation.</span></span> <span data-ttu-id="05858-121">Вы не можете получить доступ к состоянию напрямую; Вместо этого передайте состояние в подставляемую функцию [**чеккакцессфуллимаппед**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="05858-121">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="05858-122">**Чеккакцессфуллимаппед** возвращает **значение true** , если все значения из соответствующего **образца**, **сбора** или операции **загрузки** обращались к сопоставленным плиткам в [мозаичном ресурсе](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="05858-122">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="05858-123">Если какие бы то ни было значения были взяты из несопоставленной плитки, **чеккакцессфуллимаппед** возвращает **значение false**.</span><span class="sxs-lookup"><span data-stu-id="05858-123">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="05858-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="05858-124">Return value</span></span>

<span data-ttu-id="05858-125">Тип: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="05858-125">Type: **TemplateType**</span></span>

<span data-ttu-id="05858-126">Значение из четырех компонентов, тип которого совпадает с типом шаблона.</span><span class="sxs-lookup"><span data-stu-id="05858-126">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="05858-127">Примечания</span><span class="sxs-lookup"><span data-stu-id="05858-127">Remarks</span></span>

<span data-ttu-id="05858-128">Примеры текстур можно использовать для интерполяции билинейной.</span><span class="sxs-lookup"><span data-stu-id="05858-128">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="05858-129">Эта функция поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="05858-129">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="05858-130">Вершина</span><span class="sxs-lookup"><span data-stu-id="05858-130">Vertex</span></span> | <span data-ttu-id="05858-131">Поверхности</span><span class="sxs-lookup"><span data-stu-id="05858-131">Hull</span></span> | <span data-ttu-id="05858-132">Домен</span><span class="sxs-lookup"><span data-stu-id="05858-132">Domain</span></span> | <span data-ttu-id="05858-133">Геометрия</span><span class="sxs-lookup"><span data-stu-id="05858-133">Geometry</span></span> | <span data-ttu-id="05858-134">Пиксель</span><span class="sxs-lookup"><span data-stu-id="05858-134">Pixel</span></span> | <span data-ttu-id="05858-135">Вычисления</span><span class="sxs-lookup"><span data-stu-id="05858-135">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="05858-136">x</span><span class="sxs-lookup"><span data-stu-id="05858-136">x</span></span>      | <span data-ttu-id="05858-137">x</span><span class="sxs-lookup"><span data-stu-id="05858-137">x</span></span>    | <span data-ttu-id="05858-138">x</span><span class="sxs-lookup"><span data-stu-id="05858-138">x</span></span>      | <span data-ttu-id="05858-139">x</span><span class="sxs-lookup"><span data-stu-id="05858-139">x</span></span>        | <span data-ttu-id="05858-140">x</span><span class="sxs-lookup"><span data-stu-id="05858-140">x</span></span>     | <span data-ttu-id="05858-141">x</span><span class="sxs-lookup"><span data-stu-id="05858-141">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="05858-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="05858-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05858-143">Методы Гасеркмп</span><span class="sxs-lookup"><span data-stu-id="05858-143">GatherCmp methods</span></span>](texturecube-gathercmp.md)
</dt> <dt>

[<span data-ttu-id="05858-144">**текстурекубе**</span><span class="sxs-lookup"><span data-stu-id="05858-144">**TextureCube**</span></span>](texturecube.md)
</dt> </dl>

 

 
