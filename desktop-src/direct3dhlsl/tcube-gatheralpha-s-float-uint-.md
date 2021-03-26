---
title: 'Функция Текстурекубе:: Гасералфа (S, float, uint)'
description: 'Возвращает альфа-компоненты четырех значений шаг текселя, которые будут использоваться в операции линейной фильтрации, а также состояние сопоставления плиток. | Функция Текстурекубе:: Гасералфа (S, float, uint)'
ms.assetid: 19BD3024-D3E5-4AEA-8C8E-510A4EB527B5
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
ms.openlocfilehash: b915cde61309a64b77309e375284a4e5d9343724
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986345"
---
# <a name="texturecubegatheralphasfloatuint-function"></a><span data-ttu-id="734e1-105">Функция Текстурекубе:: Гасералфа (S, float, uint)</span><span class="sxs-lookup"><span data-stu-id="734e1-105">TextureCube::GatherAlpha(S,float,uint) function</span></span>

<span data-ttu-id="734e1-106">Возвращает альфа-компоненты четырех значений шаг текселя, которые будут использоваться в операции линейной фильтрации, а также состояние сопоставления плиток.</span><span class="sxs-lookup"><span data-stu-id="734e1-106">Returns the alpha components of the four texel values that would be used in a bi-linear filtering operation, along with tile-mapping status.</span></span>

## <a name="syntax"></a><span data-ttu-id="734e1-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="734e1-107">Syntax</span></span>


``` syntax
TemplateType GatherAlpha(
  in  SamplerState S,
  in  float        Location,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="734e1-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="734e1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="734e1-109">*S* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="734e1-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="734e1-110">Тип: **самплерстате**</span><span class="sxs-lookup"><span data-stu-id="734e1-110">Type: **SamplerState**</span></span>

<span data-ttu-id="734e1-111">Индекс выборки с отсчетом от нуля.</span><span class="sxs-lookup"><span data-stu-id="734e1-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="734e1-112">*Расположение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="734e1-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="734e1-113">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="734e1-113">Type: **float**</span></span>

<span data-ttu-id="734e1-114">Образцы координат (u, v).</span><span class="sxs-lookup"><span data-stu-id="734e1-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="734e1-115">*Состояние* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="734e1-115">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="734e1-116">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="734e1-116">Type: **uint**</span></span>

<span data-ttu-id="734e1-117">Состояние операции.</span><span class="sxs-lookup"><span data-stu-id="734e1-117">The status of the operation.</span></span> <span data-ttu-id="734e1-118">Вы не можете получить доступ к состоянию напрямую; Вместо этого передайте состояние в подставляемую функцию [**чеккакцессфуллимаппед**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="734e1-118">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="734e1-119">**Чеккакцессфуллимаппед** возвращает **значение true** , если все значения из соответствующего **образца**, **сбора** или операции **загрузки** обращались к сопоставленным плиткам в [мозаичном ресурсе](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="734e1-119">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="734e1-120">Если какие бы то ни было значения были взяты из несопоставленной плитки, **чеккакцессфуллимаппед** возвращает **значение false**.</span><span class="sxs-lookup"><span data-stu-id="734e1-120">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="734e1-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="734e1-121">Return value</span></span>

<span data-ttu-id="734e1-122">Тип: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="734e1-122">Type: **TemplateType**</span></span>

<span data-ttu-id="734e1-123">Значение из четырех компонентов, тип которого совпадает с типом шаблона.</span><span class="sxs-lookup"><span data-stu-id="734e1-123">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="734e1-124">Примечания</span><span class="sxs-lookup"><span data-stu-id="734e1-124">Remarks</span></span>

<span data-ttu-id="734e1-125">Примеры текстур можно использовать для интерполяции билинейной.</span><span class="sxs-lookup"><span data-stu-id="734e1-125">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="734e1-126">Эта функция поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="734e1-126">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="734e1-127">Вершина</span><span class="sxs-lookup"><span data-stu-id="734e1-127">Vertex</span></span> | <span data-ttu-id="734e1-128">Поверхности</span><span class="sxs-lookup"><span data-stu-id="734e1-128">Hull</span></span> | <span data-ttu-id="734e1-129">Домен</span><span class="sxs-lookup"><span data-stu-id="734e1-129">Domain</span></span> | <span data-ttu-id="734e1-130">Геометрия</span><span class="sxs-lookup"><span data-stu-id="734e1-130">Geometry</span></span> | <span data-ttu-id="734e1-131">Пиксель</span><span class="sxs-lookup"><span data-stu-id="734e1-131">Pixel</span></span> | <span data-ttu-id="734e1-132">Вычисления</span><span class="sxs-lookup"><span data-stu-id="734e1-132">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="734e1-133">x</span><span class="sxs-lookup"><span data-stu-id="734e1-133">x</span></span>      | <span data-ttu-id="734e1-134">x</span><span class="sxs-lookup"><span data-stu-id="734e1-134">x</span></span>    | <span data-ttu-id="734e1-135">x</span><span class="sxs-lookup"><span data-stu-id="734e1-135">x</span></span>      | <span data-ttu-id="734e1-136">x</span><span class="sxs-lookup"><span data-stu-id="734e1-136">x</span></span>        | <span data-ttu-id="734e1-137">x</span><span class="sxs-lookup"><span data-stu-id="734e1-137">x</span></span>     | <span data-ttu-id="734e1-138">x</span><span class="sxs-lookup"><span data-stu-id="734e1-138">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="734e1-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="734e1-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="734e1-140">Методы Гасералфа</span><span class="sxs-lookup"><span data-stu-id="734e1-140">GatherAlpha methods</span></span>](texturecube-gatheralpha.md)
</dt> <dt>

[<span data-ttu-id="734e1-141">**текстурекубе**</span><span class="sxs-lookup"><span data-stu-id="734e1-141">**TextureCube**</span></span>](texturecube.md)
</dt> </dl>

 

 
