---
title: 'Функция Texture2D:: Гасерред (S, float, int, uint)'
description: 'Возвращает красные компоненты четырех значений шаг текселя, которые будут использоваться в операции линейной фильтрации, вместе с состоянием сопоставления плиток. | Функция Texture2D:: Гасерред (S, float, int, uint)'
ms.assetid: B49F738F-FB5C-4004-A3F3-D87C566DB597
keywords:
- Функция Гасерред HLSL
topic_type:
- apiref
api_name:
- GatherRed
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3381bb6f7388b418e22431575b9a8431ed410b2f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104998166"
---
# <a name="texture2dgatherredsfloatintuint-function"></a><span data-ttu-id="713a4-105">Функция Texture2D:: Гасерред (S, float, int, uint)</span><span class="sxs-lookup"><span data-stu-id="713a4-105">Texture2D::GatherRed(S,float,int,uint) function</span></span>

<span data-ttu-id="713a4-106">Возвращает красные компоненты четырех значений шаг текселя, которые будут использоваться в операции линейной фильтрации, вместе с состоянием сопоставления плиток.</span><span class="sxs-lookup"><span data-stu-id="713a4-106">Returns the red components of the four texel values that would be used in a bi-linear filtering operation, along with tile-mapping status.</span></span>

## <a name="syntax"></a><span data-ttu-id="713a4-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="713a4-107">Syntax</span></span>


``` syntax
TemplateType GatherRed(
  in  SamplerState S,
  in  float        Location,
  in  int          Offset,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="713a4-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="713a4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="713a4-109">*S* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="713a4-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="713a4-110">Тип: **самплерстате**</span><span class="sxs-lookup"><span data-stu-id="713a4-110">Type: **SamplerState**</span></span>

<span data-ttu-id="713a4-111">Индекс выборки с отсчетом от нуля.</span><span class="sxs-lookup"><span data-stu-id="713a4-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="713a4-112">*Расположение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="713a4-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="713a4-113">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="713a4-113">Type: **float**</span></span>

<span data-ttu-id="713a4-114">Образцы координат (u, v).</span><span class="sxs-lookup"><span data-stu-id="713a4-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="713a4-115">*Смещение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="713a4-115">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="713a4-116">Тип: **int**</span><span class="sxs-lookup"><span data-stu-id="713a4-116">Type: **int**</span></span>

<span data-ttu-id="713a4-117">Смещение, применяемое к координатам текстуры перед выборкой.</span><span class="sxs-lookup"><span data-stu-id="713a4-117">The offset applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="713a4-118">*Состояние* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="713a4-118">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="713a4-119">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="713a4-119">Type: **uint**</span></span>

<span data-ttu-id="713a4-120">Состояние операции.</span><span class="sxs-lookup"><span data-stu-id="713a4-120">The status of the operation.</span></span> <span data-ttu-id="713a4-121">Вы не можете получить доступ к состоянию напрямую; Вместо этого передайте состояние в подставляемую функцию [**чеккакцессфуллимаппед**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="713a4-121">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="713a4-122">**Чеккакцессфуллимаппед** возвращает **значение true** , если все значения из соответствующего **образца**, **сбора** или операции **загрузки** обращались к сопоставленным плиткам в [мозаичном ресурсе](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="713a4-122">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="713a4-123">Если какие бы то ни было значения были взяты из несопоставленной плитки, **чеккакцессфуллимаппед** возвращает **значение false**.</span><span class="sxs-lookup"><span data-stu-id="713a4-123">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="713a4-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="713a4-124">Return value</span></span>

<span data-ttu-id="713a4-125">Тип: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="713a4-125">Type: **TemplateType**</span></span>

<span data-ttu-id="713a4-126">Значение из четырех компонентов, тип которого совпадает с типом шаблона.</span><span class="sxs-lookup"><span data-stu-id="713a4-126">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="713a4-127">Примечания</span><span class="sxs-lookup"><span data-stu-id="713a4-127">Remarks</span></span>

<span data-ttu-id="713a4-128">Примеры текстур можно использовать для интерполяции билинейной.</span><span class="sxs-lookup"><span data-stu-id="713a4-128">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="713a4-129">Эта функция поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="713a4-129">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="713a4-130">Вершина</span><span class="sxs-lookup"><span data-stu-id="713a4-130">Vertex</span></span> | <span data-ttu-id="713a4-131">Поверхности</span><span class="sxs-lookup"><span data-stu-id="713a4-131">Hull</span></span> | <span data-ttu-id="713a4-132">Домен</span><span class="sxs-lookup"><span data-stu-id="713a4-132">Domain</span></span> | <span data-ttu-id="713a4-133">Геометрия</span><span class="sxs-lookup"><span data-stu-id="713a4-133">Geometry</span></span> | <span data-ttu-id="713a4-134">Пиксель</span><span class="sxs-lookup"><span data-stu-id="713a4-134">Pixel</span></span> | <span data-ttu-id="713a4-135">Вычисления</span><span class="sxs-lookup"><span data-stu-id="713a4-135">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="713a4-136">x</span><span class="sxs-lookup"><span data-stu-id="713a4-136">x</span></span>      | <span data-ttu-id="713a4-137">x</span><span class="sxs-lookup"><span data-stu-id="713a4-137">x</span></span>    | <span data-ttu-id="713a4-138">x</span><span class="sxs-lookup"><span data-stu-id="713a4-138">x</span></span>      | <span data-ttu-id="713a4-139">x</span><span class="sxs-lookup"><span data-stu-id="713a4-139">x</span></span>        | <span data-ttu-id="713a4-140">x</span><span class="sxs-lookup"><span data-stu-id="713a4-140">x</span></span>     | <span data-ttu-id="713a4-141">x</span><span class="sxs-lookup"><span data-stu-id="713a4-141">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="713a4-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="713a4-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="713a4-143">Методы Гасерред</span><span class="sxs-lookup"><span data-stu-id="713a4-143">GatherRed methods</span></span>](texture2d-gatherred.md)
</dt> </dl>

 

 
