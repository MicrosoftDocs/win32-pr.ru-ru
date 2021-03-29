---
title: 'Texture2DMSArray:: Sample. Operator, функция'
description: 'Возвращает переменную ресурса, доступную только для чтения. | Texture2DMSArray:: Sample. Operator, функция'
ms.assetid: 5334c1d5-dfbd-4987-875c-0b92967b0f13
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
ms.openlocfilehash: e78746e0afe03e65a313982ca35c27a75ea14f1b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986678"
---
# <a name="texture2dmsarraysampleoperator----function"></a><span data-ttu-id="12eee-105">Texture2DMSArray:: Sample. Operator, функция</span><span class="sxs-lookup"><span data-stu-id="12eee-105">Texture2DMSArray::sample.Operator    function</span></span>

<span data-ttu-id="12eee-106">Возвращает переменную ресурса, доступную только для чтения.</span><span class="sxs-lookup"><span data-stu-id="12eee-106">Returns a read-only resource variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="12eee-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="12eee-107">Syntax</span></span>

``` syntax
R sample.Operator[][](
  in uint sampleSlice,
  in uint3 pos
);
```

## <a name="parameters"></a><span data-ttu-id="12eee-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="12eee-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12eee-109">*самплеслице* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="12eee-109">*sampleSlice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12eee-110">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="12eee-110">Type: **uint**</span></span>

<span data-ttu-id="12eee-111">Пример индекса среза.</span><span class="sxs-lookup"><span data-stu-id="12eee-111">The sample slice index.</span></span>

</dd> <dt>

<span data-ttu-id="12eee-112">*POS-терминал* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="12eee-112">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12eee-113">Тип: **uint3**</span><span class="sxs-lookup"><span data-stu-id="12eee-113">Type: **uint3**</span></span>

<span data-ttu-id="12eee-114">Позиция индекса.</span><span class="sxs-lookup"><span data-stu-id="12eee-114">The index position.</span></span> <span data-ttu-id="12eee-115">Первый и второй компоненты содержат координаты (x, y).</span><span class="sxs-lookup"><span data-stu-id="12eee-115">The first and second components contain the (x, y) coordinates.</span></span> <span data-ttu-id="12eee-116">Третий компонент указывает нужный срез массива.</span><span class="sxs-lookup"><span data-stu-id="12eee-116">The third component indicates the desired array slice.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12eee-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="12eee-117">Return value</span></span>

<span data-ttu-id="12eee-118">Тип: **R**</span><span class="sxs-lookup"><span data-stu-id="12eee-118">Type: **R**</span></span>

<span data-ttu-id="12eee-119">Переменная ресурса, доступная только для чтения.</span><span class="sxs-lookup"><span data-stu-id="12eee-119">A read-only resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="12eee-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="12eee-120">Remarks</span></span>

### <a name="usage-example"></a><span data-ttu-id="12eee-121">Пример использования</span><span class="sxs-lookup"><span data-stu-id="12eee-121">Usage Example</span></span>


```
Texture2DMSArray<float4, 4> alpha;

float4 main( float3 tcoord : texturecoord0 ) : SV_Target
{
     return s_msTexture.sample[2][tcoord];
}
```



<span data-ttu-id="12eee-122">Эта функция поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="12eee-122">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="12eee-123">Вершина</span><span class="sxs-lookup"><span data-stu-id="12eee-123">Vertex</span></span> | <span data-ttu-id="12eee-124">Поверхности</span><span class="sxs-lookup"><span data-stu-id="12eee-124">Hull</span></span> | <span data-ttu-id="12eee-125">Домен</span><span class="sxs-lookup"><span data-stu-id="12eee-125">Domain</span></span> | <span data-ttu-id="12eee-126">Геометрия</span><span class="sxs-lookup"><span data-stu-id="12eee-126">Geometry</span></span> | <span data-ttu-id="12eee-127">Пиксель</span><span class="sxs-lookup"><span data-stu-id="12eee-127">Pixel</span></span> | <span data-ttu-id="12eee-128">Вычисления</span><span class="sxs-lookup"><span data-stu-id="12eee-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="12eee-129">x</span><span class="sxs-lookup"><span data-stu-id="12eee-129">x</span></span>      | <span data-ttu-id="12eee-130">x</span><span class="sxs-lookup"><span data-stu-id="12eee-130">x</span></span>    | <span data-ttu-id="12eee-131">x</span><span class="sxs-lookup"><span data-stu-id="12eee-131">x</span></span>      | <span data-ttu-id="12eee-132">x</span><span class="sxs-lookup"><span data-stu-id="12eee-132">x</span></span>        | <span data-ttu-id="12eee-133">x</span><span class="sxs-lookup"><span data-stu-id="12eee-133">x</span></span>     | <span data-ttu-id="12eee-134">x</span><span class="sxs-lookup"><span data-stu-id="12eee-134">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="12eee-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="12eee-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12eee-136">Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="12eee-136">Texture2DMSArray</span></span>](sm5-object-texture2dmsarray.md)
</dt> <dt>

[<span data-ttu-id="12eee-137">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="12eee-137">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




