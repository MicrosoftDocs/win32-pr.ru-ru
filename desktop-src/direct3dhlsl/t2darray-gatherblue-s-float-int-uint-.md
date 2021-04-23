---
title: 'Функция Texture2DArray:: Гасерблуе (S, float, int, uint)'
description: 'Возвращает синие компоненты четырех шаг текселя значений, которые будут использоваться в операции линейной фильтрации, вместе с состоянием сопоставления плиток. | Функция Texture2DArray:: Гасерблуе (S, float, int, uint)'
ms.assetid: A0745768-EE92-4036-84F5-2699D26441B3
keywords:
- Функция Гасерблуе HLSL
topic_type:
- apiref
api_name:
- GatherBlue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ef02cec318b9362b37bb83c02e4712bb0bec5d59
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986500"
---
# <a name="texture2darraygatherbluesfloatintuint-function"></a><span data-ttu-id="f223d-105">Функция Texture2DArray:: Гасерблуе (S, float, int, uint)</span><span class="sxs-lookup"><span data-stu-id="f223d-105">Texture2DArray::GatherBlue(S,float,int,uint) function</span></span>

<span data-ttu-id="f223d-106">Возвращает синие компоненты четырех шаг текселя значений, которые будут использоваться в операции линейной фильтрации, вместе с состоянием сопоставления плиток.</span><span class="sxs-lookup"><span data-stu-id="f223d-106">Returns the blue components of the four texel values that would be used in a bi-linear filtering operation, along with tile-mapping status.</span></span>

## <a name="syntax"></a><span data-ttu-id="f223d-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f223d-107">Syntax</span></span>


``` syntax
TemplateType GatherBlue(
  in  SamplerState S,
  in  float        Location,
  in  int          Offset,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="f223d-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="f223d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f223d-109">*S* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="f223d-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f223d-110">Тип: **самплерстате**</span><span class="sxs-lookup"><span data-stu-id="f223d-110">Type: **SamplerState**</span></span>

<span data-ttu-id="f223d-111">Индекс выборки с отсчетом от нуля.</span><span class="sxs-lookup"><span data-stu-id="f223d-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="f223d-112">*Расположение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f223d-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f223d-113">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="f223d-113">Type: **float**</span></span>

<span data-ttu-id="f223d-114">Образцы координат (u, v).</span><span class="sxs-lookup"><span data-stu-id="f223d-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="f223d-115">*Смещение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f223d-115">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f223d-116">Тип: **int**</span><span class="sxs-lookup"><span data-stu-id="f223d-116">Type: **int**</span></span>

<span data-ttu-id="f223d-117">Смещение, применяемое к координатам текстуры перед выборкой.</span><span class="sxs-lookup"><span data-stu-id="f223d-117">The offset applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="f223d-118">*Состояние* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="f223d-118">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f223d-119">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="f223d-119">Type: **uint**</span></span>

<span data-ttu-id="f223d-120">Состояние операции.</span><span class="sxs-lookup"><span data-stu-id="f223d-120">The status of the operation.</span></span> <span data-ttu-id="f223d-121">Вы не можете получить доступ к состоянию напрямую; Вместо этого передайте состояние в подставляемую функцию [**чеккакцессфуллимаппед**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="f223d-121">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="f223d-122">**Чеккакцессфуллимаппед** возвращает **значение true** , если все значения из соответствующего **образца**, **сбора** или операции **загрузки** обращались к сопоставленным плиткам в [мозаичном ресурсе](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="f223d-122">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="f223d-123">Если какие бы то ни было значения были взяты из несопоставленной плитки, **чеккакцессфуллимаппед** возвращает **значение false**.</span><span class="sxs-lookup"><span data-stu-id="f223d-123">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f223d-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f223d-124">Return value</span></span>

<span data-ttu-id="f223d-125">Тип: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="f223d-125">Type: **TemplateType**</span></span>

<span data-ttu-id="f223d-126">Значение из четырех компонентов, тип которого совпадает с типом шаблона.</span><span class="sxs-lookup"><span data-stu-id="f223d-126">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="f223d-127">Примечания</span><span class="sxs-lookup"><span data-stu-id="f223d-127">Remarks</span></span>

<span data-ttu-id="f223d-128">Примеры текстур можно использовать для интерполяции билинейной.</span><span class="sxs-lookup"><span data-stu-id="f223d-128">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="f223d-129">Эта функция поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="f223d-129">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="f223d-130">Вершина</span><span class="sxs-lookup"><span data-stu-id="f223d-130">Vertex</span></span> | <span data-ttu-id="f223d-131">Поверхности</span><span class="sxs-lookup"><span data-stu-id="f223d-131">Hull</span></span> | <span data-ttu-id="f223d-132">Домен</span><span class="sxs-lookup"><span data-stu-id="f223d-132">Domain</span></span> | <span data-ttu-id="f223d-133">Геометрия</span><span class="sxs-lookup"><span data-stu-id="f223d-133">Geometry</span></span> | <span data-ttu-id="f223d-134">Пиксель</span><span class="sxs-lookup"><span data-stu-id="f223d-134">Pixel</span></span> | <span data-ttu-id="f223d-135">Вычисления</span><span class="sxs-lookup"><span data-stu-id="f223d-135">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="f223d-136">x</span><span class="sxs-lookup"><span data-stu-id="f223d-136">x</span></span>      | <span data-ttu-id="f223d-137">x</span><span class="sxs-lookup"><span data-stu-id="f223d-137">x</span></span>    | <span data-ttu-id="f223d-138">x</span><span class="sxs-lookup"><span data-stu-id="f223d-138">x</span></span>      | <span data-ttu-id="f223d-139">x</span><span class="sxs-lookup"><span data-stu-id="f223d-139">x</span></span>        | <span data-ttu-id="f223d-140">x</span><span class="sxs-lookup"><span data-stu-id="f223d-140">x</span></span>     | <span data-ttu-id="f223d-141">x</span><span class="sxs-lookup"><span data-stu-id="f223d-141">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="f223d-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f223d-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f223d-143">Методы Гасерблуе</span><span class="sxs-lookup"><span data-stu-id="f223d-143">GatherBlue methods</span></span>](texture2darray-gatherblue.md)
</dt> </dl>

 

 
