---
title: 'Функция Texture3D:: operator'
description: 'Возвращает переменную ресурса, доступную только для чтения. | Функция Texture3D:: operator'
ms.assetid: d7e27778-6a96-47f8-a58a-1966452adf04
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
ms.openlocfilehash: 5c3bb3718094ee859d1e33a046fde7016973a0aa
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "103820653"
---
# <a name="texture3doperator--function"></a><span data-ttu-id="63254-105">Функция Texture3D:: operator</span><span class="sxs-lookup"><span data-stu-id="63254-105">Texture3D::Operator  function</span></span>

<span data-ttu-id="63254-106">Возвращает переменную ресурса, доступную только для чтения.</span><span class="sxs-lookup"><span data-stu-id="63254-106">Returns a read-only resource variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="63254-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="63254-107">Syntax</span></span>

``` syntax
R Operator[](
  in uint3 pos
);
```

## <a name="parameters"></a><span data-ttu-id="63254-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="63254-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63254-109">*POS-терминал* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="63254-109">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63254-110">Тип: **uint3**</span><span class="sxs-lookup"><span data-stu-id="63254-110">Type: **uint3**</span></span>

<span data-ttu-id="63254-111">Позиция индекса.</span><span class="sxs-lookup"><span data-stu-id="63254-111">The index position.</span></span> <span data-ttu-id="63254-112">Содержит координаты (x, y, z).</span><span class="sxs-lookup"><span data-stu-id="63254-112">Contains the (x, y, z) coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63254-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="63254-113">Return value</span></span>

<span data-ttu-id="63254-114">Тип: **R**</span><span class="sxs-lookup"><span data-stu-id="63254-114">Type: **R**</span></span>

<span data-ttu-id="63254-115">Переменная ресурса, доступная только для чтения.</span><span class="sxs-lookup"><span data-stu-id="63254-115">A read-only resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="63254-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="63254-116">Remarks</span></span>

<span data-ttu-id="63254-117">Этот метод всегда обращается к первому MIP уровню.</span><span class="sxs-lookup"><span data-stu-id="63254-117">This method always accesses the first mip level.</span></span> <span data-ttu-id="63254-118">Чтобы указать другие уровни MIP, используйте вместо него [**оператор \[ \] \[ \] MIP.**](sm5-object-texture3d-mipsoperatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="63254-118">To specify other mip levels use the [**mip.operator\[\]\[\]**](sm5-object-texture3d-mipsoperatorindex.md) instead.</span></span>

<span data-ttu-id="63254-119">Эта функция поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="63254-119">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="63254-120">Вершина</span><span class="sxs-lookup"><span data-stu-id="63254-120">Vertex</span></span> | <span data-ttu-id="63254-121">Поверхности</span><span class="sxs-lookup"><span data-stu-id="63254-121">Hull</span></span> | <span data-ttu-id="63254-122">Домен</span><span class="sxs-lookup"><span data-stu-id="63254-122">Domain</span></span> | <span data-ttu-id="63254-123">Геометрия</span><span class="sxs-lookup"><span data-stu-id="63254-123">Geometry</span></span> | <span data-ttu-id="63254-124">Пиксель</span><span class="sxs-lookup"><span data-stu-id="63254-124">Pixel</span></span> | <span data-ttu-id="63254-125">Вычисления</span><span class="sxs-lookup"><span data-stu-id="63254-125">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="63254-126">x</span><span class="sxs-lookup"><span data-stu-id="63254-126">x</span></span>      | <span data-ttu-id="63254-127">x</span><span class="sxs-lookup"><span data-stu-id="63254-127">x</span></span>    | <span data-ttu-id="63254-128">x</span><span class="sxs-lookup"><span data-stu-id="63254-128">x</span></span>      | <span data-ttu-id="63254-129">x</span><span class="sxs-lookup"><span data-stu-id="63254-129">x</span></span>        | <span data-ttu-id="63254-130">x</span><span class="sxs-lookup"><span data-stu-id="63254-130">x</span></span>     | <span data-ttu-id="63254-131">x</span><span class="sxs-lookup"><span data-stu-id="63254-131">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="63254-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="63254-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63254-133">Texture3D</span><span class="sxs-lookup"><span data-stu-id="63254-133">Texture3D</span></span>](sm5-object-texture3d.md)
</dt> <dt>

[<span data-ttu-id="63254-134">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="63254-134">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




