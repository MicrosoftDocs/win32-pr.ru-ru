---
title: 'Функция Texture2D:: operator'
description: 'Возвращает переменную ресурса, доступную только для чтения. | Функция Texture2D:: operator'
ms.assetid: 72ba3fc8-04c3-479a-b307-525020898bac
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
ms.openlocfilehash: 2c397b1b80836f48cb856d03ccdf52ad2c95ce48
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986512"
---
# <a name="texture2doperator--function"></a><span data-ttu-id="b5cc1-105">Функция Texture2D:: operator</span><span class="sxs-lookup"><span data-stu-id="b5cc1-105">Texture2D::Operator  function</span></span>

<span data-ttu-id="b5cc1-106">Возвращает переменную ресурса, доступную только для чтения.</span><span class="sxs-lookup"><span data-stu-id="b5cc1-106">Returns a read-only resource variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5cc1-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b5cc1-107">Syntax</span></span>

``` syntax
R Operator[](
  in uint2 pos
);
```

## <a name="parameters"></a><span data-ttu-id="b5cc1-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="b5cc1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5cc1-109">*POS-терминал* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b5cc1-109">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5cc1-110">Тип: **uint2**</span><span class="sxs-lookup"><span data-stu-id="b5cc1-110">Type: **uint2**</span></span>

<span data-ttu-id="b5cc1-111">Позиция индекса.</span><span class="sxs-lookup"><span data-stu-id="b5cc1-111">The index position.</span></span> <span data-ttu-id="b5cc1-112">Содержит координаты (x, y).</span><span class="sxs-lookup"><span data-stu-id="b5cc1-112">Contains the (x, y) coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5cc1-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b5cc1-113">Return value</span></span>

<span data-ttu-id="b5cc1-114">Тип: **R**</span><span class="sxs-lookup"><span data-stu-id="b5cc1-114">Type: **R**</span></span>

<span data-ttu-id="b5cc1-115">Переменная ресурса, доступная только для чтения.</span><span class="sxs-lookup"><span data-stu-id="b5cc1-115">A read-only resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="b5cc1-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="b5cc1-116">Remarks</span></span>

<span data-ttu-id="b5cc1-117">Этот метод всегда обращается к первому MIP уровню.</span><span class="sxs-lookup"><span data-stu-id="b5cc1-117">This method always accesses the first mip level.</span></span> <span data-ttu-id="b5cc1-118">Чтобы указать другие уровни MIP, используйте вместо него метод [**MIP \[ \] \[ \] . operator**](sm5-object-texture2d-mipsoperatorindex.md) .</span><span class="sxs-lookup"><span data-stu-id="b5cc1-118">To specify other mip levels, use the [**mip.operator\[\]\[\]**](sm5-object-texture2d-mipsoperatorindex.md) method instead.</span></span>

<span data-ttu-id="b5cc1-119">Примеры текстур можно использовать для интерполяции билинейной.</span><span class="sxs-lookup"><span data-stu-id="b5cc1-119">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="b5cc1-120">Эта функция поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="b5cc1-120">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="b5cc1-121">Вершина</span><span class="sxs-lookup"><span data-stu-id="b5cc1-121">Vertex</span></span> | <span data-ttu-id="b5cc1-122">Поверхности</span><span class="sxs-lookup"><span data-stu-id="b5cc1-122">Hull</span></span> | <span data-ttu-id="b5cc1-123">Домен</span><span class="sxs-lookup"><span data-stu-id="b5cc1-123">Domain</span></span> | <span data-ttu-id="b5cc1-124">Геометрия</span><span class="sxs-lookup"><span data-stu-id="b5cc1-124">Geometry</span></span> | <span data-ttu-id="b5cc1-125">Пиксель</span><span class="sxs-lookup"><span data-stu-id="b5cc1-125">Pixel</span></span> | <span data-ttu-id="b5cc1-126">Вычисления</span><span class="sxs-lookup"><span data-stu-id="b5cc1-126">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="b5cc1-127">x</span><span class="sxs-lookup"><span data-stu-id="b5cc1-127">x</span></span>      | <span data-ttu-id="b5cc1-128">x</span><span class="sxs-lookup"><span data-stu-id="b5cc1-128">x</span></span>    | <span data-ttu-id="b5cc1-129">x</span><span class="sxs-lookup"><span data-stu-id="b5cc1-129">x</span></span>      | <span data-ttu-id="b5cc1-130">x</span><span class="sxs-lookup"><span data-stu-id="b5cc1-130">x</span></span>        | <span data-ttu-id="b5cc1-131">x</span><span class="sxs-lookup"><span data-stu-id="b5cc1-131">x</span></span>     | <span data-ttu-id="b5cc1-132">x</span><span class="sxs-lookup"><span data-stu-id="b5cc1-132">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="b5cc1-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b5cc1-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5cc1-134">Texture2D</span><span class="sxs-lookup"><span data-stu-id="b5cc1-134">Texture2D</span></span>](sm5-object-texture2d.md)
</dt> <dt>

[<span data-ttu-id="b5cc1-135">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="b5cc1-135">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




