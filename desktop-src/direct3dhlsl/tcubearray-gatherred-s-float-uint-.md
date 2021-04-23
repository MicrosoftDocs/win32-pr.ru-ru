---
title: 'Функция Текстурекубеаррай:: Гасерред (S, float, uint)'
description: 'Возвращает красные компоненты четырех значений шаг текселя, которые будут использоваться в операции линейной фильтрации, вместе с состоянием сопоставления плиток. | Функция Текстурекубеаррай:: Гасерред (S, float, uint)'
ms.assetid: 9776A4B5-6DDB-4B9F-96CD-F97B8908B057
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
ms.openlocfilehash: 90c6c69b8598222139a39752aefc39a0a125df2a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104352642"
---
# <a name="texturecubearraygatherredsfloatuint-function"></a><span data-ttu-id="a0a25-105">Функция Текстурекубеаррай:: Гасерред (S, float, uint)</span><span class="sxs-lookup"><span data-stu-id="a0a25-105">TextureCubeArray::GatherRed(S,float,uint) function</span></span>

<span data-ttu-id="a0a25-106">Возвращает красные компоненты четырех значений шаг текселя, которые будут использоваться в операции линейной фильтрации, вместе с состоянием сопоставления плиток.</span><span class="sxs-lookup"><span data-stu-id="a0a25-106">Returns the red components of the four texel values that would be used in a bi-linear filtering operation, along with tile-mapping status.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0a25-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a0a25-107">Syntax</span></span>


``` syntax
TemplateType GatherRed(
  in  SamplerState S,
  in  float        Location,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="a0a25-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="a0a25-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0a25-109">*S* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="a0a25-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0a25-110">Тип: **самплерстате**</span><span class="sxs-lookup"><span data-stu-id="a0a25-110">Type: **SamplerState**</span></span>

<span data-ttu-id="a0a25-111">Индекс выборки с отсчетом от нуля.</span><span class="sxs-lookup"><span data-stu-id="a0a25-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="a0a25-112">*Расположение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a0a25-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0a25-113">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="a0a25-113">Type: **float**</span></span>

<span data-ttu-id="a0a25-114">Образцы координат (u, v).</span><span class="sxs-lookup"><span data-stu-id="a0a25-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="a0a25-115">*Состояние* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="a0a25-115">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a0a25-116">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="a0a25-116">Type: **uint**</span></span>

<span data-ttu-id="a0a25-117">Состояние операции.</span><span class="sxs-lookup"><span data-stu-id="a0a25-117">The status of the operation.</span></span> <span data-ttu-id="a0a25-118">Вы не можете получить доступ к состоянию напрямую; Вместо этого передайте состояние в подставляемую функцию [**чеккакцессфуллимаппед**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="a0a25-118">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="a0a25-119">**Чеккакцессфуллимаппед** возвращает **значение true** , если все значения из соответствующего **образца**, **сбора** или операции **загрузки** обращались к сопоставленным плиткам в [мозаичном ресурсе](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="a0a25-119">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="a0a25-120">Если какие бы то ни было значения были взяты из несопоставленной плитки, **чеккакцессфуллимаппед** возвращает **значение false**.</span><span class="sxs-lookup"><span data-stu-id="a0a25-120">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0a25-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a0a25-121">Return value</span></span>

<span data-ttu-id="a0a25-122">Тип: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="a0a25-122">Type: **TemplateType**</span></span>

<span data-ttu-id="a0a25-123">Значение из четырех компонентов, тип которого совпадает с типом шаблона.</span><span class="sxs-lookup"><span data-stu-id="a0a25-123">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="a0a25-124">Примечания</span><span class="sxs-lookup"><span data-stu-id="a0a25-124">Remarks</span></span>

<span data-ttu-id="a0a25-125">Примеры текстур можно использовать для интерполяции билинейной.</span><span class="sxs-lookup"><span data-stu-id="a0a25-125">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="a0a25-126">Эта функция поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="a0a25-126">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="a0a25-127">Вершина</span><span class="sxs-lookup"><span data-stu-id="a0a25-127">Vertex</span></span> | <span data-ttu-id="a0a25-128">Поверхности</span><span class="sxs-lookup"><span data-stu-id="a0a25-128">Hull</span></span> | <span data-ttu-id="a0a25-129">Домен</span><span class="sxs-lookup"><span data-stu-id="a0a25-129">Domain</span></span> | <span data-ttu-id="a0a25-130">Геометрия</span><span class="sxs-lookup"><span data-stu-id="a0a25-130">Geometry</span></span> | <span data-ttu-id="a0a25-131">Пиксель</span><span class="sxs-lookup"><span data-stu-id="a0a25-131">Pixel</span></span> | <span data-ttu-id="a0a25-132">Вычисления</span><span class="sxs-lookup"><span data-stu-id="a0a25-132">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="a0a25-133">x</span><span class="sxs-lookup"><span data-stu-id="a0a25-133">x</span></span>      | <span data-ttu-id="a0a25-134">x</span><span class="sxs-lookup"><span data-stu-id="a0a25-134">x</span></span>    | <span data-ttu-id="a0a25-135">x</span><span class="sxs-lookup"><span data-stu-id="a0a25-135">x</span></span>      | <span data-ttu-id="a0a25-136">x</span><span class="sxs-lookup"><span data-stu-id="a0a25-136">x</span></span>        | <span data-ttu-id="a0a25-137">x</span><span class="sxs-lookup"><span data-stu-id="a0a25-137">x</span></span>     | <span data-ttu-id="a0a25-138">x</span><span class="sxs-lookup"><span data-stu-id="a0a25-138">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="a0a25-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a0a25-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0a25-140">Методы Гасерред</span><span class="sxs-lookup"><span data-stu-id="a0a25-140">GatherRed methods</span></span>](texturecubearray-gatherred.md)
</dt> <dt>

[<span data-ttu-id="a0a25-141">**текстурекубеаррай**</span><span class="sxs-lookup"><span data-stu-id="a0a25-141">**TextureCubeArray**</span></span>](texturecubearray.md)
</dt> </dl>

 

 
