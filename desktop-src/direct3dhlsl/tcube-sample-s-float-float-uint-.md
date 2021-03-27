---
title: 'Функция Текстурекубе:: Sample (S, float, float, uint)'
description: 'Выбирает текстуру с необязательным значением для фиксации в качестве примера значений уровня детализации (Лод) и возвращает состояние операции. | Функция Текстурекубе:: Sample (S, float, float, uint)'
ms.assetid: 8FA17583-9002-4DEC-A6D5-85B25DEA19B7
keywords:
- Пример функции HLSL
topic_type:
- apiref
api_name:
- Sample
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9a91e9a3dcc2df617f50175eb0872398bc564103
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986541"
---
# <a name="texturecubesamplesfloatfloatuint-function"></a><span data-ttu-id="acc03-105">Функция Текстурекубе:: Sample (S, float, float, uint)</span><span class="sxs-lookup"><span data-stu-id="acc03-105">TextureCube::Sample(S,float,float,uint) function</span></span>

<span data-ttu-id="acc03-106">Выбирает текстуру с необязательным значением для фиксации в качестве примера значений уровня детализации (Лод) и возвращает состояние операции.</span><span class="sxs-lookup"><span data-stu-id="acc03-106">Samples a texture with an optional value to clamp sample level-of-detail (LOD) values to, and returns status of the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="acc03-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="acc03-107">Syntax</span></span>


``` syntax
DXGI_FORMAT Sample(
  in  SamplerState S,
  in  float        Location,
  in  float        Clamp,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="acc03-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="acc03-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="acc03-109">*S* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="acc03-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="acc03-110">[Состояние образца](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="acc03-110">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="acc03-111">Это объект, объявленный в файле эффектов, который содержит назначения состояний.</span><span class="sxs-lookup"><span data-stu-id="acc03-111">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="acc03-112">*Расположение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="acc03-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="acc03-113">Координаты текстуры.</span><span class="sxs-lookup"><span data-stu-id="acc03-113">The texture coordinates.</span></span> <span data-ttu-id="acc03-114">Тип аргумента зависит от типа объекта текстуры.</span><span class="sxs-lookup"><span data-stu-id="acc03-114">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="acc03-115">Тип Texture-Object</span><span class="sxs-lookup"><span data-stu-id="acc03-115">Texture-Object Type</span></span>                    | <span data-ttu-id="acc03-116">Тип параметра</span><span class="sxs-lookup"><span data-stu-id="acc03-116">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="acc03-117">Texture1D</span><span class="sxs-lookup"><span data-stu-id="acc03-117">Texture1D</span></span>                              | <span data-ttu-id="acc03-118">FLOAT</span><span class="sxs-lookup"><span data-stu-id="acc03-118">float</span></span>          |
| <span data-ttu-id="acc03-119">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="acc03-119">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="acc03-120">float2</span><span class="sxs-lookup"><span data-stu-id="acc03-120">float2</span></span>         |
| <span data-ttu-id="acc03-121">Texture2DArray, Texture3D, Текстурекубе</span><span class="sxs-lookup"><span data-stu-id="acc03-121">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="acc03-122">float3</span><span class="sxs-lookup"><span data-stu-id="acc03-122">float3</span></span>         |
| <span data-ttu-id="acc03-123">текстурекубеаррай</span><span class="sxs-lookup"><span data-stu-id="acc03-123">TextureCubeArray</span></span>                       | <span data-ttu-id="acc03-124">float4</span><span class="sxs-lookup"><span data-stu-id="acc03-124">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="acc03-125">*Срез* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="acc03-125">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="acc03-126">Необязательное значение для примера среза Лод значений.</span><span class="sxs-lookup"><span data-stu-id="acc03-126">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="acc03-127">Например, если передать значение среза 2.0 f, вы убедитесь, что ни один из отдельных примеров не имеет доступа к MIP уровню менее 2.0.</span><span class="sxs-lookup"><span data-stu-id="acc03-127">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> <dt>

<span data-ttu-id="acc03-128">*Состояние* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="acc03-128">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="acc03-129">Состояние операции.</span><span class="sxs-lookup"><span data-stu-id="acc03-129">The status of the operation.</span></span> <span data-ttu-id="acc03-130">Вы не можете получить доступ к состоянию напрямую; Вместо этого передайте состояние в подставляемую функцию [**чеккакцессфуллимаппед**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="acc03-130">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="acc03-131">**Чеккакцессфуллимаппед** возвращает **значение true** , если все значения из соответствующего **образца**, **сбора** или операции **загрузки** обращались к сопоставленным плиткам в [мозаичном ресурсе](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="acc03-131">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="acc03-132">Если какие бы то ни было значения были взяты из несопоставленной плитки, **чеккакцессфуллимаппед** возвращает **значение false**.</span><span class="sxs-lookup"><span data-stu-id="acc03-132">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="acc03-133">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="acc03-133">Return value</span></span>

<span data-ttu-id="acc03-134">Формат текстуры, который является одним из типизированных значений, перечисленных в [**\_ формате DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="acc03-134">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="acc03-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="acc03-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="acc03-136">Примеры методов</span><span class="sxs-lookup"><span data-stu-id="acc03-136">Sample methods</span></span>](texturecube-sample.md)
</dt> <dt>

[<span data-ttu-id="acc03-137">**текстурекубе**</span><span class="sxs-lookup"><span data-stu-id="acc03-137">**TextureCube**</span></span>](texturecube.md)
</dt> </dl>

 

 
