---
title: 'Функция Texture2DArray:: Гасерред (S, float, int, uint)'
description: 'Возвращает красные компоненты четырех значений шаг текселя, которые будут использоваться в операции линейной фильтрации, вместе с состоянием сопоставления плиток. | Функция Texture2DArray:: Гасерред (S, float, int, uint)'
ms.assetid: 9FAFB594-5844-4A2D-9B45-7973B5F85E13
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
ms.openlocfilehash: 7fdd250cb25f6085100bb88204cae6e67a3fc0b3
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "103820781"
---
# <a name="texture2darraygatherredsfloatintuint-function"></a><span data-ttu-id="2b646-105">Функция Texture2DArray:: Гасерред (S, float, int, uint)</span><span class="sxs-lookup"><span data-stu-id="2b646-105">Texture2DArray::GatherRed(S,float,int,uint) function</span></span>

<span data-ttu-id="2b646-106">Возвращает красные компоненты четырех значений шаг текселя, которые будут использоваться в операции линейной фильтрации, вместе с состоянием сопоставления плиток.</span><span class="sxs-lookup"><span data-stu-id="2b646-106">Returns the red components of the four texel values that would be used in a bi-linear filtering operation, along with tile-mapping status.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b646-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2b646-107">Syntax</span></span>


``` syntax
TemplateType GatherRed(
  in  SamplerState S,
  in  float        Location,
  in  int          Offset,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="2b646-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="2b646-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b646-109">*S* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="2b646-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b646-110">Тип: **самплерстате**</span><span class="sxs-lookup"><span data-stu-id="2b646-110">Type: **SamplerState**</span></span>

<span data-ttu-id="2b646-111">Индекс выборки с отсчетом от нуля.</span><span class="sxs-lookup"><span data-stu-id="2b646-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="2b646-112">*Расположение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2b646-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b646-113">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="2b646-113">Type: **float**</span></span>

<span data-ttu-id="2b646-114">Образцы координат (u, v).</span><span class="sxs-lookup"><span data-stu-id="2b646-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="2b646-115">*Смещение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2b646-115">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b646-116">Тип: **int**</span><span class="sxs-lookup"><span data-stu-id="2b646-116">Type: **int**</span></span>

<span data-ttu-id="2b646-117">Смещение, применяемое к координатам текстуры перед выборкой.</span><span class="sxs-lookup"><span data-stu-id="2b646-117">The offset applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="2b646-118">*Состояние* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="2b646-118">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2b646-119">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="2b646-119">Type: **uint**</span></span>

<span data-ttu-id="2b646-120">Состояние операции.</span><span class="sxs-lookup"><span data-stu-id="2b646-120">The status of the operation.</span></span> <span data-ttu-id="2b646-121">Вы не можете получить доступ к состоянию напрямую; Вместо этого передайте состояние в подставляемую функцию [**чеккакцессфуллимаппед**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="2b646-121">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="2b646-122">**Чеккакцессфуллимаппед** возвращает **значение true** , если все значения из соответствующего **образца**, **сбора** или операции **загрузки** обращались к сопоставленным плиткам в [мозаичном ресурсе](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="2b646-122">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="2b646-123">Если какие бы то ни было значения были взяты из несопоставленной плитки, **чеккакцессфуллимаппед** возвращает **значение false**.</span><span class="sxs-lookup"><span data-stu-id="2b646-123">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2b646-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2b646-124">Return value</span></span>

<span data-ttu-id="2b646-125">Тип: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="2b646-125">Type: **TemplateType**</span></span>

<span data-ttu-id="2b646-126">Значение из четырех компонентов, тип которого совпадает с типом шаблона.</span><span class="sxs-lookup"><span data-stu-id="2b646-126">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="2b646-127">Примечания</span><span class="sxs-lookup"><span data-stu-id="2b646-127">Remarks</span></span>

<span data-ttu-id="2b646-128">Примеры текстур можно использовать для интерполяции билинейной.</span><span class="sxs-lookup"><span data-stu-id="2b646-128">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="2b646-129">Эта функция поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="2b646-129">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="2b646-130">Вершина</span><span class="sxs-lookup"><span data-stu-id="2b646-130">Vertex</span></span> | <span data-ttu-id="2b646-131">Поверхности</span><span class="sxs-lookup"><span data-stu-id="2b646-131">Hull</span></span> | <span data-ttu-id="2b646-132">Домен</span><span class="sxs-lookup"><span data-stu-id="2b646-132">Domain</span></span> | <span data-ttu-id="2b646-133">Геометрия</span><span class="sxs-lookup"><span data-stu-id="2b646-133">Geometry</span></span> | <span data-ttu-id="2b646-134">Пиксель</span><span class="sxs-lookup"><span data-stu-id="2b646-134">Pixel</span></span> | <span data-ttu-id="2b646-135">Вычисления</span><span class="sxs-lookup"><span data-stu-id="2b646-135">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="2b646-136">x</span><span class="sxs-lookup"><span data-stu-id="2b646-136">x</span></span>      | <span data-ttu-id="2b646-137">x</span><span class="sxs-lookup"><span data-stu-id="2b646-137">x</span></span>    | <span data-ttu-id="2b646-138">x</span><span class="sxs-lookup"><span data-stu-id="2b646-138">x</span></span>      | <span data-ttu-id="2b646-139">x</span><span class="sxs-lookup"><span data-stu-id="2b646-139">x</span></span>        | <span data-ttu-id="2b646-140">x</span><span class="sxs-lookup"><span data-stu-id="2b646-140">x</span></span>     | <span data-ttu-id="2b646-141">x</span><span class="sxs-lookup"><span data-stu-id="2b646-141">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="2b646-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2b646-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b646-143">Методы Гасерред</span><span class="sxs-lookup"><span data-stu-id="2b646-143">GatherRed methods</span></span>](texture2darray-gatherred.md)
</dt> </dl>

 

 
