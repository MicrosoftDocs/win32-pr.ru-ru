---
title: 'Функция Аутпутпатч:: operator'
description: 'Возвращает значение n точки управления в исправлении. | Функция Аутпутпатч:: operator'
ms.assetid: 3ac15fe8-8bab-46a2-8826-61ade927c99e
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
ms.openlocfilehash: 8194713dc4967151991fab95000fa70c40122f26
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104352712"
---
# <a name="outputpatchoperator--function"></a><span data-ttu-id="f668a-105">Функция Аутпутпатч:: operator</span><span class="sxs-lookup"><span data-stu-id="f668a-105">OutputPatch::Operator  function</span></span>

<span data-ttu-id="f668a-106">Возвращает *n*-<sup>е</sup> контрольную точку в исправлении.</span><span class="sxs-lookup"><span data-stu-id="f668a-106">Returns the *n*<sup>th</sup> control point in the patch.</span></span>

## <a name="syntax"></a><span data-ttu-id="f668a-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f668a-107">Syntax</span></span>

``` syntax
T Operator[](
  in uint n
);
```

## <a name="parameters"></a><span data-ttu-id="f668a-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="f668a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f668a-109">*n* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="f668a-109">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f668a-110">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="f668a-110">Type: **uint**</span></span>

<span data-ttu-id="f668a-111">Входной индекс.</span><span class="sxs-lookup"><span data-stu-id="f668a-111">The input index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f668a-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f668a-112">Return value</span></span>

<span data-ttu-id="f668a-113">Тип: **T**</span><span class="sxs-lookup"><span data-stu-id="f668a-113">Type: **T**</span></span>

<span data-ttu-id="f668a-114">*N*-<sup>я</sup> контрольная точка.</span><span class="sxs-lookup"><span data-stu-id="f668a-114">The *n*<sup>th</sup> control point.</span></span>

## <a name="remarks"></a><span data-ttu-id="f668a-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="f668a-115">Remarks</span></span>

<span data-ttu-id="f668a-116">Эта функция поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="f668a-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="f668a-117">Вершина</span><span class="sxs-lookup"><span data-stu-id="f668a-117">Vertex</span></span> | <span data-ttu-id="f668a-118">Поверхности</span><span class="sxs-lookup"><span data-stu-id="f668a-118">Hull</span></span> | <span data-ttu-id="f668a-119">Домен</span><span class="sxs-lookup"><span data-stu-id="f668a-119">Domain</span></span> | <span data-ttu-id="f668a-120">Геометрия</span><span class="sxs-lookup"><span data-stu-id="f668a-120">Geometry</span></span> | <span data-ttu-id="f668a-121">Пиксель</span><span class="sxs-lookup"><span data-stu-id="f668a-121">Pixel</span></span> | <span data-ttu-id="f668a-122">Вычисления</span><span class="sxs-lookup"><span data-stu-id="f668a-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="f668a-123">x</span><span class="sxs-lookup"><span data-stu-id="f668a-123">x</span></span>    | <span data-ttu-id="f668a-124">x</span><span class="sxs-lookup"><span data-stu-id="f668a-124">x</span></span>      |          |       |         |



 

## <a name="see-also"></a><span data-ttu-id="f668a-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f668a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f668a-126">аутпутпатч</span><span class="sxs-lookup"><span data-stu-id="f668a-126">OutputPatch</span></span>](sm5-object-outputpatch.md)
</dt> <dt>

[<span data-ttu-id="f668a-127">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="f668a-127">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




