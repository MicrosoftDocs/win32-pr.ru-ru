---
title: 'Функция RWTexture1DArray:: operator'
description: 'Возвращает переменную ресурса. | Функция RWTexture1DArray:: operator'
ms.assetid: 7047e670-dd78-4b73-8d80-5575e458f27c
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
ms.openlocfilehash: 6f8623ab25b42f6865e401c5b263a1774206c752
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986516"
---
# <a name="rwtexture1darrayoperator--function"></a><span data-ttu-id="17c71-105">Функция RWTexture1DArray:: operator</span><span class="sxs-lookup"><span data-stu-id="17c71-105">RWTexture1DArray::Operator  function</span></span>

<span data-ttu-id="17c71-106">Возвращает переменную ресурса.</span><span class="sxs-lookup"><span data-stu-id="17c71-106">Returns a resource variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="17c71-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="17c71-107">Syntax</span></span>

``` syntax
R Operator[](
  in uint2 pos
);
```

## <a name="parameters"></a><span data-ttu-id="17c71-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="17c71-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17c71-109">*POS-терминал* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="17c71-109">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17c71-110">Тип: **uint2**</span><span class="sxs-lookup"><span data-stu-id="17c71-110">Type: **uint2**</span></span>

<span data-ttu-id="17c71-111">Позиция индекса.</span><span class="sxs-lookup"><span data-stu-id="17c71-111">The index position.</span></span> <span data-ttu-id="17c71-112">Первый компонент содержит координату x.</span><span class="sxs-lookup"><span data-stu-id="17c71-112">The first component contains the x coordinate.</span></span> <span data-ttu-id="17c71-113">Второй компонент указывает нужный срез массива.</span><span class="sxs-lookup"><span data-stu-id="17c71-113">The second component indicates the desired array slice.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17c71-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="17c71-114">Return value</span></span>

<span data-ttu-id="17c71-115">Тип: **R**</span><span class="sxs-lookup"><span data-stu-id="17c71-115">Type: **R**</span></span>

<span data-ttu-id="17c71-116">Переменная ресурса.</span><span class="sxs-lookup"><span data-stu-id="17c71-116">A resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="17c71-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="17c71-117">Remarks</span></span>

<span data-ttu-id="17c71-118">Эта функция поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="17c71-118">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="17c71-119">Вершина</span><span class="sxs-lookup"><span data-stu-id="17c71-119">Vertex</span></span> | <span data-ttu-id="17c71-120">Поверхности</span><span class="sxs-lookup"><span data-stu-id="17c71-120">Hull</span></span> | <span data-ttu-id="17c71-121">Домен</span><span class="sxs-lookup"><span data-stu-id="17c71-121">Domain</span></span> | <span data-ttu-id="17c71-122">Геометрия</span><span class="sxs-lookup"><span data-stu-id="17c71-122">Geometry</span></span> | <span data-ttu-id="17c71-123">Пиксель</span><span class="sxs-lookup"><span data-stu-id="17c71-123">Pixel</span></span> | <span data-ttu-id="17c71-124">Вычисления</span><span class="sxs-lookup"><span data-stu-id="17c71-124">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="17c71-125">x</span><span class="sxs-lookup"><span data-stu-id="17c71-125">x</span></span>     | <span data-ttu-id="17c71-126">x</span><span class="sxs-lookup"><span data-stu-id="17c71-126">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="17c71-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="17c71-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17c71-128">RWTexture1DArray</span><span class="sxs-lookup"><span data-stu-id="17c71-128">RWTexture1DArray</span></span>](sm5-object-rwtexture1darray.md)
</dt> <dt>

[<span data-ttu-id="17c71-129">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="17c71-129">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




