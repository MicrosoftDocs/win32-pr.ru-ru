---
title: 'Функция Текстурекубеаррай:: Гасералфа (S, float, uint)'
description: 'Возвращает альфа-компоненты четырех значений шаг текселя, которые будут использоваться в операции линейной фильтрации, а также состояние сопоставления плиток. | Функция Текстурекубеаррай:: Гасералфа (S, float, uint)'
ms.assetid: C6AF896A-C68E-44EA-A779-DD9DBA30A039
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
ms.openlocfilehash: c1f9b692d81f6e26753496bb58ac114145ed21de
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104547690"
---
# <a name="texturecubearraygatheralphasfloatuint-function"></a><span data-ttu-id="6bce8-105">Функция Текстурекубеаррай:: Гасералфа (S, float, uint)</span><span class="sxs-lookup"><span data-stu-id="6bce8-105">TextureCubeArray::GatherAlpha(S,float,uint) function</span></span>

<span data-ttu-id="6bce8-106">Возвращает альфа-компоненты четырех значений шаг текселя, которые будут использоваться в операции линейной фильтрации, а также состояние сопоставления плиток.</span><span class="sxs-lookup"><span data-stu-id="6bce8-106">Returns the alpha components of the four texel values that would be used in a bi-linear filtering operation, along with tile-mapping status.</span></span>

## <a name="syntax"></a><span data-ttu-id="6bce8-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6bce8-107">Syntax</span></span>


``` syntax
TemplateType GatherAlpha(
  in  SamplerState S,
  in  float        Location,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="6bce8-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="6bce8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6bce8-109">*S* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="6bce8-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6bce8-110">Тип: **самплерстате**</span><span class="sxs-lookup"><span data-stu-id="6bce8-110">Type: **SamplerState**</span></span>

<span data-ttu-id="6bce8-111">Индекс выборки с отсчетом от нуля.</span><span class="sxs-lookup"><span data-stu-id="6bce8-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="6bce8-112">*Расположение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6bce8-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6bce8-113">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="6bce8-113">Type: **float**</span></span>

<span data-ttu-id="6bce8-114">Образцы координат (u, v).</span><span class="sxs-lookup"><span data-stu-id="6bce8-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="6bce8-115">*Состояние* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="6bce8-115">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6bce8-116">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="6bce8-116">Type: **uint**</span></span>

<span data-ttu-id="6bce8-117">Состояние операции.</span><span class="sxs-lookup"><span data-stu-id="6bce8-117">The status of the operation.</span></span> <span data-ttu-id="6bce8-118">Вы не можете получить доступ к состоянию напрямую; Вместо этого передайте состояние в подставляемую функцию [**чеккакцессфуллимаппед**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="6bce8-118">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="6bce8-119">**Чеккакцессфуллимаппед** возвращает **значение true** , если все значения из соответствующего **образца**, **сбора** или операции **загрузки** обращались к сопоставленным плиткам в [мозаичном ресурсе](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="6bce8-119">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="6bce8-120">Если какие бы то ни было значения были взяты из несопоставленной плитки, **чеккакцессфуллимаппед** возвращает **значение false**.</span><span class="sxs-lookup"><span data-stu-id="6bce8-120">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6bce8-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6bce8-121">Return value</span></span>

<span data-ttu-id="6bce8-122">Тип: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="6bce8-122">Type: **TemplateType**</span></span>

<span data-ttu-id="6bce8-123">Значение из четырех компонентов, тип которого совпадает с типом шаблона.</span><span class="sxs-lookup"><span data-stu-id="6bce8-123">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="6bce8-124">Примечания</span><span class="sxs-lookup"><span data-stu-id="6bce8-124">Remarks</span></span>

<span data-ttu-id="6bce8-125">Примеры текстур можно использовать для интерполяции билинейной.</span><span class="sxs-lookup"><span data-stu-id="6bce8-125">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="6bce8-126">Эта функция поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="6bce8-126">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="6bce8-127">Вершина</span><span class="sxs-lookup"><span data-stu-id="6bce8-127">Vertex</span></span> | <span data-ttu-id="6bce8-128">Поверхности</span><span class="sxs-lookup"><span data-stu-id="6bce8-128">Hull</span></span> | <span data-ttu-id="6bce8-129">Домен</span><span class="sxs-lookup"><span data-stu-id="6bce8-129">Domain</span></span> | <span data-ttu-id="6bce8-130">Геометрия</span><span class="sxs-lookup"><span data-stu-id="6bce8-130">Geometry</span></span> | <span data-ttu-id="6bce8-131">Пиксель</span><span class="sxs-lookup"><span data-stu-id="6bce8-131">Pixel</span></span> | <span data-ttu-id="6bce8-132">Вычисления</span><span class="sxs-lookup"><span data-stu-id="6bce8-132">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="6bce8-133">x</span><span class="sxs-lookup"><span data-stu-id="6bce8-133">x</span></span>      | <span data-ttu-id="6bce8-134">x</span><span class="sxs-lookup"><span data-stu-id="6bce8-134">x</span></span>    | <span data-ttu-id="6bce8-135">x</span><span class="sxs-lookup"><span data-stu-id="6bce8-135">x</span></span>      | <span data-ttu-id="6bce8-136">x</span><span class="sxs-lookup"><span data-stu-id="6bce8-136">x</span></span>        | <span data-ttu-id="6bce8-137">x</span><span class="sxs-lookup"><span data-stu-id="6bce8-137">x</span></span>     | <span data-ttu-id="6bce8-138">x</span><span class="sxs-lookup"><span data-stu-id="6bce8-138">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="6bce8-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6bce8-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6bce8-140">Методы Гасералфа</span><span class="sxs-lookup"><span data-stu-id="6bce8-140">GatherAlpha methods</span></span>](texturecubearray-gatheralpha.md)
</dt> <dt>

[<span data-ttu-id="6bce8-141">**текстурекубеаррай**</span><span class="sxs-lookup"><span data-stu-id="6bce8-141">**TextureCubeArray**</span></span>](texturecubearray.md)
</dt> </dl>

 

 
