---
title: 'Функция RWTexture2D:: operator'
description: 'Возвращает переменную ресурса. | Функция RWTexture2D:: operator'
ms.assetid: 339dba7d-b0c6-4112-ae40-555661577a3e
keywords:
- Оператор Function HLSL
topic_type:
- apiref
api_name:
- Operator
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8c1ff25cdf4a0f33d041500f6a81220261f216c4
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986477"
---
# <a name="rwtexture2doperator--function"></a><span data-ttu-id="2c2a2-105">Функция RWTexture2D:: operator</span><span class="sxs-lookup"><span data-stu-id="2c2a2-105">RWTexture2D::Operator  function</span></span>

<span data-ttu-id="2c2a2-106">Возвращает переменную ресурса.</span><span class="sxs-lookup"><span data-stu-id="2c2a2-106">Returns a resource variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c2a2-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2c2a2-107">Syntax</span></span>

``` syntax
R Operator[](
  in uint2 pos
);
```

## <a name="parameters"></a><span data-ttu-id="2c2a2-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="2c2a2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c2a2-109">*POS-терминал* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2c2a2-109">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2c2a2-110">Тип: **uint2**</span><span class="sxs-lookup"><span data-stu-id="2c2a2-110">Type: **uint2**</span></span>

<span data-ttu-id="2c2a2-111">Позиция индекса.</span><span class="sxs-lookup"><span data-stu-id="2c2a2-111">The index position.</span></span> <span data-ttu-id="2c2a2-112">Содержит координаты (x, y).</span><span class="sxs-lookup"><span data-stu-id="2c2a2-112">Contains the (x, y) coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c2a2-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2c2a2-113">Return value</span></span>

<span data-ttu-id="2c2a2-114">Тип: **R**</span><span class="sxs-lookup"><span data-stu-id="2c2a2-114">Type: **R**</span></span>

<span data-ttu-id="2c2a2-115">Переменная ресурса.</span><span class="sxs-lookup"><span data-stu-id="2c2a2-115">A resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="2c2a2-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="2c2a2-116">Remarks</span></span>

<span data-ttu-id="2c2a2-117">Эта функция поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="2c2a2-117">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="2c2a2-118">Вершина</span><span class="sxs-lookup"><span data-stu-id="2c2a2-118">Vertex</span></span> | <span data-ttu-id="2c2a2-119">Поверхности</span><span class="sxs-lookup"><span data-stu-id="2c2a2-119">Hull</span></span> | <span data-ttu-id="2c2a2-120">Домен</span><span class="sxs-lookup"><span data-stu-id="2c2a2-120">Domain</span></span> | <span data-ttu-id="2c2a2-121">Геометрия</span><span class="sxs-lookup"><span data-stu-id="2c2a2-121">Geometry</span></span> | <span data-ttu-id="2c2a2-122">Пиксель</span><span class="sxs-lookup"><span data-stu-id="2c2a2-122">Pixel</span></span> | <span data-ttu-id="2c2a2-123">Вычисления</span><span class="sxs-lookup"><span data-stu-id="2c2a2-123">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="2c2a2-124">x</span><span class="sxs-lookup"><span data-stu-id="2c2a2-124">x</span></span>     | <span data-ttu-id="2c2a2-125">x</span><span class="sxs-lookup"><span data-stu-id="2c2a2-125">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="2c2a2-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2c2a2-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c2a2-127">RWTexture2D</span><span class="sxs-lookup"><span data-stu-id="2c2a2-127">RWTexture2D</span></span>](sm5-object-rwtexture2d.md)
</dt> <dt>

[<span data-ttu-id="2c2a2-128">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="2c2a2-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




