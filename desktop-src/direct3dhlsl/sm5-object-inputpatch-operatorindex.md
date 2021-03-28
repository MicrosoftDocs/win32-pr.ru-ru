---
title: 'Функция Инпутпатч:: operator'
description: 'Возвращает значение n точки управления в исправлении. | Функция Инпутпатч:: operator'
ms.assetid: 2c1eda6b-a9c1-40d3-be91-7a2e8f1da9fc
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
ms.openlocfilehash: 5d95cb8adae6e7a91629614e0ae10b4161dbac3f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104273482"
---
# <a name="inputpatchoperator--function"></a><span data-ttu-id="7e83c-105">Функция Инпутпатч:: operator</span><span class="sxs-lookup"><span data-stu-id="7e83c-105">InputPatch::Operator  function</span></span>

<span data-ttu-id="7e83c-106">Возвращает *n*-<sup>е</sup> контрольную точку в исправлении.</span><span class="sxs-lookup"><span data-stu-id="7e83c-106">Returns the *n*<sup>th</sup> control point in the patch.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e83c-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7e83c-107">Syntax</span></span>

``` syntax
T Operator[](
  in uint n
);
```

## <a name="parameters"></a><span data-ttu-id="7e83c-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="7e83c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7e83c-109">*n* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="7e83c-109">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e83c-110">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="7e83c-110">Type: **uint**</span></span>

<span data-ttu-id="7e83c-111">Входной индекс.</span><span class="sxs-lookup"><span data-stu-id="7e83c-111">The input index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7e83c-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7e83c-112">Return value</span></span>

<span data-ttu-id="7e83c-113">Тип: **T**</span><span class="sxs-lookup"><span data-stu-id="7e83c-113">Type: **T**</span></span>

<span data-ttu-id="7e83c-114">*N*-<sup>я</sup> контрольная точка.</span><span class="sxs-lookup"><span data-stu-id="7e83c-114">The *n*<sup>th</sup> control point.</span></span>

## <a name="remarks"></a><span data-ttu-id="7e83c-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="7e83c-115">Remarks</span></span>

<span data-ttu-id="7e83c-116">Эта функция поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="7e83c-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="7e83c-117">Вершина</span><span class="sxs-lookup"><span data-stu-id="7e83c-117">Vertex</span></span> | <span data-ttu-id="7e83c-118">Поверхности</span><span class="sxs-lookup"><span data-stu-id="7e83c-118">Hull</span></span> | <span data-ttu-id="7e83c-119">Домен</span><span class="sxs-lookup"><span data-stu-id="7e83c-119">Domain</span></span> | <span data-ttu-id="7e83c-120">Геометрия</span><span class="sxs-lookup"><span data-stu-id="7e83c-120">Geometry</span></span> | <span data-ttu-id="7e83c-121">Пиксель</span><span class="sxs-lookup"><span data-stu-id="7e83c-121">Pixel</span></span> | <span data-ttu-id="7e83c-122">Вычисления</span><span class="sxs-lookup"><span data-stu-id="7e83c-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="7e83c-123">x</span><span class="sxs-lookup"><span data-stu-id="7e83c-123">x</span></span>    |        |          |       |         |



 

## <a name="see-also"></a><span data-ttu-id="7e83c-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7e83c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e83c-125">инпутпатч</span><span class="sxs-lookup"><span data-stu-id="7e83c-125">InputPatch</span></span>](sm5-object-inputpatch.md)
</dt> <dt>

[<span data-ttu-id="7e83c-126">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="7e83c-126">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




