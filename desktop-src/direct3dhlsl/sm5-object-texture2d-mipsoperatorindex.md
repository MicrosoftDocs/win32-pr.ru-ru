---
title: 'Texture2D:: MIPS. Operator, функция'
description: 'Возвращает переменную ресурса, доступную только для чтения. | Texture2D:: MIPS. Operator, функция'
ms.assetid: 201996a7-741f-4457-ab77-9cd653f3682b
keywords:
- MIPS. Оператор Function HLSL
topic_type:
- apiref
api_name:
- mips.Operator
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 994ede49563b1d4e568769be48a0e60592fe3dde
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986245"
---
# <a name="texture2dmipsoperator----function"></a><span data-ttu-id="bcaed-105">Texture2D:: MIPS. Operator, функция</span><span class="sxs-lookup"><span data-stu-id="bcaed-105">Texture2D::mips.Operator    function</span></span>

<span data-ttu-id="bcaed-106">Возвращает переменную ресурса, доступную только для чтения.</span><span class="sxs-lookup"><span data-stu-id="bcaed-106">Returns a read-only resource variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="bcaed-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bcaed-107">Syntax</span></span>

``` syntax
R mips.Operator[][](
  in uint mipSlice,
  in uint2 pos
);
```

## <a name="parameters"></a><span data-ttu-id="bcaed-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="bcaed-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bcaed-109">*мипслице* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bcaed-109">*mipSlice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bcaed-110">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="bcaed-110">Type: **uint**</span></span>

<span data-ttu-id="bcaed-111">Индекс среза MIP.</span><span class="sxs-lookup"><span data-stu-id="bcaed-111">The mip slice index.</span></span>

</dd> <dt>

<span data-ttu-id="bcaed-112">*POS-терминал* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bcaed-112">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bcaed-113">Тип: **uint2**</span><span class="sxs-lookup"><span data-stu-id="bcaed-113">Type: **uint2**</span></span>

<span data-ttu-id="bcaed-114">Позиция индекса.</span><span class="sxs-lookup"><span data-stu-id="bcaed-114">The index position.</span></span> <span data-ttu-id="bcaed-115">Содержит координаты (x, y).</span><span class="sxs-lookup"><span data-stu-id="bcaed-115">Contains the (x, y) coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bcaed-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bcaed-116">Return value</span></span>

<span data-ttu-id="bcaed-117">Тип: **R**</span><span class="sxs-lookup"><span data-stu-id="bcaed-117">Type: **R**</span></span>

<span data-ttu-id="bcaed-118">Переменная ресурса, доступная только для чтения.</span><span class="sxs-lookup"><span data-stu-id="bcaed-118">A read-only resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="bcaed-119">Примечания</span><span class="sxs-lookup"><span data-stu-id="bcaed-119">Remarks</span></span>

### <a name="usage-example"></a><span data-ttu-id="bcaed-120">Пример использования</span><span class="sxs-lookup"><span data-stu-id="bcaed-120">Usage Example</span></span>


```
Texture2D<float4> tex;
uint mip = 2;
uint2 pos_xy = {123, 456};
float4 f = tex.mips[mip][pos_xy];
        
```



<span data-ttu-id="bcaed-121">Эта функция поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="bcaed-121">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="bcaed-122">Вершина</span><span class="sxs-lookup"><span data-stu-id="bcaed-122">Vertex</span></span> | <span data-ttu-id="bcaed-123">Поверхности</span><span class="sxs-lookup"><span data-stu-id="bcaed-123">Hull</span></span> | <span data-ttu-id="bcaed-124">Домен</span><span class="sxs-lookup"><span data-stu-id="bcaed-124">Domain</span></span> | <span data-ttu-id="bcaed-125">Геометрия</span><span class="sxs-lookup"><span data-stu-id="bcaed-125">Geometry</span></span> | <span data-ttu-id="bcaed-126">Пиксель</span><span class="sxs-lookup"><span data-stu-id="bcaed-126">Pixel</span></span> | <span data-ttu-id="bcaed-127">Вычисления</span><span class="sxs-lookup"><span data-stu-id="bcaed-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="bcaed-128">x</span><span class="sxs-lookup"><span data-stu-id="bcaed-128">x</span></span>      | <span data-ttu-id="bcaed-129">x</span><span class="sxs-lookup"><span data-stu-id="bcaed-129">x</span></span>    | <span data-ttu-id="bcaed-130">x</span><span class="sxs-lookup"><span data-stu-id="bcaed-130">x</span></span>      | <span data-ttu-id="bcaed-131">x</span><span class="sxs-lookup"><span data-stu-id="bcaed-131">x</span></span>        | <span data-ttu-id="bcaed-132">x</span><span class="sxs-lookup"><span data-stu-id="bcaed-132">x</span></span>     | <span data-ttu-id="bcaed-133">x</span><span class="sxs-lookup"><span data-stu-id="bcaed-133">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="bcaed-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bcaed-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bcaed-135">Texture2D</span><span class="sxs-lookup"><span data-stu-id="bcaed-135">Texture2D</span></span>](sm5-object-texture2d.md)
</dt> <dt>

[<span data-ttu-id="bcaed-136">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="bcaed-136">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




