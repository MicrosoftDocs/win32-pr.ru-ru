---
title: 'Texture2DMS:: Sample. Operator, функция'
description: 'Извлекает значение из ресурса в расположении и указанном индексе выборки. | Texture2DMS:: Sample. Operator, функция'
ms.assetid: 5bc24129-b690-44dd-ae85-8533b10befaa
keywords:
- Следующий. Оператор Function HLSL
topic_type:
- apiref
api_name:
- sample.Operator
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1a73577fa67992b212b4769059f1523e584acbaf
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104273645"
---
# <a name="texture2dmssampleoperator----function"></a><span data-ttu-id="36680-105">Texture2DMS:: Sample. Operator, функция</span><span class="sxs-lookup"><span data-stu-id="36680-105">Texture2DMS::sample.Operator    function</span></span>

<span data-ttu-id="36680-106">Извлекает значение из ресурса в расположении и указанном индексе выборки.</span><span class="sxs-lookup"><span data-stu-id="36680-106">Retrieves a value from the resource at the location and sample index provided.</span></span>

## <a name="syntax"></a><span data-ttu-id="36680-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="36680-107">Syntax</span></span>

``` syntax
R sample.Operator[][](
  in uint sampleSlice,
  in uint2 pos
);
```

## <a name="parameters"></a><span data-ttu-id="36680-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="36680-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36680-109">*самплеслице* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="36680-109">*sampleSlice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="36680-110">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="36680-110">Type: **uint**</span></span>

<span data-ttu-id="36680-111">Пример индекса среза.</span><span class="sxs-lookup"><span data-stu-id="36680-111">The sample slice index.</span></span>

</dd> <dt>

<span data-ttu-id="36680-112">*POS-терминал* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="36680-112">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="36680-113">Тип: **uint2**</span><span class="sxs-lookup"><span data-stu-id="36680-113">Type: **uint2**</span></span>

<span data-ttu-id="36680-114">Позиция индекса.</span><span class="sxs-lookup"><span data-stu-id="36680-114">The index position.</span></span> <span data-ttu-id="36680-115">Компоненты содержат координаты (x, y).</span><span class="sxs-lookup"><span data-stu-id="36680-115">The components contain the (x, y) coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="36680-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="36680-116">Return value</span></span>

<span data-ttu-id="36680-117">Тип: **R**</span><span class="sxs-lookup"><span data-stu-id="36680-117">Type: **R**</span></span>

<span data-ttu-id="36680-118">Переменная ресурса, доступная только для чтения.</span><span class="sxs-lookup"><span data-stu-id="36680-118">A read-only resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="36680-119">Примечания</span><span class="sxs-lookup"><span data-stu-id="36680-119">Remarks</span></span>

### <a name="usage-example"></a><span data-ttu-id="36680-120">Пример использования</span><span class="sxs-lookup"><span data-stu-id="36680-120">Usage Example</span></span>


```
Texture2DMS<float4, 8> tex;

float4 main( float3 tcoord : texturecoord0 ) : SV_Target
{
     return s_msTexture.sample[2][tcoord];
}
```



<span data-ttu-id="36680-121">Эта функция поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="36680-121">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="36680-122">Вершина</span><span class="sxs-lookup"><span data-stu-id="36680-122">Vertex</span></span> | <span data-ttu-id="36680-123">Поверхности</span><span class="sxs-lookup"><span data-stu-id="36680-123">Hull</span></span> | <span data-ttu-id="36680-124">Домен</span><span class="sxs-lookup"><span data-stu-id="36680-124">Domain</span></span> | <span data-ttu-id="36680-125">Геометрия</span><span class="sxs-lookup"><span data-stu-id="36680-125">Geometry</span></span> | <span data-ttu-id="36680-126">Пиксель</span><span class="sxs-lookup"><span data-stu-id="36680-126">Pixel</span></span> | <span data-ttu-id="36680-127">Вычисления</span><span class="sxs-lookup"><span data-stu-id="36680-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="36680-128">x</span><span class="sxs-lookup"><span data-stu-id="36680-128">x</span></span>      | <span data-ttu-id="36680-129">x</span><span class="sxs-lookup"><span data-stu-id="36680-129">x</span></span>    | <span data-ttu-id="36680-130">x</span><span class="sxs-lookup"><span data-stu-id="36680-130">x</span></span>      | <span data-ttu-id="36680-131">x</span><span class="sxs-lookup"><span data-stu-id="36680-131">x</span></span>        | <span data-ttu-id="36680-132">x</span><span class="sxs-lookup"><span data-stu-id="36680-132">x</span></span>     | <span data-ttu-id="36680-133">x</span><span class="sxs-lookup"><span data-stu-id="36680-133">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="36680-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="36680-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36680-135">Texture2DMS</span><span class="sxs-lookup"><span data-stu-id="36680-135">Texture2DMS</span></span>](sm5-object-texture2dms.md)
</dt> <dt>

[<span data-ttu-id="36680-136">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="36680-136">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




