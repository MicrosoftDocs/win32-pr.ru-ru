---
title: 'Texture3D:: MIPS. Operator, функция'
description: 'Возвращает переменную ресурса, доступную только для чтения. | Texture3D:: MIPS. Operator, функция'
ms.assetid: d5f6cb3b-4163-44c2-8379-ac8a412b1aa6
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
ms.openlocfilehash: e8f7064459354ec4827ba6d96795e82ccab3800c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104273453"
---
# <a name="texture3dmipsoperator----function"></a><span data-ttu-id="dbf1f-105">Texture3D:: MIPS. Operator, функция</span><span class="sxs-lookup"><span data-stu-id="dbf1f-105">Texture3D::mips.Operator    function</span></span>

<span data-ttu-id="dbf1f-106">Возвращает переменную ресурса, доступную только для чтения.</span><span class="sxs-lookup"><span data-stu-id="dbf1f-106">Returns a read-only resource variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="dbf1f-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dbf1f-107">Syntax</span></span>

``` syntax
R mips.Operator[][](
  in uint mipSlice,
  in uint3 pos
);
```

## <a name="parameters"></a><span data-ttu-id="dbf1f-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="dbf1f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dbf1f-109">*мипслице* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="dbf1f-109">*mipSlice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dbf1f-110">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="dbf1f-110">Type: **uint**</span></span>

<span data-ttu-id="dbf1f-111">Индекс среза MIP.</span><span class="sxs-lookup"><span data-stu-id="dbf1f-111">The mip slice index.</span></span>

</dd> <dt>

<span data-ttu-id="dbf1f-112">*POS-терминал* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="dbf1f-112">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dbf1f-113">Тип: **uint3**</span><span class="sxs-lookup"><span data-stu-id="dbf1f-113">Type: **uint3**</span></span>

<span data-ttu-id="dbf1f-114">Позиция индекса.</span><span class="sxs-lookup"><span data-stu-id="dbf1f-114">The index position.</span></span> <span data-ttu-id="dbf1f-115">Содержит координаты (x, y, z).</span><span class="sxs-lookup"><span data-stu-id="dbf1f-115">Contains the (x, y, z) coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dbf1f-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dbf1f-116">Return value</span></span>

<span data-ttu-id="dbf1f-117">Тип: **R**</span><span class="sxs-lookup"><span data-stu-id="dbf1f-117">Type: **R**</span></span>

<span data-ttu-id="dbf1f-118">Переменная ресурса, доступная только для чтения.</span><span class="sxs-lookup"><span data-stu-id="dbf1f-118">A read-only resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="dbf1f-119">Примечания</span><span class="sxs-lookup"><span data-stu-id="dbf1f-119">Remarks</span></span>

### <a name="usage-example"></a><span data-ttu-id="dbf1f-120">Пример использования</span><span class="sxs-lookup"><span data-stu-id="dbf1f-120">Usage Example</span></span>


```
Texture3D<float4> tex;
uint mip = 2;
uint3 pos_xyz = {123, 456, 789};
float4 f = tex.mips[mip][pos_xyz];
        
```



<span data-ttu-id="dbf1f-121">Эта функция поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="dbf1f-121">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="dbf1f-122">Вершина</span><span class="sxs-lookup"><span data-stu-id="dbf1f-122">Vertex</span></span> | <span data-ttu-id="dbf1f-123">Поверхности</span><span class="sxs-lookup"><span data-stu-id="dbf1f-123">Hull</span></span> | <span data-ttu-id="dbf1f-124">Домен</span><span class="sxs-lookup"><span data-stu-id="dbf1f-124">Domain</span></span> | <span data-ttu-id="dbf1f-125">Геометрия</span><span class="sxs-lookup"><span data-stu-id="dbf1f-125">Geometry</span></span> | <span data-ttu-id="dbf1f-126">Пиксель</span><span class="sxs-lookup"><span data-stu-id="dbf1f-126">Pixel</span></span> | <span data-ttu-id="dbf1f-127">Вычисления</span><span class="sxs-lookup"><span data-stu-id="dbf1f-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="dbf1f-128">x</span><span class="sxs-lookup"><span data-stu-id="dbf1f-128">x</span></span>      | <span data-ttu-id="dbf1f-129">x</span><span class="sxs-lookup"><span data-stu-id="dbf1f-129">x</span></span>    | <span data-ttu-id="dbf1f-130">x</span><span class="sxs-lookup"><span data-stu-id="dbf1f-130">x</span></span>      | <span data-ttu-id="dbf1f-131">x</span><span class="sxs-lookup"><span data-stu-id="dbf1f-131">x</span></span>        | <span data-ttu-id="dbf1f-132">x</span><span class="sxs-lookup"><span data-stu-id="dbf1f-132">x</span></span>     | <span data-ttu-id="dbf1f-133">x</span><span class="sxs-lookup"><span data-stu-id="dbf1f-133">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="dbf1f-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dbf1f-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dbf1f-135">Texture3D</span><span class="sxs-lookup"><span data-stu-id="dbf1f-135">Texture3D</span></span>](sm5-object-texture3d.md)
</dt> <dt>

[<span data-ttu-id="dbf1f-136">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="dbf1f-136">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




