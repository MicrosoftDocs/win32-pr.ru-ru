---
title: 'Функция Текстурекубе:: Гасергрин (S, float, uint)'
description: 'Возвращает зеленые компоненты четырех значений шаг текселя, которые будут использоваться в операции линейной фильтрации, вместе с состоянием сопоставления плиток. | Функция Текстурекубе:: Гасергрин (S, float, uint)'
ms.assetid: DB0A6386-70ED-4D8C-A4EE-C058496D2F12
keywords:
- Функция Гасергрин HLSL
topic_type:
- apiref
api_name:
- GatherGreen
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1555b72b095ce0589a8ae9b396c67d29236db82c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104998218"
---
# <a name="texturecubegathergreensfloatuint-function"></a><span data-ttu-id="f03e4-105">Функция Текстурекубе:: Гасергрин (S, float, uint)</span><span class="sxs-lookup"><span data-stu-id="f03e4-105">TextureCube::GatherGreen(S,float,uint) function</span></span>

<span data-ttu-id="f03e4-106">Возвращает зеленые компоненты четырех значений шаг текселя, которые будут использоваться в операции линейной фильтрации, вместе с состоянием сопоставления плиток.</span><span class="sxs-lookup"><span data-stu-id="f03e4-106">Returns the green components of the four texel values that would be used in a bi-linear filtering operation, along with tile-mapping status.</span></span>

## <a name="syntax"></a><span data-ttu-id="f03e4-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f03e4-107">Syntax</span></span>


``` syntax
TemplateType GatherGreen(
  in  SamplerState S,
  in  float        Location,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="f03e4-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="f03e4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f03e4-109">*S* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="f03e4-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f03e4-110">Тип: **самплерстате**</span><span class="sxs-lookup"><span data-stu-id="f03e4-110">Type: **SamplerState**</span></span>

<span data-ttu-id="f03e4-111">Индекс выборки с отсчетом от нуля.</span><span class="sxs-lookup"><span data-stu-id="f03e4-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="f03e4-112">*Расположение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f03e4-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f03e4-113">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="f03e4-113">Type: **float**</span></span>

<span data-ttu-id="f03e4-114">Образцы координат (u, v).</span><span class="sxs-lookup"><span data-stu-id="f03e4-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="f03e4-115">*Состояние* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="f03e4-115">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f03e4-116">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="f03e4-116">Type: **uint**</span></span>

<span data-ttu-id="f03e4-117">Состояние операции.</span><span class="sxs-lookup"><span data-stu-id="f03e4-117">The status of the operation.</span></span> <span data-ttu-id="f03e4-118">Вы не можете получить доступ к состоянию напрямую; Вместо этого передайте состояние в подставляемую функцию [**чеккакцессфуллимаппед**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="f03e4-118">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="f03e4-119">**Чеккакцессфуллимаппед** возвращает **значение true** , если все значения из соответствующего **образца**, **сбора** или операции **загрузки** обращались к сопоставленным плиткам в [мозаичном ресурсе](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="f03e4-119">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="f03e4-120">Если какие бы то ни было значения были взяты из несопоставленной плитки, **чеккакцессфуллимаппед** возвращает **значение false**.</span><span class="sxs-lookup"><span data-stu-id="f03e4-120">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f03e4-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f03e4-121">Return value</span></span>

<span data-ttu-id="f03e4-122">Тип: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="f03e4-122">Type: **TemplateType**</span></span>

<span data-ttu-id="f03e4-123">Значение из четырех компонентов, тип которого совпадает с типом шаблона.</span><span class="sxs-lookup"><span data-stu-id="f03e4-123">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="f03e4-124">Примечания</span><span class="sxs-lookup"><span data-stu-id="f03e4-124">Remarks</span></span>

<span data-ttu-id="f03e4-125">Примеры текстур можно использовать для интерполяции билинейной.</span><span class="sxs-lookup"><span data-stu-id="f03e4-125">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="f03e4-126">Эта функция поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="f03e4-126">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="f03e4-127">Вершина</span><span class="sxs-lookup"><span data-stu-id="f03e4-127">Vertex</span></span> | <span data-ttu-id="f03e4-128">Поверхности</span><span class="sxs-lookup"><span data-stu-id="f03e4-128">Hull</span></span> | <span data-ttu-id="f03e4-129">Домен</span><span class="sxs-lookup"><span data-stu-id="f03e4-129">Domain</span></span> | <span data-ttu-id="f03e4-130">Геометрия</span><span class="sxs-lookup"><span data-stu-id="f03e4-130">Geometry</span></span> | <span data-ttu-id="f03e4-131">Пиксель</span><span class="sxs-lookup"><span data-stu-id="f03e4-131">Pixel</span></span> | <span data-ttu-id="f03e4-132">Вычисления</span><span class="sxs-lookup"><span data-stu-id="f03e4-132">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="f03e4-133">x</span><span class="sxs-lookup"><span data-stu-id="f03e4-133">x</span></span>      | <span data-ttu-id="f03e4-134">x</span><span class="sxs-lookup"><span data-stu-id="f03e4-134">x</span></span>    | <span data-ttu-id="f03e4-135">x</span><span class="sxs-lookup"><span data-stu-id="f03e4-135">x</span></span>      | <span data-ttu-id="f03e4-136">x</span><span class="sxs-lookup"><span data-stu-id="f03e4-136">x</span></span>        | <span data-ttu-id="f03e4-137">x</span><span class="sxs-lookup"><span data-stu-id="f03e4-137">x</span></span>     | <span data-ttu-id="f03e4-138">x</span><span class="sxs-lookup"><span data-stu-id="f03e4-138">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="f03e4-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f03e4-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f03e4-140">Методы Гасергрин</span><span class="sxs-lookup"><span data-stu-id="f03e4-140">GatherGreen methods</span></span>](texturecube-gathergreen.md)
</dt> <dt>

[<span data-ttu-id="f03e4-141">**текстурекубе**</span><span class="sxs-lookup"><span data-stu-id="f03e4-141">**TextureCube**</span></span>](texturecube.md)
</dt> </dl>

 

 
