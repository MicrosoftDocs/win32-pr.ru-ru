---
title: 'Функция Texture2DArray:: Гасералфа (S, float, int, uint)'
description: 'Возвращает четыре значения шаг текселя, которые будут использоваться в операции линейной фильтрации, вместе с состоянием сопоставления плиток. | Функция Texture2DArray:: Гасералфа (S, float, int, uint)'
ms.assetid: B04F29A7-0EC9-49F0-9662-00F1DD0F3E5B
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
ms.openlocfilehash: 59f5ead36b4880ba02fc50691e634fc477efea6f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104000147"
---
# <a name="texture2darraygatheralphasfloatintuint-function"></a><span data-ttu-id="8e947-105">Функция Texture2DArray:: Гасералфа (S, float, int, uint)</span><span class="sxs-lookup"><span data-stu-id="8e947-105">Texture2DArray::GatherAlpha(S,float,int,uint) function</span></span>

<span data-ttu-id="8e947-106">Возвращает четыре значения шаг текселя, которые будут использоваться в операции линейной фильтрации, вместе с состоянием сопоставления плиток.</span><span class="sxs-lookup"><span data-stu-id="8e947-106">Returns the four texel values that would be used in a bi-linear filtering operation, along with tile-mapping status.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e947-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8e947-107">Syntax</span></span>


``` syntax
TemplateType GatherAlpha(
  in  SamplerState S,
  in  float        Location,
  in  int          Offset,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="8e947-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="8e947-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e947-109">*S* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="8e947-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e947-110">Тип: **самплерстате**</span><span class="sxs-lookup"><span data-stu-id="8e947-110">Type: **SamplerState**</span></span>

<span data-ttu-id="8e947-111">Индекс выборки с отсчетом от нуля.</span><span class="sxs-lookup"><span data-stu-id="8e947-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="8e947-112">*Расположение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8e947-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e947-113">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="8e947-113">Type: **float**</span></span>

<span data-ttu-id="8e947-114">Образцы координат (u, v).</span><span class="sxs-lookup"><span data-stu-id="8e947-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="8e947-115">*Смещение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8e947-115">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e947-116">Тип: **int**</span><span class="sxs-lookup"><span data-stu-id="8e947-116">Type: **int**</span></span>

<span data-ttu-id="8e947-117">Смещение, применяемое к координатам текстуры перед выборкой.</span><span class="sxs-lookup"><span data-stu-id="8e947-117">The offset applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="8e947-118">*Состояние* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="8e947-118">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8e947-119">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="8e947-119">Type: **uint**</span></span>

<span data-ttu-id="8e947-120">Состояние операции.</span><span class="sxs-lookup"><span data-stu-id="8e947-120">The status of the operation.</span></span> <span data-ttu-id="8e947-121">Вы не можете получить доступ к состоянию напрямую; Вместо этого передайте состояние в подставляемую функцию [**чеккакцессфуллимаппед**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="8e947-121">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="8e947-122">**Чеккакцессфуллимаппед** возвращает **значение true** , если все значения из соответствующего **образца**, **сбора** или операции **загрузки** обращались к сопоставленным плиткам в [мозаичном ресурсе](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="8e947-122">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="8e947-123">Если какие бы то ни было значения были взяты из несопоставленной плитки, **чеккакцессфуллимаппед** возвращает **значение false**.</span><span class="sxs-lookup"><span data-stu-id="8e947-123">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8e947-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8e947-124">Return value</span></span>

<span data-ttu-id="8e947-125">Тип: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="8e947-125">Type: **TemplateType**</span></span>

<span data-ttu-id="8e947-126">Значение из четырех компонентов, тип которого совпадает с типом шаблона.</span><span class="sxs-lookup"><span data-stu-id="8e947-126">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="8e947-127">Примечания</span><span class="sxs-lookup"><span data-stu-id="8e947-127">Remarks</span></span>

<span data-ttu-id="8e947-128">Примеры текстур можно использовать для интерполяции билинейной.</span><span class="sxs-lookup"><span data-stu-id="8e947-128">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="8e947-129">Эта функция поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="8e947-129">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="8e947-130">Вершина</span><span class="sxs-lookup"><span data-stu-id="8e947-130">Vertex</span></span> | <span data-ttu-id="8e947-131">Поверхности</span><span class="sxs-lookup"><span data-stu-id="8e947-131">Hull</span></span> | <span data-ttu-id="8e947-132">Домен</span><span class="sxs-lookup"><span data-stu-id="8e947-132">Domain</span></span> | <span data-ttu-id="8e947-133">Геометрия</span><span class="sxs-lookup"><span data-stu-id="8e947-133">Geometry</span></span> | <span data-ttu-id="8e947-134">Пиксель</span><span class="sxs-lookup"><span data-stu-id="8e947-134">Pixel</span></span> | <span data-ttu-id="8e947-135">Вычисления</span><span class="sxs-lookup"><span data-stu-id="8e947-135">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="8e947-136">x</span><span class="sxs-lookup"><span data-stu-id="8e947-136">x</span></span>      | <span data-ttu-id="8e947-137">x</span><span class="sxs-lookup"><span data-stu-id="8e947-137">x</span></span>    | <span data-ttu-id="8e947-138">x</span><span class="sxs-lookup"><span data-stu-id="8e947-138">x</span></span>      | <span data-ttu-id="8e947-139">x</span><span class="sxs-lookup"><span data-stu-id="8e947-139">x</span></span>        | <span data-ttu-id="8e947-140">x</span><span class="sxs-lookup"><span data-stu-id="8e947-140">x</span></span>     | <span data-ttu-id="8e947-141">x</span><span class="sxs-lookup"><span data-stu-id="8e947-141">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="8e947-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8e947-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e947-143">Методы Гасералфа</span><span class="sxs-lookup"><span data-stu-id="8e947-143">GatherAlpha methods</span></span>](texture2darray-gatheralpha.md)
</dt> </dl>

 

 
