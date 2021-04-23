---
title: 'Функция RWTexture1D:: operator'
description: 'Возвращает переменную ресурса. | Функция RWTexture1D:: operator'
ms.assetid: 16e62879-8ed3-4b17-9124-9da41c41af4f
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
ms.openlocfilehash: ca44252a99e8b8e373cf109341c8c200636d8cf7
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104547511"
---
# <a name="rwtexture1doperator--function"></a><span data-ttu-id="224e0-105">Функция RWTexture1D:: operator</span><span class="sxs-lookup"><span data-stu-id="224e0-105">RWTexture1D::Operator  function</span></span>

<span data-ttu-id="224e0-106">Возвращает переменную ресурса.</span><span class="sxs-lookup"><span data-stu-id="224e0-106">Returns a resource variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="224e0-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="224e0-107">Syntax</span></span>

``` syntax
R Operator[](
  in uint pos
);
```

## <a name="parameters"></a><span data-ttu-id="224e0-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="224e0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="224e0-109">*POS-терминал* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="224e0-109">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="224e0-110">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="224e0-110">Type: **uint**</span></span>

<span data-ttu-id="224e0-111">Позиция индекса.</span><span class="sxs-lookup"><span data-stu-id="224e0-111">The index position.</span></span> <span data-ttu-id="224e0-112">Содержит координату x.</span><span class="sxs-lookup"><span data-stu-id="224e0-112">Contains the x coordinate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="224e0-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="224e0-113">Return value</span></span>

<span data-ttu-id="224e0-114">Тип: **R**</span><span class="sxs-lookup"><span data-stu-id="224e0-114">Type: **R**</span></span>

<span data-ttu-id="224e0-115">Переменная ресурса.</span><span class="sxs-lookup"><span data-stu-id="224e0-115">A resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="224e0-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="224e0-116">Remarks</span></span>

<span data-ttu-id="224e0-117">Эта функция поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="224e0-117">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="224e0-118">Вершина</span><span class="sxs-lookup"><span data-stu-id="224e0-118">Vertex</span></span> | <span data-ttu-id="224e0-119">Поверхности</span><span class="sxs-lookup"><span data-stu-id="224e0-119">Hull</span></span> | <span data-ttu-id="224e0-120">Домен</span><span class="sxs-lookup"><span data-stu-id="224e0-120">Domain</span></span> | <span data-ttu-id="224e0-121">Геометрия</span><span class="sxs-lookup"><span data-stu-id="224e0-121">Geometry</span></span> | <span data-ttu-id="224e0-122">Пиксель</span><span class="sxs-lookup"><span data-stu-id="224e0-122">Pixel</span></span> | <span data-ttu-id="224e0-123">Вычисления</span><span class="sxs-lookup"><span data-stu-id="224e0-123">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="224e0-124">x</span><span class="sxs-lookup"><span data-stu-id="224e0-124">x</span></span>     | <span data-ttu-id="224e0-125">x</span><span class="sxs-lookup"><span data-stu-id="224e0-125">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="224e0-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="224e0-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="224e0-127">RWTexture1D</span><span class="sxs-lookup"><span data-stu-id="224e0-127">RWTexture1D</span></span>](sm5-object-rwtexture1d.md)
</dt> <dt>

[<span data-ttu-id="224e0-128">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="224e0-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




