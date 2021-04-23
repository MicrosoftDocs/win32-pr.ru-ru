---
title: 'Функция Текстурекубе:: Гасерблуе (S, float, uint)'
description: 'Возвращает синие компоненты четырех шаг текселя значений, которые будут использоваться в операции линейной фильтрации, вместе с состоянием сопоставления плиток. | Функция Текстурекубе:: Гасерблуе (S, float, uint)'
ms.assetid: B2099321-3E81-4A77-A023-AF73594C68C8
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
ms.openlocfilehash: 59378e3a5754dbd55298d6040b40076a9e54eb74
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986608"
---
# <a name="texturecubegatherbluesfloatuint-function"></a><span data-ttu-id="8ca0a-105">Функция Текстурекубе:: Гасерблуе (S, float, uint)</span><span class="sxs-lookup"><span data-stu-id="8ca0a-105">TextureCube::GatherBlue(S,float,uint) function</span></span>

<span data-ttu-id="8ca0a-106">Возвращает синие компоненты четырех шаг текселя значений, которые будут использоваться в операции линейной фильтрации, вместе с состоянием сопоставления плиток.</span><span class="sxs-lookup"><span data-stu-id="8ca0a-106">Returns the blue components of the four texel values that would be used in a bi-linear filtering operation, along with tile-mapping status.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ca0a-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8ca0a-107">Syntax</span></span>


``` syntax
TemplateType GatherBlue(
  in  SamplerState S,
  in  float        Location,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="8ca0a-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="8ca0a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ca0a-109">*S* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="8ca0a-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ca0a-110">Тип: **самплерстате**</span><span class="sxs-lookup"><span data-stu-id="8ca0a-110">Type: **SamplerState**</span></span>

<span data-ttu-id="8ca0a-111">Индекс выборки с отсчетом от нуля.</span><span class="sxs-lookup"><span data-stu-id="8ca0a-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="8ca0a-112">*Расположение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8ca0a-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ca0a-113">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="8ca0a-113">Type: **float**</span></span>

<span data-ttu-id="8ca0a-114">Образцы координат (u, v).</span><span class="sxs-lookup"><span data-stu-id="8ca0a-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="8ca0a-115">*Состояние* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="8ca0a-115">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8ca0a-116">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="8ca0a-116">Type: **uint**</span></span>

<span data-ttu-id="8ca0a-117">Состояние операции.</span><span class="sxs-lookup"><span data-stu-id="8ca0a-117">The status of the operation.</span></span> <span data-ttu-id="8ca0a-118">Вы не можете получить доступ к состоянию напрямую; Вместо этого передайте состояние в подставляемую функцию [**чеккакцессфуллимаппед**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="8ca0a-118">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="8ca0a-119">**Чеккакцессфуллимаппед** возвращает **значение true** , если все значения из соответствующего **образца**, **сбора** или операции **загрузки** обращались к сопоставленным плиткам в [мозаичном ресурсе](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="8ca0a-119">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="8ca0a-120">Если какие бы то ни было значения были взяты из несопоставленной плитки, **чеккакцессфуллимаппед** возвращает **значение false**.</span><span class="sxs-lookup"><span data-stu-id="8ca0a-120">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ca0a-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8ca0a-121">Return value</span></span>

<span data-ttu-id="8ca0a-122">Тип: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="8ca0a-122">Type: **TemplateType**</span></span>

<span data-ttu-id="8ca0a-123">Значение из четырех компонентов, тип которого совпадает с типом шаблона.</span><span class="sxs-lookup"><span data-stu-id="8ca0a-123">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="8ca0a-124">Примечания</span><span class="sxs-lookup"><span data-stu-id="8ca0a-124">Remarks</span></span>

<span data-ttu-id="8ca0a-125">Примеры текстур можно использовать для интерполяции билинейной.</span><span class="sxs-lookup"><span data-stu-id="8ca0a-125">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="8ca0a-126">Эта функция поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="8ca0a-126">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="8ca0a-127">Вершина</span><span class="sxs-lookup"><span data-stu-id="8ca0a-127">Vertex</span></span> | <span data-ttu-id="8ca0a-128">Поверхности</span><span class="sxs-lookup"><span data-stu-id="8ca0a-128">Hull</span></span> | <span data-ttu-id="8ca0a-129">Домен</span><span class="sxs-lookup"><span data-stu-id="8ca0a-129">Domain</span></span> | <span data-ttu-id="8ca0a-130">Геометрия</span><span class="sxs-lookup"><span data-stu-id="8ca0a-130">Geometry</span></span> | <span data-ttu-id="8ca0a-131">Пиксель</span><span class="sxs-lookup"><span data-stu-id="8ca0a-131">Pixel</span></span> | <span data-ttu-id="8ca0a-132">Вычисления</span><span class="sxs-lookup"><span data-stu-id="8ca0a-132">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="8ca0a-133">x</span><span class="sxs-lookup"><span data-stu-id="8ca0a-133">x</span></span>      | <span data-ttu-id="8ca0a-134">x</span><span class="sxs-lookup"><span data-stu-id="8ca0a-134">x</span></span>    | <span data-ttu-id="8ca0a-135">x</span><span class="sxs-lookup"><span data-stu-id="8ca0a-135">x</span></span>      | <span data-ttu-id="8ca0a-136">x</span><span class="sxs-lookup"><span data-stu-id="8ca0a-136">x</span></span>        | <span data-ttu-id="8ca0a-137">x</span><span class="sxs-lookup"><span data-stu-id="8ca0a-137">x</span></span>     | <span data-ttu-id="8ca0a-138">x</span><span class="sxs-lookup"><span data-stu-id="8ca0a-138">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="8ca0a-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8ca0a-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ca0a-140">Методы Гасерблуе</span><span class="sxs-lookup"><span data-stu-id="8ca0a-140">GatherBlue methods</span></span>](texturecube-gatherblue.md)
</dt> <dt>

[<span data-ttu-id="8ca0a-141">**текстурекубе**</span><span class="sxs-lookup"><span data-stu-id="8ca0a-141">**TextureCube**</span></span>](texturecube.md)
</dt> </dl>

 

 
