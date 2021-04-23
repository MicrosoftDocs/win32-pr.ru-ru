---
title: 'Функция Texture2D:: Гасералфа (S, float, int, uint)'
description: 'Возвращает альфа-компоненты четырех значений шаг текселя, которые будут использоваться в операции линейной фильтрации, а также состояние сопоставления плиток. | Функция Texture2D:: Гасералфа (S, float, int, uint)'
ms.assetid: A05E9286-2DCA-4A85-A337-0E010EF98D7F
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
ms.openlocfilehash: 63bdefe7a491499a46e3a9f15d82eaedd922a0b8
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986244"
---
# <a name="texture2dgatheralphasfloatintuint-function"></a><span data-ttu-id="ef6e9-105">Функция Texture2D:: Гасералфа (S, float, int, uint)</span><span class="sxs-lookup"><span data-stu-id="ef6e9-105">Texture2D::GatherAlpha(S,float,int,uint) function</span></span>

<span data-ttu-id="ef6e9-106">Возвращает альфа-компоненты четырех значений шаг текселя, которые будут использоваться в операции линейной фильтрации, а также состояние сопоставления плиток.</span><span class="sxs-lookup"><span data-stu-id="ef6e9-106">Returns the alpha components of the four texel values that would be used in a bi-linear filtering operation, along with tile-mapping status.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef6e9-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ef6e9-107">Syntax</span></span>


``` syntax
TemplateType GatherAlpha(
  in  SamplerState S,
  in  float        Location,
  in  int          Offset,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="ef6e9-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="ef6e9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef6e9-109">*S* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="ef6e9-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef6e9-110">Тип: **самплерстате**</span><span class="sxs-lookup"><span data-stu-id="ef6e9-110">Type: **SamplerState**</span></span>

<span data-ttu-id="ef6e9-111">Индекс выборки с отсчетом от нуля.</span><span class="sxs-lookup"><span data-stu-id="ef6e9-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="ef6e9-112">*Расположение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ef6e9-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef6e9-113">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="ef6e9-113">Type: **float**</span></span>

<span data-ttu-id="ef6e9-114">Образцы координат (u, v).</span><span class="sxs-lookup"><span data-stu-id="ef6e9-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="ef6e9-115">*Смещение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ef6e9-115">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef6e9-116">Тип: **int**</span><span class="sxs-lookup"><span data-stu-id="ef6e9-116">Type: **int**</span></span>

<span data-ttu-id="ef6e9-117">Смещение, применяемое к координатам текстуры перед выборкой.</span><span class="sxs-lookup"><span data-stu-id="ef6e9-117">The offset applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="ef6e9-118">*Состояние* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="ef6e9-118">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ef6e9-119">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="ef6e9-119">Type: **uint**</span></span>

<span data-ttu-id="ef6e9-120">Состояние операции.</span><span class="sxs-lookup"><span data-stu-id="ef6e9-120">The status of the operation.</span></span> <span data-ttu-id="ef6e9-121">Вы не можете получить доступ к состоянию напрямую; Вместо этого передайте состояние в подставляемую функцию [**чеккакцессфуллимаппед**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="ef6e9-121">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="ef6e9-122">**Чеккакцессфуллимаппед** возвращает **значение true** , если все значения из соответствующего **образца**, **сбора** или операции **загрузки** обращались к сопоставленным плиткам в [мозаичном ресурсе](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="ef6e9-122">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="ef6e9-123">Если какие бы то ни было значения были взяты из несопоставленной плитки, **чеккакцессфуллимаппед** возвращает **значение false**.</span><span class="sxs-lookup"><span data-stu-id="ef6e9-123">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef6e9-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ef6e9-124">Return value</span></span>

<span data-ttu-id="ef6e9-125">Тип: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="ef6e9-125">Type: **TemplateType**</span></span>

<span data-ttu-id="ef6e9-126">Значение из четырех компонентов, тип которого совпадает с типом шаблона.</span><span class="sxs-lookup"><span data-stu-id="ef6e9-126">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="ef6e9-127">Примечания</span><span class="sxs-lookup"><span data-stu-id="ef6e9-127">Remarks</span></span>

<span data-ttu-id="ef6e9-128">Примеры текстур можно использовать для интерполяции билинейной.</span><span class="sxs-lookup"><span data-stu-id="ef6e9-128">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="ef6e9-129">Эта функция поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="ef6e9-129">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="ef6e9-130">Вершина</span><span class="sxs-lookup"><span data-stu-id="ef6e9-130">Vertex</span></span> | <span data-ttu-id="ef6e9-131">Поверхности</span><span class="sxs-lookup"><span data-stu-id="ef6e9-131">Hull</span></span> | <span data-ttu-id="ef6e9-132">Домен</span><span class="sxs-lookup"><span data-stu-id="ef6e9-132">Domain</span></span> | <span data-ttu-id="ef6e9-133">Геометрия</span><span class="sxs-lookup"><span data-stu-id="ef6e9-133">Geometry</span></span> | <span data-ttu-id="ef6e9-134">Пиксель</span><span class="sxs-lookup"><span data-stu-id="ef6e9-134">Pixel</span></span> | <span data-ttu-id="ef6e9-135">Вычисления</span><span class="sxs-lookup"><span data-stu-id="ef6e9-135">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="ef6e9-136">x</span><span class="sxs-lookup"><span data-stu-id="ef6e9-136">x</span></span>      | <span data-ttu-id="ef6e9-137">x</span><span class="sxs-lookup"><span data-stu-id="ef6e9-137">x</span></span>    | <span data-ttu-id="ef6e9-138">x</span><span class="sxs-lookup"><span data-stu-id="ef6e9-138">x</span></span>      | <span data-ttu-id="ef6e9-139">x</span><span class="sxs-lookup"><span data-stu-id="ef6e9-139">x</span></span>        | <span data-ttu-id="ef6e9-140">x</span><span class="sxs-lookup"><span data-stu-id="ef6e9-140">x</span></span>     | <span data-ttu-id="ef6e9-141">x</span><span class="sxs-lookup"><span data-stu-id="ef6e9-141">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="ef6e9-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ef6e9-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef6e9-143">Методы Гасералфа</span><span class="sxs-lookup"><span data-stu-id="ef6e9-143">GatherAlpha methods</span></span>](texture2d-gatheralpha.md)
</dt> </dl>

 

 
